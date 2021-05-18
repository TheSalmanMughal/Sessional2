# Sessional2

$(function () {
  $("#all").on("click", getAll);
  $("#get1").on("click", get1);
});

function getAll() {
  $.ajax({
    url: "https://jsonplaceholder.typicode.com/todos",
    method: "GET",
    success: function (response) {
      var Room = $("#response");
      Room.empty();
      for (var i = 0; i < response.length; i++) {
        var Vas = response[i];
        hotels.append(
          `<div class="response"><h3>${Vas.title}</h3><button class="btn btn-warning">Edit</button><button class="btn btn-danger  ">Delete</button><p style="font-weight:bold;">ID:${Vas.id}<br />USER ID:${Vas.userId} </p></div>`
        );
      }
    },
  });
}


----------


<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link
      href="https://cdn.jsdelivr.net/npm/bootstrap@5.0.0-beta3/dist/css/bootstrap.min.css"
      rel="stylesheet"
      integrity="sha384-eOJMYsd53ii+scO/bJGFsiCZc+5NDVN2yr8+0RDqr0Ql0h+rP48ckxlpbzKgwra6"
      crossorigin="anonymous"
    />
    <link rel="stylesheet" href="style.css" />
    <script
      src="https://code.jquery.com/jquery-3.6.0.js"
      integrity="sha256-H+K7U5CnXl1h5ywQfKtSj8PCmoN9aaq30gDh27Xc0jk="
      crossorigin="anonymous"
    ></script>

    <title>Lab Sessional 2</title>
  </head>
  <body>
    <section>
      <main>
        <div id="container">
          <label for="search">Room Id:</label>
          <input type="text" id="search" placeholder="Enter Id..." />
          <button id="all">Get All</button>
          <button id="get1">Get 1</button>
          <button id="create">Create</button>
          <button id="delete">Delete</button>
          <button id="update">Update</button>
          <div id="response">Response:</div>
        </div>
      </main>
    </section>
  </body>
  <script src="jquery.js"></script>
</html>
