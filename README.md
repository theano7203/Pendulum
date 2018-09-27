# Pendulum
#Could not get pytz in Python 3.6 to import so discovered Pendulum. Married it to a teaching script and modified to Pendulum and it worked
#Original script teaching code came from Tim Buchalka but had to modify it to get it to work. Reseached and lots on issues with pytz.
#Pendulum offers an alternative when pytz has fitz..https://pendulum.eustace.io/docs/#using-the-timezone-library-directly

import pendulum

import datetime

country = "Europe/Paris"

tz_to_display = pendulum.timezone(country)
local_time = datetime.datetime.now(tz=tz_to_display)
print("The time in {} is {}".format(country, local_time))
print("UTC is {}".format(datetime.datetime.utcnow()))

Output

The time in Europe/Paris is 2018-09-27 09:16:25.187765+02:00
UTC is 2018-09-27 07:16:25.187765

Process finished with exit code 0
