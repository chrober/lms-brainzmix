# BrainzMix

BrainzMix is a design-stage project for ListenBrainz-powered music
continuation in [Lyrion Music Server](https://lyrion.org/).

The intended plugin would contribute **Don't Stop The Music** (DSTM) tracks
derived from ListenBrainz
[similar-recording](https://labs.api.listenbrainz.org/similar-recordings) and
[similar-artist](https://labs.api.listenbrainz.org/similar-artists) evidence.
It would prefer playable tracks from the local Lyrion library and must work
when that library contains no embedded MusicBrainz identifiers.

This repository does not yet contain a released or working plugin. The
canonical proposal is [docs/DESIGN.md](docs/DESIGN.md).

## Important prior art

[ListenBrainz Fresh Releases](https://github.com/SimonArnold002/LMS-ListenBrainz-New-Releases)
already provides substantial ListenBrainz and Lyrion integration, including
DSTM contribution, artist-name-to-MBID resolution, and local-library matching
by MBID with an artist/title fallback. BrainzMix is specifically concerned
with exposing both similar-recording and similar-artist evidence as a reusable
capability. It must not duplicate recent work without first deciding whether
to contribute upstream, collaborate on shared code, or pursue a deliberately
different scope.

## Proposed scope

- a small, focused Lyrion plugin rather than a general ListenBrainz browser;
- one similarity-based DSTM provider using the current musical context;
- similar-recording and similar-artist candidate generation;
- local-library-first track resolution;
- no requirement to retag files with MBIDs;
- explicit identity confidence and safe handling of ambiguous matches;
- a documented evidence API reusable by DSTM and other Lyrion plugins; and
- graceful offline and provider-failure behavior.

## Status

Early design and prior-art assessment. No implementation relationship with the
ListenBrainz Fresh Releases project has been agreed.
