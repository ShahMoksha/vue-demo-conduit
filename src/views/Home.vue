<template>
  <div>
    <b-jumbotron
      class="banner banner-header"
      header="conduit"
      lead="A place to share your knowledge."
    ></b-jumbotron>
    <router-link to="/NewArticle">New Article</router-link>|
    <router-link to="/settings">Settings</router-link>|
    <router-link to="/User">Moksha</router-link>

    <div class="row">
      <div class="col-md-8 tag-container">
        <b-tabs content-class="mt-3">
          <b-tab title="Your Feed" active>
            <!-- <p>I'm the first tab</p> -->
            <div v-for="(article,index) in articles" :key="index">
              <div class="author-details">
                <div>
                  <a href="#/@authorname/" class="author">{{article.name}}</a>
                  <div class="date">{{article.date}}</div>
                </div>
                <div>
                  <button class="btn btn-sm pull-xs-right btn-outline-primary">
                    <span class="counter">0</span>
                  </button>
                </div>
              </div>
              <div style="text-align: initial;">
                <a href="/" class="preview-link">
                  <h1>{{article.articleTitle}}</h1>
                  <p>{{article.articleAbout}}</p>
                  <span>Read more...</span>
                </a>
                <hr />
              </div>
            </div>
          </b-tab>
          <b-tab title="Global Feed">
            <!-- <p>I'm the second tab</p> -->
             <div v-for="(article,index) in articles" :key="index">
                <div v-if=" index<= 5">
                  <div class="author-details">
                    <div>
                      <a href="#/@authorname/" class="author">{{article.name}}</a>
                      <div class="date">{{article.date}}</div>
                    </div>
                    <div>
                      <button class="btn btn-sm pull-xs-right btn-outline-primary">
                        <span class="counter">0</span>
                      </button>
                    </div>
                  </div>
                  <div style="text-align: initial;">
                    <a href="" class="preview-link">
                      <h1>{{article.articleTitle}}</h1>
                      <p>{{article.articleAbout}}</p>
                      <span>Read more...</span>
                    </a>
                    <hr />
                  </div>
                </div>
              </div>
            
          </b-tab>
        </b-tabs>
      </div>
      <div class="col-md-3" >
          <h4>Popular Tag</h4>
        <div style="padding:5px 10px 10px"  v-for="(article,index) in articles" :key="index" >
          <a href="#/@authorname/" class="preview-link">{{article.tag}}</a>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      articles: [
        {
          id: 1,
          articleTitle: "titleDemo",
          articleAbout: "in demo article",
          tag: "happy",
          name: "Moksha",
          date: "20 june 2018"
        },
        {
          id: 2,
          articleTitle: "titleTest",
          articleAbout: "in test article",
          tag: "as",
          name: "ABC",
          date: "30 june 2018"
        },
        {
          id: 3,
          articleTitle: "titleCheck",
          articleAbout: "in check article",
          tag: "sad",
          name: "Moksha shah",
          date: "2 june 2018"
        },
        {
          id: 4,
          articleTitle: "Demo",
          articleAbout: "in demo article for about",
          tag: "happy",
          name: "Shah",
          date: "20 june 2020"
        },
        {
          id: 5,
          articleTitle: "titleDemo",
          articleAbout: "in demo article",
          tag: "happy",
          name: "XYZ",
          date: "20 AUG 2018"
        },
        {
          id: 6,
          articleTitle: "titleDemo",
          articleAbout: "in demo article",
          tag: "as",
          name: "DEMO",
          date: "20 SEPT 2018"
        },
        {
          id: 7,
          articleTitle: "check title",
          articleAbout: "in demo  chechk aboutarticle",
          tag: "tag",
          name: "TEST",
          date: "27 june 2018"
        },
        {
          id: 8,
          articleTitle: "testDemo",
          articleAbout: "in test about article",
          tag: "sad",
          name: "PQR XYZ",
          date: "20 dec 2020"
        }
      ]
    };
  },
  name: "Home"
  // components: {
  //   HelloWorld
  // }
};
</script>

<style scoped>
.banner {
  background-color: #5cb85c;
  padding: 1rem 2rem;
}
.banner-header {
  color: white;
  font-family: "titillium web", sans-serif;
}
.display-3 {
  font-size: 56px;
  font-family: "titillium web", sans-serif;
  font-weight: 700;
}
.tag-container {
  margin: 0% 0% 0% 8%;
}

.date {
  font-size: 0.8rem;
  color: #bbb;
}

.author {
  font-weight: 500 !important;
  color: #5cb85c;
  text-decoration: none !important;
}

.preview-link {
  color: inherit !important;
  /* touch-action: manipulation; */
  text-decoration: none !important;
  text-align: initial;
}

.author-details {
  display: flex;
  justify-content: space-between;
}
</style>