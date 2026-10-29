# REVIEW — 「찢어지는 고요」

## Creative calls
- Built **storyline A** (STORYLINES.md). B「한 잎의 여행」(one leaf carried across worlds) and C「시월의 한 프레임」(one frame of letters that keeps rebuilding) were not built.
- The music sets the clock: HeyGen catalog track 341566f6, whose intro ends in near-silence at 13.9 s and whose drop lands at **14.00 s**. That gap became the film's held breath; the drop cuts land on the measured onsets (15 / 16 / 17 / 18 / 19 / 19.5 / 20 / 21 / 22 / 23.5 / 24) and the end card on the last hit at 27.0 s.
- The medium is **letters that carry a photograph inside them** (background-clip: text). Calm half: AppleMyungjo. Drop half: Apple SD Gothic Neo Heavy (both macOS system fonts via `local()`).
- All copy is original Korean. Photos are real Wikimedia Commons images (PD / CC BY / CC BY-SA), credited on the end card.

## Measured vs looked at
- `hyperframes check`: ok, 0 errors, contrast 15/15.
- Snapshots: 20 QA frames, the review sheets (beats, 4 seams, phone width 360 px) and a re-snapshot of every fixed moment.
- Music drop and onsets measured with ffmpeg RMS (0.1 s windows) and `hyperframes audio`. Each SFX is placed so its measured peak lands one frame after its picture.
- **The sound was measured, not heard.** Nobody has listened to the mix.

## Fixed in review
- 22–23.5 s: the slot montage went blank because script-swapped background images weren't loaded when the frame was seeked. Every photo is now its own layer in the HTML, toggled by opacity.
- 15 s "더" was inside the right edge's unsafe margin: moved left.
- 26.5 s "아름답다" ran into the leaf: moved into the open bokeh area at the top right.
- 18 s "듯" was filled with a dark photo and disappeared on the dark ground: swapped for the bright ginkgo.

## Weakest shot
- 20–22 s (흔들리고 / 물들고): each holds only one second on photos (England silver grass, Japan ginkgo road) that read less "October in Korea" than the rest. With more time: replace them with Korean silver-grass fields (e.g. 민둥산, 하늘공원) and give each word two beats.

## Warnings kept on purpose
- `line_unread` on 흔들리고 / 물들고 (0.96 s): single words cut on the beat in a montage. They are meant to hit, not to be read slowly.
- `line_unread` on the 시월 slot layers: a false positive. The glyphs never move; only the photo inside them changes every 0.25 s, and "시월" stays readable for 1.5 s.
- `timeline_track_too_dense` in drop.html: the seven beat panels are one musical phrase and stay in one file.
