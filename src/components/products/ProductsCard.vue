<script>
export default {
    name: 'ProductCard'
};
</script>

<template>
    <div class="product-card">
        <img :src="product.thumb" :alt="product.series">
        <p>{{ product.series }}</p>
    </div>
</template>

<style lang="scss" scoped>
.product-card {
    display: flex;
    flex-direction: column;
    padding: 10px;

    p {
        margin-top: 10px;
        font-size: 14px;
    }

    img {
        width: 100%;
        height: 150px;
        object-fit: cover;
        object-position: top;
    }
}
</style>