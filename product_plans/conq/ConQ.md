# ConQ

## Idea

### TL;DR

ConQ's aim is to provide a threaded, real-time, contextual
audio/video/textual discussion, which can be annotated, archived and
revisited later. It'll allow participants to ask, up/downvote
questions, that can be moderated, without interrupting the speaker –
across form factors, using web as the platform.

ConQ is a selective mashup between Skype, Hangouts, Discourse &
StackExchange; made entirely with web-technology that works across
platforms.

### Problem statement

#### Synopsis

Most audio/video conferencing systems at the moment, including the
web-based ones
[[see list](http://www.webrtcworld.com/webrtc-list.aspx)] are geared
towards having an audio/video chat. But the actual discussion tends to
get lost. Usually, only a handful people end up actively participating
in the meeting. The rest of the attendees often remain passive, for
the lack of a better non-interrupting participation model, even though
they might have interesting inputs.

Usually, conferences/meetings like these use a separate real-time text
chat platform (seldom integrated) to take in questions from
attendees. But, even then, there is no scope of contextual & threaded
discussion on a particular topic or concern raised by a participant.

#### The discussion barrier

The problem that we've identified here, are:

- There is no reliable way to put forward a question or an argument during the call without interrupting the current speaker.
- Neither is there an integrated participator-voting based ranking & a threaded discussion platform for the raised questions.
- There is no way for other participants to know what one participant has in mind before that participant speaks it out - which either interrupts the speaker, forks the thread of discussion or is pushed to the end of the speech.
- Usually the chance of a question that will be asked, has a 50-50 chance of being non-relevant/non-desired considering the time-constraints. Sometimes relevant questions are left unanswered for wasting time on comparatively less important one.
- After the conference is over, there's rarely an archive available for the same. Usually there are meeting notes taken; but that's nowhere close to the full audio-video with the threaded discussion as an accessible & retrievable archive.

That is where ConQ comes in.

#### Why ConQ?

The name "ConQ" is derived from "Conference & Questions". It aims to
provide an integrated audio/video/textual discussion platform in a web
browser, for desktops and handhelds, where participants can vote,
discuss and talk. ConQ's aim is to keep meetings within their allotted
times; efficiently.

In simple words, **ConQ is a selective mashup between Skype, Hangouts, Discourse & StackExchange; made entirely with web-technology that works across platforms**.

## Team

- [Kaustav Das Modak](https://www.linkedin.com/in/kaustavdm)
- [Soumya Deb](http://in.linkedin.com/in/skdeb)

-------

## Directions

### Goals

- Build a mash-up of discussion platforms like Reddit/StackOverflow and video/audio chatting platforms like Skype/Hangouts.
- Build a UX that will allow smooth discussions even while video chatting. i.e., remove the need of opening a separate text chat program while having a video call.
- Remove the need of any native client. The browser should be able to handle it all.
- Focus on making healthier discussions. Not just one-to-one video chatting.
- Focus on getting large groups discussing together. For example, Skype or Hangouts allow limited number of people per call, which can be broken by using WebRTC as technology base.

### Non-goals

- Do not build yet-another-WebRTC-based-video-chat.
- Do not compete Skype. Instead, imagine how StackOverflow would have been if it had a video chat embedded per question.
- Do not focus on having all the features of any existing video chat platform, e.g. file-sharing, emojis etc. Instead, focus strongly on getting the discussion part right.
- Do not bloat the platform with unnecessary features. Keep it lean. Make it do one thing -- discussions. And do it well.

### Risks

- If someone else launches with the same idea before we do. Given the fact that a lot of people are working on WebRTC, an early advantage and an early product launch is very crucial for us.
- If a larger organization, say Google or Skype, with a way-way-way larger engineering and marketing bandwidth incorporates the same discussion type features in their already-popular products after ConQ is launched, they will still manage to get a lot of wind, essentially getting us subdued. So, we need to spread this in media as widely as possible.

### Challenges

- ~~Implementing a positive UX pattern for ConQ that users will feel comfortable with.~~
- ~~Server bandwidth and memory requirements will be very high. Coping with scale will be an interesting DevOps challenge, but can get a good amount of dollars out of our pockets as infrastructure costs.~~
- Doing proper marketing given our limited bandwidth. We need to get covered by popular tech publications to be able to get noticed by the larger media.

----


## Market Status

### Prospective user base

- One-on-one video chat
- Meetings where at least 4 people join in on a video call.
- Live webinars.
- Implementation at physical conferences where speaker talks are broadcasted and the audience can interact worldwide, listening on them. Think of YouTube live + Stackoverflow in real-time, mashed up in one package.

### Competitions

If we count the list of other products that provide in-browser video/audio chat, the list will grow pretty big. However, *none* of them have tried to solve the discussion issue that we are trying to solve with ConQ. Here is a list of the prominent players, who can still be considered as a competition to ConQ given there pre-existing market spread, even though they don't solve the same problem.

#### Global

- [Appear.in](http://appear.in) - WebRTC based chat. Incubated by Telenor. One of the earliest players in this segment.
- [Join.me](http://join.me) - They are primarily focused on the B2B segment, making meetings more efficient with screen-sharing. Can run in browser, but *not* based on WebRTC.
- Skype's WebRTC
- [TokBox](https://tokbox.com/) - Platform to allow WebRTC based communications in-app. Not a direct competitor, but can potentially raise many more competitors by lowering the barrier of entry in the WebRTC-based real-time chat segment.
- [XirSys](http://xirsys.com) - Hosted WebRTC API for other apps. Has similar effect as TokBox.

#### India

- [Tringgr](http://tringgr.com/) - WebRTC based group chat solution, one of the first ones from India. Pluggable into 3rd party apps. Looks more like a multi-people supporting Firefox Hello at the moment.

#### Other video chats on WebRTC

- [vLine](https://vline.com/)
- [Talky](https://talky.io/)
- Most of the list mentioned in the [WebRTC Listing by WebRTC World](http://www.webrtcworld.com/webrtc-list.aspx).

## Revenue Model

### Phase 1:

- It will start as a freemium hosted service, where anyone can log in and start a video call.
- Users can use the service for free, but pay for premium features, e.g. more than certain amount of people per conference, annotated conference archiving, web service integrations etc.

### Phase 2:

- Allow private hosted deployments and on-premise deployments for companies.
- Pricing will be be based on number of licenses.

----


## Projected Expenses

### Till v1

| Expense Type | Break ups                                                     | Monthly Total |   Sub Total |
|:-------------|:--------------------------------------------------------------|--------------:|------------:|
| Salaries     | 6xFull Time @ INR80K<br>2xInterns @ INR20K                    |       INR520K |    INR6240K |
| Test Devices | iDevices @ INR140K<br>Droids @ INR100K<br>Notebooks @ INR960K |           N/A |    INR1200K |
| IT & Infra   | Office @ INR72K<br>Servers @ INR230K                          |       INR302K |    INR3624K |
| --           | --                                                            | *Gross total* |   INR11064K |
| --           | *20% bleed adjusted*                                          | *Total*       |   INR13277K |

## Projected Timeline

### Pre-alpha [02 months]

- Multi-client WebRTC implementation
- Get UX/UI designed for web and mobile.
- Threaded discussion implementation during live call
- Start gathering user feedback

### Alpha [06 months]

- Polish up branding for first public release
- Implement file-sharing
- Android app and iOS app.
- Increase user capacity per call

### Beta [08 months]

- Add billing methods
- Add archival functions, i.e. call record and storage option.

### v1.0 [09 months]

- Polish up and expose first round of premium features to the public.
- Polish up branding
- Implement client billing

### v2.0 [12 months]

- Make privately deployable, hosted instances as premium licenses.
- Gear up for on-premise installations as commercial license.
