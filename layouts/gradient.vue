<script setup lang="ts">
import { computed } from 'vue'
import { useSlideContext /* 或 useSlidevContext，看你的版本 */ } from '@slidev/client'

/**
 * 取出當前投影片的 Front-matter
 */
const { $frontmatter } = useSlideContext()   // v0.51+
/*  v0.48～0.50 如果找不到 useSlideContext()
     請改成：
     import { useSlidevContext } from '@slidev/client'
     const { $frontmatter } = useSlidevContext()
 */

const colorFrom = computed(() => $frontmatter.gradientFrom ?? '#00b4d8')
const colorTo   = computed(() => $frontmatter.gradientTo   ?? '#0077b6')
const dir       = computed(() => $frontmatter.gradientDir  ?? 'br')
const gradient  = computed(() =>
  `bg-gradient-to-${dir.value} from-[${colorFrom.value}] to-[${colorTo.value}]`,
)
</script>

<template>
  <div :class="['h-full w-full', gradient]">
    <div class="h-full w-full bg-black/20">
      <slot />
    </div>
  </div>
</template>
