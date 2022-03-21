<script setup>
import { ref } from "vue";

const passIcon = ref("pi pi-eye");
const inputPassword = ref("");

const togglePassIcon = () => {
  passIcon.value =
    passIcon.value == "pi pi-eye" ? "pi pi-eye-slash" : "pi pi-eye";
};
</script>

<template>
  <div
    style="height: 100vh"
    class="flex justify-content-center flex-wrap card-container align-content-center scalein animation-duration-500"
  >
    <Card style="width: 20rem" class="border-noround">
      <template #header>
        <div class="flex flex-column justify-content-center flex-wrap">
          <div class="text-5xl text-center">Welcome to Tambangku</div>
          <div class="flex align-items-center justify-content-center">
            <img style="width: 40%" src="/Login/logo.png" />
          </div>
        </div>
      </template>
      <template #content>
        <div class="flex flex-column">
          <InputText
            placeholder="Username"
            id="username"
            type="text"
            class="mb-3 block border-round"
          />
          <div class="flex p-input-icon-right">
            <InputText
              placeholder="Password"
              id="password"
              :type="passIcon == 'pi pi-eye' ? 'password' : 'text'"
              class="flex-grow-1 flex-shrink-1"
              v-model="inputPassword"
            />

            <i :class="passIcon" @click="togglePassIcon()" />
          </div>
          <small class="mb-3"><a href="">Forgot password ?</a></small>
          <Button
            label="Login"
            style="color: #ffffff"
            class="block p-button mb-1 login-button"
          />
        </div>
      </template>
    </Card>
    <Card style="width: 20rem" class="border-noround opacity-70">
      <template #header>
        <div
          class="flex flex-column justify-content-center flex-wrap opacity-100"
        >
          <div class="text-5xl text-center">Welcome to Tambangku</div>
          <div class="flex align-items-center justify-content-center">
            <img style="width: 40%" src="/Login/logo.png" />
          </div>
        </div>
      </template>
      <template #content>
        <div class="flex flex-column">
          <InputText
            placeholder="Username"
            id="username"
            type="text"
            class="mb-3 block border-round"
          />
          <div class="flex p-input-icon-right">
            <InputText
              placeholder="Password"
              id="password"
              :type="passIcon == 'pi pi-eye' ? 'password' : 'text'"
              class="flex-grow-1 flex-shrink-1"
              v-model="inputPassword"
            />

            <i :class="passIcon" @click="togglePassIcon()" />
          </div>
          <small class="mb-3"><a href="">Forgot password ?</a></small>
          <Button label="Login" class="block p-button mb-1" />
        </div>
      </template>
    </Card>
  </div>
</template>

<style>
body {
  background: rgb(2, 0, 36);
  background: linear-gradient(
    106deg,
    rgba(2, 0, 36, 1) 0%,
    rgba(35, 35, 195, 1) 55%,
    rgba(0, 212, 255, 1) 100%
  );
}
</style>
