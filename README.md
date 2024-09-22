import matplotlib.pyplot as plt
import pandas as pd
import numpy as np

# Sample dataset
np.random.seed(0)
ages = np.random.randint(18, 65, size=100)
genders = np.random.choice(['Male', 'Female'], size=100)

# Create DataFrame
df = pd.DataFrame({'Age': ages, 'Gender': genders})

# Bar chart: Gender Distribution
plt.figure(figsize=(8, 6))
df['Gender'].value_counts().plot(kind='bar')
plt.title('Gender Distribution')
plt.xlabel('Gender')
plt.ylabel('Frequency')
plt.show()

# Histogram: Age Distribution
plt.figure(figsize=(8, 6))
plt.hist(df['Age'], bins=np.arange(18, 70, 5), edgecolor='black')
plt.title('Age Distribution')
plt.xlabel('Age')
plt.ylabel('Frequency')
plt.show()

