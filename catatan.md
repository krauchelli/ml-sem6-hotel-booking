# catatan hasil pengecekan preparation section

## Data Type for Each Field

The table below lists the data type for each field in the dataset based on the provided summary:

| Field                          | Data Type |
|--------------------------------|-----------|
| Hotel                          | Object    |
| Lead Time                      | Integer   |
| Arrival Date Year              | Integer   |
| Arrival Date Month             | Object    |
| Arrival Date Week Number       | Integer   |
| Arrival Date Day of Month      | Integer   |
| Stays in Weekend Nights        | Integer   |
| Stays in Week Nights           | Integer   |
| Adults                         | Integer   |
| Children                       | Float     |
| Babies                         | Integer   |
| Meal                           | Object    |
| Country                        | Object    |
| Market Segment                 | Object    |
| Distribution Channel           | Object    |
| Is Repeated Guest              | Integer   |
| Previous Cancellations         | Integer   |
| Previous Bookings Not Canceled | Integer   |
| Reserved Room Type             | Object    |
| Assigned Room Type             | Object    |
| Booking Changes                | Integer   |
| Deposit Type                   | Object    |
| Agent                          | Float     |
| Company                        | Float     |
| Days in Waiting List           | Integer   |
| Customer Type                  | Object    |
| ADR                            | Float     |
| Required Car Parking Spaces    | Integer   |
| Total of Special Requests      | Integer   |
| Reservation Status             | Object    |
| Reservation Status Date        | Object    |
| Name                           | Object    |
| Email                          | Object    |
| Phone Number                   | Object    |
| Credit Card                    | Object    |
| Is Canceled                    | Integer   |

## Missing Values Summary

The following table summarizes the missing values in the dataset, including their counts and percentages:

| Field                        | Missing Values | Percentage (%) |
|------------------------------|----------------|----------------|
| Children                     | 4              | 0.003          |
| Country                      | 488            | 0.409          |
| Agent                        | 16,340         | 13.686         |
| Company                      | 112,593        | 94.307         |

### Detailed Missing Values Table

For a more comprehensive view, the table below provides the missing values and percentages for all fields in the dataset:

| Field                        | Missing Values | Percentage (%) |
|------------------------------|----------------|----------------|
| Hotel                        | 0              | 0.000          |
| Lead Time                    | 0              | 0.000          |
| Arrival Date Year            | 0              | 0.000          |
| Arrival Date Month           | 0              | 0.000          |
| Arrival Date Week Number     | 0              | 0.000          |
| Arrival Date Day of Month    | 0              | 0.000          |
| Stays in Weekend Nights      | 0              | 0.000          |
| Stays in Week Nights         | 0              | 0.000          |
| Adults                       | 0              | 0.000          |
| Children                     | 4              | 0.003          |
| Babies                       | 0              | 0.000          |
| Meal                         | 0              | 0.000          |
| Country                      | 488            | 0.409          |
| Market Segment               | 0              | 0.000          |
| Distribution Channel         | 0              | 0.000          |
| Is Repeated Guest            | 0              | 0.000          |
| Previous Cancellations       | 0              | 0.000          |
| Previous Bookings Not Canceled | 0            | 0.000          |
| Reserved Room Type           | 0              | 0.000          |
| Assigned Room Type           | 0              | 0.000          |
| Booking Changes              | 0              | 0.000          |
| Deposit Type                 | 0              | 0.000          |
| Agent                        | 16,340         | 13.686         |
| Company                      | 112,593        | 94.307         |
| Days in Waiting List         | 0              | 0.000          |
| Customer Type                | 0              | 0.000          |
| ADR                          | 0              | 0.000          |
| Required Car Parking Spaces  | 0              | 0.000          |
| Total of Special Requests    | 0              | 0.000          |
| Reservation Status           | 0              | 0.000          |
| Reservation Status Date      | 0              | 0.000          |
| Name                         | 0              | 0.000          |
| Email                        | 0              | 0.000          |
| Phone Number                 | 0              | 0.000          |
| Credit Card                  | 0              | 0.000          |
| Is Canceled                  | 0              | 0.000          |


* duplicates
none

# catatan hasil pengecekan setelah preparation dan cleaning
## cek info tipe data

The table below lists the data type for each field in the dataset after cleaning and preparation:

| Field                          | Data Type       |
|--------------------------------|-----------------|
| Hotel                          | Object          |
| Lead Time                      | Integer         |
| Arrival Date Year              | Integer         |
| Arrival Date Month             | Object          |
| Arrival Date Week Number       | Integer         |
| Arrival Date Day of Month      | Integer         |
| Stays in Weekend Nights        | Integer         |
| Stays in Week Nights           | Integer         |
| Adults                         | Integer         |
| Children                       | Float           |
| Babies                         | Integer         |
| Meal                           | Category        |
| Country                        | Category        |
| Market Segment                 | Category        |
| Distribution Channel           | Category        |
| Is Repeated Guest              | Integer         |
| Previous Cancellations         | Integer         |
| Previous Bookings Not Canceled | Integer         |
| Reserved Room Type             | Category        |
| Assigned Room Type             | Category        |
| Booking Changes                | Integer         |
| Deposit Type                   | Category        |
| Agent                          | Float           |
| Days in Waiting List           | Integer         |
| Customer Type                  | Category        |
| ADR                            | Float           |
| Required Car Parking Spaces    | Integer         |
| Total of Special Requests      | Integer         |
| Reservation Status             | Object          |
| Reservation Status Date        | Datetime        |
| Name                           | Object          |
| Email                          | Object          |
| Phone Number                   | Object          |
| Credit Card                    | Object          |
| Is Canceled                    | Integer         |


### Feature Classification Table

| Column                          | Semantic Type     | Original Dtype | Reasoning |
|---------------------------------|-------------------|----------------|-----------|
| hotel                           | Nominal           | object         | Hotel name/type; it's a label, not ordered |
| lead_time                       | Continuous        | int64          | Number of days; measurable, can be scaled |
| arrival_date_year               | Discrete          | int64          | Limited fixed set of years |
| arrival_date_month              | Ordinal           | object         | Months have natural order |
| arrival_date_week_number        | Discrete          | int64          | Week numbers are integer-indexed |
| arrival_date_day_of_month       | Discrete          | int64          | Day of month is numeric, bounded |
| stays_in_weekend_nights         | Discrete          | int64          | Count of weekend nights, whole number |
| stays_in_week_nights            | Discrete          | int64          | Count of weekday nights, whole number |
| adults                          | Discrete          | int64          | Number of adults per booking |
| children                        | Discrete          | float64        | Number of children, occasionally has `.0` but is a count |
| babies                          | Discrete          | int64          | Count of babies in booking |
| meal                            | Nominal           | object         | Categories of meal plans, no order |
| country                         | Nominal           | object         | Country code/label |
| market_segment                  | Nominal           | object         | Type of booking source (e.g. Online TA) |
| distribution_channel            | Nominal           | object         | Distribution method (e.g. Direct, TA) |
| is_repeated_guest               | Boolean           | int64          | 0 or 1, clearly binary |
| previous_cancellations          | Discrete          | int64          | Count of prior cancellations |
| previous_bookings_not_canceled  | Discrete          | int64          | Count of successful bookings |
| reserved_room_type              | Nominal           | object         | Categorical, non-ordered room code |
| assigned_room_type              | Nominal           | object         | Same as above, assigned instead of requested |
| booking_changes                 | Discrete          | int64          | Integer count of changes made |
| deposit_type                    | Nominal           | object         | Categorical: No Deposit, Non Refund, etc. |
| agent                           | Discrete          | float64        | Encoded agent ID, numeric but not continuous |
| days_in_waiting_list            | Discrete          | int64          | Integer count of waiting days |
| customer_type                   | Nominal           | object         | Contract/Transient/etc., unordered |
| adr                             | Continuous        | float64        | Average Daily Rate, measurable value |
| required_car_parking_spaces     | Discrete          | int64          | Number of parking spaces, whole number |
| total_of_special_requests       | Discrete          | int64          | Count of special requests |
| reservation_status              | Nominal           | object         | Categorical status (Canceled/Check-Out/No-Show) |
| reservation_status_date         | DateTime          | datetime64[ns] | Date of reservation status; date-based logic |
| name                            | Text              | object         | Guest’s name; not useful for modeling |
| email                           | Text              | object         | Same; personal info, possibly drop later |
| phone-number                    | Text              | object         | Not useful in modeling; identifier |
| credit_card                     | Text              | object         | Encoded for privacy, not usable for modeling |
| is_canceled                     | Boolean           | int64          | Target variable: 1 = canceled, 0 = not |


### Tabel Korelasi Fitur dengan `is_canceled`

| No | Nama Fitur                   | Korelasi | Interpretasi Singkat                                                                 |
|----|-----------------------------|----------|----------------------------------------------------------------------------------------|
| 1  | hotel_City Hotel            | 0.14     | City Hotel lebih sering dikaitkan dengan pembatalan.                                 |
| 2  | lead_time                   | 0.29     | Semakin jauh hari booking dari tanggal menginap, makin besar kemungkinan cancel.     |
| 3  | arrival_date_year           | 0.02     | Tahun kedatangan tidak terlalu berpengaruh.                                          |
| 4  | arrival_date_month          | 0.01     | Bulan kedatangan hampir tidak berpengaruh.                                           |
| 5  | arrival_date_week_number    | 0.01     | Minggu dalam tahun juga tidak signifikan.                                            |
| 6  | arrival_date_day_of_month   | -0.01    | Tidak ada pengaruh signifikan.                                                       |
| 7  | stays_in_weekend_nights     | 0.00     | Lama menginap akhir pekan tidak berkorelasi.                                         |
| 8  | stays_in_week_nights        | 0.02     | Lama menginap weekdays sedikit positif, tapi sangat lemah.                           |
| 9  | adults                      | 0.06     | Jumlah dewasa sedikit berkorelasi, tapi lemah.                                       |
| 10 | children                    | 0.01     | Hampir tidak ada pengaruh.                                                           |
| 11 | babies                      | -0.03    | Sedikit korelasi negatif, tapi sangat kecil.                                         |
| 12 | meal_FB                     | 0.04     | Tipe makan FB punya korelasi lemah terhadap cancel.                                  |
| 13 | country_PRT                 | 0.33     | Negara Portugal memiliki kontribusi tinggi terhadap pembatalan.                      |
| 14 | market_segment_Groups       | 0.22     | Pemesanan grup cenderung lebih sering cancel.                                        |
| 15 | distribution_channel_TA/TO  | 0.18     | TA/TO channel punya kecenderungan pembatalan lebih tinggi.                           |
| 16 | is_repeated_guest           | -0.08    | Tamu yang pernah menginap lebih jarang membatalkan.                                  |
| 17 | previous_cancellations      | 0.11     | Pernah cancel sebelumnya meningkatkan kemungkinan cancel lagi.                       |
| 18 | previous_bookings_not_canceled | -0.06  | Kebalikannya, jika pernah booking dan tidak cancel, lebih kecil peluang cancel lagi. |
| 19 | reserved_room_type_A        | 0.07     | Reservasi room tipe A sedikit dikaitkan dengan pembatalan.                           |
| 20 | assigned_room_type_A        | 0.20     | Mendapatkan room tipe A berkorelasi dengan pembatalan.                               |
| 21 | name                        | N/A      | Data teks unik – tidak berkorelasi langsung.                                         |
| 22 | email                       | N/A      | Sama seperti name, bukan fitur numerik/categorical yang bisa dikorelasikan.          |
| 23 | phone-number                | N/A      | Data pribadi – tidak dapat dihitung korelasinya.                                     |
| 24 | credit_card                 | N/A      | Sama, bukan fitur numerik yang relevan untuk korelasi.                               |
| 25 | is_canceled                 | 1.00     | Korelasi sempurna terhadap dirinya sendiri.                                          |



### Filter only the object dtype
| Column                          | Semantic Type | Original Dtype | Reasoning                                   |
|---------------------------------|---------------|----------------|---------------------------------------------|
| hotel                           | Nominal       | object         | Hotel name/type; it's a label, not ordered  |
| arrival_date_month              | Ordinal       | object         | Months have natural order                   |
| meal                            | Nominal       | object         | Categories of meal plans, no order          |
| country                         | Nominal       | object         | Country code/label                          |
| market_segment                  | Nominal       | object         | Type of booking source (e.g. Online TA)     |
| distribution_channel            | Nominal       | object         | Distribution method (e.g. Direct, TA)       |
| reserved_room_type              | Nominal       | object         | Categorical, non-ordered room code          |
| assigned_room_type              | Nominal       | object         | Same as above, assigned instead of requested|
| deposit_type                    | Nominal       | object         | Categorical: No Deposit, Non Refund, etc.   |
| customer_type                   | Nominal       | object         | Contract/Transient/etc., unordered          |
| reservation_status              | Nominal       | object         | Categorical status (Canceled/Check-Out/No-Show) |
| name                            | Text          | object         | Guest’s name; not useful for modeling       |
| email                           | Text          | object         | Same; personal info, possibly drop later    |
| phone-number                    | Text          | object         | Not useful in modeling; identifier          |
| credit_card                     | Text          | object         | Encoded for privacy, not usable for modeling|


# Hipotesis yang bisa dibuat
| Hipotesis | Dugaan                                                                 | Alasan                                                                 |
|-----------|------------------------------------------------------------------------|------------------------------------------------------------------------|
| H1        | Semakin besar lead_time, maka semakin tinggi kemungkinan pembatalan (`is_canceled`).  | Karena tamu lebih punya waktu untuk berubah pikiran.                   |
| H2        | Tamu dengan deposit_type = Non Refund lebih jarang membatalkan.       | Karena tidak dapat uang kembali, tamu cenderung akan datang walau kondisi berubah. |
| H3        | Booking melalui Online TA atau Offline TA/TO lebih tinggi kemungkinan pembatalannya dibanding Direct atau Corporate. | Agen perjalanan lebih fleksibel dan sering digunakan untuk opsi pencarian murah tanpa komitmen tinggi. |
| H4        | Negara asal (country) tertentu punya tren pembatalan lebih tinggi.    | Misalnya tamu dari negara tertentu mungkin sering membatalkan karena jarak atau proses visa. |
| H5        | Semakin tinggi days_in_waiting_list, semakin besar kemungkinan dibatalkan. | Tamu bisa kehilangan minat jika harus menunggu terlalu lama untuk konfirmasi. |
| H6        | Jika seluruh fitur digunakan tanpa seleksi, model cenderung overfit dan performa di data uji bisa menurun. | Karena terlalu banyak informasi bisa membuat model mempelajari noise alih-alih pola nyata. |
| H7        | Penggunaan fitur dengan korelasi sedang ke target + menghindari fitur redundan bisa meningkatkan kestabilan model. | Korelasi moderat cukup kuat memberi sinyal, sementara menghindari duplikasi mencegah pembelajaran berlebih. |
