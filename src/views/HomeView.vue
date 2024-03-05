<template>
  <div class="home">
    <div class="container">
      <input type="radio" name="slide" id="c1" checked />
      <label for="c1" class="card">
        <div class="row">
          <div class="icon">1</div>
          <div class="description">
            <h4>HATAKE KAKASHI</h4>
            <p>
              Kakashi is a highly skilled ninja in the Naruto series, renowned
              for his expertise in combat and his enigmatic personality.
            </p>
          </div>
        </div>
      </label>
      <input type="radio" name="slide" id="c2" />
      <label for="c2" class="card">
        <div class="row">
          <div class="icon">2</div>
          <div class="description">
            <h4>HARUNO SAKURA</h4>
            <p>
              Sakura is a strong kunoichi in the Naruto universe, known for her
              intelligence and medical ninjutsu skills.
            </p>
          </div>
        </div>
      </label>
      <input type="radio" name="slide" id="c3" />
      <label for="c3" class="card">
        <div class="row">
          <div class="icon">3</div>
          <div class="description">
            <h4>UCHIHA SASUKE</h4>
            <p>
              Sasuke is a formidable ninja in the Naruto universe, celebrated
              for his prodigious talent in combat and his complex, driven
              personality.
            </p>
          </div>
        </div>
      </label>
      <input type="radio" name="slide" id="c4" />
      <label for="c4" class="card">
        <div class="row">
          <div class="icon">4</div>
          <div class="description">
            <h4>UZUMAKI NARUTO</h4>
            <p>
              Naruto is a prominent character in the Naruto universe, known for
              his determination and ability to connect with others.
            </p>
          </div>
        </div>
      </label>
    </div>
  </div>
</template>

<script>
export default {
  name: "HomeView",
  components: {},
};
</script>

<style scoped>
.home {
  align-items: center;
  display: flex;
  height: 100vh;
  justify-content: center;
  width: 100%;
}
.container {
  display: flex;
  flex-wrap: nowrap;
  height: 400px;
  justify-content: start;
}
.card {
  align-items: flex-end;
  background-size: cover;
  border-radius: 0.75rem;
  border-radius: 2rem;
  box-shadow: 0px 10px 30px -5px rgba(0, 0, 0, 0.8);
  cursor: pointer;
  display: flex;
  margin: 0 10px;
  overflow: hidden;
  transition: 0.6s cubic-bezier(0.28, -0.03, 0, 0.99);
  width: 80px;
}
.card > .row {
  color: white;
  display: flex;
  flex-wrap: nowrap;
}
.card > .row > .icon {
  align-items: center;
  background: rgba(255, 255, 255, 0.2);
  border-radius: 50%;
  color: white;
  display: flex;
  justify-content: center;
  margin: 15px;
  width: 50px;
}
.card > .row > .description {
  display: flex;
  flex-direction: column;
  height: 80px;
  justify-content: center;
  opacity: 0;
  overflow: hidden;
  transform: translateY(30px);
  transition-delay: 0.3s;
  transition: all 0.3s ease;
  width: 520px;
}
.description p {
  color: rgba(255, 255, 255, 0.6);
  padding-top: 5px;
}
.description h4 {
  text-transform: uppercase;
}
input {
  display: none;
}
input:checked + label {
  width: 600px;
}
input:checked + label .description {
  opacity: 1 !important;
  transform: translateY(0) !important;
}

.card[for="c1"] {
  background-image: url("../assets/image1.png");
}
.card[for="c2"] {
  background-image: url("../assets/image2.png");
}
.card[for="c3"] {
  background-image: url("../assets/image3.png");
}
.card[for="c4"] {
  background-image: url("../assets/image4.png");
}
</style>
