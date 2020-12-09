<template>
  <div class="container">
    <div class="tiles" v-bind:key="hero.id" v-for="hero in heroes">
      <div class="menu row">
        <div
          class="menu-category list-group col-lg-3 col-md-4 col-sm-6 col-xs-12"
        >
          <h1 class="title">
            {{ hero.name }}
          </h1>
          <div class="team">
            <div class="team-img">
              <img :src="hero.image.url" alt="Team Image" />
              <div class="team-social">
                <a class="social-tw" href=""><i class="fab fa-twitter"></i></a>
                <a class="social-fb" href=""
                  ><i class="fab fa-facebook-f"></i
                ></a>
                <a class="social-li" href=""
                  ><i class="fab fa-linkedin-in"></i
                ></a>
                <a class="social-in" href=""
                  ><i class="fab fa-instagram"></i
                ></a>
                <a class="social-yt" href=""><i class="fab fa-youtube"></i></a>
              </div>
            </div>
            <div class="team-content">
              <h2>{{ hero.biography["full-name"] }}</h2>
              <h3>{{ hero.work.occupation }}</h3>
              <!-- <p>Some text goes here that describes about team member</p> -->
              <div class="team-skill">
                <div class="skill-name">
                  <p>intelligence</p>
                  <p>{{ hero.powerstats.intelligence }}%</p>
                </div>
                <div class="progress">
                  <div
                    class="progress-bar"
                    :style="{ width: `${hero.powerstats.intelligence}%` }"
                  ></div>
                </div>
                <div class="skill-name">
                  <p>strength</p>
                  <p>{{ hero.powerstats.strength }}%</p>
                </div>
                <div class="progress">
                  <div
                    :class="`progress-bar w-${hero.powerstats.strength}`"
                  ></div>
                </div>
                <div class="skill-name">
                  <p>speed</p>
                  <p>{{ hero.powerstats.speed }}%</p>
                </div>
                <div class="progress">
                  <div class="progress-bar w-80"></div>
                </div>
                <div class="skill-name">
                  <p>durability</p>
                  <p>{{ hero.powerstats.durability }}%</p>
                </div>
                <div class="progress">
                  <div class="progress-bar w-80"></div>
                </div>
                <div class="skill-name">
                  <p>power</p>
                  <p>{{ hero.powerstats.power }}%</p>
                </div>
                <div class="progress">
                  <div class="progress-bar w-80"></div>
                </div>
                <div class="skill-name">
                  <p>combat</p>
                  <p>{{ hero.powerstats.combat }}%</p>
                </div>
                <div class="progress">
                  <div class="progress-bar w-70"></div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
//import axios from "axios";

export default {
  data() {
    return {
      heroes: [
        {
          response: "success",
          id: "620",
          name: "Spider-Man",
          powerstats: {
            intelligence: "90",
            strength: "55",
            speed: "67",
            durability: "75",
            power: "74",
            combat: "85"
          },
          biography: {
            "full-name": "Peter Parker",
            "alter-egos": "No alter egos found.",
            aliases: [
              "Spiderman",
              "Bag-Man",
              "Black Marvel",
              "Captain Universe",
              "Dusk",
              "Green Hood",
              "Hornet",
              "Mad Dog 336",
              "Peter Palmer",
              "Prodigy",
              "Ricochet",
              "Scarlet Spider",
              "Spider-Boy",
              "Spider-Hulk",
              "Spider-Morphosis"
            ],
            "place-of-birth": "New York, New York",
            "first-appearance": "Amazing Fantasy #15",
            publisher: "Marvel Comics",
            alignment: "good"
          },
          appearance: {
            gender: "Male",
            race: "Human",
            height: ["5'10", "178 cm"],
            weight: ["165 lb", "74 kg"],
            "eye-color": "Hazel",
            "hair-color": "Brown"
          },
          work: {
            occupation: "Freelance photographer, teacher",
            base: "New York, New York"
          },
          connections: {
            "group-affiliation":
              "Member of the Avengers, formerly member of Outlaws, alternate Fantastic Four",
            relatives:
              "Richard Parker (father, deceased), Mary Parker(mother, deceased), Benjamin Parker (uncle, deceased), May Parker (aunt), Mary Jane Watson-Parker (wife), May Parker (daughter, allegedly deceased)"
          },
          image: {
            url:
              "https://www.superherodb.com/pictures2/portraits/10/100/133.jpg"
          }
        },
        {
          response: "success",
          id: "332",
          name: "Hulk",
          powerstats: {
            intelligence: "88",
            strength: "100",
            speed: "63",
            durability: "100",
            power: "98",
            combat: "85"
          },
          biography: {
            "full-name": "Bruce Banner",
            "alter-egos": "No alter egos found.",
            aliases: [
              "Annihilator",
              "Captain Universe",
              "Joe Fixit",
              "Mr. Fixit",
              "Mechano",
              "Professor",
              "Jade Jaws",
              "Golly Green Giant"
            ],
            "place-of-birth": "Dayton, Ohio",
            "first-appearance": "Incredible Hulk #1 (May, 1962)",
            publisher: "Marvel Comics",
            alignment: "good"
          },
          appearance: {
            gender: "Male",
            race: "Human / Radiation",
            height: ["8'0", "244 cm"],
            weight: ["1400 lb", "630 kg"],
            "eye-color": "Green",
            "hair-color": "Green"
          },
          work: {
            occupation: "Nuclear physicist, Agent of S.H.I.E.L.D.",
            base:
              "(Banner) Hulkbuster Base, New Mexico, (Hulk) mobile, but prefers New Mexico"
          },
          connections: {
            "group-affiliation":
              "Defenders, former leader of the new Hulkbusters, member of the Avengers, Pantheon, Titans Three, the Order, Hulkbusters of Counter-Earth-Franklin, alternate Fantastic Four",
            relatives:
              "Betty Ross Talbot Banner (wife), Brian Banner (father, apparently deceased), Rebecca Banner (mother, deceased), Morris Walters (uncle), Elaine Banner Walters (aunt, deceased), Jennifer Walters (She-Hulk, cousin), Thaddeus E. 'Thunderbolt' Ross (father"
          },
          image: {
            url: "https://www.superherodb.com/pictures2/portraits/10/100/83.jpg"
          }
        },
        {
          response: "success",
          id: "346",
          name: "Iron Man",
          powerstats: {
            intelligence: "100",
            strength: "85",
            speed: "58",
            durability: "85",
            power: "100",
            combat: "64"
          },
          biography: {
            "full-name": "Tony Stark",
            "alter-egos": "No alter egos found.",
            aliases: [
              "Iron Knight",
              "Hogan Potts",
              "Spare Parts Man",
              "Cobalt Man II",
              "Crimson Dynamo",
              "Ironman"
            ],
            "place-of-birth": "Long Island, New York",
            "first-appearance": "Tales of Suspence #39 (March, 1963)",
            publisher: "Marvel Comics",
            alignment: "good"
          },
          appearance: {
            gender: "Male",
            race: "Human",
            height: ["6'6", "198 cm"],
            weight: ["425 lb", "191 kg"],
            "eye-color": "Blue",
            "hair-color": "Black"
          },
          work: {
            occupation:
              "Inventor, Industrialist; former United States Secretary of Defense",
            base: "Seattle, Washington"
          },
          connections: {
            "group-affiliation":
              "Avengers, Illuminati, Stark Resilient; formerly S.H.I.E.L.D., leader of Stark Enterprises, the Pro-Registration Superhero Unit, New Avengers, Mighty Avengers, Hellfire Club, Force Works, Avengers West Coast, United States Department of Defense.",
            relatives:
              "Howard Anthony Stark (father, deceased), Maria Stark (mother, deceased), Morgan Stark (cousin), Isaac Stark (ancestor)"
          },
          image: {
            url: "https://www.superherodb.com/pictures2/portraits/10/100/85.jpg"
          }
        }
      ]
    };
  }
  // methods: {
  //   fetchData() {
  //     axios
  //       .get("https://superheroapi.com/api/10157801457699562/1")
  //       .then(response => (this.heroes = response.data))
  //       .catch(error => {
  //         console.log(error);
  //       });
  //   }
  // },
  // mounted() {
  //   this.fetchData();
  // }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
/* https://codepen.io/htmlcodex/pen/ZEbMbQr */
@media (min-width: 1200px) {
  .row > .col-lg-3:nth-child(4n + 1) {
    clear: left;
  }
}

@media (min-width: 992px) and (max-width: 1199px) {
  .row > .col-md-4:nth-child(3n + 1) {
    clear: left;
  }
}

@media (min-width: 768px) and (max-width: 991px) {
  .row > .col-sm-6:nth-child(2n + 1) {
    clear: left;
  }
}

/**********************************/
/********** Common CSS ************/
/**********************************/
*,
*::before,
*::after {
  box-sizing: border-box;
}

// .container {
//   position: relative;
//   width: 100%;
//   font-family: Arial, Helvetica, sans-serif;
//   display: flex;
//   flex-direction: row;
//   flex-wrap: wrap;
// }

.container > div.column {
  display: flex;
  flex-direction: column;
  flex-basis: 100%;
  flex: 1;
}

.container {
  // border: 1px solid red;
  display: flex;
  flex-wrap: wrap;
  margin: 0 auto;
  max-width: 2000px;
}

.tiles {
  border: 1px solid black;
  margin: 0 15px 30px 15px;
  /* flex-grow: 1; */
  flex: 0 0 220px;
  padding: 0;
  height: 220px;
  /* min-width: 220px; */
}

@media screen and (min-width: 800px) {
  .column {
    flex: 1;
  }

  .double-column {
    flex: 2;
  }
}

h1.title {
  position: relative;
  color: #353535;
  font-size: 25px;
  line-height: 35px;
  text-align: center;
  margin: 30px auto;
}

h1.title a {
  font-size: 22px;
}

/**********************************/
/************ Team CSS ************/
/**********************************/
.team {
  position: relative;
  margin: 0 auto;
  width: 100%;
  text-align: center;
  max-width: 300px;
  margin-bottom: 30px;
  box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2);
}

.team .team-img {
  position: relative;
  font-size: 0;
  color: #353535;
}

.team .team-img img {
  width: 100%;
  height: auto;
}

.team .team-social {
  position: absolute;
  width: 100%;
  height: 100%;
  padding: 20px;
  top: 0;
  left: 0;
  display: flex;
  align-items: center;
  justify-content: center;
  background: rgba(255, 255, 255, 0.5);
  transition: all 0.3s;
  font-size: 0;
  z-index: 1;
  opacity: 0;
}

.team:hover .team-social {
  opacity: 1;
}

.team .team-social a {
  display: inline-block;
  width: 40px;
  height: 40px;
  margin-right: 5px;
  padding: 11px 0 10px 0;
  font-size: 16px;
  font-weight: 300;
  line-height: 16px;
  text-align: center;
  color: #ffffff;
  transition: all 0.5s;
  margin-top: 100px;
}

.team .team-social a.social-tw {
  background: #00acee;
}

.team .team-social a.social-fb {
  background: #3b5998;
}

.team .team-social a.social-li {
  background: #0e76a8;
}

.team .team-social a.social-in {
  background: #3f729b;
}

.team .team-social a.social-yt {
  background: #c4302b;
}

.team .team-social a:last-child {
  margin-right: 0;
}

.team:hover .team-social a {
  margin-top: 0;
}

.team .team-social a:hover {
  color: #222222;
  background: #ffffff;
}

.team .team-content {
  padding: 20px;
  min-height: 400px;
}

.team .team-content h2 {
  margin: 0 0 5px 0;
  color: #353535;
  font-size: 25px;
  font-weight: 600;
  letter-spacing: 2px;
}

.team .team-content h3 {
  margin: 0 0 15px 0;
  color: #353535;
  font-size: 14px;
  font-weight: 300;
}

.team .team-content p {
  margin: 0 0 15px 0;
  color: #353535;
  font-size: 16px;
  font-weight: 400;
  line-height: 24px;
}

.team .team-skill {
  width: 100%;
}

.team .skill-name {
  text-align: left;
}

.team .skill-name p {
  display: inline-block;
  color: #353535;
  font-size: 14px;
  font-weight: 600;
  margin: 0;
}

.team .skill-name p:last-child {
  float: right;
}

.team .progress {
  position: relative;
  width: 100%;
  height: 5px;
  margin-bottom: 10px;
  background: #dddddd;
}

.team .progress:last-child {
  margin: 0;
}

.team .progress-bar {
  position: absolute;
  width: 0%;
  height: 5px;
  top: 0;
  left: 0;
  background: #454545;
  transition: all 0.7s;
  z-index: 1;
}

// @for $i from 0 through 100 {
//   .progress-bar.w-#{$i} {
//     width: $i%;
//   }
// }

.team:hover .progress-bar.w-70 {
  width: 70%;
}

.team:hover .progress-bar.w-80 {
  width: 80%;
}

.team:hover .progress-bar.w-90 {
  width: 90%;
}
</style>
