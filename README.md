
#### **الخطوة الأولى: تحليل متطلبات المهمة / Step 1: Analyzing Task Requirements**.

* **المهمة:** تصميم لوحة PCB خاصة بكلب روبوتي بحيث تكون اللوحة مزدوجة الطبقات (Double Layer PCB).
* **المكونات المطلوبة:** يجب أن تحتوي اللوحة على متحكم (Arduino Nano أو ESP32)، وأربعة منافذ لتوصيل محركات السيرفو، ومنفذ للبطارية، ومنفذ إضافي لحساس، مع مراعاة ترتيبها بشكل منطقي.
* **The Task:** Design a double-layer PCB for a robot dog.
* **Required Components:** The board must include a controller (Arduino Nano or ESP32), four ports for servo motors, a battery port, and an additional sensor port, all arranged logically.

#### **الخطوة الثانية: إعداد مساحة العمل واللوحة / Step 2: Board and Workspace Setup**

يتم إنشاء مساحة عمل جديدة للوحة وضبط الأبعاد لتتناسب مع حجم المكونات.

* تم تحديد وحدة القياس بالمليمتر (mm)، وتم اختيار شكل اللوحة ليكون مستطيلاً (Rectangular).
* تم ضبط أبعاد اللوحة بحيث يكون العرض 75 مم والارتفاع 35 مم.
* تم اختيار طبقتين من النحاس (Copper Layer: 2) لتلبية شرط المهمة باستخدام لوحة مزدوجة الطبقات.
* The measurement unit is set to millimeters (mm), and a Rectangular board outline is selected.
* The dimensions are configured to a width of 75 mm and a height of 35 mm.
* Two copper layers (Copper Layer: 2) are selected to fulfill the task's double-layer requirement.

#### **الخطوة الثالثة: ترتيب المكونات / Step 3: Component Placement**

يتم إدراج المكونات وترتيبها بشكل منظم داخل حدود اللوحة لضمان سهولة التوصيل لاحقاً.

* تم وضع متحكم Arduino Nano (المشار إليه بـ U1) في منتصف اللوحة.
* تم ترتيب أربعة منافذ لمحركات السيرفو (U2, U3, U4, U5) في الجزء العلوي الأيسر.
* تم وضع منفذ الحساس (U6) في الجزء العلوي الأيمن، بالإضافة لوحدة رفع الجهد MT3608 ومنافذ الطاقة (CN1, CN2) في مساحات مناسبة داخل الإطار البنفسجي للوحة.
* The Arduino Nano microcontroller (labeled U1) is placed centrally on the board.
* Four servo motor ports (U2, U3, U4, U5) are aligned neatly at the top left.
* The sensor port (U6) is placed at the top right, while the MT3608 boost converter and power connectors (CN1, CN2) are positioned within the purple board outline.

#### **الخطوة الرابعة: توصيل المسارات / Step 4: Routing the Connections**

في هذه المرحلة، يتم رسم المسارات النحاسية لربط المكونات ببعضها كهربائياً.

* تُستخدم الطبقة العلوية (TopLayer)، والموضحة باللون الأحمر، لتوصيل المسارات الأساسية بين الدبابيس.
* تُستخدم الطبقة السفلية (BottomLayer)، والموضحة باللون الأزرق، لتفادي تقاطع الخطوط وإكمال الدائرة بشكل سليم.
* The top layer (TopLayer), shown in red, is used for primary routing between component pins.
* The bottom layer (BottomLayer), shown in blue, is utilized to avoid intersecting lines and properly complete the circuit.

#### **الخطوة الخامسة: صب النحاس / Step 5: Copper Pour**

* تمت إضافة طبقة صب نحاس (Copper Pour) باللون الأحمر تغطي المساحات الفارغة من اللوحة، وهو إجراء يُستخدم غالباً لتحسين الأداء الكهربائي وتقليل التشويش.
* A red copper pour is applied to cover the empty areas of the board, a common practice used to enhance electrical performance and reduce noise.

#### **الخطوة السادسة: العرض ثلاثي الأبعاد / Step 6: 3D Visualization**

الخطوة الأخيرة هي معاينة التصميم للتأكد من المظهر الفيزيائي.

* من خلال شريط الأدوات العلوي، يتم الضغط على خيار "3D" لإنشاء نموذج مجسم.
* يعرض النموذج ثلاثي الأبعاد اللوحة بلون أزرق، وتظهر المكونات مثل متحكم Arduino Nano، والدبابيس، وأماكن لحام MT3608 مثبتة في أماكنها الصحيحة للتحقق من عدم وجود تداخل فيزيائي.
* Using the top toolbar, the "3D" option is clicked to generate a physical model.
* The 3D model renders a blue PCB showing components like the Arduino Nano, header pins, and MT3608 solder pads properly mounted, verifying that there are no physical collisions.
