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
      <p>Участников: 0</p>
      <ul></ul>
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
    };
  },
  computed: {
    fullName() {
      return `${this.firstName.toUpperCase()} ${this.secondName.toUpperCase()} ${this.lastName.toUpperCase()}`;
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
