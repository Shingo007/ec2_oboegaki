## 時間の変更
$ date
> Wed Oct 22 00:11:22 UTC 2025

ec2の時刻がデフォルトでUTCになってしまっている。JSTに変更する。
$ timedatectl
            Local time: Wed 2025-10-22 00:35:32 UTC
            Universal time: Wed 2025-10-22 00:35:32 UTC
            RTC time: Wed 2025-10-22 00:35:32
            Time zone: n/a (UTC, +0000)
System clock synchronized: yes
            NTP service: active
            RTC in local TZ: no

## timezoneの確認
$ sudo timedatectl list-timezones | grep Asia/Tokyo
> Asia/Tokyo

## Asia/Tokyoにする
$ sudo timedatectl set-timezone Asia/Tokyo

$ timedatectl
            Local time: Wed 2025-10-22 09:37:42 JST
            Universal time: Wed 2025-10-22 00:37:42 UTC
            RTC time: Wed 2025-10-22 00:37:42
            Time zone: Asia/Tokyo (JST, +0900)
System clock synchronized: yes
            NTP service: active
            RTC in local TZ: no

JSTに変更されている事を確認。
アプリの更新日時発行の際に忘れるから気をつける。