<script>
// @ts-nocheck
	import { Pane, Splitpanes } from 'svelte-splitpanes';
	import './styles.css';
	import Header from './Header.svelte';
	import SideIcons from './SideIcons.svelte';
	import SideMenu from './SideMenu.svelte';
    import Veiw from './Veiw.svelte';
	import Footer from './Footer.svelte';

</script>
<main>
	<Header/>
	<section>
		<Splitpanes class="splitpanes">
			<Pane minSize={20} maxSize={50} size={30} class="pane">
				<div class="menu">
					<SideIcons/>
					<SideMenu/>
				</div>
			</Pane>
			<Pane>
				<Veiw/>
				<slot/>
			</Pane>
		</Splitpanes>
	</section>
	<footer>
		<Footer />
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
	grid-template-columns: 1fr 50%;
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