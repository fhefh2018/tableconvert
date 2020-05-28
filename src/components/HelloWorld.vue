<script>
export default {
  name: "HelloWorld",
  props: {
    msg: String,
  },
  render(createElement) {
    return createElement(
      "div",
      {
        class: "hello",
        on: {
          dblclick: (e) => {
            console.log(e.target);
          },
        },
      },
      [
        createElement("p", { class: "my-awesome-class" }, "Some cool text1"),
        createElement("p", { class: "my-awesome-class" }, "Some cool text2"),
      ]
    );
  },
};
</script>
