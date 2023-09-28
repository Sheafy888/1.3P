<template>

  <section class="about-me-page">
    <div class="profile-image">
      <img src="../assets/aboutme.jfif" alt="profile" style="max-width:70%; height:auto;">
    </div>
    <div class="about-content">
      <h1>About Me</h1>
      <p>My name is Tyler Sheaf and I am currently a second year student studying Information Technology at Deakin University on the Geelong Campus. In my studies, I have chosen to do a
        major in cyber security as the main direction in my course. Some of my hobbies are AFL, Soccer, Speedway, Traveling and Gaming. Some of my hobbies I am involved with it such as 
        Soccer and speedway as I am involved with a team for both sports. I have inserted an image of another hobby of mine, this image was taken when I was in Canada sightseeing before 
        attending a wedding.</p> <br>

      <!-- <div class="profile-picture">
      <img src="../assets/aboutme.jfif" alt="profile" style="max-width:70%; height:auto;">
      </div> -->

      <p>Below this is a button to recieve my CV. This is what I have previously studied or work at. PS: I have put a tempory file as I didn't have access to my actual cv.</p>
      <button class="download-btn" @click="downloadFile">Download my resume</button>
      <p>
        Thanks for visiting, feel free to email <a href="mailto:tsheaf@deakin.edu.au"> for a conversation</a>
      </p>
    </div>
  </section>
</template>

<script>
export default {
  methods: {
    downloadFile(){
      const filePath = '../cv.pdf';

      const link = document.createElement('a');
      link.href = filePath;
      link.setAttribute('download', 'MyCV.pdf');
      link.style.display = 'none';

      document.body.appendChild(link);
      link.click();

      document.body.removeChild(link);
    },
  },
};
</script>
