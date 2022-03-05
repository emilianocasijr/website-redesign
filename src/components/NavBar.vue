<template>
  <div class="navbar-container">
    <div class="navbar">
      <h2>Emiliano Casi Jr</h2>
      <nav>
        <ul>
          <li><a href="">Projects</a></li>
          <li><a href="">Articles</a></li>
          <li><a href="">About</a></li>
          <li><a href="">Contact Me</a></li>
        </ul>
      </nav>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.navbar-container {
  position: fixed;
  display: flex;
  width: 100%;
  height: 4.375rem;

  .navbar {
    display: flex;
    margin-left: 15%;

    h2 {
      margin: 0 100px 0 0;
      display: flex;
      align-items: center;
      font-family: mulish;
      font-weight: 600;
      font-size: 22px;
      color: rgb(192, 0, 32);
    }

    ul {
      display: flex;
      list-style-type: none;
      align-items: center;
      height: 100%;
      padding: 0;
      margin: 0;

      li {
        text-decoration: none;
        margin-left: 20px;

        a {
          text-decoration: none;
          color: rgb(73, 73, 73);
          font-family: "Noto Serif", serif;
          font-size: 14px;
        }
      }
    }
  }
}
</style>
