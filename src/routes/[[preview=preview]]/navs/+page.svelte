<script lang='ts'>
  import ContentWidth from '$lib/components/ContentWidth/ContentWidth.svelte';
  import Img from '@zerodevx/svelte-img';
  import redoorNav from '$lib/assets/images/navs/reddoorNav.png?as=run'
  import erpNav from '$lib/assets/images/navs/erpNav.png?as=run'
  import oneEightNav from '$lib/assets/images/navs/oneEightNav.png?as=run'
  import beachfrontNav from '$lib/assets/images/navs/beachfrontNav.png?as=run'
  import sonderNav from '$lib/assets/images/navs/sonderNav.png?as=run'
  import heartsNav from '$lib/assets/images/navs/heartsNav.png?as=run'
  import espadaNav from '$lib/assets/images/navs/espadaNav.png?as=run'
  import evidenceNav from '$lib/assets/images/navs/dataNav.png?as=run'
  import msotNav from '$lib/assets/images/navs/msotNav.png?as=run'
  import caltexNav from '$lib/assets/images/navs/caltexNav.png?as=run'
  import hedlocNav from '$lib/assets/images/navs/hedlocNav.png?as=run'
  import c2cNav from '$lib/assets/images/navs/c2cNav.png?as=run'
  import enzosNav from '$lib/assets/images/navs/enzosNav.png?as=run'
  import { onMount } from 'svelte';

  const sites = [
	{
		name: 'Reddoor',
		link: 'https://reddoorla.com/',
		screencap: redoorNav
	},
	{
		name: 'ERP',
		link: 'https://erpfunds.com/',
		screencap: erpNav
	},
	{
		name: '1-800-Dentist',
		link: 'https://1800dentist.com/',
		screencap: oneEightNav
	},
	{
		name: 'Beachfront Dentistry',
		link: 'https://www.beachfrontdentistry.com/',
		screencap: beachfrontNav
	},
	{
		name: 'Gallery Sonder',
		link: 'https://gallerysonder.com/',
		screencap: sonderNav
	},
	{
		name: 'Hearts & Minds',
		link: 'https://www.lahomelessnessawareness.org/',
		screencap: heartsNav
	},
	{
		name: 'Espada',
		link: 'https://espadarealestate.com/',
		screencap: espadaNav
	},
	{
		name: 'Evidence360',
		link: 'http://www.datadynamiq.com/',
		screencap: evidenceNav
	},
	{
		name: 'MSOT',
		link: 'https://medicalsolutionsoftx.com/',
		screencap: msotNav
	},
	{
		name: 'CalTex',
		link: 'https://www.caltexmedical.com/',
		screencap: caltexNav
	},
	{
		name: 'Hedloc',
		link: 'https://hedloc.netlify.app/',
		screencap: hedlocNav
	},
	{
		name: 'Coast2Coast',
		link: 'https://www.c2crecruits.com/',
		screencap: c2cNav
	},
	{
		name: 'Enzos',
		link: 'https://enzoshandwash.com/',
		screencap: enzosNav
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
			<div class='w-full h-auto p-8'>
				<a href={site.link} class='relative rounded hover:opacity-95 flex items-center justify-center overflow-hidden h-24'>
					<Img src={site.screencap} class='absolute top-1/2 -translate-y-1/2 left-0 brightness-80 rounded hover:brightness-100 hover:z-30 transition object-cover'/>
					<h1 class='text-white transition z-20 hover:opacity-0'>{site.name}</h1>
				</a>
			</div>
			{/each}
		</div>


	</ContentWidth>
</section>