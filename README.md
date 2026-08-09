
## الدليل الشامل لتصميم لوحة إلكترونية لكلب روبوتي

## Comprehensive Guide: Robot Dog PCB Design


### **المرحلة الأولى: تصميم المخطط الإلكتروني (Phase 1: Schematic Design)**

#### **الخطوة 1: تهيئة مساحة العمل / Step 1: Workspace Initialization**

* من الواجهة الرئيسية لبرنامج EasyEDA (الوضع القياسي Standard Mode)، يتم النقر على "New Project" لإنشاء مشروع جديد.
* تُفتح ورقة عمل فارغة باسم (Sheet_1) تحتوي على شبكة رسم لتسهيل وضع المكونات.
* From the EasyEDA main interface (Standard Mode), click on "New Project".
* A blank schematic sheet named (Sheet_1) opens with a grid to facilitate component placement.

![img alt](https://github.com/taleensami001-lgtm/Design-a-double-layer-PCB-for-a-robot-dog/blob/da23aa2d2da2e780a91a0f2b779c0f4b6f187d45/Screenshot%202026-08-08%20152418.png)
![img alt](https://github.com/taleensami001-lgtm/Design-a-double-layer-PCB-for-a-robot-dog/blob/a5342aeb99c68b5c94c112182042ada3d35933c8/Screenshot%202026-08-08%20153036.png)

#### **الخطوة 2: إدراج المكونات الأساسية / Step 2: Inserting Main Components**

* باستخدام محرك البحث، يتم البحث عن "arduino" واختيار "ARDUINO_NANO" من مكتبة LCSC.
* يتم وضع رمز المتحكم (U1) في مساحة العمل.
* لإدارة الطاقة، يتم البحث عن وحدة "mt3608" واختيارها.
* يتم وضع وحدة رفع الجهد (M1) التي تحمل اسم "MT3608 2A BOOST MODULE" بجوار المتحكم.
* Using the search engine, search for "arduino" and select "ARDUINO_NANO" from the LCSC library.
* The microcontroller symbol (U1) is placed in the workspace.
* For power management, search for and select the "mt3608" module.
* The boost converter module (M1), labeled "MT3608 2A BOOST MODULE", is placed next to the microcontroller.

![img alt](https://github.com/taleensami001-lgtm/Design-a-double-layer-PCB-for-a-robot-dog/blob/2502269a388fa6483fde853d44a60df21ae4ba6e/Screenshot%202026-08-08%20183716.png)
![img alt](https://github.com/taleensami001-lgtm/Design-a-double-layer-PCB-for-a-robot-dog/blob/7674916547f85cefcea0c1daf50b7cfaa2d7d07e/Screenshot%202026-08-08%20184458.png)


#### **الخطوة 3: إضافة منافذ الطاقة / Step 3: Adding Power Connectors**

* يتم البحث عن موصلات ثنائية باستخدام "connector 2P" واختيار "2.0-2P ZZDK-R PCB CONNECTOR".
* يتم وضع الموصل الأول (CN1)، ثم يضاف الموصل الثاني (CN2).
* Search for two-pin connectors using "connector 2P" and select "2.0-2P ZZDK-R PCB CONNECTOR".
* Place the first connector (CN1), followed by the second connector (CN2).

![img alt]()

#### **الخطوة 4: التوصيل الكهربائي الأولي (Power Wiring) / Step 4: Initial Power Wiring**

* تُوصل أطراف الموصلين (CN1 و CN2) بمداخل وحدة الطاقة (VIN- و VIN+).
* تُوصل مخارج وحدة MT3608 (وهي VOUT- و VOUT+) بدبابيس الأردوينو رقم 29 (GND) ورقم 27 (+5V) على التوالي.
* للتنظيم، يتم إضافة رموز التأريض (GND) لمسار VOUT- وللدبوس رقم 4 في الأردوينو.
* The pins of connectors (CN1 and CN2) are wired to the power module inputs (VIN- and VIN+).
* The MT3608 outputs (VOUT- and VOUT+) are wired to Arduino pins 29 (GND) and 27 (+5V) respectively.
* For organization, Ground (GND) symbols are added to the VOUT- net and Arduino pin 4.

![img alt]()

#### **الخطوة 5: توصيل منافذ السيرفو / Step 5: Connecting Servo Ports**

* تُضاف أربعة منافذ رأسية (Headers 3x1) بأسماء (U2, U3, U4, U5) لتمثيل محركات السيرفو.
* تُوصل دبابيس الطاقة للأربعة منافذ بالخطوط المشتركة للجهد والتأريض، بينما تُوصل دبابيس الإشارة بالمنافذ الرقمية للأردوينو (مثل D2, D3, D4, D5).
* Four 3x1 headers (U2, U3, U4, U5) are added to represent the servo motor ports.
* The power pins of the four ports are tied to the common power and ground rails, while the signal pins are routed to the Arduino's digital pins (e.g., D2, D3, D4, D5).
![img alt]()


#### **الخطوة 6: إعداد أبعاد اللوحة / Step 6: Board Dimensions Setup**

* عند تحويل المخطط إلى PCB، يتم تحديد الأبعاد (مستطيل Rectangular، العرض 75 مم، الارتفاع 35 مم).
* يتم اختيار لوحة بطبقتين نحاسيتين (Copper Layer 2) استجابة لمتطلبات المهمة.
* When converting the schematic to a PCB, dimensions are set (Rectangular, Width 75 mm, Height 35 mm).
* A 2-layer copper board is selected to meet task requirements.

![img alt]()

#### **الخطوة 7: الترتيب الفيزيائي للمكونات / Step 7: Physical Component Placement**

* يتم وضع الأردوينو (U1) في المنتصف، ووحدة الطاقة (M1) مع الموصلات (CN1, CN2) في الأسفل.
* تُرتب منافذ السيرفو (U2-U5) في الأعلى مع إضافة منفذ حساس سداسي الدبابيس (U6) في الزاوية العلوية اليمنى.
* Place the Arduino (U1) centrally, with the power module (M1) and connectors (CN1, CN2) at the bottom.
* The servo ports (U2-U5) are aligned at the top, and a 6-pin sensor port (U6) is placed in the top right corner.

  ![img alt]()

#### **الخطوة 8: رسم المسارات وصب النحاس / Step 8: Routing and Copper Pour**

* يتم استخدام الطبقة العلوية الموضحة باللون الأحمر (TopLayer) والطبقة السفلية باللون الأزرق (BottomLayer) لرسم المسارات بين المكونات بدون تقاطعات.
* تُضاف طبقة صب نحاس (Copper Pour) باللون الأحمر تملأ المساحات الفارغة من اللوحة لتقليل التشويش.
* The top layer (red) and bottom layer (blue) are used to route traces between components without short circuits.
* A red copper pour is applied over the empty board areas to minimize electrical noise.

![img alt]()
#### **الخطوة 9: المعاينة ثلاثية الأبعاد / Step 9: 3D Visualization**

* للتحقق من المظهر النهائي، يتم النقر على أيقونة "3D" في شريط الأدوات العلوي.
* تظهر اللوحة مجسمة باللون الأزرق الداكن، حيث تظهر دبابيس الأردوينو وأماكن لحام MT3608 ومنافذ التوصيل بشكلها الفيزيائي الواقعي، مما يؤكد صحة التصميم.
* To verify the final look, click the "3D" icon in the top toolbar.
* The board renders in 3D with a dark blue solder mask, displaying the Arduino pins, MT3608 pads, and connectors in their physical form, confirming the design's accuracy.

  ![img alt]()
