<template>
  <div>
    <div class="header">
      <nav class="navbar">
        <ul class="nav_links">
          <!-- Delete the unnecessary ones -->

          <li>
            <a href="#" @click="joinRoomHome">Home</a>
          </li>
          <li>
            <a href="#" @click="joinAboutUs">About us</a>
          </li>
          <!--li>
            <a href="#">Register</a>
          </li-->
        </ul>
      </nav>
    </div>
    <div class="main">
      <h1 class="h1about">Contact</h1>
      <div class="aboutus">
        <p>
          Our support team is ready to help you with any questions or comments you may have! The staff will answer incoming emails within 24 hours from Monday to Friday.
          <br />E-mail: support@itrooms.com
        </p>
      </div>
      <div class="aboutus">
        Built by Developers:
        <a
          href="https://github.com/djordjeavr"
          class="aboutus-links"
          target="_blank"
        >Djordje Avram</a>,
        <a href="https://github.com/harislapo" class="aboutus-links" target="_blank">Haris Lapo</a>,
        <a
          href="https://github.com/sminela"
          class="aboutus-links"
          target="_blank"
        >Minela Salkicevic</a>,
        <a href="https://github.com/sahaa46" class="aboutus-links" target="_blank">Emin Sahat</a>.
      </div>
    </div>
    <div class="footer">
      <p>&copy; 2020 All Rights Reserved | Design By ITAcademy Group A</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "ContactUs",
  data() {
    return {};
  },
  methods: {
    joinContactUs() {
      this.$router.push({
        name: "contactus"
      });
    },
    joinAboutUs() {
      this.$router.push({
        name: "aboutus"
      });
    },
    joinRoomHome() {
      this.$router.push({
        name: "roomhome"
      });
    }
  }
};
</script>

<style lang="scss" scoped>
.header {
  display: flex;
  justify-content: flex-end;
  align-items: center;
  padding: 5px 7%;
}
li,
a {
  font-family: "Poppins", sans-serif;
  color: #ffffff;
  text-decoration: none;
}
.nav_links {
  list-style: none;
}
.nav_links li {
  display: inline-block;
  padding: 0px 20px;
}

.nav_links li a {
  font-size: 14px;
  font-family: "Poppins", sans-serif;
  text-decoration: none;
  color: #d9cfce;
  padding: 10px 10px;
  transition: all 0.3 ease 0s;
}

.nav_links li a:hover {
  color: #ffffff;
  background-color: rgba(248, 248, 248, 0.164);
}

#contactus-white {
  color: #ffffff;
}

.main {
  position: absolute;
  left: 50%;
  top: 25%;
  transform: translate(-50%, -50%);
  width: 70%;
  .aboutus {
    color: #fff;
    font-size: 20px;
    font-family: "Poppins", sans-serif;
    text-align: center;
  }
  .aboutus-links:hover {
    color: rgb(65, 225, 240);
  }
  .h1about {
    color: #fff;
    font-size: 50px;
    font-family: "Poppins", sans-serif;
  }
  .homelink {
    float: right;
    margin: 5px 5px;
  }
  .homelink:hover {
    color: #d9cfce;
  }

  .login-form {
    border-radius: 10px;
    display: flex;
    flex-direction: row;
    justify-content: center;
    padding: 70px;

    .login {
      width: 40%;
      margin: 70px 40px 0 20px;
      h1 {
        text-align: center;
        font-family: "Poppins", sans-serif;
        letter-spacing: 2px;
        font-size: 50px;
        color: #000000;
      }

      .input-fields {
        display: flex;
        flex-direction: row;
        background-color: rgb(230, 230, 230);
        border-radius: 30px;
        margin-bottom: 10px;
        height: 50px;

        input {
          padding: 15px;
          border: none;
          outline: none;
          background-color: rgb(230, 230, 230);
          margin: 5px;
          width: 90%;
          border-radius: 30px;
          font-family: "Poppins", sans-serif;
        }
      }

      .button-field {
        button {
          padding: 15px;
          border: none;
          outline: none;
          border-radius: 30px;
          margin: 15px 5px 3px 0px;
          width: 35%;
          color: white;
          font-family: "Poppins", sans-serif;
          height: 50px;
          cursor: pointer;
          font-weight: 400;
          letter-spacing: 1px;
          transition: all 0.2 ease;
        }

        .join-btn {
          background-color: rgb(82, 187, 82);
        }

        .join-btn:hover {
          background-color: #4caf50;
        }

        .create-btn {
          background-color: rgb(26, 149, 237);
        }

        .create-btn:hover {
          background-color: rgb(52, 160, 237);
        }

        p {
          text-align: center;

          a {
            color: rgb(197, 197, 197);
            font-size: 14px;
            text-decoration: none;
          }
          a:hover {
            color: rgb(168, 168, 168);
          }
        }
      }
    }
  }
}
.footer {
  position: absolute;
  bottom: 0;
  right: 2%;
  width: 100%;
  color: #ffffff;
  font-size: 12px;
  font-family: "Poppins", sans-serif;
  display: flex;
  justify-content: flex-end;
}

/* most mobile phones */
@media only screen and (max-width: 600px) {
  .header {
    display: inline-block;
    padding: 6px;
  }

  li,
  a {
    font-size: 12px;
  }

  .nav_links li {
    margin-right: 14px;
  }

  .main {
    left: 42%;
    top: 40%;

    .login-form {
      padding: 5px;

      .login {
        width: 70%;
        margin: 100px 0px 0px 70px;
        h1 {
          font-size: 40px;
        }

        .input-fields {
          margin-top: 20px;

          input {
            text-align: center;
          }
        }

        .button-field {
          button {
            font-size: 11px;
            margin: 15px 3px 0px 0px;
            width: 45%;
            letter-spacing: 2px;
          }
        }
      }
    }
  }
  .footer {
    font-size: 13px;
    justify-content: center;
  }
}

/* most tablets and laptops*/
@media only screen and (max-width: 1200px) {
  li,
  a {
    font-size: 15px;
  }

  .main {
    left: 42%;
    top: 40%;

    .login-form {
      padding: 3px;

      .login {
        width: 50%;
        margin: 100px 0px 0px 70px;

        .input-fields {
          margin-top: 20px;

          input {
            text-align: center;
          }
        }

        .button-field {
          button {
            font-size: 13px;
            margin: 15px 3px 0px 0px;
            width: 40%;
            letter-spacing: 2px;
          }
        }
      }
    }
  }
  .footer {
    font-size: 15px;
    justify-content: center;
  }
}

/* scaling for smaller phones than usual */
@media screen and (max-width: 365px) {
  li,
  a {
    font-size: 11px;
  }

  .footer {
    font-size: 11px;
  }
}
</style>