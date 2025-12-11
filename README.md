# RWRS stats history backup

This repository contains two CSV files which are the database export of all the players' stats history on official **Invasion** and **WW2 DLCs** servers, as saved by the now-defunct [RWRS](https://github.com/EpocDotFr/rwrs) (rwrstats.com) project. Exports were made the day RWRS shut down (december 12, 2025).

Stats history was only recorded for the 5000 most experienced players, and had a data retention policy of one year per RWR account, so not everyone will be present in these files.

Both files are structured as follows:

- Column separator: `,`
- Enclosure: `"`
- Escape char: `\\`
- Line terminator: `\n`
- Columns (in that order):
  - `username` (string) Name of the RWR account as shown in-game
  - `timestamp` (string) [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) date of the stats
  - `xp` (int) Experience
  - `kills` (int) Number of soldiers killed
  - `deaths` (int) Number of times died
  - `time_played` (int) Number of seconds played
  - `longest_kill_streak` (int) Highest number of killed soldiers in a row without dying
  - `targets_destroyed` (int) Number of special targets destroyed (e.g radar towers)
  - `vehicles_destroyed` (int) Number of vehicles destroyed
  - `soldiers_healed` (int) Number of soldiers healed
  - `teamkills` (int) Number of friendly soldiers killed
  - `distance_moved `(float) Number of kilometers ran
  - `shots_fired`:  (int) Number of shots fired
  - `throwables_thrown`:  (int) Number of throwables (e.g grenades) thrown

These stats must be computed by yourself (they weren't persisted in database):

  - K/D ratio: `kills / deaths`
  - Score: `kills - deaths`

See also: [rwrtrack-data](https://github.com/david-wm-sanders/rwrtrack-data)
