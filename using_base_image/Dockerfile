FROM acciom_base

#Making the Work Directory
WORKDIR /myfiles
RUN mkdir /myfiles/sharedfolder
RUN rm -r /myfiles/*
COPY . /myfiles/

#Mysql part
#ADD InsertDataScript/create_db_user.sql /docker-entrypoint-initdb.d
ENV LC_ALL="C.UTF-8"
ENV LANG="C.UTF-8"
ENV FLASK_APP="manage.py"

#RUN mysql -hmysql_cont -uacciom_user -pacciom_password < InsertDataScript/create_db.sql
#RUN python3 InsertDataScript/create_table_script_s.py
#RUN python3 InsertDataScript/create_table_script_d.py
#RUN python3 InsertDataScript/inserting_200_s.py
#RUN python3 InsertDataScript/inserting_200_d.py
#RUN flask db migrate
#RUN flask db upgrade

EXPOSE 5000
CMD ["python3","app.py"]
