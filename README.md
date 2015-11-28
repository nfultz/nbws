# Newsbeuter websocket pipe

This project allows you to use newsbeuter on a remote server, but open articles
locally. Initially, I forwarded firefox over X11, but this ended up being too
slow. Instead, we can run a websocket server that pushes urls to our browser.
This has the benefit of being browser-agnostic, and works well eg on
Chromebooks.

#Setup

    pip install mod-pywebsocket

and configure `newsbeuter` to use `$BROWSER` for opening articles.

    browser "eval $BROWSER"


Running `nbws` will start a background server, print out it's URL,
and launch newsbeuter. Pressing O should open articles locally.
