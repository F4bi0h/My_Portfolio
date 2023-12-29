<template>
    <section>
        <div>
            <h1 class="display-1">Fábio Henrique</h1>
            <p>Desenvolvedor Full-stack</p>
            <button type="button" @click="show = !show" class="btn btn-dark">Clique Aqui</button>
        </div>
    </section>
</template>

<script>
import Swal from 'sweetalert2';

export default {
    methods: {
        teste() {
            Swal.fire({
                title: 'Succes',
                text: 'Do you want to continue',
                icon: 'success',
                confirmButtonText: 'Cool'
            })
        }
    }
}
window.addEventListener('DOMContentLoaded', () => {
    document.querySelector('div').classList.add('load');
})
</script>

<style scoped>
section {
    height: 100vh;
    width: 100%;
    display: flex;
    align-items: center;
    justify-content: center;
    flex-direction: column;
    color: #fff;
    z-index: 1;
}
section div {
    display: flex;
    align-items: center;
    justify-content: center;
    flex-direction: column;
    opacity: 0;
    animation: fade-in 3s normal forwards ease-in-out;
}
section h1 {
    text-shadow: 0 0 10px gray;
    margin-bottom: -15px;
}
@keyframes fade-in {
    from {opacity: 0;}
    to {opacity: 1;}
}
</style>