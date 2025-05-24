# DIGITAL-FILTER-DESIGN

*COMPANY* : CODTECH IT SOLUTIONS

*NAME* : PUNNAMISAIPOOJITHA

*INTERN ID* : CT04DL863

*DOMAIN* : VLSI

*DURATION* : 4 WEEKS

*MENTOR* : NEELA SANTOSH

*DESCRIPTION OF THE TASK* :

This Verilog code implements a simple Finite Impulse Response (FIR) filter along with a testbench to simulate and verify its behavior. The FIR filter is defined in a module named `fir_filter` and is parameterized to use 4 filter taps (`N = 4`). It takes in a clock (`clk`), an active-high reset (`reset`), and an 8-bit signed input sample (`x_in`). The output of the filter is a 16-bit signed signal (`y_out`) that represents the weighted sum of current and previous inputs, as determined by the FIR filter coefficients.

The filter design includes a shift register `x` to store the most recent `N` input samples, and a coefficient array `coeffs` initialized with the values 1, 2, 3, and 4. During each clock cycle, if the reset is active, the shift register and output are cleared. Otherwise, the filter shifts existing samples to the right, accepts a new sample at the input, and computes the output by performing a multiply-and-accumulate (MAC) operation using the input samples and their corresponding coefficients. This is a standard implementation technique in digital signal processing for FIR filters, where the output is calculated as a linear combination of a fixed set of past input values.

The testbench module `tb_fir_filter` is used to simulate the behavior of the FIR filter in a controlled environment. It declares necessary signals to drive the inputs and observe the output. A clock signal is generated using an `always` block that toggles the clock every 5 time units, creating a periodic waveform. The stimulus is applied in the `initial` block, where the reset is first asserted, then deasserted, and a sequence of input samples (from 1 to 7) is applied to `x_in` at regular intervals. The `$monitor` system task prints the simulation time, input value, and output value to track the filter’s behavior.

This example demonstrates a basic yet powerful FIR filter implementation and simulation using Verilog. It highlights the use of shift registers for sample storage, fixed coefficients for defining filter behavior, and the MAC operation for generating the filter output. The design is ideal for small-scale digital signal processing applications and can be easily extended by increasing the number of taps or modifying the coefficients for different filtering characteristics. Furthermore, the testbench provides an easy way to validate functionality and observe the dynamic response of the filter across time steps.



*OUTPUT* :

