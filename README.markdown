Service Disruption
=============

A little library to easily tell you when the Tube has problems

## Install

    gem install service_disruption


## Running

    $: service_disruption start

    $: service_disruption stop

Extra arguments are: `-- -i` to change the polling time, defaults to once every 30 seconds

Alternatively if you'd like to see some pretty colours on your command line you can run

    $: service_disruption status

That will tell you the current state of the tube network, you can also incude it as any other ruby library. It exposes the following API:

    network = ServiceDisruption.network

    network.lines # Array of lines
    bakerloo = network.find_by_name('Bakerloo') # Line object

    bakerloo.status # Status object

    network.update! # Updates all of the lines status information if it has changed

## Who?

[Adam Carlile](http://adamcarlile.com) built this. Ping me on Twitter —
[@frozenproduce](http://twitter.com/frozenproduce).

NOTE: Not to be used for mission critical service monitoring!

