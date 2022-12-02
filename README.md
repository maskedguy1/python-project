# python-project
# clock angle problem
print("\t Greetings Ma'am\n"
      "\t This Project Is Submitted By :- \t Aayush Kumar \n"
      "\t Roll No :- 55\n"
      "\t Section :-\t k22ks\n")
print("\tClock Angle Problem")
hour = int(input("\tEnter The Time In Hours =\t"))
minutes = int(input("\tEnter The Time In Minutes =\t"))
if 12 < hour < 24 or hour==0:
    if minutes >= 0 and minutes <= 60:
        min_deg = (minutes * 6)
        hour_deg = ((hour + minutes / 60) / 12) * 360 % 360
        print("\tThe Angel Between ", hour, " : ", minutes, " = ",
              min(abs(min_deg - hour_deg), 360 - (abs(min_deg - hour_deg))), "°", sep="")
        print("\n"
              "\tTHANK YOU")
    elif minutes > 60 or minutes < 0:
        print("\tInvalid(minute input must be lower than 60 and greater than or equal to 0)")
elif hour >= 0 and hour <= 12:
    if minutes >= 0 and minutes <= 60:
        b = input("\tAm or Pm = ")
        if b=="am" or b=="AM" or b=="pm" or b=="PM" or b=="Am" or b=="Pm" or b=="aM" or b=="pM":
            min_deg = (minutes * 6)
            hour_deg = ((hour + minutes / 60) / 12) * 360 % 360
            print("\tThe Angel Between ", hour, " : ", minutes, " ", b, " = ",
                  min(abs(min_deg - hour_deg), 360 - (abs(min_deg - hour_deg))), "°", sep="")
            print("\n"
              "\tTHANK YOU")
        else:
            print("\tInvalid")
    elif minutes > 60 or minutes < 0:
        print("\tInvalid(minute input must be lower than 60 and greater than or equal to 0)")
elif hour > 23 or hour < 1:
    print("\tInvalid(hour input must be lower than 24 and greater than or equal to 0)")

