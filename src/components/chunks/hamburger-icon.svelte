<script>
</script>

<div class="hamburger-icon">
    <div class="hamburger-icon-bar" id="hamburger-icon-bar-1"></div>
    <div class="hamburger-icon-bar" id="hamburger-icon-bar-2"></div>
    <div class="hamburger-icon-bar" id="hamburger-icon-bar-3"></div>
</div>

<style>
    .hamburger-icon {
        width: 30px;
        display: inline-block
    }
    .hamburger-icon-bar {
        width: 25px;
        height: 4px;
        background-color: #000000;
        border-radius: 5px;
        transition: 0.2s;
    }
    #hamburger-icon-bar-1, #hamburger-icon-bar-2 {
        margin-bottom: 5px;
    }
    .hamburger-icon:hover #hamburger-icon-bar-1 {
        width: 30px;
    }
    .hamburger-icon:hover #hamburger-icon-bar-2 {
        width: 15px;
    }
    .hamburger-icon:hover #hamburger-icon-bar-3 {
        width: 20px;
    }
</style>