<template>
    <div class="drawer-background" :class="{show: active}" @click="$emit('close-product-drawer')" />

    <div class="drawer" :class="{show: active}">
        <div class="drawer-close" @click="$emit('close-product-drawer')">
            X
            </div>

            <div v-if="product" class="product-details">
                <h3 class="text-center">{{ product.name }}</h3>
                <p class="description">{{ product.description }}</p>
                <h3 class="text-center">kr {{ product.price.toFixed(2) }}</h3>
            </div>
        </div>
</template>

<script>

export default {
    props: ['product', 'active']
    
}
</script>
