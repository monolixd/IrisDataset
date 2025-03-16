# 🌸 Machine Learning with Iris Dataset

## 🔰 สิ่งที่ได้เรียนรู้จากโปรเจคนี้
1. **NumPy & Pandas** สำหรับการจัดการข้อมูล
2. **Matplotlib & Seaborn** สำหรับ Data Visualization
3. **Machine Learning (Random Forest)** สำหรับจำแนกสายพันธุ์ดอกไอริส
4. **Train-Test Split (80-20%)** และการประเมินผลโมเดลด้วย Accuracy และ Confusion Matrix

## 🔹 ตัวอย่างโค้ดที่ใช้สร้างโมเดล Machine Learning
```python
from sklearn.ensemble import RandomForestClassifier
from sklearn.model_selection import train_test_split
from sklearn.metrics import accuracy_score

# โหลดข้อมูล
X = df.drop(columns=["species"])
y = df["species"]
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=42)

# Train โมเดล
model = RandomForestClassifier(n_estimators=100, random_state=42)
model.fit(X_train, y_train)

# ทดสอบโมเดล
y_pred = model.predict(X_test)
accuracy = accuracy_score(y_test, y_pred)
print(f"Accuracy: {accuracy:.2f}")
