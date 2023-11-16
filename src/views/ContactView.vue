<template>
  <div class="container">
    <p>You can contact me or follow me from the following links:</p>
    <div class="contact-info">
      <p>
        <i class="fab fa-linkedin"></i>
        <a href="https://www.linkedin.com/in/yavuz-erbas/" target="_blank" rel="noopener noreferrer">LinkedIn</a>
      </p>
      <p>
        <i class="fas fa-envelope"></i>
        <a href="mailto:yavuz0erbas@gmail.com">Email</a>
      </p>
      <p>
        <i class="fab fa-github"></i>
        <a href="https://github.com/yavuzerbas" target="_blank" rel="noopener noreferrer">Github</a>
      </p>
      <p>
        <i class="fab fa-youtube"></i>
        <a href="https://www.youtube.com/channel/UCQv0s2cg9SRv6FIZIDKJuxQ" target="_blank" rel="noopener noreferrer">YouTube</a>
      </p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'ContactView'
}
</script>

<style scoped>
.container {
  display: flex;
  flex-direction: column;
  align-items: center; /* Centers content horizontally */
  height: 100vh;
}

.contact-info {
  text-align: center; /* Center align text and icons */
}

.contact-info p {
  display: flex; /* Makes <p> a flex container */
  justify-content: center; /* Centers the flex items horizontally */
  align-items: center; /* Centers the flex items vertically (useful if icons and text have different heights) */
  margin: 10px 0;
}

.contact-info i {
  margin-right: 5px;
}

.contact-info a {
  color: inherit; /* Inherit the color from parent elements */
  text-decoration: none; /* Removes the underline from links */
}

.contact-info a:hover {
  text-decoration: underline; /* Adds an underline on hover */
}
</style>
