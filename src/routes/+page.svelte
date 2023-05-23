<script lang="ts">
  const clubs = [
    {
      name: "Liverpool",
      image:
        "https://kgo.googleusercontent.com/profile_vrt_raw_bytes_1587515361_10542.jpg",
    },
    {
      name: "Chelsea",
      image:
        "https://upload.wikimedia.org/wikipedia/en/thumb/c/cc/Chelsea_FC.svg/380px-Chelsea_FC.svg.png",
    },
    {
      name: "Manchester City",
      image:
        "https://upload.wikimedia.org/wikipedia/en/thumb/e/eb/Manchester_City_FC_badge.svg/380px-Manchester_City_FC_badge.svg.png",
    },
    {
      name: "Brighton Hove Albion",
      image:
        "https://upload.wikimedia.org/wikipedia/en/thumb/f/fd/Brighton_%26_Hove_Albion_logo.svg/400px-Brighton_%26_Hove_Albion_logo.svg.png",
    },
    {
      name: "West Ham United",
      image:
        "https://upload.wikimedia.org/wikipedia/en/thumb/f/fd/Brighton_%26_Hove_Albion_logo.svg/400px-Brighton_%26_Hove_Albion_logo.svg.png",
    },
  ];
</script>

<div class="grid-container">
  {#each clubs as club}
    <div class="club-tile">
      <div>
        <img src={club.image} alt={club.name} />
      </div>
      {club.name}
    </div>
  {/each}
</div>

<style>
  :global(*) {
    margin: 0;
    padding: 0;
  }
  img {
    object-fit: contain;
    max-width: 100%;
    height: 100px;
  }
  .grid-container {
    display: grid;
    grid-template-columns: repeat(3, minmax(0, 1fr));
    gap: 16px;
    padding: 16px;
  }
  .club-tile {
    padding: 16px;
    background-color: blueviolet;
    color: white;
    height: 200px;
  }
</style>
