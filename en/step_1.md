LEDs can be quite delicate. If you have too much current passing though them, they are likely to **pop**. For this reason, most LEDs are used with a resistor to reduce the voltage they receive.

When you buy LEDs, they normally come with a data sheet like [this one](https://www.rapidonline.com/pdf/55-1792.pdf). There will be a section similar to this on it:

![led spec](images/datasheet.png)

The important values to help you choose a resistor to use with your new LEDs are the **forward voltage** and the **forward current**. In the image above, the forward voltage is _1.7V_ and the forward current is _30mA_.

Now you can use Ohm's law to calculate what kind of resistor you need. Here is the formula you need to use:

![formula](images/formula.gif)

- `Vs` stands for the voltage supply - on a Raspberry Pi that's 3.3V.
- `Vf` stands for the forward voltage of the LED, in this case 1.7V.
- `If` stands for the forward current of the LED, in this case 0.03A (30mA * 1000).

Put all these together like this:

![calculation](images/calc.gif)

You will come to an answer of around 53Ω, so you need a resistor that provides resistance of a value pretty close to this. If its resistance is much higher, your LED will appear dim; if it's much lower, you risk damaging the LED. In this case, the resistor with the closest value you are likely to find is a 56Ω one, but any resistance between 56Ω and about 100Ω would be fine.
