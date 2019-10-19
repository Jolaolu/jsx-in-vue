
<script>
export default {
  data () {
    return {
      countries: [
        {
          name: 'Nigeria',
          description: 'Nigeria is a large country that has a varied topography. It is about twice the size of the U.S. state of California and is located between Benin and Cameroon. It is the most populated country in africa'
        },
        {
          name: 'USA',
          description: 'The United States of America (USA), commonly known as the United States (U.S. or US) or America, is a country comprising 50 states, a federal district, five major self-governing territories, and various possessions.'
        },
        {
          name: 'China',
          description: "The People's Republic of China, simply known as China (Chinese:中国, pinyin: zhōng guó)is located in East Asia. It is the world's most populous country, with a population of around 1.404 billion. It is a unified multi-ethnic country with the Han nationality as the main nation."
        },
        {
          name: 'Argentina',
          description: "Argentina is a vast country located in the southern part of South America. The eighth largest country in the world, it is the second largest country in South America after Brazil, and it's about one-third the size of the United States. Argentina is bordered by the Andes Mountains and Chile to the west."
        },
        {
          name: 'Cameroon',
          description: "Cameroon is sometimes described as 'Africa in miniature' because it exhibits all the major climates and vegetation of the continent: mountains, desert, rain forest, savanna grassland, and ocean coastland. Cameroon can be divided into five geographic zones."
        },
        {
          name: 'Somalia',
          description: "With a land area of 637,657 square kilometers, Somalia's terrain consists mainly of plateaus, plains and highlands. Its coastline is more than 3,333 kilometers in length, the longest of mainland Africa and the Middle East. It has been described as being roughly shaped like a tilted number seven."
        }

      ]
    }
  },
  props: {

    // where you define props  to be used

    msg: String
  },
  methods: {
    // where you write methods used in your component
  },

  render () {
    return (
      <div>
        <div class="content">
          <h1>Hello, { this.msg } </h1>
          <main class="country-wrapper">
            {
              this.countries.map(country => {
                return (
                  <div class="country-container">
                    <h3 class="country-name ">{country.name}</h3>
                    <article class="country-description">{country.description}</article>
                  </div>
                )
              })
            }
          </main>
        </div>
      </div>
    )
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.content{
  width: 100%;
  .country-wrapper{
    width: 100%;
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    .country-container{
      display: flex;
      flex-direction: column;
      text-align:start;
      margin: 1em;
      padding: .5em;
      width: 28%;
      height: 12em;
      border: .08em solid #c4c4c4;
      .country-name{
        margin: 0;
        margin-bottom: 1em;
      }
    }
  }

}

</style>
