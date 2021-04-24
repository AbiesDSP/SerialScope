# SerialScope
Software Oscilloscope

## Serial Protocol


### Data Stream Format
194 byte payload containing 64 samples.

    int16 frame_id
    int24 sample0
    ...
    int24 sample63

### Command Format

4 byte command send to the fpga. 128 addresses. MSb of the address is 'write enable'.

    uint8 address
    int24 data

### Telemetry Format
Reply from the fpga containing all config settings.
    