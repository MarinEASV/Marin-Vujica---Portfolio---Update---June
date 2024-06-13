<template>
  <section id="contact">
  <footer>
    <p>Let’s work together and make good looking and useful design for your future projects.</p>
    <div class="contact-links">
        <a href="mailto:vujica@gmail.com" class="mail">vujojr@gmail.com</a>
        <a href="https://www.linkedin.com/in/marin-vujica/" class="app-link">Let's connect on Linkedin</a>
    </div>
  </footer>
</section>
</template>

<script>
export default {
  name: 'FooterView'
};
</script>

<style scoped>
footer {
  padding: 20px;
  background-color: #e1ede1;
  text-align: center;
}

p {
  font-size: 30px;
  font-weight: bold;
  margin: 30px;
  color: #384b47;
}

a {
  color: #384b47;
  font-size: 20px;
  text-decoration: none;

}

.mail:hover {
  text-decoration: underline;
}

.app-link {
  display: inline-block;
  margin-top: 10px;
  margin-bottom: 20px;
  padding: 10px 20px;
  background-color: #384b47;
  color: #d3e8d7;
  text-decoration: none;
  transition: background-color 0.5s;
}

.app-link:hover {
  background-color: #d3e8d7;
  color: #384b47;
  border-color: #384b47;
  border-style: solid;
}

.contact-links {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 10px;
}
</style>
