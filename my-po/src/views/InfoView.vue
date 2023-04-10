<template>
  <div class="w1200 ma_0a">
    <PageTitle :page_numOfChild="page_num" :page_nameOfChild="page_name"></PageTitle>
    <div class="d_flex">
        <div class="pro_container">
           <div class="profile" v-for="profile in profileList" :key="profile">
               <div class="pro_title flex_start_center">
                   <img :src="profile.titleImg">
                   <h2>{{ profile.title }}</h2>
               </div>
               <div class="pro_detail">
                   <div class="d_flex">
                       <p>{{ profile.detail_1 }}</p>
                       <p>{{ profile.detail_01 }}</p>
                   </div>
                   <div class="d_flex">
                       <p>{{ profile.detail_2 }}</p>
                       <p>{{ profile.detail_02 }}</p>
                   </div>
                   <div class="d_flex">
                       <p>{{ profile.detail_3 }}</p>
                       <p>{{ profile.detail_03 }}</p>
                   </div>
               </div>
           </div>
        </div>
        <div class="img_box">img_box</div>
    </div>
  </div>
</template>

<script>
import PageTitle from '@/components/PageTitle.vue';
export default {
    name: 'InfoView',
    components: {
      PageTitle,
    },
    data() {
      return {
        profileList:[
            {titleImg:require('../assets/image/icon/profile_icon.png'),title: 'Profile', detail_1: '이름', detail_01: '모은지', detail_2:'생년월일', detail_02: '2000.11.10', detail_3:'지역', detail_03: '인천 미추홀구'},
            {titleImg:require('../assets/image/icon/history_icon.png'),title: 'History', detail_1: '2021.04', detail_01: '블루선(온라인MD)', detail_2:'2021.12', detail_02: 'UXUI웹 퍼블리셔 양성과정 javascript심화과정', detail_3:'2022.08', detail_03: '니혼IPFS 웹퍼블리셔로 근무'},
            {titleImg:require('../assets/image/icon/contect_icon.png'),title: 'Contect', detail_1: 'Tel', detail_01: '010.8426.4029', detail_2:'Email', detail_02: 'moeunji12@gmail.com'},
        ],
        page_num : '01',
        page_name: 'My Information',
      }
    },
}
</script>

<style>
.main_title > h2 {
    color: #FF74B7;
}
.pro_container {
    width: 65%;
}
.pro_container {
    display: flex;
    flex-wrap: wrap;
}
.profile {
    margin: 0 15px;
}
</style>