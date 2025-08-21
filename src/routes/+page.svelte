<script>

  import { goto } from '$app/navigation';

  const routes = ['/student', '/teacher', '/parent', '/admin'];

  function handleLogin() {
    goto(routes[selected]);
  }

  let selected = 0; 
</script>

<div class="login-container">
  <select bind:value={selected}>
    <option value="0">Student</option>
    <option value="1">Teacher</option>
    <option value="2">Parent</option>
    <option value="3">Admin</option>
  </select>

  <input type="text" placeholder="Username" />
  <input type="password" placeholder="Password" />

  <p>variable value: {selected}</p>

  <button on:click={handleLogin}>Login</button>
</div>

<style>
  .login-container {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 1rem;
    width: 300px;
    margin: 5rem auto; /* centers vertically & horizontally */
    padding: 2rem;
    border: 1px solid #ddd;
    border-radius: 12px;
    background: #f9f9f9;
    box-shadow: 0 4px 12px rgba(0,0,0,0.1);
  }

  select, input {
    width: 100%;
    padding: 0.6rem 0.8rem;
    font-size: 1rem;
    border-radius: 6px;
    border: 1px solid #ccc;
  }

  select:focus, input:focus {
    outline: none;
    border-color: #3498db;
    box-shadow: 0 0 4px #3498db;
  }

  button {
    width: 100%;
    padding: 0.7rem 0;
    font-size: 1.1rem;
    font-weight: bold;
    color: white;
    background-color: #3498db;
    border: none;
    border-radius: 6px;
    cursor: pointer;
    transition: background 0.2s;
  }

  button:hover {
    background-color: #2980b9;
  }
</style>
