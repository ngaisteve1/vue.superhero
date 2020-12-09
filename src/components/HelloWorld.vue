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
              <h2 class="team-name">{{ hero.biography["full-name"] }}</h2>
              <!-- <h3>{{ hero.work.occupation }}</h3> -->
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
                    class="progress-bar"
                    :style="{ width: `${hero.powerstats.strength}%` }"
                  ></div>
                </div>
                <div class="skill-name">
                  <p>speed</p>
                  <p>{{ hero.powerstats.speed }}%</p>
                </div>
                <div class="progress">
                  <div
                    class="progress-bar"
                    :style="{ width: `${hero.powerstats.speed}%` }"
                  ></div>
                </div>
                <div class="skill-name">
                  <p>durability</p>
                  <p>{{ hero.powerstats.durability }}%</p>
                </div>
                <div class="progress">
                  <div
                    class="progress-bar"
                    :style="{ width: `${hero.powerstats.durability}%` }"
                  ></div>
                </div>
                <div class="skill-name">
                  <p>power</p>
                  <p>{{ hero.powerstats.power }}%</p>
                </div>
                <div class="progress">
                  <div
                    class="progress-bar"
                    :style="{ width: `${hero.powerstats.power}%` }"
                  ></div>
                </div>
                <div class="skill-name">
                  <p>combat</p>
                  <p>{{ hero.powerstats.combat }}%</p>
                </div>
                <div class="progress">
                  <div
                    class="progress-bar"
                    :style="{ width: `${hero.powerstats.combat}%` }"
                  ></div>
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
          id: "149",
          name: "Captain America",
          powerstats: {
            intelligence: "69",
            strength: "19",
            speed: "38",
            durability: "55",
            power: "60",
            combat: "100"
          },
          biography: {
            "full-name": "Steve Rogers",
            "alter-egos": "No alter egos found.",
            aliases: ["Nomad", "The Captain"],
            "place-of-birth": "Manhattan, New York City, New York",
            "first-appearance": "Captain America Comics #1 (March 1941)",
            publisher: "Marvel Comics",
            alignment: "good"
          },
          appearance: {
            gender: "Male",
            race: "Human",
            height: ["6'2", "188 cm"],
            weight: ["240 lb", "108 kg"],
            "eye-color": "blue",
            "hair-color": "blond"
          },
          work: {
            occupation:
              "Adventurer, federal official, intelligence operative; former soldier, Hydra agent, liaison between S.H.I.E.L.D. and the Avengers, police officer, teacher, sparring partner.",
            base: "New York City"
          },
          connections: {
            "group-affiliation":
              "Secret Avengers (Black OPS Unit Formerly,The Avengers, Secret Avengers (Civil War), New Avengers, formerly The Invaders, Secret Defenders The Redeemers; formerly partner of Bucky, Golden Girl, Rick Jones, Falcon, Demolition-Man and Nomad (Jack Monroe)",
            relatives:
              "Joseph (father, deceased), Sara (mother, deceased), Ian Zola (Nomad) (adopted son)"
          },
          image: {
            url:
              "https://www.superherodb.com/pictures2/portraits/10/100/274.jpg"
          }
        },
        {
          response: "success",
          id: "659",
          name: "Thor",
          powerstats: {
            intelligence: "69",
            strength: "100",
            speed: "83",
            durability: "100",
            power: "100",
            combat: "100"
          },
          biography: {
            "full-name": "Thor Odinson",
            "alter-egos": "Rune King Thor",
            aliases: [
              "Donald Blake",
              "Sigurd Jarlson",
              "Jake Olsen",
              "Donar the Mighty"
            ],
            "place-of-birth": "Asgard",
            "first-appearance": "Journey into Mystery #83 (August, 1962)",
            publisher: "Rune King Thor",
            alignment: "good"
          },
          appearance: {
            gender: "Male",
            race: "Asgardian",
            height: ["6'6", "198 cm"],
            weight: ["640 lb", "288 kg"],
            "eye-color": "Blue",
            "hair-color": "Blond"
          },
          work: {
            occupation: "King of Asgard; formerly EMS Technician; Physician",
            base: "New York, New York"
          },
          connections: {
            "group-affiliation": "Avengers",
            relatives:
              "Odin (father), Gaea (mother), Frigga (step-mother), Loki (step-brother), Vidar (half-brother), Buri (paternal great-grandfather), Bolthorn (maternal great grandfather), Bor (grandfather), Bestla (grandmother), Vili (uncle), Ve (uncle), Sigyn (former sister-in-law), Hela (alleged niece), Jormungand (alleged nephew), Fernis Wolf (alleged nephew)"
          },
          image: {
            url:
              "https://www.superherodb.com/pictures2/portraits/10/100/140.jpg"
          }
        },
        {
          response: "success",
          id: "107",
          name: "Black Widow",
          powerstats: {
            intelligence: "75",
            strength: "13",
            speed: "33",
            durability: "30",
            power: "36",
            combat: "100"
          },
          biography: {
            "full-name": "Natasha Romanoff",
            "alter-egos": "No alter egos found.",
            aliases: [
              "Yelena Belova",
              "Natasha Romanoff",
              "Natasha",
              "Tasha",
              "Madame Natasha",
              "Nancy Rushman",
              "Laura Matthers",
              "Nadine Roman",
              '"Oktober"',
              "Black Pearl",
              "Ebon Flame"
            ],
            "place-of-birth": "-",
            "first-appearance": "Tales of Suspense #52",
            publisher: "Marvel Comics",
            alignment: "good"
          },
          appearance: {
            gender: "Female",
            race: "Human",
            height: ["5'7", "170 cm"],
            weight: ["131 lb", "59 kg"],
            "eye-color": "Green",
            "hair-color": "Auburn"
          },
          work: {
            occupation: "Adventurer, Intelligence agent, former ballerina",
            base: "Mobile"
          },
          connections: {
            "group-affiliation":
              'Secret Avengers; formerly Thunderbolts (as Yelena Belova), Nick Fury, Mighty Avengers, S.H.I.E.L.D., Avengers, Champions of Los Angeles, Lady Liberators, KGB, "Marvel Knights", partner of Daredevil, Hawkeye, Boris Turgenov, Logan',
            relatives:
              "Unnamed parents (presumed deceased); Alexi Shostakov (Red Guardian, estranged husband); Vindiktor (alleged brother, deceased)"
          },
          image: {
            url:
              "https://www.superherodb.com/pictures2/portraits/10/100/248.jpg"
          }
        },
        {
          response: "success",
          id: "106",
          name: "Black Panther",
          powerstats: {
            intelligence: "88",
            strength: "16",
            speed: "30",
            durability: "60",
            power: "41",
            combat: "100"
          },
          biography: {
            "full-name": "T'Challa",
            "alter-egos": "No alter egos found.",
            aliases: [
              "Mr. Okonkwo",
              "The Man Without Fear",
              "Luke Charles",
              "Black Leopard",
              "the Client",
              "Coal Tiger",
              "has impersonated Daredevil and others on occasion"
            ],
            "place-of-birth": "Wakanda, Africa",
            "first-appearance": "Fantastic Four Vol. 1 #52 (1966)",
            publisher: "Marvel Comics",
            alignment: "good"
          },
          appearance: {
            gender: "Male",
            race: "Human",
            height: ["6'0", "183 cm"],
            weight: ["200 lb", "90 kg"],
            "eye-color": "Brown",
            "hair-color": "Black"
          },
          work: {
            occupation:
              "King and Chieftain of Wakanda, scientist; former school teacher",
            base: "Wakanda, Mobile"
          },
          connections: {
            "group-affiliation":
              "Formerly Fantastic Four, Secret Avengers, Avengers, Pendragons, Queen's Vengeance, former Fantastic Force financier",
            relatives:
              "Bashenga (paternal ancestor, deceased), Azzuri the Wise (paternal grandfather, deceased), Nanali (paternal grandmother, deceased), Chanda (paternal grandfather, presumably deceased), T\ufffdChaka (father, deceased), S'Yan (uncle, deceased), N\ufffdYami (mother, deceased), Ramonda (stepmother), Hunter (adopted brother), Jakarra (half-brother), Shuri (sister), Ororo Munroe (wife), Joshua Itobo, Ishanta, Zuni, M'Koni, T'Shan (cousins), Wheeler (cousin by marriage, deceased), Billy Wheeler (1st cousin once removed)"
          },
          image: {
            url:
              "https://www.superherodb.com/pictures2/portraits/10/100/247.jpg"
          }
        },
        {
          response: "success",
          id: "226",
          name: "Doctor Strange",
          powerstats: {
            intelligence: "100",
            strength: "10",
            speed: "12",
            durability: "84",
            power: "100",
            combat: "60"
          },
          biography: {
            "full-name": "Stephen Strange",
            "alter-egos": "No alter egos found.",
            aliases: [
              "Sorcerer Supreme",
              "Master of the Mystic Arts",
              "Stephen Sanders",
              "Captain Universe",
              "Vincent Stevens"
            ],
            "place-of-birth": "Philadelphia, Pennsylvania",
            "first-appearance": "Strange Tales #110 (July, 1963)",
            publisher: "Marvel Comics",
            alignment: "good"
          },
          appearance: {
            gender: "Male",
            race: "Human",
            height: ["6'2", "188 cm"],
            weight: ["180 lb", "81 kg"],
            "eye-color": "Grey",
            "hair-color": "Black"
          },
          work: {
            occupation: "Sorcerer Supreme, retired neurosurgeon",
            base: "-"
          },
          connections: {
            "group-affiliation":
              "Defenders, underground Avengers; formerly the Order, Midnight Sons; former disciple of the Ancient One",
            relatives:
              "Eugene (father, deceased), Beverly (mother, deceased), Victor (Khiron, brother, apparently deceased), Donna (sister, deceased), Clea (wife, estranged), Umar (mother-in-law), Orini (father-in-law), Dormammu (uncle-in-law)"
          },
          image: {
            url: "https://www.superherodb.com/pictures2/portraits/10/100/55.jpg"
          }
        },
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
        },
        {
          response: "success",
          id: "313",
          name: "Hawkeye",
          powerstats: {
            intelligence: "56",
            strength: "12",
            speed: "21",
            durability: "10",
            power: "29",
            combat: "80"
          },
          biography: {
            "full-name": "Clint Barton",
            "alter-egos": "Goliath, Ronin",
            aliases: [
              "Ronin",
              "Goliath",
              "Golden Archer",
              "the Marksman",
              "Father Time",
              "Longbow"
            ],
            "place-of-birth": "Waverly, Iowa",
            "first-appearance": "Tales of Suspense #57 (September, 1964)",
            publisher: "Goliath",
            alignment: "good"
          },
          appearance: {
            gender: "Male",
            race: "Human",
            height: ["6'3", "191 cm"],
            weight: ["230 lb", "104 kg"],
            "eye-color": "Blue",
            "hair-color": "Blond"
          },
          work: { occupation: "Adventurer", base: "-" },
          connections: {
            "group-affiliation":
              "Avengers, Thunderbolts, Avengers West Coast, Great Lakes Avengers, Shadows, Chain Gang, former partner of the Black Widow",
            relatives:
              "Harold Barton (father, deceased), Edith Barton (mother, deceased), Bernard Barton (brother, deceased), Barbara Morse (wife, deceased)"
          },
          image: {
            url: "https://www.superherodb.com/pictures2/portraits/10/100/73.jpg"
          }
        },
        {
          response: "success",
          id: "697",
          name: "Vision",
          powerstats: {
            intelligence: "100",
            strength: "72",
            speed: "54",
            durability: "95",
            power: "100",
            combat: "70"
          },
          biography: {
            "full-name": "Vision",
            "alter-egos": "Anti-Vision, Vision II",
            aliases: ["Victor Shade"],
            "place-of-birth": "-",
            "first-appearance": "Avengers Vol.1 #57, Young Avengers # 4",
            publisher: "Anti-Vision",
            alignment: "good"
          },
          appearance: {
            gender: "Male",
            race: "Android",
            height: ["6'3", "191 cm"],
            weight: ["300 lb", "135 kg"],
            "eye-color": "Gold",
            "hair-color": "No Hair"
          },
          work: {
            occupation: "-",
            base:
              "Mobile. Formerly Avengers Mansion, New York City and Avengers Compound"
          },
          connections: {
            "group-affiliation":
              "Young Avengers, formerly; Avengers, West Coast Avengers, Defenders, Queen's Vengeance",
            relatives:
              'Wanda Maximoff (Scarlet Witch, ex-wife), Thomas Shepherd (Speed, son), William Kaplan (Wiccan, son), Ultron ("father"), Henry Pym (Ant-Man, "grandfather"), Pietro Maximoff (Quicksilver, ex-brother-in-law), Erik Magnus Lensher (Magneto, ex-father-in-law), Jocasta (fellow creation, "sister"), Simon Williams (Wonder Man, "brother"), Victor Mancha (fellow creation, half brother), Alkhema (fellow creation, "stepmother")'
          },
          image: {
            url:
              "https://www.superherodb.com/pictures2/portraits/10/100/532.jpg"
          }
        },
        {
          response: "success",
          id: "157",
          name: "Captain Marvel",
          powerstats: {
            intelligence: "84",
            strength: "88",
            speed: "71",
            durability: "95",
            power: "100",
            combat: "90"
          },
          biography: {
            "full-name": "Carol Danvers",
            "alter-egos": "Binary, Warbird",
            aliases: [
              "Ace",
              "Binary",
              "Lady Marvel",
              "Warbird",
              "others used during her espionage career"
            ],
            "place-of-birth": "Boston, Massachusetts",
            "first-appearance": "Ms. Marvel #1",
            publisher: "Binary",
            alignment: "good"
          },
          appearance: {
            gender: "Female",
            race: "Human-Kree",
            height: ["5'11", "180 cm"],
            weight: ["165 lb", "74 kg"],
            "eye-color": "Blue",
            "hair-color": "Blond"
          },
          work: {
            occupation:
              "Former National Aeronautics and Space Administration security Chief, former magazine editor, former freelance writer, former military intelligence officer.",
            base: "Avengers Mansion"
          },
          connections: {
            "group-affiliation":
              "currently Avengers, former companion to the X-Men (as Carol Danvers), former member of the Starjammers (as Binary), Former Avenger (as Ms. Marvel)",
            relatives:
              'Marie Danvers (mother), Joseph Danvers, Sr. (father), Joseph Danvers, Jr. (brother), Steve Danvers (brother, deceased), Marcus Immortus (Danvers) ("son", deceased)'
          },
          image: {
            url:
              "https://www.superherodb.com/pictures2/portraits/10/100/103.jpg"
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

@media all and (max-width: 499px) {
  #logo {
    display: none;
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
  justify-content: center;
}

.tiles {
  background-color: #dddddd;
  border: 1px solid black;
  //margin: 0 15px 30px 15px;
  margin: 0 15px 750px 15px;
  /* flex-grow: 1; */
  // flex: 0 0 220px;
  padding: 0;
  height: 100px;

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
  margin: 10px auto;
}

h1.title a {
  font-size: 22px;
}

/**********************************/
/************ Team CSS ************/
/**********************************/
.team {
  background-color: #dddddd;
  position: relative;
  margin: 0 auto;
  width: 100%;
  text-align: center;
  max-width: 300px;
  margin-bottom: 30px;
  box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2);
}

.team-name {
  min-height: 60px;
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
  min-height: 300px;
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
