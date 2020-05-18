import time
import winsound
print("made by sherlock")
def myalarm():
    try:
        mytime = list(map(int,input("enter time in hr min sec\n").split()))
        if len(mytime) == 3:
            total_seconds=mytime[0]*60*60 + mytime[1]*60 + mytime[2]
            time.sleep(total_seconds)
            frequency = 2500  #set frequency to 2500
            duration = 1000  #set duration to 1000ms == 1 sec
            winsound.beep(frequency,duration)
        else:
            print("please enter the correct format as mentioned\n")
            myalarm()
    except Exception as e:
        print("this is the except\n",e,"so!, please enter the correct details")
        myalarm()
myalarm()
thankyou
