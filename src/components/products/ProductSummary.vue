<template>
    <div class="card">
        <h3>{{ product.name }}</h3>

        <h5 class ="price"> Pris: kr {{product.price.toFixed(2)}}</h5>
        <p class="description"> Beskrivelse: {{ description }}</p>
        <p class="text-muted">{{ product.category }}</p>
        <button class="view-product-button" @click="$emit('view-product', product)">Vis produkt</button>
    </div>
</template>

<script>
export default {
    props:['product'],
    computed: {
        description(){
            return this.product.description.substring(0, 150)
        }
    }

}
</script>

<style lang="css">
    .card {
        width: 80%;
        margin: 10%;
        padding: 10px;
        border-radius: 5px;
        background-color: azure;
        box-shadow: 0 0 5px gray;

        h5.price {
            color:gray;
        }

        p.description {
            font-size: .9rem;
        }

        p.text-muted {
            color: gray;
        }
    }

button.view-product-button {
    padding: 10px;
    background-color: lightblue;
    border: none;
    color: white;
    font-weight: bold;
    font-size: 1.15rem;
    border-radius: 5px;
    cursor: pointer;
}

@media (min-width: 500px) {
    .card {
        width: 350px;
        margin: 10px;

    }
}
</style>