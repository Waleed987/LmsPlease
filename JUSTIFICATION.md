# Chrome Web Store Privacy Justifications

## 1. Storage Permission
"The extension uses the `storage` permission to secure save the user's NUST LMS and Qalam credentials locally within their browser (using `chrome.storage.local`). This allows the extension to automatically retrieve and fill these credentials into the login forms without the user needing to type them each time. It is also used to store user preferences, such as the 'Hide CGPA' setting and the extension's enabled/disabled state. All data is stored locally on the user's device and is never transmitted to any external servers."

## 2. ActiveTab Permission
"The `activeTab` permission is requested to allow the extension to interact with the currently active tab when the user clicks the extension icon. This enables the extension to perform manual actions or status checks on the specific page the user is viewing, ensuring that the extension can function correctly even if background content script injection encounters issues. It serves as a user-initiated mechanism to grant access to the current page context."

## 3. Host Permissions
**URLs:** `https://lms.nust.edu.pk/*`, `https://www.lms.nust.edu.pk/*`, `https://qalam.nust.edu.pk/*`

"The extension requires access to these specific NUST portal domains to inject content scripts, which are the core mechanism of the extension. 
- **LMS Domain:** Scripts detect the login form on `lms.nust.edu.pk` to auto-fill credentials and handle auto-login logic.
- **Qalam Domain:** Scripts detect the login form on `qalam.nust.edu.pk` for auto-login and interact with the student dashboard DOM to implement the 'Hide CGPA' feature requested by users.
Access is strictly limited to these educational portals to provide the stated functionality."
