<template>
  <h1 class="flex items-center font-bold text-stone-700">
    <span
      class="flex h-10 w-20 items-center justify-center rounded-l-md bg-stone-700 px-4 text-sm text-stone-50"
    >
      <slot name="day" />
    </span>
    <span
      class="flex h-10 items-center rounded-r-md border border-stone-300 pl-4 pr-6 text-xl"
    >
      <slot />
    </span>
  </h1>
</template>
