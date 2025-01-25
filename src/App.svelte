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

	const deleteFeedback = (e) =>{
		const itemId = e.detail
		feedback = feedback.filter((item) => item.id != itemId)
	}
</script>

<main class = "container">
	<FeedbackList {feedback} on:delete-feedback=
	{deleteFeedback} />
</main>

