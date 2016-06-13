# Itinerary

## To Do

* [x] Ensure that all explicit references to data in the Plague HTML file are removed **or** documented.
* [ ] Ensure that all explicit references to data in the Plague datajson are mapped to 1 field.
* [ ] Ensure that the Plague JS routine is using templates for content rather than hard-coded HTML.
* [x] Ensure that all explicit references to data in the Rome HTML file are removed **or** documented.
* [x] Ensure that the Rome JS routine is using templates for content rather than hard-coded HTML.
* [x] Ensure that all explicit references to data in the Rome datajson are mapped to 1 field and NOT in the JS. (Note that this is not doable based on the current configuration, where common classes on table rows are the interface for these. However, the JS refers to specific CSS classes in the markup as hooks for this data.)

## Current State

Thus far our efforts have served to produce two working demonstrations using mapping technology to navigate historical data or literature:

* "Plague Year," which provides a timeline-based navigation tool to step through events recorded from Defoe's *A Journal of the Plague Year*.
* Melville in Rome, which enables the exploration of possible routes taken by Melville in between events recorded in his journal of his time spent there.

Our present goal is to decouple both demonstrations from any specific references to the data or content, such that they can be utilized by anyone to illustrate similar data or content. A scholar could fork the GitHub repository, enter their own CSV data, provide their own set of GeoJSON files, and render a new, unique map UI for timeline or route-based exploration. As long as the data provided conforms to an assumed JSON spec, the UI layer can parse and render that data.

We also seek to fully document both demonstrations so that such efforts are approachable, albeit with a degree of savvy when it comes to website technologies. Some assistance is likely required, but such assistance is not proprietary to the Itinerary team. The project uses widely-embraced and familiar technologies.

## Going Forward

Our next phase of development will focus on better realizing the UI layer as a portable JavaScript application that can sit atop any backend technology, as long as the data to be consumed conforms to the prescribed JSON spec. This will enable other projects to add a mapping UI layer to existing applications, or to work with their preferred technologies. We will have further explored *event*, *route*, *path*, and *region* concepts such that those can be universally adapted to different data and geographies. We will look to provide template examples for outputting data from other platforms.

Also important in our next phase will be addressing the need for unique, persistent URIs for *events*, which is our term for entries on the itinerary. As the current phase uses Jekyll to spin up a static site based on the current state of the data (in CSV format) and JavaScript to pull together that data at run-time, there is no persistent data store for itinerary entries so that those can be reliably linked to or referenced by unique identifiers. Thus it is not presently possible to reference one event in another event's notes, which is a stated goal.

As Itinerary evolves, our goal is to enable collaborative and crowdsourcing features so that scholarly communities can share insight and help refine mapped data.
