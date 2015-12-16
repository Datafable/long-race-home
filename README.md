# The long race home

Website for *The long race home*: <http://datafable.com/tlrh>

## Nerdy part

We'll be tracking 10 riders during a race across Belgium. The trackers are SPOT Trackers. The data sent by these
trackers will be displayed live on the [long race home
website](http://datafable.com/tlrh). This repository contains the following code:

* [Data crawler](./data_crawler): Python code to fetch the tracking data from the SPOT API.
* [Website](./frontend): HTML, CSS en JavaScript code to display the website and the CartoDB visualisation.

Note that this code will not work on its own. Additionally, you'll need:

* 3 CartoDB tables. One for storing the rider metadata, one where the data crawler can write the tracking data to, and
one containing the checkpoints data
* A public CartoDB visualisation that can be injected in the [Cartodbjs code](frontend/js/app.js#L58).
* A Redis database and Celery worker for setting up the data crawler. (See [data crawler documentation](./data_crawler)

Enjoy
