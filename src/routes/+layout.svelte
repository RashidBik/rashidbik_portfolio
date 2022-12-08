<script>
// @ts-nocheck
	import { Pane, Splitpanes } from 'svelte-splitpanes';
	import Header from './Header.svelte';
	import './styles.css';
</script>
<main>
	<Header/>
	<section>
		<Splitpanes class="splitpanes">
			<Pane minSize={20} maxSize={50} size={30} class="pane">
				<div class="menu">
					<aside>side</aside>
					<div>another</div>
				</div>
			</Pane>
			<Pane></Pane>
		</Splitpanes>
	</section>
	<footer>
		footer
	</footer>
</main>

<style>
section{
	height: 80vh;
	background: #888;
	width: 100%;
}
.pane:hover{
	border: 3px solid rgb(163, 60, 60);
}
.menu{
	display: grid;
	grid-template-columns: 20% 200px;
}
aside{
	background: rgb(80, 76, 76);
}
	@media (min-width: 480px) {
		footer {
			padding: 12px 0;
		}
	}
</style>