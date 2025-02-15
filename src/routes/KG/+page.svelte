<script>
  import 'bootstrap/dist/css/bootstrap.min.css';
  import '$lib/selectlesson.css';

  import { onMount } from "svelte";

  onMount(() => {
    // Checking and updating checkmarks for each lesson
    const lessons = [
      { key: 'Identifying_Counting_upto5_time', checkClass: '.check' },
      { key: 'MLGF_upto5_time', checkClass: '.check1' },
      { key: 'Identifying_Counting_upto10_time', checkClass: '.check2' },
      { key: 'MLGF_upto10_time', checkClass: '.check3' },
      { key: 'Addition_upto5_time', checkClass: '.check4' },
      { key: 'Subtraction_upto5_time', checkClass: '.check5' },
      { key: 'Addition_upto10_time', checkClass: '.check6' },
      { key: 'Subtraction_upto10_time', checkClass: '.check7' },
      { key: 'Identifying_Counting_upto20_time', checkClass: '.check8' },
      { key: 'Addition_upto20_time', checkClass: '.check9' },
      { key: 'Subtraction_upto20_time', checkClass: '.check10' },
      { key: 'Shapes_2D_time', checkClass: '.check11' },
      { key: 'Shapes_3D_time', checkClass: '.check12' },
    ];

    // Loop through each lesson and check if time is stored
    lessons.forEach(lesson => {
      const storedTime = Number(localStorage.getItem(lesson.key)) || 0;
      if (storedTime > 0) {
        document.querySelector(lesson.checkClass).innerHTML = '&#10004;';
      }
    });
  });
</script>

<svelte:head>
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.3/css/all.min.css" />
</svelte:head>
<button on:click={() => location.replace('/')} class="btn btn-primary back">
  <i class="fas fa-arrow-left" />
</button>
<ol>
  <br />
  <h1>Kindergarten - Math</h1>

  <li>
    <div class="list-item">
      <a href="./KG/Identifying_Counting_upto5" class="arrow">
        Identifying and Counting Numbers<br>(up to 5)
      </a>
      <span class="check"></span>
    </div>
  </li>  

  <li>
    <div class="list-item">
      <a href="./KG/MLGF_upto5" class="arrow">
        More, Less, Greater, Fewer (up to 5)
      </a>
      <span class="check1"></span>
    </div>
  </li>

  <li>
    <div class="list-item">
      <a href="./KG/Identifying_Counting_upto10" class="arrow">
        Identifying and Counting Numbers<br>(up to 10)
      </a>
      <span class="check2"></span>
    </div>
  </li>  

  <li>
    <div class="list-item">
      <a href="./KG/MLGF_upto10" class="arrow">
        More, Less, Greater, Fewer (up to 10)
      </a>
      <span class="check3"></span>
    </div>
  </li>

  <li>
    <div class="list-item">
      <a href="./KG/Addition_upto5" class="arrow">
        Addition (up to 5)
      </a>
      <span class="check4"></span>
    </div>
  </li>

  <li>
    <div class="list-item">
      <a href="./KG/Subtraction_upto5" class="arrow">
        Subtraction (up to 5)
      </a>
      <span class="check5"></span>
    </div>
  </li>

  <li>
    <div class="list-item">
      <a href="./KG/Addition_upto10" class="arrow">
        Addition (up to 10)
      </a>
      <span class="check6"></span>
    </div>
  </li>

  <li>
    <div class="list-item">
      <a href="./KG/Subtraction_upto10" class="arrow">
        Subtraction (up to 10)
      </a>
      <span class="check7"></span>
    </div>
  </li>

  <li>
    <div class="list-item">
      <a href="./KG/Identifying_Counting_upto20" class="arrow">
        Identifying and Counting Numbers<br>(up to 20)
      </a>
      <span class="check8"></span>
    </div>
  </li>  
  
  <li>
    <div class="list-item">
      <a href="./KG/Addition_upto10" class="arrow">
        Addition (up to 20)
      </a>
      <span class="check9"></span>
    </div>
  </li>

  <li>
    <div class="list-item">
      <a href="./KG/Subtraction_upto10" class="arrow">
        Subtraction (up to 20)
      </a>
      <span class="check10"></span>
    </div>
  </li>

  <li>
    <div class="list-item">
      <a href="./KG/Shapes_2D" class="arrow">
        Shapes (2D)
      </a>
      <span class="check11"></span>
    </div>
  </li>

  <li>
    <div class="list-item">
      <a href="./KG/Shapes_3D" class="arrow">
        Shapes (3D)
      </a>
      <span class="check12"></span>
    </div>
  </li>

</ol>