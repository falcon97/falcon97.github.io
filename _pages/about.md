---
permalink: /about/
title: "About"
excerpt: "About Kishore."
author_profile: true
layout: single
classes: wide
search: true
---

I am a Data Science aficionado, open to new experiences that help build my career as a Data Scientist.

As a self-motivated and constant learner, I have learned to be highly adaptable and collaborative in all kinds of situations. I strongly believe I have a lot of offer as I work towards utilizing opportunities that help me become a valuable asset in the industry.

When I am not coding, you can find me clicking photos, playing music, or visiting new places.

You can reach out to me by filling out the contact form below.

<a name="contact"></a>
{% comment %}
<iframe src="https://docs.google.com/forms/d/e/1FAIpQLScNIcD3ZhCw-LfmiIejyEQNch1WhCrdmBLKt2Cygd8L_PWNtQ/viewform?embedded=true" width="100%" height="822" frameborder="0" marginheight="0" marginwidth="0">Loading...</iframe>
{% endcomment %}
<div class="container">
      <form id="contactForm" class="mt-4" role="form" action="javascript:onSubmit(emailInput, nameInput, messageInput)">
        <div class="form-ground">
          <label for="nameInput">Name</label>
          <input type="text" class="form-control" id="nameInput" placeholder="Name">
        </div>
        <div class="form-group">
          <label for="emailInput">Email</label>
          <input type="email" class="form-control" id="emailInput" placeholder="name@example.com">
        </div>
        <div class="form-group mt-4">
          <label for="messageInput">Message</label>
          <textarea class="form-control" id="messageInput" rows="3" maxlength="500" style="resize: none;"></textarea>
        </div>
        <button type="submit" class="btn btn-primary">Send</button>
        <div class="form-ground" id="sendmsg" style="display: none;"> 
          Thank you for your message! I will reach out to you if necessary.
        </div>
      </form>
</div>

<script src="https://www.gstatic.com/firebasejs/8.7.1/firebase-app.js"></script>

<script src="https://www.gstatic.com/firebasejs/8.7.1/firebase-database.js"></script>

<script src="https://www.gstatic.com/firebasejs/8.7.1/firebase-app-check.js"></script>

<script>
  var firebaseConfig = {
    apiKey: "AIzaSyAYMuSplx4X83Cvin17p9hzLV7PsD29RcQ",
    authDomain: "github-portfolio-68ede.firebaseapp.com",
    projectId: "github-portfolio-68ede",
    storageBucket: "github-portfolio-68ede.appspot.com",
    messagingSenderId: "192270304814",
    appId: "1:192270304814:web:0ff8821d460a7c94b001bf"
  };
  firebase.initializeApp(firebaseConfig);
  const appCheck = firebase.appCheck();
  appCheck.activate('6LfaYoQbAAAAAOkhxEMoPBXZvTWeC460quqWSj9R');
</script>
<script type="text/javascript">
      function onSubmit(email, name, message) {
        firebase.database().ref("message").push().set({
          "timestamp": firebase.database.ServerValue.TIMESTAMP,
          "email": email.value,
          "name": name.value,
          "message": message.value
        });
        
        var x = document.getElementById("sendmsg");
        if (x.style.display === "none") {
          x.style.display = "block";
        } else {
          x.style.display = "none";
        }
        // clear the input.
        document.getElementById("contactForm").reset();
        setTimeout(() => { x.style.display = "none"; }, 5000);
      }
</script>
