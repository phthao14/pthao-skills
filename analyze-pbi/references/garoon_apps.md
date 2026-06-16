# Garoon Apps — Help URL Mapping

Base URL: `https://jp.cybozu.help/g/en/`

| App | User Help | Admin Help |
|---|---|---|
| Scheduler | /user/application/scheduler/ | /admin/application/scheduler/ |
| Workflow | /user/application/workflow/ | /admin/application/workflow/ |
| Messages | /user/application/messages/ | /admin/application/messages/ |
| Space | /user/application/space/ | /admin/application/space/ |
| Bulletin Board | /user/application/bulletin/ | /admin/application/bulletin/ |
| Cabinet | /user/application/cabinet/ | /admin/application/cabinet/ |
| Phone Messages | /user/application/phone/ | — |
| Memo | /user/application/memo/ | — |

## Usage

In Step 1.5, when the user names a Garoon app, use WebFetch with the corresponding URL above to understand current behavior before analyzing the PBI.

If the PBI involves admin settings, fetch the Admin Help URL as well.
