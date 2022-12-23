<script>
    export let segment;

    let isOpen = false;
    
    var toggleNav = () =>{
        isOpen = !isOpen;
    }

</script>
<style>
    @media screen and (min-width: 1024px) {
        .navbar {
            border-bottom: 1px solid gray;
        }
    }
</style>
<nav class="navbar" aria-label="main navigate" >
    <div class="navbar-brand">
        <a href="/home"  class="navbar-item" >
            <img src="logo.png" alt="virus">
        </a>
        <span on:click={toggleNav} class="navbar-burger" class:is-active={isOpen}  aria-label="menu" aria-expanded="false" >
            <span aria-hidden="true"></span>
            <span aria-hidden="true"></span>
            <span aria-hidden="true"></span>
        </span>
    </div>
    <div class="navbar-menu" class:is-active={isOpen}>
        <div class="navbar-start">
            <a href="/home" class="navbar-item" class:is-active={segment == undefined}>Home</a>
            <a href="/about" class="navbar-item" class:is-active={segment == 'about'}>About</a>
        </div>
    </div>
</nav>