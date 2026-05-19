---
layout: post
title: "Photography 📸"
categories: misc
---

<!-- Africa
- [Marrakech](photography/marrakech.md) 


Central / South America
- [Cancun](photography/cancun.md)
- [Peru](photography/cusco.md)

Europe
- [Budapest](photography/budapest.md)
- [Vienna](photography/vienna.md)

North America
- [Pittsburgh](photography/pittsburgh.md)
- [New york](photography/newyork.md)
- [Las Vegas](photography/vegas.md)
- [Toronto](photography/toronto.md)
 --><div id="carousel" style="max-width: 4000px; margin: auto; text-align: center;">
  <style>
    #carousel {
      display: flex;
      flex-direction: column; /* Stack the images and captions */
      justify-content: center; /* Center items vertically */
      align-items: center; /* Center items horizontally */
    }

    .carousel-image {
      width: auto; /* Prevent the image from exceeding the container width */
      height: 500px; /* Set a fixed height */
      display: none; /* Hide inactive images */
      object-fit: cover; /* Maintain aspect ratio while filling the container */
    }

    .carousel-image.active {
      display: block; /* Show active image */
    }

    .carousel-caption {
      font-size: 14px; /* Smaller font size */
      color: #555; /* Softer color */
      margin-top: 10px;
      display: flex; /* Flex layout */
      justify-content: center; /* Center items horizontally */
      align-items: center; /* Align arrows and text vertically */
      gap: 10px; /* Space between arrows and text */
    }

    .carousel-caption button {
      background: none; /* No background for buttons */
      border: none; /* No border */
      color: black; /* Default color */
      font-size: 20px; /* Arrow size */
      cursor: pointer; /* Pointer cursor */
      transition: color 0.3s ease; /* Smooth hover effect */
    }

    .carousel-caption button:hover {
      color: #007bff; /* Highlight on hover */
    }
  </style>

  <!-- Images -->
  <img src="pics/slideshows/00.jpg" class="carousel-image active">
  <img src="pics/slideshows/01.jpg" class="carousel-image">
  <img src="pics/slideshows/02.jpg" class="carousel-image">
  <img src="pics/slideshows/03.jpg" class="carousel-image">
  <img src="pics/slideshows/04.jpg" class="carousel-image">
  <img src="pics/slideshows/05.jpg" class="carousel-image">
  <img src="pics/slideshows/06.jpg" class="carousel-image">
  <img src="pics/slideshows/07.jpg" class="carousel-image">
  <img src="pics/slideshows/08.jpg" class="carousel-image">
  <img src="pics/slideshows/09.jpg" class="carousel-image">
  <img src="pics/slideshows/10.jpg" class="carousel-image">
  <img src="pics/slideshows/11.jpg" class="carousel-image">

  <!-- Caption with arrows -->
  <div id="carouselCaption" class="carousel-caption">
    <button onclick="prevImage()">&#8592;</button>
    <span>Marrakech</span>
    <button onclick="nextImage()">&#8594;</button>
  </div>

  <script>
    const images = document.querySelectorAll('.carousel-image');
    const captions = [
      'Copenhagen 2025',
      'Cancun 2024'
      'Ha Long Bay 2024',
      'San Juan 2026',
      'NYC 2024',
      'Mexico City 2025',
      'Bangkok 2024',
      'Hanoi 2024 ',
      'Lima 2024',
      'Marrakech 2024',
      'Marrakech 2024',
      'Marrakech 2024',
    ];
    const captionText = document.querySelector('#carouselCaption span');
    let currentIndex = 0;

    function showImage(index) {
      images.forEach((img, i) => img.classList.toggle('active', i === index));
      captionText.textContent = captions[index];
    }

    function nextImage() {
      currentIndex = (currentIndex + 1) % images.length;
      showImage(currentIndex);
    }

    function prevImage() {
      currentIndex = (currentIndex - 1 + images.length) % images.length;
      showImage(currentIndex);
    }
  </script>