<template>
  <div id="Info">
    <section class="experience">
      <div class="content">
        <img src="../assets/img/info-main-sofa.png" alt="Living Room" class="experience-image" />
        <div class="experience-text">
          <h2>We Provide You The Best Experience</h2>
          <p>
            You don't have to worry about the result because all of<br>
            these interiors are made by people who are professionals<br>
            in their fields, with an elegant and luxurious style and<br>
            with premium quality materials.
          </p>
          <a href="#" class="more-info">More Info</a>
        </div>
      </div>
    </section>

    <section class="materials">
      <div class="content">
        <h2>Very Serious Materials For Making Furniture</h2>
        <p>
          Because panto was very serious about designing furniture<br>
          for our environment, using a very expensive and famous<br>
          capital but at a relatively low price
        </p>
        <a href="#" class="more-info">More Info</a>
        <div class="material-images">
          <img src="../assets/img/info-chair.png" alt="chair"/>
          <img src="../assets/img/info-sofa.png" alt="sofa"/>
          <img src="../assets/img/info-chairs.png" alt="chair"/>
        </div>
      </div>
    </section>
  </div>
</template>

<script>

</script>

<style>
body {
  font-family: 'Gilroy-Light', sans-serif;
}

#Info{
  margin: auto;
}

section {
  padding: 2rem 0;
}

.experience,
.materials {
  display: flex;
  flex-direction: row;
  align-items: center;
}

.experience .content,
.materials .content {
  display: flex;
  flex-direction: column;
  align-items: flex-start;
}

.experience .experience-image {
  max-width: 600px;
  margin-right: 2rem;
}

.experience-text h2,
.materials h2 {
  font-size: 24px;
  margin-bottom: 1rem;
}

.experience-text p,
.materials p {
  font-size: 16px;
  margin-bottom: 1rem;
}

.more-info {
  color: #f9a825;
  text-decoration: none;
}

.material-images {
  display: flex;
  gap: 1rem;
  margin-top: 2rem;
}

.material-images img {
  max-width: 200px;
  border-radius: 8px;
}
</style>
