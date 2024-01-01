<script lang="ts">
    import { onMount } from "svelte";

    onMount(() => {
        
    });

    function handleSubmit() {
        window.location.href = "/Schedule";
    }
</script>

<div class="container">
  <div class="box">
    <div class="logo">
      <img src="/Logo.png" alt="logo" />
    </div>
    <h1>CREATE ACCOUNT</h1>
    <form>
      <div class="input-group">
        <label for="username">Username</label>
        <input
          type="text"
          id="username"
          name="username"
          placeholder="Enter your username"
        />
      </div>
      <div class="input-group">
        <label for="password">Password</label>
        <input
          type="password"
          id="password"
          name="password"
          placeholder="Enter your password"
        />
      </div>
      <div class="input-group">
        <label for="password">Confirm Password</label>
        <input
          type="password"
          id="Comfirm-Password"
          name="password"
          placeholder="Confirm your password"
        />
      </div>
      <div>
        <input type="submit" value="CREATE ACCOUNT" on:click={handleSubmit} />
      </div>
    </form>
    <p style="text-align: center;">
      Already have an account? <a href="/Login">Login</a>
    </p>
  </div>
</div>

<style>
  .container {
    width: 100%;
    height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
  }

  .box {
    box-shadow: 0px 0px 10px 0px rgba(0, 0, 0, 0.1);
    border: 1px solid var(--gry);
    background-color: var(--wht);
    width: 400px;
    padding: 40px;
    border-radius: 10px;
  }

  form {
    display: flex;
    flex-direction: column;
    align-items: center;
  }

  .logo {
    display: flex;
    justify-content: center;
    align-items: center;
    margin-bottom: 20px;
  }

  img {
    width: 80px;
    height: 80px;
  }

  h1 {
    text-align: center;
    font-family: var(--head);
    font-size: var(--M);
    color: var(--bck);
    margin-bottom: 20px;
  }

  .input-group {
    margin-bottom: 10px;
    text-align: left;
  }

  label {
    font-family: var(--txt);
    font-size: var(--XS);
    color: var(--bck);
    margin-bottom: 3px;
    font-weight: 500;
  }

  input {
    width: 300px;
    padding: 10px;
    margin: 5px 0;
    border: 1px solid var(--gry);
    background-color: var(--wht);
    color: var(--bck);
    border-radius: 5px;
    font-family: var(--txt);
    font-size: var(--XS);
  }

  input[type="submit"] {
    background-color: var(--bck);
    font-family: var(--head);
    font-size: var(--S);
    color: var(--wht);
    cursor: pointer;
    transition: background-color 0.3s;
    margin-top: 10px;
  }

  input[type="submit"]:hover {
    transform: translateY(-1px);
  }

  p {
    margin-top: 10px;
    font-family: var(--txt);
    font-size: var(--XS);
  }

  a {
    color: var(--bck);
  }

  a:hover {
    color: var(--gry);
  }

  @media screen and (max-width: 1000px) {
    .box {
      width: 300px;
    }

    input {
      width: 200px;
    }

    input[type="submit"] {
      width: 200px;    margin-top: 5px;
    }

    .logo {
      margin-bottom: 10px;
    }

    h1 {
      font-size: var(--S);
      margin-bottom: 5PX;
    }

    label {
      font-size: var(--XS);
    }

    input {
      font-size: var(--XS);
    }

    input[type="submit"] {
      font-size: var(--S);
    }

    p {
      font-size: var(--XS);
    }

    a {
      font-size: var(--XS);
    }

    img {
      width: 50px;
      height: 50px;
    }

    .input-group {
      margin-bottom: 5px;
    }
  }

    @media screen and (max-width: 600px) {
        .box {
        width: 250px;
        }
    
        input {
        width: 200px;
        }
    
        input[type="submit"] {
        width: 150px;
        }
    
        .logo {
        margin-bottom: 10px;
        }
    
        h1 {
        font-size: var(--XS);
        margin-bottom: 5PX;
        }
    
        label {
        font-size: var(--XXS);
        }
    
        input {
        font-size: var(--XXS);
        }
    
        input[type="submit"] {
        font-size: var(--XS);
        }
    
        p {
        font-size: var(--XXS);
        }
    
        a {
        font-size: var(--XXS);
        }
    
        img {
        width: 50px;
        height: 50px;
        }
    
        .input-group {
        margin-bottom: 5px;
        }
    }
</style>
