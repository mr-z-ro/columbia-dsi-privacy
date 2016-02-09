# Innovation and the Value of Privacy
In 1999, Scott McNealy, then CEO of Sun Microsystems, reportedly said “You have zero privacy anyway. Get over it.” Customers may value their privacy, but in practice they often give it or trade it away at low value. Companies are able to monetize the value of this information by aggregating and analyzing this information for their use, and by selling or trading it with third parties. 
 
On February 5th, 2016, the Data Science Institute and the Sanford C. Bernstein & Co. Center for Leadership and Ethics at Columbia University brought together business leaders with academics to discuss how businesses are incorporating privacy considerations into their business strategies. Industry leaders and entrepreneurs from frontier firms, including Microsoft, IBM, Deloitte, RedMorph and Dstillery, spoke on how they are changing the value of customer data and industry practices around privacy.

My notes follow, and the event webpage can be found [here](https://www8.gsb.columbia.edu/leadership/privacy).

## KEYNOTE
1. **[Kate Crawford](http://www.katecrawford.net/)** ([Microsoft Research NYC](http://research.microsoft.com/en-us/people/kate/), [MIT](https://civic.mit.edu/users/kate-crawford))
  
    A. Technology
    - Discussion of ML, [soft vs hard AI](http://blogs.wsj.com/cio/2015/01/16/soft-artificial-intelligence-is-suddenly-everywhere/)
    - In house products: [home robot](https://www.jibo.com/) launching in a couple of months
    - Only have about 5 years or less to figure out this balance between data and privacy while it's still moldable

    B. Privacy, Transparency, Accountability
    - Privacy not for its own sake but for implications: discrimination, health, etc
    - Only win by not playing? But can't choose to not play anymore
    - Opting out is gone. Not only like fb anymore where you consciously sign up to have data collected. 
    - Can partially opt out maybe [using clothing](https://ahprojects.com/projects/stealth-wear/), etc, but that's only for direct observation
    - We are exposing people to risk where there is no real threat model yet
    - Privacy alone (as we define it) is not enough
    - What about systems where even engineers don't understand dynamically evolving algos?

    C. Ethics
    - Fairness
    - Human autonomy vs machine autonomy
    - Power
    - Due Process

## RESEARCHERS
2. **[Roxana Geambasu](https://roxanageambasu.github.io/)** ([Columbia](http://www.cs.columbia.edu/~roxana/research/publications.html)): Ads
    - gmail ads: which emails trigger which ads?
    - brokers can tell when you're sick, tired, depressed, can sell that data
    - we're blind, including watchdogs
    - [Sunlight: Transparency for the Data-Driven web](http://columbia.github.com/sunlight)
    - reveals correlation of inputs with outputs based on observations from profiles with different inputs
    - gmail, amazon, youtube, most ads on arbitrary websites
    - many times results contradict privacy policies! (e.g. google targeting health, sexual orientation, gender, etc when they explicitly say they will not)

3. **[Arvind Narayanan](http://randomwalker.info/)** ([Princeton](https://www.cs.princeton.edu/people/profile/arvindn)): Dumpster Diving on the web: Why web privacy problem is transparancy problem
    - lots of info on websites coming from other sources than what we typed into the address bar, no transparency
    - [canvas fingerprinting](https://en.wikipedia.org/wiki/Canvas_fingerprinting): drawing invisible images to read it back and identify who you are
    - [addthis](http://www.addthis.com/) and [ligatus](https://www.ligatus.com/) started in 2012, Arvind's team later [released a paper](https://securehomes.esat.kuleuven.be/~gacar/persistent/index.html), the companies nearly immediately stopped
    - the measurement work (Arvind's research) **removed information asymmetry** between trackers and the rest of the web
      - not just users! sometimes even the websites don't know that they're including this
      - automated, large-scale measurements could provide this transparency
    - Created [OpenWPM](https://github.com/citp/OpenWPM) browser, measuring 1m measurements, will put out a paper on it
    - [Webtap](https://webtap.princeton.edu/) is another tool put out by Princeton

4. **[Deirdre Mulligan (Berkley)](http://www.ischool.berkeley.edu/people/faculty/deirdremulligan)**: Concepts of Privacy
    - "The morass of privacy"
    - privacy is typically narrowly defined as control over personal information, but there is a wide array (contextual integrity, intimacy, personhood, anti-totalitarianism, right to be let alone, etc)
    - we should not be focusing on identifying privacy precisely - **it is a living concept with frontiers/fringes at the edges**
    - "Which privacy are you talking about?"
    - case study: TSA scanners, "the naked machines"
      - gov't assumed ppl were concerned about data, but folks were actually concerned about exposure of the naked body
      - face blurring does not help that! the assumption that separating those who know who it is from what they look like naked is not enough!
      - [changed to the cartoon with boxes around risky areas, worked for a lot](https://www.law.cornell.edu/uscode/text/49/44901) (Congress allowed the TSA to
retain the scanners, but required a software update that
eliminated intrusive imaging)
      - women/men have different risk models so there are buttons for the guard to choose based on appearance, but transgender folks seen as anomalous and can be unfairly treated
      - risk model: whether to let your kid be scanned by a "naked machine" or grabbed during a body search? 
    - case study: facebook [emotional contagion study](http://www.pnas.org/content/111/24/8788)
      - facebook: well we didn't violate our privacy policy
      - users complaints were easily classified into 4 categories: 
        - decisional interference (you're messing with me)
        - misrepresentation/distortion (you're making me look different to my friends)
        - information loss (you're feeding me different info from my friends)
        - violation of expectations (this is not what i wanted fb to do)

5. Panel

## INDUSTRY
6. **[Brenda Dietrich (IBM fellow, VP Data Science)](https://www-03.ibm.com/ibm/history/witexhibit/wit_fellows_dietrich.html)**
    - not talking about privacy, but about what IBM is doing in their data products (have a chief privacy officer for the former piece)
    - value prop: get started faster, confidence and clarity, biased to action
      - 360 deg view of customer/enterprise relationship
    - methods: lookalikes, time/space boxes, network analysis, probabilistic paths, matching across multiple userids 
      - last one is less valuable because it is not contextual, we are different in different scenarios
    - use internal data, but also augment with external data (social media, competitive analysis, etc)
  
7. **[Claudia Perlich](https://sites.google.com/site/claudiaperlich/home)** ([Dstillery Chief Data Science](http://dstillery.com/leaders/claudia-perlich/), [NYU Stern](http://people.stern.nyu.edu/cperlich/))
    - data and privacy in digital advertising: "short trip to the belly of the beast"
    - if we're willing to live in a society that uses ads as a business model, what are we willing to do?
    - uses tracking cookies to gather data
    - agnostic predictive modeling, feature hashing
    - for ML, machine doesn't care what the axes are (doesn't need context)
      - don't care about "45yo, affluent male" - much better to directly watch behavior ("actions speak louder than demographics")
      - don't care about content of sites, just the urls (each axis can represent whether you've been to a site or not)
      - actually do not even need to know the URL! can hash into a code and tokenize
      - can map multiple urls to one code to protect actual data
    - she builds 10k models per week, and has no idea what they do
    - models will reflect biases in data
    - where's the line? things she doesn't do
      - no pii
      - stitching together cookies post deletion
      - device fingerprinting
      - optimizing for manupulation (not whether, but how to make you do something)
      - consistent person ID
  
8. **[Abhay Edlabadkar](http://www.bloomberg.com/research/stocks/private/person.asp?personId=50017992&privcapId=33348695&previousCapId=33348695&previousTitle=7Hills%20Business%20Solutions%20Ltd.)** ([RedMorph Founder](https://redmorph.com/about.html))
    - internet user has an implicit assumption to privacy
    - [2015 pew research: american attitudes on privacy](http://www.pewinternet.org/2015/05/20/americans-attitudes-about-privacy-security-and-surveillance/)
      - people don't do very much to block tracking
      - over 90% of people in US have a strong desire to control the information that's tracked about them
      - misleading websites claim user data is anonymized
      - can buy data on individuals from various orgs
      - employers using to screen candidates
        - China's sesame score
      - WE HAVE LOST CONTROL OF MOST OF OUR PERSONAL INFO
    - our data has become the currency of the internet
      - telcos, ad networks, anyone with data is rich
      - financial times has a calculator that will tell you how much your data is worth to data brokers
  
9. **Panel**
    - IBM has [chief privacy officer](http://www.cnet.com/news/ibm-appoints-chief-privacy-officer/)
    - Stereotypes and discrimination pollute models despite our best efforts, because they're inherent in human behavior
    - Customers ask how the algos work, answer is "we don't know, but it does!"
    - methods of good control aren't there!
    - how to navigate regulations?
      - information: 60-70% of germans use ad-blockers vs 20-30% in the US
      - government incentives: do not track laws, etc
    - [Deirdre's Book: "Privacy: in the books and on the ground"](http://scholarship.law.berkeley.edu/facpubs/1305/)

## KEYNOTES
10. **[Irfan Saif](https://twitter.com/irfansaif)** ([US Advisory Leader, Tech at Deloitte](http://www2.deloitte.com/us/en/profiles/isaif.html))
    - It's all about social
      - lots of metadata included
      - iphone records last known locations
        - many people the value outweighs the risk
    - Data as a currency
      - if i can get a game or service or added functionality (UX benefit) i may be willing to make concessions (adjust my definition of privacy)
    - Digital exhaust
      - things "giving off" data can be aggregated and correlated in ways that were not explicitly authorized by the subject
    - Analytics
    - Tools to Track
      - beacons, cameras, wifi/mobile networks
      - likes on fb, visits on the web
    - Tools to Protect
      - [Disconnect](https://disconnect.me/): understand trackers, control exposure, speed up the browsing experience
    - Managing Privacy
      - aboutthedata.com provided by axiom to allow users to manage what's known
      - data expiration and association with a context is very important to help manage it

11. **[Alondra Nelson](http://www.alondranelson.com/)** ([Columbia Dean of Social Science](http://sociology.columbia.edu/node/175))
    - Introduced Ashkan
  
12. **[Ashkan Soltani](http://ashkansoltani.org/)** (Independent Researcher, briefly an [advisor to White House OSTP](https://fcw.com/blogs/fcw-insider/2015/12/soltani-ostp-spinosa.aspx), pulitzer-prize team journalist at Washington Post ([1](https://en.wikipedia.org/wiki/Ashkan_Soltani#cite_note-WP13-4), [2](https://en.wikipedia.org/wiki/Ashkan_Soltani#cite_note-WP14-5), [3](https://en.wikipedia.org/wiki/Ashkan_Soltani#cite_note-WP16-6)) and WSJ)
    - Rebuttals
      - Rubuttal to "this privacy discussion causes fear, hopelessness"
        - the topic and discussion are young still, have only had these tools for not very long
      - Rebuttal to "we live in an immutable ad society"
        - this is not predetermined! there are actions to take
        - Different tradeoffs for different people
          - Folks on the poverty line don't have 
      - "This is legal, our lawyers have signed off, we don't know how it works"
        - not good enough. FAA with airplane safety as an example. Can define certain things that a system/tool should _not_ do.
        - people have taken gambling addiction self-disclosed data and marketed online gaming services to them
        - we need to make sure there are certain limits baked in
      - To read: [Paper from FTC on data discrimination](https://www.ftc.gov/system/files/documents/reports/big-data-tool-inclusion-or-exclusion-understanding-issues/160106big-data-rpt.pdf)
        - if you're discriminated against under certain factors, it's not good enough for the discriminator to say "well we didn't know our data was discriminating" or "the bias came from the data"
    - We are not doomed
      - Yes, privacy is amorphous, but there are attributes common across those definitions that we can get key insights from
      - **The Privacy Triangle:** three elements of the data to give a sense for privacy tradeoff/score in some way
        - **The data content itself.** e.g. Medical > Payments > Browsing
        - **The target of the data.** e.g. individual, group, name, address, field, class of people
        - **The audience for the data.** e.g. nuanced and dynamic definition of "public"
      - measure sensitivities in changes to one of the three pieces of the triangle
        - **"levers we can play with"** e.g. change the audience might mean we need to adjust the content or the subjects
    - Privacy is "information regret management"
    - the way to move forward is to agree to the direction we should go as opposed to accepting the status quo

## MATT'S THOUGHTS
- Data should live for a given time in a given context, then change states
- Machine Learning must have ethical heuristics baked in, since the measurement and use of the data affects the system, reinforcing biases or creating new ones.