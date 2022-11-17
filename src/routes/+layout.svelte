<script>
  import Nav from "../lib/components/Nav.svelte";
</script>

<!-- html -->
<h1 class="title is-1">web tools</h1>
<Nav></Nav>

<slot></slot>

<footer class="footer">
  <div class="content has-text-centered">
    <p>
      link to <a href="https://github.com/husita-h/web_tools_sandbox">Github Repository
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