# Same Origin Policy

In computing, Same Origin Policy or SOP refers to an important concept in Web Application Security which states that a browser will permit a page to access another page's data if and only if the second page has the same origin as the first page. Same Origin is a combination of protocol, port (if any), and host. This policy prevents a malicious script on one page to access data of another page through that page's Document Object Model (DOM).

## The SOP only applies to scripts. This means that resources such as images, CSS, and other dynamically loaded scripts can be accessed across origins via the corresponding HTML tags. Attacks takes advantage of this that the SOP doesn't apply to HTML tags.
