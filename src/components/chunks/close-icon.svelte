<script>
</script>

<div class="close-icon">
    <div class="close-icon-bar" id="close-icon-bar-1"></div>
    <div class="close-icon-bar" id="close-icon-bar-2"></div>
    <h4>[Close]</h4>
</div>

<style>
    .close-icon {
        display: inline-block
    }
    .close-icon h4 {
        opacity: 0;
        position: relative;
        bottom: 12px;
        left: 0;
        cursor: default;
        transition: 0.2s;
    }
    .close-icon-bar {
        position: absolute;
        top: 0;
        width: 30px;
        height: 4px;
        background-color: var(--text-gray);
        border-radius: 5px;
        transition: 0.2s;
    }
    .close-icon #close-icon-bar-1 {
        transform: rotate(45deg);
    }
    .close-icon #close-icon-bar-2 {
        transform: rotate(-45deg)
    }
    .close-icon:hover h4 {
        opacity: 1;
    }
    .close-icon:hover .close-icon-bar {
        opacity: 0;
    }
    .close-icon:hover #close-icon-bar-1 {
        /* transform: rotate(225deg); */
    }
    .close-icon:hover #close-icon-bar-2 {
        /* transform: rotate(-225deg); */
    }
</style>