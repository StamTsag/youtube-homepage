<script lang="ts">
	import Time from 'svelte-time';

	const videos: {
		thumbnailUrl: string;
		channelIcon: string;
		title: string;
		channelName: string;
		views: number;
		timestamp: number;
		duration: string;
		isLivestream?: boolean;
		watching?: number;
	}[] = [
		{
			thumbnailUrl:
				'https://i.ytimg.com/vi/BxoyTHOjBt0/hqdefault.jpg?sqp=-oaymwEcCOADEI4CSFXyq4qpAw4IARUAAIhCGAFwAcABBg==&rs=AOn4CLC4M_Fh6dUqPrZVQx9weEhJBKbLOg',
			channelIcon:
				'https://yt3.ggpht.com/2X1m6RdHR-jHpiGx3DuxLPXTb1k7Bz9dRrDojfWo6vEb84iboyeG2A4XBijcMQVM9k2ZOT6E6A=s68-c-k-c0x00ffffff-no-rj',
			title: 'FEAR NOTHING ~ edit',
			channelName: 'politelycorrect',
			views: 7400,
			timestamp: new Date('2022-10-26').getTime(),
			duration: '2:15'
		},
		{
			thumbnailUrl:
				'https://i.ytimg.com/vi/ueTXYhtlnjA/hq720.jpg?sqp=-oaymwEcCNAFEJQDSFXyq4qpAw4IARUAAIhCGAFwAcABBg==&rs=AOn4CLBlJq-rqxY8RqFdLNbBeInlZZJ0Ag',
			channelIcon:
				'https://yt3.ggpht.com/ytc/AMLnZu8oeNG2CnItst0bHiVcqKj8ZEdOXUS2x-sGCNF6=s68-c-k-c0x00ffffff-no-rj',
			title: "It's time... for PYTHON 3.11!",
			channelName: 'mCoding',
			views: 88000,
			timestamp: new Date('2022-10-24').getTime(),
			duration: '8:10'
		},
		{
			thumbnailUrl:
				'https://i.ytimg.com/vi/cybUqDRYUnk/hq720.jpg?sqp=-oaymwEcCNAFEJQDSFXyq4qpAw4IARUAAIhCGAFwAcABBg==&rs=AOn4CLAlvp8XOVnwfJsGHRQ1qdnUHX5kag',
			channelIcon:
				'https://yt3.ggpht.com/2orR2vekDJ0aM_lNVxGcWS03x5xXIGVv_NlMAoS3tqd9TkCzwgRTgRFq-3_vPisiO9gLngJX8g=s68-c-k-c0x00ffffff-no-rj',
			title: 'How Woke Grifters are Ruining the Workplace',
			channelName: 'Think Before You Sleep',
			views: 54000,
			timestamp: new Date('2022-10-27').getTime(),
			duration: '31:00'
		},
		{
			thumbnailUrl:
				'https://i.ytimg.com/vi/ZLg4nhNTT5Y/hq720.jpg?sqp=-oaymwEcCNAFEJQDSFXyq4qpAw4IARUAAIhCGAFwAcABBg==&rs=AOn4CLCez7CekgExl6lPaFw7R-xAOEaUQQ',
			channelIcon:
				'https://yt3.ggpht.com/z-m4FNdZE9htx5wsm3Twz-PLFH29YwAhWIw6I-975YFne2zfzQObkqcwHRiIBiZToJuFUqO8=s68-c-k-c0x00ffffff-no-rj',
			title:
				"Are you feeling behind in life bro? You're literally 2 years old, go easy on yourself",
			channelName: 'Hamza',
			views: 306000,
			timestamp: new Date('2021-12-01').getTime(),
			duration: '21:31'
		},
		{
			thumbnailUrl:
				'https://i.ytimg.com/vi/QKgTZWbwD1U/hq720.jpg?sqp=-oaymwEcCNAFEJQDSFXyq4qpAw4IARUAAIhCGAFwAcABBg==&rs=AOn4CLDB1QNESNGOIjm1QOWYGj-8VFRWqQ',
			channelIcon:
				'https://yt3.ggpht.com/ytc/AMLnZu80d66aj0mK3KEyMfpdGFyrVWdV5tfezE17IwRkhw=s68-c-k-c0x00ffffff-no-rj',
			title: 'Godot in 100 seconds',
			channelName: 'Fireship',
			views: 219000,
			timestamp: new Date('2022-10-25').getTime(),
			duration: '2:40'
		},
		{
			thumbnailUrl:
				'https://i.ytimg.com/vi/Cdp-nSNm1bk/hqdefault.jpg?sqp=-oaymwEcCOADEI4CSFXyq4qpAw4IARUAAIhCGAFwAcABBg==&rs=AOn4CLBtn1nKuMNaOIkwLaj00bzWWyYTog',
			channelIcon:
				'https://yt3.ggpht.com/o_t7dOv9r3zbQWFUnTW5qd4237HwrxZExcN9tcKii6imS0slqSOcOrOHrVil8HAKRq_zK3KBW90=s68-c-k-c0x00ffffff-no-rj',
			title: '7 Relationship Behaviors You Should Never Tolerate',
			channelName: 'Psych2Go',
			views: 53000,
			timestamp: new Date('2022-10-26').getTime(),
			duration: '3:57'
		},
		{
			thumbnailUrl:
				'https://i.ytimg.com/vi/-eTblF79ygA/hq720.jpg?sqp=-oaymwEcCNAFEJQDSFXyq4qpAw4IARUAAIhCGAFwAcABBg==&rs=AOn4CLDKpBydne3eAJtsaZYZt2WvwiJXdA',
			channelIcon:
				'https://yt3.ggpht.com/ytc/AMLnZu9tnLidv7Bc6_DYVf_tg4tvqhV-v-U4NilQqzY9=s68-c-k-c0x00ffffff-no-rj',
			title: 'DID ANDREW TATE JUST ACCEPT ISLAM?',
			channelName: 'Ali Dawah',
			views: 622000,
			timestamp: new Date('2022-10-23').getTime(),
			duration: '9:24'
		},
		{
			thumbnailUrl:
				'https://i.ytimg.com/vi/qpre30WHIiQ/hqdefault.jpg?sqp=-oaymwEcCOADEI4CSFXyq4qpAw4IARUAAIhCGAFwAcABBg==&rs=AOn4CLDwWUQLr2t4L3OPQXE-d7cYIIA34A',
			channelIcon:
				'https://yt3.ggpht.com/2fclvwpxV56TKX2eTi2VdGFNtNkHi6esNDVZeTotULWIEipeuFEgpOSfiPLS3ef0Yx5x2f1f=s68-c-k-c0x00ffffff-no-rj',
			title: 'The truth about Iman Gadzhi',
			channelName: 'Sigma Financial',
			views: 6500,
			timestamp: new Date('2022-10-27').getTime(),
			duration: '8:47'
		},
		{
			thumbnailUrl:
				'https://i.ytimg.com/vi/X0W6CX-uHhk/hq720.jpg?sqp=-oaymwEcCNAFEJQDSFXyq4qpAw4IARUAAIhCGAFwAcABBg==&rs=AOn4CLBDFYyh1_pTHGRHOpHuV06fhoF3gw',
			channelIcon:
				'https://yt3.ggpht.com/ytc/AMLnZu9ZZRWkIpRhCZEAFuMunSmr68Kxwma-PrLfOksccw=s68-c-k-c0x00ffffff-no-rj',
			title: "All I'm Offering is the Truth | The Philosophy of the Matrix",
			channelName: 'Einzelgänger',
			views: 1500000,
			timestamp: new Date('2021-10-21').getTime(),
			duration: '23:10'
		},
		{
			thumbnailUrl:
				'https://i.ytimg.com/vi/5GvTWMCd7AA/hq720.jpg?sqp=-oaymwEcCNAFEJQDSFXyq4qpAw4IARUAAIhCGAFwAcABBg==&rs=AOn4CLDCgfaVgQgCXabHuubf96xXCZncdw',
			channelIcon:
				'https://yt3.ggpht.com/vIhQIfjf_lOd_Fi-ZCcZnzFxTQD_22eEkke7MS_bDwEmBgQ-n19MKGjrGozY1DChxuqQZumzaw=s68-c-k-c0x00ffffff-no-rj',
			title: '"KILL ALL MEN AND MALE BABIES"',
			channelName: 'Balkan Gains',
			views: 1000000,
			timestamp: new Date('2022-02-10').getTime(),
			duration: '1:00'
		},
		{
			thumbnailUrl:
				'https://i.ytimg.com/vi/ZMIt7Tf7f7g/hq720.jpg?sqp=-oaymwEcCNAFEJQDSFXyq4qpAw4IARUAAIhCGAFwAcABBg==&rs=AOn4CLAYMmCXSx9M6LTpU_Tg3ezQTihpkg',
			channelIcon:
				'https://yt3.ggpht.com/rPTMAygaSNkMnSRNRscSk8LYA_d_lUSUbVnswtDjYpzz_Xf7WXXvCL4G7eDmgclQqcIJRwwBAw4=s68-c-k-c0x00ffffff-no-rj',
			title: '#1 Rule of the internet:',
			channelName: 'Beluga',
			views: 14000,
			timestamp: new Date('2022-10-27').getTime(),
			duration: '3:08'
		},
		{
			thumbnailUrl:
				'https://i.ytimg.com/vi/lCTjCFhpIR8/hq720_live.jpg?sqp=CLCU6poG-oaymwEcCNAFEJQDSFXyq4qpAw4IARUAAIhCGAFwAcABBg==&rs=AOn4CLCkoEPoziXGyS0kt1a3KeQClqPYig',
			channelIcon:
				'https://yt3.ggpht.com/ytc/AMLnZu_5kbrJzpSCIx4i60Rj0BlseBoGjYs-sJFMV53PNQ=s68-c-k-c0x00ffffff-no-rj',
			title: 'JetBrains GameDev Day Online 2022',
			channelName: 'JetBrainsTV',
			views: -1,
			timestamp: -1,
			duration: '',
			isLivestream: true,
			watching: 242
		},
		{
			thumbnailUrl:
				'https://i.ytimg.com/vi/0219isX81Q8/hq720.jpg?sqp=-oaymwEcCNAFEJQDSFXyq4qpAw4IARUAAIhCGAFwAcABBg==&rs=AOn4CLBWiMc8_qmT6enHpzHraKDGyNwMYw',
			channelIcon:
				'https://yt3.ggpht.com/81vc3m0OrDr944weRwj3UgjfOuKKm0WU36bY5B1qJaW_qjRM8yrO7huIJaIF6kZ8EEqW76vd2Q=s68-c-k-c0x00ffffff-no-rj',
			title: '$10,000 per month is achievable for anyone who tries',
			channelName: 'Hamza Unfiltered',
			views: 245000,
			timestamp: new Date('2021-12-07').getTime(),
			duration: '25:36'
		},
		{
			thumbnailUrl:
				'https://i.ytimg.com/vi/X_qEJcYASQg/hq720.jpg?sqp=-oaymwEcCNAFEJQDSFXyq4qpAw4IARUAAIhCGAFwAcABBg==&rs=AOn4CLDSznFUXc6n-oMQNso-YD2c_CDYSQ',
			channelIcon:
				'https://yt3.ggpht.com/z-m4FNdZE9htx5wsm3Twz-PLFH29YwAhWIw6I-975YFne2zfzQObkqcwHRiIBiZToJuFUqO8=s68-c-k-c0x00ffffff-no-rj',
			title: 'Delete TikTok now',
			channelName: 'Hamza',
			views: 245000,
			timestamp: new Date('2021-07-27').getTime(),
			duration: '23:01'
		}
	];
</script>

<div class="videos">
	{#each videos as { thumbnailUrl, channelIcon, title, channelName, views, timestamp, duration, isLivestream, watching }}
		<div id="general">
			<img id="thumbnail" src={thumbnailUrl} alt={`${title}'s thumbnail`} draggable={false} />
			<div id="below">
				<img id="icon" src={channelIcon} alt={`${channelIcon}'s icon`} />

				<div id="below-info">
					<h1 id="title">{title}</h1>
					<h1 id="channel">{channelName}</h1>

					{#if !isLivestream}
						<h1 id="grouped">
							{Intl.NumberFormat('en-US', { notation: 'compact' }).format(views)} views •
							<Time relative format={'dddd HH:mm · MMMM D YYYY'} live={60000} {timestamp} />
						</h1>
					{:else}
						<h1 id="grouped">
							Live • {Intl.NumberFormat('en-US', { notation: 'compact' }).format(watching)} watching
						</h1>
					{/if}
				</div>
			</div>
		</div>
	{/each}
</div>

<style>
	.videos {
		display: flex;
		flex-direction: row;
		align-items: start;
		justify-content: center;
		flex-wrap: wrap;
		z-index: -1;
		margin-left: 85px;
		margin-top: 10px;
	}

	.videos #general {
		width: 350px;
		cursor: pointer;
		transition: 0.25s;
		margin-right: 10px;
		margin-bottom: 50px;
	}

	.videos #general img {
		width: 350px;
		border-radius: 5px;
		transition: 0.25s;
	}

	#below {
		display: flex;
	}

	#below #icon {
		width: 48px;
		height: 48px;
		margin-right: 5px;
	}

	#below-info {
		display: flex;
		flex-direction: column;
	}

	#below-info #title {
		font-size: 1rem;
		display: -webkit-box;
		overflow: hidden;
		width: 100%;
		-webkit-line-clamp: 4;
		-webkit-box-orient: vertical;
		font-weight: 900;
	}

	#below-info #channel {
		font-size: 1rem;
	}

	#below-info #grouped {
		font-size: 0.9rem;
	}

	@media screen and (max-width: 850px) {
		.videos #general {
			width: 300px;
		}

		.videos #general img {
			width: 300px;
		}

		#below #icon {
			width: 40px;
			height: 40px;
		}

		#below-info #title {
			font-size: 0.9rem;
		}

		#below-info #channel {
			font-size: 0.9rem;
		}

		#below-info #grouped {
			font-size: 0.9rem;
		}
	}

	@media screen and (max-width: 750px) {
		.videos {
			margin-top: 75px;
			margin-left: 0;
		}

		.videos #general {
			width: 100%;
			justify-content: center;
			align-items: center;
			text-align: center;
			margin: 0;
			margin-bottom: 50px;
		}

		.videos #general img {
			width: 60%;
		}

		#below {
			width: 100%;
			text-align: center;
			justify-content: center;
			align-items: center;
		}

		#below #icon {
			width: 48px;
			height: 48px;
		}

		#below-info {
			width: 50%;
		}

		#below-info #title {
			font-size: 1rem;
			max-width: initial;
			width: 90%;
		}

		#below-info #channel {
			font-size: 1rem;
		}

		#below-info #grouped {
			font-size: 1rem;
		}
	}
</style>
