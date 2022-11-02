+++
Description = ""
Date = {{ .Date }}
PublishDate = {{ .Date }} # this is the datetime for the when the epsiode was published. This will default to Date if it is not set. Example is "2016-04-25T04:09:45-05:00"
podcast_file = "###.mp3" # the name of the podcast file, after the media prefix.
podcast_duration = "" #required, The duration of the podcast, up to the amount of seconds.
#podcast_bytes = "" # the length of the episode in bytes
episode_image = "img/episode/default.jpg"
#episode_banner = "" #The banner to represent the episode. This image needs to be relative to your baseURL. This image will be display at the top of the episode page, as well as the top of the home page for the most recent episode. Recommend that it is at least 1024 pixels wide.
#guests = [] # The names of your guests, based on the filename without extension.
#sponsors = []
#episode = ""
title = ""
#subtitle = ""
images = ["img/episode/default-social.jpg"] #The square thumbnail to represent the episode. A default image is provided, and the archetype will pre-populate it. This image needs to be relative to your baseURL.
#hosts = [] # The names of your hosts, based on the filename without extension.
#aliases = ["/##"]
#youtube = ""
#guid = "" #A fixed, globally unique identifier for the episode which should never change. If one is not specified the URL of the podcast_file will be used instead.
#transcript = "" #The path to the transcript file. The file can have Markdown or be in HTML. It must be relative to the root of your site (this is a file path, not a URL). It is recommended to put them in your static directory so that Hugo doesn't try to process them.
explicit = "no" # values are "yes" or "no"
#media_override # if you want to use a specific URL for the audio file
#truncate = ""
#upcoming = true # set to true if you want this to be listed as upcoming, etc, etc
#categories = []
#series = []
#tags = []
+++
