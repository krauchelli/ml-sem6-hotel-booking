# catatan hasil pengecekan preparation section

## Dataset example (rough copy paste from the csv)
```
hotel,lead_time,arrival_date_year,arrival_date_month,arrival_date_week_number,arrival_date_day_of_month,stays_in_weekend_nights,stays_in_week_nights,adults,children,babies,meal,country,market_segment,distribution_channel,is_repeated_guest,previous_cancellations,previous_bookings_not_canceled,reserved_room_type,assigned_room_type,booking_changes,deposit_type,agent,company,days_in_waiting_list,customer_type,adr,required_car_parking_spaces,total_of_special_requests,reservation_status,reservation_status_date,name,email,phone-number,credit_card,is_canceled
Resort Hotel,342,2015,July,27,1,0,0,2,0,0,BB,PRT,Direct,Direct,0,0,0,C,C,3,No Deposit,,,0,Transient,0,0,0,Check-Out,7/1/2015,Ernest Barnes,Ernest.Barnes31@outlook.com,669-792-1661,************4322,0
Resort Hotel,737,2015,July,27,1,0,0,2,0,0,BB,PRT,Direct,Direct,0,0,0,C,C,4,No Deposit,,,0,Transient,0,0,0,Check-Out,7/1/2015,Andrea Baker,Andrea_Baker94@aol.com,858-637-6955,************9157,0
Resort Hotel,7,2015,July,27,1,0,1,1,0,0,BB,GBR,Direct,Direct,0,0,0,A,C,0,No Deposit,,,0,Transient,75,0,0,Check-Out,7/2/2015,Rebecca Parker,Rebecca_Parker@comcast.net,652-885-2745,************3734,0
Resort Hotel,13,2015,July,27,1,0,1,1,0,0,BB,GBR,Corporate,Corporate,0,0,0,A,A,0,No Deposit,304,,0,Transient,75,0,0,Check-Out,7/2/2015,Laura Murray,Laura_M@gmail.com,364-656-8427,************5677,0
Resort Hotel,14,2015,July,27,1,0,2,2,0,0,BB,GBR,Online TA,TA/TO,0,0,0,A,A,0,No Deposit,240,,0,Transient,98,0,1,Check-Out,7/3/2015,Linda Hines,LHines@verizon.com,713-226-5883,************5498,0
Resort Hotel,14,2015,July,27,1,0,2,2,0,0,BB,GBR,Online TA,TA/TO,0,0,0,A,A,0,No Deposit,240,,0,Transient,98,0,1,Check-Out,7/3/2015,Jasmine Fletcher,JFletcher43@xfinity.com,190-271-6743,************9263,0
Resort Hotel,0,2015,July,27,1,0,2,2,0,0,BB,PRT,Direct,Direct,0,0,0,C,C,0,No Deposit,,,0,Transient,107,0,0,Check-Out,7/3/2015,Dylan Rangel,Rangel.Dylan@comcast.net,420-332-5209,************6994,0
Resort Hotel,9,2015,July,27,1,0,2,2,0,0,FB,PRT,Direct,Direct,0,0,0,C,C,0,No Deposit,303,,0,Transient,103,0,1,Check-Out,7/3/2015,William Velez,Velez_William@mail.com,286-669-4333,************8729,0
Resort Hotel,85,2015,July,27,1,0,3,2,0,0,BB,PRT,Online TA,TA/TO,0,0,0,A,A,0,No Deposit,240,,0,Transient,82,0,1,Canceled,5/6/2015,Steven Murphy,Steven.Murphy54@aol.com,341-726-5787,************3639,1
Resort Hotel,75,2015,July,27,1,0,3,2,0,0,HB,PRT,Offline TA/TO,TA/TO,0,0,0,D,D,0,No Deposit,15,,0,Transient,105.5,0,0,Canceled,4/22/2015,Michael Moore,MichaelMoore81@outlook.com,316-648-6176,************9190,1
Resort Hotel,23,2015,July,27,1,0,4,2,0,0,BB,PRT,Online TA,TA/TO,0,0,0,E,E,0,No Deposit,240,,0,Transient,123,0,0,Canceled,6/23/2015,Priscilla Collins PhD,PhD.Priscilla74@att.com,833-887-7898,************4642,1
Resort Hotel,35,2015,July,27,1,0,4,2,0,0,HB,PRT,Online TA,TA/TO,0,0,0,D,D,0,No Deposit,240,,0,Transient,145,0,0,Check-Out,7/5/2015,Laurie Smith,Smith.Laurie@att.com,804-383-4080,************5450,0
```

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

### Notes:
- Fields with a high percentage of missing values, such as `Company` (94.307%) and `Agent` (13.686%), may require further investigation or specific handling strategies.
- Consider the following approaches for handling missing values:
    - Imputation: Fill missing values with mean, median, mode, or other contextually appropriate values.
    - Removal: Exclude rows or columns with excessive missing values if they are not critical to the analysis.
    - Flagging: Mark missing values for special treatment during analysis.
- Ensure that the handling of missing values aligns with the goals and context of the analysis.
- Document any assumptions or decisions made during the data cleaning process.


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

### Notes:
- The dataset now contains 35 columns with appropriate data types.
- Categorical fields (`Meal`, `Country`, `Market Segment`, etc.) have been converted to the `Category` data type for optimized memory usage.
- The `Reservation Status Date` field has been converted to `Datetime` for easier date-based operations.
- Ensure that these data types align with the intended analysis and processing requirements.
- Document any further changes or assumptions made during the data preparation process.

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