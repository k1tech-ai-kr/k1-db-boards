# Optional board data 1.0.0

These JSON files are data, not executable code. They are downloaded only on request; the APK retains its built-in bank.

- chess.json: 4,999 additional Lichess puzzles, CC0-1.0. Source https://database.lichess.org/#puzzles (checked 2026-10-28). The opponent's first move is applied before the puzzle starts; the remaining solution was legally replayed with python-chess. The app validates the first answer. Original puzzle IDs and source URLs are retained.
- go.json: 495 additional JGDB historical replay positions. https://pjreddie.com/projects/jgdb/ explicitly releases JGDB into the public domain (checked 2026-10-28). Full SGF main lines replayed with sgfmill; exported answers accepted by the app. Metadata is limited: do not describe these as identified 9-dan or unique best-move exercises.
- janggi.json: 159 K1-generated rule exercises, CC0-1.0, not professional records. Legal paths and king safety checked with the app engine. Any legal capture at the target square is accepted.

Existing IDs and board/turn/answer duplicates are excluded. manifest.json records byte sizes, SHA-256 and rejected candidates. Changes to existing packs require a new version; do not overwrite an immutable published data revision.

Rebuild: python scripts/board-db/export-extra-puzzles.py <corpus-directory>; python scripts/board-db/export-extra-go.py <corpus-directory>; node scripts/board-db/build-extra-packs.mjs <corpus-directory>. Corpus includes the original compressed CSV/SGF and tools-runtime; no database migration is performed. See docs/board-database.md for the earlier acquisition records.

CC0 legal text: https://creativecommons.org/publicdomain/zero/1.0/legalcode
This notice concerns these data files only and does not relicense application code.
