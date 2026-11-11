# jadwal-kerja

Feed iCalendar (.ics) jadwal kegiatan Martino, dibaca Google Calendar.

## URL langganan

Google Calendar -> Other calendars -> tombol + -> From URL, tempel:

    https://raw.githubusercontent.com/MartinoKelvin/jadwal-kerja/main/jadwal.ics

## Isi

- agenda rutin mingguan (kuliah, blok TA di kafe, lari, gereja) - berulang tiap minggu
- acara sekali jalan (sempro, ujian, janji)
- pengecualian khusus satu tanggal (mis. lari dihapus, bimbingan jam 10-12)
- deadline tugas

## Cara update

File `jadwal.ics` di repo ini DIHASILKAN OTOMATIS, jangan diedit manual.
Data aslinya ada di laptop: `C:\Users\marti\jadwal-kerja\jadwal.json`.
Ubah file itu (atau minta Hermes), lalu:

    python C:/Users/marti/AppData/Local/hermes/scripts/jadwal_ics.py
    cd C:/Users/marti/jadwal-kerja/repo && git add -A && git commit -m "update jadwal" && git push

## Catatan

- Google menarik ulang feed ini kira-kira tiap 8-24 jam dan itu tidak bisa dipaksa.
- Google mengabaikan alarm yang tertulis di dalam file .ics. Notifikasi diatur
  sekali di Google Calendar: Settings -> kalender "Jadwal Martino" -> Event notifications.
- Pengingat cepat (malam 20.00, pagi sebelum agenda pertama, deadline H-24 jam)
  dikirim lewat Telegram oleh Hermes yang jalan di laptop.
