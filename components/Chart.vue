<script>
import { Bar } from 'vue-chartjs';

export default {
    extends: Bar,
    name: 'chart',
    data () {
        return {
        data: {
            labels: ['2021年1月', '2021年2月', '2021年3月', '2021年4月'],
            
            datasets: [
            {
                label: 'レッスン',
                data: [108,115,135,120],
                borderWidth: 1,
                backgroundColor:'red'
            },
            {
                label: '生演奏',
                data: [6,8,7,15],
                backgroundColor: 'blue',
            }
            ]
        },
        options: {
            maintainAspectRatio: false,
            // title:{
            //     display:true,
            //     position:'top',
            //     fontSize:'20px',
            //     text:"依頼数推移"
            // },
            scales: {
            xAxes: [{
                scaleLabel: {
                display: true,
                }
            }],
            yAxes: [{
                ticks: {
                beginAtZero: true,
                stepSize: 35,
                }
            }]
            }
        }
        }
    },
    mounted () {
        this.renderChart(this.data, this.options)
    }
    }
</script>