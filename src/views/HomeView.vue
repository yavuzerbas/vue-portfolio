<template>
  <div class="container">
    <!-- Header Section -->
    <header class="header">
      <h1>Welcome</h1>
    </header>

    <!-- Introduction Section -->
    <div class="introduction">
      <p>
        Hi, I'm Yavuz Erbaş!<br> Welcome to my personal website. This website is developed with vue.js and ChatGPT prompts.<br>
        My expertise lies in mobile application development, with a focus on Android and Flutter.<br>
        Additionally, I am intrigued by various other fields such as AI and IoT.<br>
        In my free time, I enjoy team sports, computer games, and board games, though finding time can be challenging :)
      </p>
      <img src="@/assets/me.jpg" alt="Yavuz Erbaş">
      <p>I earned a B.Sc. in Computer Engineering from the Middle East Technical University in 2023, where I had the opportunity to engage in numerous beneficial courses, including Machine Learning, Computer Graphics, Information and Network Security, Computer Organization, Data Structures, Algorithms, and Object-Oriented Programming Languages.</p>
      <img src="@/assets/meGrad.jpg" alt="Yavuz Erbaş graduation">
      <p>Feel free to explore my YouTube channel for the projects I've created and participated in. Below, you can view one such project, a social media application developed with Flutter, which was part of our graduation project.</p>

      <!-- YouTube Video Embed with Wrapper -->
      <div class="video-wrapper">
        <div class="video-container">
          <iframe width="560" height="315" src="https://www.youtube.com/embed/02O4UkQx-Ts" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
        </div>
      </div>
      <p> You can find links to all of my projects in Contact page.</p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HomeView'
}
</script>

<style scoped>
.container {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: flex-start;
  min-height: 100vh;
}

.header {
  width: 100%;
  padding: 20px 0;
  text-align: center;
  color: inherit;
}

.introduction {
  text-align: center;
  margin-top: 20px;
}

.introduction img {
  width: 300px;
  height: auto;
  border-radius: 5%;
  margin-bottom: 20px;
}

.introduction p + p {
  margin-top: 20px;
}

.softassist-link {
  color: #3498db;
  text-decoration: none;
}

.softassist-link:hover {
  text-decoration: underline;
}

.video-wrapper {
  margin-bottom: 20px; /* Adds space below the video */
}

.video-container {
  position: relative;
  overflow: hidden;
  width: 100%;
  padding-top: 56.25%; /* 16:9 Aspect Ratio */
}

.video-container iframe {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
}
</style>
