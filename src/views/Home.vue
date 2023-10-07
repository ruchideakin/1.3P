<template>
  <div class="container">
    <div id="name-container">
      <img id="avatar" src="./../assets/logos/icons8-female-48.png" alt="avatar" />
      <h1>Ruchika Bhimani</h1>
    </div>
    <div class="title-desc-container">
      <a id="github" href="https://github.com/ruchideakin" target="_blank" rel="noopener noreferrer"
        ><img class="title-font" src="./../assets/images/github.svg" />Developer</a
      >
      <span>/</span>
      <a id="linkedin" href="http://linkedin.com/in/ruchi-bhimani-97b995286" target="_blank" rel="noopener noreferrer"
        ><img class="title-font" src="./../assets/logos/linkedin.png" />Linkedin</a
      >
    </div>
    <div class="article">
      <h2>WHO AM I</h2>
      <p>
        I'm <i>Ruchika Bhimani</i>. Open and friendly person who approaches addressing normal requirements and overcoming unique problems with composure and objectivity. Employee with a strong drive to take on new tasks. Strong work ethic, flexibility, and outstanding social skills. 
      </p>

      <h2>Academics</h2>
      <ul>
        <li>
          🙇 Student at Deakin University
        </li>
        <li>Bachelor of Information Technology 2023-2026</li>
        <li>🔭 <b>Fields of interest:</b> Web Development / Food Tasting</li>
      </ul>

      <h2>Experience</h2>
      <ul>
        <b>FORK AND SPOON RESTAURANT</b>
        <li>June 2022 – Nov 2022</li>
        <li>Position: Kitchen Hand</li>
        <li>Description: Ensuring Customer Satisfaction,
Collaborating within fast-paced team environment
</li>
      </ul>

      <h2>Skills</h2>
      <p>
       I possess a well-rounded skill set, including strong communication, problem-solving, and customer service abilities. I excel in multitasking, collaborate effectively in teams, and have a rapid learning curve. Efficient time management ensures timely task completion. My approach to complaint handling is empathetic and solution-oriented. I demonstrate leadership qualities and adapt seamlessly to changing situations, reflecting my flexibility.
      </p>

      <h2>Contacts</h2>
      <ul>
        <li>
          <b>Email：</b>
          <a href="mailto:spencer.wushangbo@gmail.com">s223685406@deakin.edu.au</a><i> (Preferred)</i>
        </li>
      </ul>
    </div>
  </div>
</template>

<style lang="css" scoped>
#name-container {
  display: flex;
  flex-direction: row;
  justify-content: flex-start;
  align-items: center;
}

#avatar {
  width: 42px;
  height: 42px;
  border-radius: 50%;
  margin-right: 12px;
}

#copyright:hover {
  border: none;
}

.title-font {
  width: 16px;
  height: 16px;
  margin-right: 4px;
}

.title-desc-container {
  display: flex;
  align-items: center;
  justify-content: flex-start;
  margin: 8px 0;
}

.title-desc-container a {
  display: flex;
  align-items: center;
}

.title-desc-container span {
  margin: 0px 4px;
}

.title-desc-container #github {
  color: #24292e;
}

.title-desc-container #sspai {
  color: #ca2c2a;
}

.title-desc-container #blog {
  color: #0070f3;
}
</style>
