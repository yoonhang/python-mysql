혼공_SQL 2021.09.22
https://www.youtube.com/watch?v=BUHj-behLyc&list=PLVsNizTWUw7GCfy5RH27cQL5MeKYnl8Pm&index=14

#pip install pymysql

#import pymysql

# 전역변수 선언부
conn, cur = None, None
data1, data2, data3, data4 = "", "", "", ""
sql=""

# 메인 코드
conn = pymysql.connect(host='127.0.0.1', user='root', password='0000', db='soloDB', charset='utf8')
cur = conn.cursor()

while (True) :
    data1 = input("사용자 ID ==> ")
    if data1 == "" :
        break;
    data2 = input("사용자 이름 ==> ")
    data3 = input("사용자 이메일 ==> ")
    data4 = input("사용자 출생연도 ==> ")
    sql = "INSERT INTO userTable VALUES('" + data1 + "','" + data2 + "','" + data3 + "'," + data4 + ")"
    cur.execute(sql)

conn.commit()
conn.close()

###############
#파이썬 윈도우 프로그래밍

from tkinter import *
root = Tk()
root.geometry("200x250")

