<script>
    import { onMount } from 'svelte'
    import { slide } from 'svelte/transition'
  
    let jsEnabled = true
    let mounted = false
  
    onMount(() => {
      jsEnabled = false
      mounted = true
    })
  </script>
  
  <header>
    <div class="navbar">
      <title>SPATwater</title>
      <img class="logo" src="logotest2.png" alt="logo spatwater" />
      <label for="toggle" aria-label="menu icon">&#9776;</label>
    </div>
  
    <input id="toggle" type="checkbox" class="sr-only" class:js={mounted} bind:checked={jsEnabled} />
  
    {#if jsEnabled}
    <nav transition:slide>
        <ul>
            <li><a href="/">Home</a></li>
            <li><a href="/over">Over</a></li>
            <li><a href="/expertise">Expertise</a></li>
            <li><a href="/projecten">Projecten</a></li>
            <li><a href="/kennisbank">Kennisbank</a></li>
            <li><a href="/team">Team</a></li>
            <li><a href="/contact"><span>Contact</span></a></li>
          </ul>
    </nav>
    {/if}
  </header>
  
<style>
    @import url("https://fonts.googleapis.com/css2?family=Poppins&display=swap");
    @import url("https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.3/css/all.min.css");

    :root {
        --spat: #7faec5;
        --lg-bg: #fafafa;
        --green: #4ecd5d;
        --darkblue: #384b61;
  }
    .sr-only {
        position: absolute;
        width: 1px;
        height: 1px;
        padding: 0;
        margin: -1px;
        overflow: hidden;
        clip: rect(0, 0, 0, 0);
        white-space: nowrap;
        border-width: 0;
        cursor: pointer;
    }
    
    .navbar {
        display: flex;
        flex-direction: row;
        align-items: center;
        box-shadow: -1px 0 4px rgba(14, 55, 63, 0.15);
        justify-content: space-between;
        padding: 1em;
        background: white;
    }
    
   .logo{
        width: 7rem;
   }
    
    .navbar label {
        font-size: 1.25rem;
        cursor: pointer;
        padding: 1rem;
        border-radius: 0.25em;
    }
    
    nav {
        padding-bottom: 1.5em;
    }
    
    nav ul {
        list-style: none;
        padding: 1em;
        margin: 0;
        display: flex;
        flex-direction: column;
        align-items: center;
        gap: 1.3em;
        font-size: 1.25rem;
    }

    li a{
        text-decoration: none;
        font-family: 'Poppins';
        font-size: 1.3rem;
        color: var(--darkblue);
    }

    span{
        background-color:var(--green);
        color: white;
        padding: 0.3rem 1rem;
        border-radius: 0.3rem;
    }

    #toggle:not(.js) ~ nav {
        display: none;
    }
  
    #toggle:not(.js):checked ~ nav {
        display: block;
    }
  </style>
