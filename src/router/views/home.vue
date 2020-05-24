<template>
  <div
    class="h-screen flex w-full bg-img vx-row no-gutter items-center justify-center"
    id="page-login"
  >
    <div class="vx-col sm:w-1/2 md:w-1/2 lg:w-3/4 xl:w-3/5 sm:m-0 ">
      <vx-card>
        <div slot="no-body" class="full-page-bg-color">
          <div class="vx-row no-gutter justify-center items-center">
            <div class="vx-col sm:w-full md:w-full lg:block lg:w-1/2 ">
              <img
                src="@assets/images/pages/login.png"
                alt="register"
                class="w-full object-cover mx-auto"
              />
            </div>
            <div
              class="vx-col sm:w-full md:w-full lg:w-1/2 d-theme-dark-bg h-36"
            >
              <div class="p-8">
                <div class="vx-card__title mb-8">
                  <h4 class="mb-4">Login</h4>
                  <p>Welcome back, please login to your account.</p>
                </div>
                <vs-input
                  name="phoneNumber"
                  icon="icon icon-user"
                  icon-pack="feather"
                  label-placeholder="Mobile"
                  v-model="phoneNumber"
                  @input="$v.phoneNumber.$touch()"
                  class="w-full no-icon-border"
                />
                <span
                  v-if="!$v.phoneNumber.required && $v.phoneNumber.$dirty"
                  class="text-danger text-sm"
                >
                  phoneNumber is required.
                </span>

                <vs-input
                  type="password"
                  name="password"
                  icon="icon icon-lock"
                  icon-pack="feather"
                  label-placeholder="Password"
                  v-model="password"
                  @input="$v.password.$touch()"
                  class="w-full mt-6 no-icon-border"
                />
                <span v-if="$v.password.$error" class="text-danger text-sm">
                  Password is required.
                </span>

                <div class="flex flex-wrap justify-between my-5">
                  <vs-checkbox v-model="checkbox_remember_me" class="mb-3"
                    >Remember Me</vs-checkbox
                  >
                  <router-link
                    >Forgot Password?</router-link
                  >
                </div>
                <div class="flex justify-between">
                  <vs-button @click="">Register</vs-button>
                  <vs-button @click="">Login</vs-button>
                </div>

                <div class="flex flex-wrap justify-between items-center">
                  <div class="w-full text-center mb-4">
                    <p>Want to Register as a bussiness partner ?</p>
                  </div>
                  <div class="w-full ">
                    <vs-button
                      @click=""
                      class="w-full"
                      color="#eb5424"
                      >Register Bussiness</vs-button
                    >
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </vx-card>
    </div>
  </div>
</template>

<script>
import { required } from 'vuelidate/lib/validators'
export default {
  page: {
    title: 'Home',
    meta: [{ name: 'description', content: 'Home' }],
  },
  data() {
    return {
      phoneNumber: '9876543210',
      password: 'demodemo',
      checkbox_remember_me: false,
    }
  },

  computed: {},
  methods: {
  },
  validations: {
    phoneNumber: {
      required,
    },
    password: {
      required,
    },
  },
}
</script>

<style lang="scss" scoped>
#page-login {
  .social-login {
    .bg-facebook {
      background-color: #1551b1;
    }
    .bg-twitter {
      background-color: #00aaff;
    }
    .bg-google {
      background-color: #4285f4;
    }
    .bg-github {
      background-color: #333;
    }
  }
}
.h-36 {
  height: 36rem;
}
</style>
