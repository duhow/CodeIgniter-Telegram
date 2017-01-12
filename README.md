# DEPRECATED - See [Telegram-PHP](https://github.com/duhow/Telegram-PHP).
All future updates will be available in [Telegram-PHP](https://github.com/duhow/Telegram-PHP).

# CodeIgniter-Telegram

- Configure *config/telegram.php* with Telegram API data.
- Configure *config/autoload.php* for *config* and *model*, or run when needed.
- Set a page as webhook and be sure to run the model Telegram.

# Usage

Once the page is loaded (manually or via webhook), you can send or reply the requests.

To send a message to a user or group chat:
```php
$this->telegram->send
  ->chat("123456")
  ->text("Hello world!")
->send();
```

To reply a user command:
```php
if($this->telegram->text_command("start")){
  $this->telegram->send
    ->text("Hi!")
  ->send();
}
```

To reply a user message:
```php
if($this->telegram->text_has("are you alive")){
  $this->telegram->send
    ->text("Yes!")
  ->send();
}
```

# Examples
- [Profesor Oak](https://github.com/duhow/ProfesorOak), an assistant for Pokemon GO.
