<script>
  import { onMount } from "svelte";

  let canvas;
  let ctx;

  // Drawing functions
  function draw() {
    ctx = canvas.getContext("2d");

    // Clear the canvas
    ctx.clearRect(0, 0, canvas.width, canvas.height);

    // Draw a line
    ctx.beginPath();
    ctx.moveTo(50, 50); // Move the path to the starting point
    ctx.lineTo(200, 200); // Draw a line to the end point
    ctx.strokeStyle = "#ff0000";
    ctx.lineWidth = 5;
    ctx.stroke(); // Render the path (stroke)

    // Draw a rectangle
    ctx.fillStyle = "#00ff00";
    ctx.fillRect(100, 100, 150, 100);
    ctx.strokeStyle = "#0000ff";
    ctx.strokeRect(300, 300, 100, 150);
    ctx.fillStyle = "#0000ff";
    ctx.fillRect(100, 300, 100, 150);

    // Draw a circle
    ctx.beginPath();
    ctx.arc(300, 100, 50, 0, 2 * Math.PI);
    ctx.fillStyle = "#ffff00";
    ctx.fill();
    ctx.strokeStyle = "#000000";
    ctx.lineWidth = 2;
    ctx.stroke();
  }

  onMount(() => {
    draw();
  });
</script>

<canvas
  bind:this={canvas}
  width="500"
  height="500"
  style="border:1px solid #000000;"
></canvas>
