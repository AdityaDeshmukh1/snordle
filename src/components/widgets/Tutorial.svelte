<script lang="ts">
	import { Tile } from "../board";
	export let visible: boolean;
</script>

<h3>how to play</h3>
<div>You already know how to play Wordle Sneha :P</div>

<div class:complete={visible} class="examples">
	<div><strong>Examples</strong></div>
	<div class="row">
		<Tile value="s" state="🟩" />
		<Tile value="n" state="🔳" />
		<Tile value="e" state="🔳" />
		<Tile value="b" state="🔳" />
		<Tile value="o" state="🔳" />
	</div>
	<div>The letter <strong>S</strong> is in the word and in the correct spot.</div>
	<div class="row">
		<Tile value="b" state="🔳" />
		<Tile value="a" state="🟨" />
		<Tile value="l" state="🔳" />
		<Tile value="l" state="🔳" />
		<Tile value="s" state="🔳" />
	</div>
	<div>The letter <strong>A</strong> is in the word but in the wrong spot.</div>
	<div class="row">
		<Tile value="m" state="🔳" />
		<Tile value="u" state="🔳" />
		<Tile value="c" state="🔳" />
		<Tile value="h" state="⬛" />
		<Tile value="u" state="🔳" />
	</div>
	<div>The letter <strong>H</strong> is not in the word in any spot.</div>
</div>
<div>
	I really love you bubs, I know I'm busy sometimes so you can just pass the time playing Snordle (Sneha + Wordle?) for as long as you want baby.
</div>

<style lang="scss">
	div {
		margin: 14px 0;
	}
	.examples {
		border-top: 1px solid var(--border-primary);
		border-bottom: 1px solid var(--border-primary);
		:global(.row > *) {
			height: 100%;
			aspect-ratio: 1;
		}
		&:not(.complete) :global(.row .back) {
			transition-delay: 0.3s;
		}
	}
	.row {
		height: 40px;
		display: flex;
		gap: 4px;
	}
</style>
