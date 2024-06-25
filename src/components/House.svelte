<script>
  import { onMount } from "svelte";

  let canvas;
  let ctx;
  function draw() {
    ctx = canvas.getContext("2d");
    ctx.clearRect(0, 0, canvas.width, canvas.height);

    ctx.beginPath();
    ctx.moveTo(10, 10);
    ctx.lineTo(100, 10);
    ctx.strokeStyle = "red";
    ctx.stroke();

    // Draw the house body
    ctx.fillStyle = "#8B4513";
    ctx.fillRect(50, 200, 400, 200);

    // Draw the roof
    ctx.beginPath();
    ctx.moveTo(50, 200);
    ctx.lineTo(250, 100);
    ctx.lineTo(450, 200);
    ctx.closePath();
    ctx.fillStyle = "#A52A2A";
    ctx.fill();
    ctx.stroke();

    // Draw the door
    ctx.fillStyle = "#654321";
    ctx.fillRect(215, 250, 80, 150);

    // Draw the window
    ctx.fillStyle = "#654321";
    ctx.fillRect(125, 300, 50, 50);
    // Draw the window
    ctx.fillStyle = "#654321";
    ctx.fillRect(335, 300, 50, 50);

    // Draw the sun
    ctx.beginPath();
    ctx.arc(400, 50, 30, 0, 2 * Math.PI);
    ctx.fillStyle = "#FFD700";
    ctx.fill();
    ctx.stroke();

    // Draw sun rays
    ctx.strokeStyle = "#FFD700";
    ctx.lineWidth = 2;
    for (let i = 0; i < 8; i++) {
      ctx.beginPath();
      ctx.moveTo(400, 50);
      ctx.lineTo(
        400 + 40 * Math.cos((i * Math.PI) / 4),
        50 + 40 * Math.sin((i * Math.PI) / 4)
      );
      ctx.stroke();
    }
  }
  onMount(() => {
    draw();
  });
</script>

<canvas
  bind:this={canvas}
  width="500"
  height="500"
  style="border: 5px solid black;"
></canvas>
<h2>This is House</h2>
