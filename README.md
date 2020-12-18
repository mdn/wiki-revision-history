# Wiki Revision History

When [MDN Web Docs](https://developer.mozilla.org)
[moved from a Wiki to a new
platform](https://hacks.mozilla.org/2020/12/welcome-yari-mdn-web-docs-has-a-new-platform/)
called [Yari](https://github.com/mdn/yari) it did so by extracting all
"documents" from a central MySQL database to individual files in a
`git` repo, it lost a lot of the revision history from the years that
MDN Web Docs was a Wiki. **This repo attempts to be a historical record
of those Wiki revisions**.

## About the `revisions.csv` file

The `revisions.csv` file is a chronological (descending) list of revisions
created. The following revisions are filtered out:

* Same author on the same exact URL is squashed into 1

* Certain test slug prefixes like `Experiment:` or `User_project:`

* Revisions created by the `mdnwebdocs-bot` user

The CSV has a heading on the first row.

The URL for any revision is simply made by taking the `locale` and the `slug`
and combining it like so:

    https://developer.mozilla.org/$LOCALE/docs/$SLUG

Note that many of the URLs in the CSV files no longer resolve as 200 OK
on `developer.mozilla.org`. The remaining ones hopefully resolve to
redirects. But some might resolve to 404 Page not found.

The `username` field is identical to the same user even if that same
user has changed their username in the past. E.g. if `chrisdavidmills`
used to have the username `chris` back in 2013, the records for 2013
will go under his "new" username.

## A note about Wiki revision history in Yari

Any page in MDN Web Docs always has a `/contributors.txt` you can add
to the URL. For example:

[https://developer.mozilla.org/en-US/docs/Web/JavaScript/contributors.txt](https://developer.mozilla.org/en-US/docs/Web/JavaScript/contributors.txt)

That list of usernames is similar to the list in `revisions.csv` except their,
each username is made distinct and in order of most recently touched first.

## License

[See LICENSE.md](LICENSE.md).
