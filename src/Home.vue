<template>
  <div id="app">
    <video autoplay muted id="myVideo">
      <source src="./assets/video.mp4" type="video/mp4" id="video-file">
    </video>
    <div class="links">
      <a href="http://psmag.com" target="_blank"><img src="./assets/logo.png" class="logo" alt="Pacific Standard Magazine"></a>
      <a href="https://psmag.com/tag/march-2018" target="_blank"><img src="./assets/10th.png" alt="Our 10th Anniversary Issue" class="links__tenth"></a>
    </div>
    <div class="intro">
      <div class="intro__title">
        <p><img src="./assets/arrow.svg" class="arrow" id="arrow" alt="Welcome"></p>
        <h2>Dispatches from each of the 50 states plus the District of Columbia and the U.S. territories.</h2>
      </div>
      <div class="intro__content">
        <div class="intro__text">
          <p><strong>WITH OUR NATION</strong> at a turning point, and so much at stake for the economically and politically disenfranchised, and with grave threats posed to our climate and natural resources, and deeply ingrained patterns of racism and sexism beginning to be turned on their heads, the editors of Pacific Standard set out to document the state of our union.</p>

          <p>We contacted writers and public figures in each of the 50 states—plus the District of Columbia and the U.S. territories—and asked them to write about something that has captured the attention of their community in this time of great divisiveness and unrest.</p>

          <p>What kinds of openings has a polarized America presented, we wondered, and what are the different ways that people are stepping into them and reshaping what it means to be American? Are there glimmers of unity, or of unified purpose? What is the shape of the resistance, and where is it getting some traction in restoring justice and fairness to our institutions and our democracy? The result is a state-by-state accounting of some of the best and worst things happening in our country at this moment in time.</p>

          <p><img src="./assets/sign.png" alt="" /></p>

          <blockquote>“What kinds of openings has a polarized America presented? Are there glimmers of unity, or of unified purpose?”</blockquote>
        </div>
        <div class="intro__text">
          <p><img src="./assets/state.png" alt="" /></p>

          <blockquote>“The new American narrative isn’t one single story. It is a multitude of stories playing out in diverse and far-flung places.”</blockquote>

          <p>In the dispatches that follow, you will read about local issues, and about national issues as seen through the lens of different locales. There are communities divided, and communities coming together to right a wrong. There are stories of wonder, and stories of hardship; stories not just from the big coastal cities but from all over, even the small, out-of-the-way places that tend to get ignored.</p>

          <p>The new American narrative isn’t one single story. It is a multitude of stories playing out in diverse and far-flung places. Here are 52 of them. Together, they provide a mosaic view of our country and our moment. We hope you enjoy them. And perhaps, in here somewhere, you’ll  nd a sense of who we are as a country, and what truly makes us great.</p>
        </div>
      </div>
    </div>
    <State :info="states.alabama" layout="text-left" />
    <State :info="states.alaska" layout="text-right" />
    <State :info="states.arizona" layout="text-left" />
    <State :info="states.arkansas" layout="text-right" />
    <State :info="states.california" layout="text-left" />
    <State :info="states.colorado" layout="text-right" />
    <State :info="states.connecticut" layout="text-left" />
    <State :info="states.delaware" layout="text-right" />
    <State :info="states.florida" layout="text-left" />
    <State :info="states.georgia" layout="text-right" />
    <State :info="states.hawaii" layout="text-left" />
    <State :info="states.idaho" layout="text-right" />
    <State :info="states.illinois" layout="text-left" />
    <State :info="states.indiana" layout="text-right" />
    <State :info="states.iowa" layout="text-left" />
    <State :info="states.kansas" layout="text-right" />
    <State :info="states.kentucky" layout="text-left" />
    <State :info="states.louisiana" layout="text-right" />
    <State :info="states.maine" layout="text-left" />
    <State :info="states.maryland" layout="text-right" />
    <State :info="states.massachusetts" layout="text-left" />
    <State :info="states.michigan" layout="text-right" />
    <State :info="states.minnesota" layout="text-left" />
    <State :info="states.mississippi" layout="text-right" />
    <State :info="states.missouri" layout="text-left" />
    <State :info="states.montana" layout="text-right" />
    <State :info="states.nebraska" layout="text-left" />
    <State :info="states.nevada" layout="text-right" />
    <State :info="states.newHampshire" layout="text-left" />
    <State :info="states.newJersey" layout="text-right" />
    <State :info="states.newMexico" layout="text-left" />
    <State :info="states.newYork" layout="text-right" />
    <State :info="states.northCarolina" layout="text-left" />
    <State :info="states.northDakota" layout="text-right" />
    <State :info="states.ohio" layout="text-left" />
    <State :info="states.oklahoma" layout="text-right" />
    <State :info="states.oregon" layout="text-left" />
    <State :info="states.pennsylvania" layout="text-right" />
    <State :info="states.rhodeIsland" layout="text-left" />
    <State :info="states.southCarolina" layout="text-right" />
    <State :info="states.southDakota" layout="text-left" />
    <State :info="states.tennessee" layout="text-right" />
    <State :info="states.texas" layout="text-left" />
    <State :info="states.utah" layout="text-right" />
    <State :info="states.vermont" layout="text-left" />
    <State :info="states.virginia" layout="text-right" />
    <State :info="states.washington" layout="text-left" />
    <State :info="states.westVirginia" layout="text-right" />
    <State :info="states.wisconsin" layout="text-left" />
    <State :info="states.wyoming" layout="text-right" />
    <State :info="states.districtOfColumbia" layout="text-left" />
    <State :info="states.colonies" layout="text-right" />
    <div class="footer">
      <div class="footer__image">
        <img src="./assets/rv.png" id="rv" alt="an RV" class="rv" />
      </div>
      <div class="footer__content">
        <nav class="footer__nav">
          <a href="https://psmag.com/page/about" target="_blank">WHO WE ARE</a>
          <a href="https://psmag.com/page/subscribe" target="_blank">SUBSCRIBE TO OUR MAGAZINE</a>
          <a href="https://psmag.com/page/newsletter" target="_blank">SIGN UP FOR OUR NEWSLETTER</a>
        </nav>
        <p class="footer__credit">Thanks to Elias Stein and Diana Lopez for design.</p>
        <p class="footer__copyright">© 2018 The Social Justice Foundation</p>
      </div>
    </div>
  </div>
</template>

<script>
import State from '@/components/State'
import Rellax from 'rellax'
import * as basicScroll from 'basicscroll'

export default {
  name: 'App',
  components: {
    State
  },
  mounted() {
    const instance = basicScroll.create({
       elem: document.querySelector('.rv'),
       from: 'top-top',
       to: 'bottom-middle',
       props: {
          '--tx': {
             from: 0,
             to: -window.innerWidth + 'px',
             direct: true
          }
       }
    })
    instance.start();

    document.getElementById('myVideo').addEventListener('ended',this.myHandler,false);

    let el = document.getElementById('arrow');
    window.addEventListener('scroll', function() {
      if (this.isInViewport(el) && !el.classList.contains('rotate')) {
        if (el.classList)
          el.classList.add('rotate');
        else
          el.className += ' ' + 'rotate';
       }
    }.bind(this));
  },
  methods: {
    isInViewport: function(element) {
      var rect = element.getBoundingClientRect();
      var html = document.documentElement;
      return (
        rect.top >= 0 &&
        rect.left >= 0 &&
        rect.bottom <= (window.innerHeight || html.clientHeight) &&
        rect.right <= (window.innerWidth || html.clientWidth)
      );
    },
    myHandler: function(e) {
      var el = document.getElementById('myVideo');
      let videoHeight = el.offsetHeight
        if (window.pageYOffset < videoHeight) {
          window.scroll({top: videoHeight, left: 0, behavior: 'smooth'})
        }
    }
  },
  data () {
    return {
      states: {
        alabama: {
          key: 'alabama',
          number: 1,
          name: 'Alabama',
          author: 'Matthew Teague',
          bio: 'Matthew Teague is Souther Correspondent for The Guardian',
          text: `It’s not often, here in Alabama, that we lead the way in a cultural movement.
          Unfortunately, the state has seized the lead over the past couple of years in a nationwide effort to collapse the separation of church and state. The most visible embodiment of that is Judge Roy Moore, who this past fall was both angling for a United States Senate seat and accused of sexually assaulting teenagers.
          Just before the 2016 presidential election, an interim pastor visited my Baptist church in Fairhope. His sermon was a bizarre story about how he would never marry Chelsea Clinton because of her mother. If you wouldn’t have Hillary Clinton as your mother-in-law, he said, why would you have her as your president? The congregation applauded.
          I walked out during the service and waited for the pastor outside.
          “You’re tearing apart the church,” I told him.
          He grinned. “I don’t think so,” he said.
          And I realized, as people poured past, slapping his shoulders, that he was right. And soon evangelical voters, as a bloc, elected Trump.
          The win, I realized, justified the sin.
          Nothing could be further from Christian belief. Or further, even, from mere Baptist principles: In 1802, new President Thomas Jefferson <a target="_blank" href="https://www.loc.gov/loc/lcib/9806/danpre.html" target="_blank">wrote to a Baptist church</a> in Connecticut to confirm “a wall of separation between Church & State.”
          It was a novel phrase and appears nowhere in the Constitution itself, but it formed a central tenet for Baptists.
          That idea is being dismantled now, traded away for momentary political influence. It’s a technique pioneered during the dark days of Jim Crow and revived in Alabama by Moore and those who will surely follow in his wake. When he made a campaign appearance outside Mobile last fall to deny charges that he molested, to varying degrees, a growing list of women—one as young as 14—he did it standing in Magnolia Springs Baptist Church.
          “It’s a sign of our times,” he said.
          It was the closest he came, that day, to gospel truth.`
        },
        alaska: {
          key: 'alaska',
          number: 2,
          name: 'Alaska',
          author: 'Colleen E. Swan',
          bio: 'Colleen E. Swan is an Alaska Native BORN AND RAISED IN KIVALINA.',
          text: `Here in Kivalina, a small village about a hundred miles above the Arctic Circle, the facts of the disrupted climate are quickly becoming harder to bear. In 50 years’ time, a good portion of the coast of Alaska will be underwater, according to University of Alaska–Fairbanks professor Vladimir Romanovsky. That projection is conservative. The pace of environmental change is accelerating at an alarming rate. The changes that the indigenous people of Kivalina have witnessed have gone from gradual to extreme.
Although our people are adaptable, adjusting to the changing climate has proven to be difficult from year to year. We have come to the point where we need modern Western weather monitoring and reporting more than we have ever needed it in the past. Our people, especially the hunters, observe weather patterns in order to plan their days. But the weather has become too unpredictable. Skills that had been honed by thousands of years of observation and oral legend are no longer enough. It is a difficult thing to accept, when you know that decisions continue to be made by people in positions of authority that will lead to more non-renewable resource extraction and be even more detrimental to wildlife and human habitat. Here in Kivalina, we are preparing for more climate-induced encroachment of seawater onto the land.`
        },
        arizona: {
          key: 'arizona',
          number: 3,
          name: 'Arizona',
          author: 'Alberto Ríos',
          bio: 'Alberto Ríos is the Poet Laureate of Arizona and the director of Arizona State University’s Virginia G. Piper Center for Creative Writing.',
          text: `There are two Nogaleses—one American, one Mexican. Or, rather, there’s one Nogales, cut in half by a fence. I grew up on the Arizona side, but the border was different then. On festival days, the gates were thrown open. The Cinco de Mayo parade would begin in Mexico and move onto Morley Avenue on the American side. There were bands and floats, the men and women who had fought in World War II, their VFW and American Legion caps, the precision of the drums and bugles echoing in the small canyon of storefronts, the poppies people wore. It was a moment of shared struggle, of two towns so clearly drawn together in the midst of a very large world.
That Nogales bears almost no resemblance to Nogales now.
The last time I was at the border, I went with a friend, a little late in the day, with dusk starting its cricket entrance. We had not brought passports—a disagreeable new requirement for just crossing over, even for the afternoon. So we walked through the old downtown, talking about the old stores and the old life, and inevitably about the wall that scars the hilly landscape. We walked up a trail on Grand Avenue that allows a view of the other side and saw some young boys in Sonora standing around talking in the early evening sun.
Just after dusk had begun to turn dark, banks of floodlights, the kind one might see at a construction site, quite suddenly and dramatically came to life on the American side. The boys whooped their hands up in the air, and we saw then that they had a basketball. What we couldn’t see from our vista was that they had attached a hoop to the Mexico side of the wall and could now start their game. We laughed and watched them for a while. I was happy to find again that border town—and border life—I remember and love. It is so hard to find now.`
        },
        arkansas: {
          key: 'arkansas',
          number: 4,
          name: 'Arkansas',
          author: 'Jeff Winkler',
          bio: 'Jeff Winkler is a Southerner and college dropout. His work has appeared in Texas Monthly, Oxford American, Vice, and elsewhere.',
          text: `A few years back, my old man started a newspaper in a small Arkansas town, population 2,500. He’d never been a journalist and quickly made enemies. Not infrequently, townsfolk would tell him: “Half the town hates you!” Pops would respond with glee: “Well, what about that other half?”
Pops wanted to smash the town’s good ol’ boy cabal, to open up the local government to an informed and involved citizenry. The town’s municipal functionaries are all related to each other; the local government organizational tree looks more like a stump. At one meeting, a councilman took a swing at Pops for asking questions, and also possibly for Pops’ having reported that the councilman had dragged his stepson through the street by his hair.
The newspaper eventually went under. The citizens loved gossip, but news was too much. News meant accountability, for both townsfolk and town leaders. At coffee klatches, they whisper: It’d sure be nice to have some new businesses in town—so long as I don’t have to get involved. Pops got involved, stayed involved. But now he’s talking about quitting civic life.
The good ol’ boy system is entrenched. Those who agree with change say so quietly. Or, worse, they redirect their frustration to national debates. Same thing happens in the bigger university city down the road: People are eager to make grandiose denouncements of national figures, march in colorful Saturday protests, or join social media crusades. Pops doesn’t see those virtual citizens on city council nights. It’s the good ol’ boys who show up then. And so it’s the good ol’ boys who run politics all the way up to the state level. And Pops keeps asking: “What about that other half?”`
        },
        california: {
          key: 'california',
          number: 5,
          name: 'California',
          author: 'Susan Straight',
          bio: 'Susan Straight has published eight novels and hundredS of essays.',
          text: `There may be no place in the nation where two Americas are more starkly apparent than in the Coachella Valley, where an ancient lake bed is now a grid of north-south streets named for dozens of former presidents and vice presidents. In the town of Thermal, between Tyler and Polk streets and 61st and 62nd avenues, an eight-foot wall surrounds 344 acres of land that the ancestors of the Torres Martinez tribe would have used; land which, according to Saul, a young security guard, was blessed with chants, songs, and burnt sage to appease the spirits before miles of golden-tinted concrete blocks molded to resemble old adobe bricks went up. The Thermal Club is a racetrack for members, who might live in Rancho Mirage or in Europe. To become a member and acquire a “home site” can cost nearly $1 million, with most members spending millions more to build their houses.
Working for minimum wage on a temporary basis, Saul, born in Mexicali and brought here when he was nine, said pensively: “To get my citizenship, it would be cheaper if I got married. But my girlfriend’s mom, she has no papers.” His girlfriend has a green card; her mother was born in Colima, Mexico. He sighs. “I finished the college courses for law enforcement, but I can’t get hired with a green card.” The Thermal Club is surrounded by carrot fields, date orchards, mesquite and smoke trees, and a cemetery in the distance. We are 6.8 miles on a straight line from the ancient Fish Traps site in the Santa Rosa range: many rows of rock pits, <a target="_blank" href="https://npgallery.nps.gov/NRHP/AssetDetail?assetID=815ed0e0-68cd-4a95-96fb-276a6d81d025">constructed more than 500 years ago</a>, where Cahuilla peoples caught fish for sustenance.`
        },
        colorado: {
          key: 'colorado',
          number: 6,
          name: 'Colorado',
          author: 'Camille T. Dungy',
          bio: 'Camille T. Dungy is the author of Guidebook to Relative Strangers: Journeys Into Race, Motherhood, and History.',
          text: `Since I’ve come back to Colorado, I’ve watched the removal of three prairie-dog towns. Some call them steppe squirrels, but what we call them won’t matter if they’re not around to name. We bought an old house because I don’t want to encroach on the landscape I’ve come to love. I’ve caught myself giving the side-eye to people who live in new-build communities, as if I were grandfathered into this ecosystem and the blood of the steppe squirrels is on these newcomers’ hands alone.
I drive alternate routes to avoid confronting new developments. But many are impossible to avoid. When I visited in the ’80s and ’90s, I’d take I-25 from the airport. Then, it seemed the only things between me and the Rockies were open fields. After I resumed permanent residence, I started seeing tan tanks on these agricultural expanses. I told myself they were holding tanks for water until, driving with a friend who was working on a book about seismicity, I learned they were parts of fracking installations. Now, what I see: wells, pump jacks, drill rigs, SandCastles, flare pipes, the hay walls intended to hide whatever machinations allow us to get at shale buried millennia deep.
In an environmental literature class I taught at the state university, more than half the students were intimately connected with the fracking industry. <a target="_blank" href="https://www.bloomberg.com/news/articles/2017-10-03/these-suburbanites-may-have-no-fracking-choice">That money</a> makes things happen in Colorado as much as the tourism, housing, and business developments encouraged by our state’s new and newly affluent residents. This part of Colorado seems to be half scenic byway, half mining town. On the road to Breckenridge and A-Basin, I pass more resource extraction towns than I can name. And what is it to ski than to extract from the mountain the materials needed for my own pleasure? Silver, gold, uranium, natural gas, the feed lots and slaughter houses of Greeley, and the land on which so many of us try to build some kind of life. It’s beautiful here, but there’s a price tag on everything.`
        },
        connecticut: {
          key: 'connecticut',
          number: 7,
          name: 'Connecticut',
          author: 'Hanif Abdurraqib',
          bio: 'Hanif Abdurraqib’s latest book is They Can’t Kill Us Until They Kill Us.',
          text: `A couple of years back, just blocks from my New Haven apartment, <a target="_blank" href="https://yaledailynews.com/blog/2015/11/05/students-confront-christakis-about-halloween-email/">tensions boiled over at Yale</a> University, following a lecturer’s open letter that seemed to defend racially insensitive Halloween costumes. The ensuing protests were a continuation of earlier demonstrations against the school’s historical ties to slavery and its mistreatment of black cafeteria workers. That fall, I stood on the outskirts of Yale while young people of color chanted into megaphones, eventually leading a march of hundreds—all ages and races—throughout the streets of New Haven. The demonstration ended with an impromptu dance party to Kendrick Lamar’s “Alright.”
It was the start of two years of action in Connecticut, a period that was pivotal in changing my idea of what protest could be. These students protested racial injustice and demanded that Yale rename Calhoun College, named after John C. Calhoun, the country’s seventh vice president and a passionate white supremacist who argued fiercely that slavery was a <a target="_blank" href="https://www.stolaf.edu/people/fitz/COURSES/calhoun.html">“positive good.”</a> Protesters wrote letters and op-eds and gathered outside of administration buildings, chanting, dancing, and singing. In February of 2017, Yale President Peter Salovey announced that Calhoun College would be <a target="_blank" href="https://news.yale.edu/2017/02/11/yale-change-calhoun-college-s-name-honor-grace-murray-hopper-0">renamed after Grace Murray Hopper</a>, a Yale graduate and World War II veteran who pioneered computer programming languages.
Seeing young people hold each other up through the rigor of march and protest and seeing the lasting impact of their efforts challenged all the models of protest that I’d been growing weary of, where men, usually older, were in the front, leading chants, directions, and demands. The recent protests in Connecticut were carried out by young people, for the liberation of young people, and they belied the notion that the younger generation is lazy, or unwilling to make sacrifices in the name of justice.`
        },
        delaware: {
          key: 'delaware',
          number: 8,
          name: 'Delaware',
          author: 'Dave Weigel',
          bio: 'Dave Weigel is a political reporter for the Washington Post.',
          text: `Delaware began last year doing something that surprised even this Delaware-born political reporter: It kicked off the Democratic resistance.
The Delaware I grew up in was a microcosm—emphasis on the “micro”—of the U.S. Republicans and Democrats split control, trading elections back and forth, like a four-year game of catch. Liberal and suburbanized New Castle County, with around two-thirds of our population, generally decided elections; liberal-leaning Republicans, like the much-missed Mike Castle, won my hometown easily. Your party label was less important than your fealty to DuPont and the state’s banking industry.
Starting in 2000, as Republicans moved right, Delaware staggered to the left. By 2010, Mike Castle <a target="_blank" href="http://www.washingtonpost.com/wp-dyn/content/article/2010/09/14/AR2010091407063.html">lost the GOP senate primary</a> to Christine “I Am Not a Witch” O’Donnell, in an election that effectively snuffed out moderate Republicans.
Still, I was amazed last year when a little stretch of suburbia, the 10th state senate district, opened up and became the most important race in America. At some point in January, national Democrats realized that, if they lost the seat, they’d lose one of their last <a target="_blank" href="https://ballotpedia.org/State_government_trifectas_and_triplexes">six “trifecta” governments</a>. Stephanie Hansen, the Democrat, suddenly found herself with <a target="_blank" href="http://www.delawareonline.com/story/news/politics/2017/03/08/outside-money-delaware/98897874/">nearly $1 million in donations</a> and super PAC money, a ridiculous sum in Delaware or anywhere else. Joe Biden cut short his political exile to <a target="_blank" href="http://www.delawareonline.com/story/news/politics/2017/02/25/senate-district-10-race-draws-crowd-complaints/98375166/">shake hands in strip-mall parking lots</a>.
It worked: Hansen won. My little state, like Massachusetts in 2010, proved that the opponents of a powerful president would knock on doors until their knuckles bled if it meant winning back power. The political story of the next few years might be how Republicans melt away in the suburbs, cleaving American voters into supporters of the white rural party and the diverse urban/suburban party. And it started along the highways where I used to shop tax-free.`
        },
        florida: {
          key: 'florida',
          number: 9,
          name: 'Florida',
          author: 'Erin Belieu',
          bio: 'Erin Belieu is a professor of creative writing at Florida State University and the author of four collections of poetry, most recently Slant Six.',
          text: `Seen from the outside, Florida makes a credible bid to be considered America’s most preposterous state: land of your more colorful variety of PWSAL (People Who Suck at Life), whose dingle-headed exploits fill multiple Twitter accounts. Still paradisiacal in many spots, lush with sugar-sand beaches, sprinkled liberally with pretty, young co-eds in bikini tops and Daisy Dukes, Florida is the repository for our nation’s most libertine fantasies.
But that’s the tourist perspective. Our state’s tug-of-war between blue and red values speaks to the strong streak of patriarchal conservatism found here, from North Florida’s Foghorn Leghorn style of masculinity down to the Speedo-clad machismo of Miami. And for folks who like to party as hard as Floridians do, outside of its relatively large Jewish population, Florida’s citizens can seem a strangely churchy bunch, with <a target="_blank" href="http://www.pewforum.org/religious-landscape-study/state/florida/">large numbers of evangelical and Catholic</a> worshipers who attend services weekly.
Florida’s retrograde treatment of its female citizens is also notable, and likely arises from many rural and suburban white voters’ idea of “traditional family values.” As recent studies demonstrate, Florida <a target="_blank" href="https://nwlc.org/wp-content/uploads/2017/09/Wage-Gap-State-By-State-2017.pdf">isn’t a great place for women</a> of any color; they make $0.87 for every dollar that men do, and the state lands in the bottom half when ranking states by economic opportunity and leadership roles available to women. And yet Hillary Clinton lost Florida’s white women voters, a big chunk of them choosing a self-described pussy grabber and dog-whistling racist rather than a wildly qualified feminist woman as their president.
As long as so many white women voters in this key swing state identify awith their race privilege first and continue to support the structures of white patriarchal power, Florida will struggle with its purpleness. But in this moment, when toxic masculinity is increasingly revealed for all its ugliness, and as white women wake up to the fact that the game has always been rigged against them, too, I have hope Florida will grow bluer and bluer in the years ahead.`
        },
        georgia: {
          key: 'georgia',
          number: 10,
          name: 'Georgia',
          author: 'Amanda Mull',
          bio: 'Amanda Mull is a journalist, essayist, and cultural critic currently living in Brooklyn. She’s a native Georgian, as well as an alumna of the University of Georgia.',
          text: `Usually, people outside the South think about Georgia without realizing it, through food or music or a movie filmed in an Atlanta that’s either a leafy American suburb or dystopian hellscape. The state is woven deeply into American culture in ways that tend to go unacknowledged; when something from Georgia becomes sufficiently popular, the context of its source gets erased. You get used to being ignored.
When the political eyes of America turned to a congressional election in suburban Atlanta in early 2017, though, Georgians suddenly found everyone looking at us. Hillary Clinton’s 2016 margin of defeat in Georgia was slimmer than in Ohio, one of the top three states where Clinton spent the most money (Georgia was not one of them). Between the introduction of Jon Ossoff, the Democrats’ photogenic candidate for the sixth district election, and the race’s runoff, national journalists examined Georgia as though they had just been alerted to our existence. They posited Georgia could be a bellwether, that a win might point a path forward for reeling progressives. <a target="_blank" href="https://www.nytimes.com/2017/06/19/upshot/this-list-of-well-educated-districts-explains-why-georgias-election-is-close.html?_r=0">The New York Times, condescendingly, explained</a> Trump’s unpopularity in the traditionally Republican district by noting that it was among the most well-educated districts in the nation.
Ossoff lost, of course. He was picked by a party whose contempt for Southerners, among other things, long ago ceded the South to Republicans, and the money that poured in couldn’t buy enough yard signs to transmogrify a white, white-collar district into a microcosm of a hopeful future. Expecting Georgia to save us all was foolish; most Americans don’t even know who Georgia is. But they’d know if they listened, because, from Carson McCullers to André 3000, Georgians have been trying to tell the country who we are for ages.`
        },
        hawaii: {
          key: 'hawaii',
          number: 11,
          name: 'Hawaii',
          author: 'Dana Naone Hall',
          bio: 'Dana Naone Hall is the author of Life of the Land: Articulations of a Native Writer, a recently published volume of poetry, testimonies, letters, talks, and essays.',
          text: `For Hawaiian people, certain landscapes have the power to anchor us physically, psychically, spiritually, and culturally. We depend upon these places to identify not only where we are, but who we are. This is why we search for a view of Le‘ahi (Diamond Head) on the crowded streets of Waikīkī. Even a glimpse of a familiar landform is reassuring.
Because of this unbroken connection between ‘āina (land) and Native Hawaiians, opposition to the construction of two huge astronomy telescopes near the summits of Haleakalā and Mauna Kea, the tallest mountains on Maui and Hawai‘i respectively at 10,000 and almost 14,000 feet, is especially fierce.
The 18-story-tall <a target="_blank" href="https://dlnr.hawaii.gov/mk/files/2017/09/882-BLNR-FOFCOLDO.pdf">Thirty Meter Telescope project</a> approved for Mauna Kea is a resonant example of the ongoing clash between out-of-state development interests, bolstered by the glittering promise of scientific advances, and the desire of many Hawaiians and their supporters to prevent further damage to the mountain already blighted by 13 smaller telescopes.
Project proponents argue that ancient Hawaiians studied the heavens and that the new telescope would be a continuation of these observations. Mauna (mountain) protectors reject this facile proposition and point to the circumnavigation of the globe recently accomplished by the double-hulled Polynesian voyaging canoe, Hōkūle‘a, relying only on traditional navigation methods—a distance of over 47,000 nautical miles.
The mana (power) of the ‘ike kupuna (ancestral knowledge) is imbued in the land. Another winter season arrives, and the mountain protectors are present in ever greater numbers to witness, once again, the summit wrapped in the blazing white shawl of the snow goddess, Poli‘ahu.`
        },
        idaho: {
          key: 'idaho',
          number: 12,
          name: 'Idaho',
          author: 'Anne Helen Petersen',
          bio: 'Anne Helen Petersen covers culture and the West for BuzzFeed News.',
          text: `Idaho has never been a place people look to for national trends. I remember friends watching Napoleon Dynamite—a movie set in the south of the state—and thinking it was set in the 1980s. Nope: Ideas just come here 10 years late. But these days, few places elucidate the forces tearing the GOP apart quite as well as big ol’ Idaho.
For much of the 20th century, Idaho, like the rest of the Mountain West, was politically “purple”—a mix of conservatives and “lunch box” Democrats, most associated with the unions that dominated the timber and mining industries. That began to change in the 1990s, in part because those union jobs went away, but also because <a target="_blank" href="http://www.idahostatesman.com/news/local/article164420672.html">conservative Californians began to move to North Idaho en masse</a>, seeking an old-fashioned way of life far from the “strife” of a California they no longer recognized as their own. Today, Idaho is one of the reddest states in the nation—and without Democratic opposition, these Californian conservatives, far to the right of most native Idahoans, have taken over the GOP from the ground up, practicing an exacting sort of tribalism in which anyone who doesn’t toe the far-right line is labeled a liberal, a RINO (Republican in Name Only), or worse. Americans are increasingly migrating to places—on the coasts, in places like Idaho—where they can be surrounded with those who share their politics. But in the county commissioner meetings, in the school board races, in the letters to the editor, and on Facebook, the result isn’t political harmony; it’s civil war.`
        },
        illinois: {
          key: 'illinois',
          number: 13,
          name: 'Illinois',
          author: 'Luis Alberto Urrea',
          bio: 'Luis Alberto Urrea is the author of The House of Broken Angels and 16 other books.',
          text: `Well, I miss mountains. But that’s what the skyscrapers of Chicago will do to you—artificial Alps beside the inland sea of Lake Michigan. There may have been hills before the ice sheets ironed us into prairies as they carved out the lake bed. Illinois is a place where the past and the present wrestle with the future. It’s tumult and evolution wrestling with stasis and devolution. Where hot dogs come with a small garden piled on them (no ketchup), and where traffic jams appear at 11 p.m. on a Sunday. When I moved here 18 years ago, a local translated Illinois for me: “It makes you ill and is annoying.” Unfair! Except for our politics. Our politics could make you puke up your hot dog. The whole history of this great city and its land is written and rewritten so fast that I feel I have seen at least 10 versions of Chicago since I’ve lived here. All the while, the magic of the prairie makes one believe that a verity, a wholeness, reigns unchanging. In 2017, <a target="_blank" href="http://www.chicagotribune.com/news/data/ct-shooting-victims-map-charts-htmlstory.html">3,563 shootings in Chicago</a> alone, while five miles from that general blast zone, art and theater and ballet and opera flourish in a fantastic movie set of a city laid out on Indian trails and the rubble of the Great Fire. Foreign invaders have changed things some: The zebra mussels have cleaned the murky waters of the lake. It’s glassy now. Abraham Lincoln’s ghost could see his toes.`
        },
        indiana: {
          key: 'indiana',
          number: 14,
          name: 'Indiana',
          author: 'Terese Marie Mailhot',
          bio: 'Terese Marie Mailhot is the author of Heart Berries: A Memoir from Counterpoint Press, works at the Institute of American Indian Arts as creative writing faculty, and is a Tecumseh Postdoctoral Fellow at Purdue University. ',
          text: `Indiana means the “Land of the Indians,” but the <a target="_blank" href="https://www.census.gov/quickfacts/IN">latest census estimates</a> the Native population at 0.4 percent. The only Indian in the school gym besides my sons and myself is a mascot on the wall in a headdress. My son attends Battle Ground Middle School: the Tomahawks. His school’s namesake refers to the Battle of Tippecanoe, in which U.S. forces slaughtered the Shawnee. The high school he will eventually attend, William Henry Harrison High School, is named after America’s ninth president and the architect of the slaughter. Indians are always living in a post-apocalyptic world.
The gym is filling with parents who have come to listen to the band concert, and I’m only slightly envious of the white women in Patagonia coats. Patagonia has just declared <a target="_blank" href="http://www.patagonia.com/protect-public-lands.html">“The President Stole Your Land,”</a> and I’m waiting for the first of the month to get myself a coat. Being the only Indian in the land of the Indians feels like being trapped in a carnival of cruel ironies and monuments and diversity initiatives. Our subdivision in West Lafayette is called Colony Pines. “We’re taking our land back, one duplex at a time,” I joke to my husband.
Above the bleachers, there are banners with team names like Trojans and Indians and the resident Tomahawks. When my little Indian boy gets up and blows his trombone next to his peers, I try to imagine that the Indians won the Battle of Tippecanoe. We wouldn’t make mascots out of white people; we’d just be less forgotten. `
        },
        iowa: {
          key: 'iowa',
          number: 15,
          name: 'Iowa',
          author: 'Dean Bakopoulos',
          bio: 'Dean Bakopoulos is an assistant professor at Grinnell College in Iowa.',
          text: `Grinnell College, where I teach, is at the heart of our small town. Ringing campus are institutions not quite in line with the college’s values: evangelical churches, a Monsanto plant, and Brownells, a leading firearms dealer whose chief executive is president of the National Rifle Association. When Iowa went red in 2016, the media surveyed this landscape and nodded knowingly. They chalked it up to “economic anxiety.” <a target="_blank" href="https://www.iowaworkforcedevelopment.gov/sites/search.iowaworkforcedevelopment.gov/files/documents/iowaworkforceandtheeconomy_2017R.pdf">But Iowa’s economy is humming</a>; most cities here face labor shortages rather than mass unemployment.
I’ve lived my whole life in the Midwest—Rust Belt cities and tiny towns—and I’ve learned that good times make stoic Midwesterners more fearful than bad. When Barack Obama won Iowa in 2008, times were terrible, and Iowans wanted a leader who could confront hard truths. When the chips are down, my fellow citizens are tolerant, progressive, and open to change. Solutions matter here when the shit hits the fan.
Strangely, when times are good, fear often takes hold in a more sinister way. Throughout 2016, what I overheard at PTA events, taverns, and city celebrations was Midwesterners worked up to worry, precisely because everything was going so well. This region knows how quickly the good times can slip away—layoffs, droughts, floods.
The Trump campaign succeeded here because it trafficked in the nationalist-fascist idea that someone is going to take everything away. Trump’s message was not Make America Great Again. It was: They’re coming for you. “They” are an interchangeable cast of demons—immigrants, transgender individuals, gun-control advocates, people of color. But the message was consistent and was focused on communities where diversity is simply lacking. They’re coming for you, he said in every stump speech, and only I can stop them.`
        },
        kansas: {
          key: 'kansas',
          number: 16,
          name: 'Kansas',
          author: 'Sarah Smarsh',
          bio: 'Sarah Smarsh’s book on the working poor and her upbringing in rural Kansas will be published by Scribner in September.',
          text: `The winter wheat I helped raise west of Wichita was modified by man. Selected for a high yield come harvest, it grew in chemicals sprayed by low-flying planes that as a child I chased along the fields’ edges. We were in those fields while powerful people discussed farm subsidies at restaurant tables. They researched and debated “the issues.” Grandpa Arnie, who left school in sixth grade because his second-generation German-American dad said it was time to work, had a hole in his face where the skin cancer got cut out after decades on the tractor. So I reckon he knew quite a lot about the issues.
But there was a distance between what we knew and what we had the language or access to express. The people who taught me how to talk about America didn’t talk much about it all—cynicism about so-called democracy arising in the void where our access to it might have been. We were starved for someone to even feign to care about us. In my lifetime, Republicans have done the feigning, to great effect. But, in my experience, rural areas are a flight risk to either party. Free from allegiance to definitions that so often constrain the chattering class, my family’s politics are more like prairie grass than neat rows of wheat crops—independent, wild, overlooked. During the 2016 presidential primaries, like many working-class Americans, they supported a socialist from Vermont.
Kansas politics, while presumed “deep red” in modern times, in earlier years was among the most progressive in the nation. The prairie populism of those times is largely forgotten, but I see it sprouting where CNN isn’t looking. The great divide in America today is not between red and blue but between what is discussed in powerful rooms and what is understood in the field.`
        },
        kentucky: {
          key: 'kentucky',
          number: 17,
          name: 'Kentucky',
          author: 'Erik Reece',
          bio: 'Erik Reece is the author of five books of non-fiction, most recently Utopia Drive: A Road Trip Through America’s Most Radical Idea. He teaches writing at the University of Kentucky. ',
          text: `I’ll say this for white supremacists: They’ve done a great service to those of us who have grown sick of these moribund, monolithic Confederate generals on horseback. The more Nazis march, the faster Civil War monuments come down.
It happened last night in my hometown of Lexington. As late October light settled over Cheapside Park, formerly one of the largest slave markets in the country, <a target="_blank" href="http://www.kentucky.com/news/local/counties/fayette-county/article179392076.html">Mayor Jim Gray authorized cranes</a> to lift from their pedestals the statues of Confederate War Secretary John C. Breckinridge and Confederate marauder John Hunt Morgan (the horse Morgan rides in his statue is probably one he stole).
Some argued that taking down the statues “erases history,” but as in many other cases across the South, these monuments were erected during the Lost Cause movement of the Jim Crow era for the sole purpose of rewriting history, making the Confederacy look triumphant despite having lost. And they largely succeeded—until Charlottesville.
After that fatal day, many white Lexingtonians finally woke up to the hideous irony of celebrating those who perpetuated slavery in a former slave market, in the same state where the phrase “getting sold down the river” originated. A movement called <a target="_blank" href="https://www.takebackcheapside.com/">Take Back Cheapside</a>, co-founded by DeBraun Thomas, the great-grandson of a slave, spurred the mayor into action, and the city council voted unanimously to remove the statues of a traitor and a terrorist. Gray convinced the Lexington cemetery, where Breckinridge and Morgan are buried, to park the bronze figures next to their respective grave sites, and a contentious civic debate was artfully resolved.`
        },
        louisiana: {
          key: 'louisiana',
          number: 18,
          name: 'Louisiana',
          author: 'Maurice Carlos Ruffin',
          bio: 'Maurice Carlos Ruffin is the author of the novel We Cast a Shadow, forthcoming from One World Random House in 2019.',
          text: `I’m sitting in a gray, cinderblock room when the man enters. He’s mid-forties. Ruddy complexioned. Paunchy in that happily married, father-of-two way some guys have. He carries a fishing rod and chats up the guard, who’s jittery. I’m jittery too. It’s not every day I visit my brother-in-law, who I helped raise, in a central Louisiana prison.
My father, an uncle, and some cousins all spent time inside. My white friends always ask why I don’t do drugs. I tell them about my dad. They wonder how somebody gets real jail time for weed. “Exactly,” I always say.
My brother-in-law, call him Percy, is one of my favorite people. I spent a lot of time big-brothering him back in the day. Asking about school. Tossing around a football. He was great at throwing, so I considered doing something with him I was better at, like jogging or fishing. But I never got around to it.
Turns out, the guy with the fishing rod is the warden. He’s stopped in to check on his holdings. He’s still making that guard nervous when I get called back to see Percy.
In the interview closet, Percy and I chat like old times. He was slim, but each day they feed the inmates ham on white with mayo, which packs on the pounds quick. I’ve heard most of the inmates wind up with diabetes. I don’t blame myself for Percy’s chains, but I wonder what it would be like to finally catch some redfish with him.`
        },
        maine: {
          key: 'maine',
          number: 19,
          name: 'Maine',
          author: 'Roxanne Quimby',
          bio: 'Roxanne Quimby is the co-founder of Burt’s Bees.',
          text: `Here at the tail end of the North American jet stream, all outdoor growth has ended for the year. Dormancy and hibernation are the rule; daylight is fleeting; inky-dark nights offer ample time for rest and contemplation. My mind wanders back to the days of lilacs and lavender and buttercups. It doesn’t seem possible that just months ago such fragile beauty could have pushed itself through this presently cement-hard, olive-drab meadow out my window. But it did, and it will again. Regeneration is the way of nature.
A little over 18 months ago, the <a target="_blank" href="http://mainepublic.org/post/its-official-obama-declares-katahdin-woods-and-waters-national-monument#stream/0">Katahdin Woods and Waters National Monument was created</a> with land I helped conserve. A lot of the forest had been <a target="_blank" href="http://mainepublic.org/post/quimby-donates-87000-acres-land-federal-government">heavily harvested</a> before I purchased it and then donated it to the federal government. It will take many years for the forest to become whole again, just as it will take many years for this patch of land to become a real national park. I hope the Park Service will create more infrastructure for visitors: Improve the road, put up signage, welcome visitors with ranger-led activities in the regenerating forest.`
        },
        maryland: {
          key: 'maryland',
          number: 20,
          name: 'Maryland',
          author: 'John Lingan',
          bio: 'John Lingan’s first book, a history of the last honky-tonk in the Virginias, will be published in July.',
          text: `In 2015, as the national fight over Confederate statuary heated up, my <a herf="https://wtop.com/montgomery-county/2017/07/confederate-statue-moved-courthouse-maryland/">county executive announced</a> that a 13-ton bronze depiction of a gallant-looking Johnny Reb would be removed from the courthouse square about a mile from my house. It was the first I’d heard that Rockville—a deep-blue, multicultural city in the outer D.C. suburbs—even had such a thing. The statue was mostly shrouded in trees, blocks from the town center, amid a cluster of local government buildings. But news of the removal inspired a <a target="_blank" href="http://www.baltimoresun.com/news/maryland/bs-md-rockville-confederate-statue-20150804-story.html">Black Lives Matter graffiti tag</a> on its base, and the county moved to prevent further vandalism by encasing it in a comparatively high-visibility plywood cube. For two years it sat there, cheap-looking and inscrutable, like a hardware-store tribute to The Day the Earth Stood Still.
Finally the rebel was moved about 40 miles northwest this past summer, to the countryside grounds of a <a target="_blank" href="https://patch.com/maryland/rockville/controversial-confederate-soldier-statue-moves-whites-ferry">privately owned ferry business</a> that shuttles customers across the Potomac River to Virginia on a boat named for Confederate General Jubal Early. Many people assume that Maryland, the “Old Line State,” is Southern because our northern border is the Mason-Dixon line, but the Potomac, which wriggles along our southern reach, is really the truer barrier between North and South, and the confusion underlines the indeterminacy of my state. You can see it reflected in our schizophrenically patterned flag, and in our Civil War legacy of <a target="_blank" href="http://antietam.com/civil-war-pitted-brother-against-brother
">“brother against brother.”</a> In Maryland, blasphemous monuments may come down, but they don’t have to travel far to be welcomed home again.`
        },
        massachusetts: {
          key: 'massachusetts',
          number: 21,
          name: 'Massachusetts',
          author: 'Charles C. Mann',
          bio: 'Charles C. Mann is the author of 1491, 1493, and, most recently, The Wizard and the Prophet.',
          text: `For about 30 years, I’ve lived in the university town of Amherst. Statistically, it’s an odd place. A <a target="_blank" href="http://www.massbenchmarks.org/statedata/data/median99.pdf">middle-class</a> blue bubble in a well-off blue state, it has better-than-usual public schools and lower-than-usual rates of unemployment, divorce, and crime. But in one depressing way our town is just like the rest of the nation: We’re having trouble with this whole democracy thing.
Our government is a descendant of the storied New England town meeting, in which the colonists gathered en masse to pool their expertise, weighing tradeoffs as they created a new way of life in a new place. Now expertise and compromise seem increasingly beside the point, and way too much of our town meeting is spent fighting to reclaim a vision of the past.
Amherst is growing rapidly—over 13 percent since 2000. But the town has been stubbornly preoccupied with preserving its long-ago rural character, mostly by acquiring open space and fighting development. My wife, an architect, briefly volunteered for the town’s planning committee. Having experience with the construction industry, she pointed out that the nigh inevitable result of locking up land would be artificial inflation of the price of housing, which in turn would make our town unaffordable for working people and people on fixed incomes. She was accused of being a “tool of the developers.” Today about a third of the town is open space—and rents are amazingly high.
Like every modern U.S. town, Amherst must navigate through a horribly complex legal, regulatory, and technological landscape. Hardly anyone has more than a fraction of the required expertise. As a result, people at town meeting make choices based on gut feelings about right and wrong, regardless of whether those impulses are conflicting. I still love living here, but I worry that we are becoming ungovernable.`
        },
        michigan: {
          key: 'michigan',
          number: 22,
          name: 'Michigan',
          author: 'Benjamin Busch',
          bio: 'Benjamin Busch is a filmmaker, illustrator, and the author of Dust to Dust: A Memoir.',
          text: `We welcome you to Pure Michigan on our border signs, but we’re selling a pre-human adjective. Purity is mythology; we have no living memory of it here.
The state was once known for its 16 million acres of old-growth forest. You can find one of the largest surviving tracts of virgin white pine in Grayling. It’s 49 acres. <a target="_blank" href="http://www.passengerpigeon.org/states/Michigan.html">The last “grand nesting”</a> of passenger pigeons on Earth was slaughtered in Petoskey in 1878. Over a million birds. Detroit is spending hundreds of millions of dollars of everyone’s taxes to demolish <a target="_blank" href="https://www.nytimes.com/2014/05/28/us/detroit-task-force-says-blight-cleanup-will-cost-850-million.html">40,000 abandoned homes</a>. The Kalamazoo River is the site of the nation’s largest inland oil spill, and Flint’s city water is poisoned with lead. Our abundance has protected us from scrutiny.
Michigan was made by water, our peninsula formed from glacial till. The land is still rising, the Earth’s crust slowly recovering from the weight of ice one mile thick. We touch four of the five Great Lakes and take our name from one of them as if we live on water too: the Ojibwe word Michigama, meaning “large lake.” Our auto, steel, and agricultural industries have dumped, spewed, and sprayed so many toxins into it, you can only eat one eight-ounce serving of brown trout or whitefish a year (none if you’re pregnant). We go too far, then act surprised.
But some of our deep aquifers are still clean—and they’re worth money. Nestlé pumps 13,000 gallons an hour from its Ice Mountain well 13 miles from my farm. (The nearest mountain is actually 400 miles away.) Now <a target="_blank" href="https://www.freep.com/story/news/local/michigan/2017/04/19/nestle-groundwater-michigan-great-lakes/100663218/">they’re pushing to increase their pumping limit</a>, imposed to protect regional springs, to 24,000 gallons an hour. They contend that this is “reasonable use” and that they can draw the groundwater like any citizen with a well in their yard. Nestlé is a Swiss company worth over $200 billion. They pay a $200 annual licensing fee to the state. If you ask me, selling public water is like commercializing air, like being proprietary about rain. But there it is: We let a foreign corporation drain aquifers beneath our properties and sell it back to us, while we pay the taxes. That’s pure Michigan.`
        },
        minnesota: {
          key: 'minnesota',
          number: 23,
          name: 'Minnesota',
          author: 'Patrick Nathan',
          bio: 'Patrick Nathan’s first novel, Some Hell, was published by Graywolf Press in February. He lives in Minneapolis.',
          text: `Minnesotan culture functions on an absence of vocalized conflict, or “Minnesota nice.” One positive repercussion of the last presidential election was the shattering of this culture. For years, many of us have known people—friends, family, co-workers—who are subtly if not overtly racist, which means many of us have tolerated racism. Post-election, I see white Minnesotans doing the work. One no longer hesitates to explain how the black community is terrorized by police, or how Somali and Latinx families strengthen Minnesota neighborhoods. This was unthinkable before the election, when people just had “different beliefs.”
When a friend of mine, who is black, wrote a scathing post about the Minneapolis police, a white acquaintance of ours commented, “There are two sides to every story.”
“Yes,” my friend replied, “but I’m on the side that keeps getting shot.”
Those who lament a supposed breakdown of “civility” are always those who benefit from a civilization that elevates one group of people at the expense of another. In Minnesota, I’m happy to see this civility go, especially if it means, with work, we can turn a civilization into a society.`
        },
        mississippi: {
          key: 'mississippi',
          number: 24,
          name: 'Mississippi',
          author: 'W. Ralph Eubanks',
          bio: 'W. Ralph Eubanks is the author of Ever Is a Long Time: A Journey Into Mississippi’s Dark Past.',
          text: `In Mississippi, the state’s obsession with myth and tradition fuels politics. Nowhere is this preoccupation more evident than in the long-running controversy over the Confederate emblem in its state flag. Even after white supremacist and neo-Confederate Dylann Roof killed nine people in a Charleston, South Carolina, church shooting, and riots led by Confederate flag-bearing neo-Nazis in Charlottesville, Virginia, caused death and injury to innocent bystanders, Mississippi’s political leaders continue to deny that there is any link between the Confederate emblem emblazoned on their flag and the politics of racial intimidation.
Of course, that’s what the flag has always been about. After the Civil War, Mississippi was a majority African-American state, electing black candidates to the U.S. Senate. In response, the nearly all-white Mississippi legislature passed a new constitution, which effectively disenfranchised most African-American voters by instituting discriminatory poll taxes and literacy tests. The new state flag, <a target="_blank" href="https://www.newyorker.com/news/news-desk/mississippi-the-two-flag-state">adopted in 1894</a>, was meant to permanently enshrine that bigotry, even if it harmed the state by marginalizing half its population.
Today, it is no secret that Mississippi sits at the <a target="_blank" href="https://www.usnews.com/news/best-states/mississippi">bottom rung of several national rankings</a>—in education, poverty, health care, economic development, even the number of its residents who own passports—driving away the best of the state’s young people. Mississippi has lost the largest percentage of its Millennial population of any state. While none of this is directly related to the flag flying over the state house in Jackson, that flag has come to symbolize the state’s lack of progress.
Last year, lawyer and municipal judge Carlos Moore <a target="_blank" href="https://www.npr.org/sections/thetwo-way/2017/11/27/566737228/supreme-court-rejects-case-over-confederate-emblem-on-mississippi-flag">petitioned the U.S. Supreme Court</a>, saying that the “message in Mississippi’s flag has always been one of racial hostility and insult.” In the end, the court did not hear the case, but Moore says he is not giving up. If the flag ever changes, it could lead Mississippi, at last, to pay attention to long-term political and economic issues—but myths, like moonlight and magnolias, hold the real power down here.`
        },
        missouri: {
          key: 'missouri',
          number: 25,
          name: 'Missouri',
          author: 'Jason Kander',
          bio: 'Jason Kander is the former secretary of state of Missouri and the founder of Let America Vote.',
          text: `In early 2013, I went toe-to-toe with Kris Kobach at my first National Association of Secretaries of State meeting in D.C. He wanted to pass a resolution instructing the federal government to give states “maximum flexibility” in running elections, in order to clear the path for a national voter-suppression effort like the one <a target="_blank" href="https://www.nytimes.com/2017/06/13/magazine/the-man-behind-trumps-voter-fraud-obsession.html">he had implemented in Kansas</a>. When I accused him of injecting partisanship into a non-partisan organization, he said there was nothing partisan about his proposal, and that as state election officials we should all oppose federal involvement in elections. I responded: “Let’s talk about what we’re really talking about. One party wants the federal government to stay out of elections, and the other party wants to let black people vote.” (Kobach says he has no recollection of the conversation.)
It took him until 2017, but Kobach finally got a federal government interested in voter suppression. It began when President Trump told the biggest lie an American president has ever told: that there were <a target="_blank" href="https://www.washingtonpost.com/news/post-politics/wp/2017/01/23/at-white-house-trump-tells-congressional-leaders-3-5-million-illegal-ballots-cost-him-the-popular-vote/?utm_term=.dedb19f04bc3">three to five million illegal votes</a> in the 2016 election. And the truth is, it was the first step of Trump’s re-election strategy. By repeating this lie, he provided cover for Republican legislatures to pass restrictive laws like voter ID requirements, which make it harder to vote for a whole bunch of people who have the nasty habit of voting Democratic. And, ironically, Kobach led the charge from his perch at Trump’s federal voter-suppression commission. But in January, after the commission failed to produce evidence of fraud, <a target="_blank" href="https://www.cnn.com/2018/01/03/politics/presidential-election-commission/index.html">Trump dissolved it</a>—blaming states for not cooperating with his fishing expedition.
I started Let America Vote because I believe that, if politicians make it harder for people to vote, it should be harder for those politicians to get re-elected. This year, we tested that message on a national stage. We knocked on almost 200,000 doors in Virginia and won every race we targeted, replacing seven vote-suppressing Republicans with pro-voting Democrats. In 2018, we’re opening offices in five more states. Let America Vote is going to make sure that there are political consequences for voter suppression, so that politicians will think twice before trying to strip away your voting rights. If they want to take away the rights of Americans, they’re going to have to go through us.`
        },
        montana: {
          key: 'montana',
          number: 26,
          name: 'Montana',
          author: 'Molly Priddy',
          bio: 'Molly Priddy is a writer and editor living in northwest Montana.',
          text: `Smoke from <a hre="http://www.greatfallstribune.com/story/news/2017/09/07/montanas-million-acre-burn-all-you-need-know-fire-season/633420001/">one of the worst wildfire seasons ever in Montana</a> obscured the skies as summer turned to autumn, and the local kids went back to school. 
Tourists slowly rolled out of our mountain valley, and impending snow promised to put out the fires we couldn’t.
Then, everything stopped, the transitional time turning into one of stasis. <a target="_blank" href="http://cordilleramontana.worldnow.com/story/36362734/flathead-co-school-classes-canceled-friday-amidst-threat">School in Columbia Falls was canceled</a>, the Flathead County sheriff said, because there were threats against the children. 
Within a day, other school administrators began receiving threats, and <a target="_blank" href="https://www.usnews.com/news/best-states/montana/articles/2017-09-14/the-latest-officers-questioning-people-in-school-threats">authorities decided to close all of the schools in the county</a>.
For three weekdays and one weekend in between, more than 30 schools in this valley to the west of Glacier National Park were held hostage by what we would learn was an international organization calling itself <a target="_blank" href="http://flatheadbeacon.com/2017/09/19/cyber-expert-sheds-light-hackers-motives-strategy/">TheDarkOverlord Solutions</a>, which had infiltrated one of the school district’s computers and sent messages promising death and chaos unless they were paid in Bitcoin. 
People couldn’t work because they had to stay home with their kids, and many events and activities involving children were canceled. 
Even the FBI couldn’t immediately parse the highly sophisticated cyber attack.
There was fear. But there was also the sense of a community coming together, standing side by side, ready to defend our children.
By the time authorities determined the death threats weren’t credible, cooler weather was moving into the valley, with frost warnings and high-elevation snowfall.
The fires are out now, though the burn areas remain, and our small mountain valley has added a new existential threat to the list. We will confront this new threat the same way as all the others: together, or not at all.`
        },
        nebraska: {
          key: 'nebraska',
          number: 27,
          name: 'Nebraska',
          author: 'Carson Vaughan',
          bio: 'Carson Vaughan is a freelance writer based in Omaha.',
          text: `When I was a college sophomore, I returned over Christmas break to my hometown in rural Nebraska. Looking for an excuse to leave the house, I asked an old friend to meet me at the bar. When the waitress spotted us grabbing a table near the jukebox, she tilted her head and drawled: “Y’all two gay or somethin’? You don’t look like you’re from around here.”
On the surface, it makes me laugh: two lifelong friends deemed homosexual for looking a little out of place in our own hometown. But it’s the layers that keep me stewing. Did she intend to offend us? I don’t think so. She said it with a smile. But what if we had been? How would she respond? And if she were simply kidding around, isn’t that worse? That her idea of a joke was calling someone gay?
It keeps me stewing because my hometown and so many like it in rural Nebraska reflexively call bullshit when confronted with claims of homophobia, or xenophobia, or an -ism of one kind or another. They contend stories like this are indicative of little more than “PC culture,” where liberals and “lamestream” media cherry-pick their anecdotes, and surely now and then they’re right.
I have no clue where that waitress stood on gay rights. But I do know this: Recently a law student from my hometown returned to lead a recall effort against a pair of school board members who, in his view, have hijacked the school budget to lower their property taxes. He also happens to be gay. The morning after he filed the affidavits, he woke to find the rear window of his car shattered. Later, at the county fair, he was stopped by an older gentleman who warned, “We don’t want your kind here.” And while he was celebrating his birthday at the new restaurant in town, the words “recall” and “faggot” repeatedly dribbled down from the end of the bar, so egregiously the bystanders later apologized.
There is plenty of virtue to be found in rural Nebraska. But there is also plenty of shame. If we hope to stem the brain drain we so frequently bemoan, perhaps we should start with our long-neglected culture of intolerance. Perhaps we should start at the bar.`
        },
        nevada: {
          key: 'nevada',
          number: 28,
          name: 'Nevada',
          author: 'Michael P. Branch',
          bio: 'Michael P. Branch’s recent and forthcoming books are Raising Wild, Rants From the Hill, and How to Cuss in Western.',
          text: `If the population of its two urban anomalies—the metropolitan areas of Las Vegas and Reno—were removed from the headcount, each of Nevada’s 110,000 square miles would average a population density of six folks. <a target="_blank" href="https://www.cbsnews.com/pictures/most-heavily-armed-states-in-america/45/">Many of those rural Nevadans</a>, including myself, own firearms, which we use for sport, hunting, or home defense.
I live with my family at 6,000 feet on an isolated, sage-dotted knoll in the western Great Basin Desert, adjacent to a mountainous swath of 75 million acres of public lands. This high, cold desert is so remote and so spectacularly beautiful that news of the world, when it reaches us, sometimes feels abstract and unreal.
Today’s news concerns <a target="_blank" href="https://www.reviewjournal.com/local/the-strip/shooting-memorial-crosses-will-be-moved-sunday-to-clark-county-museum/">the dismantling of a spontaneous memorial</a> that had sprung up in the shadow of the iconic Welcome to Fabulous Las Vegas sign. Fifty-eight white crosses, one for each victim of the mass shooting that occurred nearby on October 1st, each cross covered with flowers, letters, photographs, mementos of every kind. Small gestures of remembrance offered by friends or strangers, now boxed up and trucked away. This is yet another act of erasure, part of a larger moral failure to keep the unthinkable costs of the American epidemic of gun violence squarely in our view.
I am almost 500 miles from the vanished memorial, and all I can see from my kitchen window is alpenglow on early season snowfields. But even here, in the glowing vastness of the high desert, there is no longer an away to run to. Those of us who choose to own weapons must stand up for reasonable reforms that might help prevent the need for more white crosses in our communities.`
        },
        newHampshire: {
          key: 'newHampshire',
          number: 29,
          name: 'New Hampshire',
          author: 'Alexander Chee',
          bio: 'Alexander Chee is the author of How to Write an Autobiographical Novel and associate professor of creative non-fiction and fiction writing at Dartmouth College.',
          text: `Last year, before a state election, Kris Kobach, leader of the now-disbanded election integrity commission, <a target="_blank" href="https://www.washingtonpost.com/news/fact-checker/wp/2017/09/25/kris-kobachs-claim-that-there-is-now-proof-of-voter-fraud-in-new-hampshire/?utm_term=.8d78c90ca057">took notice of New Hampshire’s law</a> that allows same-day voter registration. The law was <a target="_blank" href="http://www.wmur.com/article/sununu-would-love-to-do-away-with-same-day-voter-registration/8341844">passed in 1994</a> to retain what New Hampshire voters consider to be their independence in the face of the National Voting Rights Act—a very local and Republican states’ rights posture. But now, national Republicans like Kobach say there’s no way of knowing if college students are voting twice, in their home state and also in New Hampshire. This is part of a national effort to restrict student voting, which runs liberal.
White House adviser <a target="_blank" href="https://www.washingtonpost.com/news/politics/wp/2017/02/12/mixed-into-his-falsehoods-on-voter-fraud-stephen-miller-did-hit-on-one-truth/?utm_term=.9eb0e8ee9bc5">Stephen Miller said</a>: “I can tell you that this issue of busing voters into New Hampshire [from Massachusetts] is widely known by anyone who’s worked in New Hampshire politics. It’s very real. It’s very serious.” It isn’t. They blame Republican Senator Kelly Ayotte’s loss of her seat on this supposed fraud, but there’s no evidence. There are no photos on social media of buses from Massachusetts, no record of a massive number of Massachusetts drivers’ licenses used to vote in the towns near the border. In fact, outside of Nashua, Ayotte did better in those border towns. If people were coming into New Hampshire from Massachusetts to vote, it seems they voted for her.
Just three years ago, when <a target="_blank" href="https://www.bostonglobe.com/metro/new-hampshire/2015/05/14/new-hampshire-lawmakers-consider-canning-same-day-voter-registration/iDczVMRKABTfPcY5akGNWJ/story.html">New Hampshire legislators considered limiting same-day registration</a> for voters by requiring proof of 30 days’ residency, it was seen as a move that would be disadvantageous to the state’s Republicans and independents, who like to decide not only if they’re going to vote but who they’ll vote for right up until the day of the election—part of the reason the state is so hard to game for national campaigns during the primaries. The law affects a very small number of voters, but enough potentially to swing an election. But again: This is what New Hampshire voters like about it. The law is unlikely to change, and if it does, it won’t change because of Kris Kobach. Note to national Republicans: You campaigned on states’ rights for decades. Local Republicans remember this even if you don’t—and, in New Hampshire, they won’t roll over on it for you, no matter what you call yourselves.`
        },
        newJersey: {
          key: 'newJersey',
          number: 30,
          name: 'New Jersey',
          author: 'Tom Colicchio',
          bio: 'Tom Colicchio is a chef and the co-founder of Food Policy Action.',
          text: `For nearly 20 years, my mom ran the school lunch program at Elizabeth High School. As my brothers and I got established and more successful, we urged her to retire. “Mom, you’re always complaining that you’re tired,” we’d say. “Why don’t you quit and take it easy?” She always resisted—and finally explained that, for many of the kids at her school, the meal she planned and prepared at lunchtime was the only food they got all day. At that time, 70 percent of the kids in Elizabeth qualified for free or reduced-cost lunch. There were thousands of kids in just that one school who didn’t get a fruit or a vegetable at home. How could she retire, if she couldn’t be sure that all those kids would get at least one good, healthy meal every day?
New Jersey has made great strides in its free and reduced-price meals programs since then, moving from 48th in the nation to 19th, for how many qualified kids it serves breakfast and lunch to. I would like to see every child in New Jersey receive a free breakfast and a free lunch. <a target="_blank" href="http://www.sciencedirect.com/science/article/pii/S0272775713000885">Plenty of hard data</a> shows that kids’ learning improves when we do this. Feeding children a wholesome diet of fruits and vegetables—and giving them nutrition education in the classroom—also helps them establish lifelong healthy eating habits that will reduce preventable illnesses like diabetes and heart disease. These changes would make for more productive graduates and save us on health-care costs in the long run.
Most of all, it’s the right thing to do. No kid should go hungry at school. No kid should be forced to eat food that contributes to future health problems. My mom wouldn’t allow that, and neither should we.`
        },
        newMexico: {
          key: 'newMexico',
          number: 31,
          name: 'New Mexico',
          author: 'Alex Heard',
          bio: 'Alex Heard is the editorial director at Outside in Santa Fe.',
          text: `Friends who’ve never been to northern New Mexico are surprised when I tell them that Santa Fe sits at 7,000 feet, next to a massive stretch of the southern Rockies known as the Sangre de Cristo range. That means “blood of Christ,” and some people take the phrase literally. New Mexico has long been home to a <a target="_blank" href="https://www.huffingtonpost.com/2015/04/03/penitentes-new-mexico_n_6990204.html">sect of self-flagellating Catholics</a> called Penitentes. Though their goriest days are past, they’re still around. But I’ve found a different kind of solace and self-revelation on the trails through these public lands.
I’ve hiked hundreds of miles in the Sangres. Almost the entire range in New Mexico falls into two national forests: the Carson and Santa Fe. Along the way, I’ve bumped into some serious mojo: elaborate crosses built in the middle of trails; light that illuminated the night sky over my backpacking tent (I didn’t crawl out to look, but I assume it came from a UFO or a <a target="_blank" href="http://www.santafenewmexican.com/news/local_news/a-haunted-history-new-mexico-s-rich-past-means-state/article_4e6e9881-4450-59d1-b6f0-78c150f04848.html">flaming bruja</a>, a flying witch); and, on two occasions, encounters with actual Christ figures.
Two years ago in early spring, I was coming down the side of a mountain, through snow, when I saw a long-haired man moving fast up a cold, muddy trail. He was barefoot, wore a robe, and used a staff. I didn’t ask if he was Jesus—that seemed too forward—but I did want to know about the shoelessness: Why? “One hundred thousand years of human evolution can’t be wrong!” he said.
Six months later, at the sundown end of a big trek—14 miles, 3,000 feet of elevation gain—I ran into an old Santa Claus-looking guy who was moving at a rate of 10 feet per minute. He said he liked to hike in the dark and would eventually make it seven miles into the wilderness before turning around. Moved by his genuine oddness, I blurted out details of a serious health problem I had at the time, which made the hike I’d done not just hard, but dangerous and stupid. In the tone of someone who truly cared, he said: “Hey, if you can do all that, feeling like you do? You’re going to be fine.” Turned out he was right. Don’t tell me there’s no magic in those hills.`
        },
        newYork: {
          key: 'newYork',
          number: 32,
          name: 'New York',
          author: 'Lisa Lucas',
          bio: 'Lisa Lucas is the executive director of the National Book Foundation.',
          text: `Every morning, we crowd in. Backpacks, coats, today’s groceries, a new set of pillows, who-knows-what-else—all crammed in with us into each subway car as we head out to the various places we are going. It’s a mystery that we have so much in common, that we spend so much time in close proximity, and yet are complete strangers—personally, politically, in a million different ways. One morning, you spill everything in your bag on the floor and the people around you scramble to help. Another morning, you ask a gentleman to move in and make space and he screams, “Our president is not a racist!” People’s motives, whether well-meaning or mean-spirited, are obscure, because we are passing through our days without the ability to access the realities of other lives. We are together, profoundly together, in these small, shared spaces, and yet we know nothing about the person whose armpit we just spent 20 minutes sniffing—how they vote, why they vote, what inspires them, what holds them back.
I like to look at all the books people are reading. Watching my fellow New Yorkers reading about the lives of others, whether real or imagined, in the in-depth and engaged way that only books provide, gives me comfort in this divided time. I sometimes refer to 2017 as the year that Americans collectively realized that we don’t know each other very well. We New Yorkers don’t really either. Despite what the news might have you think, we’re not a unified city or state. But when I look at all the bookstores that thrive here, all the publishers that charge ahead here, all the poets and writers who live or pass through here, all the readers on trains and planes and busses and in waiting rooms that learn here, I have hope that we New Yorkers want to know each other better, and the world better, and that, in this way, we will create more connections than divisions. Every day I see a book on the subway that is lighting someone’s way with knowledge.`
        },
        northCarolina: {
          key: 'northCarolina',
          number: 33,
          name: 'North Carolina',
          author: 'Bronwen Dickey',
          bio: 'Bronwen Dickey is a contributing editor at Oxford American and the author of Pit Bull: The Battle Over an American Icon.',
          text: `When the people of Durham cast their ballots in the city’s mayoral primary last October, the overwhelming majority voted for the <a target="_blank" href="http://www.heraldsun.com/news/local/counties/durham-county/article188061049.html">most progressive candidate</a>. When that candidate went on to win the general election, Durhamites were probably expecting that their new mayor would <a target="_blank" href="https://www.stevefordurham.com/">deliver on his promises</a>: affordable housing, police reform, LGBT anti-discrimination laws, greater protections for immigrants, and stricter environmental regulations. What North Carolina voters might not understand, however, is that the state legislature can, and most likely will, block him from doing pretty much anything.
Here, as in many other states, the General Assembly can use a legal process known as state preemption to overrule decisions made by local governments in virtually every area of civic life, from employment regulations (like changes in the minimum wage) and environmental protections (fracking bans, bans on plastic bags) to anti-discrimination ordinances and laws designed to shield immigrants from harassment and deportation (sanctuary cities).
The city of Charlotte learned the hard lesson of state preemption back in 2016, when it tried to expand its existing anti-discrimination ordinance to protect members of the LGBT community, including the right of transgender citizens to use whichever public bathrooms they felt most comfortable in. The General Assembly responded with House Bill 2, better known as the bathroom bill, which not only rendered Charlotte’s expanded law illegal, but also placed restrictions on local governments enacting higher minimum wage laws, among other things. The ensuing national uproar over HB2 <a target="_blank" href="https://www.cnbc.com/2017/03/27/bathroom-bill-to-cost-north-carolina-376-billion.html">wounded the state’s economy</a>, prompting an eventual “compromise” repeal, but even that left equal-rights advocates despondent.
State preemption doesn’t have to be socially regressive, of course, but increasingly, the preemption trend moves in only one direction. Because larger, more racially diverse urban centers tend to enact more liberal policies—only four of the mayors in America’s largest 25 cities are Republican—this amounts to an ongoing power struggle in conservative states, with cities almost always losing out. Doesn’t sound so democratic, does it?`
        },
        northDakota: {
          key: 'northDakota',
          number: 34,
          name: 'North Dakota',
          author: 'Debra Marquart',
          bio: 'The author of a several books of poetry and a memoir, The Horizontal World, Debra Marquart grew up in North Dakota on land her great-grandparents claimed after they emigrated from Russia—land that is also considered the ancient tribal homeland of the Oceti Sakowin.',
          text: `On a ranch outside Fort Yates, not far from the now infamous Lake Oahe Reservoir on the ancestral homelands of the Standing Rock Sioux Tribe, a man named Jon Eagle Sr. is engaged in a patient and necessary life’s work: healing young people and families through equine therapy. <a target="_blank" href="http://becomingonewiththespiritofthehorse.com/home">His project, Sung Nagi Kici Okiju</a>: Becoming One With the Spirit of the Horse, offers participants guided interactions with the traditional American Paint horses that he raises. “I once had someone ask me, ‘How do you teach someone how to ride a horse?’ I thought about it for a while, then said: ‘You don’t. You teach them how to have a relationship with a horse.’” The foundation of Lakota horsemanship begins with developing a relationship of mutual respect and trust with the horse.
“[W]e seem to have forgotten ... how traumatic the loss of the horse was to our ancestors,” Eagle writes, citing the 350 war ponies that were forcibly confiscated when Sitting Bull surrendered at Fort Buford in 1881. In this century and through the long lens of history and memory, Jon Eagle Sr. works on renewing the compact of trust with the “horse nation.” “Our ancestors weren’t just good horsemen, they were good relatives,” he writes. The need for reconnection is acute. Among native populations ranging between ages 15 and 24, the <a target="_blank" href="https://www.ihs.gov/dps/includes/themes/responsive2017/display_objects/documents/Trends2014Book508.pdf">second-largest cause of death is suicide</a>—and it occurs at a rate over three times the national average. The causes: economics, isolation, despair, intergenerational trauma, poor access to mental-health care. Eagle believes the wisdom of the horse nation has the power to reach inside and guide us all toward healing, if only we will respectfully come into its presence. “When a horse shares breath with us,” he once said, “that’s a sacred thing.”`
        },
        ohio: {
          key: 'ohio',
          number: 35,
          name: 'Ohio',
          author: 'Connie Schultz',
          bio: 'Connie Schultz won a Pulitzer Prize for her columns for the Cleveland Plain Dealer and is now a nationally syndicated columnist for Creators Syndicate.',
          text: `I’m a professional-in-residence at Kent State’s journalism school. In my campus office is a framed canvas reproduction of Norman Rockwell’s <a target="_blank" href="https://www.thisamericanlife.org/562/the-problem-we-all-live-with-part-one">The Problem We All Live With</a>. The painting depicts six-year-old Ruby Bridges, just steps away from becoming the first black student to enter an all-white school in the South. She is flanked by federal marshals, but the little girl in the white dress, with a bow on her braid and another at the small of her back, looks so alone. There she is, notebooks and ruler in her hand, as she makes her way past the thrown tomatoes splattered on the wall behind her and the scrawled slur nigger looming just above her head.
For a time, the original Rockwell painting <a target="_blank" href="https://www.washingtonpost.com/lifestyle/style/norman-rockwell-painting-of-ruby-bridges-is-on-display-at-the-white-house/2011/08/26/gIQA66QhlJ_story.html">hung in the White House</a>, just outside the Oval Office. During Barack Obama’s tenure, I should add. When we had a president who cared about the history of our country’s civil rights movement, I should also add.
I bought the canvas print in early 2017, soon after a conservative cartoonist <a target="_blank" href="https://www.nbcnews.com/news/nbcblk/cartoon-comparing-betsy-devos-ruby-bridges-sparks-backlash-n721531
">swapped out Ruby Bridges</a> for an infantilized image of Secretary of Education Betsy DeVos, a white billionaire whom protesters temporarily blocked from entering a school. The cartoon version replaced the racist epithet with conservative, and took a shot at the largest teachers’ union by scrawling nea at the wall’s edge.
I taught ethics and feature writing that semester, and we discussed the two illustrations in both of my classes. All of the black students knew about Ruby Bridges. Virtually none of my white students, many of whom share my working-class roots, had ever heard of her.
That evening, I ordered the print. When it arrived, I lugged it from my car to my third-floor office, where I nailed it to the wall. Most weeks, at least one young person does a double-take at the sight of that image. As always, the conversation is everything. We talk about Ruby Bridges and why her story is our story, too, in this battleground state of Ohio.`
        },
        oklahoma: {
          key: 'oklahoma',
          number: 36,
          name: 'Oklahoma',
          author: 'Rilla Askew',
          bio: 'Rilla Askew’s most recent book, Most American: Notes From a Wounded Place, explores the legacy of mass violence in Oklahoma.',
          text: `In the small white Baptist church in the small white Oklahoma town where my family has worshipped for nearly a century, the community holds an annual celebration called Guns & Gravy. The men of the church bring their guns and hunting trophies to Fellowship Hall, where they mount huge racks of antlers, heads of bucks, wild hogs, stuffed foxes, the occasional elk or bear. The women cook up huge batches of biscuits and gravy, and throughout the day visitors come from all over the county to admire the trophies, eat, swap stories, and talk about guns and God and good hunting.
At news of the <a target="_blank" href="http://wjla.com/news/nation-world/multiple-injuries-reported-at-a-church-shooting-in-sutherland-springs-tex
">slaughter in the church</a> in Sutherland Springs, Texas, last November, these were the faces I saw, the people of my parents’ church: their sweet spirits, their children. My Facebook feed was filled with strident calls for gun control legislation, because most of my friends are urban liberals with little understanding of or tolerance for gun culture. But I grew up with guns in Oklahoma. My father, a hunter, owned dozens. My sister Ruth lives in our same small town. Her post said: “The problem is the semiautomatic weapon. If this latest guy had toted a .22 or shotgun, he might have killed the ex-mother-in-law he blamed for his trouble, but he would not have decimated an entire community.” But I don’t think the people of our parents’ church can hear her. I think of how this divides us, this understanding of God and guns. On both sides, we’ve stopped our ears. I think: The people I love have been misled. Fundamentalism, in faith or politics, brooks no compromise.
But I remain hopeful that moral courage may someday come to our leadership, in politics and in religion: moral courage and nuance and articulate voices and open ears. I remain hopeful that someday the slaughter will be sufficient.`
        },
        oregon: {
          key: 'oregon',
          number: 37,
          name: 'Oregon',
          author: 'Garrett Hongo',
          bio: 'Garrett Hongo is the author of Coral Road and distinguished professor of creative writing at the University of Oregon.',
          text: `At first, news of the <a target="_blank" href="http://www.oregonlive.com/portland/index.ssf/2017/02/oregon_standoff_timeline_41_da.html">occupation of the Malheur Wildlife Refuge</a> by armed “protesters” in January of 2016 didn’t bother me. It seemed a clown show, an attempt to grab media attention by a group of yahoos in shearling jackets and cowboy hats, a re-enactment of Wild West movie standoffs between sheepherders and cattlemen—a theater for the nostalgic whiteness of bad-boy John Waynes. That they usurped land-use by peaceful citizens (birders, mostly), local ranchers, and <a target="_blank" href="https://www.scribd.com/document/303442094/3-9-16-ECF-282-U-S-A-v-A-BUNDY-et-al-Superseding-Indictment">members of the Burns Paiute tribe</a>, whose burial grounds are within the refuge, became clear to me later. That pissed me off. When the standoff dragged on to over 40 days, I realized the occupiers hoped to spark a wider conflict in American society—between those who believed in bounty and its plunder and those who believed in communal sharing and responsibility. But it was still a clown show—until a federal agent shot and killed one of the yahoos as they drove to a meeting off the refuge.
When Jeremy Christian, <a target="_blank" href="http://www.oregonlive.com/portland/index.ssf/2017/06/jeremy_christians_path_from_tr.html">a white supremacist</a>, murdered two men and stabbed another on a TriMet MAX train in Portland last May, I got very upset. I mourned for the victims (white men) and pitied the two women (one black, the other Muslim) they were trying to defend as Christian shouted racialized hate speech at them. Why hadn’t the two Samaritans realized Christian’s intent was to trigger his own violence? Trying to confront him was foolish—whatever social power the victims thought they might have had over him or mutuality they might have appealed to in that horrible moment just evaporated in Christian’s malevolence. They should have shielded the women and retreated as far as they could. Or they would have had to fight him.
Why is violence so ready as a solution for differences? What is this juvenile romance with privileges that have to be defended? And why does it flourish in our current climate, stoking grievances against people of color, immigrants, anyone who wishes to share in a common good? Who incites these angers? Who profits?`
        },
        pennsylvania: {
          key: 'pennsylvania',
          number: 38,
          name: 'Pennsylvania',
          author: 'Jason Fagone',
          bio: 'Jason Fagone is the author of The Woman Who Smashed Codes.',
          text: `One of the great dividers of Pennsylvanians is a single sentence of 30 words planted like a toxic tree in the soil of the state constitution. Called the <a target="_blank" href="https://www.picpa.org/articles/picpa-news/2015/09/03/the-power-behind-pennsylvania-s-uniformity-clause">Uniformity Clause</a>, it mandates that “all taxes shall be uniform, upon the same class of subjects, within the territorial limits of the authority levying the tax, and shall be levied and collected under general laws.” It means that any taxing authority in Pennsylvania, from the state itself to a city like Philadelphia and down to the tiniest town, has to make sure that similar “classes of subjects” are taxed at the same rate. In general, commercial real estate can’t be taxed at higher rates than residential real estate, and the wealthy can’t be taxed at higher rates than the poor. Taxes have to be “flat.”
Though other states also have uniformity rules, Pennsylvania’s clause, which dates to 1874, is uniquely broad and powerful—“a giant among its peers,” according to the Pennsylvania CPA Journal. And it distorts the state in strange and poisonous ways. To take one example: Recently, Philadelphia leaders decided to expand the public school system to include pre-kindergarten classes. <a target="_blank" href="https://www.npr.org/sections/ed/2017/12/12/568378251/does-preschool-pay-off-tulsa-says-yes">Studies</a> show that pre-K helps kids make faster progress and gives a particular boost to children from disadvantaged families. It’s a good, smart, sensible thing. But how to pay for it without violating the clause? Unable to raise taxes on businesses or rich residents, the city taxed poor families instead. In 2016, the city council passed a “<a target="_blank" href="https://www.theguardian.com/business/2016/jun/20/philadelphia-soda-tax-pre-k-funding-obesity-health">soda tax</a>” that jacked up the prices of all sweetened beverages, reaching straight into the pockets of kids buying lemonades, hurting the businesses of bodega owners, and spawning legal challenges from the beverage industry that are expensive to fight—all because of 30 words in a 144-year-old clause and an insistence that money to provide opportunity for those with the least shouldn’t come from those with the most.`
        },
        rhodeIsland: {
          key: 'rhodeIsland',
          number: 39,
          name: 'Rhode Island ',
          author: 'Elizabeth Rush',
          bio: 'Elizabeth Rush is the author of Rising: Dispatches From the New American Shore (Milkweed Editions). She teaches creative non-fiction at Brown University.',
          text: `There are two standard license plate options in Rhode Island. One design features the smooth silhouette of a light blue wave about to break. The other is more old-school New England: a line drawing of a schooner. Both designs pay homage to the sea, but in one, it is a dynamic force, always in motion; in the other, it appears more static, a mere stage for a boat. These days I worry that, when we hold onto a static image of the ocean, we’re less prepared for how its ongoing transformations are likely to change our coastal communities.
When I moved to Providence from New York City in 2015, I chose the wave. I unwrapped my plate in the parking lot and was pleased to find it was also graced by Rhode Island’s official nickname: Ocean State. No state save Maryland, and it only by a hair, ranks higher in the ratio of coastline to overall acreage. The year I moved to Lil’ Rhody was also the year the Coastal Resources Management Council <a target="_blank" href="http://www.crmc.ri.gov/maps/maps_slamm.html">released a set of detailed maps</a> showing the long-term impact of sea level rise on my new postage stamp-sized home state.
Local communities are now using these maps to prepare for the water that will come. In Warwick, a portion of Sea View Drive that flooded repeatedly in the past was, instead of being repaired, <a target="_blank" href="http://www.providencejournal.com/news/20171009/heres-how-rhode-island-can-begin-to-resist-rising-seas">recently turned into a bike path</a>. In Cranston, <a target="_blank" href="https://www.ecori.org/climate-change/2015/10/24/to-meet-rising-waters-homeowners-must-rise-up-or-get-out">over 20 homes in high-risk flood areas</a> have been purchased and demolished, an experiment in the controversial adaptation strategy known as managed retreat. Walking away from the things we love most isn’t easy, but it’s better than being forced.`
        },
        southCarolina: {
          key: 'southCarolina',
          number: 40,
          name: 'South Carolina',
          author: 'J. Drew Lanham',
          bio: 'J. Drew Lanham is a native of Edgefield and an alumni distinguished professor of wildlife ecology and master teacher at Clemson University.',
          text: `I have never left the plantation. I am a South Carolinian marooned on enslavement-tainted land. After growing up on property near where my ancestors worked cotton and cane, I left Edgefield—“Home of Ten [racist] Governors”—and went to school at Clemson University, built on the grounds of John C. Calhoun’s Fort Hill Plantation. Oddly enough, Benjamin Tillman—“<a target="_blank" href="http://historymatters.gmu.edu/d/55">Pitchfork Ben</a>” of Edgefield, rumored friend of the Lanhams, who owned my kin—helped found “Dear Ol’ Clemson” as a part of his run to populist political fame. See how this history seems to follow me? Tillman, the 84th governor of South Carolina, proudly claimed murder and violence as a “solution” to the “problem” of black political enfranchisement. What to do when a racist lynching advocate is a <a target="_blank" href="https://www.clemson.edu/about/history/bios/ben-tillman.html">celebrated founder of your school</a>? When the iconic central building of the school’s campus, where you now teach, bears his name? Protests and petitions go largely the way of the wind. It seems so “fiddle-dee-dee” to traditionalists, but is more painful to those whose ancestors bear the marks and memories of bondage and terrorism borne on the bloody reputations of those such as Ben Tillman. It’s now a part of the monumental debate over monuments to despots like Tillman, who are indeed a part of history but whose true stories are buried by genteel lies and whitewashed legend and sealed beneath carved stone and cast bronze. Want to leave the names and monuments standing? Then I want us to erect new monuments to tell the goddamned truth. All of it.`
        },
        southDakota: {
          key: 'southDakota',
          number: 41,
          name: 'South Dakota',
          author: 'Tasiyagnunpa Barondeau',
          bio: 'Tasiyagnunpa (Livermont) Barondeau is a journalist and an enrolled member of the Oglala Sioux Tribe, born on the Pine Ridge Indian Reservation to a Lakota rancher and an East River farmgirl.',
          text: `As corporate destruction threatens South Dakota and the Oceti Sakowin Oyate (Great Sioux Nation), a pipeline might hold the answer.
In Lakota legend, the Wakinyan saved the people from an enemy that gobbled up everything in its path. The Wakinyan, arriving as growling thunder and flashing lightning, can be destructive, the perfect match against such an enemy, and, indeed, they killed it. So how can a pipeline be both destructive and life saving?
When it’s filled with water.
For more than a decade, the Cheyenne River Sioux Tribe, whose land spans almost all of two South Dakota counties, has faced <a target="_blank" href="http://www.sdhda.org/housing-development-docs/housing-needs-study-program/1147-cheyenne-river-housing-authority-housing-study/file.html">a housing crisis</a> caused by a <a target="_blank" href="https://www.usda.gov/media/blog/2014/05/2/20-years-leadership-and-vision-tribal-water-project-heralds-new-opportunities">moratorium</a> on new water users, the result of an aging system that served an area the size of Connecticut.
When, on April 24th, 2014, in partnership with the tribe, Mni Was’te Water Company broke ground on the new water pipeline, shovels gleaming in the bright sun, two tribal councilmen started singing, while one struck a hand drum.
As the wind picked up and joined in, the elder of the two began to pray. In Lakota, he asked our non-human relatives to recognize the people’s need. We asked, but didn’t beg, confident our relatives understood. We could trust Unci Maka (Grandmother Earth) and the plant nations to make space for such crucial resources.
Imagine what could happen in the rest of South Dakota, and the United States of America, if we prudently planned for our true needs and petitioned the Earth itself as an involved partner.`
        },
        tennessee: {
          key: 'tennessee',
          number: 42,
          name: 'Tennessee',
          author: 'TJ Jarrett',
          bio: 'TJ Jarrett is a poet and software developer in Nashville and the author of Ain’t No Grave and Zion.',
          text: `We talk about shame a lot while we’re out on the loading dock smoking. We have good jobs and we make good money. We have done well for ourselves, but there’s so much shame these days to go around. It’s just the state of the world we’re living in. B always said that he thinks we are living through a set of unintended consequences. He says it, and he never listens when I tell him that the world they voted for is the world they wanted. He asks the same question to the air: How can the world go on like this?
Last October, <a target="_blank" href="https://www.tennessean.com/story/news/2017/11/01/white-lives-matter-shelbyville-rally-attendance-white-nationalist/819784001/
">the alt-right came through Shelbyville</a>, where B lives. While we waited for them to descend upon us, he kept saying that he couldn’t believe that it was happening. And he did that thing again where he would talk to the air while I asked: How could you not see this coming? Don’t you know they’ve been here forever? He’s a white man from East Tennessee. He’s not the only one wandering in disbelief. He’s not the only one who thinks that the shame is his alone to carry. Don’t you know, he said once, that I’m everything they think I am? My mother is strung out on drugs, my family is broke, and I feel like I’m drowning.
This is what I feel as a black woman most of the time; there’s always someone in need of saving. I say it over and over: This is the way it has always been. It comes upon us like weather because no one will claim to be the cause of it. And he keeps talking past me. He is unwilling even to share the air. And as the world falls around us, he will believe it falls hardest on him, even as my arms tremble from the weight.`
        },
        texas: {
          key: 'texas',
          number: 43,
          name: 'Texas',
          author: 'Roger Hodge',
          bio: 'Roger Hodge is deputy editor of The Intercept and author of Texas Blood: Seven Generations Among the Outlaws, Ranchers, Indians, Missionaries, Soldiers, and Smugglers of the Borderlands.',
          text: `The Rio Grande flows out of <a target="_blank" href="http://aconcagua.geol.usu.edu/~arlowry/RGR/faq.html">its rift valley</a> in the Rocky Mountains into Texas and assumes its geopolitical destiny at the precise point where Texas, New Mexico, and Chihuahua meet. From there, the river meanders for 1,255 miles through varied geographies of its own making to the Gulf of Mexico.
In the almost 500 years since the Spanish castaway Álvar Núñez Cabeza de Vaca wandered naked and barefoot through this rugged landscape, the communities clustered along the Rio Grande have suffered raids by Spanish slavers, invasions by the Apaches and Comanches, depredations by Anglo scalpers and Texas Rangers, conquest and reconquest and civil war.
All through those centuries of violence, a sense of common history and shared blood endured, binding border communities together. But today that bond is fraying. Not only physical walls, but psychological and other more corrosive virtual barriers have been raised along the U.S.-Mexico border.
The U.S. government has dropped an unprecedented surveillance net across the border country. Predator drones, tethered aerostats, seismic probes, radar towers, license-plate scanners, and long-range infrared cameras train their sensors on millions of American citizens who live within the border zone as they go about their daily business. The border has long been a testing ground for military technology. Today, the U.S. has embarked upon a massive experiment in “<a target="_blank" href="https://www.popsci.com/technology/article/2011-12/how-us-reengineering-homeland-security-borders#page-3">total domain awareness</a>”—the domestic application of military tactics to the civilian population. Total border security is a fantasy that can be achieved only via the oppressive illusion of total homeland security.`
        },
        utah: {
          key: 'utah',
          number: 44,
          name: 'Utah',
          author: 'Terry Tempest Williams',
          bio: 'Terry Tempest Williams stirred controversy in 2015 when she and her husband purchased BLM oil and gas leases as a conservation buyer. She is currently writer-in-residence at the Harvard Divinity School.',
          text: `The first tar-sands mine in the U.S. is already defunct, long before delivering its promised 2,000 barrels a day. U.S. Oil Sands, a company based in Canada, has walked away from the PR Spring mine in Utah’s remote Book Cliffs because it can’t pay its bills. Bankrupt. Another prospector’s dream in the desert has been foiled. Another legacy of land abuse laid bare. The Utah politicians who said yes, once again, to an irresponsible company engaged in irresponsible actions on public lands are bankrupt too, in the moral sense. All the while, activists camped across from PR Spring with Canyonlands National Park in view kept a steady drumbeat of climate justice alive with their chants of “Keep it in the ground.”
Farther south, Secretary of the Interior Ryan Zinke recommended radically reducing the size of the newly established Bears Ears National Monument, as well as Grand Staircase-Escalante National Monument, established in 1996. <a target="_blank" href="https://www.nytimes.com/2017/12/04/us/trump-bears-ears.html">Trump traveled to Utah on December 4th, 2017</a>, to announce that he would oblige—gutting Bears Ears by 85 percent and Grand Staircase-Escalante by half. The goal here is transparent: more oil and gas development and coal plants on these protected lands, regardless of the fact that these are the ancestral grounds of the Hopi, Navajo, Ute, Mountain Ute, and Zuni Nations, whose relatives’ bones are buried here.
The Trump administration, with the support of Senator Orrin Hatch, says that monument designation is “<a target="_blank" href="https://www.telluridenews.com/article_bea83ef4-89ed-11e7-9b99-9b9e4265b337.html">not the best use of the land</a>,” while the Utah Office of Tourism, with its slogan “Life Elevated,” beckons you to visit our state’s “five national parks, seven national monuments, five national forests, 43 state parks, and 22.8 million acres of public lands.” When thousands of Utahns gathered in Salt Lake City on December 2nd, 2017, at a citizens’ rally to protect our national monuments, one sign held high said: Beauty Is Its Own Natural Resource.`
        },
        vermont: {
          key: 'vermont',
          number: 45,
          name: 'Vermont',
          author: 'Bill McKibben',
          bio: 'Bill McKibben is the founder of 350.org and the author of numerous books, most recently Radio Free Vermont: A Fable of Resistance.',
          text: `Depending on the census, Vermont is always the <a target="_blank" href="https://www.citylab.com/equity/2016/12/a-complex-portrait-of-rural-america/509828/">first- or second-most rural state in the union</a>, with the fewest people living in a metropolitan area. And so white! Which, you would think, would make it quite happy to be in Trump’s America. Oddly, however, <a target="_blank" href="https://www.cbsnews.com/news/trump-v-clinton-what-the-popular-vote-in-each-state-shows-electoral-college/">the Donald did worse here than almost any place in the country</a>.
It’s not geography (New Hampshire, just across the Connecticut River, almost went Trump), and it’s not partisanship (we <a target="_blank" href="https://www.sevendaysvt.com/vermont/great-scott-liberal-vermont-elects-a-republican-governor/Content?oid=3811520">elected a moderate Republican governor that same night</a>—and he is a race car driver, so take that Mississippi). It’s culture, informed by history. Vermont is the state where town meeting is taken most seriously: <a target="_blank" href="https://www.timeanddate.com/holidays/us/town-meeting-day-vermont
">We govern ourselves in annual meetings</a> that every neighbor can attend, and most do. And so we know that making political progress requires not being an asshole. If someone like Donald Trump stood up at town meeting and began spouting off in that fashion, people would, literally, pay no attention. The second time he did it, they would murmur. Eventually someone would say, first privately and then publicly, that this was not how it’s done.
We fight for what we believe in, obviously—from Ethan Allen to Bernie Sanders. But when Sanders said, during his debate with Hillary Clinton, “Enough of the emails, let’s talk about the real issues facing America”—that was town meeting talking.
Vermont doesn’t do everything best—our cell service, for instance, would embarrass the average Mongolian. But we brew the planet’s best beer, and we do politics right. If you’re not civil, no one’s going to listen.`
        },
        virginia: {
          key: 'virginia',
          number: 46,
          name: 'Virgina',
          author: 'Amy Woolard',
          bio: 'Amy Woolard is a Legal Aid Justice Center attorney living in Charlottesville. Regina is The pseudonym of a client involved in her organization’s Drive Down the Debt campaign.',
          text: `Regina hasn’t had her driver’s license since 2011. When she wasn’t able to pay a court fine, her license was automatically suspended by Virginia law—indefinitely. Regina lost her children to foster care. The only way she can even dream of getting them back is if she completes a court-ordered drug program. The only way she can get to treatment is to drive. Six times now, she’s been stopped going to or from treatment and cited for driving on a suspended license. So far she’s spent about 30 days in jail for it. Each time, she racks up new court debt she can’t afford. Each time, she’s put back at day one in her treatment program, ever further away from reuniting with her kids.
This isn’t the <a target="_blank" href="https://psmag.com/social-justice/how-social-media-helped-organize-and-radicalize-americas-newest-white-supremacists">Charlottesville story</a> you might have been looking for. This isn’t about tiki torches or Confederate generals or two days of under-policing while a community is assaulted, but about years of over-policing low-income people of color in ways that don’t make headlines. A court fine sounds like one simple problem, but our clients at Legal Aid Justice Center can’t afford the upgrade. They don’t get the justice system where a credit card gets you same-day delivery. For our clients, one court fine is 12 problems. It’s losing your license when you have to drive to work, or the grocery store, or the doctor. It’s going to jail for driving anyway. It’s losing your job, your food stamps, your kids. It’s leaving jail with more debt waiting for you like quicksand.
There are fewer than six million drivers in Virginia, and nearly a <a target="_blank" href="http://reason.com/blog/2018/01/24/a-year-after-reforms-virginia-still-susp">million of them</a> have a suspended license for unpaid court debt. Justice shouldn’t be a commodity. Through class-action litigation and proposed legislation, we’re working to rewrite the law so our clients and the million others like them will have a chance to rewrite their stories. Until then, the endings are devastatingly predictable.
`
        },
        washington: {
          key: 'washington',
          number: 47,
          name: 'Washington',
          author: 'Brooke Jarvis',
          bio: 'Brooke Jarvis is a writer living in Seattle.',
          text: `Never mind that, geographically, you’re far closer to the state’s western edge than its eastern border. Once you’ve crossed the peaks of the Cascade mountains, leaving Seattle and the Puget Sound and the mossy forests behind you, colloquially speaking you’re in eastern Washington. Other divides, more on our minds, prevail.
If ever there was a tale of two states, this is it, and not just because one side of the mountains has firs and orcas and the other has ponderosa pines and endless grasslands. One has a <a target="_blank" href="https://www.thestranger.com/slog/2017/10/18/25477378/forbes-richest-americans-list-once-again-topped-by-seattle-billionaires">lot of billionaires</a> and the <a target="_blank" href="https://www.seattletimes.com/seattle-news/data/seattle-once-again-nations-fastest-growing-big-city-population-exceeds-700000/">fastest-growing city</a> in the nation and an exploding tech economy that other cities are currently begging to share (not to mention its shadow: sprawl and skyrocketing housing costs and a humanitarian crisis of homelessness). The other has wheat fields and agricultural workers, open spaces and tight-knit, struggling towns, a quarter the population in double the space. <a target="_blank" href="https://www.nytimes.com/elections/results/washington">One side mostly voted Trump</a>; the other has vowed to be his chief adversary. We call each other racist and ungrateful or condescending and foolish. People on both sides of the mountains speak, sometimes, about a dream of seceding from the other, each suspecting we could do better, be less tied down, become more ourselves, by striking out on our own.
The easy ways to describe a place are never either false or true. They’re both; they’re also exhausting. We see the obvious boundaries and reinforce them in our minds, but miss the gaping holes in them—the diversity of the east side, the hypocrisy of the west, the inevitability of our shared future—and the swirl of complication and confusion that makes a place real.
In the mountains this year, the snow is heavy. Our fractious, divided, shared government is sending plows up and down the roads that connect us, keeping them open.`
        },
        westVirginia: {
          key: 'westVirginia',
          number: 48,
          name: 'West Virginia',
          author: 'Brent Cunningham',
          bio: 'Brent Cunningham is managing editor of the Food & Environment Reporting Network.',
          text: `Some years back, one of my high school friends became a coal miner. He was well into his thirties, with a wife and kids, when he said he got tired of the restaurant business and decided to go underground. He wanted to put in an “honest day’s work.” I thought he was crazy. But we lived in different worlds by then—he not far from the West Virginia town where we grew up and me in New York. For a long time, I didn’t think much about it.
Then, in 2016, Don Blankenship, the former chief executive officer of Massey Energy, <a target="_blank" href="https://www.nytimes.com/2016/04/07/us/donald-blankenship-sentenced-to-a-year-in-prison-in-mine-safety-case.html">went to prison</a> for conspiring to violate mine-safety laws after an explosion in West Virginia killed 29 miners. Jail time for someone like Blankenship, one of the industry’s highest-paid executives, was unprecedented. It seemed the state might finally alter the tragic arc of its history, diversify its economy, and end its decades-long run on the wrong end of nearly every measure of prosperity. Coal now accounted for less than 3 percent of the state’s jobs; how could the industry survive such blatant disregard for its workers?
Then came Trump. He won nearly 70 percent of West Virginia’s vote by vowing to “bring back coal.” Even some industry executives admit that won’t happen. Done in by cheap natural gas and rising resistance to its ecological villainy, coal is never coming back. But for people like my friend, your time underground remains more than a job; it is an identity, the arbiter of an honest day’s work.
Meanwhile, Blankenship is out of prison—and <a target="_blank" href="https://www.npr.org/2018/01/20/579330266/out-of-prison-former-massey-ceo-don-blankenship-running-for-senator">running for Senate</a>. He has <a target="_blank" href="https://www.washingtonpost.com/news/post-nation/wp/2017/05/17/don-blankenship-asked-trump-to-oppose-legislation-for-harsher-punishment-for-coal-mine-supervisors/">asked Trump</a> for a review of the investigation into the Upper Big Branch explosion, hoping to exonerate himself and repeal the laws that hold executives accountable for health and safety violations in their mines. In West Virginia, coal mining is dying, but coal barons remain king.`
        },
        wisconsin: {
          key: 'wisconsin',
          number: 49,
          name: 'Wisconsin',
          author: 'Randy Bryce',
          bio: 'Randy Bryce is a union ironworker, U.S. Army veteran, and cancer survivor. He is running against Paul Ryan for Congress in Wisconsin’s 1st Congressional District.',
          text: `In southeast Wisconsin, Governor Scott Walker is giving a multibillion-dollar foreign corporate giant called Foxconn <a target="_blank" href="https://www.washingtonpost.com/news/wonk/wp/2017/09/18/scott-walker-signs-3-billion-foxconn-deal-in-wisconsin/">$3 billion of our hard-earned taxpayer dollars</a> to open a plant to manufacture LCD display panels for flat-screen televisions and other electronic devices. When you do the math, they’ll spend an estimated $230,000 for each job—jobs that don’t even pay half that to workers. Walker is also waiving environmental regulations on Foxconn, allowing it to dump waste directly into local wetlands. Did I mention that the founder of Foxconn is worth nearly $10 billion?
Those of us who work for a living are <a target="_blank" href="https://academic.oup.com/qje/article/131/2/519/2607097">constantly getting less and less</a>—while another billionaire gets more and more. And for those of us who have to budget out every doctor’s visit, grocery store purchase, and quarter tank of gas, that pinch hurts. Slowly, as everything gets a bit tougher, many of us withdraw from our communities. We worry about fighting with our neighbors over the scraps that remain. We shouldn’t have to accept an offer like the one given to Foxconn—which promises jobs only if it gets massive tax goodies handed to it, and only if it can pollute our lakes, rivers, and our own neighbors’ backyards.
We can do better. And we should have jobs for working people that are protected by unions. Because when we are united, we can bargain. My union guarantees me and my fellow ironworkers <a target="_blank" href="http://www.buildacea.org/wp-content/uploads/2015-2018-Ironworkers-Labor-Agreement.pdf">health insurance</a>. It negotiates for all of us, on average, 20 percent higher wages than non-union workers receive. And these dollars aren’t swindled from taxpayers in the form of corporate welfare. Our union members stand up for one another if the boss tries to take advantage of us. In a key way, they bring our community closer together by helping all of us succeed. And that’s a whole lot better than when the only winner is the foreign multibillion-dollar corporate behemoth.`
        },
        wyoming: {
          key: 'wyoming',
          number: 50,
          name: 'Wyoming',
          author: 'Nina McConigley',
          bio: 'Nina McConigley’s collection of short stories, Cowboys and East Indians, won the PEN Open Book Award.',
          text: `If you didn’t grow up in a rural state, it must be very hard not to regard us as a little backward. I grew up in Wyoming. My dad and many of my friends’ parents worked in the energy industry. Our class size depended on where oil prices stood. In a state where “BLM” means nothing about black lives mattering and is instead all about the Bureau of Land Management, the boom-and-bust cycles are a way of life. So we cheer when Environmental Protection Agency Administrator Scott Pruitt says, “The <a target="_blank" href="https://www.washingtonpost.com/news/energy-environment/wp/2017/10/09/pruitt-tells-coal-miners-he-will-repeal-power-plan-rule-tuesday-the-war-on-coal-is-over/">war on coal is over</a>.” But we also know: That’s a bit of a stretch. Coal isn’t coming back. It can’t.
Yes, we produce the energy that America consumes, but not only coal, oil, and gas. We’re also leaders in renewable energy like wind. Maybe a person in California or New York just can’t get that. Outsiders are hard on the energy industry and concerned about environmental impact. They see the Tetons and Yellowstone, and say, That land shouldn’t be touched! But they are less concerned with how closing mines or idling drilling rigs affects people’s lives. We must seem very far away.
It’s not that people in Wyoming don’t care about the environment. Plenty of people passionately do. Most hunters and ranchers are the best conservationists I know. What divides many here from the rest of America is the way we see environmental problems, climate change, and energy use. We understand how the energy market drives everything—from paving the roads to making sure that public schools stay open. Wyoming needs to diversify. Everyone agrees. But here in the least-populated state in the union, if we are going to make that change, we need someone to lend a hand, not just point the finger.`
        },
        districtOfColumbia: {
          key: 'districtOfColumbia',
          number: 51,
          name: 'District of Columbia',
          author: 'Ralph Nader',
          bio: 'Ralph Nader is a consumer advocate and author of the recent book Breaking Through Power: It’s Easier Than We Think.',
          text: `The nearly 700,000 residents of the District of Columbia know that “democracy delayed is democracy denied.” D.C. has been a colony with no real voting power in Congress, which knows little of local needs yet remains the District’s ultimate ruler. Congress <a target="_blank" href="http://dccouncil.us/pages/dc-home-rule">must approve the District’s budget</a>, and can override any actions of the city government. Members of Congress have <a target="_blank" href="https://www.cadc.uscourts.gov/internet/opinions.nsf/A866C40B942DDE4485256F82005D6F46/$file/02-5133a.txt">prevented the District</a> from taxing income earned by large numbers of commuting residents of Virginia and Maryland. Congress has, with impunity, often overturned the judgment of local elected officials and popular referenda on public health, tax, budget, and school issues.
Over <a target="_blank" href="https://www.dcboe.org/election_info/election_results/v3/2016/November-8-General-Election">78 percent</a> of the people in the District favor statehood. Poverty is rife. As is income and wealth inequality. District residents—maybe 500 of them—have engaged in protests and demonstrations, which have involved mayors, “shadow senators” like Jesse Jackson, a <a target="_blank" href="https://www.huffingtonpost.com/ben-zucker/hunger-strike-day-6-dc-ba_b_1146687.html">hunger strike</a>, and celebrities from outside D.C. Alas, to no avail. A statehood convocation in cavernous Constitution Hall only drew about 300 people in September of 2016. Well-to-do D.C. residents appear to not be bothered by their not having a voting representative and two senators, or they would fund a sustained movement for statehood.
D.C. citizens pay about <a target="_blank" href="https://www.washingtonpost.com/local/dc-politics/decades-long-effort-to-exempt-dc-residents-from-us-income-tax-still-simmers/2013/04/13/2b364794-a3b8-11e2-be47-b44febada3a8_story.html?utm_term=.602d3c714a4a">$3.9 billion</a> a year in federal income taxes—more than each of several states—and they have served and died in the armed forces. This prominent shame on America’s “democracy” should be met by ending the shame of those many passive D.C. residents and most of their corporate and political leaders who accept their disenfranchisement. It is time for Columbia, our 51st state.`
        },
        colonies: {
          key: 'colonies',
          number: 52,
          name: 'American Samoa, Guam, Puerto Rico, the Northern Mariana Islands & the U.S. Virgin Islands',
          author: 'Tiphanie Yanique',
          bio: 'Tiphanie Yanique is a novelist, short story writer, and poet from Saint Thomas, U.S. Virgin Islands. ',
          text: `The Insular United States is the official term for the U.S. territories. I’d rather call it the Liminal United States, after the intellectual idea of persons at a threshold. Insular doesn’t make sense anyway: These places are not insulated, are not culturally inward. In fact, quite the opposite. These places are located beyond the edges of the mainland, are more ethnically diverse than the mainland itself, and served—often continue to serve—as strategic locations for military positioning. For these same reasons, our lands were also understood to be expendable, and continue to be thought of as foreign territory. While our island-born forebears were dispossessed into their Americanness—their land became American without their consent—we are American by birth and by birthright.
But now, with many fatal attacks on U.S. soil coming not from the outside but from within, often by continental Americans themselves, we are somewhat released from our role as military outposts. We have become tourist destinations, a seemingly less sinister use of our land. And yet this new role has only clarified how foreign we are made to feel—as we perform exotica for our fellow countrymen. So now we are asking the radical questions: Who and what are we?
But liminal, remember. Artists like <a target="_blank" href="https://www.poetryfoundation.org/poets/craig-santos-perez">Craig Santos Perez</a>, poet of Unincorporated Territory, and myself, writer of Land of Love and Drowning, have begun to communicate to the nation and to our liminal compatriots that we are culturally profound within our regional and national contexts. A working group of Virgin Islands artists and scholars—made up of La Vaughn Belle, Tami Navarro, Hadiya Sewer, and myself—have begun to discuss collectively what it might mean to create a sustainable and dynamic dialogue about Virgin Islands identity within the conversation of U.S. liminality. In religious ritual, liminality is the space where a person is transformed into a more true self. Let’s do that.`
        }
      }
    }
  }
}
</script>

<style lang="scss">
@font-face {
  font-family: 'maritime';
  src: url('./assets/maritimechampion-bold-webfont.woff2') format('woff2'),
       url('./assets/maritimechampion-bold-webfont.woff') format('woff');
  font-weight: normal;
  font-style: normal;
}
@font-face {
  font-family: 'maritime-outline';
  src: url('./assets/maritimechampionsl-bold-webfont.woff2') format('woff2'),
       url('./assets/maritimechampionsl-bold-webfont.woff') format('woff');
  font-weight: normal;
  font-style: normal;
}
::-moz-selection { /* Code for Firefox */
    background: #bb4b34;
    color: #f6f4e5;
}
::selection {
    background: #bb4b34; 
    color: #f6f4e5;
}
body {
  background:#f6f4e4 url(./assets/66.png);
  color:#000203;
  font-size:14px;
  font-family:'proxima-nova';
  line-height:1.5;
  background-size:auto 240px;
  background-position:bottom -8rem center;
  padding-bottom:9rem;
  background-repeat:no-repeat;
}
*, *:before, *:after {
  margin: 0;
  padding: 0;
  max-width: 100%;
  box-sizing: border-box
}
h2 {
  font-family: 'maritime';
  font-size: 18px;
}
.links {
  padding:1rem;
  display:flex;
  align-items:flex-start;
  justify-content:space-between;
  width:100%;
  font-size:16px;
  @media (max-width:768px) {
    flex-direction:column
  }
  &__tenth {
    width:120px;
  }
}
.logo {
  height:20px;
}
strong {
  font-weight:800;
  text-transform:uppercase;
}
a {
  text-decoration:none;
  color:#000203;
}
.intro {
  padding:0 2rem;
  p, h2 {
    & + * {
      margin-top:1rem;
    }
  }
  h2 {
    margin:1rem 0;
  }
  width:960px;
  margin:0 auto 4rem;
  &__title {
    width:480px;
    margin:2rem auto 3rem;
    text-align:center;
  }
  &__content {
    display:flex;
    @media (max-width:768px) {
      flex-direction:column
    }
  }
  &__text {
    flex:0 0 50%;
    &:first-child {
      padding-right:2rem;
      @media (max-width:768px) {
        padding-right:0
      }
      img {
        margin-top:2rem;
        margin-bottom:2rem;
        width:240px;
      }
    }
    &:last-child {
      padding-left:2rem;
      @media (max-width:768px) {
        padding-left:0
      }
      img {
        margin-top:0;
        margin-bottom:2rem;
        width:400px;
      }
    }
    img {
      display:block;
      margin-left:auto;
      margin-right:auto;
    }
  }
}
blockquote {
  color:#BB4B34;
  font:20px 'merriweather', serif;
  border-top:2px dotted #BB4B34;
  border-bottom:4px solid #BB4B34;
  padding:1rem;
  margin-bottom:2rem;
  text-align:center;
}
.arrow {
  display:block;
  text-align:center;
  margin:2rem auto 2rem;
  height:24px;
}
.rotate {
  animation:rotateArrow 3s cubic-bezier(0.68, -0.55, 0.265, 1.55) forwards;
}
.rv {
  width:240px;
  transform:translateX(var(--tx));
  transition:transform .1s linear;
  will-change:transform;
  display:block;
  margin-left:auto;
  margin-right:auto;
  z-index:99;
  position:relative
}
.footer {
  margin-top:2rem;
  &__image {
    border-bottom:#000203 4px solid;
    padding:0 2rem;
    text-align:center;
  }
  &__content {
    width:640px;
    margin:2rem auto 0;
    text-align:center;
    padding:0 2rem;
  }
  &__nav {
    display:flex;
    align-items:center;
    justify-content:space-between;
    a {
      color:#bb4b34;
      font-weight:800;
    }
    @media (max-width:768px) {
      flex-direction:column;
    }
  }
  &__credit {
    margin:1rem 0 0;
    font-family:'merriweather', serif;
    font-weight:800;
    font-style:italic;
  }
  &__copyright {
    margin:1rem 0 0;
    opacity:.5;
  }
}
#myVideo {
  transition:margin-top 2s ease, opacity 2s ease;
  width:100%;
  background:url('./assets/postcards.png') center no-repeat;
  background-size:960px auto;
  @media (max-width:768px) {
    background-size:320px auto;
  }
}
@keyframes rotateArrow{
  0% {
    transform:rotate(0deg);
  }
  80% {
    transform:rotate(790deg);
  }
  99% {
    transform:rotate(817deg);
  }
  100% {
    transform:rotate(810deg);
  }
}
/* width */
::-webkit-scrollbar {
    width: 6px;
}
/* Track */
::-webkit-scrollbar-track {
    background:transparent; 
}
/* Handle */
::-webkit-scrollbar-thumb {
    background: #cbc9af; 
    border-radius:1000px;
}
/* Handle on hover */
::-webkit-scrollbar-thumb:hover {
    background: #cbc9af; 
}
</style>
