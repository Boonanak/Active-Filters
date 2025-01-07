<h1>Active Filters</h1>

### [YouTube Demonstration Coming Soon](INSERTLINK)

<h2>Description</h2>
<p>An active filter is an electronic circuit designed to allow low-frequency signals,(low pass), high frequency signals, (high pass), or a specific band of frequency signals, (band pass), to pass through while attenuating all others signals. The term "active" indicates that the circuit uses active components, in our case an operational amplifier, in addition to passive components like resistors and capacitors. The op-amp provides gain and enhances the filter's performance compared to passive filters, allowing for better control over the filter's cutoff frequency and gain.</p>

<h2>Environments Used</h2>
<ul>
  <li><b>EasyEDA</b></li>
  <li><b>Excel</b></li>
</ul>

<h2>Parts List</h2>
<ul>
  <li><strong>Capacitor (0.01uF)</strong>
    <ul>
      <li>Manufacturer: Nichicon</li>
      <li>Specifications: 10µF, 25V, Electrolytic</li>
      <li><a href="https://www.digikey.com/en/products/detail/nichicon/UCS2G100MPD1TD/3768673">Datasheet</a></li>
      <li>Supplier: Digikey</li>
    </ul>
  </li>
  <li><strong>Resistor (10kΩ) x 2</strong>
    <ul>
      <li>Manufacturer: BOJACK</li>
      <li>Specifications: 10kΩ, 1/4W, ±1%</li>
      <li><a href="https://www.amazon.com/BOJACK-Values-Resistor-Resistors-Assortment/dp/B08FD1XVL6/ref" target="_blank">Datasheet</a></li>
      <li>Supplier: Amazon</li>
    </ul>
  </li>
  <li><strong>Resistor (1kΩ)</strong>
    <ul>
      <li>Manufacturer: BOJACK</li>
      <li>Specifications: 10kΩ, 1/4W, ±1%</li>
      <li><a href="https://www.amazon.com/BOJACK-Values-Resistor-Resistors-Assortment/dp/B08FD1XVL6/ref" target="_blank">Datasheet</a></li>
      <li>Supplier: Amazon</li>
    </ul>
  </li>
  <li><strong>Operational Amplifier</strong>
    <ul>
      <li>Manufacturer: Texas Instruments</li>
      <li>Specifications: LM258AP, Dual Operational Amplifier, 3V to 32V (single supply) or ±1.5V to ±16V (dual supply)</li>
      <li><a href="https://www.digikey.com/en/products/detail/texas-instruments/LM258AP/1510009" target="_blank">Datasheet</a></li>
      <li>Supplier: Digikey</li>
    </ul>
  </li>
</ul>

<h2>Type of Active Low Pass Filters</h2>
<ul>
  <li><strong>First-Order Active Low-Pass Filter (Series)</strong>
  <ul>
      <li>Resistor in series, capacitor and op-amp in feedback:
      <ul>
          <li>The resistor is placed in series with the input signal.</li>
          <li>The capacitor is part of the feedback loop with the op-amp, defining the cutoff frequency.</li>
          <li>Behavior: Low frequencies pass through to the output, while high frequencies are attenuated by the feedback network.</li>
          <li>Application: Basic filtering tasks in audio systems, removing high-frequency noise.</li>
      </ul>
      </li>
  </ul>
  </li>             
  <li><strong>First-Order Active Low-Pass Filter (Parallel)</strong>
  <ul>
      <li>Capacitor and resistor in parallel with op-amp:
      <ul>
          <li>The capacitor and resistor are connected in parallel, forming a voltage divider with the op-amp input.</li>
          <li>The output is taken from the op-amp, which amplifies the low-frequency signal.</li>
          <li>Behavior: High frequencies are attenuated by the capacitor, while low frequencies are passed to the output.</li>
          <li>Application: Useful in applications where gain control and low-pass filtering are needed.</li>
      </ul>
      </li>
  </ul>
  </li>
  <li><strong>Second-Order Active Low-Pass Filter (Series)</strong>
  <ul>
      <li>Enhanced series configuration with additional components:
      <ul>
          <li>Two resistors and capacitors form a network around the op-amp.</li>
          <li>The output is taken after the second RC stage for sharper attenuation of high frequencies.</li>
          <li>Behavior: Offers a steeper roll-off (40 dB/decade) compared to first-order filters.</li>
          <li>Application: Common in audio processing and equalizer circuits for selective frequency control.</li>
      </ul>
      </li>
  </ul>
  </li>
  <li><strong>Second-Order Active Low-Pass Filter (Parallel)</strong>
  <ul>
      <li>Parallel feedback network for improved selectivity:
      <ul>
          <li>Two capacitors and resistors in a parallel configuration around the op-amp.</li>
          <li>The output is taken from the op-amp, which processes the parallel RC network's response.</li>
          <li>Behavior: Offers a smooth response with sharper attenuation in the stopband.</li>
          <li>Application: Suitable for applications requiring precise control of signal bandwidth.</li>
      </ul>
      </li>
  </ul>
  </li>
</ul>

<h2>Summary of Configurations</h2>
<ul>
  <li>First-Order Active Low-Pass Filter (Series): Resistor in series with input, capacitor in feedback loop.</li>
  <li>First-Order Active Low-Pass Filter (Parallel): Resistor and capacitor in parallel with the op-amp input.</li>
  <li>Second-Order Active Low-Pass Filter (Series): Two resistors and two capacitors forming a network around the op-amp.</li>
  <li>Second-Order Active Low-Pass Filter (Parallel): Two resistors and two capacitors in  parallel configuration around the op-amp.</li>
</ul>

<h2>Background</h2>
<p>For my active filter I will be designing a active low pass filter, I used a configuration of a resistor and a capacitor in parallel to the op-amp. The behavior of RC components in relation to signal frequencies helps explain why this functions as a active low-pass filter.</p>
<ul>
  <li>Resistors' impedance remains constant regardless of the signal frequency.</li>
  <li>Capacitors, however, block high-frequency signals because their impedance decreases at higher frequencies. At low frequencies, the capacitor has a higher impedance, so it allows more of the low-frequency signal to appear across it.</li>
  <li>The op-amp is used to amplify the input signal and can provide gain, making the filter "active." The op-amp generally operates with a feedback network to control the filter's behavior.</li>
</ul>
<p>At low frequencies, the impedance of the capacitor is high, meaning it doesn't conduct much current. The resistor, on the other hand, has a constant resistance. The input signal is primarily passed through the resistor, and the op-amp amplifies the signal without much attenuation. At high frequencies, the impedance of the capacitor decreases, allowing more current to flow through it. As the capacitor conducts more, it shunts the higher-frequency components away from the output. The op-amp will still try to amplify the signal, but the capacitor's impedance essentially "shorts out" the high-frequency components, attenuating them.</p>

<h2>Motivation</h2>
<p>However, you may ask, at what point does the filter decide what is a low-frequency signal and what is a high-frequency signal? That is defined by the cutoff frequency. The cutoff frequency is determined based on the value of the resistor and capacitor that you chose and is calculated using the below formula:</p>
<img src="https://github.com/user-attachments/assets/51e86869-7400-42ba-883b-bc56991d7783"/>

<h2>Experiment</h2>
<h3>Setup</h3>
<p>For my low-pass filter, I used a 10k-ohm resistor and a 0.01uF capacitor, meaning that my expected cutoff frequency in a perfect world would be roughly 1600 Hz. However it is also important to note that I also used a load resistor that connects Vout to ground and this could have an effect on the cutoff frequency. In addition to the load resistor I also used a resistor connected to the input to limit the current to the op-amp and stablize the input.</p>
<img src="/Active_Low_Pass.png"/>
<p>To test this, I made my own active low-pass filter (which can be seen in the simple schematic above) and then connected the input voltage to a wave generator and the output voltage to an oscilloscope. I also connected the input voltage straight from the wave generator to the oscilloscope so I could see both waves side by side. I took readings of the amplitude of the output voltage, (peak to peak). Once I gathered the amplitude readings I derived the gain from them. My results are pictured below along with corresponding graphs. It is also important to note that I plotted the linear gain, (unitless), instead of using the dB scale.</p>

<h2>Results</h2>
<img src="/Active_Low_Pass_Findings.png"/>

<h2>Gain Analysis</h2>
<p>As you can see from the Gain vs. Frequency graph, there appears to be a drop-off between 400 and 1000 Hz. Signals with a frequency greater than 1000 Hz appear to be significantly attenuated, while signals with an amplitude less than 400 Hz have only minor attenuation. In other words, only signals less than 400 Hz (around the cutoff frequency) pass through relatively unattenuated.</p>
<ul>
  <li><strong>Low Frequencies (10 Hz - 500 Hz):</strong>
    <ul>
      <li>The gain values at these lower frequencies are approximately 10, which means that the filter is allowing these lower frequencies to pass with only mild to no attenuation. A high-pass filter would typically attenuate lower frequencies more aggressively, rather than allowing them to pass with relatively modest losses.</li>
    </ul>
  </li>
  <li><strong>Higher Frequencies (10 kHz - 1 MHz):</strong>
    <ul>
      <li>From 10 kHz onward, the gain sharply decreases, at 10 kHz the gain is 9.87, at 50 kHz the gain is 6.79, at 500 kHz the gain is 2.05, and at 1 MHz the gain is 1.46. This significant attenuation of higher frequencies is the key indicator of a low-pass filter, as it demonstrates that the filter is strongly reducing the amplitude of signals in the higher frequency range.</li>
    </ul>
  </li>
</ul>

<h2>Conclusion</h2>
<p>In conclusion, the active low-pass filter constructed using two 10k-ohm resistor, a 1k-ohm resistor and a 0.01uF capacitor successfully attenuates high-frequency signals while allowing lower frequency signals to pass relatively unattenuated. The cutoff frequency calculated generally aligns with the observed results, demonstrating the practical effectiveness of passive RC active low-pass filters in signal processing applications.</p>

<h2>Future Work</h2>
<p>Future improvements could include experimenting with different resistor and capacitor values to modify the cutoff frequency further, utilizing more complex filter designs to achieve sharper roll-offs such as Sallen-Key, Butterworth, or Chebyshev configurations, or a simple task such as debouncing a button.</p>
