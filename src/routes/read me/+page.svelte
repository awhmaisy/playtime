<script>
    let items = [
      { title: "physical theory of diffraction", type: "defense", year: 1971, image: "images/f117.jpg", description: "great and incredulous research" },
      { title: "x_x", type: "parsing and collecting", year: 2099, image: "images/miracles are created.jpg", description: "soon, you may see" },
      { title: "old microsoft", type: "parsing and collecting", year: 2099, image: "images/microsoft.png", description: "i wonder if i may have loved you in another life" },
    ];
  
    let selectedItem = null;
  
    function selectItem(item) {
      selectedItem = item;
    }
  </script>
  
  <div class="container">
    <div class="left-side">
      {#each items as item}
        <div class="item" on:click={() => selectItem(item)}>
          {item.title} - {item.type} - {item.year}
        </div>
      {/each}
    </div>
    <div class="right-side">
      {#if selectedItem}
        <img src={selectedItem.image} alt={selectedItem.title} style="width: 100%;" />
        <p class="description">{selectedItem.description}</p>
      {/if}
    </div>
  </div>

  <style>
    .container {
      display: flex;
    }
    .left-side {
      width: 50%;
    }
    .right-side {
      width: 50%;
      padding-left: 20px;
    }
    .item {
      cursor: pointer;
      padding: 10px;
      border-bottom: 1px solid #ccc;
    }
    .item:hover {
      background-color: #f0f0f0;
    }
    .description {
      margin-top: 10px;
      padding-bottom: 100px;
      text-align: justify;
      font-size: 12px;
    }
  </style>