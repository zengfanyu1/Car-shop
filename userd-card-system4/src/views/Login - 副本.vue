<template>
  <div class="login">
    <van-nav-bar title="登录" />
    <van-cell-group class="cardGroups">
      <van-field
        :value="username"
        label="用户名:"
        icon="question-o"
        placeholder="请输入用户名"
        bind:click-icon="onClickIcon"
      />
      <van-field :value="password" type="password" label="密码:" placeholder="请输入密码" />
    </van-cell-group>
    <van-button class="cardBtn" type="default" size="normal" @click="ToHome">登陆</van-button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      username: "",
      password: ""
    };
  },
  methods: {
    onChange(event) {
      // event.detail 为当前输入的值
      console.log(event.detail);
    },
      ToHome() {
        this.$router.push("/")
      }
  }
};
</script>

<style lang="scss" scoped>
.cardGroups {
  margin-top: 1rem;
}
.cardBtn {
  width: 5rem;
  margin-top: 0.5rem;
}
</style>