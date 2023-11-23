<template>
  <aside class="sidebar">
    <div class="sidebar__inner">
      <h2 class="sidebar__title">Boshqaruv paneli</h2>
      <div class="sidebar__items">
        <a href="#" class="sidebar__link">
          <img src="@/assets/img/home.svg" class="sidebar__icon">
          <span>Bosh sahifa</span>
        </a>
        <a href="#" class="sidebar__link">
          <img src="@/assets/img/human.svg" class="sidebar__icon">
          <span>Hisobda turganlar</span>
        </a>
        <a href="#" class="sidebar__link">
          <img src="@/assets/img/human.svg" class="sidebar__icon">
          <span>Jamiyat a'zolari</span>
        </a>
        <a href="#" class="sidebar__link">
          <img src="@/assets/img/home.svg" class="sidebar__icon">
          <span>Bo’linmalar</span>
        </a>
        <a href="#" class="sidebar__link">
          <img src="@/assets/img/stat.svg" class="sidebar__icon">
          <span>Statistika</span>
        </a>
        <a href="#" class="sidebar__link">
          <img src="@/assets/img/setting.svg" class="sidebar__icon">
          <span>Sozlamalar</span>
        </a>
      </div>
      <div class="sidebar__footer">
        <a href="#" class="sidebar__link">
          <img src="@/assets/img/logout.svg" class="sidebar__icon">
          <span>Chiqish</span>
        </a>
      </div>
    </div>
  </aside>
</template>
<script>
export default {
  data() {
    return {
      title: ''
    }
  },
  mounted() {
    fetch("http://localhost:3000/home")
      .then(res => res.json())
      .then(data => {
        this.title = data.title
      })
  },
};
</script>
<style lang="scss">
.sidebar {
  padding: 16px;
  height: 100vh;
  width: 100%;
  max-width: 266px;
  background-color: #FFF;
  &__inner {
    display: flex;
    flex-direction: column;
    justify-content: flex-start;
    height: 100%;
  }
  
  &__title {
    padding: 30px 0 45px;
    color: #110B56;
    font-size: 2rem;
    font-weight: 900;
    line-height: 2rem;
    letter-spacing: 0.4px;
    text-align: center;
  }
  &__items {
    display: flex;
    flex-direction: column;
  }
  &__footer {
    margin-top: auto;
  }
  &__icon {
    margin-right: 16px;
  }
  &__link {
    &:hover {
      color: #56549E;
      background: linear-gradient(to left, #E7E9FE00, #E7E9FE);
    }
    width: 100%;
    display: inline-flex;
    align-items: center;
    justify-content: flex-start;
    border-radius: 8px;
    padding: 16px 25px;
    text-decoration: none;
    color: #79798B;
    font-size: 1.4rem;
    font-weight: 500;
    line-height: normal;
    letter-spacing: 0.28px;
  }
}
</style>