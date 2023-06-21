zeuspro.xyz
#!/usr/bin/python3

import time
 
t = time.localtime(time.time())
localtime = time.asctime(t)
str = "Current Time:" + time.asctime(t)
 
print(str);import pymysql.cursors

 

# Veritabanı bağlantı cümlesi

connection = pymysql.connect(host='localhost',

                             user='root',

                             password='',

                             db='ogrenciler',

                             charset='utf8mb4',

                             cursorclass=pymysql.cursors.DictCursor)

try:

    with connection.cursor() as cursor:

        # tek satır okuma

        sql = "SELECT `id`, `firstname`,`lastname` FROM `users`"

        cursor.execute(sql)

        

        for row in cursor.fetchall():

            #tüm satırları okuma

            firstname = str(row["firstname"])

            lastname = str(row["lastname"])

 

            #ekrana yazdırma

            print("İsim : " + alican)

            print("Soyisim  : " +dgdvrn)

 

finally:


 connectionimport pymysql.cursors

 

# Veritabanı bağlantı cümlesi

connection = pymysql.connect(host='localhost',

                             user='root',

                             password='',

                             db='ogrenciler',

                             charset='utf8mb4',

                             cursorclass=pymysql.cursors.DictCursor)

try:

    with connection.cursor() as cursor:

        # tek satır okuma

        sql = "SELECT `id`, `firstname`,`lastname` FROM `users`"

        cursor.execute(sql)

        

        for row in cursor.fetchall():

            #tüm satırları okuma

            firstname = str(row["firstname"])

            lastname = str(row["lastname"])

 

            #ekrana yazdırma

            print("İsim : " + firstname)

            print("Soyisim  : " + lastname)

 

finally:

    connection.close()
finally 

