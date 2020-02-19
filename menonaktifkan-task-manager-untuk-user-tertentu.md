# Menonaktifkan Task Manager Untuk User Tertentu

Ada suatu pekerjaan SCADA yang customernya berharap agar akses terhadap aplikasi dan fitur windows dibatasi. Sehingga ketika user operator login ke windows, user tersebut hanya bisa menggunakan fitur yang disediakan pada aplikasi SCADA.

Cara yang saya lakukan adalah dengan menonaktifkan akses ke windows explorer dan task manager.

Pada pembahasan kali ini saya akan membahas bagaimana caranya untuk menonaktifkan task manager.

Silahkan ikuti langkah-langkah berikut:

1. Buat user baru, misalnya operator, kemudian set password untuk user tersebut.
2. Tambahkan user baru tade ke group Administrators **(ini hanya sementara)**.
3. Login menggunakan akun yang baru dibuat.
4. Buka regisry editor.
5. Navigasi ke:  
   _HKEY_CURRENT_USER/Software/Microsoft/Windows/CurrentVersion/Policies/System_  
   Jika key system belum ada, silahkan ditambahkan.
6. Di dalam path system, tambahkan nilai DWORD 32 bit dengan nama DisableTaskMgr dan set nilainya menjadi 1
7. Kalau sudah, silahkan logout, kemudian login lagi untuk menguji.
