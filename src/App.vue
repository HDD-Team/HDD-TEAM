<template>
  <div class="container mx-auto p-8">
    <h1 class="text-4xl font-bold text-center mb-8">Команда HDD</h1>
    <p class="text-center text-lg mb-12">
      Наша команда состоит из молодых специалистов в области ML разработки и дизайна. Мы стремимся
      создавать высококачественные и инновационные решения для наших клиентов.
    </p>
    <div class="text-center mt-12">
      <a href="https://github.com/HDD-Team" target="_blank" class="text-blue-500 text-lg"
        >GitHub команды</a
      >
    </div>
    <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
      <div v-for="member in team" :key="member.name" class="bg-white p-6 rounded-lg shadow-lg">
        <img
          :src="`public/images/${member.image}`"
          alt="team member"
          class="w-32 h-32 rounded-full mx-auto mb-4"
        />
        <h2 class="text-xl font-bold text-center">{{ member.name }}</h2>
        <p class="text-center mb-4">{{ member.description }}</p>
        <div class="flex justify-center">
          <a :href="member.telegram" target="_blank" class="text-blue-500">
            <svg
              class="w-6 h-6"
              fill="currentColor"
              viewBox="0 0 24 24"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                d="M12 0C5.371 0 0 5.371 0 12C0 18.629 5.371 24 12 24C18.629 24 24 18.629 24 12C24 5.371 18.629 0 12 0ZM17.707 8.707L16.293 15.293C16.16 15.908 15.789 16.043 15.292 15.792L12.449 13.964L11.067 15.346C10.92 15.492 10.801 15.611 10.516 15.611L10.717 12.754L14.939 9.186C15.151 9.007 14.916 8.891 14.644 9.07L9.331 12.324L6.55 11.462C5.942 11.262 5.924 10.886 6.632 10.626L17.041 6.521C17.521 6.341 17.96 6.626 17.707 8.707Z"
              />
            </svg>
          </a>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      team: [
        {
          name: 'Бражко Денис',
          image: 'denis.jpg',
          description: 'Тимлид, бэкенд разработчик, ML разработчик.',
          telegram: 'https://t.me/T1nnLD'
        },
        {
          name: 'Буренок Андрей',
          image: 'andrey.jpg',
          description: 'Бэкенд разработчик, ML разработчик.',
          telegram: 'https://t.me/Lord_Baranius'
        },
        {
          name: 'Шургин Никита',
          image: 'nikita.jpg',
          description: 'ML разработчик.',
          telegram: 'https://t.me/whoa2ht'
        },
        {
          name: 'Гунько Даниил',
          image: 'daniil.jpg',
          description: 'ML разработчик.',
          telegram: 'https://t.me/setsudanik'
        },
        {
          name: 'Далиба Богдан',
          image: 'bogdan.jpg',
          description: 'Фронтенд разработчик, дизайнер, спикер.',
          telegram: 'https://t.me/Hogur'
        }
      ]
    }
  }
}
</script>

<style scoped>
.container {
  max-width: 1200px;
}
</style>
