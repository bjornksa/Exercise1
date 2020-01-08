Results
-------

Running the programs gives a new random number each time. This is unsurprising as we have two threads simultanously modifying a single value wich causes this unpredictable behaviour due to race conditions deciding wich threads accessess the file at what times.
