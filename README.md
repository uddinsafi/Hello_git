# Hello_git
def generate_next_date(day,month,year):
    if(month==4 or month==6 or month==9 or month==11):
        if(day<=29):
            day=day+1
        else:
            day=1
            month=month+1
    elif(month==2):
        if(day<28):
            day=day+1
        else:
            if(day==28 and year%400==0):
                day=day+1
            else:
                day=1
                month=month+1
    else:
        if(day<31):
            day=day+1
        elif(day==31 and month==12):
            day=1
            month=1
            year=year+1
        else:
            day=1
            month=month+1
    print(day,"-",month,"-",year)
    

generate_next_date(31,12,2016)
