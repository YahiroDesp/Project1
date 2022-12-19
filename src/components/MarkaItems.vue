<template>
    <div id="Magaz">
        <div class="magazz" v-for="product in products" :key="product.id">
            <div class="magaz-item" id="id">
                <h2>Порядковый номер: {{product.id}}</h2>
            </div>
            <div class="magaz-item" id="name">
                <h2>Название продукта: {{product.name}}</h2>
            </div>
            <div class="magaz-item" id="date">
                <h2>Дата приема товара: {{product.date}}</h2>
            </div>
            <div class="magaz-item" id="amount">
                <h2>Количество продукта: {{product.amount}}</h2>
            </div>
            <div class="magaz-item" id="price">
                <h2>Цена за товар: {{product.price}}</h2>
            </div>
            <div class="magaz-item" id="price">
                <h2>Итоговая сумма: {{product.eventualPrice}}</h2>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    props: {
        products: {
            type: Array,
            required: true
        }
    }
}
</script>

<style scoped>

#Magaz {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    padding: 40px 0;
}
.magazz {
    width: 70%;
}


.magazz:not(:last-child) {
    margin-bottom: 50px;
}

.magaz-item {
    padding: 20px 0 20px 10px;
}

.magaz-item:not(:first-child, :last-child) {
    border: 2px solid rgba(55, 18, 143, 0.7);
    border-top: none;
}

.products__item:nth-child(2) {
    border-top: 2px solid rgba(152, 31, 207, 0.7);
}
</style>