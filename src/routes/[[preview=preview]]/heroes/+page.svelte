<script lang='ts'>
  import ContentWidth from '$lib/components/ContentWidth/ContentWidth.svelte';
  import Img from '@zerodevx/svelte-img';
  import redoorHero from '$lib/assets/images/heroes/reddoorHero.png?as=run'
  import erpHero from '$lib/assets/images/heroes/erpHero.png?as=run'
  import oneEightHero from '$lib/assets/images/heroes/1800DentistHero.png?as=run'
  import beachfrontHero from '$lib/assets/images/heroes/beachfrontHero.png?as=run'
  import sonderHero from '$lib/assets/images/heroes/sonderHero.png?as=run'
  import heartsHero from '$lib/assets/images/heroes/heartsHero.png?as=run'
  import espadaHero from '$lib/assets/images/heroes/espadaHero.png?as=run'
  import evidenceHero from '$lib/assets/images/heroes/dataHero.png?as=run'
  import msotHero from '$lib/assets/images/heroes/msotHero.png?as=run'
  import caltexHero from '$lib/assets/images/heroes/caltexHero.png?as=run'
  import hedlocHero from '$lib/assets/images/heroes/hedlocHero.png?as=run'
  import c2cHero from '$lib/assets/images/heroes/c2cHero.png?as=run'
  import enzosHero from '$lib/assets/images/heroes/enzosHero.png?as=run'
  import { onMount } from 'svelte';

  const sites = [
	{
		name: 'Reddoor',
		link: 'https://reddoorla.com/',
		screencap: redoorHero
	},
	{
		name: 'ERP',
		link: 'https://erpfunds.com/',
		screencap: erpHero
	},
	{
		name: '1-800-Dentist',
		link: 'https://1800dentist.com/',
		screencap: oneEightHero
	},
	{
		name: 'Beachfront Dentistry',
		link: 'https://www.beachfrontdentistry.com/',
		screencap: beachfrontHero
	},
	{
		name: 'Gallery Sonder',
		link: 'https://gallerysonder.com/',
		screencap: sonderHero
	},
	{
		name: 'Hearts & Minds',
		link: 'https://www.lahomelessnessawareness.org/',
		screencap: heartsHero
	},
	{
		name: 'Espada',
		link: 'https://espadarealestate.com/',
		screencap: espadaHero
	},
	{
		name: 'Evidence360',
		link: 'http://www.datadynamiq.com/',
		screencap: evidenceHero
	},
	{
		name: 'MSOT',
		link: 'https://medicalsolutionsoftx.com/',
		screencap: msotHero
	},
	{
		name: 'CalTex',
		link: 'https://www.caltexmedical.com/',
		screencap: caltexHero
	},
	{
		name: 'Hedloc',
		link: 'https://hedloc.netlify.app/',
		screencap: hedlocHero
	},
	{
		name: 'Coast2Coast',
		link: 'https://www.c2crecruits.com/',
		screencap: c2cHero
	},
	{
		name: 'Enzos',
		link: 'https://enzoshandwash.com/',
		screencap: enzosHero
	},
  ]


	let viewpoortWidth=$state(1024)


</script>

<svelte:head>
	<title>Reddoor Component Library</title>
</svelte:head>

<svelte:window bind:innerWidth={viewpoortWidth} />

<section class='py-32'>
	<ContentWidth>
	

		<div class='flex flex-row justify-center flex-wrap'>
			{#each sites as site}
			<div class='w-160 h-92 p-8'>
				<a href={site.link} class='w-full h-full relative rounded hover:opacity-95 flex items-center justify-center overflow-hidden'>
					<Img src={site.screencap} class='w-full h-full absolute top-0 left-0 brightness-50 hover:brightness-100 hover:z-30 transition object-cover'/>
					<h1 class='text-white transition z-20'>{site.name}</h1>
				</a>
			</div>
			{/each}
		</div>


	</ContentWidth>
</section>