<!DOCTYPE html><html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Muhammed Razi - Digital Assistant</title>
  <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;700&display=swap" rel="stylesheet" />
  <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css" rel="stylesheet" />
  <script src="https://cdn.jsdelivr.net/npm/sweetalert2@11"></script>
  <style>
    * {
      box-sizing: border-box;
      font-family: 'Montserrat', sans-serif;
      margin: 0;
      padding: 0;
    }
    body {
      background: linear-gradient(135deg, #e0c3fc, #8ec5fc);
      overflow-y: auto;
      color: #333;
      line-height: 1.6;
      scroll-behavior: smooth;
    }
    header {
      background: rgba(44, 62, 80, 0.85);
      color: white;
      padding: 2rem;
      text-align: center;
    }
    header img {
      width: 150px;
      height: 150px;
      border-radius: 50%;
      object-fit: cover;
      margin-bottom: 1rem;
    }
    section {
      padding: 2rem;
      background-color: rgba(255, 255, 255, 0.85);
      margin: 1rem;
      border-radius: 10px;
    }
    h2 {
      color: #2c3e50;
      margin-bottom: 1rem;
    }
    ul {
      margin-left: 2rem;
    }
    .enquiry {
      text-align: center;
      margin: 2rem 0;
    }
    .enquiry button {
      padding: 0.75rem 1.5rem;
      font-size: 1rem;
      color: white;
      background: linear-gradient(45deg, #ff9a9e, #fad0c4);
      border: none;
      border-radius: 10px;
      cursor: pointer;
      transition: transform 0.3s ease;
    }
    .enquiry button:hover {
      transform: scale(1.1);
    }
    footer {
      background-color: rgba(44, 62, 80, 0.85);
      color: white;
      text-align: center;
      padding: 1rem;
    }
    .contact-icons p i {
      margin-right: 10px;
      color: #2c3e50;
    }
    .bubble {
      position: fixed;
      bottom: -100px;
      border-radius: 50%;
      opacity: 0.6;
      animation: rise 10s infinite ease-in;
      z-index: -1;
    }
    @keyframes rise {
      0% {
        transform: translateY(0);
      }
      100% {
        transform: translateY(-120vh);
      }
    }
    a {
      color: inherit;
      text-decoration: none;
    }
  </style>
</head>
<body>
  <header>
    <img src="your-photo.jpg" alt="Muhammed Razi" />
    <h1>Muhammed Razi</h1>
    <p>Digital Assistant</p>
  </header>  <section>
    <h2>About Me</h2>
    <p>I am a digitally driven and goal-oriented individual with hands-on experience as an admission consultant, marketing assistant, and digital assistant. Currently pursuing a course in Customer Service Essentials, I also actively explore crypto trading and online platforms. With a passion for technology and communication, I stay highly engaged in the digital world, aiming to grow through continuous learning and real-world experience.</p>
  </section>  <section>
    <h2>Work Experience</h2>
    <h3>Digital Assistant (2025 - Present)</h3>
    <ul>
      <li>Assisted with digital tasks such as online research, organizing data, and creating documents</li>
      <li>Gained practical knowledge in digital marketing and online trading platforms</li>
      <li>Handled social media activities and supported digital marketing efforts</li>
    </ul>
    <h3>Marketing Assistant (2022 - 2025 ongoing)</h3>
    <ul>
      <li>Promoted services and products through social media and direct outreach</li>
      <li>Managed communication with both local and international clients</li>
      <li>Built and maintained trusted networks with pet buyers and traders</li>
    </ul>
    <h3>Admission Consultant (2023 - 2025 ongoing)</h3>
    <ul>
      <li>Guided students in selecting suitable courses and institutions</li>
      <li>Assisted in application form filling and document submission</li>
      <li>Helped students make informed decisions about their academic future</li>
    </ul>
  </section>  <section>
    <h2>Skills</h2>
    <ul>
      <li>Task Completion</li>
      <li>Remote work</li>
      <li>Teamwork</li>
      <li>Time Management</li>
      <li>Leadership</li>
      <li>Effective Communication</li>
      <li>Online Research</li>
      <li>Digital Marketing</li>
    </ul>
  </section>  <section>
    <h2>Education</h2>
    <ul>
      <li>AI & Robotics Course – Hillsinai Finishing School, Medhavi University (2023-2025)</li>
      <li>Customer Service Essentials – Great Learning (2025 - ongoing)</li>
      <li>Digital Marketing – Digital Marketing Institute (2025 - ongoing)</li>
    </ul>
  </section>  <section>
    <h2>Languages</h2>
    <ul>
      <li>English (Fluent)</li>
      <li>Malayalam (Fluent)</li>
      <li>Hindi (Basic)</li>
      <li>Tamil (Basic)</li>
      <li>Arabic (Basic)</li>
    </ul>
  </section>  <section class="enquiry">
    <button onclick="handleEnquiry()">Enquiry</button>
  </section>  <section>
    <h2>Contact</h2>
    <div class="contact-icons">
      <p><i class="fas fa-phone-alt"></i> +91 8714335313</p>
      <p><i class="fas fa-envelope"></i> contactrazii@gmail.com</p>
      <p><i class="fas fa-map-marker-alt"></i> Kollam, Kerala</p>
      <p><a href="https://instagram.com/bbaaiz" target="_blank"><i class="fab fa-instagram"></i> @bbaaiz</a></p>
    </div>
  </section>  <footer>
    <p>&copy; 2025 Muhammed Razi. All rights reserved.</p>
  </footer>  <script>
    function handleEnquiry() {
      Swal.fire({
        title: 'Enter Your Contact Number',
        input: 'text',
        inputLabel: 'Your number will be used to contact you',
        inputPlaceholder: 'e.g. +91 9876543210',
        showCancelButton: true
      }).then((result) => {
        if (result.isConfirmed && result.value) {
          Swal.fire('Catch you soon!', 'We will contact you shortly.', 'success');
          fetch('https://yourserver.com/notify', {
            method: 'POST',
            headers: {
              'Content-Type': 'application/json'
            },
            body: JSON.stringify({
              number: result.value,
              timestamp: new Date().toISOString()
            })
          });
        }
      });
    }

    for (let i = 0; i < 20; i++) {
      const bubble = document.createElement('div');
      bubble.className = 'bubble';
      bubble.style.width = `${Math.random() * 40 + 10}px`;
      bubble.style.height = bubble.style.width;
      bubble.style.left = `${Math.random() * 100}vw`;
      bubble.style.background = `rgba(${Math.random()*255},${Math.random()*255},${Math.random()*255},0.4)`;
      bubble.style.animationDuration = `${Math.random() * 10 + 5}s`;
      document.body.appendChild(bubble);
    }
  </script></body>
</html><!DOCTYPE html><html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Muhammed Razi - Digital Assistant</title>
  <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;700&display=swap" rel="stylesheet" />
  <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css" rel="stylesheet" />
  <script src="https://cdn.jsdelivr.net/npm/sweetalert2@11"></script>
  <style>
    * {
      box-sizing: border-box;
      font-family: 'Montserrat', sans-serif;
      margin: 0;
      padding: 0;
    }
    body {
      background: linear-gradient(135deg, #e0c3fc, #8ec5fc);
      overflow-y: auto;
      color: #333;
      line-height: 1.6;
      scroll-behavior: smooth;
    }
    header {
      background: rgba(44, 62, 80, 0.85);
      color: white;
      padding: 2rem;
      text-align: center;
    }
    header img {
      width: 150px;
      height: 150px;
      border-radius: 50%;
      object-fit: cover;
      margin-bottom: 1rem;
    }
    section {
      padding: 2rem;
      background-color: rgba(255, 255, 255, 0.85);
      margin: 1rem;
      border-radius: 10px;
    }
    h2 {
      color: #2c3e50;
      margin-bottom: 1rem;
    }
    ul {
      margin-left: 2rem;
    }
    .enquiry {
      text-align: center;
      margin: 2rem 0;
    }
    .enquiry button {
      padding: 0.75rem 1.5rem;
      font-size: 1rem;
      color: white;
      background: linear-gradient(45deg, #ff9a9e, #fad0c4);
      border: none;
      border-radius: 10px;
      cursor: pointer;
      transition: transform 0.3s ease;
    }
    .enquiry button:hover {
      transform: scale(1.1);
    }
    footer {
      background-color: rgba(44, 62, 80, 0.85);
      color: white;
      text-align: center;
      padding: 1rem;
    }
    .contact-icons p i {
      margin-right: 10px;
      color: #2c3e50;
    }
    .bubble {
      position: fixed;
      bottom: -100px;
      border-radius: 50%;
      opacity: 0.6;
      animation: rise 10s infinite ease-in;
      z-index: -1;
    }
    @keyframes rise {
      0% {
        transform: translateY(0);
      }
      100% {
        transform: translateY(-120vh);
      }
    }
    a {
      color: inherit;
      text-decoration: none;
    }
  </style>
</head>
<body>
  <header>
    <img src="your-photo.jpg" alt="Muhammed Razi" />
    <h1>Muhammed Razi</h1>
    <p>Digital Assistant</p>
  </header>  <section>
    <h2>About Me</h2>
    <p>I am a digitally driven and goal-oriented individual with hands-on experience as an admission consultant, marketing assistant, and digital assistant. Currently pursuing a course in Customer Service Essentials, I also actively explore crypto trading and online platforms. With a passion for technology and communication, I stay highly engaged in the digital world, aiming to grow through continuous learning and real-world experience.</p>
  </section>  <section>
    <h2>Work Experience</h2>
    <h3>Digital Assistant (2025 - Present)</h3>
    <ul>
      <li>Assisted with digital tasks such as online research, organizing data, and creating documents</li>
      <li>Gained practical knowledge in digital marketing and online trading platforms</li>
      <li>Handled social media activities and supported digital marketing efforts</li>
    </ul>
    <h3>Marketing Assistant (2022 - 2025 ongoing)</h3>
    <ul>
      <li>Promoted services and products through social media and direct outreach</li>
      <li>Managed communication with both local and international clients</li>
      <li>Built and maintained trusted networks with pet buyers and traders</li>
    </ul>
    <h3>Admission Consultant (2023 - 2025 ongoing)</h3>
    <ul>
      <li>Guided students in selecting suitable courses and institutions</li>
      <li>Assisted in application form filling and document submission</li>
      <li>Helped students make informed decisions about their academic future</li>
    </ul>
  </section>  <section>
    <h2>Skills</h2>
    <ul>
      <li>Task Completion</li>
      <li>Remote work</li>
      <li>Teamwork</li>
      <li>Time Management</li>
      <li>Leadership</li>
      <li>Effective Communication</li>
      <li>Online Research</li>
      <li>Digital Marketing</li>
    </ul>
  </section>  <section>
    <h2>Education</h2>
    <ul>
      <li>AI & Robotics Course – Hillsinai Finishing School, Medhavi University (2023-2025)</li>
      <li>Customer Service Essentials – Great Learning (2025 - ongoing)</li>
      <li>Digital Marketing – Digital Marketing Institute (2025 - ongoing)</li>
    </ul>
  </section>  <section>
    <h2>Languages</h2>
    <ul>
      <li>English (Fluent)</li>
      <li>Malayalam (Fluent)</li>
      <li>Hindi (Basic)</li>
      <li>Tamil (Basic)</li>
      <li>Arabic (Basic)</li>
    </ul>
  </section>  <section class="enquiry">
    <button onclick="handleEnquiry()">Enquiry</button>
  </section>  <section>
    <h2>Contact</h2>
    <div class="contact-icons">
      <p><i class="fas fa-phone-alt"></i> +91 8714335313</p>
      <p><i class="fas fa-envelope"></i> contactrazii@gmail.com</p>
      <p><i class="fas fa-map-marker-alt"></i> Kollam, Kerala</p>
      <p><a href="https://instagram.com/bbaaiz" target="_blank"><i class="fab fa-instagram"></i> @bbaaiz</a></p>
    </div>
  </section>  <footer>
    <p>&copy; 2025 Muhammed Razi. All rights reserved.</p>
  </footer>  <script>
    function handleEnquiry() {
      Swal.fire({
        title: 'Enter Your Contact Number',
        input: 'text',
        inputLabel: 'Your number will be used to contact you',
        inputPlaceholder: 'e.g. +91 9876543210',
        showCancelButton: true
      }).then((result) => {
        if (result.isConfirmed && result.value) {
          Swal.fire('Catch you soon!', 'We will contact you shortly.', 'success');
          fetch('https://yourserver.com/notify', {
            method: 'POST',
            headers: {
              'Content-Type': 'application/json'
            },
            body: JSON.stringify({
              number: result.value,
              timestamp: new Date().toISOString()
            })
          });
        }
      });
    }

    for (let i = 0; i < 20; i++) {
      const bubble = document.createElement('div');
      bubble.className = 'bubble';
      bubble.style.width = `${Math.random() * 40 + 10}px`;
      bubble.style.height = bubble.style.width;
      bubble.style.left = `${Math.random() * 100}vw`;
      bubble.style.background = `rgba(${Math.random()*255},${Math.random()*255},${Math.random()*255},0.4)`;
      bubble.style.animationDuration = `${Math.random() * 10 + 5}s`;
      document.body.appendChild(bubble);
    }
  </script></body>
</html>