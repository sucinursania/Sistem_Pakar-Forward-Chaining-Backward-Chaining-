# Sistem_Pakar-Forward-Chaining-Backward-Chaining-
Dalam pengembangan sistem pakar berbasis aturan menggunakan pustaka Experta di Python, saya telah melakukan penambahan 5 penyakit baru beserta gejala-gejalanya. Penambahan ini bertujuan untuk memperluas kemampuan sistem dalam memberikan diagnosis yang lebih beragam dan akurat berdasarkan fakta yang diberikan oleh pengguna.
Daftar Penyakit dan Gejala yang Ditambahkan:

Penyakit	Gejala yang Digunakan:
1	Allergic Reaction	rash=True, itching=True
2	Chickenpox	rash=True, fever=True, itching=True
3	Arthritis	joint_pain=True, fatigue=True
4	Malaria	fever=True, chills=True, joint_pain=True
5	Tuberculosis (TBC)	night_sweats=True, cough=True, fatigue=True
Setiap penyakit direpresentasikan dalam bentuk @Rule pada kelas Diagnosis, dan jika kondisi (fakta) pada rule tersebut terpenuhi, sistem akan memberikan diagnosis yang sesuai.

Contoh implementasi salah satu rule:
@Rule(Fact(rash=True) & Fact(itching=True))
def allergic_reaction(self):
    print("Diagnosis: You may have an Allergic Reaction.")
    
⚙ Penyesuaian Fungsi get_input()
Agar sistem dapat menanyakan gejala-gejala tambahan tersebut, saya juga menyesuaikan fungsi get_input() dengan menambahkan beberapa pertanyaan baru kepada pengguna:
"rash": ask_question("Do you have a skin rash?"),
"itching": ask_question("Do you feel itchy?"),
"joint_pain": ask_question("Do you have joint pain?"),
"chills": ask_question("Are you experiencing chills?"),
"night_sweats": ask_question("Do you experience night sweats?")
Hal ini memastikan bahwa semua rule yang dibuat memiliki input (fakta) yang diperlukan agar bisa dijalankan oleh sistem pakar.

Kesimpulan
Dengan penambahan 5 penyakit dan gejala-gejalanya, sistem pakar ini menjadi lebih kompleks dan mampu menangani lebih banyak kemungkinan kondisi kesehatan. Hal ini mencerminkan fleksibilitas dan skalabilitas sistem pakar berbasis aturan dalam menangani kasus nyata di bidang medis secara sederhana.

