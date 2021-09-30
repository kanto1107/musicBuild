<template>
    <div>
        <div class="tabBox">
            <div id="tabs" class="d-flex">
                <div class="mr-3">
                    <input type="radio" value="1" id="tab1" v-model="isActive">
                    <label for="tab1">演奏依頼</label>
                </div>
                <div class="mr-3">
                    <input type="radio" value="2" id="tab2" v-model="isActive">
                    <label for="tab2">ユニット管理</label>
                </div>
                <div>
                    <input type="radio" value="3" id="tab3" v-model="isActive">
                    <label for="tab3">会場マスタ管理</label>
                </div>
            </div>
            <ul id="contents" class="mt-5">
                <li v-if="isActive == '1'">
                    <div class="d-flex">
                        <div>
                            <div class="d-flex">
                                <p class="mt-3" style="width:95px;">依頼番号</p>
                                <input type="text" placeholder="依頼番号" style="background-color:white; height:30px; width:150px;" class="ml-3 mt-2">
                            </div>
                            <div class="d-flex">
                                <p class="mt-3" style="width:95px;">依頼者名</p>
                                <input type="text" placeholder="依頼者名" style="background-color:white; height:30px; width:150px;" class="ml-3 mt-2">
                            </div>
                            <div class="d-flex" >
                                <p class="mt-3 text-caption" style="letter-spacing:-0.1em; font-size:11px;">売り上げチェック</p>
                                <input type="radio" v-model="checkContent" value="one" class="mt-3 mx-2">
                                <label for="one" class="mt-2">売上額</label>
                                <input type="radio" v-model="checkContent" value="zero" class="mx-2 mt-3">
                                <label value="zero" class="mt-2">未入金</label>
                            </div>
                            <div class="d-flex">
                                <p class="mt-3" style="width:95px;">楽器</p>
                                <input type="text" placeholder="楽器部分一致" style="background-color:white; height:30px; width:150px;" class="ml-3 mt-2">
                            </div>
                            <div class="d-flex">
                                <p class="mt-3 mr-10">最終確認</p>
                                <div style="width:150px">
                                    <v-select :items="finalItems" class="" label="最終確認"></v-select>
                                </div>
                            </div>
                        </div>
                        <div>
                            <div class="d-flex">
                                <p class="mt-3 ml-5 mr-14">処理</p>
                                <div style="width:150px;">
                                    <v-select :items="processItems" class="pt-1" label="処理"></v-select>
                                </div>
                            </div>
                            <div class="d-flex">
                                <p class="mt-3 ml-5 mr-2">顧客番号</p>
                                <input type="text" placeholder="顧客番号" style="background-color:white; height:30px; width:150px;" class="ml-3 mt-2">
                            </div>
                            <div class="d-flex">
                                <p class="mt-3 mx-5">演奏番号</p>
                                <div style="width:150px;">
                                    <v-select :items="playContent" class="pt-1" label="演奏内容"></v-select>
                                </div>
                            </div>
                            <div class="d-flex">
                                <p class="mt-3 mx-5">顧客区分</p>
                                <div style="width:150px;">
                                    <v-select :items="custermerSeparate" class="pt-1" label="顧客区分"></v-select>
                                </div>
                            </div>
                        </div>
                        <div>
                            <div class="d-flex pt-1">
                                <p class="mt-3 ml-5 mr-10">期間</p>
                                <datepicker :format="returnDate" class="mt-3" label="yyyy/mm/dd" style="background-color:white; height:20px; display:block; font-size:11px;"></datepicker>
                            </div>
                            <div class="d-flex pt-2">
                                <p class="mt-3 ml-5 mr-2">会場名</p>
                                <input type="text" placeholder="会場名部分一致" style="background-color:white; height:30px; width:110px;" class="ml-3 mt-2">
                            </div>
                            <div class="d-flex pt-1">
                                <p class="mt-3 ml-5">演奏形態</p>
                                <div style="width:120px;">
                                    <v-select :items="playParts" class="ml-2 pt-0" label="演奏形態"></v-select>
                                </div>
                            </div>
                            <div class="d-flex mt-1">
                                <p class="ml-5 mr-2">会員番号</p>
                                <input type="text" style="background-color:white; width:110px; height:30px;" placeholder="会員番号">
                            </div>
                        </div>
                        <div>
                            <div class="d-flex">
                                <p class="mt-4 ml-5 mr-3 pl-3" style="width:60px;">~</p>
                                <div style="width:110px;">
                                    <datepicker :format="returnDate" class="mt-4" label="yyyy/mm/dd" style="background-color:white; height:20px; display:block; font-size:11px"></datepicker>
                                </div>
                            </div>
                            <div class="d-flex pt-1">
                                <p class="mt-4 ml-5" style="width:60px;">担当</p>
                                <div style="width:130px;">
                                    <v-select :items="playParts" class="ml-2 pt-0" label="担当"></v-select>
                                </div>
                            </div>
                            <div class="d-flex pt-1">
                                <p class="mt-3 ml-5" style="width:70px;">備考</p>
                                <input type="text" style="background-color:white; width:120px; height:30px;" placeholder="備考">
                            </div>
                            <div class="d-flex pt-1">
                                <p class="mt-3 ml-5 mr-3">顧客TEL</p>
                                <input type="text" style="background-color:white; width:120px; height:30px;" placeholder="顧客TEL">
                            </div>
                        </div>
                    </div>
                    <div>

                    </div>
                </li>
        
                <li v-else-if="isActive == '2'">
                    <p class="title">テスト2</p>
                    <p>テスト本文2テスト本文2テスト本文2テスト本文2テスト本文2<br>
                    テスト本文2テスト本文2テスト本文2テスト本文2テスト本文2テスト本文2</p>
                </li>
        
                <li v-else-if="isActive == '3'">
                    <p class="title">テスト3</p>
                    <p>テスト本文3テスト本文3テスト本文3テスト本文3テスト本文3<br>
                    テスト本文3テスト本文3テスト本文3テスト本文3テスト本文3テスト本文3</p>
                </li>
            </ul>
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
            isActive:'1',
            finalItems:[
                '確認１',
                '確認２',
                '確認３'
            ],
            processItems:[
                '処理１',
                '未処理'
            ],
            checkContent:'',
            playContent:[
                'ミニコンサート',
                '結婚式',
                'イベント'
            ],
            custermerSeparate:[
                'aa',
                'bb',
                'cc'
            ],
            playParts:[
                'カルテット',
                'オンライン',
                'ソロ',
                'その他'
            ]
        }
    },
    methods:{
        returnDate(date){
            return moment(date).format('yyyy/M/DD');
        },
    }
}
</script>

<style>
ul{
    list-style: none;
}

#tabs input {
    display: none;
}
#tabs label {
    display: block;
    width: 180px;
    text-align: center;
    transition: 0.3s;
    border-radius: 10px;
}
#tabs input:checked + label,
#tabs label:hover {
    background: gray;
    color: #fff;
}
#contents {
    width: 100%;
    
    background-color: gray;
}


</style>