~``<template lang="html">
  <div class="profile-area">
    <img id="profile-image" v-bind:src="defaultImage"/>
    <div class="profile-info-area">
      <div class="profile-info-top">
        <span class="profile-info-name">비어원</span>
        <ul class="profile-counting-info fa-ul">
          <li>
            <i class="fa fa-li fa-users"></i>32.1k
          </li>
          <li>
            <i class="fa fa-li fa-eye"></i>576
          </li>
          <li>
            <i class="fa fa-li fa-heart"></i>2.1K
          </li>
          <li>
            <i class="fa fa-li fa-clipboard"></i>421
          </li>
        </ul>
      </div>
      <div class="profile-info-content">
        <p>
          그냥 소소하게 이것저것 시도해보고 있습니다.<br/>
          재밌게 봐주셨으면 팔로우, 포스팅 많이 해주세요!<br/>
          가성비 오지는 요리 위주로 연구 중입니다~
        </p>
      </div>
      <div class="profile-info-buttom">
        <img class="profile-cook-thumbnail" v-bind:src="samples[0]"/>
        <img class="profile-cook-thumbnail" v-bind:src="samples[1]"/>
        <img class="profile-cook-thumbnail" v-bind:src="samples[2]"/>
      </div>
    </div>
  </div>
</template>

<script>
import defaultProfileImage from '@/assets/default-profile-image.jpg'
import sample1 from '@/assets/sample1.jpeg'
import sample2 from '@/assets/sample2.jpeg'
import sample3 from '@/assets/sample3.jpeg'

export default {
  data() {
    return {
      defaultImage: defaultProfileImage,
      samples: [
        sample1, sample2, sample3
      ]
    }
  }
}
</script>

<style lang="css" scoped>
.profile-area {
  max-width: 800px;
  height: 300px;
  margin: 10px 0px 10px 0px;
  background-color: #000;

  display: flex;
  flex-direction: row;
  justify-content: flex-start;
}

#profile-image {
  width: 200px;
}
.profile-info-area {
  background-color: black;
  flex-grow: 1;

  padding: 0px 30px 0px 30px;

  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  color: white;
}

.profile-info-top {
  display: flex;
  flex-direction: row;
  padding-bottom: 8px;

  flex-grow: 1;
  align-items: flex-end;
  border-bottom: 1px solid gray;
}
.profile-info-name {
  font-size: 30px;
}
.profile-counting-info {
  margin-left: 50px;
}
.fa-ul {
  margin-bottom: 0px;
}
.profile-counting-info > li {
  float: left;
  margin-right: 40px;
}

.profile-info-content {
  flex-grow: 2;
  border-bottom: 1px solid gray;
}

.profile-info-buttom {
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
  flex-grow: 2;
}
.profile-cook-thumbnail {
  margin: 0px 15px 0px 15px;
  width: 120px;
  height: auto;
}
</style>