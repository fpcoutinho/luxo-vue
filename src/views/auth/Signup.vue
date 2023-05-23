<template>
  <main>
    <form @submit="signup">
      <form-header>
        <h2>Cadastrar</h2>
      </form-header>
      <form-group>
        <label for="name">Nome</label>
        <input type="text" id="name" name="name" required />
        <div class="name error"></div>
        <label for="surname">Sobrenome</label>
        <input type="text" id="surname" name="surname" required />
        <div class="surname error"></div>
      </form-group>
      <form-group>
        <label for="email">E-mail</label>
        <input type="email" id="email" name="email" required />
        <div class="email error"></div>
      </form-group>
      <form-group>
        <label for="dataNascimento">Data de Nascimento</label>
        <input type="date" id="dataNascimento" name="dataNascimento" required />
        <div class="dataNascimento error"></div>
      </form-group>
      <form-group>
        <label for="password">Senha</label>
        <input type="password" id="password" name="password" required />
        <div class="password error"></div>
      </form-group>
      <form-group>
        <label for="confirmPassword">Confirmar Senha</label>
        <input
          type="password"
          id="confirmPassword"
          name="confirmPassword"
          required
        />
        <div class="confirmPassword error"></div>
      </form-group>
      <form-group>
        <button type="submit">Sign Up</button>
      </form-group>
    </form>
  </main>
</template>

<script>
export default {
  name: 'Signup',
  data() {
    return {
      name: '',
      surname: '',
      email: '',
      dataNascimento: '',
      password: '',
      confirmPassword: '',
    }
  },
  methods: {
    async signup(e) {
      e.preventDefault()
      const name = form.name.value
      const surname = form.surname.value
      const email = form.email.value
      const dataNascimento = form.dataNascimento.value
      const password = form.password.value
      const confirmPassword = form.confirmPassword.value

      try {
        const res = await fetch('/auth/signup', {
          method: 'POST',
          body: JSON.stringify({
            name,
            surname,
            email,
            dataNascimento,
            password,
            confirmPassword,
          }),
          headers: { 'Content-Type': 'application/json' },
        })
        const data = await res.json()

        if (data.errors) {
          nameError.textContent = data.errors.name
          surnameError.textContent = data.errors.surname
          emailError.textContent = data.errors.email
          dataNascimentoError.textContent = data.errors.dataNascimento
          passwordError.textContent = data.errors.password
          confirmPasswordError.textContent = data.errors.confirmPassword
        }
        if (password !== confirmPassword) {
          document.querySelector('.confirmPassword.error').textContent =
            'As senhas não coincidem.'
        }
        if (data.user) {
          location.assign('/')
        }
      } catch (err) {
        console.log(err)
      }
    },
  },
}
</script>

<style scoped>
a {
  color: var(--rosa);
  text-decoration: none;
}

a:hover {
  text-decoration: underline;
}

h2 {
  color: var(--h);
}

ul {
  padding: 0;
  display: flex;
  gap: 1rem;
}

li {
  list-style: none;
}

form {
  width: 400px;
  margin: 0 auto;
  padding: 30px;
  box-shadow: 1px 2px 3px rgba(0, 0, 0, 0.1);
  border-radius: 10px;
  background: white;
}
form button {
  margin: auto;
  margin-top: 10px;
}
form a {
  display: block;
  text-align: center;
  margin-top: 20px;
  color: #999;
  font-size: 0.8em;
}
form a:hover {
  color: #333;
}
input,
select,
textarea {
  padding: 10px 12px;
  border-radius: 4px;
  border: 1px solid #ddd;
  font-size: 1em;
  width: 100%;
}
select {
  width: 26.67em;
}
label {
  display: block;
  margin: 20px 0 10px;
}
button {
  margin-top: 30px;
  border-radius: 36px;
  background-color: var(--h);
  color: var(--bg);
  border: 0;
  text-transform: uppercase;
  font-weight: 700;
  font-size: 0.8em;
  display: block;
  padding: 10px 16px;
  letter-spacing: 2px;
}
.error {
  color: #ff0099;
  margin: 10px 2px;
  font-size: 0.8em;
  font-weight: bold;
}

form-group button:hover {
  background-color: var(--h-hover);
}

@media screen and (min-width: 768px) {
  main {
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 1rem;
    margin: 1rem;
  }
}
</style>
