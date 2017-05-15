# xplex - Live interactive game streaming

**Note: brain dump. Needs rephrasing and edits**

xplex's initial plan is to provide a service to stream live audio and video to multiple platforms like Twitch, YouTube etc, simultaneously with no extra overhead. Gamer sends one stream up, we distribute that to different video platforms.

At the core, xplex is a multi-streaming service for audio and video. xplex is built primarily for gamers, with the premise that the gaming industry evolves fast and has very rigorous demands on both efficiency and performance, though it can be useful throughout sports and entertainment industry once matured.

The next phase for xplex is to provide a rich and interactive experience for viewers in real-time, where viewers can choose between different perspectives live in the think and commentators and, optionally, interact with the streamers/broadcasters. Think of this as the equivalent of viewing a cricket match where you can select which camera to view from, which commentator to hear and after the match join the conversation with the commentators.

xplex aims to do this while taking away any infrastructual overhead from the gaming rig so that gamers can focus on the gaming. Fun part: we can eventually do this outside e-sports as well.

**Table of Contents**:

- [Background](#background)
- [xplex v2](#xplex-v2)

---

# Background

## Live e-sports broadcasts today

Game streaming today is very similar to traditional live sports broadcast. Viewers start viewing a channel and they passively consume any content that is broadcasted. They cannot interact with the station or choose a viewing angle. Live interactive broadcast is changing the unidirectional and preset mode of the sports and entertainment industry by breaking that barrier.

## Aspects of interactive broadcasts:

There are two aspects of live interactive broadcasts:

**Live participation:** First, using interactive broadcasts, talk shows and live programs can now get viewers to come on-stage and be a part of that program. Think of a talk show where you have a group of experts speaking on a topic. Traditionally, if a viewer needed to participate in the show, they had to call on a number, wait on line till they are online. Now, talk shows can have a web or mobile app through viewers can participate live. <TODO: Add case study, e.g. NFL>

**Choice of perspective:** Second, in sports, each game has multiple teams, each team with multiple players. There are multiple cameras covering different perspectives. Then there are commentators and meaningful statistics that are rendered live. At this point, a viewer cannot choose a perspective. They cannot choose between commentary in different languages if available. What if a viewer could choose which perspective to view, which camera to view from, which commentator to listen? The gaming equivalent of this is more straightforward. There are usually multiple players in a game in multiple teams. There are broadcasters who provide live expert commentary, without participating in the game. Like traditional sports broadcasts, these broadcasters choose which player to show, which area of the map to focus on, add their commentary and any statistics to show, and send out a stream which are broadcasted to viewers.

# xplex v2

- You play. We stream to the world.
- Experience immersive game stream viewing

In addition to letting streamers send in one stream and broadcast to multiple video platforms simultaneously, the v2 of xplex will have these abilities: (listed not in any particular order)

## Features

### Perspective:

Objective: Allow viewers to choose between different players/broadcasters in a live game stream, just like they can do in the game client.

- Multi-stream the views of different players, letting viewers choose at runtime which player's stream they want to watch in a game.
- Let viewers do this from a web browser. (This can be done through the game client. The goal here is to expand viewership to multiple platforms while providing an engaging experience in very low latency)
- Similar to a video conference like Hangouts, except viewers would see the game stream of a player.
- Choosing a broadcaster and switching to another view would retain the audio from the broadcaster but show the video of the selected view.

### Low/no overhead for streamers:

Objective: Remove requirement for streamers to upload multiple video streams by directly connecting xplex to game servers and fetching streams from there.

- Gamers do not want to upload videos while gaming, because that would cause unnecessary bandwidth and processor choke on their side.
- Instead, for important games/tournaments, broadcasters upload their stream. But, it will not be feasible to askk broadcasters to upload multiple streams, one for each player.
- So, the way receive multiple streams instead is to have xplex connect to the game servers through the games' clients in spectator mode and record those streams and send to xplex's media router.

### Interaction with broadcasters:

Objective: Allow viewers to participate live and be a part of the experience.

- Viewers can send a question which can be upvoted, downvoted or answered by other viewers.
- Questions/comments with enough (need to define criteria) upvotes will bubble up to broadcasters/streamers to respond
- Streamers will have the capability to bring up chosen viewers to stage and interact with them through the broadcast.

## Technology

## Opportunities

## Challenges

## Competition
