<script>
  import FeedbackList from "./components/FeedbackList.svelte";
  import FeedbackStats from "./components/FeedbackStats.svelte";
  import FeedbackForm from "./components/FeedbackForm.svelte";

  let feedback = [
    {
      id: 1,
      rating: 10,
      text: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Unde perferendis molestias sint alias dicta ratione rem cupiditate quae qui ea ex ad ullam, optio excepturi eos! Aspernatur, autem veritatis? Veniam?",
    },
    {
      id: 2,
      rating: 9,
      text: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Unde perferendis molestias sint alias dicta ratione rem cupiditate quae qui ea ex ad ullam, optio excepturi eos! Aspernatur, autem veritatis? Veniam?",
    },
    {
      id: 3,
      rating: 8,
      text: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Unde perferendis molestias sint alias dicta ratione rem cupiditate quae qui ea ex ad ullam, optio excepturi eos! Aspernatur, autem veritatis? Veniam?",
    },
  ];

  $: count = feedback.length;
  $: average =
    feedback.reduce((a, { rating }) => a + rating, 0) / feedback.length;

  const deleteFeedback = (e) => {
    const itemId = e.detail;
    feedback = feedback.filter((item) => item.id != itemId);
  };
</script>

<main class="container">
  <FeedbackForm />
  <FeedbackStats {count} {average} />
  <FeedbackList {feedback} on:delete-feedback={deleteFeedback} />
</main>
