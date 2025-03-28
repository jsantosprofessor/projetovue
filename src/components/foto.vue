<template>
    <div class="customer-reviews">
        <h2>Avaliações de Clientes</h2>
        <div class="reviews">
            <div v-for="(review, index) in reviews" :key="index" class="review">
                <img :src="review.photo" :alt="'Foto de ' + review.name" class="review-photo" />
                <p class="review-name">{{ review.name }}</p>
                <p class="review-comment">"{{ review.comment }}"</p>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "CustomerFoto",
    data() {
        return {
            reviews: [
                {
                    name: "João Silva",
                    photo: "@/assets/pictures.jpg",
                    comment: "Ótimo serviço, recomendo!"
                },
                {
                    name: "Maria Oliveira",
                    photo: "https://via.placeholder.com/150",
                    comment: "Adorei a experiência, voltarei com certeza!"
                },
                {
                    name: "Carlos Pereira",
                    photo: "https://via.placeholder.com/150",
                    comment: "Muito bom, superou minhas expectativas!"
                }
            ]
        };
    }
};
</script>

<style scoped>
.customer-reviews {
    text-align: center;
    padding: 20px;
}

.reviews {
    display: flex;
    justify-content: center;
    gap: 20px;
    flex-wrap: wrap;
}

.review {
    border: 1px solid #ddd;
    border-radius: 8px;
    padding: 10px;
    max-width: 200px;
    text-align: center;
}

.review-photo {
    width: 100px;
    height: 100px;
    border-radius: 50%;
    object-fit: cover;
    margin-bottom: 10px;
}

.review-name {
    font-weight: bold;
    margin-bottom: 5px;
}

.review-comment {
    font-style: italic;
    color: #555;
}
</style>