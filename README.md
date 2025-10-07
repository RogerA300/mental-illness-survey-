# mental-illness-survey
visualization for mental illness survey 


import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
df = pd.read_csv('E:/Mental Health/survey.csv')



# 📊 Step 1: Import Libraries
import matplotlib.pyplot as plt
import seaborn as sns

# Set global style for visuals
sns.set(style='whitegrid', palette='muted')
plt.rcParams['figure.figsize'] = (7,5)

# -----------------------------------------
# 1️⃣ Overall Mental Health Treatment Distribution
# -----------------------------------------
df['treatment'].value_counts().plot(kind='bar', color=['#5DADE2', '#48C9B0'])
plt.title('Distribution of Mental Health Treatment', fontsize=14, fontweight='bold')
plt.xlabel('Treatment')
plt.ylabel('Count')
plt.xticks(rotation=0)
plt.show()

# -----------------------------------------
# 2️⃣ Mental Health Treatment by Gender
# -----------------------------------------
plt.figure(figsize=(7,5))
sns.countplot(data=df, x='Gender', hue='treatment', palette='coolwarm')
plt.title('Mental Health Treatment by Gender', fontsize=14, fontweight='bold')
plt.xlabel('Gender')
plt.ylabel('Count')
plt.legend(title='Treatment')
plt.xticks(rotation=45)
plt.show()

# -----------------------------------------
# 3️⃣ Treatment by Family History
# -----------------------------------------
plt.figure(figsize=(6,5))
sns.countplot(data=df, x='family_history', hue='treatment', palette='mako')
plt.title('Treatment by Family History', fontsize=14, fontweight='bold')
plt.xlabel('Family History of Mental Illness')
plt.ylabel('Count')
plt.legend(title='Treatment')
plt.show()

# -----------------------------------------
# 4️⃣ Work Interference vs. Treatment
# -----------------------------------------
plt.figure(figsize=(7,5))
sns.countplot(data=df, x='work_interfere', hue='treatment', palette='viridis')
plt.title('Work Interference vs. Treatment', fontsize=14, fontweight='bold')
plt.xlabel('Work Interference Level')
plt.ylabel('Count')
plt.legend(title='Treatment')
plt.show()

# -----------------------------------------
# 5️⃣ Company Size vs. Treatment
# -----------------------------------------
plt.figure(figsize=(8,5))
sns.countplot(data=df, x='no_employees', hue='treatment', palette='plasma')
plt.title('Company Size vs. Mental Health Treatment', fontsize=14, fontweight='bold')
plt.xlabel('Number of Employees')
plt.ylabel('Count')
plt.legend(title='Treatment')
plt.xticks(rotation=45)
plt.show()
