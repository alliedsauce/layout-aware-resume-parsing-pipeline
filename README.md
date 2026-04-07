# A Layout-Aware Resume Parsing Pipeline Using YOLO, OCR, and NLP

## Project Overview

โครงการนี้มีเป้าหมายเพื่อพัฒนาระบบ **Resume Parsing แบบ Layout-Aware** สำหรับแปลงเรซูเม่ในรูปแบบภาพหรือ PDF ซึ่งเป็นเอกสารที่ไม่มีโครงสร้าง ให้กลายเป็นข้อมูลเชิงโครงสร้างโดยอัตโนมัติ ระบบถูกออกแบบให้เข้าใจทั้งการจัดวางของเอกสาร (layout) และความหมายของข้อความ (semantic content) ร่วมกัน เพื่อรองรับเรซูเม่ที่มีรูปแบบหลากหลาย

ระบบใช้สถาปัตยกรรมแบบ **Hybrid Pipeline** โดยผสานเทคนิคจาก Computer Vision, Optical Character Recognition (OCR) และ Natural Language Processing (NLP) เริ่มจากการตรวจจับโครงสร้างของเรซูเม่ด้วย YOLO จากนั้นดึงข้อความด้วย OCR และประมวลผลเชิงความหมายเพื่อสร้างผลลัพธ์ในรูปแบบข้อมูลเชิงโครงสร้าง (Structured JSON)

โครงการนี้ได้รับแรงบันดาลใจจากงานวิจัยเรื่อง  
**“A Hybrid OCR–XGBoost–Transformer Pipeline for Resume Parsing with Spatial‑Semantic Integration”**

---

## Problem Statement

เรซูเม่มักอยู่ในรูปแบบเอกสารที่ไม่มีโครงสร้าง เช่น PDF หรือรูปภาพ และมีการจัดวางข้อมูลที่แตกต่างกันไป ข้อมูลที่มีความหมาย เช่น Education, Experience และ Skills จึงไม่สามารถดึงออกมาใช้งานโดยอัตโนมัติได้ง่าย ระบบที่พึ่งพาการประมวลผลข้อความเพียงอย่างเดียวหรือกฎแบบตายตัวมักไม่สามารถรองรับความหลากหลายของรูปแบบเรซูเม่ได้อย่างมีประสิทธิภาพ

ปัญหาหลักคือการขาดระบบที่สามารถใช้ทั้งตำแหน่งของข้อความในเอกสารและความหมายของเนื้อหาร่วมกัน เพื่อแยกส่วนข้อมูลสำคัญและแปลงเรซูเม่ที่ไม่มีโครงสร้างให้เป็นข้อมูลเชิงโครงสร้างได้อย่างถูกต้อง

---

## Objectives

- พัฒนาระบบ Resume Parsing แบบ **Layout-Aware**
- ผสานเทคนิคจาก **Computer Vision, OCR และ NLP** ในรูปแบบ Hybrid Pipeline
- แยกส่วนประกอบหลักของเรซูเม่ เช่น Education, Experience และ Skills โดยอัตโนมัติ
- ดึงข้อมูลเชิงความหมายจากแต่ละส่วนของเรซูเม่ได้อย่างเป็นระบบ
- แปลงเรซูเม่ที่ไม่มีโครงสร้างให้เป็นข้อมูลเชิงโครงสร้าง (Structured JSON)

---

## Dataset Description

ชุดข้อมูลที่ใช้ประกอบด้วย **เรซูเม่จำนวน 200 ใบ** ในรูปแบบไฟล์ภาพและ PDF โดยมีความหลากหลายของโครงสร้างการจัดวาง และใช้ทั้งภาษาไทยและภาษาอังกฤษ ข้อมูลชุดนี้ถูกใช้เพื่อทดสอบความสามารถของระบบในการตรวจจับโครงสร้างเอกสารและดึงข้อมูลจากเรซูเม่ที่ไม่มีโครงสร้าง

---

## Tools & Libraries
- **YOLO** – ตรวจจับโครงสร้างและส่วนประกอบของเรซูเม่  
- **OpenCV** – จัดการและประมวลผลภาพ  
- **OCR Engine (EasyOCR / Tesseract)** – แปลงข้อความจากภาพ  
- **spaCy** – ประมวลผลภาษาธรรมชาติและดึงข้อมูลเชิงความหมาย  
- **Python** – ภาษาหลักในการพัฒนาระบบ  

---

## Methodology







---

## System Architecture

Resume Image / PDF
↓
Layout Detection (YOLO)
↓
Section-based Cropping
↓
Optical Character Recognition (OCR)
↓
Semantic Information Extraction (NLP / NER)
↓
Structured Resume Output (JSON)

---

## Experimental / Sample Results



---

