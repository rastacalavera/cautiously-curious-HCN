# cautiously-curious-HCN
Alt to Castopod
This was created to help me center my thoughts. I was getting too in the weeds with branches on the LL lit and trying to sync from Gl to Gh so I figured I would take a 100% fresh approach.

What I learned so far:
* Fork Castanet theme and make changes there, don't mess with site and theme at the same time.
* When the "upcoming" horizontal line is seen on main page, the current process is to take the user to a landing page from the site params that references the `upcoming/xyz.html` file which is different from the episode page (md file).
* The important parts of the theme for modification include
  * partials:
    * row-upcoming
    * grid-upcoming
  * layout:
    * `upcoming/list.html`

* The code that I would use to embed the live stream is below:
```
<div class ="center">
<iframe src="https://demo.azuracast.com/public/azuratest_radio/embed?theme=light" frameborder="0" allowtransparency="true" style="width: 100%; min-height: 150px; border: 0;"></iframe>
</div>
```
* The code for RSS generation should be modified a bit as well
```
<rss version="2.0"
     xmlns:podcast="https://github.com/Podcastindex-org/podcast-namespace/blob/main/docs/1.0.md"
     xmlns:content="http://purl.org/rss/1.0/modules/content/"
     xmlns:wfw="http://wellformedweb.org/CommentAPI/"
     xmlns:dc="http://purl.org/dc/elements/1.1/"
     xmlns:atom="http://www.w3.org/2005/Atom"
     xmlns:sy="http://purl.org/rss/1.0/modules/syndication/"
     xmlns:slash="http://purl.org/rss/1.0/modules/slash/"
     xmlns:itunes="http://www.itunes.com/dtds/podcast-1.0.dtd"
     xmlns:media="http://search.yahoo.com/mrss/"
     xmlns:googleplay="http://www.google.com/schemas/play-podcasts/1.0"
    >
  <channel>
      <podcast:value>type="lightning" method="keysend" suggested="0.00000005000"
      <podcast:valueRecipient name="rastacalavera" type="node" address="" split="100" />
      </podcast:value>
    <podcast:liveItem> status={{ .Site.Params.show_live_status }} start="{{ .Site.Params.show_live_start }}" end="{{ .Site.Params.show_live_end }}"</podcast:liveItem>
    <title>{{ $.Site.Title }}</title>
```
* The main `toml` config has to have additional modifications as well to pull in the `.Site.Params.xyz` from the code above
* The `archetypes` in the theme can be modifed or new ones created
