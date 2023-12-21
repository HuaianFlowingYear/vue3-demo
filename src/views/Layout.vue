<script setup>
import {
  UserOutlined,
  LockOutlined,
  UnlockOutlined,
  MailOutlined,
} from "@ant-design/icons-vue";
import { ref } from "vue";
const formState = ref({
  username: "",
  password: "",
  remember: true,
});

console.log(formState);
</script>
<template>
  <div class="wrapper">
    <div class="content">
      <div class="icons">
        <svg
          data-v-37dfd6fc=""
          viewBox="0 0 24 24"
          fill="none"
          style="font-size: 30px; height: 30px"
        >
          <path
            data-v-37dfd6fc=""
            fill-rule="evenodd"
            clip-rule="evenodd"
            d="M12 21a9 9 0 100-18 9 9 0 000 18zm0-4.737a4.263 4.263 0 100-8.526 4.263 4.263 0 000 8.526z"
            fill="#165DFF"
          ></path>
          <path
            data-v-37dfd6fc=""
            fill-rule="evenodd"
            clip-rule="evenodd"
            d="M16.263 7.737H21v4.353l-.013.384h-4.75c.024-.237.026-.41.026-.41V7.737zM11.526 3.013c.207-.01.402-.013.402-.013h4.335v4.737h-4.35s-.202.004-.387.025v-4.75z"
            fill="#165DFF"
          ></path>
          <path data-v-37dfd6fc="" fill="#16D2AC" d="M15 3h6v6h-6z"></path>
        </svg>
        <span>Arco</span>
      </div>
      <div class="block">
        <a-form name="normal_login" class="min-w-[320px]">
          <a-form-item
            name="username"
            :rules="[{ required: true, message: '请输入用户名' }]"
          >
            <a-input placeholder="请输入用户名">
              <template #prefix>
                <UserOutlined class="site-form-item-icon" />
              </template>
            </a-input>
          </a-form-item>
          <a-form-item
            name="username"
            :rules="[{ required: true, message: '请输入邮箱' }]"
          >
            <a-input placeholder="请输入邮箱">
              <template #prefix>
                <!--  -->
                <MailOutlined class="site-form-item-icon" />
                <!-- <UserOutlined class="site-form-item-icon" /> -->
              </template>
            </a-input>
          </a-form-item>
          <a-form-item
            name="password"
            :rules="[{ required: true, message: '密码不能少于六位数' }]"
          >
            <a-input-password placeholder="请输入密码">
              <template #prefix>
                <!-- <MailOutlined class="site-form-item-icon" /> -->
                <!-- <UnlockOutlined /> -->
                <LockOutlined class="site-form-item-icon" />
              </template>
            </a-input-password>
          </a-form-item>
          <a-form-item
            name="username"
            :rules="[{ required: true, message: '两次密码得一致' }]"
          >
            <a-input placeholder="请确认密码">
              <template #prefix>
                <UnlockOutlined class="site-form-item-icon" />
                <!-- <UnlockOutlined class="site-form-item-icon" /> -->
                <!-- <a-icon type="user" class="site-form-item-icon" /> -->
              </template>
            </a-input>
          </a-form-item>

          <div class="flex justify-between items-center">
            <a-form-item>
              <a-button type="primary" html-type="submit" class="w-[12vw]">
                注册
              </a-button>
            </a-form-item>
            <a-form-item>
              <a-button html-type="submit" class="w-[12vw]"> 去登录</a-button>
            </a-form-item>
          </div>
        </a-form>
      </div>
    </div>
  </div>
</template>
<style scoped lang="less">
.wrapper {
  display: flex;
  height: 100vh;
  background-image: url(https://gw.alipayobjects.com/zos/rmsportal/TVYTbAXWheQpRcWDaDMu.svg);
  background-repeat: no-repeat;
  background-position: center 110px;
  background-size: 100%;
  .content {
    position: relative;
    display: flex;
    flex: 1;
    align-items: center;
    justify-content: center;
    padding-bottom: 40px;
    .icons {
      position: fixed;
      top: 24px;
      left: 22px;
      z-index: 1;
      display: inline-flex;
      align-items: center;
      span {
        font-size: 20px;
      }
    }
  }
}
</style>
