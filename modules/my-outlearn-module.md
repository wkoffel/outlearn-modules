<!--
{
"name": "my-outlearn-module",
"version" : "0.1",
"title" : "My Outlearn Module",
"description" : "This module will grow to be the best module ever",
"homepage" : "https://www.test.com",
"coverImage": "http://upload.wikimedia.org/wikipedia/commons/thumb/2/25/Variations_on_a_Waltz_by_Diabelli_-_Theme.svg/2000px-Variations_on_a_Waltz_by_Diabelli_-_Theme.svg.png",
"freshnessDate" : 2015-05-18,
"license" : "CC BY 4.0",
"tags" : "outlearn, wkoffel, golang, c++, hello world"
}
-->

<!-- @section -->

# What is this page?

This is a placeholder Learning Module for you to customize.  Look in the `my-outlearn-module.md` to see how it is coded up, and then start editing away with your own content.

<!-- @link, "url" : "http://www.nodejs.org", "text": "Just testing http: protocol" -->

<!-- @link, "url" : "http://codepen.io/ericrasch/pen/Irlpm", "text": "Play with this CodePen" -->

Features Recipe type  | values
 - | -
 ca n have dependencies | yes
 uses type friendly injection | shown at the top of Path cards
 object available in config phase | shown on the Path card as additional information

 <p data-height="268" data-theme-id="0" data-slug-hash="Irlpm" data-default-tab="result" data-user="ericrasch" class='codepen'>See the Pen <a href='http://codepen.io/ericrasch/pen/Irlpm/'>CSS line behind title text</a> by Eric Rasch (<a href='http://codepen.io/ericrasch'>@ericrasch</a>) on <a href='http://codepen.io'>CodePen</a>.</p>
 <script async src="//assets.codepen.io/assets/embed/ei.js"></script>

### Using Markdown

<iframe height='268' scrolling='no' src='//codepen.io/ericrasch/embed/Irlpm/?height=268&theme-id=0&default-tab=result' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>See the Pen <a href='http://codepen.io/ericrasch/pen/Irlpm/'>CSS line behind title text</a> by Eric Rasch (<a href='http://codepen.io/ericrasch'>@ericrasch</a>) on <a href='http://codepen.io'>CodePen</a>.
</iframe>

You may have already used Markdown. It's an awesome format for technical publishing. If you need a refresher, GitHub has a great overview.

<!-- @link, "url" : "https://help.github.com/articles/markdown-basics/", "text": "I know enough about Markdown." -->

GitHub-flavored markdown will work just fine, and you can preview your files in your favorite text editor or Markdown preview tool before uploading them to Outlearn for final proof-reading.

If you want to enrich your content with more features, this sample module has a few examples, including the Unfurled Link above, and the interactive features described in the next section.

> Block quotes get special styling on Outlearn. They turn into highlight boxes.

```ruby
def testingSmartQuotes
  string = “This is a string with smart quotes”
  return string
end
```

<!-- @section -->

# Multiple Choice Test

<!-- @multipleChoice -->

### Operator Precedence

The following code snippet:

```javascript
`var x = a + b * c + d;`
 ```

is equivalent to which of the answers below?

- [ ] `var x = (a + b) * (c + d);`
- [ ] `var x = a + ((b * (c + d));`
- [X] `var x = (a + (b * c)) + d;`
- [ ] `var x = ((a + b) * c) + d;`

Remember, `*` has higher precedence than `+`, so it will bind tighter.

<!-- @end -->

<!-- @multipleChoice -->

Which of these people created Linux?

- [ ] ![](http://upload.wikimedia.org/wikipedia/commons/thumb/0/01/Bill_Gates_July_2014.jpg/220px-Bill_Gates_July_2014.jpg)

  **Bill Gates**

- [X] ![](http://upload.wikimedia.org/wikipedia/commons/thumb/5/52/LinuxCon_Europe_Linus_Torvalds_03.jpg/220px-LinuxCon_Europe_Linus_Torvalds_03.jpg)

  **Linus Torvalds**

- [ ] ![](http://upload.wikimedia.org/wikipedia/commons/thumb/6/66/Guido_van_Rossum_OSCON_2006.jpg/200px-Guido_van_Rossum_OSCON_2006.jpg)

  **Guido van Rossum**

<!-- @end -->

<!-- @section -->

# Images and videos

You can include images using Markdown syntax.

![sea](https://raw.githubusercontent.com/outlearn-content/outlearn-modules/master/assets/sea.jpg)


You can embed hosted videos in your paths using Outlearn @asset syntax. Here is a Vimeo video:

<!-- @asset, "contentType": "outlearn/video", "provider": "vimeo", "url": "https://player.vimeo.com/video/67325705" -->

And here is another one form YouTube:

<!-- @asset, "contentType": "outlearn/video", "provider": "youtube", "url": "https://www.youtube.com/embed/CmjeCchGRQo" -->

<!-- @section -->

# Let's make our module Fancy

If you want to get your audience to practice what you preach, give them a task.

```python
# Transpose a matrix:
>>> l = [[1, 2, 3], [4, 5, 6]]
>>> zip(*l)
[(1, 4), (2, 5), (3, 6)]

# Divide a list into groups of n:
>>> l = [3, 1, 4, 1, 5, 9, 2, 6, 5, 3, 5, 8]
>>> zip(*[iter(l)] * 3)
[(3, 1, 4), (1, 5, 9), (2, 6, 5), (3, 5, 8)]
```

<!-- @task, "text" : "Go and run these clever code examples on your own machine, lazy bones!"-->

And if they are making something worth sharing, why not let them share it with you?

<!-- @task, "hasDeliverable" : true, "text" : "Write and submit a haiku about your favorite compiler."-->

If you need more details on how to author, please visit the [Outlearn Publishing Guide](https://pilot.outlearn.com/learn/outlearn/outlearn-publishing), where you'll find more examples along with the full specification for the format used by this sample module.

# More tests

<a class="jsbin-embed" href="http://jsbin.com/hobada/2/embed?html,css,js,output">JS Bin on jsbin.com</a><script src="http://static.jsbin.com/js/embed.min.js?3.34.3"></script>
