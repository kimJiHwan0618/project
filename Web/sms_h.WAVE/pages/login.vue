<template>
  <div class="login__wrap">
    <div class="login__wrap__inner">
      <div class="inner__left">
        <h1><img src="@/assets/img/logo_b.png" alt="h.WAVE logo" /></h1>
        <h2 class="f-midium">Login to Your Account</h2>
        <form action="">
          <ul>
            <li>
              <input class="__input __text" type="email" placeholder="Email" />
            </li>
            <li>
              <input
                class="__input __text"
                type="password"
                placeholder="Password"
              />
            </li>
            <li>
              <span>
                <input type="checkbox" name="loginRemember" id="loginCheck" />
                <label for="loginCheck">Remember me</label>
              </span>
              <a href="#" class="f-midium">Forgot password?</a>
            </li>
            <li>
              <input class="__input f-midium" type="submit" value="Login" />
            </li>
          </ul>
        </form>
        <p>
          Don't have an account yet? <a href="#" class="f-midium">Sign Up</a>
        </p>
      </div>
      <div class="inner__right">
        <dl>
          <dt class="f-bold">All in this hingomWAVE</dt>
          <dd>
            Sales collection and analysis solution base on Cloud With
            hingomWAVE, experience efficient item sales management, stock
            management, customer management and intelliectual sales management.
          </dd>
        </dl>
      </div>
    </div>
  </div>
</template>

<script>
import { defineComponent } from '@vue/composition-api';
export default defineComponent({
  setup() {
    return {};
  },
});
</script>
