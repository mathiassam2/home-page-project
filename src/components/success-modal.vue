<template>
    <div class="backdrop">
        <div class="modal" :class="{ rainbowModal: theme === 'rainbow' }">
            <div class="content">
                <p><i class="fas fa-check"></i></p>
                <p class="success-msg">{{successMsg}}</p>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    props: ['successMsg', 'customBorder']
}
</script>

<style scoped>
.success-msg {
    font-weight: bold;
    font-size: 18px;
    color: rgb(49, 47, 58);
}
.modal {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    width: 200px;
    height: 200px;
    background-color: #fff;
    border-radius: 10px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.5);
    z-index: 100;
    display: flex;
    justify-content: center;
    align-items: center;
    padding: 10px;
}

.backdrop {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-color: rgba(0, 0, 0, 0.5);
    z-index: 99;
}

.content {
    text-align: center;
}

/* Style the checkmark */
.modal p {
    text-align: center;
}

.modal i.fas.fa-check {
    color: rgb(79, 179, 79);
    font-size: 48px; /* Adjust size as needed */
    border: 2px solid rgb(79, 179, 79);
    border-radius: 50%; /* Make it circular */
    padding: 10px; /* Add some padding */
}
</style>
