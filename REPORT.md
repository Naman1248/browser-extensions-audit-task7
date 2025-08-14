# REPORT – Browser Extensions Audit

## System Info
- OS: Kali Linux
- Browser: Firefox

## Extensions Summary
- Total extensions found (Firefox): 1
- Removed/Disabled: 0 (Kept for use)

## Extension Audited
**Name:** FoxyProxy  
**Version:** 9.2  
**Developer:** Eric Jung  
**Source:** AMO (addons.mozilla.org)

## Permissions Review
- **Required:** Download files & modify download history, display notifications, control proxy settings, access browser tabs.
- **Optional:** Clear history/cookies, modify privacy settings, access data for all websites.

## Risk Flags
- Broad host access (`*://*/*`)
- Ability to modify privacy settings & history
- High control over browser settings

## Decision & Action
- Kept extension (needed for proxy tasks)
- Disabled unnecessary optional permissions
- Disabled Private Windows access

## Post-cleanup Verification
- `about:performance` shows no unusual CPU/memory usage.
- No unexpected pop-ups or redirects.

## Recommendations
- Keep permissions minimal (least-privilege principle)
- Review extension updates for permission changes
- Quarterly extension audit
