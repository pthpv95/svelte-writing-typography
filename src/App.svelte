<script>
  let rows = new Array(12).fill(0)
  let columns = new Array(9).fill(0)
  let text=''
</script>

<main>
  <div>
    <textarea cols="5" rows="5" class="input-text" bind:value={text} />
  </div>

  <div class="board">
    <div class="main-content"><p>{text}</p></div>
    {#each columns as column}
      <div class="cells">
        {#each rows as row}
          <table class="cell">
            <tr>
              <td>
                <div class="content" />
              </td>
              <td>
                <div class="content" />
              </td>
              <td>
                <div class="content" />
              </td>
              <td>
                <div class="content" />
              </td>
            </tr>
            <tr>
              <td>
                <div class="content" />
              </td>
              <td>
                <div class="content" />
              </td>
              <td>
                <div class="content" />
              </td>
              <td>
                <div class="content" />
              </td>
            </tr>
            <tr>
              <td>
                <div class="content" />
              </td>
              <td>
                <div class="content" />
              </td>
              <td>
                <div class="content" />
              </td>
              <td>
                <div class="content" />
              </td>
            </tr>
            <tr>
              <td>
                <div class="content" />
              </td>
              <td>
                <div class="content" />
              </td>
              <td>
                <div class="content" />
              </td>
              <td>
                <div class="content" />
              </td>
            </tr>
          </table>
        {/each}
      </div>
    {/each}
  </div>
</main>

<style>
  main {
    font-family: 'tapviet';
    height: 100%;
    width: 100%;
  }

  .main-content {
    position: absolute;
    z-index: 101;
    top: -10px;
  }
  .main-content p {
    font-size: 50px;
  }
  .input-text {
    width: 100%;
    font-size: 30px;
  }

  .board {
    background-color: #d3effc;
    padding: 10px;
    width: fit-content;
    margin: 0 auto;
    position: relative;
    z-index: 100;
  }

  .cells {
    display: flex;
    justify-content: center;
  }
  .cell {
    width: 80px;
    height: 80px;
  }

  table {
    width: 100%;
    border-spacing: 1px;
  }

  td {
    width: 25%;
    position: relative;
  }

  td:after {
    content: '';
    display: block;
    margin-top: 100%;
  }

  td .content {
    position: absolute;
    top: 0;
    bottom: 0;
    left: 0;
    right: 0;
    background: white;
  }
</style>
