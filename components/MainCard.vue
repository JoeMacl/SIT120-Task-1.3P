<template>

<div class="main-container">
        <div class="container-one">
            <div class="profile">
                <img src="../assets/face.jpg" alt="">
                <h3>Joe Maclean</h3>
                <p>Software Developer</p>
        </div>
        <div class="social-links">
                <div class="link">
                <img src="../assets/github.webp" alt="">
                <a href="">
                    <h2>Github</h2>
                </a>
            </div>
                <div class="link">
                <img src="../assets/linkin.png" alt="">
                <a href="">
                    <h2>LinkedIn</h2>
                </a>
            </div>
                <div class="link">
                <img src="../assets/x.png" alt="">
                <a href="">
                    <h2>X</h2>
                </a>
            </div>
                <div class="link">
                <img src="../assets/ins.png" alt="">
                    <h2>Instagram</h2>
                </div>
            </div>
        </div>
    
        <div class="container-two">
            <div class="about-me">
                <h1>{{ headingText }}</h1>
                <p> {{ currentText }}
                </p>
                <br>
            </div>
            <div class="technology-section">
                <h1>Technologies Studied</h1>
                <br>
                <div class="logos">
                    <img src="../assets/j.png" alt="">
                    <img src="../assets/ht.png" alt="">
                    <img src="../assets/cs.png" alt="">
                </div>

            </div>
            <div class="button-container">
                <div class="projects-button">
                    <a href="#" @click="toggleText('My Resume')">My Resume</a>
                </div>
                <div>
                    <div class="projects-button">
                        <a href="#" @click="toggleText('About Me')">About Me</a>

                </div>
                </div>
            </div>
        </div>
    </div>
    
</template>

<script>

export default {
  data() {
    return {
      originalHeading: "About Me",
      originalText: "I am presently enrolled as a student at Deakin University, pursuing a computer science degree. I have proficiency in a variety of programming languages, including C++, C#, Java, CSS, Python, and more. I am a passionate and diligent individual, and I invite you to explore my portfolio, showcasing my previous projects and works.",
      resumeText: "As a computer science student, I'm dedicated to expanding my skills and knowledge in programming, software development, and problem-solving. Proficient in languages like Python, Java, and C++, I've tackled diverse projects, from web applications to algorithm optimization. My passion for technology is complemented by my strong analytical thinking and teamwork abilities. Eager to contribute to innovative projects and eager to learn and adapt to new challenges. I am currently pursuing my degree in computer science, driven to make a meaningful impact in the tech industry.",
      currentText: "I am presently enrolled as a student at Deakin University, pursuing a computer science degree. I have proficiency in a variety of programming languages, including C++, C#, Java, CSS, Python, and more. I am a passionate and diligent individual, and I invite you to explore my portfolio, showcasing my previous projects and works.",
      headingText: "About Me"
    };
  },
  methods: {
    toggleText(buttonText) {
      if (buttonText === "My Resume") {
        this.headingText = "My Resume";
        this.currentText = this.resumeText;
      } else {
        this.headingText = "About Me";
        this.currentText = this.originalText;
      }
    }
  }
};

</script>

<style scoped>


    img {
        height: 20px;
    }

    .main-container {
        height: 80vh; 
        width: 100%;
        display: flex;
        flex-direction: row;
        background-color: #efe9e2;
        border-radius: 25px;
        margin-top: 15%;
        background-color: #887a7a;
        box-shadow: rgba(0, 0, 0, 0.25) 0px 3px 8px;
    }

    .container-one {
        background-color: #c0b8b8;
        padding: 2.5%;
        width: 30%;
        border-radius: 25px;
        box-shadow: rgba(0, 0, 0, 0.25) 0px 3px 8px;

    }

    .container-two {
        background-color: 	#c0b8b8;
        width: 100%;
        margin: 3%;
        border-radius: 20px;
        box-shadow: rgba(0, 0, 0, 0.25) 0px 3px 8px;
    }

    .about-me {
        text-align: left;
    }

    .profile img {
        height: 7rem;
        border-radius: 50%;
        display: block;
        margin: 0 auto;

    }
    

    .social-links {
        align-self: center;
        margin-top: 1%;
    }

    .link {
        text-align: center;         
        margin: 10px;
    }

    .link a {
        text-decoration: none;
        color: black;
        font-size: 12px;
    }

    .link img {
        height: 2rem;
    }

    .logos {
        text-align: center;
    }

    .logos img {
        height: 2rem;
    }

    .technology-section {
        align-self: center;
    }

    .button-container {
        margin-top: 5%;
        display: flex;
        flex-direction: row;
        justify-content: center;
        align-items: center;
    }

    .projects-button {
        background-color: black;
        border-radius: 15px;
        padding: 5px;
        margin: 4px;
    }

    .projects-button a{
        text-decoration: none;
        color: white;
    }

    @media only screen and (max-width: 950px) {
        .main-container {
            width: 95%;
        }
    }

    h3 {
        text-align: center;
        margin-top: 5%;
    }

    p {
        text-align: center;
    }

    h2 {
        text-align: center;
    }

    h1 {
        text-align: center;
    }

    P {
        padding-left: 4%;
        padding-right: 4%;
    }

    
</style>