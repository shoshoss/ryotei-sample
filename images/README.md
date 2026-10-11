# 料亭 川音 LP 素材

## 写真（images/、WebP・各2サイズ）
| ファイル | 比率 | 使う場所 | alt |
|---|---|---|---|
| kawaoto_01_fv_pc_1600w / 1024w | 16:9 | ファーストビュー（PC・タブレット） | 窓の外に夜の川が見える個室 |
| kawaoto_02_fv_sp_1080w / 750w | 3:4 | ファーストビュー（スマホ） | 窓の外に夜の川が見える個室 |
| kawaoto_03_room_small_1500w / 750w | 3:2 | 選ばれる理由1、お部屋（小部屋） | 床の間のある奥の小部屋 |
| kawaoto_04_support_1500w / 750w | 3:2 | 選ばれる理由2 | 席札とお手土産をご用意する手元 |
| kawaoto_05_dish_1500w / 750w | 3:2 | 選ばれる理由3 | 季節の会席料理の椀物 |
| kawaoto_06_scene_settai_1200w / 800w | 4:3 | ご利用シーン：ご接待・ご会食 | 個室の卓に並んだ会席料理 |
| kawaoto_07_scene_enkai_1200w / 800w | 4:3 | ご利用シーン：ご宴会 | 宴席の膳が整えられた大広間 |
| kawaoto_08_scene_hoji_1200w / 800w | 4:3 | ご利用シーン：慶事・法事 | 会席の膳が並んだお部屋 |
| kawaoto_09_scene_trip_1200w / 800w | 4:3 | ご利用シーン：ご旅行・記念日 | 2名分の会席が並んだ小部屋の卓 |
| kawaoto_10_room_middle_1500w / 750w | 3:2 | お部屋（中部屋） | 6〜10名様向けのテーブル席の中部屋 |
| kawaoto_11_room_large_1500w / 750w | 3:2 | お部屋（大広間） | 襖で仕切ることができる大広間 |
| kawaoto_12_chef_1500w / 750w | 3:2 | 料理長と店の歩み | 料理長がお造りを盛り付ける手元 |

### 使い方の例
```html
<img src="images/kawaoto_03_room_small_750w.webp"
     srcset="images/kawaoto_03_room_small_750w.webp 750w, images/kawaoto_03_room_small_1500w.webp 1500w"
     sizes="(min-width: 1080px) 60vw, 100vw"
     width="1500" height="1000" loading="lazy"
     alt="床の間のある奥の小部屋">
```
* ファーストビューは `<picture>` で、スマホ（〜767px）は fv_sp、それ以外は fv_pc を出し分ける。ファーストビューの画像だけは `loading="lazy"` を付けない
* width と height を必ず指定し、読み込み時のレイアウトのずれを防ぐ

## アイコン（icons/、SVG）
| ファイル | 使う場所 |
|---|---|
| icon_fan.svg | ファーストビュー：創業昭和38年 |
| icon_people.svg | ファーストビュー：全室個室・2〜40名様 |
| icon_car.svg | ファーストビュー：八丁堀から車で5分 |
| icon_phone.svg | 電話ボタン、ヘッダーの電話番号 |
| icon_calendar.svg | Web予約ボタン |

* 線の色は `currentColor`。親要素の `color` で色が変わる（電話ボタン内では白、明るい背景では墨色）
* 装飾として使うため `aria-hidden="true"` 付き。HTMLに直接埋め込んで使う
