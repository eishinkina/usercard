<template>
  <div class="conatiner">
    <div class="user-card">
      <h1>Научу зарабатывать от 50 000р. в час</h1>
      <div class="main-information flex">
        <img src="../assets/images/коуч.jpg" width="500px" />
        <div class="info">
          <h2>
            {{ fullName }}
          </h2>
          <strong>Бизнес-коуч</strong>
          <ul class="list">
            <li>
              Учу делать РЕАЛЬНЫЕ бабки, на себя просто не хватило времени
            </li>
            <li>
              НЕ знаю, что такое "Успешный Успех", но знаю, что нужно ТЕБЕ!
            </li>
            <li>Пообещал, что побреюсь, когда кого-нибудь ОБМАНУ.</li>
          </ul>
        </div>
      </div>
      <p>Участников: {{ users.length }}</p>
      <ul>
        <li v-for="(user, i) in users" :key="user.id">
          {{ i + 1 }}. {{ getFullName(user) }}
        </li>
      </ul>
      <!-- input type text -->
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      firstName: "Иван",
      secondName: "Иванович",
      lastName: "Иванов",
      users: [
        {
          id: 1,
          name: "Иванов Иван Иванович",
          age: 25,
          email: "ivan@goggle.com",
        },
        {
          id: 2,
          name: "Петров Петр Петрович",
          age: 30,
          email: "petr@google.com",
        },
        {
          id: 3,
          name: "Сидоров Сидор Сидорович",
          age: 35,
          email: "sidor@google.com",
        },
        {
          id: 4,
          name: "Александров Александр Александрович",
          age: 40,
          email: "alex@google.com",
        },
      ],
    };
  },
  computed: {
    fullName() {
      return `${this.firstName.toUpperCase()} ${this.secondName.toUpperCase()} ${this.lastName.toUpperCase()}`;
    },
  },
  methods: {
    getFullName(user) {
      return `${user.name} - ${user.age} лет, email: ${user.email}`;
    },
  },
};
</script>

<style lang="scss" scoped>
.user-card {
  margin-top: 40px;
}
.info {
  margin-left: 50px;
}
h2 {
  margin-bottom: 14px;
}
</style>
