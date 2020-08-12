<script>
	export let segment;
</script>

<style>
	nav {
		border-bottom: 1px solid #db5d7d;
		padding: 0 1em;
	}

	h1 {
		text-align: center;
		color: #EB1B95;
		text-shadow: 0 0 10px #EB1B95;
	}

	ul {
		margin: 0;
		padding: 0;
		display: flex;
		justify-content: space-evenly;
		width: 100%;
		text-align: center;
	}

	/* clearfix */
	ul::after {
		content: '';
		display: block;
		clear: both;
	}

	li {
		display: block;
	}

	[aria-current] {
		position: relative;
		display: inline-block;
	}

	[aria-current]::after {
		position: absolute;
		content: '';
		width: calc(100% - 1em);
		height: 2px;
		box-shadow: 0px 1px 5px #ffed00,
					0px -1px 5px #ffed00;
		display: block;
		bottom: -1px;
	}

	a {
		text-decoration: none;
		padding: 1em 0.5em;
		display: block;
		text-align: center;
	}
</style>

<nav>
	<h1>Adriaan van der Bergh</h1>
	<ul>
		<li><a aria-current="{segment === undefined ? 'page' : undefined}" href=".">Experience</a></li>
		<li><a aria-current="{segment === 'projects' ? 'page' : undefined}" href="projects">Projects</a></li>
		<li><a aria-current="{segment === 'education' ? 'page' : undefined}" href="education">Education & Certifications</a></li>
		<li><a aria-current="{segment === 'skills' ? 'page' : undefined}" href="skills">Skills</a></li>
	</ul>
</nav>
