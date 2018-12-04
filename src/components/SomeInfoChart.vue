<script>
import { Line } from 'vue-chartjs'

export default {
  extends: Line,
  props: ['title'],
  methods: {
      refresh: function(labels, highPressure, lowPressure) {
            let self = this;
            this.renderChart({
                labels: labels,
                datasets: [
                    {
                        label: 'High Pressure',
                        backgroundColor: 'rgb(153, 0, 0)',
                        borderColor: 'rgb(153, 0, 0)',
                        data: highPressure,
                        borderWidth: 2,
                        fill: false,
                        lineTension: 0,
                    },
                    {
                        label: 'Low Pressure',
                        backgroundColor: 'rgb(51, 51, 153)',
                        borderColor: 'rgb(51, 51, 153)',
                        data: lowPressure,
                        borderWidth: 2,
                        fill: false,
                        lineTension: 0,
                    }
                ]
            }, 
        {responsive: true, maintainAspectRatio: false})    
    }
  },
  mounted () {
      this.refresh(["L" , "M", "M", "J", "V", "S", "D"], [8, 9, 8, 7, 6, 7, 7], [11, 11, 13, 12, 11, 13, 10]);  
  }, 
}
</script>