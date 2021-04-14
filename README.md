# hugo-calendly-shortcode [![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
Add a Calendly link directly into your Hugo page in no time with a simple shortcode block!  
Without having to copy & paste then edit plain html.

Simply add a shortcode block to any page like this...
```
{{< calendly calendar="<insert your calendar name here>" />}}
```
... and that's it. Hugo will take care of the rest.

Your page will show a link that takes your visitors straight to your Calendly page where they can book a time with you.

![demo gif of hugo-calendly-shortcode](http://i.imgur.com/KxnCQ7i.gif)

Visit my [demo page](https://bespokesy.github.io/hugo-calendly-shortcode-demo-site/) for more examples.

# Requirements
You will need:
- a [Hugo](https://gohugo.io/) page,
- a [Calendly](https://calendly.com) account,

  (In case you don't have one yet: it has a generous FREE tier.)
- [git](https://git-scm.com/) to install hugo-calendly-shortcode as a [submodule](https://git-scm.com/book/en/v2/Git-Tools-Submodules)

# Install hugo-calendly-shortcode
There are two ways to install it:
1. [As a git submodule](#install-as-git-submodule).
2. Simply [copy and paste it](#install-via-copy-and-paste)

   Downside: You'll need to manually copy the files for future updates.


## Install as git submodule
1. Navigate to your Hugo page's home folder.
2. Add hugo-calendly-shortcode as a theme submodule with git:

   ```bash
   git submodule add git@github.com:bespokesy/hugo-calendly-shortcode.git themes/hugo-calendly-shortcode
   ```
3. Add `hugo-calendly-shortcode` as an element of the `theme` list in your `config.toml`. For example:
   ```
   theme = ["hugo-calendly-shortcode, "my-theme"]
   ```
   (Note: adding it as left-most entry makes sure other themes won't override it by accident.)

### Update hugo-calendly-shortcode
From Hugo's home folder, run this git command to update the submodule (including all the other ones):
```bash
git submodule update --remote --merge
```

### Uninstall hugo-calendly-shortcode
1. Remove the shortcodes from any pages,
2. Remove the theme from your `config.toml` file,
3. From Hugo's home folder, run these commands to uninstall the submodule: 
   ```
   git submodule deinit -f themes/hugo-calendly-shortcode
   git rm -f themes/hugo-calendly-shortcode
   ```

## Install via copy and paste
1. Copy the [calendly.html](layouts/shortcodes/calendly.html) file into `<your_hugo_page_root>/layouts/shortcodes/` folder.

# Using hugo-calendly
In order to embed it we need a Calendly calendar name, and a bit of shortcode for your hugo page.  
That's all.

1. Pick a Calendly calendar name. e.g. `janedoe`
   - *(Optional)* If you want to target a specific event type, append it after a `/` symbol. e.g. `janedoe/my-event`
   - If you need help with event types, [follow Calendly's instructions](https://help.calendly.com/hc/en-us/articles/115002939274-Account-setup#2).
2. Add a shortcode to your page's markdown file and add the calendar/event name as `calendar` parameter. 
   
   For example:
   ```
   {{< calendly calendar="janedoe" />}}
   ```
   Or with a specific event type:
   ```
   {{< calendly calendar="janedoe/my-event" />}}
   ```

And that's all. You should be ready to go.

## Demo page
To see more examples, visit my [demo page](https://bespokesy.github.io/hugo-calendly-shortcode-demo-site/). It will show you the shortcode and what it looks like on an actual Hugo page.

## Change the link text
By default, the shortcode will make the link text say: "Schedule a time".

To change the text, simply add a closing shortcode tag and put your desired text between the shortcode tags:
```
{{< calendly calendar="janedoe" >}}
  Book a time to talk now!
{{< /calendly >}}
```

Now your Calendly link will say "Book a time to talk now!"

# Advanced features with hugo-calendly-shortcode-plus
I am building a version with more features for Calendly Premium or Pro owners.  
Additional features will enable you to:
- Apply CSS styles to customize the look and feel for Calendly
- Add UTM parameters to track your embedded Calendly forms
- Pull parameter sets from different sources:
  - Shortcode parameters (same as with this version),
  - Hugo page front-matter,
  - Hugo site configuration parameters,
  - Hugo data files, or
  - A mix of all of the above.

If you would like to receive notifications as my work on that progresses, follow [this link to subscribe to updates by mail](https://landing.mailerlite.com/webforms/landing/v3z7p1).

# Troubleshooting, bugs & help
If you run into any problems, check if someone else raised the same [issue on GitHub](https://github.com/bespokesy/hugo-calendly-shortcode/issues) and add a comment. If not, please add a new issue so I can address it.

# Get in touch
Just want to say hi? Ask something else?  
Sure thing! You will find my contact details on [bespokesy.dev/contact](https://bespokesy.dev/contact/).