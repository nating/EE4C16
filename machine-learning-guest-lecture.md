
# Machine Learning Guest Lecture

Machine learning for embedded systems

Challenges in embedding ai in embedded systems

## Background on Xilinx and challenges in the industry

Have devices deployed everywhere

Invented the FPGA

GPGA used to be simply a 2D LUT. Ten different colymns for functions were added.

Now they're supposed to call FPGAs All programable GAs now instead.

The computation time is a lot less because therre are a lot less instructions to be excecuted, and that means that there is a lot les energy consumed as well.

## Machine learning and its Challenges

Since 2005 the clock speeds of computing haven't really got better.

Needs really sophisicated equipment to make the size of transistors smaller and smaller. This is why the computers and phones are more and more expensive. It takes a lot more money to make the computers faster.

"They're out of tricks" an't fit more taransistors, can't get more power, can't continure as they do and expect computers to get faster

Because they can solve so many challenges, thet all reqire different networks.

For different use cases, there's a diffeent figure of merit (want better accuracy / want better speed / power consumption etc.)

NNs use a lot of power and memory. (hundreds of gigabytes of data) (Far exceeds cache sizes which slows things down)

Al the limits are going in the wrong direction considering what we need for al of the macine learning we are doing.

There's a lot of different options when designing a neural network, and each of the choices in design changes the throughput/performance/hardware cost/ etc.

## Xilinx effort

They are reducing precision of the operators (goindo from floating point to fixed point)

This helps them to stay completely on chip

loating point to fixed point can save around nine times the power

Good graph on how they reduce the quantization and increase accuracy while decreasing hardware consumption
She is concinced that the reduced quantization will beat the original quantization in the long reducing
New architectures for the GPUs for NNs code using the FPGA. They completel y make the neural network topology inside the FPGA. recreate the pipeline of the NN in hardware on the chip.

TOLO! finds multiple cats in an iamge and where they architectures
They have a python enabled platform like the raspberry pi only 55 dollars that has two arm cores and an fpga with python apis and things are packaged in jupiter notbook. And they're pyutting together a robotics kit soon as wel.

They haev top in class performance. But there is a lot left to understand, and a lot left to research.

## Summary and Questtions

To train a binary network:
Quantize the weights during training. directly after the activation function.

Floating point takes a lot more computing power than fixed point because you have to scale the mantissa etc before doing the operation
