## Python script to record audio :notes: :microphone:

Provides WAV recording functionality via two approaches:

- Blocking mode (record for a set duration):
```rec = Recorder(channels=2)
with rec.open('blocking.wav', 'wb') as recfile:
  recfile.record(duration=5.0) 
```

- Non-blocking mode (start and stop recording):
``` rec = Recorder(channels=2)
with rec.open('nonblocking.wav', 'wb') as recfile2:
  recfile2.start_recording()
  time.sleep(5.0)
  recfile2.stop_recording() ```
