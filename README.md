<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Student Section Finder</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      padding: 2rem;
      max-width: 600px;
      margin: auto;
    }
    h1 {
      text-align: center;
    }
    input {
      width: 100%;
      padding: 0.75rem;
      margin-top: 1rem;
      font-size: 1rem;
    }
    .result {
      margin-top: 1.5rem;
      font-size: 1.2rem;
      font-weight: bold;
      color: green;
    }
    .not-found {
      color: red;
    }
  </style>
</head>
<body>
  <h1>Student Section Finder</h1>
  <input type="text" id="search" placeholder="Enter your full name..." />
  <div class="result" id="result"></div>

  <script>
    const students = {
      "Almonte Kevin James": "Grade 11 - Aristotle",
      "Apura Lourence": "Grade 11 - Aristotle",
      "Baang Kent Nathaniele": "Grade 11 - Aristotle",
      "Bacon Denielle Jake": "Grade 11 - Aristotle",
      "Dayanan Cristof": "Grade 11 - Aristotle",
      "Fernandez John Mark": "Grade 11 - Aristotle",
      "Gako Christian": "Grade 11 - Aristotle",
      "Irona Dave": "Grade 11 - Aristotle",
      "Lauron Christian": "Grade 11 - Aristotle",
      "Lausa BB Jenboy": "Grade 11 - Aristotle",
      "Lu- ang Richard Dems": "Grade 11 - Aristotle",
      "Pantilgan Jackris": "Grade 11 - Aristotle",
      "Remo Criss Michol": "Grade 11 - Aristotle",
      "Satinitigan June Vincent": "Grade 11 - Aristotle",
      "Tangaro Negro Patrick": "Grade 11 - Aristotle",
      "Tumulak Kienneth": "Grade 11 - Aristotle",
      "Ygona Ansel": "Grade 11 - Aristotle",
      "Amistad Mary Cris": "Grade 11 - Aristotle",
      "Cabungcal Nechel Mae": "Grade 11 - Aristotle",
      "Cabungcal Krisha Marie": "Grade 11 - Aristotle",
      "Dela Cerna Samantha": "Grade 11 - Aristotle",
      "Enad Sweet Kiel": "Grade 11 - Aristotle",
      "Erezo Kristel": "Grade 11 - Aristotle",
      "Espinosa Angelie": "Grade 11 - Aristotle",
      "Larrobis Glyza Mar": "Grade 11 - Aristotle",
      "Lauron Shane": "Grade 11 - Aristotle",
      "Legarte Jhilia Mie": "Grade 11 - Aristotle",
      "Liniojan Beverly": "Grade 11 - Aristotle",
      "Mortifero Shane": "Grade 11 - Aristotle",
      "Navarro Chiecky Jayne": "Grade 11 - Aristotle",
      "Naveo Maria Ivonne": "Grade 11 - Aristotle",
      "Navoa Kisha Mae": "Grade 11 - Aristotle",
      "Pansan Fhebe Gail": "Grade 11 - Aristotle",
      "Parame Kylla": "Grade 11 - Aristotle",
      "Rudila Zairra": "Grade 11 - Aristotle",
      "Sabala Rhia Madjih": "Grade 11 - Aristotle",
      "Tangaro Ella Mae": "Grade 11 - Aristotle",
      "Larrobis Rachel": "Grade 11 - Socrates",
      "Dayondon Aveah": "Grade 11 - Socrates",
      "Monopollo Michaela Mae": "Grade 11 - Socrates",
      "Tangkay Jennifer": "Grade 11 - Socrates",
      "Castañares Frencis Yancy": "Grade 11 - Socrates",
      "Castañares Nichole Kerstine": "Grade 11 - Socrates",
      "Cabungcal Jane Claire": "Grade 11 - Socrates",
      "Larrobis John Nes": "Grade 11 - Socrates",
      "Conley Trisha Rose": "Grade 11 - Socrates",
      "Cuizon Jamaica": "Grade 11 - Socrates",
      "Lauron Alexa": "Grade 11 - Socrates",
      "Lauron Hanna Jency": "Grade 11 - Socrates",
      "Borja Rhosebhel Khay": "Grade 11 - Socrates",
      "Santuyo Asia Gayle": "Grade 11 - Socrates",
      "Oaper Hannah Keziah": "Grade 11 - Socrates",
      "Tapic Mary Andrie": "Grade 11 - Socrates",
      "Paldo Hannah Rucel": "Grade 11 - Socrates",
      "Campaña Aira Mae": "Grade 11 - Socrates",
      "Blanco Cassie Zyrine": "Grade 11 - Socrates",
      "Racoma Zeanne Carlo": "Grade 11 - Socrates",
      "Emphasis John Carl": "Grade 11 - Socrates",
      "Lauron Ivan Roy": "Grade 11 - Socrates",
      "Bacalso Kyle Andrey": "Grade 11 - Socrates",
      "Satera Jemuel": "Grade 11 - Socrates",
      "Manayaga Cyrus": "Grade 11 - Socrates",
      "Lauron Deejie": "Grade 11 - Socrates",
      "Sabala Vincent": "Grade 11 - Socrates",
      "Lausa John Khyl": "Grade 11 - Socrates",
      "Rim Raven": "Grade 11 - Socrates",
      "Fernandez John Lloyd": "Grade 11 - Socrates",
      "Ybañez Vaughn Uriel": "Grade 11 - Socrates",
      "Aldaya Bhorly": "Grade 11 - Socrates",
      "Lauron Brian": "Grade 11 - Socrates",
      "Siboco John Lenard": "Grade 11 - Socrates",
      "Satinitigan Rendy": "Grade 11 - Socrates",
      "Baculpo John Mike": "Grade 11 - Socrates"
    };

    const searchInput = document.getElementById('search');
    const resultDiv = document.getElementById('result');

    searchInput.addEventListener('input', () => {
      const query = searchInput.value.trim().toLowerCase();
      const match = Object.keys(students).find(name => name.toLowerCase() === query);
      if (match) {
        resultDiv.textContent = `${match} is enrolled in ${students[match]}`;
        resultDiv.className = 'result';
      } else {
        resultDiv.textContent = query ? 'Student not found.' : '';
        resultDiv.className = 'result not-found';
      }
    });
  </script>
</body>
</html>
