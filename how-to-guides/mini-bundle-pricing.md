# Mini bundle pricing

Some publishers advertise a special price if you buy a few titles bundled together (and they often assign this "mini bundle" its own ISSN).

Currently Unsub only supports pricing at the single-journal level. We have a few suggestions on how to handle "mini bundles", though not any perfect solution yet unfortunately.

What some Unsub users have done is remove the non-primary bundled titles (so all the journals except for its "main" title) from their COUNTER files (like, delete those rows, then re-upload), so they don't show up in their forecasts, and then if it came to subscribing you'd get them for "free" from the publisher if the main journal is enough to warrant subscribing.

A different workaround others have done is to add the usage together for the bundles in their COUNTER file (you only have to modify the "total", we ignore the months columns) so that usage of the other titles are included in the main title.

You could make the price be $0 for "free with a bundle", but then its Cost Per Use will be $0 and any way of subscribing by most cost effective journal first will pick it, which could get confusing.
