<!doctype html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Chatterly</title>
    <link rel="stylesheet" href="chat-platform.css" />
  </head>
  <body>
    <main class="chat-app">
      <aside class="sidebar">
        <header class="brand-row">
          <div>
            <p class="eyebrow">Private messages</p>
            <h1>WhatsChat</h1>
          </div>
          <button id="themeToggle" class="icon-button" type="button" aria-label="Toggle theme">Dark</button>
        </header>

        <form id="addContactForm" class="add-contact">
          <div class="contact-fields">
            <label>
              <span>Contact name</span>
              <input id="contactNameInput" type="text" placeholder="Friend name" autocomplete="off" />
            </label>
            <label>
              <span>Phone number</span>
              <input id="contactPhoneInput" type="tel" placeholder="+91 98765 43210" autocomplete="off" />
            </label>
          </div>
          <button type="submit">Add</button>
        </form>

        <label class="search-box">
          <span>Search</span>
          <input id="searchInput" type="search" placeholder="Search or start new chat" />
        </label>

        <section class="contacts" id="contacts" aria-label="Chat contacts"></section>
      </aside>

      <section class="conversation">
        <header class="chat-header">
          <div class="profile">
            <div id="activeAvatar" class="avatar">A</div>
            <div>
              <h2 id="activeName">Aarav</h2>
              <p id="activeStatus">Online now</p>
            </div>
          </div>
          <div class="header-actions">
            <button class="icon-button" type="button" aria-label="Start call">Call</button>
            <button class="icon-button" type="button" aria-label="More options">...</button>
          </div>
        </header>

        <div id="messages" class="messages" aria-live="polite"></div>

        <p id="typing" class="typing" hidden>Aarav is typing...</p>

        <form id="messageForm" class="composer">
          <button class="icon-button" type="button" aria-label="Attach file">+</button>
          <input id="messageInput" type="text" placeholder="Type a message" autocomplete="off" />
          <button class="send-button" type="submit">Send</button>
        </form>
      </section>
    </main>

    <script src="chat-platform.js"></script>
  </body>
</html>
