<header>
  <div class="app-name">
    <h1>Store.</h1>
  </div>
  <div class="search-bar">
    <input type="text" id="search-input" placeholder="search" />
  </div>
  <div class="actions">
    <li>down</li>
  </div>
</header>

<style>
  header {
    display: flex;
    width: var(--app-max-width);
    height: 10vh;
    background: whitesmoke;
    box-shadow: 0px 2px 20px rgba(0, 0, 0, 0.2);

    & .app-name {
      font-family: milo;
      padding-left: 10px;
      font-size: var(--lg-font-size);
    }

    & .search-bar {
      margin: auto;
      margin: auto;

      display: flex;

    & input {
        width: 20vw;
        height: 5vh;
        border: none;
        border-radius: var(--border-radius);
        margin: auto;
        font-size: var(--md-font-size);
        text-align: center;
      }
    }

    & .actions {
      margin-top: auto;
      margin-bottom: auto;
      margin-left: auto;
      padding: 5px;

      & li {
        list-style: none;
        text-decoration: none;
      }
    }
  }
</style>
