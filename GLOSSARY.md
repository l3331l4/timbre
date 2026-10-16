# Timbre

A discovery engine for underground electronic music that finds tracks by how they actually sound, not by genre tags or listening patterns.

## People

**User**:
Someone hunting for new music by sound, usually starting from tracks they already love.
_Avoid_: Digger, listener, fan

**Producer**:
A User who searches for a particular sound to use in their own work, sometimes starting from their own audio.
_Avoid_: Artist (when meaning the searcher), creator

## Music

**Track**:
A single piece of music; the thing a User finds and listens to.
_Avoid_: Song, item, result

**Segment**:
A contiguous section of a Track whose sound is analysed on its own, so matches can point to where a Track sounds a certain way.
_Avoid_: Clip, chunk, section, window

**Artist**:
Whoever made a Track.
_Avoid_: Creator, producer (when meaning the maker of a Track)

**Release**:
A published group of Tracks, such as an album, EP or single.
_Avoid_: Record, drop

**Label**:
The organisation that put out a Release.
_Avoid_: Imprint, publisher

**Source**:
The original page where a Track lives, such as its Bandcamp or SoundCloud page; Users follow it to listen.
_Avoid_: Origin, link, URL

**Catalogue**:
Every Track Timbre has analysed and can recommend. A Track whose Source has disappeared can no longer be recommended.
_Avoid_: Library, index, database

**Scene Label**:
A genre or scene name attached to a Track as metadata; it can filter results but never affects similarity.
_Avoid_: Genre (as a similarity signal), tag, category

## Sound

**Sonic Profile**:
Everything Timbre knows about how a Track or Segment sounds.
_Avoid_: Texture, timbre, sound signature, fingerprint

**Descriptor**:
One named, human-readable dimension of a Sonic Profile, such as transient weight. A Descriptor is either scalar (an amount) or categorical (a kind), and scalar values are judged relative to the rest of the Catalogue.
_Avoid_: Feature, attribute, parameter

**Listening Notes**:
A short written description of how a Track sounds and where it changes, written by an Annotating Agent.
_Avoid_: Description, caption, review

### Descriptors

**Transient Weight**: How hard and punchy the attacks are. Scalar.

**Distortion Character**: The kind of distortion, such as clipping, bitcrush, tape saturation, fuzz, or wavefolding. Categorical.

**Distortion Amount**: How much distortion there is. Scalar.

**Density**: How busy the sound is: how many events happen and how full the arrangement is. Scalar.

**Micro-dynamics**: How much small-scale movement the sound has, from static and squashed to alive with detail. Scalar.

**Low-end Weight**: How much energy sits in the sub and bass. Scalar.

**Spectral Tilt**: How dark or bright the overall sound is. Scalar.

**Noise Content**: How tonal or noisy the sound is. Scalar.

**Rhythmic Regularity**: How closely the rhythm follows a straight grid, from strict to broken or arrhythmic. Scalar.

**Space**: How dry or cavernous the sound is. Scalar.

## Searching

**Search**:
A request for Matches: a Seed, plus optional Steering and Filters.
_Avoid_: Query, lookup

**Seed**:
A Track, or a time range within one, that a Search starts from ("more like this"). Any Source can be a Seed, even one not yet in the Catalogue.
_Avoid_: Query track, reference, anchor

**Steering**:
A plain-language change to a Search relative to its Seed ("this, but crunchier and with more distorted vocals"). Steering builds up, one phrase after another, until it is cleared or the Seed changes.
_Avoid_: Text search, prompt, tuning, adjusting

**Match**:
A Track returned by a Search, together with why it matched (the Segments that matched, the Descriptors they share, and how it fits any Steering) and where in the Track to start listening.
_Avoid_: Result, hit, recommendation

**Filter**:
A condition that removes Tracks from a Search's Matches without affecting their order, such as by Scene Label or Obscurity.
_Avoid_: Facet, constraint

**Obscurity**:
How little-known a Track is, judged from play and supporter counts on its Source. Used only as a Filter.
_Avoid_: Popularity, rarity

**Gap**:
A Search where the Catalogue holds nothing close; it sends Digging Agents to dig in that direction.
_Avoid_: Miss, cold spot, empty result

## Agents

**Digging Agent**:
An agent that works in the background to find new Tracks and add them to the Catalogue.
_Avoid_: Crawler, scraper, bot

**Starting List**:
The hand-picked Artists, Labels and fan collections that Digging Agents first dig from to fill the Catalogue.
_Avoid_: Seed list, whitelist

**Annotating Agent**:
An agent that listens to Tracks and describes their sound.
_Avoid_: Tagger, labeller, classifier

## Evaluation

**Judgement**:
One person's answer to "does Track A sound closer to B or to C?", given by ear and used to measure whether Timbre hears the way Users do.
_Avoid_: Label, rating, triplet (in prose)

**Blind Comparison**:
A test where someone rates Timbre's Matches and another recommender's picks for the same Seed, shuffled together without knowing which came from where.
_Avoid_: A/B test, user study
