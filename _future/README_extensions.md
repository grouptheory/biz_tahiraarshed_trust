# Extensions Directory

This directory is reserved for future extensions to the Trust record-keeping system.

## Purpose

New types of documents and event categories can be developed here before being promoted to the main numbered directory structure (01_instrument, 02_parties, etc.).

## How to Extend

1. Create new subdirectories in `_future/` for your new document categories
2. Add event type mappings to `future_mappings` in `.event_directories.json`
3. Create templates in `templates/` directory
4. Test and refine the new event types
5. Once stable, move the directories to numbered locations (e.g., `11_new_category/`)
6. Update `.event_directories.json` to move mappings from `future_mappings` to `event_directories`

## Example

If you want to add "charitable_giving" tracking:
- Create `_future/charitable/grants/`
- Add `"charitable_grant": "_future/charitable/grants"` to `future_mappings`
- Create template `templates/charitable_grant.md`
- Test it
- Move to `11_charitable/grants/` and update config
