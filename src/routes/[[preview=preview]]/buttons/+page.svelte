<script lang='ts'>
  import ContentWidth from '$lib/components/ContentWidth/ContentWidth.svelte';
  import Img from '@zerodevx/svelte-img';
  import redoorButtons from '$lib/assets/images/buttons/reddoorButtons.png?as=run'
  import erpButtons from '$lib/assets/images/buttons/erpButtons.png?as=run'
  import oneEightButtons from '$lib/assets/images/buttons/oneEightButtons.png?as=run'
  import beachfrontButtons from '$lib/assets/images/buttons/beachfrontButtons.png?as=run'
  import sonderButtons from '$lib/assets/images/buttons/sonderButtons.png?as=run'
  import heartsButtons from '$lib/assets/images/buttons/heartButtons.png?as=run'
  import espadaButtons from '$lib/assets/images/buttons/espadaButtons.png?as=run'
  import evidenceButtons from '$lib/assets/images/buttons/dataButtons.png?as=run'
  import msotButtons from '$lib/assets/images/buttons/msotButtons.png?as=run'
  import caltexButtons from '$lib/assets/images/buttons/caltexButtons.png?as=run'
  import hedlocButtons from '$lib/assets/images/buttons/hedlocButtons.png?as=run'
  import c2cButtons from '$lib/assets/images/buttons/c2cButtons.png?as=run'
  import enzosButtons from '$lib/assets/images/buttons/enzosButtons.png?as=run'
  import { onMount } from 'svelte';

  const sites = [
	{
		name: 'Reddoor',
		link: 'https://reddoorla.com/',
		screencap: redoorButtons
	},
	{
		name: 'ERP',
		link: 'https://erpfunds.com/',
		screencap: erpButtons
	},
	{
		name: '1-800-Dentist',
		link: 'https://1800dentist.com/',
		screencap: oneEightButtons
	},
	{
		name: 'Beachfront Dentistry',
		link: 'https://www.beachfrontdentistry.com/',
		screencap: beachfrontButtons
	},
	{
		name: 'Gallery Sonder',
		link: 'https://gallerysonder.com/',
		screencap: sonderButtons
	},
	{
		name: 'Hearts & Minds',
		link: 'https://www.lahomelessnessawareness.org/',
		screencap: heartsButtons
	},
	{
		name: 'Espada',
		link: 'https://espadarealestate.com/',
		screencap: espadaButtons
	},
	{
		name: 'Evidence360',
		link: 'http://www.datadynamiq.com/',
		screencap: evidenceButtons
	},
	{
		name: 'MSOT',
		link: 'https://medicalsolutionsoftx.com/',
		screencap: msotButtons
	},
	{
		name: 'CalTex',
		link: 'https://www.caltexmedical.com/',
		screencap: caltexButtons
	},
	{
		name: 'Hedloc',
		link: 'https://hedloc.netlify.app/',
		screencap: hedlocButtons
	},
	{
		name: 'Coast2Coast',
		link: 'https://www.c2crecruits.com/',
		screencap: c2cButtons
	},
	{
		name: 'Enzos',
		link: 'https://enzoshandwash.com/',
		screencap: enzosButtons
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
			<div class='w-160 h-64 p-8'>
				<a href={site.link} class='w-full h-full relative rounded hover:opacity-95 flex items-center justify-center overflow-hidden'>
					<Img src={site.screencap} class='w-full h-full absolute top-0 left-0 brightness-50 hover:brightness-100 hover:z-30 transition object-cover'/>
					<h1 class='text-white transition z-20'>{site.name}</h1>
				</a>
			</div>
			{/each}
		</div>


	</ContentWidth>
</section>