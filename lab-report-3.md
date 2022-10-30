# Lab Report 3
The command I focused on was ```less```.
## 1) ```-N```
### Example 1:
The command ```-N``` displays the number of each line on the left-hand side of the preview of the file in the terminal. It can be useful when wanting to find a certain line or reference a certain part in the file. 

-Input:
```
czhang@Catherines-MBP skill-demo1 % less -N ./technical/government/Media/Annual_Fee.txt
```
-Output:
```
      1 
      2 
      3 
      4 
      5 Annual Fee to Rise $49; Legal Aid Gets Boost
      6 
      7 John Flynn Rooney
      8 October 4, 2002
      9 The Illinois Supreme Court on Friday hiked attorney registration
     10 fees by $49 a year to boost both legal aid services and support for
     11 lawyers with drug and alcohol problems. Under the high court's
     12 order, the base annual fee for active lawyers rises to $229 as of
     13 Jan. 1. Last year, the high court raised that fee to $180 from
     14 $140. Lawyers in their first three years of practice or who are
     15 inactive but wish to remain on the roll of attorneys pay $90.
     16 Most of the latest increase -- $42 -- will go to the Lawyers
     17 Trust Fund of Illinois, which disburses monies to legal aid
     18 organizations that assist low- income residents in civil matters.
     19 The other $7 will go the Lawyers' Assistance Program Inc., which
     20 helps lawyers overcome drug or alcohol addiction and mental
     21 illness.
     22 The Lawyers Trust Fund and LAP aim, respectively, to improve
```
### Example 2:
The lines are numbered from top to bottom, with the first line being labeled with 1. Lines that are just blank space are also counted. 

-Input:
```
czhang@Catherines-MBP skill-demo1 % less -N ./technical/plos/pmed.0020035.txt
```
-Output:
```
      1 
      2   
      3     
      4       
      5         
      6         In 1997, United States President Bill Clinton announced the challenge to develop an AIDS
      7         vaccine by 2007. Since 1997, the AIDS Vaccine Advocacy Coalition (AVAC) has published
      8         annual reports on the global status of the effort to meet Clinton's deadline. Last year's
      9         report, entitled “AIDS Vaccine Trials—Getting the Global House in Order,” officially ends
     10         the countdown. Saying that “we are on a long term mission,” AVAC concludes that there will
     11         not be a safe and efficient vaccine in 2007, and that we need to “focus on the long haul
     12         and set an agenda for sustained and sustainable action that stretches well beyond 2007.” It
     13         is not that there are no vaccine candidates in clinical trials, but there is little hope
     14         that any of the current candidates will turn out to be a cheap and safe vaccine that
     15         affords long-term protection.
     16         Among notable developments over the past 12 months, the AVAC report highlights the
     17         Global HIV/AIDS Vaccine Enterprise as an effort to improve coordination within the AIDS
     18         vaccine field. The Enterprise was announced in June 2003 and now shares its scientific
     19         strategic plan with everyone affected by the AIDS pandemic—that is, all of us—by publishing
     20         it in 
     21         PLoS Medicine (DOI: 10.1371/journal.pmed.0020025).
     22         In its plan the Enterprise presents itself as a global endeavor and emphasizes the need
     23         for integration and capacity building around the world. It is not “a discrete organization
     24         with a pool of money” but a “coordinating group of individual funding agencies that will
     25         support specific areas of research using their own mechanisms, according to their own
     26         practices and policies, and following the Enterprise's principles.” These principles
     27         include collaboration, standardization, and coordination among international researchers
     28         and agencies. The plan focuses on specific scientific roadblocks that need to be overcome,
     29         but also looks ahead and mentions the need to build capacity for product manufacturing and
     30         clinical trials, and to address regulatory issues.
     31         These are noble goals, and the fact that they are stipulated jointly by many of the
     32         leaders in the field will generate excitement and expectations, even though much of what is
```
### Example 3:
Once previewing the file, you can also type the line number + `g` to skip to that line in the file, which is a helpful tool when used in combination with the `-N` command.

-Input:

-Output:
## 2) `-p`
### Example 1:
Using `-p` allows you to skip to a certain "pattern" or String phrase in the file in the preview menu. It is similar to Command + F on Mac.
*Note: I needed to use screenshots instead of codeblocks to properly show the effects of the command in that it highlights words in the file

-Input:
```
czhang@Catherines-MBP skill-demo1 % less -pasthma ./technical/plos/pmed.0010008.txt
```

- Output:

### Example 2:
The String typed after the ```-p``` will be highlighted in the preview of the file in the terminal.

-Input:

-Output:

### Example 3:
## 3) `-X`
### Example 1:
`-X` will keep the contents of the file in the terminal after you quit the preview, which can be helpful if you are working in the terminal and do not want to have to switch between viewing the file and coding in the terminal. 

-Input:
`czhang@Catherines-MBP skill-demo1 % less -X ./technical/plos/journal.pbio.0020019.txt`

-Output: after pressing the key q
```
  
    
      
        
        Individuals within a wild population show remarkably little morphological variation,
        given the amount of environmental variation they encounter during development and the
        amount of genetic variation within the population. This phenotypic constancy led to the
        proposal that individuals were somehow buffered, or canalized, against genetic and
        environmental variation (Waddington 1942). Clearly, such a mechanism would have important
        evolutionary consequences; because natural selection acts upon phenotypic variation within
czhang@Catherines-MBP skill-demo1 % 
```
### Example 2:
As shown in this example, the contents of the file Cohenetal_comparison.txt will stay in the terminal even after the key q is pressed. The terminal prints as far as you scrolled in the file, so it may not print the complete file.

-Input:
```
czhang@Catherines-MBP skill-demo1 % less -X ./technical/government/Post_Rate_Comm/Cohenetal_comparison.txt
```

-Output: after pressing the key q
```




A Comparison of the Burden of Universal Service in Italy
*
./technical/government/Post_Rate_Comm/Cohenetal_comparison.txt...skipping...




A Comparison of the Burden of Universal Service in Italy
*


and the United States
Robert Cohen Rossana Scocchera
Postal Rate Commission Poste Italiane
Carla Pace Vincenzo Visco Comandini
Poste Italiane Poste Italiane
Matthew Robinson John Waller
Postal Rate Commission Postal Rate Commission
Gennaro Scarfiglieri Spyros Xenakis
Poste Italiane Postal Rate Commission




A Comparison of the Burden of Universal Service in Italy
*


and the United States
Robert Cohen Rossana Scocchera
Postal Rate Commission Poste Italiane
Carla Pace Vincenzo Visco Comandini
Poste Italiane Poste Italiane
Matthew Robinson John Waller
Postal Rate Commission Postal Rate Commission
Gennaro Scarfiglieri Spyros Xenakis
Poste Italiane Postal Rate Commission

:...skipping...




A Comparison of the Burden of Universal Service in Italy
*


and the United States
Robert Cohen Rossana Scocchera
Postal Rate Commission Poste Italiane
Carla Pace Vincenzo Visco Comandini
Poste Italiane Poste Italiane
Matthew Robinson John Waller
Postal Rate Commission Postal Rate Commission
Gennaro Scarfiglieri Spyros Xenakis
Poste Italiane Postal Rate Commission

1. INTRODUCTION
Samuel Johnson said Patriotism is the last refuge of a scoundrel
and many postal observers believe that the Universal Service
Obligation (USO) is the last refuge of a postal service wishing to
protect inefficiency, monopoly profits, or economic rents. Despite
inefficient service, opaque accounts, and large rents, many postal
officials maintain that the monopoly, whatever its faults, is the
only means of ensuring universal, affordable postal service for
citizens throughout the nation. Without the monopoly, they argue,
the post office would be crushed by the cost of the USO. This paper
examines when this argument might be valid.
All posts probably have some cost associated with the USO, but
it has been difficult to quantify. We agree with John Panzar (2001)
that the cost of the USO is the cost of the services that would not
be provided in a competitive market. Under this definition, in
practice, there has been no discernable USO cost. Competition
exists in both Sweden and New Zealand and the incumbent posts have
continued to provide universal service with no subsidy.
The USO as defined by the proponents of the monopoly goes well
beyond ubiquitous service. It also includes a uniform price with
respect to location of the recipient1 and a uniform frequency of
delivery. These conditions might have been appropriate a century
ago when the post was the primary means of communication. Today
however, this definition seems unduly restrictive. It is incumbent
on defenders of the restrictive definition of USO to explain why
postal service should be treated
*
The views expressed in this paper are those of the authors and
do not necessarily represent the opinions of Poste Italiane or the
Postal Rate Commission.
In other words a firm cannot charge more for delivering similar
items to addresses in one section of the country than another.
Under this definition United Parcel Service (UPS) is not a true
universal service provider because it imposes a surcharge for
residential delivery. This is ironic because UPS delivers to every
address in the continental U.S. and delivers right to the door. The
Postal Service which is a universal service provider under the
definition used here, delivers to mail boxes that are, in many
cases, remote from the actual address.
differently from other important products such as groceries,
bank accounts and internet service.2 Notwithstanding, we use this
restrictive definition of universal service for this paper.
The obligation to provide ubiquitous service is not in itself
onerous. It has been pointed out by the American co-authors of this
paper that a post could rationalize its delivery costs by reducing
the frequency of service on unprofitable routes to the point where
they become profitable (Cohen et al. 2000). A post could also
rationalize its prices by reflecting the cost of service to
different areas. The restrictive definition of the USO does not
allow a post to rationalize either its cost or pricing structure,3
thus, creating cream-skimming opportunities under liberalization.
The burden that the restrictive USO imposes on a post is the
increase in its unit costs resulting from cream skimming under
liberalization caused by the requirements of uniform pricing and
levels of service. We use the term "burden of the USO" to
distinguish our concept from other papers that use the term "cost
of the USO."
We believe that insights into the burden of the USO can be
gained by comparing postal systems. Assuming that the keenest
insights can be gained by comparing systems with large differences,
the Italian and United States systems are good candidates. The
U.S. has the highest volume per capita in the industrial world
(739 pieces in 1999), while Italy has one of the lowest (115 pieces
in 1999).4
Previous work by Cohen et al. shows that the U.S. Postal Service
(USPS) is not likely to require the monopoly to continue to satisfy
the USO. (Cohen 1999, 2000) However, this result may not apply to
all posts and it is important to distinguish magnitudes of burden
for different posts. To this end, we develop a model to determine
the USO burden for posts with different per capita volumes. In
particular, applying the model demonstrates that the burden of USO
is very great for Poste Italiane and other posts with small per
capita volumes. On the other hand, for the U.S. and other posts
with large and medium per capita volumes the burden is small.
We first compare some statistics for Italy and the U.S. We then
examine the consequences of volume loss on postal systems in order
to provide a measure of burden in terms of increases in average
unit costs as volume is lost to competitors, or
2
Many postal services are increasingly becoming primarily
carriers of advertising. U.S. households receive far more
advertising than letters, bills or other similar matter. According
to the Household Diary Study (United States Postal Service 2000),
in 1999, 56 percent of the pieces received by U.S. households were
advertising mail.
3
An apparent exception is Consignia. It rationalizes its delivery
cost by delivering twice a day in most urban areas and once a day
in rural areas.
4
Italy has a very undeveloped direct mail market and the Italian
monopoly does not include direct mail. The
U.S. monopoly includes all addressed direct mail consisting of
fewer than 24 pages. The U.S. Postal Service handled 314 pieces per
capita of direct mail in 1999.
equivalently, the increase in average rates for the volume
remaining.5 Next we introduce the concept of delivery route profit
and quantify the relative profits from delivered mail and mail not
requiring delivery in both Italy and the U.S. We then compare the
distribution of profit margins for routes in Italy and the U.S. and
the effect this has on vulnerability to cream skimming. Finally, we
discuss two measures of the cost of universal service, the entry
pricing measure and the net avoided cost measure in the context of
delivery profits. We compare them with our burden measure for the
Poste Italiane and the U.S. Postal Service.
Our principal findings are:
The burden of the USO is much greater for small per capita
volume posts than it is for large and medium per capita volume
posts.
The likelihood of a graveyard spiral resulting from volume loss
to cream skimmers is remote for medium to large volume per capita
posts; whereas it is a real threat to small volume per capita
posts.
The measure of burden presented here combined with the
czhang@Catherines-MBP skill-demo1 % 
```

### Example 3:
This command can become a useful shortcut to save time from calling `-less` repeatedly when you need to view and reference the file, while still typing commands in the terminal.

-Input:
```
czhang@Catherines-MBP skill-demo1 % less -X ./technical/911report/chapter-13.1.txt
```
-Output: after pressing the key q
```

    
        
            HOW TO DO IT? A DIFFERENT WAY OF ORGANIZING THE GOVERNMENT
            As presently configured, the national security institutions of the U.S. government
                are still the institutions constructed to win the Cold War. The United States
                confronts a very different world today. Instead of facing a few very dangerous
                adversaries, the United States confronts a number of less visible challenges that
                surpass the boundaries of traditional nation-states and call for quick, imaginative,
                and agile responses.
            The men and women of the World War II generation rose to the challenges of the 1940s
                and 1950s. They restructured the government so that it could protect the country.
                That is now the job of the generation that experienced 9/11. Those attacks showed,
                emphatically, that ways of doing business rooted in a different era are just not
                good enough. Americans should not settle for incremental, ad hoc adjustments to a
                system designed generations ago for a world that no longer exists.
            We recommend significant changes in the organization of the government. We know that
                the quality of the people is more important than the quality of the wiring diagrams.
                Some of the saddest aspects of the 9/11 story are the outstanding efforts of so many
                individual officials straining, often without success, against the boundaries of the
                possible. Good people can overcome bad structures. They should not have to.
            The United States has the resources and the people. The government should combine
                them more effectively, achieving unity of effort. We offer five major
                recommendations to do that:
            
                unifying strategic intelligence and operational planning against Islamist
                    terrorists across the foreign-domestic divide with a National Counterterrorism
                    Center;
                unifying the intelligence community with a new National Intelligence Director;
                unifying the many participants in the counterterrorism effort and their
                    knowledge in a network-based information-sharing system that transcends
                    traditional governmental boundaries;
                unifying and strengthening congressional oversight to improve quality and
                    accountability; and
                strengthening the FBI and homeland defenders.
            
            UNITY OF EFFORT ACROSS THE FOREIGN-DOMESTIC DIVIDE
            Joint Action
            Much of the public commentary about the 9/11 attacks has dealt with "lost
                opportunities,"some of which we reviewed in chapter 11. These are often
                characterized as problems of "watchlisting," of "information sharing," or of
                "connecting the dots." In chapter 11 we explained that these labels are too narrow.
                They describe the symptoms, not the disease.
            In each of our examples, no one was firmly in charge of managing the case and able to
                confronts a very different world today. Instead of facing a few very dangerous
                adversaries, the United States confronts a number of less visible challenges that
                surpass the boundaries of traditional nation-states and call for quick, imaginative,
                and agile responses.
            The men and women of the World War II generation rose to the challenges of the 1940s
                and 1950s. They restructured the government so that it could protect the country.
                That is now the job of the generation that experienced 9/11. Those attacks showed,
                emphatically, that ways of doing business rooted in a different era are just not
                good enough. Americans should not settle for incremental, ad hoc adjustments to a
                system designed generations ago for a world that no longer exists.
            We recommend significant changes in the organization of the government. We know that
                the quality of the people is more important than the quality of the wiring diagrams.
                Some of the saddest aspects of the 9/11 story are the outstanding efforts of so many
                individual officials straining, often without success, against the boundaries of the
                possible. Good people can overcome bad structures. They should not have to.
            The United States has the resources and the people. The government should combine
                them more effectively, achieving unity of effort. We offer five major
                recommendations to do that:
            
                unifying strategic intelligence and operational planning against Islamist
                    terrorists across the foreign-domestic divide with a National Counterterrorism
                    Center;
                unifying the intelligence community with a new National Intelligence Director;
                unifying the many participants in the counterterrorism effort and their
                    knowledge in a network-based information-sharing system that transcends
                    traditional governmental boundaries;
                unifying and strengthening congressional oversight to improve quality and
czhang@Catherines-MBP skill-demo1 % 
```
