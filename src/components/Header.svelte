<script lang="ts">
  export let paginaActual: string;
  
</script>

<header>
	

	<nav>
		<svg viewBox="0 0 2 3" aria-hidden="true">
			<path d="M0,0 L1,2 C1.5,3 1.5,3 2,3 L2,0 Z" />
		</svg>
		<ul>
			<li >
				<a href="/"><img src="/fmt.svg" alt=""></a>
			</li>
			<li class={paginaActual === 'home' ? 'active' : ''}>
				<a href="/">Home</a>
			</li>
            <li class={paginaActual === 'create' ? 'active' : ''}>
				<a href="/creation">Creation de site</a>
                
			</li>
			<li class={paginaActual === 'com' ? 'active' : ''}>
				<a href="/communication">Communication</a>
			</li>
			<li class={paginaActual === 'price' ? 'active' : ''}>
				<a href="/prix">Prix</a>
			</li>
            <li class={paginaActual === 'about' ? 'active' : ''}>
                <!-- svelte-ignore a11y-mouse-events-have-key-events -->
                <a href="/about" >Agence</a>
                <ul>
                  <!-- Aquí van los elementos del submenú -->
                    <li><a href="/settings/profile">Présentation</a></li>
                    <li><a href="/settings/security">L'agence</a></li>
                    
                </ul>
            </li>
			
		</ul>
		<svg viewBox="0 0 2 3" aria-hidden="true">
			<path d="M0,0 L0,3 C0.5,3 0.5,3 1,2 L2,0 Z" />
		</svg>
	</nav>

	
</header>

<style>
	header {
		display: flex;
		justify-content: space-around;
	}


	nav {
		position: fixed;
		z-index: 1;
		display: flex;
		justify-content: center;
		--background: rgba(255, 255, 255, 0.7);
	}

	svg {
		width: 3.3em;
		height: 5em;
		display: block;
	}

	path {
		fill: var(--background);
	}

	ul {
		position: relative;
		padding: 0;
		margin: 0;
		height: 5em;
		display: flex;
		justify-content: center;
		align-items: center;
		list-style: none;
		background: var(--background);
		background-size: contain;
	}

	li {
		position: relative;
		height: 100%;
        transition:all .5s ease-in-out;
	}

	li.active::before {
		--size: 15px;
		content: '';
		width: 0;
		height: 0;
		position: absolute;
		top: 0;
		left: calc(50% - var(--size));
		border: var(--size) solid transparent;
		border-top: var(--size) solid var(--color-theme-1);
	}

	nav a {
		display: flex;
		height: 100%;
		align-items: center;
		padding: 0 0.5rem;
		color: var(--color-text);
		font-weight: 700;
		font-size: 1.2rem;
		text-transform: uppercase;
		letter-spacing: 0.1em;
		text-decoration: none;
		transition: color 0.2s linear ;

	}

	a:hover {
		color: var(--color-theme-1);
	}
    nav a img{
        width: 2em;
		height: 2em;
		object-fit: contain;
    }

   nav ul li ul{
    position: absolute;
    align-items:flex-start;
    opacity: 0;
    width: 0;
    height: 0;
    width: 100%;
    transition: all .5s ease-in-out;
    z-index: 1;
  } 
    nav ul li:hover > ul{
    opacity: 1;
    top: 80px;
    left: 0;
    width: 190px;
    height: 100%;
    display: flex;
    flex-direction: column;
    background:var(--background);
    border-radius: 3px;
  }
  


  


    
</style>