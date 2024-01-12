# Django-codes
## Get xlsx file from DB data
```def userlist():
    print(">>>>>>>>>>>>userlist<<<<<<<<<<<<")
    try:
       
        alluserdata = User.objects.all()
        fields = (['ID', 'First Name', 'Last Name', 'Email'])  

        with open('All_Users_in DB_12_01_24.xlsx', 'a') as outfile:
            outfile.write(str(fields) + '\n')
            for user in alluserdata:
                print(user.user.id)
                outfile.write(str(user.user.id)+";"+str(user.user.first_name)+";"+str(user.user.last_name)+";"+str(user.user.email)+";"+ '\n')   
        return True
    except Exception as e:
        pass

userlist()
```
