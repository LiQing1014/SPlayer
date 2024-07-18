<!-- 主导航栏 -->
<template>
  <nav :class="{ 'main-nav': true, 'no-sider': !showSider }">
    <div class="left">
      <div :class="['logo', asideMenuCollapsed ? 'collapsed' : null]" @click="router.push('/')">
        <!-- <n-avatar class="logo-img" src="/imgs/icons/favicon.png?asset" /> -->
        <n-icon class="logo-img" size="30">
          <!--          <svg-->
          <!--            xmlns="http://www.w3.org/2000/svg"-->
          <!--            xmlns:xlink="http://www.w3.org/1999/xlink"-->
          <!--            viewBox="0 0 1024 1024"-->
          <!--          >-->
          <!--            <path-->
          <!--              d="M511.764091 131.708086a446.145957 446.145957 0 1 0 446.145957 446.145957 446.145957 446.145957 0 0 0-446.145957-446.145957z m0 519.76004A71.829499 71.829499 0 1 1 583.59359 580.530919 72.275645 72.275645 0 0 1 511.764091 651.468126z"-->
          <!--              :fill="themeAutoCover ? 'var(&#45;&#45;main-second-color)' : '#F55E55'"-->
          <!--            />-->
          <!--            <path-->
          <!--              d="M802.205109 0.541175l-168.197026 37.030114a67.814185 67.814185 0 0 0-53.091369 66.029602V223.614153l3.569168 349.778431h114.213365V223.614153h108.859613a26.322611 26.322611 0 0 0 26.768758-26.322611V26.863786a26.768757 26.768757 0 0 0-32.122509-26.322611z"-->
          <!--              :fill="themeAutoCover ? 'var(&#45;&#45;main-color)' : '#F9BBB8'"-->
          <!--            />-->
          <!--            <path-->
          <!--              d="M511.764091 386.457428a186.935156 186.935156 0 1 0 186.935156 186.48901A186.935156 186.935156 0 0 0 511.764091 386.457428z m0 264.564552a71.383353 71.383353 0 1 1 71.383353-71.383353 71.383353 71.383353 0 0 1-71.383353 71.383353z"-->
          <!--              :fill="themeAutoCover ? 'var(&#45;&#45;main-color)' : '#F9BBB8'"-->
          <!--            />-->
          <!--          </svg>-->
          <svg
            t="1721277022867"
            class="icon"
            viewBox="0 0 1024 1024"
            version="1.1"
            xmlns="http://www.w3.org/2000/svg"
            p-id="12134"
            width="48"
            height="48"
          >
            <path
              d="M849.92 51.2H174.08c-67.8656 0-122.88 55.0144-122.88 122.88v675.84c0 67.8656 55.0144 122.88 122.88 122.88h675.84c67.8656 0 122.88-55.0144 122.88-122.88V174.08c0-67.8656-55.0144-122.88-122.88-122.88z m-80.38912 605.91104c-32.82432 77.88032-90.5728 128.10752-171.7504 151.20384a284.83584 284.83584 0 0 1-94.592 10.39872c-66.60096-3.7888-124.29824-28.9536-172.90752-74.4448-47.95392-44.88192-77.85472-100.06016-88.25856-164.83328-14.15168-88.10496 7.55712-167.10656 64.96256-235.61216 31.5392-37.632 70.8864-64.75264 116.77696-82.26304 15.81568-6.03648 33.1264-0.41984 41.8048 13.39392 8.86272 14.10048 6.78912 32.25088-5.49888 43.48416-3.47136 3.1744-7.85408 5.67808-12.2368 7.46496-69.95968 28.56448-116.18304 78.86848-134.53824 152.22784-17.81248 71.17824-2.06336 136.33024 43.41248 193.73056 28.50304 35.98336 65.32608 60.14976 109.89568 72.01792 28.80512 7.66976 57.91744 8.17152 87.25504 3.6352 30.27456-4.67968 58.5472-14.63296 83.90656-31.99488 34.8928-23.88992 59.74528-55.75168 72.17664-96.26624 10.74176-34.9952 11.10528-70.31296-2.16064-105.04192-10.6752-27.94496-29.5424-49.45408-53.20704-67.18464-12.6464-9.472-26.21952-16.87552-41.69728-20.50048-0.70144-0.16384-1.41824-0.24576-2.69824-0.45056 2.11456 8.09984 4.08064 15.79008 6.10816 23.45984 4.91008 18.5088 9.92256 36.98688 14.75072 55.51616 10.48576 40.2688 0.34304 75.55584-27.392 105.62048-25.6512 27.81184-58.31168 39.9104-95.77472 36.28544-41.70752-4.0448-71.4752-26.6752-90.90048-63.32416-10.17344-19.18976-14.56128-39.87456-15.37024-61.5168-1.29024-34.4576 6.75328-66.27328 26.49088-94.70976 21.20192-30.54592 50.57024-50.14016 85.26336-62.32576 2.73408-0.95744 5.49376-1.82784 8.69888-2.8928-1.86368-7.08608-3.81952-14.0032-5.49376-20.992-2.31424-9.60512-5.28384-19.15904-6.44608-28.91776-3.44064-28.8512 5.42208-53.95968 25.35936-74.96704 16.32256-17.2032 36.12672-28.11904 59.84256-31.37536 2.61632-0.3584 5.2224-0.75776 7.82336-1.13664h10.68032c6.20544 1.00864 12.48256 1.72544 18.62144 3.07712 21.57056 4.75136 40.88832 14.30016 57.9328 28.29824 11.1872 9.18016 15.75424 21.15584 12.51328 35.34336-2.90304 12.75392-11.06432 21.34016-23.64928 25.0112-11.89376 3.47136-22.656 0.83968-32.43008-6.99392-12.38016-9.92256-26.12224-16.7936-42.59328-15.32416-13.95712 1.24416-27.31008 15.92832-26.112 29.04064 0.5376 5.86752 2.6368 11.5968 4.12672 17.36192 2.6368 10.19392 5.34016 20.36736 8.01792 30.5408 0.46592 1.75616 0.896 3.15904 3.34848 3.29216 37.51936 2.048 71.32672 14.25408 101.44768 36.8896 29.6192 22.26176 53.87264 48.96768 70.12864 82.52928 11.92448 24.63232 18.6112 50.64192 20.3776 77.94688 2.36544 36.28544-1.8944 71.7824-16.01536 105.29792z"
              fill="#D81E06"
              p-id="12135"
            ></path>
            <path
              d="M548.52096 462.01344l-8.77568-33.19808c-20.54656 6.528-38.29248 16.49664-51.58912 33.08544-17.80224 22.21568-21.35552 47.73376-15.67232 74.8544 2.94912 14.08 9.83552 26.13248 21.92384 34.54464 15.11424 10.5216 35.69664 10.06592 51.50208-0.87552 16.1536-11.1872 23.3472-29.22496 18.62656-47.72864-5.1712-20.26496-10.66496-40.45312-16.01536-60.68224z"
              fill="#D81E06"
              p-id="12136"
            ></path>
          </svg>
        </n-icon>
        <Transition name="fade" mode="out-in">
          <n-text v-if="!asideMenuCollapsed && showSider" class="site-name">
            {{ siteName }}
          </n-text>
        </Transition>
      </div>
      <n-flex :class="['navigation', { hidden: searchInputFocus }]" :size="6">
        <n-button :focusable="false" class="nav-icon" quaternary @click="router.go(-1)">
          <template #icon>
            <n-icon>
              <SvgIcon icon="chevron-left" />
            </n-icon>
          </template>
        </n-button>
        <n-button :focusable="false" class="nav-icon" quaternary @click="router.go(1)">
          <template #icon>
            <n-icon>
              <SvgIcon icon="chevron-right" />
            </n-icon>
          </template>
        </n-button>
      </n-flex>
      <!-- 搜索框 -->
      <SearchInp />
      <!-- GitHub -->
      <!--      <Transition name="fade" mode="out-in">-->
      <!--        <n-button-->
      <!--          v-if="showGithub"-->
      <!--          :focusable="false"-->
      <!--          class="github"-->
      <!--          circle-->
      <!--          quaternary-->
      <!--          @click="openGithub"-->
      <!--        >-->
      <!--          <template #icon>-->
      <!--            <n-icon size="20">-->
      <!--              <SvgIcon icon="github"/>-->
      <!--            </n-icon>-->
      <!--          </template>-->
      <!--        </n-button>-->
      <!--      </Transition>-->
    </div>
    <div class="right">
      <!-- 全局菜单 -->
      <n-dropdown
        :show="mainMenuShow"
        :show-arrow="true"
        :options="mainMenuOptions"
        placement="bottom-end"
        @clickoutside="mainMenuShow = false"
      >
        <n-button
          :style="{ pointerEvents: mainMenuShow ? 'none' : 'auto' }"
          :class="['main-menu', { show: !showSider }]"
          secondary
          strong
          round
          @click="mainMenuShow = !mainMenuShow"
        >
          <template #icon>
            <n-icon>
              <SvgIcon icon="menu" />
            </n-icon>
          </template>
        </n-button>
      </n-dropdown>
      <!-- 用户信息 -->
      <userData />
      <!-- TitleBar -->
      <TitleBar v-if="checkPlatform.electron()" />
    </div>
  </nav>
</template>

<script setup>
import { NScrollbar } from "naive-ui";
import { storeToRefs } from "pinia";
import { siteStatus, siteSettings } from "@/stores";
import { checkPlatform } from "@/utils/helper";
import { useRouter } from "vue-router";
import Menu from "@/components/Global/Menu";
import packageJson from "@/../package.json";

const router = useRouter();
const status = siteStatus();
const settings = siteSettings();
const { asideMenuCollapsed, searchInputFocus } = storeToRefs(status);
const { showGithub, showSider, themeAutoCover } = storeToRefs(settings);

// 站点信息
const siteName = import.meta.env.RENDERER_VITE_SITE_TITLE;

// 打开 GitHub
const openGithub = () => {
  console.log(packageJson.github);
  window.open(packageJson.github);
};

// 主菜单渲染
const mainMenuShow = ref(false);
const mainMenuOptions = computed(() => [
  {
    key: "menu",
    type: "render",
    props: {
      onClick: () => (mainMenuShow.value = false),
    },
    render: () => {
      return h(NScrollbar, { style: { maxHeight: "calc(100vh - 200px)", minWidth: "280px" } }, () =>
        h(Menu),
      );
    },
  },
]);
</script>

<style lang="scss" scoped>
.main-nav {
  width: 100%;
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: space-between;
  padding: 0 16px;

  .left,
  .right {
    display: flex;
    flex-direction: row;
    align-items: center;
  }

  .logo {
    width: 224px;
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: flex-start;
    padding-left: 6px;
    box-sizing: border-box;
    transition:
      width 0.3s,
      padding-left 0.3s;
    -webkit-app-region: no-drag;
    cursor: pointer;

    .logo-img {
      width: 30px;
      height: 30px;
      min-width: 30px;
      background-color: transparent;
      transition: transform 0.3s;

      &:hover {
        transform: scale(1.15);
      }

      &:active {
        transform: scale(1);
      }
    }

    .site-name {
      margin-left: 12px;
      font-size: 20px;
      font-weight: bold;
    }

    &.collapsed {
      width: 48px;
      padding-left: 0;
    }
  }

  .navigation {
    display: flex;
    flex-direction: row;
    justify-content: flex-start;
    height: 34px;
    width: 86px;
    min-width: 86px;
    transition:
      width 0.3s,
      min-width 0.3s,
      opacity 0.3s;
    overflow: hidden;
    -webkit-app-region: no-drag;

    .nav-icon {
      border-radius: 8px;
      padding: 0 8px;

      .n-icon {
        font-size: 24px;
      }
    }

    @media (max-width: 700px) {
      &.hidden {
        opacity: 0;
        width: 0px;
        min-width: 0px;
      }
    }
  }

  .github {
    margin-left: 12px;
    -webkit-app-region: no-drag;
  }

  .main-menu {
    -webkit-app-region: no-drag;
    margin-right: 12px;
    display: none;

    &.show {
      display: flex;
    }

    @media (max-width: 900px) {
      display: flex;
    }
  }

  &.no-sider {
    max-width: 1400px;
    margin: 0 auto;
    padding: 0 10vw;
    @media (max-width: 1200px) {
      padding: 0 5vw;
    }

    .logo {
      width: auto;
      padding-left: 0;
      margin-right: 12px;
    }
  }

  @media (max-width: 900px) {
    .left {
      .logo {
        width: auto;
        padding-left: 0;
        margin-right: 12px;

        .site-name {
          display: none;
        }
      }
    }
  }
  @media (max-width: 700px) {
    .left {
      width: 100%;
    }
    .github {
      display: none;
    }
  }
}
</style>
