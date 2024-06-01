<template>
    <div class="d-flex align-items-center">
        <i class="fa-solid fa-paper-plane px-2" :class="{ enlarge: isEnlarging }"></i>
        <p class="align-middle mb-0">{{ currentWord }}</p>
        <p class="blink mb-0" :class="{ hidden: hideCursor }">|</p>
    </div>
</template>

<script>
export default {
    data() {
        return {
            word: "Contact Us",
            currentWord: "",
            isDeleting: false,
            hideCursor: false,
            isEnlarging: false,
            timer: null,
        };
    },
    mounted() {
        this.typingEffect();
    },
    methods: {
        typingEffect() {
            if (this.isDeleting) {
                this.currentWord = this.word.substring(0, this.currentWord.length - 1);
            } else {
                this.currentWord = this.word.substring(0, this.currentWord.length + 1);
            }

            let typingSpeed = this.isDeleting ? 200 : 500;

            if (!this.isDeleting && this.currentWord === this.word) {
                typingSpeed = 2000; // Pausa quando la parola è completamente scritta
                this.isDeleting = true;
            } else if (this.isDeleting && this.currentWord === "") {
                this.isDeleting = false;
                this.hideCursor = true;
                this.isEnlarging = true;
                setTimeout(() => {
                    this.hideCursor = false;
                    this.isEnlarging = false;
                    this.typingEffect();
                }, 1500); // Pausa di 1 secondo quando l'ultima lettera viene cancellata
                return;
            }

            this.timer = setTimeout(this.typingEffect, typingSpeed);
        },
    },
    beforeDestroy() {
        clearTimeout(this.timer);
    },
};
</script>

<style scoped>
.blink {
    animation: blink 0.5s infinite;
}

.hidden {
    visibility: hidden;
}

.enlarge {
    animation: enlarge 1.5s ease-in;
}

@keyframes blink {
    to {
        opacity: 0;
    }
}

@keyframes enlarge {
    0% {
        transform: scale(1);
    }

    50% {
        transform: scale(1.5);
    }

    75% {
        transform: scale(1.25);
    }

    100% {
        transform: scale(1);
    }
}
</style>
