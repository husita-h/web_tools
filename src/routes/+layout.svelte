<script>
  import Nav from "../lib/components/Nav.svelte";
</script>

<!-- html -->
<h1 class="title is-1">Web tools</h1>
<Nav></Nav>

<slot></slot>

<footer class="footer">
  <div class="content has-text-centered">
    <p>
      <strong>link to </strong><a href="https://www.google.com/">Github Repository
    </p>
  </div>
</footer>
<!-- html -->

<style>
.footer {
  position: fixed;
  right: 0;
  bottom: 0;
  left: 0;
}
</style>