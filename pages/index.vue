<template>
  <div>
    <div class="sm:flex mb-4 landing-page-banner">
      <div class="sm:w-1/2 landing-page-left-div sm:flex justify-center">
        <div class="div-wrapper">
          <div class="bold-header">
            The Business
            <span>Software</span>
            for a Connected Economy
          </div>
          <div class="light-text-header top-text">
            Transform with Cloudenly and experience the power of a unified
            business operation.
          </div>
          <div class="light-text-header bottom-text">
            CRM. Sales. Purchase. Inventory. Operations. Commerce. Finance.
            Cloud Storage. HRM.
          </div>
          <div class="call-to-action-div sm:flex">
            <button class="blue-btn">TRY FOR FREE</button>
            <button class="white-btn-border">EXPLORE MORE</button>
          </div>
        </div>
      </div>
      <div class="sm:w-1/2 landing-page-right-div flex">
        <img src="/img/mana-img.svg" />
      </div>
    </div>
    <div class="enterprices flex flex-wrap">
      <div class="trust-enterprices">
        Trusted by your favourite enterprises.
      </div>
      <div class="enterprice-box">
        <img src="/img/Mansaard-logo.svg" />
        Mansaard Inc.
      </div>
      <div class="enterprice-box">
        <img src="/img/YorkShire-logo.svg" />
        YorkShire Ent.
      </div>
      <div class="enterprice-box">
        <img src="/img/Shally-logo.svg" />
        YorkShire Ent.
      </div>
      <div class="enterprice-box">
        <img src="/img/Circle-logo.svg" />
        Circle Comp
      </div>
      <div class="chat-icon-div">
        <img src="/img/chat-icon.svg" />
      </div>
    </div>
    <div class="cloudenly-suite sm:flex">
      <div class="cloudenly-headline">Cloudenly Suite</div>
      <div class="cloudenly-light-headline">
        Our Product help your team work from anywhere delivering exceptional
        customer experiences.
      </div>
      <div class="products-container sm:flex">
        <div class="product-div">
          <div class="product-top-line optima-top"></div>
          <div class="product-desc">
            <img src="/img/Optima-logo.svg" />
            <div class="product-name">Optima</div>
            <div class="product-explain">
              Streamline your retail, supply chain, commerce, finance, and
              accounting for improved customer experience, operational
              efficiency, business intelligence, and agility.
            </div>
            <button class="product-btn optima-btn">TRY FOR FREE</button>
          </div>
        </div>
        <div class="product-div">
          <div class="product-top-line humana-top"></div>
          <div class="product-desc">
            <img src="/img/Humana-logo.svg" />
            <div class="product-name">HumanaR</div>
            <div class="product-explain">
              Amplify your HR processes with ease, and achieve better employee
              experience with self-service. Improve people and business
              performance through workforce analytics.
            </div>
            <button class="product-btn humana-btn">TRY FOR FREE</button>
          </div>
        </div>
        <div class="product-div">
          <div class="product-top-line dome-top"></div>
          <div class="product-desc">
            <img src="/img/Dome-logo.svg" />
            <div class="product-name">Dome</div>
            <div class="product-explain" style="max-width: 247px">
              Manage files and folders securely on the cloud and collaborate
              remotely. Enjoy the boundless opportunity.
            </div>
            <button class="product-btn dome-btn">TRY FOR FREE</button>
          </div>
        </div>
        <div class="product-div lite-margin">
          <div class="product-top-line lite-top"></div>
          <div class="product-desc">
            <img src="/img/Optima-logo.svg" />
            <div class="product-name">Lite</div>
            <div class="product-explain">
              Built for micro and small businesses, to unify purchase,
              inventory, sales, customer, expense management, and more. Scaling
              from Lite to other Apps is seamless.
            </div>
            <button class="product-btn lite-btn">TRY FOR FREE</button>
          </div>
        </div>
      </div>
    </div>
    <WhyCloudenly />
    <div class="high-growth-companies sm:flex justify-center">
      <div class="cloudenly-headline">
        Powering Growth for Amazing Businesses.
      </div>
      <div
        class="sm:flex justify-center brand-wrapper"
        style="margin-top: 30px"
      >
        <div class="company-div"><img src="/img/aws.png" /></div>
        <div class="company-div"><img src="/img/beans.png" /></div>
        <div class="company-div"><img src="/img/oya.png" /></div>
        <div class="company-div"><img src="/img/microsoft.png" /></div>
        <div class="company-div"><img src="/img/slack.png" /></div>
      </div>
      <button class="blue-btn all-brand-btn">SEE ALL BRANDS</button>
    </div>
    <ProductPackComponent />
    <div class="try-product-free sm:flex justify-center">
      <div class="cloudenly-headline">Try Cloudenly for free.</div>
      <div class="free-try-text">
        No software installation required, no credit card required, easy to
        setup.
      </div>
      <button class="blue-btn free-try-btn">TRY FOR FREE</button>
    </div>
  </div>
</template>

<script>
import WhyCloudenly from '../components/contents/WhyCloudenly'
import ProductPackComponent from '../components/contents/ProductPackComponent'
export default {
  components: {
    WhyCloudenly,
    ProductPackComponent,
  },
  data() {
    return {
      frame: 3,
      rightArrow: true,
      leftArrow: false,
      scrollWidth: 0,
      count: 0,
    }
  },
  methods: {
    previous() {
      // this.portArrowRight=true;
      this.count--
      this.count = this.count--
      this.scroll('previous')
    },
    next() {
      // this.portArrowLeft=true;
      this.count++
      this.count = this.count++
      this.scroll('next')
    },
    scroll(position) {
      const el = document.getElementById('slide')
      let pos = 0
      const id = setInterval(frame, 5)
      const num = 3 - this.frame
      const width = 200
      const resize = num * width
      const check = position === 'reset' ? resize : width
      // var obj=this;
      function frame() {
        if (pos === check) {
          clearInterval(id)
        } else {
          pos += 5
          if (position === 'next') {
            el.scrollLeft += 5
          } else {
            el.scrollLeft -= 5
          }
          // obj.portfolioScroll(el.scrollLeft);
        }
      }
    },
  },
}
</script>

<style scoped>
@media (max-width: 768px) {
  .white-btn-border {
    margin-top: 20px;
  }
  .header-text-light {
    margin-top: 20px;
  }
}
</style>
