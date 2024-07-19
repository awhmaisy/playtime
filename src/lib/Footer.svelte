<script>
    import { onMount } from 'svelte';
    import Typed from 'typed.js';
    import jQuery from 'jquery';

    let typed;
    onMount(() => {
        typed = new Typed('#caption-wrapper', {
            strings: [
                "no mud, no lotus — professor child",
                "im Being all that i wanna be",
                "I no longer fear the [algorithm] guarding my heel",
                "enter portals to be creative",
                "death, regeneration, legacy"
            ],
            typeSpeed: 60,
            backSpeed: 30,
            loop: true,
            shuffle: true,
            backDelay: 2300,
            fadeOut: true
        });

        jQuery(document).ready(function () {
            jQuery("#caption").hide();

            setTimeout(function(){
                jQuery(".screenwipe").css("animation", "none").hide();
                jQuery("#caption").fadeIn(2500);
            }, 2700);
        });
    });
</script>

<footer>
    <div class="footer-left">
        <p>mei higashi</p>
    </div>
    <div class="footer-right">
        <div id="caption-wrapper"></div>
    </div>
</footer>


<style>
    body {
        margin: 0;
        display: flex;
        flex-direction: column;
        min-height: 100vh;
        font-size: 12px;
    }
    footer {
        position: fixed;
        bottom: 0;
        left: 0;
        width: 100%;
        display: flex;
        justify-content: space-between;
        align-items: center;
        font-size: 12px;
    }
    .footer-left {
        flex: 1;
        text-align: left;
        padding-left: 20px;
    }
    .footer-right {
        flex: 1;
        text-align: right;
        padding-right: 20px;
    }
    #caption-wrapper {
        display: inline; 
        font-size: 12px;
    }
    #caption-wrapper a {
        text-decoration: none; 
        color: inherit;
        display: none; 
    }
</style>
