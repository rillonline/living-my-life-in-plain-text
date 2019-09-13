Initially, I set up my calendar file in the format for Emacs Diary. Then
I decided to go whole hog into orgmode and set up the calendar as
described in Josh Errickson\'s post [Org Agenda As A
Calendar](https://errickson.net/org_agenda_calendar.html). I don\'t like
it so I am going back to Emacs diary.

Storing the Diary File
======================

By default, the diary file is stored in the `.emacs.d` folder. I moved
it to my `~/org` folder.

I made the following changes to my Emacs configuration file. In addition
to changing the diary\'s location, I told Org to include this file in
the agenda view.

``` {.example}
(setq diary-file (concat org-directory "/diary"))
(setq org-agenda-diary-file diary-file)
(setq org-agenda-include-diary t)
```

You may notice that the diary file has no extension. This is because the
agenda view lists the source of diary entries. Reading, for example,
`diary.txt` is a bit off-putting so I changed my file name to only
`diary` but added a mode line at the top of the file so that I would
still be editing in textmode. Fundamental did not work for me.

``` {.example}
; -*- mode: Text;-*-
```

Diary File Format
=================

I followed the formatting instructions for [Format of the Diary
File](https://www.gnu.org/software/emacs/manual/html_node/emacs/Format-of-Diary-File.html).

If you are using the 12-hour clock, be sure to put pm after times.
Otherwise, they are assumed to be am. I had a hair cut scheduled for
2:30 am.

On a personal note, it is funny to read the earlier examples. Clearly
the writer taught at Princeton University. I graduated from Princeton
High School.

Conclusion
==========

I prefer this diary look in my org agenda.

For Further Reading
===================

[Customizing the Calendar and
Diary](https://ftp.gnu.org/old-gnu/Manuals/elisp-manual-20-2.5/html_chapter/elisp_40.html)
