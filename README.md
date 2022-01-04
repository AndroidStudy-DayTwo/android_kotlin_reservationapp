# Reservation_App (Kotlin) ⌚🧾
<br>
🔗 시간, 날짜를 설정하여 예약을 하고 총 예약하는 과정에서 몇 분이 걸렸는지 알 수 있는 앱
<br>
<br>
<br>

## Main Screen
![KakaoTalk_20220104_141135980](https://user-images.githubusercontent.com/72568433/148012396-8c6ef716-ef61-4fd9-8cc3-7b0ea0b40137.jpg)

## Code
<br>
<br>

1. 크로노미터를 0으로 초기화하여 <예약 시작> 버튼을 클릭할 때마다 초기화되게 한다.
<br>

   ```
   btnStart.setOnClickListener {
            chrono.base = SystemClock.elapsedRealtime() //크로노미터를 0으로 초기화
            chrono.start()
            chrono.setTextColor(Color.RED) //타이머가 시작되면 빨간 글씨로
        }
   ```
 <br>
 <br>
 <br>

2. 캘린더뷰를 클릭하면 연월일이 전역변수에 대입된다. 월은 0부터 시작하므로 1을 더해주었다.
<br>

   ```
   calView.setOnDateChangeListener{ view, year, month, dayOfMonth ->
            selectYear = year
            selectMonth = month + 1
            selectDay = dayOfMonth
        }
   ```
   
 <br>
 <br>
 <br>

3. <예약 완료>를 클릭하면 캘린더뷰에서 설정한 연, 월, 일과 타임피커에서 설정한 시, 분이 맨 아래 텍스트뷰에 채워지게 한다.
<br>

   ```
    btnEnd.setOnClickListener {
            chrono.stop() //크로노미터 정지
            chrono.setTextColor(Color.BLUE) //타이머가 정지되면 파란 글씨로

            tvYear.text = Integer.toString(selectYear)
            tvMonth.text = Integer.toString(selectMonth)
            tvDay.text = Integer.toString(selectDay)
            tvHour.text = Integer.toString(tPicker.currentHour)
            tvMinute.text = Integer.toString(tPicker.currentMinute)
        }
   ```
 <br>
 
 
![KakaoTalk_20220104_141135980_03](https://user-images.githubusercontent.com/72568433/148013844-f2242631-7d07-4ed6-be27-25f535f2d7c1.jpg)
 <br>
 <br>

