<script>
  import { onMount } from "svelte";

  let canvas;
  let ctx;

  function draw() {
    ctx = canvas.getContext("2d");
    ctx.clearRect(0, 0, canvas.width, canvas.height);

    // Draw rectangle
    ctx.strokeStyle = "#ffff";
    ctx.strokeRect(40, 10, 200, 200);
    ctx.strokeRect(260, 10, 200, 200);

    // Draw a line
    ctx.beginPath();
    ctx.moveTo(40, 250);
    ctx.lineTo(40, 350);
    ctx.lineTo(240, 350);
    ctx.closePath();
    ctx.strokeStyle = "#ffffff";
    ctx.lineWidth = 5;
    ctx.stroke();

    // Draw a line
    ctx.fillStyle = "blue";
    ctx.beginPath();
    ctx.moveTo(260, 250);
    ctx.lineTo(460, 250);
    ctx.lineTo(460, 350);
    ctx.closePath();
    ctx.fill();

    // Draw a circle
    ctx.beginPath();
    ctx.arc(410, 430, 50, 0, 2 * Math.PI);
    ctx.fill();

    // Draw a circle
    ctx.beginPath();
    ctx.arc(100, 430, 50, 0, 2 * Math.PI);
    ctx.strokeStyle = "red";
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
  style="border: 5px solid black;"
></canvas>
<h2>Practice Canvas</h2>
<br />
