<template>
  <!-- <div>
    <b-jumbotron
      class="banner-user banner-header"
      header=":)"
      lead="Moksha"
    ></b-jumbotron>
  </div>-->
  <div>
    <div class="user-info">
      <div class="container">
        <div class="row">
          <div class="col-xs-12 col-md-10 offset-md-1">
            <img class="user-img" src="https://static.productionready.io/images/smiley-cyrus.jpg" />
            <p></p>
            <h4 style="font-weight:700">Moksha</h4>
            <p></p>
            <div style="    text-align: end;">
              <a href="/settings" class="btn btn-sm btn-outline-secondary action-btn">
                <i class="ion-gear-a"></i> Edit Profile Settings
              </a>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="row">
      <b-col sm="12" offset="1">
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
                    <a href="/" class="preview-link">
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
      </b-col>
      <!-- <div class="col-md-3">
        <div style="padding:5px 10px 10px">
          <h1>hello moksha</h1>
        </div>
      </div>-->
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
  }
};
</script>

<style scoped>
.banner-user {
  background-color: #f3f3f3;
  padding: 1rem 2rem;
}
.banner-header {
  color: #373a3c;
  font-family: "titillium web", sans-serif;
}
.user-info {
  background: #f3f3f3;
}
.container {
  padding: 32px 0px 16px;
}
.tag-container {
  margin: 2% 0% 0% 8%;
}

.user-img {
  border-radius: 100px;
  height: 100px;
  width: 100px;
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