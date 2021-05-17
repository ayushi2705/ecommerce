<template>
  <div class="event-single">

    <section class="event-content">
      <div class="container">

        <div class="event-images columns is-multiline">
            <img class="column is-two-fifths" :src="product.image" :alt="product.name"/>
            <div class="column">
                <p class="is-size-3 "> <strong>{{ product.shortDescription }}</strong> </p>
                <p style="font-size: 15px; color: darkgray; font-weight: 500;"> <span> Ratings: {{ product.avgRating }}/5 </span>
                <span>  &  Seller Count: {{ product.sellerCount }} </span> </p>
                <p style="font-size: 1.5rem; color: #B12704;"> Price: <span> &#8377; </span> {{ product.price }} </p>
                <p style="font-size: .80rem; font-weight: bold; "> Inclusive of all taxes </p>
                <p style="font-size: 1rem;  font-weight: bold;" v-if="product.deliveryCharge == 0">
                    FREE delivery on this product
                </p>
                <p v-else style="font-size: 1rem; font-weight: bold;">
                    Delivery Charges: <span> &#8377; </span> {{ product.deliveryCharge }}
                </p>
            </div>
        </div>

        <hr>

        <div>
         <h2 >PRODUCT DESCRIPTION</h2>
         <p style="font-family: Georgia, Times New Roman, Times, serif; color: #3f414d; font-size: 15px;" >{{ product.description }}</p>
        </div>

        <hr>
        <div>
          <h2>PRODUCT REVIEWS</h2>
          <div class = "overall-review">
              <p style="font-size: 15px; font-weight: 500; padding-top:13px;"> <span> {{ product.avgRating }}/5 <strong>Overall Ratings</strong></span> </p>
          </div>
           <div v-for="review in product.reviews"  :key="review.id" class="column is-half">
            <p  style="font-family: Source Sans Pro,sans-serif; font-size: 15px; font-weight: bold;">" {{review.title}} "</p>
            <p>{{review.body}}</p>
            <hr>
           </div>
        </div>
      </div>
    </section>
  </div>
</template>


<script>
export default {
  name: 'ProductDescription',
  data () {
    return {
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
      product: {}
    }
  },
  created() {
    const ID = Number(this.$route.params.id);
    let event = this.products.find(product => product.id === ID);
    this.product = event;
  }
}
</script>

<style lang="scss" scoped>
  .overall-review {
  width: 190px;
  height: 50px;
  box-shadow: 3px 2px 5px 1px #969696;
  margin: 10px;
  text-align: center;
  }
  hr{
       box-shadow: 3px 2px 5px 0px #969696;
  }
  h2{
      font-family: Georgia, Times New Roman, Times, serif;
      color: #3f414d;
      font-size: 20px;
      margin-top: 32px;
      margin-bottom: 20px;
      font-weight: 400;
  }
</style>
