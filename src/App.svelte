<script>
import FeedbackList from "./components/FeedbackList.svelte";

	let feedback = [
		{
			id: 1,
			rating: 10,
			text: 'yeNaNa'
		},
		{
			id: 2,
			rating: 7,
			text: 'yeNaNa'
		},
		{
			id: 3,
			rating: 5,
			text: 'yeNaNa'
		},
		{
			id: 4,
			rating: 6,
			text: 'yeNaNa'
		},
	]
</script>

<main>
	<FeedbackList {feedback}/>
</main>

