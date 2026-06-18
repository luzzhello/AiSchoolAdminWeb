<script lang="ts" setup>
import { AuthPageLayout } from '@vben/layouts';

import { $t } from '#/locales';

const appName = import.meta.env.VITE_APP_TITLE || '码蚁AI ADMIN';
const logo = '/mayi-logo.png';
</script>

<template>
  <AuthPageLayout
    :app-name="appName"
    :logo="logo"
    :page-description="$t('authentication.pageDesc')"
    :page-title="$t('authentication.pageTitle')"
  >
    <template #logo>
      <div class="absolute left-0 top-0 z-10 flex flex-1">
        <div
          class="text-foreground lg:text-foreground ml-4 mt-4 flex flex-1 items-center sm:left-6 sm:top-6"
        >
          <img
            :alt="appName"
            :src="logo"
            class="mr-2 h-[42px] w-[42px] object-contain"
          />
          <p class="m-0 text-xl font-medium">
            {{ appName }}
          </p>
        </div>
      </div>
    </template>
  </AuthPageLayout>
</template>
