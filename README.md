# Impact-of-Sleep-Deprivationimport os

# ข้อความเนื้อหา Data Description ของ Sleep_Deprivation.csv
markdown_content = """# คำอธิบายข้อมูล (Data Description)

โฟลเดอร์นี้อธิบายข้อมูลที่ใช้ในโครงงาน **Sleep Deprivation and Cognitive Reaction Time Analysis**

## 1. แหล่งที่มาและสิทธิ์การใช้ข้อมูล

| หัวข้อ | รายละเอียด |
| --- | --- |
| ชื่อชุดข้อมูล | Sleep Deprivation and Cognitive Performance Dataset |
| แหล่งที่มาเดิม | ข้อมูลจากการเก็บรวบรวมเพื่อวิเคราะห์ความสัมพันธ์ระหว่างชั่วโมงการนอนหลับและเวลาตอบสนองทางปัญญา |
| ประเภทข้อมูล | ข้อมูลการทดลองและการสำรวจ (Experimental & Survey Data) 1 แถวต่อผู้เข้าร่วมการทดลอง 1 คน |

## 2. ไฟล์ในโฟลเดอร์นี้

| ตำแหน่งไฟล์ | คำอธิบาย |
| --- | --- |
| `data/raw/Sleep_Deprivation.csv` | ไฟล์ดิบตามที่รวบรวมมา **ห้ามแก้ไขด้วยมือ** มี 60 แถว และ 13 คอลัมน์ |
| `data/processed/sleep_deprivation_clean.csv` | ข้อมูลที่ล้างและจัดรูปแบบแล้ว 60 แถว และ 13 คอลัมน์ **สร้างจาก** `code/01_clean_sleep_data.py` |

วิธีสร้างไฟล์ที่ประมวลผลแล้วขึ้นใหม่: วางไฟล์ดิบที่ `data/raw/Sleep_Deprivation.csv` แล้วรันสคริปต์ภาษา Python `code/01_clean_sleep_data.py`

## 3. พจนานุกรมข้อมูล (Data Dictionary) ของ `Sleep_Deprivation.csv`

ข้อมูลทั้งหมดมี 60 แถว โดยในชุดข้อมูลนี้ไม่มีค่าว่าง (Missing Values) ตารางต่อไปนี้แสดงชื่อคอลัมน์ ชนิดข้อมูล คำอธิบาย และจำนวนค่าว่างของแต่ละคอลัมน์

| คอลัมน์ | ชนิดข้อมูล | คำอธิบาย / ค่าที่เป็นไปได้ | ค่าว่าง |
| --- | --- | --- | ---: |
| `Participant_ID` | ข้อความ | รหัสประจำตัวของผู้เข้าร่วมการทดลอง (เช่น P1, P2, ...) | 0 |
| `Sleep_Hours` | ตัวเลข | จำนวนชั่วโมงการนอนหลับเฉลี่ยต่อคืน | 0 |
| `Sleep_Quality_Score` | ตัวเลข | คะแนนประเมินคุณภาพการนอนหลับ | 0 |
| `Daytime_Sleepiness` | ตัวเลข | คะแนนระดับความง่วงในเวลากลางวัน | 0 |
| `Stroop_Task_Reaction_Time` | ตัวเลข | เวลาตอบสนองในแบบทดสอบ Stroop Task หน่วยเป็นวินาที | 0 |
| `N_Back_Accuracy` | ตัวเลข | ความแม่นยำในการทำแบบทดสอบ N-Back หน่วยเป็นเปอร์เซ็นต์ | 0 |
| `Emotion_Regulation_Score` | ตัวเลข | คะแนนการประเมินการจัดการอารมณ์ | 0 |
| `PVT_Reaction_Time` | ตัวเลข | เวลาตอบสนองจากแบบทดสอบ Psychomotor Vigilance Task (PVT) หน่วยเป็นมิลลิวินาที | 0 |
| `Age` | ตัวเลข | อายุของผู้เข้าร่วมการทดลอง หน่วยเป็นปี | 0 |
| `Gender` | ข้อความ | เพศของผู้เข้าร่วมการทดลอง ได้แก่ Female และ Male | 0 |
| `bmi` | ตัวเลข | ดัชนีมวลกาย (BMI) ของผู้เข้าร่วมการทดลอง | 0 |
| `gender_code` | ตัวเลข | รหัสตัวเลขแทนเพศ (0 สำหรับ Female และ 1 สำหรับ Male) | 0 |
| `bmi_category` | ข้อความ | หมวดหมู่ดัชนีมวลกาย ได้แก่ Normal, Overweight และ Obesity | 0 |

**หมายเหตุ**
- จำนวนค่าว่าง (Missing Values) นับจากชุดข้อมูลปัจจุบันจำนวน 60 แถว ไม่พบค่าว่างในทุกคอลัมน์
"""

# บันทึกเป็นไฟล์ Markdown
with open("Sleep_Deprivation_Description.md", "w", encoding="utf-8") as f:
    f.write(markdown_content)

print("สร้างไฟล์ Markdown สำเร็จแล้ว!")
