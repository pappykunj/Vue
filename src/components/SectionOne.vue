<template>
  <div>
    <v-layout wrap justify-center >
      <v-flex lg11> 
        <v-layout wrap justify-center style="margin-top:3%">
          <v-flex lg12 px-8 >
            <p style="font-size:25px" >THE MOST <b>LATEST NEWS </b>OF THE WEEK</p>
          </v-flex>
          <v-flex lg4 pa-6 text-center v-for="(item,i) in images" :key="i" >
            <v-card elevation="0"><!--Helps to give the full card structure-->
              <v-layout wrap pa-2>
                <v-flex lg12>
                  <v-img :src="require('../assets/images/'+item.pic)" height="200px"></v-img>
                </v-flex>
                <v-flex lg12 pa-2 text-left class="bold">
                  {{item.content}}
                </v-flex>
                <v-flex lg12 pa-2 text-left>
                  {{item.content1}}
                </v-flex>
                <v-flex lg12 pa-2 text-left class="small" >
                  {{item.content2}}
                </v-flex>
                <v-flex lg6 v-for="(item,i) in images2" :key="i" ></v-flex>
              </v-layout>
            </v-card>
          </v-flex>
        </v-layout>
      </v-flex>
    </v-layout>
    
    <v-layout wrap justify-center>
      <v-flex lg10>
        <v-layout wrap >
          <v-flex lg6 v-for="(item,i) in images2" :key="i" >
            <v-layout wrap>
              <v-flex>
                <v-card elevation="0">
                  <v-layout wrap >
                    <v-flex lg2 >
                      <v-img  class="mx-auto" :src="require('../assets/images/'+item.pic1)" height="70px" ></v-img>
                    </v-flex>
                    <v-flex lg10  px-3 text-left class="boldtext" style="font-size:15px">
                      <v-layout wrap>
                        <v-flex lg12>{{item.content3}}</v-flex>
                        <v-flex lg12 py-3 class="small" >{{item.content4}}</v-flex>
                      </v-layout>
                    </v-flex>
                  </v-layout>
                </v-card>
              </v-flex>
            </v-layout>
          </v-flex>
        </v-layout>
      </v-flex>
    </v-layout>
    <v-layout wrap justify-center style="margin-top:4%">
      <v-flex lg2 style="text-align:center" >
        <v-btn
          outlined
          rounded
          color="indigo"
        >
          View <v-icon>mdi-arrow-right</v-icon>
        </v-btn>
      </v-flex>
    </v-layout>
  </div>
</template>

 

<script>

export default {
  data()
  {
    return{
      images:[
        {
          pic:"pic1.jpg",
          content:"Contrary to the popular belief.Lorem ipsum is not a simply random text",
          content1:"With the number of Corona Virus positive cases declining day by day and business also seeing growth..",
          content2:"Tue,12th Jan 2021"
        },
        {
          pic:"pic2.jpg",
          content:"Contrary to the popular belief.Lorem ipsum is not a simply random text123",
          content1:"With the number of Corona Virus positive cases declining day by day and business also seeing growth..",
          content2:"Tue,12th Jan 2021"
        },
        {
          pic:"pic3.jpg",
          content:"Contrary to the popular belief.Lorem ipsum is not a simply random text321",
          content1:"With the number of Corona Virus positive cases declining day by day and business also seeing growth..",
          content2:"Tue,12th Jan 2021"
        }
      ],
      images2:[
        {
          pic1:"pic2.jpg",
          content3:"Recovering from COVID-19... Tourist footfall increases at Mysore Palace,Zoo-Star of Mysore",
          content4:"Tue,12th Jan 2021"
        },
        {
          pic1:"pic3.jpg",
          content3:"Recovering from COVID-19... Tourist footfall increases at Mysore Palace,Zoo-Star of Mysore",
          content4:"Tue,12th Jan 2021"
        }
      ]
    }
  }
}

</script>