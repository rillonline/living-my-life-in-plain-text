Introduction
============

1.  Capture ideas and important stuff
2.  Refile what you like and discard the rest.
3.  Review your agenda.
4.  Revise your to dos and calendar as needed, making notes as you go.
5.  Archive what you have finished.

Thinking About Doing
====================

Perhaps this is an odd way to put it, but the difficult part of getting
organized with Orgmode is figuring out what I actually want to
accomplish. This is true about the tasks themselves--what do I want to
work on--and, more important for this article, how do I want to think
about what I want to do.

You can scatter `TODO` headlines throught all of your org files. You
just have to tell Org where to look for them. Since files can get
deleted or moved off of your computer, keeping them in one file for the
purpose seems smart to me.

Once I decided to have a dedicated file, I had to figure out where to
put it and what to call it. After some experimentation, I decided to
have a directory called `org` in my home directory `~/org`. After more
experimentation, I decided to name my file `organizer` without an
extension. This is because the agenda view names the source for the
entry. `organizer=is shorter than =organizer.org` and does not introduce
confusion which `todo.org` or just `todo` did for me.

Then I look at the tasks in my list. They naturally sorted themselves
into different groups with some left over. The divisions have some
overlap, but I was eventually able to sort them out with a miscellaneous
`Tasks` heading for everything else. I could have called it that, but
decided against it.

Agenda
======

Your Agenda
-----------

Use the letter `r` to refresh your agenda view after making changes. In
this way, you can keep a dedicated buffer with a current agenda view.

Using Capture
=============

Ignore the key binding for `capture` in the org documentation. Emacspeak
has its own key binding.

``` {.example}
c-; r
```

This is control plus semicolon followed by the letter lowercase `r` for
remember. Before using this command, you must set up a template. The org
manual shows you how to set up templates to capture notes in different
files. My strategy is to use one file like this:

``` {.example}

```

(setq org-default-notes-file \"\~/organizer.org\")

Priority
========

`c-c ,` (comma) will set a priority. The default priority is \"b\".
After pressing =c-c ,\" you can enter \"a\", \"b\" or \"c\" with \"a\"
being highest and \"c\" being lowest. If you need a different system,
you can customize this list.

Calendar
========

Org can use theemacs diary, however, I found this to be unsatisfying.
Setting up the diary file by hand is easy enough, but the default agenda
view just lists the contents of the file first before showing anything
else.

A better way is to set the diary file up as an org file with headings
and special properties and tags.

Allow `refile` to see more than the top heading in your file.

``` {.example}

```

(setq org-refile-targets \'((org-agenda-files . (:maxlevel . 6))))

\*co TODO Keywords

-   finished task keywords
    -   done (completed)
    -   deferred (no plan to work on this right now)
    -   cancelled (never going to do this)

Archiving Finished Tasks
========================

When a task is marked with one of the finished keywords, archive it. The
task and its associated information will go into a file called
`archive.org`. It will grow and grow as you finish tasks. You may never
need to open this file but it is available if you do. Your notes may
become very important in this case.

`c-c c=x c=a` will archive the task at point.

Using Capture to Corral New Tasks
=================================

The point here is not to be distracted and to keep interruptions to a
minimum while you are working. Find a regular time to go through the
list. Weed out anything you don\'t need or want to do and memorialize
the rest.

Displaying Your Agenda on Initial EMacs Startup
===============================================

Add the following to your `init.el` file:

``` {.example}
(setq initial-buffer-choice 'org-agenda-list)
```

References
==========

-   [Using org-mode as a Day
    Planner](http://nfewartisans.com/2007/08/using-org-mode-as-a-day-planner/)
    This is an old article. Verify the code if you plan to use it. I
    include it here because it has a very solid plan for organizing
    tasks and getting things done.

-   [Learn How to Take Notes More Efficiently in Org
    Mode](https://sachachua.com/blog/2015/02/learn-take-notes-efficiently-org-mode/)
    Of particular interest is how to learn to refile notes. Includes a
    strategy for notetaking and org instructions. Since orgmode has its
    own completion process, I don\'t understand why it is included in
    this article unless the article predates orgmode\'s inclusion of
    completions. See [15.1
    Completions](https://orgmode.org/manual/Completion.html) in the
    orgmode manual.
