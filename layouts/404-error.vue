<template>
  <NuxtLayout name="default">
    <article class="page-404">
      <div class="page-404__content">
        <div class="page-404__line-back">
          <div class="page-404__error-message-container">
            <h1 class="page-404__error-message">Page not found </h1>
          </div>
          <div class="page-404__button-container">
            <bx-btn class="page-404__button" href="/">
              Go to dashboard <IconGo slot="icon" />
            </bx-btn>
          </div>
        </div>
        <div class="page-404__img-container">
          <img class="page-404__img" src="/images/error_page/error-bg.38367ed.svg">
        </div>
    </div>
</article>
  </NuxtLayout>
</template>
<script lang="ts" setup>

import '@carbon/web-components/es/components/button/index.js'
import '@carbon/web-components/es/components/link/index.js'
import IconGo from '@carbon/icons-vue/es/arrow--right/16'

</script>
<style lang="scss" scoped>
@use '~/assets/scss/carbon.scss'
.page-404 {
    @include carbon.breakpoint-down(xlg) {
        padding: carbon.$spacing-10 carbon.$spacing-12;
    }
    @include carbon.breakpoint-down(lg) {
        padding: carbon.$spacing-09 carbon.$spacing-07;
    }
    @include carbon.breakpoint-down(md) {
        position: relative;
        display: grid;
        flex-direction: row;
        grid-template-rows: auto 1fr;
        grid-template-columns: 1fr 1fr;
        gap: 0;
        padding-right: 0;
        padding-left: carbon.$spacing-05;
    }
    @include carbon.breakpoint-down(sm) {
        display: flex;
        flex-direction: column;
        padding: carbon.$spacing-06 carbon.$spacing-05;
    }
    padding-top: 3rem;
    width: 100%;
    background-color: rgb(38 38 38);
    height: 100%;
    &__line-back {
        width: 2rem;
        height: 0.125rem;
        background-color: #4589ff;
    }
    &__content {
        margin-top: 3rem;
        margin-left: 3rem;
        @include carbon.breakpoint-up(md) {
            position: absolute;
        }
    }
    &__error-message-container{
        margin: 1.5rem 0 1.5rem 0;
    }
    &__error-message {
        color: #f4f4f4;
        font-size: 2rem;
        font-weight: 400;
        letter-spacing: 0;
        line-height: 1.25;
    }
    &__button-container {
        margin-top: 3rem;
    }
    &__button {
        justify-content: space-between;
        font-size: 1rem;
        background-color: #0f62fe;
    }
    &__img-container {
        margin-top: 3rem;
        display: flex;
        justify-content: right;
        align-items: right;
        margin-bottom: 3rem;
      //width: 50%;
    }
    &__img {
        width: 50%;
        max-height: 75rem;
    }
}
</style>
