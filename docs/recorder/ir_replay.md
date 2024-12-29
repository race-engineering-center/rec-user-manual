# Recording from iRacing replay

Recorder (or to be more precise, iRacing live plugin for Recorder) supports telemetry
recording from iRacing replays. Follow these steps to retrieve telemetry from iRacing 
replay:

1. Open iRacing replay in iRacing and run Recorder (in any order);
2. Scroll to the beginning of the lap you want to record. Leave a couple of seconds before
the start of the lap so that Recorder correctly detects the start of the lap;
3. Make sure Recorder is connected to iRacing and the necessary car is checked;
4. Start replaying by pressing "Play" button in iRacing and wait for the lap(s) you want
recorded to be replayed;
5. Don't pause or rewind/fast-forward a lap, this will cause recording to be stopped;
6. After the lap is finished leave a couple of seconds of overlap with the next lap
to correctly detect a lap end;

!!! Note 
    Currently Recorder only supports recording telemetry from your car (the car of the player,
    that saved this replay) due to the limitations of the data provided by iRacing.

After recording is finished, go to Analyzer [lap library](../analyzer/laplibrary.md) to 
check your lap.

!!! Note
    iRacing live plugin records all the data provided by iRacing, however the telemetry recorded 
    from the replay will contain smaller set of channels because iRacing does not provide some
    telemetry in replay.
