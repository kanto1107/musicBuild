<script>
import { Bar } from 'vue-chartjs';

export default {
    extends: Bar,
    name: 'secondChart',
    data () {
        return {
        data: {
            labels: ['2021年1月', '2021年2月', '2021年3月', '2021年4月'],
            
            datasets: [
            {
                label:"会員数",
                data: [150,200,210,220],
                borderWidth: 0,
                backgroundColor:'green'
            },
            ]
        },
        options: {
            maintainAspectRatio: false,
            scales: {
            xAxes: [{
                scaleLabel: {
                display: true,
                }
            }],
            yAxes: [{
                ticks: {
                beginAtZero: true,
                stepSize: 60,
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