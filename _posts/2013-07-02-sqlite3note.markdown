---
layout: post
title: "Sqlite3 usage"
date: 2013-07-02 16:17
comments: true
categories: [Note, Database]
---
Recently I wirte a spider to greb infomation. And I have to store the data somewhere for reuse. And I chose sqlite. Here are the command used in python.

####import the package
>import sqlite3
####connect to a db
>con = sqlire3.connect("dbname")
####get a cursor
>cur = con.cursor()
####initial db
>cur.execute('''creat table if not exists tablename(id integer, name text, score real)''')
####insert into db
>val = [12, 'asdf', 12.0]
>cur.execute('insert into doc values(?,?,?)', val)
>con.commit()
####select from db
>result = cur.execute('select * from doc')
####use the selected result
>rows = result.fetchall()
>for row in rows:
>>print row
>row = result.fetchone()
>>print row
####update db
>cur.execute('update doc det score = ? where id = ?', (score, id))
>con.commit()

####view db in shell
>sqlite3 dbname    
>select * from doc;    

####tips:
Don't forget to commit()
