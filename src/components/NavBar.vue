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
    <div class="search-container">
      <form role="search" id="form">
        <input
          type="search"
          id="query"
          name="q"
          placeholder="Search..."
          aria-label="Search through site content"
        />
        <button>O-</button>
      </form>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.navbar-container {
  position: sticky;
  display: flex;
  justify-content: space-between;
  width: 100%;
  height: 4.375rem;
  top: 0;
  border-bottom: 1px solid #e15100;

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
      color: #e15100;
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

  .search-container {
    margin: auto 15% auto 0;

    input {
      background-color: #dbdbdb;
      border: none;
      padding: 10px;
      margin-right: 5px;
    }
  }
}
</style>
