# Project 2 - *Twitter FBU*

**Name of your app** is an android app that allows a user to view their Twitter timeline and post a new tweet. The app utilizes [Twitter REST API](https://dev.twitter.com/rest/public).

Time spent: **X** hours spent in total

## User Stories

The following **required** functionality is completed:

* [✔️]	User can **sign in to Twitter** using OAuth login
* ![login](https://user-images.githubusercontent.com/56266109/172922153-649d2d36-c9e9-4515-baf6-aefe850629ea.gif)

* [✔️]	User can **view tweets from their home timeline**
  * [✔️] User is displayed the username, name, and body for each tweet
  * ![timeline](https://user-images.githubusercontent.com/56266109/173122968-c3889245-5a15-4c0e-b53f-79bf94bb5cfb.gif)
* [✔️] User can **compose and post a new tweet**
* ![composeToast](https://user-images.githubusercontent.com/56266109/172922235-f2306ba1-7414-42d1-a4a3-030122a9b02e.gif)
  * [✔️] User can click a “Compose” icon in the Action Bar on the top right
  * [✔️] User can then enter a new tweet and post this to Twitter
  ![composing](https://user-images.githubusercontent.com/56266109/173123369-3b7075af-243d-445e-81d1-6ab38d644363.gif)
  * [✔️] User is taken back to home timeline with **new tweet visible** in timeline
  * [✔️] Newly created tweet should be manually inserted into the timeline and not rely on a full refresh
* [✔️] User can **see a counter with total number of characters left for tweet** on compose tweet page
* [✔️] User can **pull down to refresh tweets timeline**
* ![refresh]
* (https://user-images.githubusercontent.com/56266109/173123559-0b1c6feb-2968-4f04-b8ca-739bac4cc6ff.gif)
* [✔️] User can **see embedded image media within a tweet** on list or detail view.
<img width="286" alt="Screen Shot 2022-06-10 at 10 53 39 AM" src="https://user-images.githubusercontent.com/56266109/173123607-bc5143ed-ed35-4c16-bb0f-e0dcf5e7c104.png">

The following **optional** features are implemented:
* [✔️] User is displayed the [relative timestamp](https://gist.github.com/nesquena/f786232f5ef72f6e10a7) for each tweet "8m", "7h"
* <img width="272" alt="Screen Shot 2022-06-10 at 10 54 00 AM" src="https://user-images.githubusercontent.com/56266109/173123661-f4026f34-b42d-419c-92ee-be2c5b1ffe4d.png">
* [ ] User is using **"Twitter branded" colors and styles**
* [✔️] User sees an **indeterminate progress indicator** when any background or network task is happening
* ![progress](https://user-images.githubusercontent.com/56266109/173123787-3125ca99-9361-42c6-a260-05886104bfe7.gif)
* [ ] User can **select "reply" from home timeline to respond to a tweet**
  * [ ] User that wrote the original tweet is **automatically "@" replied in compose**
* [ ] User can tap a tweet to **open a detailed tweet view**
  * [ ] User can **take favorite (and unfavorite) or retweet** actions on a tweet
* [ ] User can view more tweets as they scroll with infinite pagination
* [ ] Compose tweet functionality is built using modal overlay
* [ ] User can **click a link within a tweet body** on tweet details view. The click will launch the web browser with relevant page opened.
* [ ] Replace all icon drawables and other static image assets with [vector drawables](http://guides.codepath.org/android/Drawables#vector-drawables) where appropriate.
* [ ] User can view following / followers list through any profile they view.
* [ ] Use the View Binding library to reduce view boilerplate.
* [ ] On the Twitter timeline, apply scrolling effects such as [hiding/showing the toolbar](http://guides.codepath.org/android/Using-the-App-ToolBar#reacting-to-scroll) by implementing [CoordinatorLayout](http://guides.codepath.org/android/Handling-Scrolls-with-CoordinatorLayout#responding-to-scroll-events).
* [ ] User can **open the twitter app offline and see last loaded tweets**. Persisted in SQLite tweets are refreshed on every application launch. While "live data" is displayed when app can get it from Twitter API, it is also saved for use in offline mode.

The following **additional** features are implemented:

* [ ] List anything else that you can get done to improve the app functionality!

## Video Walkthrough

Here's a walkthrough of implemented user stories:

<img src='http://i.imgur.com/link/to/your/gif/file.gif' title='Video Walkthrough' width='' alt='Video Walkthrough' />
![timeline](https://user-images.githubusercontent.com/56266109/173124530-8f10c089-ad34-494d-9bca-913463938956.gif)


GIF created with [Kap](https://getkap.co/).

## Notes
I encountered issues while building the relative timestamp, because depending on how do you calculate the time span between the creation of the tweet and the actual time, you could get a negative number and always show just now. To solve it you only need to be sure you are either using the absolute value of the difference, or you are substracting the createdAt to the now

## Open-source libraries used

- [Android Async HTTP](https://github.com/loopj/android-async-http) - Simple asynchronous HTTP requests with JSON parsing
- [Glide](https://github.com/bumptech/glide) - Image loading and caching library for Android

## License

    Copyright [yyyy] [name of copyright owner]

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
