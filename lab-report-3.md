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
-Input:
-Output:
## 2) `-p`
### Example 1:
### Example 2:
### Example 3:
## 3) `-X`
### Example 1:
`-X` will keep the contents of the file in the terminal after you quit the preview, which can be helpful if you are working in the terminal and do not want to have to switch between viewing the file and coding in the terminal. 
### Example 2:
As shown in this example, the contents of the file dafa;df;aev will stay in the terminal even after the key q is pressed.
### Example 3:
This command can become a useful shortcut to save time from calling `-less` repeatedly when you want to view the file.
