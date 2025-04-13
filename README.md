# QAM-Noise
 A GNU Radio Flowgraph that models QAM and similar digital modes
# QAM Noise

QAM Noise simulates quadrature amplitude modulation in GNU Radio Companion, and is designed to be used as a simple teaching tool in a communications systems class. The amount of noise in the communications channel is configurable, and two constellations are provided to visualize the signal with and without noise. The primary simulated mode is 16-QAM, but 8PSK and QPSK are also selectable. Additionally, two text files are generated, one with the transmitted data and one with the received data, which can be compared to calculate the amount of loss in the channel. 

## Initial Assignment Prompt (from ECSE 351 @ CWRU, GNU Radio Problem Set)

Using the QAM Mod and QAM Demod blocks, simulate quadrature amplitude modulation in GNU
Radio. Add or create a visualization of the QAM constellation. (There are some existing blocks for constellation visualization which may help here). Next, add a noise source which is summed with the modulated signal, and visualize the constellation with and without noise. For a given raw bitrate, and a given amount of noise, are you better off with more constellation points running slower, or fewer constellation points flagging faster? An excellent version will be used in future curriculum, with acknowledgment of your work.

## Approach

While the provided problem specifies the use of the QAM Mod and Demod blocks, those have been deprecating in GNU Radio Companion since version 3.8. I researched how to get around this, and found the Constellation Object, which when coupled with Encode and Decode blocks, can simulate 16-QAM along with other modes including BPSK, QPSK, and 8PSK out of the box. 

## License

[MIT](https://choosealicense.com/licenses/mit/)