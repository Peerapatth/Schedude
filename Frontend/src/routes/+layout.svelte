<script>
    import './style.css';
    import { onMount } from "svelte";
  
    let darkMode = false;
    let currentPage = "";
  
    onMount(() => {
      darkMode = localStorage.getItem("darkMode") === "true";
      currentPage = getCurrentPage();

      applyDarkModeStyles();
    });
  
    function toggleDarkMode() {
      darkMode = !darkMode;
  
      localStorage.setItem("darkMode", darkMode.toString());
      applyDarkModeStyles();
    }
  
    function getCurrentPage() {
      const path = window.location.pathname;
      if (path === "/") return "/";
      if (path === "/Schedule") return "/Schedule";
      return "";
    }

    function applyDarkModeStyles() {
    document.documentElement.style.setProperty('--bck', darkMode ? '#f6f6f6' : '#131212');
    document.documentElement.style.setProperty('--wht', darkMode ? '#131212' : '#f6f6f6');
  }

  </script>
  
  <div class="container">
    <nav>
      <div class="nav">
        <div class="logo">
          <div>SCHEDULE.</div>
        </div>
        <div class="nav-link">
          <a href="/" class:active={currentPage === '/'} on:click={() => (currentPage = '/')}>
            TODAY
          </a>
          <a href="/Schedule" class:active={currentPage === '/Schedule'} on:click={() => (currentPage = '/Schedule')}>
            SCHEDULE
          </a>
  
          <button class="mode-toggle" on:click={toggleDarkMode}>
            <div
              class="bx bxs-sun"
              style="background-color: var(--bck); color: var(--wht);"
            ></div>
            <div
              class="bx bxs-moon"
              style="background-color: var(--wht); color: var(--bck);"
            ></div>
          </button>
        </div>
      </div>
    </nav>
  </div>
  <slot />
  
  <style>
    .container {
      margin-top: 30px;
      padding: 0px 5% 0px 5%;
    }
  
    .nav {
      display: grid;
      grid-template-columns: 1fr 1fr;
    }
  
    .logo {
      font-size: var(--L);
      font-weight: 600;
      color: var(--bck);
    }
  
    .nav-link {
      display: flex;
      justify-content: flex-end;
      align-items: center;
    }
  
    .nav a {
      font-size: var(--M);
      text-decoration: none;
      color: var(--gry);
      margin-right: 16px;
    }
  
    .nav a:hover {
      color: var(--bck);
    }
  
    .mode-toggle {
      width: 80px;
      height: 40px;
      border-radius: 10px;
      border: 1px solid var(--bck);
      background-color: none;
      display: grid;
      grid-template-columns: 1fr 1fr;
    }
  
    .mode-toggle:hover {
      cursor: pointer;
    }
  
    .mode-toggle .bx {
      width: 100%;
      height: 100%;
      font-size: 20px;
      display: flex;
      justify-content: center;
      align-items: center;
      border-radius: 10px;
      transition: background-color 0.7s, color 0.7s;
      transition: color 0.5s ease;
    }
  
    .nav a.active {
      color: var(--bck);
    }
  
    @media screen and (max-width: 1000px) {
      .logo {
        font-size: var(--M);
      }
  
      .nav a {
        font-size: var(--S);
      }
  
      .mode-toggle {
        width: 60px;
        height: 30px;
        border-radius: 7px;
      }
  
      .mode-toggle .bx {
        font-size: 15px;
        border-radius: 7px;
      }
    }
  
    @media screen and (max-width: 600px) {
      .logo {
        font-size: var(--S);
      }
  
      .nav a {
        font-size: var(--XS);
      }
  
      .mode-toggle {
        width: 40px;
        height: 20px;
        border-radius: 5px;
      }
  
      .mode-toggle .bx {
        font-size: 10px;
        border-radius: 5px;
      }
    }
  </style>
  