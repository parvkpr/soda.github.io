---
layout: page
permalink: /
# subtitle:
# #<a href='#'>Affiliations</a>. Address. Contacts. Moto. Etc.

# profile:
#   align: left
#   image: prof_pic.jpg
#   address: 

news: true  # includes a list of news items
# selected_papers: false # includes a list of papers marked as "selected={true}"
# social: true  # includes social icons at the bottom of the page
---
We research and develop tools for software assurance and design at [Carnegie Mellon University](https://www.cmu.edu/) led by Professor [Eunsuk Kang](https://eskang.github.io/) . We are a part of the [Software and Societal Systems Department](https://s3d.cmu.edu/) in  the [School of Computer Science](https://www.cs.cmu.edu/). 

If you are interested in joining our lab, please fill out [this form](https://docs.google.com/forms/d/e/1FAIpQLSddQ--uka2G7yDAaOrrtqH5BmBMmCAhq7GZp6zbwzG2ZXg1wA/viewform?usp=sf_link). 



<div class="slideshow-container">
  <div class="mySlides fade">
    <img src="assets/img/team.jpg" style="width:100%">
  </div>

  <div class="mySlides fade">
    <img src="assets/img/soda_logo.webp" style="width:100%">
  </div>

  <div class="mySlides fade">
    <img src="assets/img/eunsuk_cool_sweater.jpg" style="width:100%">
  </div>

  <!-- Next and previous buttons -->
  <a class="prev" onclick="plusSlides(-1)">&#10094;</a>
  <a class="next" onclick="plusSlides(1)">&#10095;</a>
</div>
<br>

<!-- The dots/circles -->
<div style="text-align:center">
  <span class="dot" onclick="currentSlide(1)"></span> 
  <span class="dot" onclick="currentSlide(2)"></span> 
  <span class="dot" onclick="currentSlide(3)"></span> 
</div>

<script>
var slideIndex = 1;
showSlides(slideIndex);

// Next/previous controls
function plusSlides(n) {
  showSlides(slideIndex += n);
}

// Thumbnail image controls
function currentSlide(n) {
  showSlides(slideIndex = n);
}

function showSlides(n) {
  var i;
  var slides = document.getElementsByClassName("mySlides");
  var dots = document.getElementsByClassName("dot");
  if (n > slides.length) {slideIndex = 1}    
  if (n < 1) {slideIndex = slides.length}
  for (i = 0; i < slides.length; i++) {
      slides[i].style.display = "none";  
  }
  for (i = 0; i < dots.length; i++) {
      dots[i].className = dots[i].className.replace(" active", "");
  }
  slides[slideIndex-1].style.display = "block";  
  dots[slideIndex-1].className += " active";
}

</script>