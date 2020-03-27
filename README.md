
# RGBLedSliders

RGB Led connected to an Arduino and controled by sliders in a web page served by an node.js application. This app has been made for education purposes.

## Tech

This application uses the following techologies:
    -[Arduino board](htttp://arduino.cc): with firmata protocol loaded.
    -[node.js](http://nodejs.org).
    -[serialport](https://serialport.io/): Is a module to send and receive data, through serial port, from the arduino in a JavaScript application.
    -[Jonny-five](http://johnny-five.io/): A library to control components that are usually connected to an arduino board such as leds, servos, ...
    -[Express](https://expressjs.com/): Is a module to serve pages to a web browser.
    -[socket.io](https://socket.io/): To send and receive messages between a browser (client) and a node.js application (server)

### Prerequisites

The follogwing are required to run this application:
    -Install the FDTI drivers in the computer where the aruino is attached to. This makes the usb port to be used as a serial port.
    -An arduino UNO board.
    -The arduino IDE.
    -firmata protocol loaded. In de Arduino IDE, load the schetch StandardFirmata.ino to the arduino.
    -RGB led connected to the arduino. I use a common cathode type. The cathode is connected to the ground pin (GND). The red green and blue anodes are conected to PWM outputs on pins 3, 5 and 6 respectively, using 220 ohm resistors.
    -Download and install node.js in your computer to run javascript applications.

### Installing

    -Copy the files in a directory of your choice and type: npm install. This will install all the modules specified in the file package.json
    -Find which serial port is used to connect with the arduino. See in the arduino IDE or in the Device Manager in Windows. By default the serial port is COM5, so in the app.js file set the line: board = new five.Board({port: "COM5"}); to board = new five.Board({port: "COMX"}); where X is your serial port assigned.

## Running the tests

To run the application do the following:
    -In your working directory type: node app.js
    -In your web browser load the page: localhost:3000

## Version

1.0.0 

## Authors

* **Luis Cárceles** - *Initial work* - [GitHub RGBLedSliders](https://github.com/luisC62/RGBLedSliders)

See also the list of [contributors](https://github.com/your/project/contributors) who participated in this project.

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

## Acknowledgments


