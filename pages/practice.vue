<template>
    <div>
        <div id="tabBox">
            <div id="tabs">
                <input type="radio" value="1" id="tab1" v-model="isActive">
                <label for="tab1">タブ1</label>
        
                <input type="radio" value="2" id="tab2" v-model="isActive">
                <label for="tab2">タブ2</label>
        
                <input type="radio" value="3" id="tab3" v-model="isActive">
                <label for="tab3">タブ3</label>
            </div>
            <ul id="contents">
                <li v-if="isActive == '1'">
                    <p class="title">テスト</p>
                    <p>テスト本文テスト本文テスト本文テスト本文テスト本文<br>
                    テスト本文テスト本文テスト本文テスト本文テスト本文テスト本文</p>
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
export default {
    data(){
        return{
            isActive: '1',
        }
    }
}
</script>
<style>
#tabs {
    overflow: hidden;
}
 
#tabs input {
  display: none;
}
 
#tabs label {
    display: inline-block;
    line-height: 40px;
    width: 120px;
    text-align: center;
    cursor: pointer;
    background: #eee;
    transition: 0.3s;
    border-radius: 10px 10px 0 0;
}
 
#tabs input:checked + label,
#tabs label:hover {
    background: #56B4BE;
    color: #fff;
}
 
#contents {
    width: 500px;
    height: 90px;
    padding: 5px 10px;
    box-shadow: 1px 1px 1px 0 rgba(0,0,0,0.2);
    border: 1px solid #eee;
    border-top: 2px solid #56B4BE;
}
 
#contents p {
  font-size: 15px;
  margin: 0;
}
 
#contents p.title {
  font-size: 16px;
  font-weight: bold;
}
</style>