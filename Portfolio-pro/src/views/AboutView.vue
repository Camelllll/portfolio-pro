<template>
  <div class="profile">
    <h1>Profil</h1>

    <div class="big-section">
      <div class="flex">
        <section class="section">
          <h2>Section 1</h2>
          <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec a diam lectus.</p>
        </section>

        <section class="section">
          <h2>Section 2</h2>
          <p>Sed orci ipsum, malesuada nec pellentesque sit amet, vestibulum in velit.</p>
        </section>

        <section class="section">
          <h2>Section 3</h2>
          <p>Proin eu purus eget diam vehicula aliquet sit amet a lectus.</p>
        </section>
      </div>
    </div>

  </div>
</template>

<style scoped>

.big-section {
  border-radius: 20px 20px 0 0;
  overflow: hidden;
}

.flex {
  display: flex;
  justify-content: space-between;
  gap: 0; 
}

.section {
  width: 33.33%; 
  padding: 20px;
  border: 0.2px solid #ccc;
  background-color: #fff;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}

</style>