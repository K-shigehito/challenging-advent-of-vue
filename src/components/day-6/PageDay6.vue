<script setup lang="ts">
import { onMounted } from "vue";
import ComparisonSummary from "./ComparisonSummary.vue";
import ItemSelect from "./ItemSelect.vue";
import { useItemComparison } from "@/composables/itemComparison";

const apiUrl = "https://dummyjson.com/products";
const { isFetchingItems, availableItems } = useItemComparison();

onMounted(async () => {
  try {
    const { products } = await (await fetch(`${apiUrl}?limit=100`)).json();
    availableItems.value = products;
    console.log(availableItems.value);
    isFetchingItems.value = false;
  } catch (error) {
    console.log(error);
    alert("商品の取得に失敗しました");
  }
});
</script>

<template>
  <div class="max-w-lg">
    <div class="flex flex-col justify-center gap-2">
      <ItemSelect />
      <ItemSelect />
      <div class="mt-6">
        <ComparisonSummary />
      </div>
    </div>
  </div>
</template>
