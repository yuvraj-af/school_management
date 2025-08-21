<script>
  import { page } from '$app/stores';
  
</script>

<header>
  <h1>🏫 My School Management System</h1>
</header>

<main>
  <slot />
</main>

<footer>
  <p>© 2025 My School. All Rights Reserved.</p>
</footer>


<style>
  header {
    text-align: center;
    background: #2c3e50;
    color: white;
    padding: 0.5rem 0;
  }

  main {
  max-height: 60vh;
  display: flex;
  flex-direction: column; /* stack content naturally */
  justify-content: flex-start;
  padding: 2rem;
  }

  footer {
    text-align: center;
    background: #34495e;
    color: #bdc3c7;
    padding: 1rem 0;
  }
</style>