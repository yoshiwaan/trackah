# trackah
Arbitrary life event tracker

The goal is to create events of a certain type by lego bricking together standard field types.
The types will have a label (with effort but in to try and have a controlled vocabulary per user between events)

Users can then create events of things they want to track and log them as necessary. Metrics can then be pulled from the events.

We all know that manual self recorded data isn't exactly accurate, but this isn't intended to be anything serious :)
Besides the data is designed to be relevant only the user inputting the metrics, not to a scientific level, so there is a consistency of result that comes from the consistent bias of a user

# Goal
- [ ] Create base event fields: Words, Numbers, Checkbox, Rating
- [ ] Allow users to construct event types to track
- [ ] Allow users to fill in details to log an event
- [ ] Validate that event matches constructed type
- [ ] Create API to send events to
- [ ] Create query endpoint for API to get events
- [ ] Create easy metrics from query API

# Concepts

### Event Definition
The definition of an event, created by a user, which is something that a user wants to track. Users log events against a definition, allowing metrics over time.

All event definitions have a title (immutible, at least initially) and a description (mutable) as well as up to 10 fields.

Once an event definition is created it can have fields added to it, but not removed or altered

### Events
An event is a thing that has happened in a users life that is tracked. An event is entered into the app using an event definition they have created.

### Fields
A field is associated with an event. All fields have a title which is created by the user and a type which restricts the data that can be entered into it.

Fields can be be added to an event def

### Title
A human friendly string that is created by a user when creating an event definition or adding a field to an event definition
Effort will be taken to ensure that titles between event types are shared when possible in order to keep vocabulary controlled

### User
A user uses the app (dur). Users create event definitions using fields and titles, then log events as time goes by