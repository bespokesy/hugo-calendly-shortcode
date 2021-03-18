# hugo-calendly-shortcode [![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
Add a Calendly link directly into your Hugo page in no time with a simple shortcode block!  
Without having to copy&paste then edit plain html.

Simply add a shortcode block to any page like this...
```
{{< calendly calendar="<insert your calendar name here>" >}}
```
... and that's it. Hugo will take care of the rest.

Your page will show a link that takes your visitors straight to your Calendly page where they can book a time with you.

![demo gif of hugo-calendly-shortcode](http://i.imgur.com/KxnCQ7i.gif)

# Requirements
You will need:
- a [Hugo](https://gohugo.io/) page,
- a [Calendly](https://calendly.com) account,

  (In case you don't have one yet: it has a generous FREE tier.)
- [git](https://git-scm.com/) to install hugo-calendly-shortcode as a [submodule](https://git-scm.com/book/en/v2/Git-Tools-Submodules)

# Install hugo-calendly-shortcode
1. Navigate to your Hugo page's home folder.
2. Add hugo-calendly-shortcode as a theme submodule with git:

   ```bash
   git submodule add git@github.com:bvotteler/hugo-calendly-shortcode.git themes/hugo-calendly-shortcode
   ```
3. Add `hugo-calendly-shortcode` as an element of the `theme` list in your `config.toml`. For example:
   ```
   theme = ["hugo-calendly-shortcode, "my-theme"]
   ```
   (Note: adding it as left-most entry makes sure other themes won't override it by accident.)

## Update hugo-calendly-shortcode
From Hugo's home folder, run this git command to update the submodule (including all the other ones):
```bash
git submodule update --remote --merge
```

## Uninstall hugo-calendly-shortcode
To uninstall the submodule, use these commands:
```
git submodule deinit themes/hugo-calendly-shortcode
git rm themes/hugo-calendly-shortcode
```

# Using hugo-calendly
In order to embed it we need a Calendly calendar name, and a bit of shortcode for your hugo page.  
That's all.

## Pick your Calendly calendar name
I will assume you have an event type setup.  
(If you need help with that, [follow Calendly's instructions](https://help.calendly.com/hc/en-us/articles/115002939274-Account-setup#2).)
1. Visit your [Calendly events page](https://calendly.com/event_types/user/me),
2. Jot down your calendly name.

   It should show under your name on the events page. e.g. if it shows `calendly.com/janedoe`, we want the part after `calendly.com/`. In this example that is `janedoe`

3. *(Optional)* If you want to direct people to a specific event, open that event and get the event name from the event link shown under "What event is this?".

   e.g. Your event invitation link shows `calendly.com/janedoe/my-event`. In this case, our calendar name is `janedoe/my-event`

## Add hugo-calendly-shortcode to your page
From the examples above, let's assume we have found the calendar name `janedoe`.

1. Add a shortcode to your page's markdown file:

   ```
   {{< calendly calendar="janedoe" >}}
   ```
2. *(Optional)* Or, if you want to point directly to the event type from the example above, use this:

   ```
   {{< calendly calendar="janedoe/my-event" >}}
   ```

And that's all. You should be ready to go.

## Change the link text
By default, the shortcode will make the link text say: "Schedule a time".  
You can change that.

Simply add a closing shortcode tag and put your desired text between the shortcode tags:
```
{{< calendly calendar="janedoe" >}}
  Book a time to talk now!
{{< /calendly >}}
```

Now your Calendly link will say "Book a time to talk now!"

# Troubleshooting, bugs & help
If you run into any problems, check if someone else raised the same [issue on GitHub](https://github.com/bvotteler/hugo-calendly-shortcode/issues) and add a comment. If not, please add a new issue so I can address it.