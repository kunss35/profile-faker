import csv
import random
import faker
import pandas as pd  # Mengimpor library pandas

# Inisialisasi faker untuk menghasilkan data palsu
fake = faker.Faker()

# Fungsi untuk menggenerate data profil
def generate_profile_data(num_profiles):
    profiles = []
    for _ in range(num_profiles):
        profile = {
            "username": fake.user_name(),
            "name": fake.name(),
            "address": fake.address().replace("\n", ", "),  # Mengganti baris baru dengan koma
            "email": fake.email()
        }
        profiles.append(profile)
    return profiles

# Fungsi untuk menyimpan data ke file CSV menggunakan pandas
def save_to_csv_with_pandas(profiles, filename):
    # Membuat DataFrame dari data profil
    df = pd.DataFrame(profiles)
    # Menyimpan DataFrame ke file CSV
    df.to_csv(filename, index=False)  # index=False agar tidak menulis index pada file CSV

# Menentukan jumlah profil yang ingin dihasilkan
num_profiles = 10  # Ubah sesuai kebutuhan

# Mengenerate data dan menyimpannya ke file CSV
profiles = generate_profile_data(num_profiles)
save_to_csv_with_pandas(profiles, 'profile.csv')

print(f"{num_profiles} profil telah berhasil dibuat dan disimpan ke 'profile.csv'")
