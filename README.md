# Reservation_App (Kotlin) βπ§Ύ
<br>
π μκ°, λ μ§λ₯Ό μ€μ νμ¬ μμ½μ νκ³  μ΄ μμ½νλ κ³Όμ μμ λͺ λΆμ΄ κ±Έλ Έλμ§ μ μ μλ μ±
<br>
<br>
<br>

## Main Screen
![KakaoTalk_20220104_141135980](https://user-images.githubusercontent.com/72568433/148012396-8c6ef716-ef61-4fd9-8cc3-7b0ea0b40137.jpg)

## Code
<br>
<br>

1. ν¬λ‘λΈλ―Έν°λ₯Ό 0μΌλ‘ μ΄κΈ°ννμ¬ <μμ½ μμ> λ²νΌμ ν΄λ¦­ν  λλ§λ€ μ΄κΈ°νλκ² νλ€.
<br>

   ```
   btnStart.setOnClickListener {
            chrono.base = SystemClock.elapsedRealtime() //ν¬λ‘λΈλ―Έν°λ₯Ό 0μΌλ‘ μ΄κΈ°ν
            chrono.start()
            chrono.setTextColor(Color.RED) //νμ΄λ¨Έκ° μμλλ©΄ λΉ¨κ° κΈμ¨λ‘
        }
   ```
 <br>
 <br>
 <br>

2. μΊλ¦°λλ·°λ₯Ό ν΄λ¦­νλ©΄ μ°μμΌμ΄ μ μ­λ³μμ λμλλ€. μμ 0λΆν° μμνλ―λ‘ 1μ λν΄μ£Όμλ€.
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

3. <μμ½ μλ£>λ₯Ό ν΄λ¦­νλ©΄ μΊλ¦°λλ·°μμ μ€μ ν μ°, μ, μΌκ³Ό νμνΌμ»€μμ μ€μ ν μ, λΆμ΄ λ§¨ μλ νμ€νΈλ·°μ μ±μμ§κ² νλ€.
<br>

   ```
    btnEnd.setOnClickListener {
            chrono.stop() //ν¬λ‘λΈλ―Έν° μ μ§
            chrono.setTextColor(Color.BLUE) //νμ΄λ¨Έκ° μ μ§λλ©΄ νλ κΈμ¨λ‘

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

