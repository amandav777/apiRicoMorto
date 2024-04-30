<template>
  <section class="section about-section gray-bg" id="about">
    <div class="container">
      <div class="row align-items-center flex-row-reverse">
        <div class="col-lg-6">
          <div class="about-text go-to">
            <h3 style="color: deeppink;" >Sobre mim</h3>
            <h6>Estagiária de UX Design &amp; Front com Angular</h6>
            <p>
              Estou me especializando em <mark>UX/UI</mark>, que é área que
              gosto em tecnologia. Sou pesquisadora pelo PIIC e meus hobbies são
              jogar lol e cozinhar.
            </p>
            <div class="row about-list">
              <div class="col-md-6">
                <div class="media">
                  <label>Nome</label>
                  <p>Amanda Vieira Silva</p>
                </div>
                <div class="media">
                  <label>Curso</label>
                  <p>ADS</p>
                </div>
              </div>
              <div class="col-md-6">
                <div class="media">
                  <label>RA</label>
                  <p>1957029</p>
                </div>
                <div class="media">
                  <label>Termo</label>
                  <p>3º A</p>
                </div>
              </div>
            </div>
          </div>
        </div>
        <div class="col-lg-6">
          <div class="about-avatar">
            <img
              src="/src/assets/images/zLVWdJeX_400x400.jpg"
              title=""
              alt=""
            />
          </div>
        </div>
      </div>
      <div class="counter">
        <div class="stack">
          <img
            src="/src/assets/images/Figma-logo.svg"
            alt=""
            style="width: 50px; margin-bottom: 10px"
          />
          <h6 class="count h2" data-to="500" data-speed="500">Figma</h6>
          <p class="m-0px font-w-600">avançado</p>
        </div>

        <div class="stack">
          <img
            src="/src/assets/images/Angular_full_color_logo.svg.png"
            alt=""
            style="width: 50px; margin-bottom: 10px"
          />
          <h6 class="count h2" data-to="150" data-speed="150">Angular</h6>
          <p class="m-0px font-w-600">avançado</p>
        </div>

        <div class="stack">
          <div class="count-data text-center">
            <img
              src="/src/assets/images/16492.png"
              alt=""
              style="width: 50px; margin-bottom: 10px"
            />
            <h6 class="count h2" data-to="850" data-speed="850">Pesquisa</h6>
            <p class="m-0px font-w-600">avançada</p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
body {
  margin-top: 20px;
}
.section {
  padding: 100px 0;
  position: relative;
}
img {
  max-width: 100%;
}
img {
  vertical-align: middle;
  border-style: none;
}

.about-text h3 {
  font-family: "Montserrat", sans-serif;
  font-size: 45px;
  font-weight: 700;
  margin: 0 0 6px;
}
@media (max-width: 767px) {
  .about-text h3 {
    font-size: 35px;
  }
}
.about-text h6 {
  font-weight: 600;
  margin-bottom: 15px;
}
@media (max-width: 767px) {
  .about-text h6 {
    font-size: 18px;
  }
}
.about-text p {
  font-size: 18px;
  max-width: 450px;
}
.about-text p mark {
  font-weight: 600;
  color: hotpink;
}

.about-list {
  padding-top: 10px;
}
.about-list .media {
  padding: 5px 0;
}
.about-list label {
  color: hot;
  font-weight: 600;
  width: 88px;
  margin: 0;
  position: relative;
}
.about-list label:after {
  content: "";
  position: absolute;
  top: 0;
  bottom: 0;
  right: 11px;
  width: 1px;
  height: 12px;
  background: hotpink;
  -moz-transform: rotate(15deg);
  -o-transform: rotate(15deg);
  -ms-transform: rotate(15deg);
  -webkit-transform: rotate(15deg);
  transform: rotate(15deg);
  margin: auto;
  opacity: 0.5;
}
.about-list p {
  margin: 0;
  font-size: 15px;
}

@media (max-width: 991px) {
  .about-avatar {
    margin-top: 30px;
  }
}

.about-section .counter {
  padding: 22px 20px;
  background: #ffffff;
  border-radius: 10px;
  box-shadow: 0 0 30px rgba(31, 45, 61, 0.125);
  margin-top: 5%;
  display: inline-flex;
  flex-direction: row;
  justify-content: space-between;
  width: 100%;
  gap: 20%;
}

.about-section .counter .count {
  font-weight: 700;
  color: hotpink;
  margin: 0 0 5px;
}
.about-section .counter p {
  font-weight: 600;
  margin: 0;
}

mark {
  background-size: 100% 3px;
  background-repeat: no-repeat;
  background-position: 0 bottom;
  background-color: transparent;
  padding: 0;
  color: currentColor;
}

.theme-color {
  color: deeppink;
}
h6 {
  color: deeppink;
}

.stack{
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

</style>
