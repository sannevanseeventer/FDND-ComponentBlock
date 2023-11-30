<script>

</script>
  

    <nav>
      <input type="checkbox" id="checkbox" class="checkbox">
      <label for="checkbox" class="toggle">

        <svg class="menu" viewBox="0 0 448 512" width="100" title="bars">
          <path d="M16 132h416c8.837 0 16-7.163 16-16V76c0-8.837-7.163-16-16-16H16C7.163 60 0 67.163 0 76v40c0 8.837 7.163 16 16 16zm0 160h416c8.837 0 16-7.163 16-16v-40c0-8.837-7.163-16-16-16H16c-8.837 0-16 7.163-16 16v40c0 8.837 7.163 16 16 16zm0 160h416c8.837 0 16-7.163 16-16v-40c0-8.837-7.163-16-16-16H16c-8.837 0-16 7.163-16 16v40c0 8.837 7.163 16 16 16z" />
        </svg>

        <svg class="close" viewBox="0 0 384 512" width="100" title="close">
          <path d="M242.72 256l100.07-100.07c12.28-12.28 12.28-32.19 0-44.48l-22.24-22.24c-12.28-12.28-32.19-12.28-44.48 0L176 189.28 75.93 89.21c-12.28-12.28-32.19-12.28-44.48 0L9.21 111.45c-12.28 12.28-12.28 32.19 0 44.48L109.28 256 9.21 356.07c-12.28 12.28-12.28 32.19 0 44.48l22.24 22.24c12.28 12.28 32.2 12.28 44.48 0L176 322.72l100.07 100.07c12.28 12.28 32.2 12.28 44.48 0l22.24-22.24c12.28-12.28 12.28-32.19 0-44.48L242.72 256z" />
        </svg>

      </label>

      <ul class="nav-menu">
        <li><a href="/"><img class="logo" src="logotest2.png" alt="logo spatwater" width="100" height="auto" /></a></li>
        <li><a href="/over">Over</a></li>
        <li><a href="/expertise">Expertise</a></li>
        <li><a href="/projecten">Projecten</a></li>
        <li><a href="/kennisbank">Kennisbank</a></li>
        <li><a href="/team">Team</a></li>
        <li><a href="/contact"><span>Contact</span></a></li>
      </ul>
    </nav>


<style>
nav {
    box-shadow: -1px 0 4px rgba(14, 55, 63, 0.15);
    height: 5rem;
}

.logo{
    width: 6.5rem;
    height: auto;
    margin: 1rem 1rem;
}

.toggle {
  position: absolute;
  cursor: pointer;
  margin: 1.6rem 1.5rem;
  right: 0;
}
.toggle svg {
  width: 1rem;
  fill: #2a324b;
}
.toggle .close {
  display: none;
}
.toggle .menu {
  margin-top: 0.2rem;
}
.checkbox {
  display: none;
}
.nav-menu {
  display: flex;
  flex-direction: column;
  gap: 2rem;
  align-items: center;
}
.nav-menu li {
  list-style: none;
  display: none;
}

.nav-menu span {
padding: 0.5rem 0.8rem;
background-color: var(--green);
color: white;
border-radius: 5px;
}

.nav-menu li:first-child {
  margin-right: auto;
  display: block;
}
.nav-menu a {
  text-decoration: none;
  color: var(--darkblue);
  font-size: 1rem;
}

#checkbox:checked ~ ul.nav-menu li {
  display: block;
}

#checkbox:checked ~ label.toggle .close {
  display: block;
}

#checkbox:checked ~ label.toggle .menu {
  display: none;
}

@media only screen and (min-width: 560px) {

    nav {
 height: 5rem;
}

  .toggle {
    display: none;
  }
  .nav-menu {
    flex-direction: row;
    margin-right: 1.5rem;
  }
  .nav-menu li {
    display: block;
  }

  .logo{
    width: 7rem;
}

}

</style>