<template>
  <div class="aside-container">
    <div class="aside-content">
      <h3>Let’s Make Your Website Look Awesome!</h3>
      <p>Im a Web Developer transitioning from mechanical engineering.</p>
      <p>
        This is a website where I share my projects and my knowledge, and
        hopefully help someone else that needs it.
      </p>
      <p>
        I'd like to show the world my skills, but to also learn from the best.
      </p>
      <button>Contact Me</button>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.aside-container {
  margin-top: 100px;
  width: 310px;
  background: #fff9e4;
  border-radius: 21px;
  height: 620px;

  .aside-content {
    padding: 38px;

    h3 {
      font-family: "Inter", sans-serif;
      font-weight: 800;
      padding-bottom: 35px;
      text-align: center;
      font-size: 24px;
      color: #2a2c2b;
    }

    p {
      font-family: "Roboto", sans-serif;
      padding-bottom: 25px;
      text-align: center;
      font-size: 18px;
    }

    button {
      text-align: center;
      padding: 20px 35px;
      margin: 30px auto 45px;
      display: block;
      border-radius: 11px;
      font-family: "Inter", sans-serif;
      font-weight: 800;
      color: white;
      font-size: 20px;
      border: none;
      background-color: #e15100;
    }
  }
}
</style>
