<script>
import FeedbackList from "./components/FeedbackList.svelte";
import FeedbackStats from "./components/FeedbackStats.svelte";

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

	$: count = feedback.length
	$: average = feedback.reduce((a,{rating}) => a + rating , 0) / feedback.length

	const deleteFeedback = (e) =>{
		const itemId = e.detail
		feedback = feedback.filter((item) => item.id != itemId)
	}
</script>

<main class = "container">
	<FeedbackStats {count} {average} />
	<FeedbackList {feedback} on:delete-feedback=
	{deleteFeedback} />
</main>

