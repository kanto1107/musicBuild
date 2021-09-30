<template>
  <div>
    <section id="firstBox" style="background-color:white;">
      <p class="pt-5 pl-3">お問い合わせ・業務状況</p>
      <div class="d-flex justify-space-between pb-3 px-5">
        <v-card color="orange darken-1" class="mr-10" style="width:15%;">
          <v-card-title style="color:white; width:100%;" class="cardWrap text-subtitle-1">お客様から</v-card-title>
          <div class="d-flex justify-center pb-5">
            <v-card-action class="d-flex justify-center" style="background-color:#FFE0B2; width:150px; height:100px;">
              <v-card-text>
                <div class="d-flex">
                  <p style="color:red;">新着</p>
                  <v-spacer />
                  <a style="color:red;">2</a>
                </div>
                <div class="d-flex">
                  <p>未対応</p>
                  <v-spacer />
                  <a style="color:black;">2</a>
                </div>
              </v-card-text>
            </v-card-action>
          </div>
        </v-card>
        <v-card color="blue-grey darken-2 mr-10" style="width:15%;">
          <v-card-title style="color:white; width:100%;" class="cardWrap text-subtitle-1">会員様から</v-card-title>
          <div class="d-flex justify-center pb-5">
            <v-card-action class="d-flex justify-center" style="background-color:#CFD8DC; width:150px; height:100px;">
              <v-card-text>
                <div class="d-flex">
                  <p style="color:red;">新着</p>
                  <v-spacer />
                  <a style="color:red;">2</a>
                </div>
                <div class="d-flex">
                  <p>未対応</p>
                  <v-spacer />
                  <a style="color:black;">2</a>
                </div>
              </v-card-text>
            </v-card-action>
          </div>
        </v-card>
        <v-card color="lime darken-3" class="mr-10" style="width:15%;">
          <v-card-title style="color:white; width:110%;" class="cardWrap text-subtitle-1">パッケージ商品</v-card-title>
          <div class="d-flex justify-center pb-5">
            <v-card-action class="d-flex justify-center" style="background-color:#F0F4C3; width:150px; height:100px;">
              <v-card-text>
                <div class="d-flex">
                  <p style="color:red;">新着</p>
                  <v-spacer />
                  <a style="color:red;">2</a>
                </div>
                <div class="d-flex">
                  <p>未対応</p>
                  <v-spacer />
                  <a style="color:black;">2</a>
                </div>
              </v-card-text>
            </v-card-action>
          </div>
        </v-card>
        <v-card color="cyan darken-4" class="mr-10" style="width:15%;">
          <v-card-title style="color:white; width:100%;" class="cardWrap text-subtitle-1">おっかけ状況</v-card-title>
          <div class="d-flex justify-center pb-5">
            <v-card-action class="d-flex justify-center" style="background-color:#B2EBF2; width:150px; height:100px;">
              <v-card-text>
                <div class="d-flex">
                  <p style="color:red;">新着</p>
                  <v-spacer />
                  <a style="color:red;">2</a>
                </div>
                <div class="d-flex">
                  <p>未対応</p>
                  <v-spacer />
                  <a style="color:black;">2</a>
                </div>
              </v-card-text>
            </v-card-action>
          </div>
        </v-card>
        <v-card color="red darken-4" style="width:15%;">
          <v-card-title style="color:white; width:100%;" class="cardWrap text-subtitle-1">業務報告状況</v-card-title>
          <div class="d-flex justify-center pb-5">
            <v-card-action class="d-flex justify-center" style="background-color:#EF9A9A; width:150px; height:100px;">
              <v-card-text>
                <div class="d-flex">
                  <p style="color:red;">新着</p>
                  <v-spacer />
                  <a style="color:red;">2</a>
                </div>
                <div class="d-flex">
                  <p>未対応</p>
                  <v-spacer />
                  <a style="color:black;">2</a>
                </div>
              </v-card-text>
            </v-card-action>
          </div>
        </v-card>
      </div>
    </section>
    <section id="secondBox" class="mt-10" style="background-color:white;">
      <p class="pt-5 pl-3">レッスン依頼から完了までの状況</p>
      <div class="d-flex mx-5 pb-3 justify-space-between">
        <v-card color="grey lighten-1" style="width:15%;">
          <v-card-title style="color:white; width:100%;" class="cardWrap text-subtitle-1">依頼数</v-card-title>
          <div class="d-flex justify-center pb-5">
            <v-card-action class="d-flex justify-center align-center" style="background-color:white; width:150px; height:100px;">
              <v-card-text>
                <div class="d-flex">
                  <p >件数</p>
                  <v-spacer />
                  <a style="color:black;">１０</a>
                </div>
              </v-card-text>
            </v-card-action>
          </div>
        </v-card>
        <v-card color="grey darken-1" style="width:15%;">
          <v-card-title style="color:white; width:100%;" class="cardWrap text-subtitle-1">アサイン状況</v-card-title>
          <div class="d-flex justify-center pb-5">
            <v-card-action class="d-flex justify-center align-center" style="background-color:white; width:150px; height:100px;">
              <v-card-text>
                <div class="d-flex">
                  <p style="color:red;">完了</p>
                  <v-spacer />
                  <a style="color:black;">2</a>
                </div>
                <div class="d-flex">
                  <p>未完了</p>
                  <v-spacer />
                  <a style="color:black;">2</a>
                </div>
              </v-card-text>
            </v-card-action>
          </div>
        </v-card>
        <v-card color="grey darken-3" style="width:15%;">
          <v-card-title style="color:white; width:120%;" class="cardWrap text-subtitle-1">初回日決定状況</v-card-title>
          <div class="d-flex justify-center pb-5">
            <v-card-action class="d-flex justify-center align-center" style="background-color:white; width:150px; height:100px;">
              <v-card-text>
                <div class="d-flex">
                  <p style="color:black;">完了</p>
                  <v-spacer />
                  <a style="color:black;">2</a>
                </div>
                <div class="d-flex">
                  <p>未完了</p>
                  <v-spacer />
                  <a style="color:red;">2</a>
                </div>
              </v-card-text>
            </v-card-action>
          </div>
        </v-card>
        <v-card color="grey darken-4" style="width:15%;">
          <v-card-title style="color:white; width:100%;" class="cardWrap text-subtitle-1">体験実施状況</v-card-title>
          <div class="d-flex justify-center pb-5">
            <v-card-action class="d-flex justify-center align-center" style="background-color:white; width:150px; height:100px;">
              <v-card-text>
                <div class="d-flex">
                  <p style="color:black;">完了</p>
                  <v-spacer />
                  <a style="color:red;">2</a>
                </div>
                <div class="d-flex">
                  <p>キャンセル</p>
                  <v-spacer />
                  <a style="color:red;">2</a>
                </div>
              </v-card-text>
            </v-card-action>
          </div>
        </v-card>
        <v-card color="black" style="width:15%;">
          <v-card-title style="color:white; width:100%;" class="cardWrap text-subtitle-1">体験完了状況</v-card-title>
          <div class="d-flex justify-center pb-5">
            <v-card-action class="d-flex justify-center align-center" style="background-color:white; width:150px; height:100px;">
              <v-card-text>
                <div class="d-flex">
                  <p style="color:black;">完了</p>
                  <v-spacer />
                  <a style="color:red;">2</a>
                </div>
                <div class="d-flex">
                  <p>未完了</p>
                  <v-spacer />
                  <a style="color:red;">2</a>
                </div>
              </v-card-text>
            </v-card-action>
          </div>
        </v-card>
      </div>
    </section>
    <section id="thirdBox" class="mt-10 py-5 px-3" style="background-color:white;">
      <p>起床・到着完了一覧</p>
      <!-- <template class="text-left"> -->
        <!-- <v-container> -->
          <v-data-table :headers="headers" :items="items">
            <template #item.area="{ item }">
              <div style="white-space: pre;">{{ item.area }}</div>
            </template>
            <template #item.pro="{ item }">
              <div style="white-space: pre;">{{ item.pro }}</div>
            </template>
          </v-data-table>
        <!-- </v-container> -->
      <!-- </template>  -->
    </section>
    <section id="fourthBox" style="background-color:white;" class="mt-10">
      <p class="pt-5 pl-3">生演奏依頼から完了までの状況</p>
      <div class="d-flex mx-5 pb-3 justify-space-between">
        <v-card color="grey lighten-1" style="width:15%;">
          <v-card-title style="color:white; width:100%;" class="cardWrap text-subtitle-1">依頼数</v-card-title>
          <div class="d-flex justify-center pb-5">
            <v-card-action class="d-flex justify-center align-center" style="background-color:white; width:150px; height:100px;">
              <v-card-text>
                <div class="d-flex">
                  <p >件数</p>
                  <v-spacer />
                  <a style="color:black;">１０</a>
                </div>
              </v-card-text>
            </v-card-action>
          </div>
        </v-card>
        <v-card color="grey darken-1" style="width:15%;">
          <v-card-title style="color:white; width:100%;" class="cardWrap text-subtitle-1">受付状況</v-card-title>
          <div class="d-flex justify-center pb-5">
            <v-card-action class="d-flex justify-center align-center" style="background-color:white; width:150px; height:100px;">
              <v-card-text>
                <div class="d-flex">
                  <p style="color:red;">完了</p>
                  <v-spacer />
                  <a style="color:black;">2</a>
                </div>
                <div class="d-flex">
                  <p>未完了</p>
                  <v-spacer />
                  <a style="color:black;">2</a>
                </div>
              </v-card-text>
            </v-card-action>
          </div>
        </v-card>
        <v-card color="grey darken-3" style="width:15%;">
          <v-card-title style="color:white; width:110%;" class="cardWrap text-subtitle-1">見積書など状況</v-card-title>
          <div class="d-flex justify-center pb-5">
            <v-card-action class="d-flex justify-center align-center" style="background-color:white; width:150px; height:100px;">
              <v-card-text>
                <div class="d-flex">
                  <p style="color:red;">完了</p>
                  <v-spacer />
                  <a style="color:black;">2</a>
                </div>
                <div class="d-flex">
                  <p>未完了</p>
                  <v-spacer />
                  <a style="color:red;">2</a>
                </div>
              </v-card-text>
            </v-card-action>
          </div>
        </v-card>
        <v-card color="grey darken-4" style="width:15%;">
          <v-card-title style="color:white; width:120%;" class="cardWrap text-subtitle-1">演奏者など状況</v-card-title>
          <div class="d-flex justify-center pb-5">
            <v-card-action class="d-flex justify-center align-center" style="background-color:white; width:150px; height:100px;">
              <v-card-text>
                <div class="d-flex">
                  <p style="color:red;">完了</p>
                  <v-spacer />
                  <a style="color:red;">2</a>
                </div>
                <div class="d-flex">
                  <p>キャンセル</p>
                  <v-spacer />
                  <a style="color:red;">2</a>
                </div>
              </v-card-text>
            </v-card-action>
          </div>
        </v-card>
        <v-card color="black" style="width:15%;">
          <v-card-title style="color:white; width:100%;" class="cardWrap text-subtitle-1">最終確認状況</v-card-title>
          <div class="d-flex justify-center pb-5">
            <v-card-action class="d-flex justify-center align-center" style="background-color:white; width:150px; height:100px;">
              <v-card-text>
                <div class="d-flex">
                  <p style="color:red;">完了</p>
                  <v-spacer />
                  <a style="color:red;">2</a>
                </div>
                <div class="d-flex">
                  <p>未完了</p>
                  <v-spacer />
                  <a style="color:red;">2</a>
                </div>
              </v-card-text>
            </v-card-action>
          </div>
        </v-card>
      </div>
    </section>
    <section id="fifthBox" class="d-flex">
      <div id="requestIncrease" class="mt-10 mr-auto" style="background-color:white; width:30%;">
        <p class="text-h5 pt-3 pl-3">依頼数推移</p>
        <template>
          <chart class="pa-3"></chart>
        </template>
      </div>
      <div id="custermerIncrease" class="mt-10 mr-auto" style="background-color:white; width:30%;">
        <p class="text-h5 pt-3 pl-3">顧客数推移</p>
        <template>
          <secondChart class="pa-3"></secondChart>
        </template>
      </div>
      <div id="memberIncrease" class="mt-10" style="background-color:white; width:30%;">
        <p class="text-h5 pt-3 pl-3">会員数推移</p>
        <template>
          <thirdChart class="pa-3"></thirdChart>
        </template>
      </div>
    </section>
  </div>
</template>

<script>
import Chart from '~/components/Chart.vue';
import secondChart from '~/components/secondChart.vue';
import thirdChart from '~/components/thirdChart.vue';
export default {
  components: {
    Chart,
    secondChart,
    thirdChart
  },
  data(){
    return{
      width:300,

      headers:[
        {
          text:'日時',
          value:'time'
        },
        {
          text:'会場',
          value:'area'
        },
        {
          text:'代表者',
          value:'pro'
        },
        {
          text:'起床確認',
          value:'up'
        },
        {
          text:'到着確認',
          value:'arrival'
        }

      ],
      items:[
        {
          'time':'2021/6/5 12:00',
          'area':'ハイアットリージェンシー大阪\r\n06-1234-5678',
          'pro': "大村　明子\r\n080-1234-5678",
          'up':'5/5',
          'arrival':'3/5'
        },
        {
          'time':'2021/6/3010:00',
          'area':'リッツカールトン\r\n06-2345-7890',
          'pro': '浅井　久美子\r\n090-1234-5678',
          'up':'0/5',
          'arrival':'0/5'
        }
      ],
    }
  },

  methods:{

  },
  computed:{
    chartbox(){
      return{
        width: `${this.width}px`,
      }
    }
  }
}
</script>

<style>


</style>
