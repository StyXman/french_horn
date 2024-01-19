* count = None
* while count is None or count > 0:
    * count = 0
    * fetch home
    * for each toot:
        * if reblog:
            * unwrap

        * if id in known:
            * if edited_at > created_at:
                * mark unread
                * save diff?

            * if boost:
                * ???

            * if replies_count > known.replies_count:
                * fetch context
                * mark unread?
                * update last_replied

            * continue

        * count++

        * if in_reply_to_account_id == account.id:
            * thread
            * fetch context

        * if not in_reply_to_id and replies_count:
            * conversation root
            * fetch context

        * if in_reply_to_id in known + new:
            * add to thread

        * if in_reply_to_id or replies_count:
            * mark with *
            * allow fetch context

        * if spoiler_text:
            * CW

        * if language not in known_languages:
            * add to title

        * title is boosted + context + unknown lang + tags + beginning of content

* for toot in [ toot.last_replied > now - 1w ]:
    * chek if replies_count > known.replies_count

* 2/3rds is list, 1/3rd is content

* TODO:
    * build threads?

* actions:
    * mark as read
    * mark as unread
    * boost
    * like
    * quote-write
    * write
    * delete
    * show/hide read
        * does not automatically hide toots
