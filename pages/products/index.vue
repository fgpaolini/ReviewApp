<template>
    <div class="h-full bg-slate-100">
<!--         <div class="flex flex-wrap justify-around items-center bg-slate-500">
            <div class="col-4 p-8">
                <ProductCard/>
            </div>
            <div class="col-4 p-8">
                <ProductCard/>
            </div>
            <div class="col-4 p-8">
                <ProductCard/>
            </div>
            <div class="col-4 p-8">
                <ProductCard/>
            </div>
        </div> -->
        <div class="card">
        <Carousel :value="products" :numVisible="4" :numScroll="3" :responsiveOptions="responsiveOptions" circular :autoplayInterval="4000">
            <template #item="slotProps">
                <div class="m-2 p-3">
                    <ProductCard :name="slotProps.data.name" :category="slotProps.data.category" :rating="slotProps.data.rating" :to="slotProps.data.id" />
                </div>
            </template>
        </Carousel>
    </div>
    </div>
</template>

<script setup lang="ts">


const products = ref([
    {
                    id: '1000',
                    code: 'f230fh0g3',
                    name: 'Bamboo Watch',
                    description: 'Product Description',
                    image: 'bamboo-watch.jpg',
                    price: 65,
                    category: 'Accessories',
                    quantity: 24,
                    inventoryStatus: 'INSTOCK',
                    rating: 5
                },
                {
                    id: '1001',
                    code: 'nvklal433',
                    name: 'Black Watch',
                    description: 'Product Description',
                    image: 'black-watch.jpg',
                    price: 72,
                    category: 'Accessories',
                    quantity: 61,
                    inventoryStatus: 'INSTOCK',
                    rating: 4
                },
                {
                    id: '1002',
                    code: 'zz21cz3c1',
                    name: 'Blue Band',
                    description: 'Product Description',
                    image: 'blue-band.jpg',
                    price: 79,
                    category: 'Fitness',
                    quantity: 2,
                    inventoryStatus: 'LOWSTOCK',
                    rating: 3
                },
                {
                    id: '1003',
                    code: '244wgerg2',
                    name: 'Blue T-Shirt',
                    description: 'Product Description',
                    image: 'blue-t-shirt.jpg',
                    price: 29,
                    category: 'Clothing',
                    quantity: 25,
                    inventoryStatus: 'INSTOCK',
                    rating: 5
                },
                {
                    id: '1004',
                    code: 'h456wer53',
                    name: 'Bracelet',
                    description: 'Product Description',
                    image: 'bracelet.jpg',
                    price: 15,
                    category: 'Accessories',
                    quantity: 73,
                    inventoryStatus: 'INSTOCK',
                    rating: 4
                },
                {
                    id: '1005',
                    code: 'av2231fwg',
                    name: 'Brown Purse',
                    description: 'Product Description',
                    image: 'brown-purse.jpg',
                    price: 120,
                    category: 'Accessories',
                    quantity: 0,
                    inventoryStatus: 'OUTOFSTOCK',
                    rating: 4
                },
                {
                    id: '1006',
                    code: 'bib36pfvm',
                    name: 'Chakra Bracelet',
                    description: 'Product Description',
                    image: 'chakra-bracelet.jpg',
                    price: 32,
                    category: 'Accessories',
                    quantity: 5,
                    inventoryStatus: 'LOWSTOCK',
                    rating: 3
                },
                {
                    id: '1007',
                    code: 'mbvjkgip5',
                    name: 'Galaxy Earrings',
                    description: 'Product Description',
                    image: 'galaxy-earrings.jpg',
                    price: 34,
                    category: 'Accessories',
                    quantity: 23,
                    inventoryStatus: 'INSTOCK',
                    rating: 5
                },
                {
                    id: '1008',
                    code: 'vbb124btr',
                    name: 'Game Controller',
                    description: 'Product Description',
                    image: 'game-controller.jpg',
                    price: 99,
                    category: 'Electronics',
                    quantity: 2,
                    inventoryStatus: 'LOWSTOCK',
                    rating: 4
                },
                {
                    id: '1009',
                    code: 'cm230f032',
                    name: 'Gaming Set',
                    description: 'Product Description',
                    image: 'gaming-set.jpg',
                    price: 299,
                    category: 'Electronics',
                    quantity: 63,
                    inventoryStatus: 'INSTOCK',
                    rating: 3
                },
                {
                    id: '1010',
                    code: 'plb34234v',
                    name: 'Gold Phone Case',
                    description: 'Product Description',
                    image: 'gold-phone-case.jpg',
                    price: 24,
                    category: 'Accessories',
                    quantity: 0,
                    inventoryStatus: 'OUTOFSTOCK',
                    rating: 4
                },
                {
                    id: '1011',
                    code: '4920nnc2d',
                    name: 'Green Earbuds',
                    description: 'Product Description',
                    image: 'green-earbuds.jpg',
                    price: 89,
                    category: 'Electronics',
                    quantity: 23,
                    inventoryStatus: 'INSTOCK',
                    rating: 4
                },
                {
                    id: '1012',
                    code: '250vm23cc',
                    name: 'Green T-Shirt',
                    description: 'Product Description',
                    image: 'green-t-shirt.jpg',
                    price: 49,
                    category: 'Clothing',
                    quantity: 74,
                    inventoryStatus: 'INSTOCK',
                    rating: 5
                },
                {
                    id: '1013',
                    code: 'fldsmn31b',
                    name: 'Grey T-Shirt',
                    description: 'Product Description',
                    image: 'grey-t-shirt.jpg',
                    price: 48,
                    category: 'Clothing',
                    quantity: 0,
                    inventoryStatus: 'OUTOFSTOCK',
                    rating: 3
                },
                {
                    id: '1014',
                    code: 'waas1x2as',
                    name: 'Headphones',
                    description: 'Product Description',
                    image: 'headphones.jpg',
                    price: 175,
                    category: 'Electronics',
                    quantity: 8,
                    inventoryStatus: 'LOWSTOCK',
                    rating: 5
                },
                {
                    id: '1015',
                    code: 'vb34btbg5',
                    name: 'Light Green T-Shirt',
                    description: 'Product Description',
                    image: 'light-green-t-shirt.jpg',
                    price: 49,
                    category: 'Clothing',
                    quantity: 34,
                    inventoryStatus: 'INSTOCK',
                    rating: 4
                },
                {
                    id: '1016',
                    code: 'k8l6j58jl',
                    name: 'Lime Band',
                    description: 'Product Description',
                    image: 'lime-band.jpg',
                    price: 79,
                    category: 'Fitness',
                    quantity: 12,
                    inventoryStatus: 'INSTOCK',
                    rating: 3
                },
                {
                    id: '1017',
                    code: 'v435nn85n',
                    name: 'Mini Speakers',
                    description: 'Product Description',
                    image: 'mini-speakers.jpg',
                    price: 85,
                    category: 'Clothing',
                    quantity: 42,
                    inventoryStatus: 'INSTOCK',
                    rating: 4
                },
                {
                    id: '1018',
                    code: '09zx9c0zc',
                    name: 'Painted Phone Case',
                    description: 'Product Description',
                    image: 'painted-phone-case.jpg',
                    price: 56,
                    category: 'Accessories',
                    quantity: 41,
                    inventoryStatus: 'INSTOCK',
                    rating: 5
                },
                {
                    id: '1019',
                    code: 'mnb5mb2m5',
                    name: 'Pink Band',
                    description: 'Product Description',
                    image: 'pink-band.jpg',
                    price: 79,
                    category: 'Fitness',
                    quantity: 63,
                    inventoryStatus: 'INSTOCK',
                    rating: 4
                },
                {
                    id: '1020',
                    code: 'r23fwf2w3',
                    name: 'Pink Purse',
                    description: 'Product Description',
                    image: 'pink-purse.jpg',
                    price: 110,
                    category: 'Accessories',
                    quantity: 0,
                    inventoryStatus: 'OUTOFSTOCK',
                    rating: 4
                },
]);
const responsiveOptions = ref([
    {
        breakpoint: '1400px',
        numVisible: 2,
        numScroll: 1
    },
    {
        breakpoint: '1199px',
        numVisible: 3,
        numScroll: 1
    },
    {
        breakpoint: '767px',
        numVisible: 2,
        numScroll: 1
    },
    {
        breakpoint: '575px',
        numVisible: 1,
        numScroll: 1
    }
]);

const getSeverity = (status: string) => {
    switch (status) {
        case 'INSTOCK':
            return 'success';

        case 'LOWSTOCK':
            return 'warning';

        case 'OUTOFSTOCK':
            return 'danger';

        default:
            return null;
    }
};

</script>

<style scoped>

</style>