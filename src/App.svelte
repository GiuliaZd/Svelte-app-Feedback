<script>
  import FeedbackList from "./components/FeedbackList.svelte";

  let feedback = [
    {
      id: "1",
      rating: "3",
      text: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Unde perferendis molestias sint alias dicta ratione rem cupiditate quae qui ea ex ad ullam, optio excepturi eos! Aspernatur, autem veritatis? Veniam?",
    },
    {
      id: "2",
      rating: "10",
      text: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Unde perferendis molestias sint alias dicta ratione rem cupiditate quae qui ea ex ad ullam, optio excepturi eos! Aspernatur, autem veritatis? Veniam?",
    },
    {
      id: "3",
      rating: "5",
      text: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Unde perferendis molestias sint alias dicta ratione rem cupiditate quae qui ea ex ad ullam, optio excepturi eos! Aspernatur, autem veritatis? Veniam?",
    },
  ];
</script>

<main>
  <FeedbackList {feedback} />
</main>
