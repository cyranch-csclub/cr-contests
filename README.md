# Contests offered at Cypress Ranch HS Website

This is a site for all the contests offered at cypress ranch high school. To add contests, make a pull request.

Contests are located in [contests.yaml](data/contests.yaml), and structured as follows:

```yaml
key: # this doesn't really matter, is used for organization
  category: # this is the overall category of contest (type of contest, etc.). For example, UIL Mathematics, Science Olympiad, etc.
  contest: # this is the name of the actual contest.
  officialWebsite: # a link to the official page of the contest. OPTIONAL & can be left blank if only schoolwide.
  description: # a description of the contest.
  clubDesc: # this is description of the clubs that will administer the contest... contact points for anyone that wants to participate
    name: # name of the club
    website: ~ # OPTIONAL, the website of the club
    room: # room the club will meet
    meetTimes: # meeting times of the club
  teacher_sponsor: # the teacher sponsor of the club. if there are multiple, list only one
    name: # name of the sponsor
    email: # email of the sponsor
  interestForm: ~ # OPTIONAL, an interest form of the club. Will be displayed as a button with a link.
```

All fields except the ones marked as optional are required. Any field that is marked optional and null won't be displayed on the site. Any field that is required and is null will show `<Content Missing>` on the site.

Optional fields:

- `officialWebsite`
- `clubDesc.website`
- `interestForm`

An example structure:

```yaml
uil1:
  category: UIL Mathematics
  contest: Mathematics
  officialWebsite: https://www.uiltexas.org/academics/stem/mathematics
  description: > 
    A 40-minute, multiple-choice exam with 60 questions, 
    designed to test knowledge and understanding in Algebra I, 
    Geometry, Algebra II, Pre-calculus, AP Calculus (BC) and AP Statistics.
  clubDesc:
    name: Competitive Math Club
    website: ~
    room: B1178
    meetTimes: TBD
  teacher_sponsor:
    name: Bryce Hulett 
    email: bryce.hulett@cfisd.net
  interestForm: ~
```
