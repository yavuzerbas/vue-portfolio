<template>
  <div>
    <nav class="navbar navbar-expand-lg" :class="{'navbar-dark bg-dark': isDarkTheme, 'navbar-light bg-light': !isDarkTheme}">
      <ul class="navbar-nav mr-auto">
        <li class="nav-item">
          <router-link class="nav-link" to="/" exact>Home</router-link>
        </li>
        <li class="nav-item">
          <router-link class="nav-link" to="/contact">Contact</router-link>
        </li>
      </ul>
      <ul class="navbar-nav">
        <li class="nav-item">
          <button @click="toggleTheme" class="btn icon-button">
            <i :class="isDarkTheme ? 'fas fa-sun' : 'fas fa-moon'"></i>
          </button>
        </li>
      </ul>
    </nav>
    <router-view />

    <!-- Footer Section -->
    <footer class="footer">
      &copy; 2023 Yavuz Erbaş. All Rights Reserved.
    </footer>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isDarkTheme: false,
    };
  },
  mounted() {
    this.isDarkTheme = localStorage.getItem('theme') === 'dark';
    this.applyTheme();
    document.title = "Yavuz Erbaş";
  },
  methods: {
    toggleTheme() {
      this.isDarkTheme = !this.isDarkTheme;
      localStorage.setItem('theme', this.isDarkTheme ? 'dark' : 'light');
      this.applyTheme();
    },
    applyTheme() {
      document.body.className = this.isDarkTheme ? 'dark-theme' : '';
    },
  }
};
</script>

<style>
/* Base styles */
body {
  background-color: #fff; /* White background for light theme */
  color: #212529; /* Dark text for light theme */
  transition: background-color 0.3s, color 0.3s;
}

/* Navbar styles */
.navbar-nav {
  list-style: none;
  padding-left: 0;
  display: flex;
  flex-flow: row nowrap;
  justify-content: center;
  margin-bottom: 0;
}

.nav-item {
  margin: 0 0.5rem;
}

.nav-link {
  color: inherit;
  text-decoration: none;
  transition: color 0.3s ease-in-out;
}

/* Active link style */
.navbar-nav .nav-link.router-link-exact-active,
.navbar-nav .nav-link.router-link-exact-active:hover {
  font-weight: bold;
  font-size: 1.006em;
  border-bottom: 3px solid #42b983;
}

/* Dark theme styles */
.dark-theme {
  background-color: #343a40;
  color: #f8f9fa;
}

.dark-theme .navbar {
  background-color: #212529;
}

.dark-theme .navbar-nav .nav-link {
  color: #f8f9fa;
}

/* Icon button styles */
.icon-button {
  background: none;
  border: none;
  cursor: pointer;
}

/* Icon styles for visibility in both themes */
.icon-button i {
  font-size: 1.25em;
}

/* Ensure icons are visible at all times in light theme */
.navbar-light .navbar-nav .nav-link .fas,
.navbar-light .navbar .btn.icon-button .fas {
  color: #212529; /* Dark color for icons in light theme */
}

/* Ensure icons are visible at all times in dark theme */
.dark-theme .navbar-nav .nav-link .fas,
.dark-theme .navbar .btn.icon-button .fas {
  color: #f8f9fa; /* Light color for icons in dark theme */
}

/* Align the toggle theme button to the right */
.navbar .navbar-nav {
  align-items: center;
}

.navbar .navbar-nav:last-child {
  margin-left: auto;
}

/* Footer styles */
.footer {
  text-align: center;
  padding: 15px 0;
  font-size: 0.9em;
  background-color: #f8f9fa; /* Light background for light theme */
  color: #212529; /* Dark text for light theme */
  transition: background-color 0.3s, color 0.3s;
}

.dark-theme .footer {
  background-color: #212529; /* Dark background for dark theme */
  color: #f8f9fa; /* Light text for dark theme */
}
</style>
