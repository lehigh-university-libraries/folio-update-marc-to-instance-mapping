# Script to refresh Instances against an+updated MARC Bib-to-Inventory Instance map
Based on the shell script at https://wiki.folio.org/display/FOLIJET/MODDATAIMP-567%3A+Script+to+refresh+Instances+against+an+updated+MARC+Bib-to-Inventory+Instance+map

> For any library storing MARC Bibliographic records in Source Record Storage (SRS), FOLIO contains a default MARC-to-Instance map. FOLIO uses that map when creating or updating Inventory Instances with Source = MARC. The map identifies the Instance fields that are controlled by the underlying MARC Bibliographic record, and which fields and subfields of MARC data populate into which Instance fields. Occasionally libraries may adjust their default map, either because of 1) updated default mappings delivered in a new FOLIO release or 2) local fields or mapping decisions that differ from the default map. When a library's default map is updated, those updated mappings will affect any Instances created or updated after the map change. However, some libraries would like to update all of their existing Instances to reflect the updated mappings. This script allows for that to happen. 

## Local Changes

- Alternate mode to process a specific list (file-based) of Instance UUIDs
- Logs progress at the end of each batch
- More cron-friendly (aborts at startup if another process is already running)
- Bash-compatible
- Stable sort of instances