I wrote about [Recurring Tasks in
Orgmode](https://rillonline.github.io/posts/2019/08/28/recurring-tasks-in-orgmode/)
previously. Once I had this to-do working properly, I went onto the next
task. I wanted to list my ideas for articles and bigger writing
projects. In my opinion, I did not need to set this all up as a big list
of to-dos. That certainly becomes overwhelming to me.I might just stop
writing altogether because the ideas keep coming but the time and
patience to write them may not be available at the moment. I do want to
be sure I have a stash of ideas to choose from when I am able to sit
down and write out a complete article.

I created a file name \"ideas.org\". I inserted three headings:

``` {.example}
* Writing Ideas Big and Small
** Blog Ideas [/]
** Bigger WRiting Projects [/]
```

You may have noticed that at the end of the second level headings there
are two square brackets \"\[\]\" enclosing a slash \"/\". More on this
later.

Organizing the list
-------------------

At first I thought I would just write a list like this:

``` {.example}
- smart quotess and other typography
- less than shortcuts in orgmode
- Braile pack at public museum
- photo op with Nick
- a walk in the park with Nick
- using org capture
- Using checkboxes in org
```

Then I thought about using checkboxes so I could check them off as I
went. Now this section of the file looks like this:

``` {.example}
- [ ] smart quotess and other typography
- [ ] less than shortcuts in orgmode
- [ ] Braile pack at public museum
- [ ] photo op with Nick
- [ ] a walk in the park with Nick
- [ ] using org capture
- [ ] Using checkboxes in org
```

Who knows, you might even see some of these articles in the future!

Why Use Checkboxes?
-------------------

Why use checkboxes? After all, I could simply delete the item from the
file once I published it.

It\'s a good point. I decided to try this methodology just to see how I
liked it and for two other reasons:

1.  It would let me know how I was doing at keeping up with my ideas.
2.  It would let me know if I needed to be thinking more about writing
    opportunities.

It seems to me that a writer is stuck here: Coming up with ideas and
getting them written.

Using the Checkboxes
--------------------

To check off an item, press \"c-c c-c\" on that line. Then you have:

:- \[X\] Using checkboxes in org

Here\'s what the heading now looks like:

``` {.example}
 ** Blog Ideas [1/7]
```

If I turn the \"/\" (slash) into a percent sign (%) it looks like this:

:\*\* Blog Ideas \[14%\]

If I feel ambitious, I can delete these lines or I can sort them so that
all the unchecked boxes are together.

Sorting Lines
-------------

1.  Highlight the list
2.  Type \"m-x sort-lines\". All the checked off items will be gathered
    together at the end of the list. The items appear in alphabetical
    order.

    ``` {.example}
    - [ ] Braile pack at public museum
    - [ ] a walk in the park with Nick
    - [ ] less than shortcuts in orgmode
    - [ ] photo op with Nick
    - [ ] smart quotess and other typography
       - [ ] using org capture
    - [X] Using checkboxes in org 
    ```

    This list now is in a different order than the way I originally
    wrote it down. I can read through it until I come to an item with a
    checkbox. I know there are no more new items.

3.  If I want to sort in reverse order, I type: \"c-u m-x sort-lines\".
    Here is what I now have:

    ``` {.example}
    - [X] Using checkboxes in org
    - [ ] using org capture
    - [ ] smart quotess and other typography
    - [ ] photo op with Nick
    - [ ] less than shortcuts in orgmode
    - [ ] a walk in the park with Nick
    - [ ] Braile pack at public museum
    ```

    I don\'t think I will use this ordering unless I need a confidence
    boost. I would have to go past everything I\'ve already done.
