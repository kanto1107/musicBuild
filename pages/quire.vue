<template>
    <div>
        <div style="background-color:#2e2a29;">
            <div class="d-flex" v-if="closePicker">
                <div class="servicedatePicker">
                    <div class="quireTime d-flex align-center">
                        <!-- <select name="selectBtn" v-model="selected" style="border:1px solid black">
                            <option disabled value="">サービス</option>
                            <option v-for="(value, index) in serviceData" :key="index">{{value.name}}</option>
                        </select> -->
                        <p class="pt-5 ml-1" style="color:white; width:107px;">サービス</p>
                        <v-select :items="services" label="サービス" class="selectBox" style="background-color:white; height:45px;" v-model="serviceSearch">   
                        </v-select>
                    </div>
                    <div class="untreatDate d-flex mt-5">
                        <p class="mr-10 ml-1" style="color:white;">受付日</p>
                        <datepicker :format="returnDate" class="datepicker" v-model="startDateSearch" label="yyyy/mm/dd"></datepicker>
                    </div>
                </div>
                <div>
                    <div class="custermerPicker d-flex align-center ml-8" style="height:60px;">
                        <p class="mr-5 mt-3" style="color:white;">お客様名</p>
                        <!-- <input type="text" v-model="keyword" style="border:1px solid black;" class="pb-3"> -->
                        <v-text-field v-model="custermerSearch" label="漢字カナ部分一致" style="background-color:white; height:40px;" class="pb-8">
                        </v-text-field>
                    </div>
                    <div class="untreatDate d-flex align-center ml-10 mt-5">
                        <p class="mr-7" style="color:white;">受付日</p>
                        <datepicker :format="returnDate" class="datepicker mb-2" v-model="endDateSearch"></datepicker>
                    </div>
                </div>
                <div>
                    <div class="d-flex">
                        <p class="mt-5 mx-5" style="color:white;">メールアドレス</p>
                        <v-text-field v-model="mailSearch" label="部分一致" style="background-color:white; height:40px;" class="mt-3">
                        </v-text-field>
                    </div>
                    <div>
                        <div class="d-flex mt-5 mx-5">
                            <input type="radio" id="one" value="処理" v-model="picked" class="mr-3 mt-1">
                            <label for="処理" class="mr-5" style="color:white;">処理</label>
                            <br>
                            <input type="radio" id="two" value="未処理" v-model="picked" class="mr-3 mt-1">
                            <label for="未処理" style="color:white;">未処理</label>
                        </div>
                    </div>
                </div>
                <div class="d-flex">　
                    <p class="mt-5 mx-5" style="color:white;">種類</p>
                    <v-select :items="kind" label="お問い合わせ種類" outlined class="selectBox mt-3" style="background-color:white; height:48px;" v-model="kindSearch">   
                    </v-select>
                </div>
            </div>
            <div class="d-flex justify-center">
                <v-btn color="orange" class="px-14 my-6 mr-4">検索</v-btn>
                <a class="mt-7">検索条件リセット</a>
            </div>
            <div class="d-flex justify-end">
                <v-btn @click="close" class="mr-14 mb-5">閉じる</v-btn>
            </div>
        </div>
        <div>
            <p class="red--text py-3" style="background-color:#f7b079;">４件の新しいお問い合わせがあります</p>
            <p class="ml-3">100件中6件ヒットしました。</p>
        </div>    
        <div class="mt-10">
            <v-data-table :headers="headers" :items="users" :search="search">
            </v-data-table>
        </div>
    </div>
</template>

<script>
import moment from 'moment'
import Datepicker from 'vuejs-datepicker';
export default {
    components: {
        Datepicker
    },
    data(){
        return{
            keyword:'',
            search:'',
            picked:'',
            serviceSearch:'',
            custermerSearch:'',
            startDateSearch:'',
            endDateSearch:'',
            mailSearch:'',
            kindSearch:'',
            closePicker:true,
            services:[
                '会員ページ',
                'サービス２',
                'サービス３'
            ],
            kind:[
                'ご相談',
                'タイム確認書',
                'レッスン・ベビーシッター',
                'コース変更について',
                ''
            ],
            users:[
                {
                    id:1,
                    name:'山田花子',
                    rename:'ヤマダハナコ',
                    mail:'aaa.com',
                    service:'会員ページ',
                    about:null,
                    area:'北海道',
                    time:'',
                    process:true,
                    response:'伊藤'
                },
                {
                    id:2
                },
                {
                    id:3,
                    name:'ららr',
                    rename:'あああ',
                    mail:'aaa.com',
                    service:'会員ページ',
                    about:null,
                    area:'北海道',
                    time:'11時',
                    process:true,
                    response:'伊藤'
                }
            ],

        }
    },
    methods:{
        returnDate(date){
            return moment(date).format('yyyy/M/DD');
        },
        close(){
            this.closePicker = !this.closePicker
        }
        

    },
    computed:{
        headers(){
            return [
                {
                    text:'受付番号',
                    value:'id'
                },
                {
                    text:'お客様名',
                    value:'name',
                },
                {
                    text:'フリガナ',
                    value:'rename',
                },
                {
                    text:'メールアドレス',
                    value:'mail',
                },
                {
                    text:'サービス',
                    value:'service',
                },
                {
                    text:'お問い合わせ種類',
                    value:'about'
                },
                {
                    text:'場所',
                    value:'area'
                },
                {
                    text:'受付時間',
                    value:'time'
                },
                {
                    text:'処理',
                    value:'process'
                },
                {
                    text:'担当',
                    value:'response'
                }
            ]
        }
    }
}
</script>

<style>

.quireTime{
    width:250px;
}

.datepicker{
    background-color:white;
    width:158px;
    height: 30px;
}

</style>