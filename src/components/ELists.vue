<template>
  <div class="events container">
    <h2 class="subtitle is-3">
    Check out our upcoming events
    </h2>
    <div class="columns is-multiline">
      <div v-for="product in products" :product="product" :key="product.id" class="column is-one-quarter">
        <router-link :to="'/product/' + product.id">
          <Ecard :product="product" />
        </router-link>
      </div>
    </div>
  </div>
</template>

<script>
  import Ecard from '@/components/Ecard';
  export default {
    name: 'ELists',
    components : {
      Ecard
    },
  data () {
    return {
      product: {},
      products: [
        {
          id: 1,
          displayName: 'Ariel Matic',
          shortDescription: 'Ariel Matic Top Load Detergent Washing Powder - 4 kg with Free Detergent Powder - 2 kg',
          description: 'New & Improved Ariel Matic gives you tough stain removal for a bright clean in just 1 wash. Especially designed to be used in front loading machines, Ariel Matic Front Load offers brilliant stain removal for full loads. The new Brightguard technology keeps your clothes bright wash after wash. Ariel Matic powder also provides deep down cleaning and long-lasting freshness. Formulated specifically for fully automatic washing machines, it generates the right amount of foam in the machine to deliver superior cleaning inside the machine itself, without damaging the machine due to excess foam. It requires just 1 scoop for normal loads, and 1.5 scoops for heavy loads, providing performance along with value. Ariel Matic’s cutting edge technology provides impeccable cleaning for all your clothes, and removes tough stains like juice, chocolate, tomato and butter/ghee and maintains the brightness of the clothes. So now, goodbye stains and dullness!',
          category: 'essentials',
          price: '300',
          deliveryCharge: '0',
          sellerCount: '10',
          avgRating: '3.5',
          image : 'https://minutebag.com/wp-content/uploads/2018/10/ariel-matic-fl-2kg1.gif',
          reviews :[
              {
                  title: "Very Good Product",
                  body: "I’ve been using these products since a long time and ariel products are best !!!!!!"
              },
               {
                  title: "Love it",
                  body:  "The product is amazing . Highly recommend it "
              }
          ]
        },
        {
          id: 2,
          displayName: 'Surf',
          shortDescription: 'Surf Top Load Detergent Washing Powder - 4 kg with Free Detergent Powder - 2 kg',
          description: 'New & Improved Surf gives you tough stain removal for a bright clean in just 1 wash. Especially designed to be used in front loading machines, Ariel Matic Front Load offers brilliant stain removal for full loads. The new Brightguard technology keeps your clothes bright wash after wash. Ariel Matic powder also provides deep down cleaning and long-lasting freshness. Formulated specifically for fully automatic washing machines, it generates the right amount of foam in the machine to deliver superior cleaning inside the machine itself, without damaging the machine due to excess foam. It requires just 1 scoop for normal loads, and 1.5 scoops for heavy loads, providing performance along with value. Ariel Matic’s cutting edge technology provides impeccable cleaning for all your clothes, and removes tough stains like juice, chocolate, tomato and butter/ghee and maintains the brightness of the clothes. So now, goodbye stains and dullness!',
          category: 'essentials',
          price: '500',
          deliveryCharge: '70',
          sellerCount: '10',
          avgRating: '4.5',
          image : 'https://placekitten.com/500/500',
          reviews :[
              {
                  title: "Very Good Product",
                  body: "I’ve been using these products since a long time and the products are best !!!!!!"
              },
               {
                  title: "Love it",
                  body:  "The product is amazing . Highly recommend it "
              }
          ]
        }
      ],
    }
  }
  }
</script>
<style lang="scss" scoped>
  .events {
    margin-top: 100px;
    text-align: center;
  }
</style>