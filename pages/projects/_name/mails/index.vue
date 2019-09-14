<template>
  <div>
    <div class="row">
      <div class="col-lg-6 col-sm-6">
        <card type="timeline" class="card-plain">
          <time-line type="simple">
            <time-line-item
              inverted
              badge-type="danger"
              badge-icon="tim-icons icon-bag-16"
            >
              <span slot="header" class="badge badge-danger">Some title</span>
              <p slot="content">
                Wifey made the best Father's Day meal ever. So thankful so happy
                so blessed. Thank you for making my family We just had fun with
                the “future” theme !!! It was a fun night all together ... The
                always rude Kanye Show at 2am Sold Out Famous viewing @ Figueroa
                and 12th in downtown.
              </p>

              <h6 slot="footer">
                <i class="ti-time"></i> 11 hours ago via Twitter
              </h6>
            </time-line-item>

            <time-line-item
              inverted
              badge-type="success"
              badge-icon="tim-icons icon-gift-2"
            >
              <span slot="header" class="badge badge-success"
                >Another Title</span
              >
              <p slot="content">
                Thank God for the support of my wife and real friends. I also
                wanted to point out that it’s the first album to go number 1 off
                of streaming!!! I love you Ellen and also my number one design
                rule of anything I do from shoes to music to homes is that Kim
                has to like it....
              </p>
            </time-line-item>

            <time-line-item
              inverted
              badge-type="info"
              badge-icon="tim-icons icon-planet"
            >
              <span slot="header" class="badges badge-info">Another Title</span>

              <template slot="content">
                <p>
                  Called I Miss the Old Kanye That’s all it was Kanye And I love
                  you like Kanye loves Kanye Famous viewing @ Figueroa and 12th
                  in downtown LA 11:10PM
                </p>
                <p>
                  What if Kanye made a song about Kanye Royère doesn't make a
                  Polar bear bed but the Polar bear couch is my favorite piece
                  of furniture we own It wasn’t any Kanyes Set on his goals
                  Kanye
                </p>
                <hr />
              </template>

              <base-dropdown
                slot="footer"
                title-classes="btn btn-round btn-info"
              >
                <i slot="title" class="tim-icons icon-bullet-list-67"></i>

                <a class="dropdown-item" href="#">Action</a>
                <a class="dropdown-item" href="#">Another action</a>
                <a class="dropdown-item" href="#">Something else here</a>
              </base-dropdown>
            </time-line-item>
          </time-line>
        </card>
      </div>
    </div>
  </div>
</template>
<script>
import TaskList from '@/components/Dashboard/TaskList';
import {
  BaseSwitch,
  TimeLine,
  TimeLineItem,
  BaseCheckbox
} from '@/components';

export default {
  name: 'widgets-page',
  components: {
    BaseSwitch,
    TimeLine,
    TimeLineItem,
    TaskList,
    BaseCheckbox
  },
  data() {
    return {
      allContributions: true,
      pastWeekContributions: false
    };
  }
};
</script>
<style></style>
