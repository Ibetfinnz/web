<!DOCTYPE html>
<html lang="th">

<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>password door lock</title>
    <style>
        /* ตั้งค่าสไตล์พื้นฐาน */
        
        body {
            font-family: 'Arial', sans-serif;
            color: #f1f5f9;
            background: linear-gradient(135deg, #0f172a, #1e293b);
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            margin: 0;
            padding: 20px;
            position: relative;
        }
        
        .container {
            max-width: 800px;
            width: 100%;
            padding: 20px;
            background: rgba(30, 41, 59, 0.85);
            border-radius: 12px;
            box-shadow: 0 12px 24px rgba(0, 0, 0, 0.4);
            backdrop-filter: blur(10px);
            animation: fadeIn 1s ease-out;
            position: relative;
        }
        
        .card {
            background: linear-gradient(145deg, #334155, #475569);
            padding: 20px;
            border-radius: 12px;
            margin-bottom: 20px;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.3);
            transition: transform 0.2s ease, box-shadow 0.2s ease;
        }
        
        .card:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 16px rgba(0, 0, 0, 0.5);
        }
        
        .card-title {
            font-size: 1.8em;
            color: #60a5fa;
            font-weight: bold;
            margin-bottom: 5px;
            border-bottom: 2px solid #60a5fa;
            padding-bottom: 5px;
            text-align: center;
            font-size: 2.5em;
        }
        
        .date-author {
            display: flex;
            justify-content: space-between;
            color: #cbd5e1;
            font-size: 0.85em;
            margin-top: 5px;
        }
        
        .section-title {
            font-size: 1.4em;
            color: #60a5fa;
            font-weight: bold;
            margin-top: 15px;
        }
        
        .section-content {
            color: #e2e8f0;
            line-height: 1.7;
            margin-top: 8px;
        }
        
        @keyframes fadeIn {
            0% {
                opacity: 0;
                transform: scale(0.95);
            }
            100% {
                opacity: 1;
                transform: scale(1);
            }
        }
        /* ปุ่มด้านบนขวา */
        
        .sidebar {
            position: fixed;
            top: 20px;
            right: 20px;
        }
        
        .sidebar button {
            display: block;
            margin-bottom: 10px;
            padding: 10px;
            color: #fff;
            background: #dc2626;
            border: none;
            border-radius: 8px;
            cursor: pointer;
            font-weight: bold;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.3);
            transition: background 0.2s ease, box-shadow 0.2s ease;
        }
        
        .sidebar button:hover {
            background: #b91c1c;
            box-shadow: 0 6px 12px rgba(0, 0, 0, 0.5);
        }
    </style>
</head>

<body>
    <div class="container">
        <div class="card" id="header">
            <div class="card-title">password door lock arduino project</div>
        </div>

        <div class="card" id="abstract">
            <div class="section">
                <div class="section-title">บทคัดย่อ</div>
                <div class="section-content">
                    Project นี้เป็นการบูรณาการในการใช้งาน Microcontroller ในรายวิชา PHYSICAL COMPUTING โดยเป็นการทำเป็นHardware สำหรับระบบการทำระบบล็อกประตูโดยใส่รหัส เมื่อใส่รหัสถูกก็จะปลดล็อก เมื่อใส่รหัสผิดก็จะไม่ปลดล็อกโดยการใส่รหัสจะใส่ลงบนอุปกรณ์ Keypad โดยจะมี Micro
                    Servo เป็นการหมุนเพื่อทำการปลดล็อก และจะมีจอLCDเพื่อแสดงผล
                </div>
            </div>
        </div>

        <div class="card" id="equipment">
            <div class="section">
                <div class="section-title">อุปกรณ์</div>
                <div class="section-content">
                    <figure>
                        <figcaption>1.LCD Module</figcaption>
                        <img src="LCD_module.04a8cc1f.png" alt="LCD Module" style="max-width: 250px; height: 250px;">
                    </figure>
                    <figure>
                        <figcaption>2.Arduino Uno</figcaption>
                        <img src="Arduino Uno.png" alt="Arduino" style="max-width: 300px; height: 200px;">
                    </figure>
                    <figure>
                        <figcaption>3.4x4 Keypad Matrix</figcaption>
                        <img src="Keypad.png" alt="Keypad" style="max-width: 400px; height: 350px;">
                    </figure>
                    <figure>
                        <figcaption>4.Servo Motor</figcaption>
                        <img src="Servo.png" alt="Servo" style="max-width: 350px; height: 250px;">
                    </figure>
                </div>
            </div>
        </div>

        <div class="card" id="functions">
            <div class="section">
                <div class="section-title">ฟังก์ชันหลัก</div>
                <div class="section-content">
                    - ระบบจำลองการเข้ารหัสเพื่อปลดล็อกประตู <br> - เพื่อลดการพกกุญแจทำให้ไม่ต้องพกให้ยุ่งยาก
                </div>
            </div>
        </div>


        <div class="card" id="รูปproject">
            <div class="section">
                <div class="section-title">รูปproject</div>
                <div class="section-content">
                    <figure>
                        <img src="IMG_2656.jpg" alt="LCD Module" style="max-width: 500px; height: 500px; transform: rotate(-90deg); display: block; margin: 0 auto;">
                    </figure>
                </div>
            </div>
        </div>
        <div class="card" id="source-code">
            <div class="section">
                <div class="section-title">Source Code</div>
                <div class="section-content">
                    <pre>
        #include &lt;Servo.h&gt;
        #include &lt;Password.h&gt;
        #include &lt;LiquidCrystal_I2C.h&gt;  // ไลบรารีจอ LCD I2C
        Servo servo;
        Password password = Password("1111"); // ตั้งรหัสผ่านเป็น "1111"
        byte maxPasswordLength = 6;
        byte currentPasswordLength = 0;
        
        LiquidCrystal_I2C lcd(0x27, 16, 2);  // กำหนดที่อยู่ I2C ของ LCD
        
        // กำหนดพิน Keypad
        const byte numRows = 4;
        const byte numCols = 4;
        int rowPins[numRows] = {9, 8, 7, 6}; // พินแถวของ Keypad
        int colPins[numCols] = {5, 4, 3, 2}; // พินคอลัมน์ของ Keypad
        char keymap[numRows][numCols] = {
          {'1', '2', '3', 'A'},
          {'4', '5', '6', 'B'},
          {'7', '8', '9', 'C'},
          {'*', '0', '#', 'D'}
        };
        
        #define NO_KEY '\0'
        
        void setup() {
          Serial.begin(9600);
          servo.attach(10);  // พินที่เชื่อมต่อกับ servo
          servo.write(90);   // เริ่มต้นให้หยุดหมุน
          initializeKeypadPins();
        
          // เริ่มต้นการทำงานของจอ LCD
          lcd.init();
          lcd.backlight();
          lcd.setCursor(0, 0);
          lcd.print("Enter Password:");
        }
        
        void loop() {
          char key = scanKeypad();  // อ่านค่าจาก Keypad
        
          if (key != NO_KEY) {
            Serial.println(key); // แสดงค่าที่กดใน Serial Monitor
        
            if (key == 'C') {  // รีเซ็ตรหัสผ่านหากกดปุ่ม 'C'
              resetPassword();
            } else if (key == 'D') {  // ล็อกหรือปลดล็อกประตูเมื่อกดปุ่ม 'D'
              toggleDoor();
            } else {
              processNumberKey(key);  // จัดการกับการกดตัวเลข
            }
          }
        }
        
        // ฟังก์ชันตั้งค่า Pin สำหรับ Keypad
        void initializeKeypadPins() {
          for (int i = 0; i < numRows; i++) {
            pinMode(rowPins[i], OUTPUT);
            digitalWrite(rowPins[i], HIGH);  // ตั้งแถวเป็น HIGH
          }
          for (int i = 0; i < numCols; i++) {
            pinMode(colPins[i], INPUT_PULLUP);  // ตั้งคอลัมน์เป็น input พร้อม pull-up
          }
        }
        
        // ฟังก์ชันสแกน Keypad และรับคีย์ที่ถูกกด
        char scanKeypad() {
          for (int row = 0; row < numRows; row++) {
            digitalWrite(rowPins[row], LOW);  // ตั้งแถวปัจจุบันเป็น LOW
            for (int col = 0; col < numCols; col++) {
              if (digitalRead(colPins[col]) == LOW) {
                while (digitalRead(colPins[col]) == LOW);  // รอจนกว่าจะปล่อยคีย์
                digitalWrite(rowPins[row], HIGH);  // ตั้งแถวกลับเป็น HIGH
                return keymap[row][col];  // ส่งคีย์ที่ถูกกดกลับ
              }
            }
            digitalWrite(rowPins[row], HIGH);  // ตั้งแถวกลับเป็น HIGH
          }
          return NO_KEY;  // หากไม่มีการกดคีย์ ให้ส่งค่า NO_KEY
        }
        
        // ฟังก์ชันจัดการการกดตัวเลขบน keypad
        void processNumberKey(char key) {
          currentPasswordLength++;
          password.append(key);  // เพิ่มตัวเลขที่กดเข้ากับรหัสผ่าน
        
          // แสดงรหัสที่กดบนจอ LCD
          lcd.setCursor(currentPasswordLength - 1, 1); // ตั้งตำแหน่งของเคอร์เซอร์
          lcd.print('*');  // แสดงเครื่องหมาย '*' แทนรหัสผ่าน
        
          if (currentPasswordLength == maxPasswordLength) {
            dooropen();  // ตรวจสอบรหัสผ่านเมื่อใส่ครบ
          }
        }
        
        // ฟังก์ชันเปิดประตูเมื่อรหัสถูกต้อง
        void dooropen() {
          if (password.evaluate()) {
            Serial.println("Access Granted.");
            delay(500);
            lcd.clear();
            lcd.setCursor(0, 0);
            lcd.print("Access Granted");  // แสดงข้อความปลดล็อกบน LCD
            toggleServo(); // เรียกฟังก์ชันสลับสถานะเซอร์โว
          } else {
            Serial.println("Access Denied. Wrong Password.");
            
            lcd.clear();
            lcd.setCursor(0, 0);
            lcd.print("Access Denied!");
            delay(1000);// แสดงข้อความผิดพลาด
          }
          resetPassword();  // รีเซ็ตรหัสผ่านหลังจากเช็คเสร็จ
        }
        
        // ฟังก์ชันสลับการล็อกและปลดล็อกประตู
        void toggleDoor() {
          // ใช้ฟังก์ชันเดียวกับการเปิดประตูเพื่อให้สามารถกดรหัสอีกครั้งได้
          dooropen();
        }
        
        // ฟังก์ชันสลับสถานะเซอร์โว
        void toggleServo() {
          static bool doorOpen = false;  // ใช้ตัวแปรนี้ในการเก็บสถานะของประตู
        
          doorOpen = !doorOpen;  // สลับสถานะประตู
          if (doorOpen) {
            servo.write(180);    // หมุนไปที่ 45 องศาเพื่อปลดล็อกประตู
            delay(1000);
            Serial.println("Door Unlocked.");
            lcd.setCursor(0, 1);
            lcd.print("Door Unlocked.");
          } else {
            servo.write(90);   // หยุดการหมุนของ servo (ล็อก)
            delay(1000);
            Serial.println("Door Locked.");
            lcd.setCursor(0, 1);
            lcd.print("Door Locked.  ");
          }
        }
        
        // ฟังก์ชันรีเซ็ตรหัสผ่าน
        void resetPassword() {
          password.reset();
          currentPasswordLength = 0;  // รีเซ็ตความยาวของรหัสผ่าน
          Serial.println("Password Reset.");
          lcd.clear();
          lcd.setCursor(0, 0);
          lcd.print("Enter Password:");
        }
                    </pre>
                </div>
            </div>
        </div>
        <div class="card" id="members">
            <div class="section">
                <div class="section-title">สมาชิกผู้จัดทำ</div>
                <div class="section-content">
                    1.นาย กิตติพิชญ์ เพ็งแจ่ม รหัสประจําตัว 66070240<br>2.นาย ธิเบศ สว่างการ รหัสประจําตัว 66070272 <br>3.นาย ธนาธิป ช่างเจรจา รหัสประจําตัว 66070268
                </div>
            </div>
        </div>

    </div>


    <div class="sidebar">
        <button onclick="scrollToSection('header')">ชื่อproject</button>
        <button onclick="scrollToSection('abstract')">บทคัดย่อ</button>
        <button onclick="scrollToSection('equipment')">อุปกรณ์</button>
        <button onclick="scrollToSection('functions')">ฟังก์ชันหลัก</button>
        <button onclick="scrollToSection('รูปproject')">รูปproject</button>
        <button onclick="scrollToSection('source-code')">Source Code</button>
        <button onclick="scrollToSection('members')">สมาชิกผู้จัดทำ</button>

    </div>

    <script>
        function scrollToSection(id) {
            document.getElementById(id).scrollIntoView({
                behavior: 'smooth'
            });
        }
    </script>
</body>

</html>