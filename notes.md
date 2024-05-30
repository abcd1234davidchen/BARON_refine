Set:
    Three mode
        off patch   off attacker
            tBS in AMF
            tBS not AMF
        on patch    off attacker
            tBS in AMF
            tBS not AMF
        on patch    on attacker
            after tBS in AMF
            after tBS not AMF
            after tBS is sBS
    1001 rounds
    12+1 base station

Loop:   run until first two at least 1001 rounds and set time vector

    2 AMF 12 BS
    AMF 1  0,0
        2  2200,1100

    BS  1   200,1000    1
        2   450,800     1
        3   800,400     1
        4   1000,50     1
        5   100,650     1
        6   300,200     1

        7   950,900     2
        8   1250,500    2
        9   1400,250    2
        10  1200,1100   2
        11  1850,1000   2
        12  2000,750    2

    UE ID:12 random location from (0~2200,0~1300)
    
    UE connect second strongest BS

    if there is attacker, set fBS to one other than UE connected
    
    2D double array for channel [base station(12)][0]=signal power [1]=BS ID

    BSnum+3 amount of messages address
    msg[0]=ue
    msg[1]~[12]=BS
    msg[13]~[14]=AMF
    all set to null

    transit beacon function: set each channel to the right amount of power
    set best_bs to be the one with highest power

    handover start

    UE set target
    UE sent measurement report to tBS
    push the transit time from UE to BS

    type_transmition: for calculate time consume

    std/baron
    43434141
    42424141
    4324234141

    baron w/attacker
    43434141
    42424141
    43242341414341
    4324234141423241
    42343241414241

    pushback process time
    pushback compute delay

    sum up time

    push to overall_time vector

    clean data
end of loop

