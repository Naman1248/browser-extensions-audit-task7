# browser-extensions-audit-task7
Firefox extension audit – FoxyProxy permissions review, risk analysis, CSV log, screenshots, and security best practices.

## Objective
Audit installed browser extensions, identify suspicious or unnecessary ones, and take appropriate action (disable/remove).

---

## Steps Performed
1. **Checked installed extensions** in Firefox (`about:addons` → Extensions tab).
2. Found only **one extension**: FoxyProxy.
3. Opened its **Details** page and reviewed:
   - Permissions
   - Private Windows access
   - Developer info & update history
4. **Permissions Analysis**:
   - Required: Download files, modify download history, control proxy settings, access browser tabs.
   - Optional: Clear history/cookies, modify privacy settings, access data for all websites.
   - Risk flags: Broad all-sites access (`*://*/*`), modifies privacy settings, high control over browser settings.
5. **Decision**:
   - Kept the extension (needed for proxy switching on Kali Linux).
   - Disabled unnecessary optional permissions and Private Windows access.
6. **Verification**:
   - Checked `about:performance` → No unusual CPU/memory usage.
   - Browsing behavior normal; no pop-ups or redirects.

---

## Evidence
Screenshots in `screenshots/` folder:
- firefox_extensions_list.png
- foxyproxy_permissions.png
- foxyproxy_details.png

---

## Conclusion
Even with a single extension, the audit process ensures awareness of permissions and potential risks. Regular audits are recommended to maintain browser security.

---

## Best Practices
- Install extensions only from official sources (AMO/Chrome Web Store).
- Review permissions before installing.
- Disable/remove unused extensions.
- Disable Private Windows/Incognito access unless required.
- Periodically review installed extensions.
