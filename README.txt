# Openflow_Switch

1. Location of file
    of_tutorial1.py -------- /home/pox/pox/misc

2. act_like_switch
    a. Open a controller
        first open a terminal
        $ cd pox
        $./pox.py log.level --DEBUG misc.of_tutorial (what already included in pox)

    b. Create Topology
        open another terminal
        $ sudo mn -c        
        $ sudo mn --topo single,3 --mac --switch ovsk --controller remote
    c. Test
        mininet> pingall
        mininet> iperf
        
And then we modify the of_tutorial.py, implement the function of act_like_switch. Test again, comparing the result of iperf 
    d. Compare result
        $ sudo killall controller 
        $ cd pox
        $./pox.py log.level --DEBUG misc.of_tutorial1
        mininet>quit
        mininet> pingall
        mininet> iperf
According to the result, the reported iperf bandwidth should be much higher, and should match the number we got earlier.
