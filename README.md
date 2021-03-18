# hugo-calendly [![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
Add a Calendly link directly into your Hugo page in no time with a simple shortcode block!  
Without having to copy&paste then edit plain html.

Simply add a shortcode block to any page like this...
```
{{< hugo-calendly calendar="<insert your calendar name here>">}}
```
... and that's it. Hugo will take care of the rest.

Your page will show a link that takes your visitors straight to your Calendly page where they can book a time with you.

TODO: insert example gif

# Requirements
You will need:
- a [Calendly](https://calendly.com) account,

  (If you don't have one, yet: it has a generous FREE tier.)
- a [Hugo](https://gohugo.io/) page,

  (Guess what? It's FREE, too.)
- [git](https://git-scm.com/) to install this addon as a [submodule](https://git-scm.com/book/en/v2/Git-Tools-Submodules)

  (And again: it's FREE.)

# Installing hugo-calendly
1. Navigate to your Hugo page's home folder.
2. Add hugo-calendly as submodule via git:

   ```bash
   git submodule add git@github.com:bvotteler/hugo-calendly.git layouts/shortcodes/hugo-calendly
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

## Add hugo-calendly shortcode to your page
From the examples above, let's assume we have found the calendar name `janedoe`.

1. Add a shortcode to your page's markdown file:

   ```
   {{< hugo-calendly/calendly calendar="janedoe" >}}
   ```
2. *(Optional)* Or, if you want to point directly to the event type from the example above, use this:

   ```
   {{< hugo-calendly/calendly calendar="janedoe/my-event" >}}
   ```

And that's all. You should be ready to go.

## Change the link text
By default, the shortcode will make the link text say: "Schedule a time".  
You can change that.

Simply add a closing shortcode tag and put your desired text between the shortcode tags:
```
{{< hugo-calendly/calendly calendar="janedoe" >}}
  Book a time to talk now!
{{< /hugo-calendly/calendly >}}
```

Now your Calendly link will say "Book a time to talk now!"

# Troubleshooting / Bugs
If you run into any problems, check if someone else raised an [issue](https://github.com/bvotteler/hugo-calendly/issues) yet. If not, add a new one and I'll take get back to you.