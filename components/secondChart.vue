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
                label:"顧客数",
                data: [500,600,700,800],
                borderWidth: 0.4,
                backgroundColor:'blue'
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
                stepSize: 200,
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