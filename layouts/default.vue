<template>
  <v-app style="background-color:#F5F5F5;">
    <v-navigation-drawer
      v-model="drawer"
      :mini-variant="miniVariant"
      :clipped="clipped"
      fixed
      app
    >
      <v-list>
        <v-list-item
          v-for="(item, i) in items"
          :key="i"
          :to="item.to"
          router
          exact
        >
          <v-list-item-content>
            <v-list-item-title v-text="item.title" />
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
    <v-app-bar
      :clipped-left="clipped"
      value
      fixed
      app
    >

      <v-toolbar-title v-text="title" />
      <v-app-bar-nav-icon @click.stop="drawer = !drawer" />
      <v-spacer />
      2021年6月1日　月曜日　12時30分59秒　　|　　　
      <v-icon>mdi-account-group-outline</v-icon>
      　徳増若菜　
      <v-menu offset-y>
        <template v-slot:activator="{ on }">
          <v-icon v-on="on">mdi-arrow-down-drop-circle</v-icon>
        </template>
        <v-list>
          <v-list-item v-for="(Ntitles, index) in Ntitle" :key="index">
            <v-list-item-title>{{Ntitles.name_title}}</v-list-item-title>
          </v-list-item>
        </v-list>
      </v-menu>
    </v-app-bar>
    <v-main>
      <v-container>
        <Nuxt />
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
export default {
  data () {
    return {
      clipped: false,
      drawer: false,
      fixed: false,
      items: [
        {
          title: 'ホーム',
          to: '/'
        },
        {
          title: 'お問い合わせ管理',
          to: '/quire'
        },
        {
          title: '演奏依頼',
          to: '/musicRequest'
        },
        {
          title: 'レッスン依頼',
          to: '/inspire'
        },
        {
          title: 'パッケージ管理',
          to: '/inspire'
        },
        {
          title: '顧客管理',
          to: '/inspire'
        },
        {
          title: '会員管理',
          to: '/inspire'
        },
        {
          title: 'メール管理',
          to: '/inspire'
        },
        {
          title: '業務管理',
          to: '/inspire'
        },
        {
          title: '営業管理',
          to: '/inspire'
        },
        {
          title: '設定（Admin）',
          to: '/inspire'
        },
        {
          title: '経理（Admin）',
          to: '/inspire'
        },
        {
          title: 'MESPO',
          to: '/inspire'
        }
      ],
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: '音楽家派遣運用管理',
      Ntitle:[
        { name_title:'aaa'},
        { name_title:'bbb'}
      ]
    }
  }
}
</script>
