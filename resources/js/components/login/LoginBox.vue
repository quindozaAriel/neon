<template>
  <b-container fluid>
    <b-row class="d-flex justify-content-center align-items-center full-screen">
      <b-col md="4">
        <div class="login__box">
          <b-form>
            <label class="mb-4">NEON</label>
            <input
              class="login__inputs w-50 mb-4"
              type="text"
              placeholder="Enter username"
            />
            <input
              class="login__inputs w-50"
              type="password"
              placeholder="Enter password"
            />
            <a class="mt-3 link">Forgot Password ?</a>
            <button class="login__btn mt-4" type="submit">
              <span></span>
              <span></span>
              <span></span>
              <span></span>
              LOGIN
            </button>
          </b-form>
        </div>
      </b-col>
    </b-row>
  </b-container>
</template>
<script>
export default {
  data() {
    return {
      username:'',
      password:'',
    };
  },
};
</script>
<style lang="scss">
@import "../../../sass/general";

.full-screen {
  height: 100vh;
  overflow: hidden;
  background: #d1d9dc;
}

.login__box {
  background-image: linear-gradient(to right, #1d353d, #2a4e5d);
  height: 500px;
  position: relative;
  width: 100%;
  overflow: none;
}

.login__box::after {
  content: "";
  animation: spin 8s ease-in-out forwards;
  background: #d1d9dc;
  border-radius: 30%;
  bottom: -20%;
  height: 200%;
  left: -50%;
  position: absolute;
  width: 200%;
}

@keyframes spin {
  0% {
    transform: translateY(0) rotate(0deg);
  }
  100% {
    transform: translateY(-100%) rotate(500deg);
  }
}

form {
  align-items: center;
  display: flex;
  flex-direction: column;
  height: 100%;
  justify-content: center;
  width: 100%;
}

label {
  color: #30a5ab;
  font-size: 3rem;
}

.login__inputs {
  background-image: linear-gradient(to right, #355863, #56818e);
  border: 0;
  color: white;
  height: 40px;
  outline: none;
  padding: 5px;
  text-align: center;
  transition: 0.5s;
  width: 100%;
}

.login__inputs::placeholder {
  color: rgb(172, 172, 172);
}

.login__inputs:focus {
  -moz-box-shadow: 0 0 15px 5px rgb(26, 165, 170);
  -webkit-box-shadow: 0 0 15px 5px rgb(26, 165, 170);
  box-shadow: 0 0 15px 5px rgb(26, 165, 170);
}

.link {
  color: #71b4c7;
  transition: 0.5s;
  cursor: pointer;
}

.link:hover {
  color: #c6d7db;
  text-decoration: none;
}

.login__btn {
  background: transparent;
  border: 1px solid #557f8c;
  color: #30a5ab;
  outline: none;
  overflow: hidden;
  padding: 10px;
  width: 50%;
  position: relative;
  transition:1s;
  span {
    position: absolute;
    display: block;
  }

  span:nth-child(1) {
    top: 0;
    left: -50%;
    width: 50%;
    height: 2px;
    background: linear-gradient(90deg, transparent, #30a5ab);
  }

  span:nth-child(2) {
    bottom: 0;
    right: -50%;
    width: 50%;
    height: 2px;
    background: linear-gradient(90deg, transparent, #30a5ab);
  }

  span:nth-child(3) {
    top: -100%;
    right: 0;
    width: 2px;
    height: 100%;
    background: linear-gradient(180deg, transparent, #30a5ab);
  }

  span:nth-child(4) {
    bottom: -100%;
    left: 0;
    width: 2px;
    height: 100%;
    background: linear-gradient(360deg, transparent, #30a5ab);
  }
}

.login__btn:focus {
  outline: none;
}

.login__btn:hover {
  span:nth-child(1) {
    left: 100%;
    transition: .5s;
  }

  span:nth-child(2) {
    right: 100%;
    transition: .5s;
  }

  span:nth-child(3) {
    top: 100%;
    transition: .5s;
    transition-delay: 0.5s;
  }

  span:nth-child(4) {
    bottom: 100%;
    transition: .5s;
    transition-delay: 0.5s;
  }

  background: #30a5ab;
  color: white;
  -moz-box-shadow: 0 0 15px 8px rgb(26, 165, 170);
  -webkit-box-shadow: 0 0 15px 8px rgb(26, 165, 170);
  box-shadow: 0 0 15px 10px rgb(26, 165, 170);
  border:0;
  transition-delay:.8s;
}
</style>