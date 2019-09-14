<template>
  <div>
    <div class="row">
      <div class="col-lg-6 col-sm-6 text-center">
        <card type="contributions">
          <h1 class="card-title">1</h1>
          <h3 class="card-category">eLegacy</h3>
          <p class="card-description">
            Lorem ipsum
          </p>
          <hr />

          <template slot="footer">
            <div class="row">
              <div class="col-lg-6 col-md-8 ml-auto mr-auto">
              </div>
              <div class="col-lg-6 col-md-8 ml-auto mr-auto">
                <div class="card-stats justify-content-center">
                  <nuxt-link to="/projects/eLegacy">Vai</nuxt-link>
                </div>
              </div>
            </div>
          </template>
        </card>
      </div>
      <div class="col-lg-6 col-sm-6 text-center">
        <card type="contributions">
          <h1 class="card-title">2</h1>
          <h3 class="card-category">eMemory</h3>
          <p class="card-description">
            Lorem ipsum
          </p>
          <hr />

          <template slot="footer">
            <div class="row">
              <div class="col-lg-6 col-md-8 ml-auto mr-auto">
              </div>
              <div class="col-lg-6 col-md-8 ml-auto mr-auto">
                <div class="card-stats justify-content-center">
                  <nuxt-link to="/projects/eMemory">Vai</nuxt-link>
                </div>
              </div>
            </div>
          </template>
        </card>
      </div>
    </div>
  </div>
</template>