<h1 align="center">What if Bugzilla was made in 2015?</h2>

## Idea
Bugz.IO is a freemium service (B2C) and a deployable solution (B2B) based on Bugzilla, that provides a richer user experience on top of existing Bugzilla-deployments, with better mobility of access, saved searches, multiple profile sync, offline capabilities, extensibility, web-hooks, and crunches data to give the user a highly personalized infographics as dashboard.

## Assumptions
- Bugzilla is a feature-rich & powerful issue tracking system [[citation](http://en.wikipedia.org/wiki/Comparison_of_issue-tracking_systems)]
- Highest Bugzilla dropout is caused for its primitive, 90's web-interface
- Less capable alternatives are getting market, grossly because of just having a better UX
- Bugzilla accumulates a rich set of data over time
  - Making it difficult to move over to other solutions with all the history
  - The data is precious for creating infographics & generating insights
  - The data can also be used for various kinds of process management
- Bugzilla integrates well with code-review, continuous-integration and so forth

## Directions
### Goals
- Build **the** most effective & impressive user-experience for an issue tracking system
- Study the projected user-base for habitual & behavioral patterns to optimize the experience
- Deliver in small bursts, with gradual enhancements; doesn't need to be feature complete on day-0
- Consider Bandwidth, Flexibility, Integration, Minimalism, Performance to be of prime design parameters

### Non-Goals
- Do not set out to build Yet-Another-Project-Management-Tool (but don't fail, if used that way)
- Do not strategize how to stop people leaving Bugzilla; plan how to keep them with Bugzilla
- Do not prioritize implementing/augmenting non-Bugzilla (competitor's) features first

### Risks
- If our assumptions fail about: "users leave bugzilla because of sucky Web-UX"
- Any other organization comes in with the same plan & delivers faster
- We fail to implement OR promote the most effective Bugzilla UX 

### Challenges
- Find the UX balance between the makers & the managers
  - Sometimes there may not be a balance; fallback to prefs
  - Current UX best practices are generally drawn over the *average* userbase
  - Our targeted users are a subset on one side of the distribution, with different set of defaults
- Identifying the right infographics for the dashboard, which gives just enough information to be productive
- Integration with ElasticSearch, Gerrit, Jenkins & building such complex deployable containers

## Market Status
### Current State of Bugzilla
According to latest (2015/01/01) **[official data](https://www.bugzilla.org/installation-list/)** available, the number of publicly deployed Bugzilla deployments (of the organizations who wanted to be listed, hence not an exhaustive list) is 148. To quote the official source, “there are probably at least 10 times as many private ones” (~1500).

### Prospective User Base
Breaking down the State of Bugzilla information in three different sets (entity form factor) of two kinds (user tiers) of projections:

| Form Factor               | 20 Large Orgs  | 50 Medium Orgs | 500 Small Orgs |    Total    |
|:--------------------------|:--------------:|:--------------:|:--------------:|:-----------:|
| Prospective Free Users    |    500 each    |    50 each     |    10 each     |    13000    |
| Prospective Paid Users    |    100 each    |    20 each     |     1 each     |     3500    |

These figures are considering:
- Only the current usage share of Bugzilla, and no change over time
- Only the users with sufficient exposure to Bugzilla 
  - Users who spend more than 20min on bugzilla per day: free tier
  - Users who spend more than 50min on bugzilla per day: paid tier
- All Organizations/Employees (50%) aren’t ready to try or know about Bugz.IO
- The figures are projected only for the first six months to one year
- The figures are projected only for the Type 1 revenue source (explained next)

### Competitions
Bugzilla has competitors. Bugz.IO hasn't really got a direct competitor. There are other clients that connect to Bugzilla instances, but none of them are as a hosted/deployable service. The nearest competitor for Bugz.IO are:

- **[Deskzilla](http://almworks.com/deskzilla/overview.html)** [Commercial] - Desktop client with offline mode, time-tracking and custom workspaces. Has an IDE-like feel. Single-user license:  USD 189. Team license: USD 490 — $3,990
- **[Bugzi](http://www.getbugzi.com/)** [Commercial] - Android client for Bugzilla, with custom queries and multi-account handling. Development has apparently stopped. Pro version priced at about USD 7.
- **[BugDroid](https://play.google.com/store/apps/details?id=fr.julienvermet.bugdroid&hl=en)** - Android client for Bugzilla, with basic CRUD. Reported to not work smoothly.

The entire purpose of Bugz.IO is to work as the afterburner of Bugzilla (which is already a robust issue tracking platform, and formidable against the competition even with a primitive, web-only frontend client), and to give it more momentum against its competitors.

Here're some of the most catching up Bugzilla competitors:
- **[Bloodhound](http://bloodhound.apache.org/)**: Open source project, from Apache (Fork of Trac), thrives to make an easy to use, easy to deploy issue tracking tool
- **[GitHub Issues](https://guides.github.com/features/issues/)**: Integrated (not separately deployable) with GitHub, has high adoption rate globally (for good reasons)
- **[JIRA](https://www.atlassian.com/software/jira)**: Proprietary, free for selective cases, has high adoption rate among closed source projects
- **[YouTrack](http://www.jetbrains.com/youtrack/)**: Proprietary, free for 10 users, free for open source projects

## Revenue Model
### Revenue Sources
1. Monthly subscription model for end-users (focus, first 6 months)
2. Deployment, Hosting & Managing infra for organizations (focus, next 6 months)
3. Consult & give support for deployment to larger enterprises (focus, next 1 year)

### Expected Revenue
#### Type 1: Through User Subscriptions
Following is a revenue projection for the type 1 revenue source (user subscription). The the projection for the other sources are difficult, given they're dependent on Bugz.IO's promotions & reach in first 6 months.

If t is time (unit month), we have a linear increase of user base by the factor of m (with initial user c & total U paid users on the first month), charging Q amount each month from each of them for total n months, the revenue becomes:

![Formula of Expected Revenue from Revenue Source Type 1](http://i.imgur.com/yRxESoJ.gif "Formula of Expected Revenue from Revenue Source Type 1")

**From the data gathered, in our case having the parameters can be set to:** t ranging from 1-6 (6th to 12th month), U as 100 new paid users by the end of 1st month, m can be 2 (after 2nd month, 4 times the user than first month end, without counting initial users), c is 100 initial users, and Q is $10 per month.

<img align="right" src="http://i.imgur.com/LUB9uzx.gif" title="Revenue projection graph" alt="Revenue projection graph" />
The final amount is: $40000.

![Supporting summation over the assumed limits](http://i.imgur.com/MqkEltE.gif "Supporting summation over the assumed limits")

#### Type 2 & 3: As a Hosted Solution
We're holding the projections off for the type 2 & 3 revenue model (managed on Bugz.IO cloud or privately hosted) till we have more data & the prospective penetration paths of Bugz.IO. These deployments will have bulk licenses.

The KPIs are:
- Number of private hosted deployments at any instance
- Number of active private hosted deployments at any instance
- Number of users per private hosted deployments on an average
- Percentage of private hosted deployments running beyond 6 months
- Number of organizations moving from other issue tracking system to Bugz.IO
- Number of new private hosted deployments registered organically through our website
- Percentage of user conversion from freemiup subscription to organization cloud instance

## Projected Expenses
| Expense Type | Break ups                                                     | Monthly Total |   Sub Total |
|:-------------|:--------------------------------------------------------------|--------------:|------------:|
| Salaries     | 4xFull Time @ INR50K<br>2xInterns @ INR10K                    |       INR220K |    INR1320K |
| Test Devices | iDevices @ INR100K<br>Droids @ INR100K<br>Notebooks @ INR300K |           N/A |     INR500K |
| IT & Infra   | Office Rent @ INR5K<br>Services @ INR10K<br>Server @ INR10K   |        INR25K |     INR150K |
| Gross Total  | Covering all expenses; 10-20% estimation bleed possible       |       INR245K |    INR1970K |

The gross total of INR1970K is approximately USD32K. This is the projection for the time until the first public version of the service is ready. Going forward, the estimation will differ in facets & scale, while the service will also start generating revenue.

## Projected Timeline
|    Timeline    |    Release     |    Expense         |    Revenue^    |   Users^          |
|:---------------|:--------------:|-------------------:|---------------:|------------------:|
| **1 Month**    | PoC            |            INR372K |             $0 |                10 |
| **2 Month**    | ---            |            INR385K |             $0 |                10 |
| **3 Month**    | Alpha          |            INR377K |             $0 |               100 |
| **4 Month**    | Beta           |            INR245K |             $0 |               500 |
| **5 Month**    | ---            |            INR245K |             $0 |               500 |
| **6 Month**    | v1.0           |            INR245K |           $10K |             1,000 |
| **1 Year**     | v2.0           |            ------- |           $40K |             4,000 |

^ Based on users of the public hosted instance on Bugz.IO only. This does not include projections of private hosted deployments or on-premise deployments of Bugz.

### Monthly Expense Breakups
|    Month    |    Devices     |  Salaries  |   IT/Infra  |   Total   |
|:------------|---------------:|-----------:|------------:|----------:|
|     1st     |        INR140K |    INR220K |      INR12K |   INR372K |
|     2nd     |        INR140K |    INR220K |      INR25K |   INR385K |
|     3rd     |        INR140K |    INR220K |      INR37K |   INR377K |
|     4th     |            --- |    INR220K |  INR25+50K* |   INR245K |
|     5th     |            --- |    INR220K |  INR25+50K* |   INR245K |
|     6th     |            --- |    INR220K |  INR25+50K* |   INR245K |
* INR50K is the expense for running the ElasticSearch instance.

![Expenditure Milestones](http://i.imgur.com/4OZNN8P.png "Expenditure Milestones")

#### PoC [Month 1]
- Identify tools of trade
- Build wrapper lib to abstract REST & RPC
- Proof of concept app with required features
- Identifying development pain-points & priorities

#### Alpha [Month 3]
- Design info-dash & the app IA
- UX prototype with preset defaults
- Branding and aesthetics iterations
- Web portal for profiles & prep for PR

#### Beta [Month 4]
- User-testing & studies
- Introduce user preferences
- Tuning & reworking the defaults
- Marketing push, local/global publicity

#### v1.0 [Month 6]
- Multiple profiles
- Realtime conversation
- Synchronize user-preferences
- Special early-bird discounted subscription
- Preset config for popular/public Bugzilla instances

#### v2.0 [Month 12]
- Introduce extensions & hooks
- Integration with peer-platforms
- Start targeting for BZ bounce-backs
- Pitch & engage Start Ups & Enterprises
