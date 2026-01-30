# OpenChaos-Backend

Used to persist data for the view tracker on `openchaos.dev`.

## How it works
 - Individual containers keep track of pageviews locally and flush data into files in the `partials` directory every 60 seconds.
 - A github action triggers every 6 minutes that adds up the partials, deletes them, and updates the `consolidated_total.txt` file.
