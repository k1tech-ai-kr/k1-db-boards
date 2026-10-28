# K1 optional board learning data

Version 1.0.0: 4,999 chess tactical first-move exercises (Lichess, CC0-1.0), 495 Go historical replay positions (JGDB, public domain), and 159 original K1 Janggi rule exercises (CC0-1.0).

Only redistributable JSON data and its provenance are published here. No application code, credentials, user records or account configuration is included. Downloads require no account or token. Consumers should pin a full commit SHA, verify manifest byte sizes and SHA-256, validate the JSON schema, then replace a pack atomically. Preserve previous data on error.

Each JSON file is an array with id, game, title, position, answer, kind, source, rights, explanation and open fields. Position boards are row-major: chess 8x8, Go 19x19, Janggi 10x9. Chess/Janggi answers are source/destination indices (chess includes promotion); Go answers are a single placement index. Historical moves are factual replay, not engine-certified unique best moves. Janggi exercises are generated, not professional games.

See [data and attribution](data-packs/boards-1.0.0/README.md) and [manifest](data-packs/boards-1.0.0/manifest.json). Source licenses concern the data only. Application code is not relicensed.

Sources checked 2026-10-28: https://database.lichess.org/ and https://pjreddie.com/projects/jgdb/ . CC0 legal text: https://creativecommons.org/publicdomain/zero/1.0/legalcode .
