DoorDuino
===================
DoorDuino is an Arduino equipped with an [Ethernet Shield](http://arduino.cc/en/Main/ArduinoEthernetShield) that receives secured messages from a [Doorbot](https://github.com/lord/doorbot) server on the local intranet.  Hacker School uses this setup to open the door.

##Installation
To set up your DoorDuino microcontoller, you'll need the following:

+ an Arduino
+ the Arduino sketch files (code), which includes:
    * A modified verison of the `Sha` library, included in this repo
    * The sketch `door_ethernet_server.ino` if you plan to use a hashed secure password to communicate with the Doorbot, or `door_ethernet_server_local.ino` if not
+ Your own `password.h` header file to define the secret password to be included only in the Arduino and on the Doorbot server.  The entirety of the file can be the single line `#define PASSWORD <your password here>`
+ Electronic components
    * Breadboard
    * Wires
    * Relay (Not included with Arduino)
    * Transistor (those that came with the Arduino will do)
    * Alligator clips (most likely)

    <?xml version='1.0' encoding='UTF-8' standalone='no'?>
    <!-- Created with Fritzing (http://www.fritzing.org/) -->
    <svg xmlns:svg='http://www.w3.org/2000/svg' xmlns='http://www.w3.org/2000/svg' version='1.2' baseProfile='tiny' x='0in' y='0in' width='6.31704in' height='3.70167in' viewBox='0 0 454.827 266.52' >
    <g partID='56350'><g transform='translate(197.833,266.52)' ><g transform='matrix(0,-1,1,0,0,0)'  ><g transform="matrix(1, 0, 0, 1, 0.199995, 1.63829e-06)">
     <g  id="breadboardbreadboard">
      <rect  width="233.726" x="2.22043e-17" y="-0.00038177" fill="#d9d9d9" height="151.2" id="rect5"/>
      <rect  width="228.753" x="-0.199995" y="20.9316" fill="#b3b0b0" height="0.4" id="rect8"/>
      <rect  width="230.585" x="-0.199995" y="129.476" fill="#b3b0b0" height="0.4" id="rect10"/>
      <rect  width="224.827" x="-0.199995" y="19.1996" fill="#ff0000" height="0.4" id="rect14"/>
      <rect  width="225.351" x="-0.199995" y="148.8" fill="#ff0000" height="0.4" id="rect16"/>
      <rect  width="224.566" x="-0.199995" y="2.39962" fill="#0000ff" height="0.4" id="rect18"/>
      <rect  width="226.136" x="-0.199995" y="132" fill="#0000ff" height="0.4" id="rect20"/>
      <rect  width="223.257" x="-0.199995" y="71.1996" fill="#ccc9c9" height="7.2" id="rect24"/>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin1A">
        <path  fill="#bfbfbf" id="path28" d="m8.52636,115.2a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path30" d="m13.3135,115.2a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="10.9199" cy="115.2" r="1.19679" id="circle32"/>
       </g>
      </g>7   <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin1B">
        <path  fill="#bfbfbf" id="path35" d="m8.52636,108a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path37" d="m13.3135,108a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="10.9199" cy="108" r="1.19679" id="circle39"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin1C">
        <path  fill="#bfbfbf" id="path42" d="m8.52636,100.8a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path44" d="m13.3135,100.8a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="10.9199" cy="100.8" r="1.19679" id="circle46"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin1D">
        <path  fill="#bfbfbf" id="path49" d="m8.52636,93.6a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path51" d="m13.3135,93.6a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="10.9199" cy="93.6" r="1.19679" id="circle53"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin1E">
        <path  fill="#bfbfbf" id="path56" d="m8.52636,86.4a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path58" d="m13.3135,86.4a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="10.9199" cy="86.4" r="1.19679" id="circle60"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin1F">
        <path  fill="#bfbfbf" id="path63" d="m8.52636,64.8a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path65" d="m13.3135,64.8a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="10.9199" cy="64.8" r="1.19679" id="circle67"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin1G">
        <path  fill="#bfbfbf" id="path70" d="m8.52636,57.6a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path72" d="m13.3135,57.6a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="10.9199" cy="57.6" r="1.19679" id="circle74"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin1H">
        <path  fill="#bfbfbf" id="path77" d="m8.52636,50.4a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path79" d="m13.3135,50.4a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="10.9199" cy="50.4" r="1.19679" id="circle81"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin1I">
        <path  fill="#bfbfbf" id="path84" d="m8.52636,43.2a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path86" d="m13.3135,43.2a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="10.9199" cy="43.2" r="1.19679" id="circle88"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin1J">
        <path  fill="#bfbfbf" id="path91" d="m8.52636,36a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path93" d="m13.3135,36a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="10.9199" cy="36" r="1.19679" id="circle95"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin2A">
        <path  fill="#bfbfbf" id="path98" d="m15.7263,115.2a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path100" d="m20.5135,115.2a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="18.1199" cy="115.2" r="1.19679" id="circle102"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin2B">
        <path  fill="#bfbfbf" id="path105" d="m15.7263,108a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path107" d="m20.5135,108a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="18.1199" cy="108" r="1.19679" id="circle109"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin2C">
        <path  fill="#bfbfbf" id="path112" d="m15.7263,100.8a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path114" d="m20.5135,100.8a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="18.1199" cy="100.8" r="1.19679" id="circle116"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin2D">
        <path  fill="#bfbfbf" id="path119" d="m15.7263,93.6a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path121" d="m20.5135,93.6a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="18.1199" cy="93.6" r="1.19679" id="circle123"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin2E">
        <path  fill="#bfbfbf" id="path126" d="m15.7263,86.4a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path128" d="m20.5135,86.4a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="18.1199" cy="86.4" r="1.19679" id="circle130"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin2F">
        <path  fill="#bfbfbf" id="path133" d="m15.7263,64.8a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path135" d="m20.5135,64.8a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="18.1199" cy="64.8" r="1.19679" id="circle137"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin2G">
        <path  fill="#bfbfbf" id="path140" d="m15.7263,57.6a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path142" d="m20.5135,57.6a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="18.1199" cy="57.6" r="1.19679" id="circle144"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin2H">
        <path  fill="#bfbfbf" id="path147" d="m15.7263,50.4a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path149" d="m20.5135,50.4a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="18.1199" cy="50.4" r="1.19679" id="circle151"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin2I">
        <path  fill="#bfbfbf" id="path154" d="m15.7263,43.2a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path156" d="m20.5135,43.2a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="18.1199" cy="43.2" r="1.19679" id="circle158"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin2J">
        <path  fill="#bfbfbf" id="path161" d="m15.7263,36a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path163" d="m20.5135,36a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="18.1199" cy="36" r="1.19679" id="circle165"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin3A">
        <path  fill="#bfbfbf" id="path168" d="m22.9263,115.2a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path170" d="m27.7135,115.2a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="25.3199" cy="115.2" r="1.19679" id="circle172"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin3B">
        <path  fill="#bfbfbf" id="path175" d="m22.9263,108a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path177" d="m27.7135,108a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="25.3199" cy="108" r="1.19679" id="circle179"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin3C">
        <path  fill="#bfbfbf" id="path182" d="m22.9263,100.8a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path184" d="m27.7135,100.8a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="25.3199" cy="100.8" r="1.19679" id="circle186"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin3D">
        <path  fill="#bfbfbf" id="path189" d="m22.9263,93.6a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path191" d="m27.7135,93.6a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="25.3199" cy="93.6" r="1.19679" id="circle193"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin3E">
        <path  fill="#bfbfbf" id="path196" d="m22.9263,86.4a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path198" d="m27.7135,86.4a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="25.3199" cy="86.4" r="1.19679" id="circle200"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin3F">
        <path  fill="#bfbfbf" id="path203" d="m22.9263,64.8a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path205" d="m27.7135,64.8a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="25.3199" cy="64.8" r="1.19679" id="circle207"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin3G">
        <path  fill="#bfbfbf" id="path210" d="m22.9263,57.6a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path212" d="m27.7135,57.6a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="25.3199" cy="57.6" r="1.19679" id="circle214"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin3H">
        <path  fill="#bfbfbf" id="path217" d="m22.9263,50.4a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path219" d="m27.7135,50.4a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="25.3199" cy="50.4" r="1.19679" id="circle221"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin3I">
        <path  fill="#bfbfbf" id="path224" d="m22.9263,43.2a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path226" d="m27.7135,43.2a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="25.3199" cy="43.2" r="1.19679" id="circle228"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin3J">
        <path  fill="#bfbfbf" id="path231" d="m22.9263,36a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path233" d="m27.7135,36a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="25.3199" cy="36" r="1.19679" id="circle235"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin4A">
        <path  fill="#bfbfbf" id="path238" d="m30.1262,115.2a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path240" d="m34.9134,115.2a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="32.5198" cy="115.2" r="1.19679" id="circle242"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin4B">
        <path  fill="#bfbfbf" id="path245" d="m30.1262,108a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path247" d="m34.9134,108a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="32.5198" cy="108" r="1.19679" id="circle249"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin4C">
        <path  fill="#bfbfbf" id="path252" d="m30.1262,100.8a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path254" d="m34.9134,100.8a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="32.5198" cy="100.8" r="1.19679" id="circle256"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin4D">
        <path  fill="#bfbfbf" id="path259" d="m30.1262,93.6a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path261" d="m34.9134,93.6a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="32.5198" cy="93.6" r="1.19679" id="circle263"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin4E">
        <path  fill="#bfbfbf" id="path266" d="m30.1262,86.4a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path268" d="m34.9134,86.4a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="32.5198" cy="86.4" r="1.19679" id="circle270"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin4F">
        <path  fill="#bfbfbf" id="path273" d="m30.1262,64.8a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path275" d="m34.9134,64.8a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="32.5198" cy="64.8" r="1.19679" id="circle277"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin4G">
        <path  fill="#bfbfbf" id="path280" d="m30.1262,57.6a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path282" d="m34.9134,57.6a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="32.5198" cy="57.6" r="1.19679" id="circle284"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin4H">
        <path  fill="#bfbfbf" id="path287" d="m30.1262,50.4a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path289" d="m34.9134,50.4a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="32.5198" cy="50.4" r="1.19679" id="circle291"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin4I">
        <path  fill="#bfbfbf" id="path294" d="m30.1262,43.2a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path296" d="m34.9134,43.2a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="32.5198" cy="43.2" r="1.19679" id="circle298"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin4J">
        <path  fill="#bfbfbf" id="path301" d="m30.1262,36a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path303" d="m34.9134,36a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="32.5198" cy="36" r="1.19679" id="circle305"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin5A">
        <path  fill="#bfbfbf" id="path308" d="m37.3262,115.2a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path310" d="m42.1134,115.2a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="39.7198" cy="115.2" r="1.19679" id="circle312"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin5B">
        <path  fill="#bfbfbf" id="path315" d="m37.3262,108a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path317" d="m42.1134,108a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="39.7198" cy="108" r="1.19679" id="circle319"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin5C">
        <path  fill="#bfbfbf" id="path322" d="m37.3262,100.8a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path324" d="m42.1134,100.8a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="39.7198" cy="100.8" r="1.19679" id="circle326"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin5D">
        <path  fill="#bfbfbf" id="path329" d="m37.3262,93.6a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path331" d="m42.1134,93.6a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="39.7198" cy="93.6" r="1.19679" id="circle333"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin5E">
        <path  fill="#bfbfbf" id="path336" d="m37.3262,86.4a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path338" d="m42.1134,86.4a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="39.7198" cy="86.4" r="1.19679" id="circle340"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin5F">
        <path  fill="#bfbfbf" id="path343" d="m37.3262,64.8a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path345" d="m42.1134,64.8a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="39.7198" cy="64.8" r="1.19679" id="circle347"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin5G">
        <path  fill="#bfbfbf" id="path350" d="m37.3262,57.6a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path352" d="m42.1134,57.6a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="39.7198" cy="57.6" r="1.19679" id="circle354"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin5H">
        <path  fill="#bfbfbf" id="path357" d="m37.3262,50.4a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path359" d="m42.1134,50.4a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="39.7198" cy="50.4" r="1.19679" id="circle361"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin5I">
        <path  fill="#bfbfbf" id="path364" d="m37.3262,43.2a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path366" d="m42.1134,43.2a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="39.7198" cy="43.2" r="1.19679" id="circle368"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin5J">
        <path  fill="#bfbfbf" id="path371" d="m37.3262,36a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path373" d="m42.1134,36a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="39.7198" cy="36" r="1.19679" id="circle375"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin6A">
        <path  fill="#bfbfbf" id="path378" d="m44.5262,115.2a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path380" d="m49.3133,115.2a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="46.9198" cy="115.2" r="1.19679" id="circle382"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin6B">
        <path  fill="#bfbfbf" id="path385" d="m44.5262,108a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path387" d="m49.3133,108a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="46.9198" cy="108" r="1.19679" id="circle389"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin6C">
        <path  fill="#bfbfbf" id="path392" d="m44.5262,100.8a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path394" d="m49.3133,100.8a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="46.9198" cy="100.8" r="1.19679" id="circle396"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin6D">
        <path  fill="#bfbfbf" id="path399" d="m44.5262,93.6a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path401" d="m49.3133,93.6a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="46.9198" cy="93.6" r="1.19679" id="circle403"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin6E">
        <path  fill="#bfbfbf" id="path406" d="m44.5262,86.4a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path408" d="m49.3133,86.4a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="46.9198" cy="86.4" r="1.19679" id="circle410"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin6F">
        <path  fill="#bfbfbf" id="path413" d="m44.5262,64.8a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path415" d="m49.3133,64.8a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="46.9198" cy="64.8" r="1.19679" id="circle417"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin6G">
        <path  fill="#bfbfbf" id="path420" d="m44.5262,57.6a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path422" d="m49.3133,57.6a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="46.9198" cy="57.6" r="1.19679" id="circle424"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin6H">
        <path  fill="#bfbfbf" id="path427" d="m44.5262,50.4a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path429" d="m49.3133,50.4a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="46.9198" cy="50.4" r="1.19679" id="circle431"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin6I">
        <path  fill="#bfbfbf" id="path434" d="m44.5262,43.2a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path436" d="m49.3133,43.2a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="46.9198" cy="43.2" r="1.19679" id="circle438"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin6J">
        <path  fill="#bfbfbf" id="path441" d="m44.5262,36a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path443" d="m49.3133,36a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="46.9198" cy="36" r="1.19679" id="circle445"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin7A">
        <path  fill="#bfbfbf" id="path448" d="m51.7261,115.2a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path450" d="m56.5133,115.2a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="54.1197" cy="115.2" r="1.19679" id="circle452"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin7B">
        <path  fill="#bfbfbf" id="path455" d="m51.7261,108a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path457" d="m56.5133,108a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="54.1197" cy="108" r="1.19679" id="circle459"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin7C">
        <path  fill="#bfbfbf" id="path462" d="m51.7261,100.8a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path464" d="m56.5133,100.8a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="54.1197" cy="100.8" r="1.19679" id="circle466"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin7D">
        <path  fill="#bfbfbf" id="path469" d="m51.7261,93.6a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path471" d="m56.5133,93.6a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="54.1197" cy="93.6" r="1.19679" id="circle473"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin7E">
        <path  fill="#bfbfbf" id="path476" d="m51.7261,86.4a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path478" d="m56.5133,86.4a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="54.1197" cy="86.4" r="1.19679" id="circle480"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin7F">
        <path  fill="#bfbfbf" id="path483" d="m51.7261,64.8a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path485" d="m56.5133,64.8a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="54.1197" cy="64.8" r="1.19679" id="circle487"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin7G">
        <path  fill="#bfbfbf" id="path490" d="m51.7261,57.6a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path492" d="m56.5133,57.6a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="54.1197" cy="57.6" r="1.19679" id="circle494"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin7H">
        <path  fill="#bfbfbf" id="path497" d="m51.7261,50.4a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path499" d="m56.5133,50.4a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="54.1197" cy="50.4" r="1.19679" id="circle501"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin7I">
        <path  fill="#bfbfbf" id="path504" d="m51.7261,43.2a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path506" d="m56.5133,43.2a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="54.1197" cy="43.2" r="1.19679" id="circle508"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin7J">
        <path  fill="#bfbfbf" id="path511" d="m51.7261,36a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path513" d="m56.5133,36a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="54.1197" cy="36" r="1.19679" id="circle515"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin8A">
        <path  fill="#bfbfbf" id="path518" d="m58.9261,115.2a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path520" d="m63.7133,115.2a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="61.3197" cy="115.2" r="1.19679" id="circle522"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin8B">
        <path  fill="#bfbfbf" id="path525" d="m58.9261,108a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path527" d="m63.7133,108a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="61.3197" cy="108" r="1.19679" id="circle529"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin8C">
        <path  fill="#bfbfbf" id="path532" d="m58.9261,100.8a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path534" d="m63.7133,100.8a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="61.3197" cy="100.8" r="1.19679" id="circle536"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin8D">
        <path  fill="#bfbfbf" id="path539" d="m58.9261,93.6a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path541" d="m63.7133,93.6a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="61.3197" cy="93.6" r="1.19679" id="circle543"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin8E">
        <path  fill="#bfbfbf" id="path546" d="m58.9261,86.4a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path548" d="m63.7133,86.4a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="61.3197" cy="86.4" r="1.19679" id="circle550"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin8F">
        <path  fill="#bfbfbf" id="path553" d="m58.9261,64.8a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path555" d="m63.7133,64.8a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="61.3197" cy="64.8" r="1.19679" id="circle557"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin8G">
        <path  fill="#bfbfbf" id="path560" d="m58.9261,57.6a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path562" d="m63.7133,57.6a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="61.3197" cy="57.6" r="1.19679" id="circle564"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin8H">
        <path  fill="#bfbfbf" id="path567" d="m58.9261,50.4a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path569" d="m63.7133,50.4a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="61.3197" cy="50.4" r="1.19679" id="circle571"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin8I">
        <path  fill="#bfbfbf" id="path574" d="m58.9261,43.2a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path576" d="m63.7133,43.2a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="61.3197" cy="43.2" r="1.19679" id="circle578"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin8J">
        <path  fill="#bfbfbf" id="path581" d="m58.9261,36a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path583" d="m63.7133,36a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="61.3197" cy="36" r="1.19679" id="circle585"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin9A">
        <path  fill="#bfbfbf" id="path588" d="m66.1261,115.2a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path590" d="m70.9132,115.2a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="68.5197" cy="115.2" r="1.19679" id="circle592"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin9B">
        <path  fill="#bfbfbf" id="path595" d="m66.1261,108a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path597" d="m70.9132,108a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="68.5197" cy="108" r="1.19679" id="circle599"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin9C">
        <path  fill="#bfbfbf" id="path602" d="m66.1261,100.8a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path604" d="m70.9132,100.8a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="68.5197" cy="100.8" r="1.19679" id="circle606"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin9D">
        <path  fill="#bfbfbf" id="path609" d="m66.1261,93.6a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path611" d="m70.9132,93.6a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="68.5197" cy="93.6" r="1.19679" id="circle613"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin9E">
        <path  fill="#bfbfbf" id="path616" d="m66.1261,86.4a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path618" d="m70.9132,86.4a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="68.5197" cy="86.4" r="1.19679" id="circle620"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin9F">
        <path  fill="#bfbfbf" id="path623" d="m66.1261,64.8a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path625" d="m70.9132,64.8a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="68.5197" cy="64.8" r="1.19679" id="circle627"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin9G">
        <path  fill="#bfbfbf" id="path630" d="m66.1261,57.6a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path632" d="m70.9132,57.6a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="68.5197" cy="57.6" r="1.19679" id="circle634"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin9H">
        <path  fill="#bfbfbf" id="path637" d="m66.1261,50.4a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path639" d="m70.9132,50.4a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="68.5197" cy="50.4" r="1.19679" id="circle641"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin9I">
        <path  fill="#bfbfbf" id="path644" d="m66.1261,43.2a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path646" d="m70.9132,43.2a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="68.5197" cy="43.2" r="1.19679" id="circle648"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin9J">
        <path  fill="#bfbfbf" id="path651" d="m66.1261,36a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path653" d="m70.9132,36a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="68.5197" cy="36" r="1.19679" id="circle655"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin10A">
        <path  fill="#bfbfbf" id="path658" d="m73.326,115.2a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path660" d="m78.1132,115.2a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="75.7196" cy="115.2" r="1.19679" id="circle662"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin10B">
        <path  fill="#bfbfbf" id="path665" d="m73.326,108a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path667" d="m78.1132,108a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="75.7196" cy="108" r="1.19679" id="circle669"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin10C">
        <path  fill="#bfbfbf" id="path672" d="m73.326,100.8a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path674" d="m78.1132,100.8a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="75.7196" cy="100.8" r="1.19679" id="circle676"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin10D">
        <path  fill="#bfbfbf" id="path679" d="m73.326,93.6a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path681" d="m78.1132,93.6a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="75.7196" cy="93.6" r="1.19679" id="circle683"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin10E">
        <path  fill="#bfbfbf" id="path686" d="m73.326,86.4a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path688" d="m78.1132,86.4a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="75.7196" cy="86.4" r="1.19679" id="circle690"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin10F">
        <path  fill="#bfbfbf" id="path693" d="m73.326,64.8a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path695" d="m78.1132,64.8a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="75.7196" cy="64.8" r="1.19679" id="circle697"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin10G">
        <path  fill="#bfbfbf" id="path700" d="m73.326,57.6a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path702" d="m78.1132,57.6a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="75.7196" cy="57.6" r="1.19679" id="circle704"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin10H">
        <path  fill="#bfbfbf" id="path707" d="m73.326,50.4a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path709" d="m78.1132,50.4a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="75.7196" cy="50.4" r="1.19679" id="circle711"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin10I">
        <path  fill="#bfbfbf" id="path714" d="m73.326,43.2a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path716" d="m78.1132,43.2a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="75.7196" cy="43.2" r="1.19679" id="circle718"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin10J">
        <path  fill="#bfbfbf" id="path721" d="m73.326,36a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path723" d="m78.1132,36a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="75.7196" cy="36" r="1.19679" id="circle725"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin11A">
        <path  fill="#bfbfbf" id="path728" d="m80.526,115.2a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path730" d="m85.3132,115.2a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="82.9196" cy="115.2" r="1.19679" id="circle732"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin11B">
        <path  fill="#bfbfbf" id="path735" d="m80.526,108a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path737" d="m85.3132,108a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="82.9196" cy="108" r="1.19679" id="circle739"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin11C">
        <path  fill="#bfbfbf" id="path742" d="m80.526,100.8a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path744" d="m85.3132,100.8a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="82.9196" cy="100.8" r="1.19679" id="circle746"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin11D">
        <path  fill="#bfbfbf" id="path749" d="m80.526,93.6a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path751" d="m85.3132,93.6a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="82.9196" cy="93.6" r="1.19679" id="circle753"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin11E">
        <path  fill="#bfbfbf" id="path756" d="m80.526,86.4a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path758" d="m85.3132,86.4a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="82.9196" cy="86.4" r="1.19679" id="circle760"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin11F">
        <path  fill="#bfbfbf" id="path763" d="m80.526,64.8a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path765" d="m85.3132,64.8a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="82.9196" cy="64.8" r="1.19679" id="circle767"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin11G">
        <path  fill="#bfbfbf" id="path770" d="m80.526,57.6a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path772" d="m85.3132,57.6a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="82.9196" cy="57.6" r="1.19679" id="circle774"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin11H">
        <path  fill="#bfbfbf" id="path777" d="m80.526,50.4a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path779" d="m85.3132,50.4a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="82.9196" cy="50.4" r="1.19679" id="circle781"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin11I">
        <path  fill="#bfbfbf" id="path784" d="m80.526,43.2a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path786" d="m85.3132,43.2a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="82.9196" cy="43.2" r="1.19679" id="circle788"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin11J">
        <path  fill="#bfbfbf" id="path791" d="m80.526,36a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path793" d="m85.3132,36a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="82.9196" cy="36" r="1.19679" id="circle795"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin12A">
        <path  fill="#bfbfbf" id="path798" d="m87.726,115.2a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path800" d="m92.5131,115.2a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="90.1195" cy="115.2" r="1.19679" id="circle802"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin12B">
        <path  fill="#bfbfbf" id="path805" d="m87.726,108a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path807" d="m92.5131,108a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="90.1195" cy="108" r="1.19679" id="circle809"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin12C">
        <path  fill="#bfbfbf" id="path812" d="m87.726,100.8a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path814" d="m92.5131,100.8a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="90.1195" cy="100.8" r="1.19679" id="circle816"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin12D">
        <path  fill="#bfbfbf" id="path819" d="m87.726,93.6a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path821" d="m92.5131,93.6a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="90.1195" cy="93.6" r="1.19679" id="circle823"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin12E">
        <path  fill="#bfbfbf" id="path826" d="m87.726,86.4a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path828" d="m92.5131,86.4a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="90.1195" cy="86.4" r="1.19679" id="circle830"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin12F">
        <path  fill="#bfbfbf" id="path833" d="m87.726,64.8a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path835" d="m92.5131,64.8a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="90.1195" cy="64.8" r="1.19679" id="circle837"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin12G">
        <path  fill="#bfbfbf" id="path840" d="m87.726,57.6a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path842" d="m92.5131,57.6a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="90.1195" cy="57.6" r="1.19679" id="circle844"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin12H">
        <path  fill="#bfbfbf" id="path847" d="m87.726,50.4a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path849" d="m92.5131,50.4a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="90.1195" cy="50.4" r="1.19679" id="circle851"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin12I">
        <path  fill="#bfbfbf" id="path854" d="m87.726,43.2a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path856" d="m92.5131,43.2a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="90.1195" cy="43.2" r="1.19679" id="circle858"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin12J">
        <path  fill="#bfbfbf" id="path861" d="m87.726,36a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path863" d="m92.5131,36a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="90.1195" cy="36" r="1.19679" id="circle865"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin13A">
        <path  fill="#bfbfbf" id="path868" d="m94.9259,115.2a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path870" d="m99.7131,115.2a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="97.3195" cy="115.2" r="1.19679" id="circle872"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin13B">
        <path  fill="#bfbfbf" id="path875" d="m94.9259,108a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path877" d="m99.7131,108a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="97.3195" cy="108" r="1.19679" id="circle879"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin13C">
        <path  fill="#bfbfbf" id="path882" d="m94.9259,100.8a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path884" d="m99.7131,100.8a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="97.3195" cy="100.8" r="1.19679" id="circle886"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin13D">
        <path  fill="#bfbfbf" id="path889" d="m94.9259,93.6a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path891" d="m99.7131,93.6a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="97.3195" cy="93.6" r="1.19679" id="circle893"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin13E">
        <path  fill="#bfbfbf" id="path896" d="m94.9259,86.4a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path898" d="m99.7131,86.4a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="97.3195" cy="86.4" r="1.19679" id="circle900"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin13F">
        <path  fill="#bfbfbf" id="path903" d="m94.9259,64.8a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path905" d="m99.7131,64.8a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="97.3195" cy="64.8" r="1.19679" id="circle907"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin13G">
        <path  fill="#bfbfbf" id="path910" d="m94.9259,57.6a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path912" d="m99.7131,57.6a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="97.3195" cy="57.6" r="1.19679" id="circle914"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin13H">
        <path  fill="#bfbfbf" id="path917" d="m94.9259,50.4a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path919" d="m99.7131,50.4a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="97.3195" cy="50.4" r="1.19679" id="circle921"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin13I">
        <path  fill="#bfbfbf" id="path924" d="m94.9259,43.2a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path926" d="m99.7131,43.2a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="97.3195" cy="43.2" r="1.19679" id="circle928"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin13J">
        <path  fill="#bfbfbf" id="path931" d="m94.9259,36a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path933" d="m99.7131,36a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="97.3195" cy="36" r="1.19679" id="circle935"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin14A">
        <path  fill="#bfbfbf" id="path938" d="m102.126,115.2a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path940" d="m106.913,115.2a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="104.519" cy="115.2" r="1.19679" id="circle942"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin14B">
        <path  fill="#bfbfbf" id="path945" d="m102.126,108a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path947" d="m106.913,108a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="104.519" cy="108" r="1.19679" id="circle949"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin14C">
        <path  fill="#bfbfbf" id="path952" d="m102.126,100.8a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path954" d="m106.913,100.8a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="104.519" cy="100.8" r="1.19679" id="circle956"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin14D">
        <path  fill="#bfbfbf" id="path959" d="m102.126,93.6a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path961" d="m106.913,93.6a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="104.519" cy="93.6" r="1.19679" id="circle963"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin14E">
        <path  fill="#bfbfbf" id="path966" d="m102.126,86.4a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path968" d="m106.913,86.4a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="104.519" cy="86.4" r="1.19679" id="circle970"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin14F">
        <path  fill="#bfbfbf" id="path973" d="m102.126,64.8a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path975" d="m106.913,64.8a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="104.519" cy="64.8" r="1.19679" id="circle977"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin14G">
        <path  fill="#bfbfbf" id="path980" d="m102.126,57.6a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path982" d="m106.913,57.6a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="104.519" cy="57.6" r="1.19679" id="circle984"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin14H">
        <path  fill="#bfbfbf" id="path987" d="m102.126,50.4a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path989" d="m106.913,50.4a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="104.519" cy="50.4" r="1.19679" id="circle991"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin14I">
        <path  fill="#bfbfbf" id="path994" d="m102.126,43.2a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path996" d="m106.913,43.2a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="104.519" cy="43.2" r="1.19679" id="circle998"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin14J">
        <path  fill="#bfbfbf" id="path1001" d="m102.126,36a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1003" d="m106.913,36a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="104.519" cy="36" r="1.19679" id="circle1005"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin15A">
        <path  fill="#bfbfbf" id="path1008" d="m109.326,115.2a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1010" d="m114.113,115.2a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="111.719" cy="115.2" r="1.19679" id="circle1012"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin15B">
        <path  fill="#bfbfbf" id="path1015" d="m109.326,108a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1017" d="m114.113,108a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="111.719" cy="108" r="1.19679" id="circle1019"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin15C">
        <path  fill="#bfbfbf" id="path1022" d="m109.326,100.8a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1024" d="m114.113,100.8a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="111.719" cy="100.8" r="1.19679" id="circle1026"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin15D">
        <path  fill="#bfbfbf" id="path1029" d="m109.326,93.6a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1031" d="m114.113,93.6a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="111.719" cy="93.6" r="1.19679" id="circle1033"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin15E">
        <path  fill="#bfbfbf" id="path1036" d="m109.326,86.4a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1038" d="m114.113,86.4a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="111.719" cy="86.4" r="1.19679" id="circle1040"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin15F">
        <path  fill="#bfbfbf" id="path1043" d="m109.326,64.8a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1045" d="m114.113,64.8a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="111.719" cy="64.8" r="1.19679" id="circle1047"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin15G">
        <path  fill="#bfbfbf" id="path1050" d="m109.326,57.6a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1052" d="m114.113,57.6a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="111.719" cy="57.6" r="1.19679" id="circle1054"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin15H">
        <path  fill="#bfbfbf" id="path1057" d="m109.326,50.4a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1059" d="m114.113,50.4a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="111.719" cy="50.4" r="1.19679" id="circle1061"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin15I">
        <path  fill="#bfbfbf" id="path1064" d="m109.326,43.2a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1066" d="m114.113,43.2a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="111.719" cy="43.2" r="1.19679" id="circle1068"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin15J">
        <path  fill="#bfbfbf" id="path1071" d="m109.326,36a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1073" d="m114.113,36a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="111.719" cy="36" r="1.19679" id="circle1075"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin16A">
        <path  fill="#bfbfbf" id="path1078" d="m116.526,115.2a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1080" d="m121.313,115.2a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="118.919" cy="115.2" r="1.19679" id="circle1082"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin16B">
        <path  fill="#bfbfbf" id="path1085" d="m116.526,108a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1087" d="m121.313,108a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="118.919" cy="108" r="1.19679" id="circle1089"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin16C">
        <path  fill="#bfbfbf" id="path1092" d="m116.526,100.8a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1094" d="m121.313,100.8a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="118.919" cy="100.8" r="1.19679" id="circle1096"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin16D">
        <path  fill="#bfbfbf" id="path1099" d="m116.526,93.6a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1101" d="m121.313,93.6a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="118.919" cy="93.6" r="1.19679" id="circle1103"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin16E">
        <path  fill="#bfbfbf" id="path1106" d="m116.526,86.4a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1108" d="m121.313,86.4a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="118.919" cy="86.4" r="1.19679" id="circle1110"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin16F">
        <path  fill="#bfbfbf" id="path1113" d="m116.526,64.8a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1115" d="m121.313,64.8a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="118.919" cy="64.8" r="1.19679" id="circle1117"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin16G">
        <path  fill="#bfbfbf" id="path1120" d="m116.526,57.6a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1122" d="m121.313,57.6a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="118.919" cy="57.6" r="1.19679" id="circle1124"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin16H">
        <path  fill="#bfbfbf" id="path1127" d="m116.526,50.4a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1129" d="m121.313,50.4a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="118.919" cy="50.4" r="1.19679" id="circle1131"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin16I">
        <path  fill="#bfbfbf" id="path1134" d="m116.526,43.2a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1136" d="m121.313,43.2a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="118.919" cy="43.2" r="1.19679" id="circle1138"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin16J">
        <path  fill="#bfbfbf" id="path1141" d="m116.526,36a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1143" d="m121.313,36a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="118.919" cy="36" r="1.19679" id="circle1145"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin17A">
        <path  fill="#bfbfbf" id="path1148" d="m123.726,115.2a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1150" d="m128.513,115.2a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="126.119" cy="115.2" r="1.19679" id="circle1152"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin17B">
        <path  fill="#bfbfbf" id="path1155" d="m123.726,108a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1157" d="m128.513,108a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="126.119" cy="108" r="1.19679" id="circle1159"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin17C">
        <path  fill="#bfbfbf" id="path1162" d="m123.726,100.8a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1164" d="m128.513,100.8a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="126.119" cy="100.8" r="1.19679" id="circle1166"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin17D">
        <path  fill="#bfbfbf" id="path1169" d="m123.726,93.6a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1171" d="m128.513,93.6a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="126.119" cy="93.6" r="1.19679" id="circle1173"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin17E">
        <path  fill="#bfbfbf" id="path1176" d="m123.726,86.4a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1178" d="m128.513,86.4a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="126.119" cy="86.4" r="1.19679" id="circle1180"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin17F">
        <path  fill="#bfbfbf" id="path1183" d="m123.726,64.8a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1185" d="m128.513,64.8a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="126.119" cy="64.8" r="1.19679" id="circle1187"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin17G">
        <path  fill="#bfbfbf" id="path1190" d="m123.726,57.6a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1192" d="m128.513,57.6a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="126.119" cy="57.6" r="1.19679" id="circle1194"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin17H">
        <path  fill="#bfbfbf" id="path1197" d="m123.726,50.4a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1199" d="m128.513,50.4a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="126.119" cy="50.4" r="1.19679" id="circle1201"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin17I">
        <path  fill="#bfbfbf" id="path1204" d="m123.726,43.2a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1206" d="m128.513,43.2a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="126.119" cy="43.2" r="1.19679" id="circle1208"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin17J">
        <path  fill="#bfbfbf" id="path1211" d="m123.726,36a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1213" d="m128.513,36a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="126.119" cy="36" r="1.19679" id="circle1215"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin18A">
        <path  fill="#bfbfbf" id="path1218" d="m130.926,115.2a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1220" d="m135.713,115.2a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="133.319" cy="115.2" r="1.19679" id="circle1222"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin18B">
        <path  fill="#bfbfbf" id="path1225" d="m130.926,108a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1227" d="m135.713,108a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="133.319" cy="108" r="1.19679" id="circle1229"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin18C">
        <path  fill="#bfbfbf" id="path1232" d="m130.926,100.8a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1234" d="m135.713,100.8a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="133.319" cy="100.8" r="1.19679" id="circle1236"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin18D">
        <path  fill="#bfbfbf" id="path1239" d="m130.926,93.6a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1241" d="m135.713,93.6a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="133.319" cy="93.6" r="1.19679" id="circle1243"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin18E">
        <path  fill="#bfbfbf" id="path1246" d="m130.926,86.4a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1248" d="m135.713,86.4a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="133.319" cy="86.4" r="1.19679" id="circle1250"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin18F">
        <path  fill="#bfbfbf" id="path1253" d="m130.926,64.8a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1255" d="m135.713,64.8a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="133.319" cy="64.8" r="1.19679" id="circle1257"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin18G">
        <path  fill="#bfbfbf" id="path1260" d="m130.926,57.6a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1262" d="m135.713,57.6a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="133.319" cy="57.6" r="1.19679" id="circle1264"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin18H">
        <path  fill="#bfbfbf" id="path1267" d="m130.926,50.4a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1269" d="m135.713,50.4a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="133.319" cy="50.4" r="1.19679" id="circle1271"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin18I">
        <path  fill="#bfbfbf" id="path1274" d="m130.926,43.2a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1276" d="m135.713,43.2a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="133.319" cy="43.2" r="1.19679" id="circle1278"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin18J">
        <path  fill="#bfbfbf" id="path1281" d="m130.926,36a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1283" d="m135.713,36a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="133.319" cy="36" r="1.19679" id="circle1285"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin19A">
        <path  fill="#bfbfbf" id="path1288" d="m138.126,115.2a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1290" d="m142.913,115.2a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="140.519" cy="115.2" r="1.19679" id="circle1292"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin19B">
        <path  fill="#bfbfbf" id="path1295" d="m138.126,108a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1297" d="m142.913,108a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="140.519" cy="108" r="1.19679" id="circle1299"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin19C">
        <path  fill="#bfbfbf" id="path1302" d="m138.126,100.8a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1304" d="m142.913,100.8a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="140.519" cy="100.8" r="1.19679" id="circle1306"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin19D">
        <path  fill="#bfbfbf" id="path1309" d="m138.126,93.6a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1311" d="m142.913,93.6a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="140.519" cy="93.6" r="1.19679" id="circle1313"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin19E">
        <path  fill="#bfbfbf" id="path1316" d="m138.126,86.4a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1318" d="m142.913,86.4a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="140.519" cy="86.4" r="1.19679" id="circle1320"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin19F">
        <path  fill="#bfbfbf" id="path1323" d="m138.126,64.8a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1325" d="m142.913,64.8a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="140.519" cy="64.8" r="1.19679" id="circle1327"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin19G">
        <path  fill="#bfbfbf" id="path1330" d="m138.126,57.6a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1332" d="m142.913,57.6a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="140.519" cy="57.6" r="1.19679" id="circle1334"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin19H">
        <path  fill="#bfbfbf" id="path1337" d="m138.126,50.4a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1339" d="m142.913,50.4a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="140.519" cy="50.4" r="1.19679" id="circle1341"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin19I">
        <path  fill="#bfbfbf" id="path1344" d="m138.126,43.2a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1346" d="m142.913,43.2a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="140.519" cy="43.2" r="1.19679" id="circle1348"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin19J">
        <path  fill="#bfbfbf" id="path1351" d="m138.126,36a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1353" d="m142.913,36a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="140.519" cy="36" r="1.19679" id="circle1355"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin20A">
        <path  fill="#bfbfbf" id="path1358" d="m145.326,115.2a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1360" d="m150.113,115.2a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="147.719" cy="115.2" r="1.19679" id="circle1362"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin20B">
        <path  fill="#bfbfbf" id="path1365" d="m145.326,108a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1367" d="m150.113,108a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="147.719" cy="108" r="1.19679" id="circle1369"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin20C">
        <path  fill="#bfbfbf" id="path1372" d="m145.326,100.8a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1374" d="m150.113,100.8a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="147.719" cy="100.8" r="1.19679" id="circle1376"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin20D">
        <path  fill="#bfbfbf" id="path1379" d="m145.326,93.6a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1381" d="m150.113,93.6a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="147.719" cy="93.6" r="1.19679" id="circle1383"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin20E">
        <path  fill="#bfbfbf" id="path1386" d="m145.326,86.4a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1388" d="m150.113,86.4a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="147.719" cy="86.4" r="1.19679" id="circle1390"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin20F">
        <path  fill="#bfbfbf" id="path1393" d="m145.326,64.8a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1395" d="m150.113,64.8a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="147.719" cy="64.8" r="1.19679" id="circle1397"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin20G">
        <path  fill="#bfbfbf" id="path1400" d="m145.326,57.6a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1402" d="m150.113,57.6a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="147.719" cy="57.6" r="1.19679" id="circle1404"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin20H">
        <path  fill="#bfbfbf" id="path1407" d="m145.326,50.4a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1409" d="m150.113,50.4a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="147.719" cy="50.4" r="1.19679" id="circle1411"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin20I">
        <path  fill="#bfbfbf" id="path1414" d="m145.326,43.2a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1416" d="m150.113,43.2a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="147.719" cy="43.2" r="1.19679" id="circle1418"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin20J">
        <path  fill="#bfbfbf" id="path1421" d="m145.326,36a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1423" d="m150.113,36a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="147.719" cy="36" r="1.19679" id="circle1425"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin21A">
        <path  fill="#bfbfbf" id="path1428" d="m152.526,115.2a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1430" d="m157.313,115.2a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="154.919" cy="115.2" r="1.19679" id="circle1432"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin21B">
        <path  fill="#bfbfbf" id="path1435" d="m152.526,108a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1437" d="m157.313,108a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="154.919" cy="108" r="1.19679" id="circle1439"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin21C">
        <path  fill="#bfbfbf" id="path1442" d="m152.526,100.8a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1444" d="m157.313,100.8a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="154.919" cy="100.8" r="1.19679" id="circle1446"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin21D">
        <path  fill="#bfbfbf" id="path1449" d="m152.526,93.6a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1451" d="m157.313,93.6a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="154.919" cy="93.6" r="1.19679" id="circle1453"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin21E">
        <path  fill="#bfbfbf" id="path1456" d="m152.526,86.4a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1458" d="m157.313,86.4a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="154.919" cy="86.4" r="1.19679" id="circle1460"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin21F">
        <path  fill="#bfbfbf" id="path1463" d="m152.526,64.8a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1465" d="m157.313,64.8a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="154.919" cy="64.8" r="1.19679" id="circle1467"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin21G">
        <path  fill="#bfbfbf" id="path1470" d="m152.526,57.6a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1472" d="m157.313,57.6a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="154.919" cy="57.6" r="1.19679" id="circle1474"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin21H">
        <path  fill="#bfbfbf" id="path1477" d="m152.526,50.4a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1479" d="m157.313,50.4a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="154.919" cy="50.4" r="1.19679" id="circle1481"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin21I">
        <path  fill="#bfbfbf" id="path1484" d="m152.526,43.2a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1486" d="m157.313,43.2a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="154.919" cy="43.2" r="1.19679" id="circle1488"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin21J">
        <path  fill="#bfbfbf" id="path1491" d="m152.526,36a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1493" d="m157.313,36a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="154.919" cy="36" r="1.19679" id="circle1495"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin22A">
        <path  fill="#bfbfbf" id="path1498" d="m159.726,115.2a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1500" d="m164.513,115.2a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="162.119" cy="115.2" r="1.19679" id="circle1502"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin22B">
        <path  fill="#bfbfbf" id="path1505" d="m159.726,108a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1507" d="m164.513,108a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="162.119" cy="108" r="1.19679" id="circle1509"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin22C">
        <path  fill="#bfbfbf" id="path1512" d="m159.726,100.8a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1514" d="m164.513,100.8a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="162.119" cy="100.8" r="1.19679" id="circle1516"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin22D">
        <path  fill="#bfbfbf" id="path1519" d="m159.726,93.6a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1521" d="m164.513,93.6a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="162.119" cy="93.6" r="1.19679" id="circle1523"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin22E">
        <path  fill="#bfbfbf" id="path1526" d="m159.726,86.4a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1528" d="m164.513,86.4a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="162.119" cy="86.4" r="1.19679" id="circle1530"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin22F">
        <path  fill="#bfbfbf" id="path1533" d="m159.726,64.8a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1535" d="m164.513,64.8a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="162.119" cy="64.8" r="1.19679" id="circle1537"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin22G">
        <path  fill="#bfbfbf" id="path1540" d="m159.726,57.6a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1542" d="m164.513,57.6a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="162.119" cy="57.6" r="1.19679" id="circle1544"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin22H">
        <path  fill="#bfbfbf" id="path1547" d="m159.726,50.4a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1549" d="m164.513,50.4a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="162.119" cy="50.4" r="1.19679" id="circle1551"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin22I">
        <path  fill="#bfbfbf" id="path1554" d="m159.726,43.2a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1556" d="m164.513,43.2a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="162.119" cy="43.2" r="1.19679" id="circle1558"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin22J">
        <path  fill="#bfbfbf" id="path1561" d="m159.726,36a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1563" d="m164.513,36a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="162.119" cy="36" r="1.19679" id="circle1565"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin23A">
        <path  fill="#bfbfbf" id="path1568" d="m166.926,115.2a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1570" d="m171.713,115.2a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="169.319" cy="115.2" r="1.19679" id="circle1572"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin23B">
        <path  fill="#bfbfbf" id="path1575" d="m166.926,108a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1577" d="m171.713,108a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="169.319" cy="108" r="1.19679" id="circle1579"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin23C">
        <path  fill="#bfbfbf" id="path1582" d="m166.926,100.8a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1584" d="m171.713,100.8a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="169.319" cy="100.8" r="1.19679" id="circle1586"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin23D">
        <path  fill="#bfbfbf" id="path1589" d="m166.926,93.6a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1591" d="m171.713,93.6a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="169.319" cy="93.6" r="1.19679" id="circle1593"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin23E">
        <path  fill="#bfbfbf" id="path1596" d="m166.926,86.4a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1598" d="m171.713,86.4a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="169.319" cy="86.4" r="1.19679" id="circle1600"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin23F">
        <path  fill="#bfbfbf" id="path1603" d="m166.926,64.8a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1605" d="m171.713,64.8a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="169.319" cy="64.8" r="1.19679" id="circle1607"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin23G">
        <path  fill="#bfbfbf" id="path1610" d="m166.926,57.6a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1612" d="m171.713,57.6a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="169.319" cy="57.6" r="1.19679" id="circle1614"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin23H">
        <path  fill="#bfbfbf" id="path1617" d="m166.926,50.4a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1619" d="m171.713,50.4a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="169.319" cy="50.4" r="1.19679" id="circle1621"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin23I">
        <path  fill="#bfbfbf" id="path1624" d="m166.926,43.2a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1626" d="m171.713,43.2a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="169.319" cy="43.2" r="1.19679" id="circle1628"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin23J">
        <path  fill="#bfbfbf" id="path1631" d="m166.926,36a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1633" d="m171.713,36a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="169.319" cy="36" r="1.19679" id="circle1635"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin24A">
        <path  fill="#bfbfbf" id="path1638" d="m174.126,115.2a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1640" d="m178.913,115.2a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="176.519" cy="115.2" r="1.19679" id="circle1642"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin24B">
        <path  fill="#bfbfbf" id="path1645" d="m174.126,108a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1647" d="m178.913,108a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="176.519" cy="108" r="1.19679" id="circle1649"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin24C">
        <path  fill="#bfbfbf" id="path1652" d="m174.126,100.8a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1654" d="m178.913,100.8a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="176.519" cy="100.8" r="1.19679" id="circle1656"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin24D">
        <path  fill="#bfbfbf" id="path1659" d="m174.126,93.6a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1661" d="m178.913,93.6a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="176.519" cy="93.6" r="1.19679" id="circle1663"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin24E">
        <path  fill="#bfbfbf" id="path1666" d="m174.126,86.4a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1668" d="m178.913,86.4a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="176.519" cy="86.4" r="1.19679" id="circle1670"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin24F">
        <path  fill="#bfbfbf" id="path1673" d="m174.126,64.8a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1675" d="m178.913,64.8a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="176.519" cy="64.8" r="1.19679" id="circle1677"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin24G">
        <path  fill="#bfbfbf" id="path1680" d="m174.126,57.6a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1682" d="m178.913,57.6a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="176.519" cy="57.6" r="1.19679" id="circle1684"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin24H">
        <path  fill="#bfbfbf" id="path1687" d="m174.126,50.4a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1689" d="m178.913,50.4a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="176.519" cy="50.4" r="1.19679" id="circle1691"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin24I">
        <path  fill="#bfbfbf" id="path1694" d="m174.126,43.2a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1696" d="m178.913,43.2a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="176.519" cy="43.2" r="1.19679" id="circle1698"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin24J">
        <path  fill="#bfbfbf" id="path1701" d="m174.126,36a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1703" d="m178.913,36a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="176.519" cy="36" r="1.19679" id="circle1705"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin25A">
        <path  fill="#bfbfbf" id="path1708" d="m181.325,115.2a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1710" d="m186.113,115.2a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="183.719" cy="115.2" r="1.19679" id="circle1712"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin25B">
        <path  fill="#bfbfbf" id="path1715" d="m181.325,108a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1717" d="m186.113,108a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="183.719" cy="108" r="1.19679" id="circle1719"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin25C">
        <path  fill="#bfbfbf" id="path1722" d="m181.325,100.8a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1724" d="m186.113,100.8a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="183.719" cy="100.8" r="1.19679" id="circle1726"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin25D">
        <path  fill="#bfbfbf" id="path1729" d="m181.325,93.6a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1731" d="m186.113,93.6a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="183.719" cy="93.6" r="1.19679" id="circle1733"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin25E">
        <path  fill="#bfbfbf" id="path1736" d="m181.325,86.4a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1738" d="m186.113,86.4a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="183.719" cy="86.4" r="1.19679" id="circle1740"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin25F">
        <path  fill="#bfbfbf" id="path1743" d="m181.325,64.8a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1745" d="m186.113,64.8a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="183.719" cy="64.8" r="1.19679" id="circle1747"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin25G">
        <path  fill="#bfbfbf" id="path1750" d="m181.325,57.6a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1752" d="m186.113,57.6a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="183.719" cy="57.6" r="1.19679" id="circle1754"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin25H">
        <path  fill="#bfbfbf" id="path1757" d="m181.325,50.4a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1759" d="m186.113,50.4a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="183.719" cy="50.4" r="1.19679" id="circle1761"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin25I">
        <path  fill="#bfbfbf" id="path1764" d="m181.325,43.2a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1766" d="m186.113,43.2a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="183.719" cy="43.2" r="1.19679" id="circle1768"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin25J">
        <path  fill="#bfbfbf" id="path1771" d="m181.325,36a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1773" d="m186.113,36a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="183.719" cy="36" r="1.19679" id="circle1775"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin26A">
        <path  fill="#bfbfbf" id="path1778" d="m188.525,115.2a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1780" d="m193.313,115.2a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="190.919" cy="115.2" r="1.19679" id="circle1782"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin26B">
        <path  fill="#bfbfbf" id="path1785" d="m188.525,108a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1787" d="m193.313,108a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="190.919" cy="108" r="1.19679" id="circle1789"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin26C">
        <path  fill="#bfbfbf" id="path1792" d="m188.525,100.8a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1794" d="m193.313,100.8a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="190.919" cy="100.8" r="1.19679" id="circle1796"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin26D">
        <path  fill="#bfbfbf" id="path1799" d="m188.525,93.6a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1801" d="m193.313,93.6a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="190.919" cy="93.6" r="1.19679" id="circle1803"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin26E">
        <path  fill="#bfbfbf" id="path1806" d="m188.525,86.4a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1808" d="m193.313,86.4a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="190.919" cy="86.4" r="1.19679" id="circle1810"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin26F">
        <path  fill="#bfbfbf" id="path1813" d="m188.525,64.8a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1815" d="m193.313,64.8a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="190.919" cy="64.8" r="1.19679" id="circle1817"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin26G">
        <path  fill="#bfbfbf" id="path1820" d="m188.525,57.6a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1822" d="m193.313,57.6a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="190.919" cy="57.6" r="1.19679" id="circle1824"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin26H">
        <path  fill="#bfbfbf" id="path1827" d="m188.525,50.4a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1829" d="m193.313,50.4a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="190.919" cy="50.4" r="1.19679" id="circle1831"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin26I">
        <path  fill="#bfbfbf" id="path1834" d="m188.525,43.2a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1836" d="m193.313,43.2a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="190.919" cy="43.2" r="1.19679" id="circle1838"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin26J">
        <path  fill="#bfbfbf" id="path1841" d="m188.525,36a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1843" d="m193.313,36a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="190.919" cy="36" r="1.19679" id="circle1845"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin27A">
        <path  fill="#bfbfbf" id="path1848" d="m195.725,115.2a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1850" d="m200.513,115.2a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="198.119" cy="115.2" r="1.19679" id="circle1852"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin27B">
        <path  fill="#bfbfbf" id="path1855" d="m195.725,108a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1857" d="m200.513,108a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="198.119" cy="108" r="1.19679" id="circle1859"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin27C">
        <path  fill="#bfbfbf" id="path1862" d="m195.725,100.8a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1864" d="m200.513,100.8a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="198.119" cy="100.8" r="1.19679" id="circle1866"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin27D">
        <path  fill="#bfbfbf" id="path1869" d="m195.725,93.6a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1871" d="m200.513,93.6a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="198.119" cy="93.6" r="1.19679" id="circle1873"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin27E">
        <path  fill="#bfbfbf" id="path1876" d="m195.725,86.4a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1878" d="m200.513,86.4a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="198.119" cy="86.4" r="1.19679" id="circle1880"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin27F">
        <path  fill="#bfbfbf" id="path1883" d="m195.725,64.8a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1885" d="m200.513,64.8a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="198.119" cy="64.8" r="1.19679" id="circle1887"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin27G">
        <path  fill="#bfbfbf" id="path1890" d="m195.725,57.6a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1892" d="m200.513,57.6a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="198.119" cy="57.6" r="1.19679" id="circle1894"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin27H">
        <path  fill="#bfbfbf" id="path1897" d="m195.725,50.4a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1899" d="m200.513,50.4a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="198.119" cy="50.4" r="1.19679" id="circle1901"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin27I">
        <path  fill="#bfbfbf" id="path1904" d="m195.725,43.2a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1906" d="m200.513,43.2a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="198.119" cy="43.2" r="1.19679" id="circle1908"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin27J">
        <path  fill="#bfbfbf" id="path1911" d="m195.725,36a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1913" d="m200.513,36a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="198.119" cy="36" r="1.19679" id="circle1915"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin28A">
        <path  fill="#bfbfbf" id="path1918" d="m202.925,115.2a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1920" d="m207.713,115.2a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="205.319" cy="115.2" r="1.19679" id="circle1922"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin28B">
        <path  fill="#bfbfbf" id="path1925" d="m202.925,108a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1927" d="m207.713,108a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="205.319" cy="108" r="1.19679" id="circle1929"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin28C">
        <path  fill="#bfbfbf" id="path1932" d="m202.925,100.8a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1934" d="m207.713,100.8a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="205.319" cy="100.8" r="1.19679" id="circle1936"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin28D">
        <path  fill="#bfbfbf" id="path1939" d="m202.925,93.6a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1941" d="m207.713,93.6a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="205.319" cy="93.6" r="1.19679" id="circle1943"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin28E">
        <path  fill="#bfbfbf" id="path1946" d="m202.925,86.4a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1948" d="m207.713,86.4a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="205.319" cy="86.4" r="1.19679" id="circle1950"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin28F">
        <path  fill="#bfbfbf" id="path1953" d="m202.925,64.8a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1955" d="m207.713,64.8a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="205.319" cy="64.8" r="1.19679" id="circle1957"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin28G">
        <path  fill="#bfbfbf" id="path1960" d="m202.925,57.6a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1962" d="m207.713,57.6a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="205.319" cy="57.6" r="1.19679" id="circle1964"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin28H">
        <path  fill="#bfbfbf" id="path1967" d="m202.925,50.4a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1969" d="m207.713,50.4a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="205.319" cy="50.4" r="1.19679" id="circle1971"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin28I">
        <path  fill="#bfbfbf" id="path1974" d="m202.925,43.2a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1976" d="m207.713,43.2a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="205.319" cy="43.2" r="1.19679" id="circle1978"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin28J">
        <path  fill="#bfbfbf" id="path1981" d="m202.925,36a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1983" d="m207.713,36a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="205.319" cy="36" r="1.19679" id="circle1985"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin29A">
        <path  fill="#bfbfbf" id="path1988" d="m210.125,115.2a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1990" d="m214.913,115.2a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="212.519" cy="115.2" r="1.19679" id="circle1992"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin29B">
        <path  fill="#bfbfbf" id="path1995" d="m210.125,108a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path1997" d="m214.913,108a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="212.519" cy="108" r="1.19679" id="circle1999"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin29C">
        <path  fill="#bfbfbf" id="path2002" d="m210.125,100.8a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path2004" d="m214.913,100.8a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="212.519" cy="100.8" r="1.19679" id="circle2006"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin29D">
        <path  fill="#bfbfbf" id="path2009" d="m210.125,93.6a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path2011" d="m214.913,93.6a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="212.519" cy="93.6" r="1.19679" id="circle2013"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin29E">
        <path  fill="#bfbfbf" id="path2016" d="m210.125,86.4a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path2018" d="m214.913,86.4a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="212.519" cy="86.4" r="1.19679" id="circle2020"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin29F">
        <path  fill="#bfbfbf" id="path2023" d="m210.125,64.8a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path2025" d="m214.913,64.8a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="212.519" cy="64.8" r="1.19679" id="circle2027"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin29G">
        <path  fill="#bfbfbf" id="path2030" d="m210.125,57.6a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path2032" d="m214.913,57.6a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="212.519" cy="57.6" r="1.19679" id="circle2034"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin29H">
        <path  fill="#bfbfbf" id="path2037" d="m210.125,50.4a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path2039" d="m214.913,50.4a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="212.519" cy="50.4" r="1.19679" id="circle2041"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin29I">
        <path  fill="#bfbfbf" id="path2044" d="m210.125,43.2a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path2046" d="m214.913,43.2a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="212.519" cy="43.2" r="1.19679" id="circle2048"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin29J">
        <path  fill="#bfbfbf" id="path2051" d="m210.125,36a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path2053" d="m214.913,36a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="212.519" cy="36" r="1.19679" id="circle2055"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin30A">
        <path  fill="#bfbfbf" id="path2058" d="m217.325,115.2a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path2060" d="m222.112,115.2a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="219.719" cy="115.2" r="1.19679" id="circle2062"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin30B">
        <path  fill="#bfbfbf" id="path2065" d="m217.325,108a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path2067" d="m222.112,108a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="219.719" cy="108" r="1.19679" id="circle2069"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin30C">
        <path  fill="#bfbfbf" id="path2072" d="m217.325,100.8a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path2074" d="m222.112,100.8a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="219.719" cy="100.8" r="1.19679" id="circle2076"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin30D">
        <path  fill="#bfbfbf" id="path2079" d="m217.325,93.6a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path2081" d="m222.112,93.6a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="219.719" cy="93.6" r="1.19679" id="circle2083"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin30E">
        <path  fill="#bfbfbf" id="path2086" d="m217.325,86.4a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path2088" d="m222.112,86.4a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="219.719" cy="86.4" r="1.19679" id="circle2090"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin30F">
        <path  fill="#bfbfbf" id="path2093" d="m217.325,64.8a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path2095" d="m222.112,64.8a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="219.719" cy="64.8" r="1.19679" id="circle2097"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin30G">
        <path  fill="#bfbfbf" id="path2100" d="m217.325,57.6a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path2102" d="m222.112,57.6a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="219.719" cy="57.6" r="1.19679" id="circle2104"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin30H">
        <path  fill="#bfbfbf" id="path2107" d="m217.325,50.4a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path2109" d="m222.112,50.4a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="219.719" cy="50.4" r="1.19679" id="circle2111"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin30I">
        <path  fill="#bfbfbf" id="path2114" d="m217.325,43.2a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path2116" d="m222.112,43.2a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="219.719" cy="43.2" r="1.19679" id="circle2118"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -0.199995, -0.000383215)">
       <g  id="pin30J">
        <path  fill="#bfbfbf" id="path2121" d="m217.325,36a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path2123" d="m222.112,36a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="219.719" cy="36" r="1.19679" id="circle2125"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -11.4, -0.000383215)">
       <g  id="pin3W">
        <path  fill="#bfbfbf" id="path4438" d="m22.4063,144a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path4440" d="m27.1935,144a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="24.7999" cy="144" r="1.19679" id="circle4442"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -11.4, -0.000383215)">
       <g  id="pin3X">
        <path  fill="#bfbfbf" id="path4445" d="m22.4063,136.8a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path4447" d="m27.1935,136.8a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="24.7999" cy="136.8" r="1.19679" id="circle4449"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -11.4, -0.000383215)">
       <g  id="pin3Y">
        <path  fill="#bfbfbf" id="path4452" d="m22.4063,14.4a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path4454" d="m27.1935,14.4a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="24.7999" cy="14.4" r="1.19679" id="circle4456"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -11.4, -0.000383215)">
       <g  id="pin3Z">
        <path  fill="#bfbfbf" id="path4459" d="m22.4063,7.2a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path4461" d="M27.1935,7.2A2.39359,2.3936,0,1,1,22.4063,7.2"/>
        <circle  fill="#383838" cx="24.7999" cy="7.2" r="1.19679" id="circle4463"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -11.4, -0.000383215)">
       <g  id="pin4W">
        <path  fill="#bfbfbf" id="path4466" d="m29.6062,144a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path4468" d="m34.3934,144a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="31.9998" cy="144" r="1.19679" id="circle4470"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -11.4, -0.000383215)">
       <g  id="pin4X">
        <path  fill="#bfbfbf" id="path4473" d="m29.6062,136.8a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path4475" d="m34.3934,136.8a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="31.9998" cy="136.8" r="1.19679" id="circle4477"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -11.4, -0.000383215)">
       <g  id="pin4Y">
        <path  fill="#bfbfbf" id="path4480" d="m29.6062,14.4a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path4482" d="m34.3934,14.4a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="31.9998" cy="14.4" r="1.19679" id="circle4484"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -11.4, -0.000383215)">
       <g  id="pin4Z">
        <path  fill="#bfbfbf" id="path4487" d="m29.6062,7.2a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path4489" d="M34.3934,7.2A2.39359,2.3936,0,1,1,29.6062,7.2"/>
        <circle  fill="#383838" cx="31.9998" cy="7.2" r="1.19679" id="circle4491"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -11.4, -0.000383215)">
       <g  id="pin5W">
        <path  fill="#bfbfbf" id="path4494" d="m36.8062,144a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path4496" d="m41.5934,144a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="39.1998" cy="144" r="1.19679" id="circle4498"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -11.4, -0.000383215)">
       <g  id="pin5X">
        <path  fill="#bfbfbf" id="path4501" d="m36.8062,136.8a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path4503" d="m41.5934,136.8a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="39.1998" cy="136.8" r="1.19679" id="circle4505"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -11.4, -0.000383215)">
       <g  id="pin5Y">
        <path  fill="#bfbfbf" id="path4508" d="m36.8062,14.4a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path4510" d="m41.5934,14.4a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="39.1998" cy="14.4" r="1.19679" id="circle4512"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -11.4, -0.000383215)">
       <g  id="pin5Z">
        <path  fill="#bfbfbf" id="path4515" d="m36.8062,7.2a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path4517" d="M41.5934,7.2A2.39359,2.3936,0,1,1,36.8062,7.2"/>
        <circle  fill="#383838" cx="39.1998" cy="7.2" r="1.19679" id="circle4519"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -11.4, -0.000383215)">
       <g  id="pin6W">
        <path  fill="#bfbfbf" id="path4522" d="m44.0062,144a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path4524" d="m48.7934,144a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="46.3998" cy="144" r="1.19679" id="circle4526"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -11.4, -0.000383215)">
       <g  id="pin6X">
        <path  fill="#bfbfbf" id="path4529" d="m44.0062,136.8a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path4531" d="m48.7934,136.8a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="46.3998" cy="136.8" r="1.19679" id="circle4533"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -11.4, -0.000383215)">
       <g  id="pin6Y">
        <path  fill="#bfbfbf" id="path4536" d="m44.0062,14.4a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path4538" d="m48.7934,14.4a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="46.3998" cy="14.4" r="1.19679" id="circle4540"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -11.4, -0.000383215)">
       <g  id="pin6Z">
        <path  fill="#bfbfbf" id="path4543" d="m44.0062,7.2a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path4545" d="M48.7934,7.2A2.39359,2.3936,0,1,1,44.0062,7.2"/>
        <circle  fill="#383838" cx="46.3998" cy="7.2" r="1.19679" id="circle4547"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -11.4, -0.000383215)">
       <g  id="pin7W">
        <path  fill="#bfbfbf" id="path4550" d="m51.2061,144a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path4552" d="m55.9933,144a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="53.5997" cy="144" r="1.19679" id="circle4554"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -11.4, -0.000383215)">
       <g  id="pin7X">
        <path  fill="#bfbfbf" id="path4557" d="m51.2061,136.8a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path4559" d="m55.9933,136.8a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="53.5997" cy="136.8" r="1.19679" id="circle4561"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -11.4, -0.000383215)">
       <g  id="pin7Y">
        <path  fill="#bfbfbf" id="path4564" d="m51.2061,14.4a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path4566" d="m55.9933,14.4a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="53.5997" cy="14.4" r="1.19679" id="circle4568"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -11.4, -0.000383215)">
       <g  id="pin7Z">
        <path  fill="#bfbfbf" id="path4571" d="m51.2061,7.2a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path4573" d="M55.9933,7.2A2.39359,2.3936,0,1,1,51.2061,7.2"/>
        <circle  fill="#383838" cx="53.5997" cy="7.2" r="1.19679" id="circle4575"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -11.4, -0.000383215)">
       <g  id="pin9W">
        <path  fill="#bfbfbf" id="path4578" d="m65.6061,144a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path4580" d="m70.3932,144a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="67.9997" cy="144" r="1.19679" id="circle4582"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -11.4, -0.000383215)">
       <g  id="pin9X">
        <path  fill="#bfbfbf" id="path4585" d="m65.6061,136.8a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path4587" d="m70.3932,136.8a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="67.9997" cy="136.8" r="1.19679" id="circle4589"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -11.4, -0.000383215)">
       <g  id="pin9Y">
        <path  fill="#bfbfbf" id="path4592" d="m65.6061,14.4a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path4594" d="m70.3932,14.4a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="67.9997" cy="14.4" r="1.19679" id="circle4596"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -11.4, -0.000383215)">
       <g  id="pin9Z">
        <path  fill="#bfbfbf" id="path4599" d="m65.6061,7.2a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path4601" d="M70.3932,7.2A2.39359,2.3936,0,1,1,65.6061,7.2"/>
        <circle  fill="#383838" cx="67.9997" cy="7.2" r="1.19679" id="circle4603"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -11.4, -0.000383215)">
       <g  id="pin10W">
        <path  fill="#bfbfbf" id="path4606" d="m72.806,144a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path4608" d="m77.5932,144a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="75.1996" cy="144" r="1.19679" id="circle4610"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -11.4, -0.000383215)">
       <g  id="pin10X">
        <path  fill="#bfbfbf" id="path4613" d="m72.806,136.8a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path4615" d="m77.5932,136.8a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="75.1996" cy="136.8" r="1.19679" id="circle4617"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -11.4, -0.000383215)">
       <g  id="pin10Y">
        <path  fill="#bfbfbf" id="path4620" d="m72.806,14.4a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path4622" d="m77.5932,14.4a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="75.1996" cy="14.4" r="1.19679" id="circle4624"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -11.4, -0.000383215)">
       <g  id="pin10Z">
        <path  fill="#bfbfbf" id="path4627" d="m72.806,7.2a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path4629" d="M77.5932,7.2A2.39359,2.3936,0,1,1,72.806,7.2"/>
        <circle  fill="#383838" cx="75.1996" cy="7.2" r="1.19679" id="circle4631"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -11.4, -0.000383215)">
       <g  id="pin11W">
        <path  fill="#bfbfbf" id="path4634" d="m80.006,144a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path4636" d="m84.7932,144a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="82.3996" cy="144" r="1.19679" id="circle4638"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -11.4, -0.000383215)">
       <g  id="pin11X">
        <path  fill="#bfbfbf" id="path4641" d="m80.006,136.8a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path4643" d="m84.7932,136.8a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="82.3996" cy="136.8" r="1.19679" id="circle4645"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -11.4, -0.000383215)">
       <g  id="pin11Y">
        <path  fill="#bfbfbf" id="path4648" d="m80.006,14.4a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path4650" d="m84.7932,14.4a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="82.3996" cy="14.4" r="1.19679" id="circle4652"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -11.4, -0.000383215)">
       <g  id="pin11Z">
        <path  fill="#bfbfbf" id="path4655" d="m80.006,7.2a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path4657" d="m84.7932,7.2a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="82.3996" cy="7.2" r="1.19679" id="circle4659"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -11.4, -0.000383215)">
       <g  id="pin12W">
        <path  fill="#bfbfbf" id="path4662" d="m87.206,144a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path4664" d="m91.9931,144a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="89.5995" cy="144" r="1.19679" id="circle4666"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -11.4, -0.000383215)">
       <g  id="pin12X">
        <path  fill="#bfbfbf" id="path4669" d="m87.206,136.8a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path4671" d="m91.9931,136.8a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="89.5995" cy="136.8" r="1.19679" id="circle4673"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -11.4, -0.000383215)">
       <g  id="pin12Y">
        <path  fill="#bfbfbf" id="path4676" d="m87.206,14.4a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path4678" d="m91.9931,14.4a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="89.5995" cy="14.4" r="1.19679" id="circle4680"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -11.4, -0.000383215)">
       <g  id="pin12Z">
        <path  fill="#bfbfbf" id="path4683" d="m87.206,7.2a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path4685" d="m91.9931,7.2a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="89.5995" cy="7.2" r="1.19679" id="circle4687"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -11.4, -0.000383215)">
       <g  id="pin13W">
        <path  fill="#bfbfbf" id="path4690" d="m94.4059,144a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path4692" d="m99.1931,144a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="96.7995" cy="144" r="1.19679" id="circle4694"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -11.4, -0.000383215)">
       <g  id="pin13X">
        <path  fill="#bfbfbf" id="path4697" d="m94.4059,136.8a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path4699" d="m99.1931,136.8a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="96.7995" cy="136.8" r="1.19679" id="circle4701"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -11.4, -0.000383215)">
       <g  id="pin13Y">
        <path  fill="#bfbfbf" id="path4704" d="m94.4059,14.4a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path4706" d="m99.1931,14.4a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="96.7995" cy="14.4" r="1.19679" id="circle4708"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -11.4, -0.000383215)">
       <g  id="pin13Z">
        <path  fill="#bfbfbf" id="path4711" d="m94.4059,7.2a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path4713" d="m99.1931,7.2a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="96.7995" cy="7.2" r="1.19679" id="circle4715"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -11.4, -0.000383215)">
       <g  id="pin15W">
        <path  fill="#bfbfbf" id="path4718" d="m108.806,144a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path4720" d="m113.593,144a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="111.199" cy="144" r="1.19679" id="circle4722"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -11.4, -0.000383215)">
       <g  id="pin15X">
        <path  fill="#bfbfbf" id="path4725" d="m108.806,136.8a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path4727" d="m113.593,136.8a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="111.199" cy="136.8" r="1.19679" id="circle4729"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -11.4, -0.000383215)">
       <g  id="pin15Y">
        <path  fill="#bfbfbf" id="path4732" d="m108.806,14.4a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path4734" d="m113.593,14.4a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="111.199" cy="14.4" r="1.19679" id="circle4736"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -11.4, -0.000383215)">
       <g  id="pin15Z">
        <path  fill="#bfbfbf" id="path4739" d="m108.806,7.2a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path4741" d="m113.593,7.2a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="111.199" cy="7.2" r="1.19679" id="circle4743"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -11.4, -0.000383215)">
       <g  id="pin16W">
        <path  fill="#bfbfbf" id="path4746" d="m116.006,144a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path4748" d="m120.793,144a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="118.399" cy="144" r="1.19679" id="circle4750"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -11.4, -0.000383215)">
       <g  id="pin16X">
        <path  fill="#bfbfbf" id="path4753" d="m116.006,136.8a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path4755" d="m120.793,136.8a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="118.399" cy="136.8" r="1.19679" id="circle4757"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -11.4, -0.000383215)">
       <g  id="pin16Y">
        <path  fill="#bfbfbf" id="path4760" d="m116.006,14.4a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path4762" d="m120.793,14.4a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="118.399" cy="14.4" r="1.19679" id="circle4764"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -11.4, -0.000383215)">
       <g  id="pin16Z">
        <path  fill="#bfbfbf" id="path4767" d="m116.006,7.2a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path4769" d="m120.793,7.2a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="118.399" cy="7.2" r="1.19679" id="circle4771"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -11.4, -0.000383215)">
       <g  id="pin17W">
        <path  fill="#bfbfbf" id="path4774" d="m123.206,144a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path4776" d="m127.993,144a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="125.599" cy="144" r="1.19679" id="circle4778"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -11.4, -0.000383215)">
       <g  id="pin17X">
        <path  fill="#bfbfbf" id="path4781" d="m123.206,136.8a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path4783" d="m127.993,136.8a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="125.599" cy="136.8" r="1.19679" id="circle4785"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -11.4, -0.000383215)">
       <g  id="pin17Y">
        <path  fill="#bfbfbf" id="path4788" d="m123.206,14.4a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path4790" d="m127.993,14.4a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="125.599" cy="14.4" r="1.19679" id="circle4792"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -11.4, -0.000383215)">
       <g  id="pin17Z">
        <path  fill="#bfbfbf" id="path4795" d="m123.206,7.2a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path4797" d="m127.993,7.2a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="125.599" cy="7.2" r="1.19679" id="circle4799"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -11.4, -0.000383215)">
       <g  id="pin18W">
        <path  fill="#bfbfbf" id="path4802" d="m130.406,144a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path4804" d="m135.193,144a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="132.799" cy="144" r="1.19679" id="circle4806"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -11.4, -0.000383215)">
       <g  id="pin18X">
        <path  fill="#bfbfbf" id="path4809" d="m130.406,136.8a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path4811" d="m135.193,136.8a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="132.799" cy="136.8" r="1.19679" id="circle4813"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -11.4, -0.000383215)">
       <g  id="pin18Y">
        <path  fill="#bfbfbf" id="path4816" d="m130.406,14.4a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path4818" d="m135.193,14.4a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="132.799" cy="14.4" r="1.19679" id="circle4820"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -11.4, -0.000383215)">
       <g  id="pin18Z">
        <path  fill="#bfbfbf" id="path4823" d="m130.406,7.2a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path4825" d="m135.193,7.2a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="132.799" cy="7.2" r="1.19679" id="circle4827"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -11.4, -0.000383215)">
       <g  id="pin19W">
        <path  fill="#bfbfbf" id="path4830" d="m137.606,144a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path4832" d="m142.393,144a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="139.999" cy="144" r="1.19679" id="circle4834"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -11.4, -0.000383215)">
       <g  id="pin19X">
        <path  fill="#bfbfbf" id="path4837" d="m137.606,136.8a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path4839" d="m142.393,136.8a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="139.999" cy="136.8" r="1.19679" id="circle4841"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -11.4, -0.000383215)">
       <g  id="pin19Y">
        <path  fill="#bfbfbf" id="path4844" d="m137.606,14.4a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path4846" d="m142.393,14.4a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="139.999" cy="14.4" r="1.19679" id="circle4848"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -11.4, -0.000383215)">
       <g  id="pin19Z">
        <path  fill="#bfbfbf" id="path4851" d="m137.606,7.2a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path4853" d="m142.393,7.2a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="139.999" cy="7.2" r="1.19679" id="circle4855"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -11.4, -0.000383215)">
       <g  id="pin21W">
        <path  fill="#bfbfbf" id="path4858" d="m152.006,144a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path4860" d="m156.793,144a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="154.399" cy="144" r="1.19679" id="circle4862"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -11.4, -0.000383215)">
       <g  id="pin21X">
        <path  fill="#bfbfbf" id="path4865" d="m152.006,136.8a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path4867" d="m156.793,136.8a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="154.399" cy="136.8" r="1.19679" id="circle4869"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -11.4, -0.000383215)">
       <g  id="pin21Y">
        <path  fill="#bfbfbf" id="path4872" d="m152.006,14.4a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path4874" d="m156.793,14.4a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="154.399" cy="14.4" r="1.19679" id="circle4876"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -11.4, -0.000383215)">
       <g  id="pin21Z">
        <path  fill="#bfbfbf" id="path4879" d="m152.006,7.2a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path4881" d="m156.793,7.2a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="154.399" cy="7.2" r="1.19679" id="circle4883"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -11.4, -0.000383215)">
       <g  id="pin22W">
        <path  fill="#bfbfbf" id="path4886" d="m159.206,144a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path4888" d="m163.993,144a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="161.599" cy="144" r="1.19679" id="circle4890"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -11.4, -0.000383215)">
       <g  id="pin22X">
        <path  fill="#bfbfbf" id="path4893" d="m159.206,136.8a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path4895" d="m163.993,136.8a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="161.599" cy="136.8" r="1.19679" id="circle4897"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -11.4, -0.000383215)">
       <g  id="pin22Y">
        <path  fill="#bfbfbf" id="path4900" d="m159.206,14.4a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path4902" d="m163.993,14.4a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="161.599" cy="14.4" r="1.19679" id="circle4904"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -11.4, -0.000383215)">
       <g  id="pin22Z">
        <path  fill="#bfbfbf" id="path4907" d="m159.206,7.2a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path4909" d="m163.993,7.2a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="161.599" cy="7.2" r="1.19679" id="circle4911"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -11.4, -0.000383215)">
       <g  id="pin23W">
        <path  fill="#bfbfbf" id="path4914" d="m166.406,144a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path4916" d="m171.193,144a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="168.799" cy="144" r="1.19679" id="circle4918"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -11.4, -0.000383215)">
       <g  id="pin23X">
        <path  fill="#bfbfbf" id="path4921" d="m166.406,136.8a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path4923" d="m171.193,136.8a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="168.799" cy="136.8" r="1.19679" id="circle4925"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -11.4, -0.000383215)">
       <g  id="pin23Y">
        <path  fill="#bfbfbf" id="path4928" d="m166.406,14.4a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path4930" d="m171.193,14.4a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="168.799" cy="14.4" r="1.19679" id="circle4932"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -11.4, -0.000383215)">
       <g  id="pin23Z">
        <path  fill="#bfbfbf" id="path4935" d="m166.406,7.2a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path4937" d="m171.193,7.2a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="168.799" cy="7.2" r="1.19679" id="circle4939"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -11.4, -0.000383215)">
       <g  id="pin24W">
        <path  fill="#bfbfbf" id="path4942" d="m173.606,144a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path4944" d="m178.393,144a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="175.999" cy="144" r="1.19679" id="circle4946"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -11.4, -0.000383215)">
       <g  id="pin24X">
        <path  fill="#bfbfbf" id="path4949" d="m173.606,136.8a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path4951" d="m178.393,136.8a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="175.999" cy="136.8" r="1.19679" id="circle4953"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -11.4, -0.000383215)">
       <g  id="pin24Y">
        <path  fill="#bfbfbf" id="path4956" d="m173.606,14.4a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path4958" d="m178.393,14.4a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="175.999" cy="14.4" r="1.19679" id="circle4960"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -11.4, -0.000383215)">
       <g  id="pin24Z">
        <path  fill="#bfbfbf" id="path4963" d="m173.606,7.2a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path4965" d="m178.393,7.2a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="175.999" cy="7.2" r="1.19679" id="circle4967"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -11.4, -0.000383215)">
       <g  id="pin25W">
        <path  fill="#bfbfbf" id="path4970" d="m180.805,144a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path4972" d="m185.593,144a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="183.199" cy="144" r="1.19679" id="circle4974"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -11.4, -0.000383215)">
       <g  id="pin25X">
        <path  fill="#bfbfbf" id="path4977" d="m180.805,136.8a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path4979" d="m185.593,136.8a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="183.199" cy="136.8" r="1.19679" id="circle4981"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -11.4, -0.000383215)">
       <g  id="pin25Y">
        <path  fill="#bfbfbf" id="path4984" d="m180.805,14.4a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path4986" d="m185.593,14.4a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="183.199" cy="14.4" r="1.19679" id="circle4988"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -11.4, -0.000383215)">
       <g  id="pin25Z">
        <path  fill="#bfbfbf" id="path4991" d="m180.805,7.2a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path4993" d="m185.593,7.2a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="183.199" cy="7.2" r="1.19679" id="circle4995"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -11.4, -0.000383215)">
       <g  id="pin27W">
        <path  fill="#bfbfbf" id="path4998" d="m195.205,144a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path5000" d="m199.993,144a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="197.599" cy="144" r="1.19679" id="circle5002"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -11.4, -0.000383215)">
       <g  id="pin27X">
        <path  fill="#bfbfbf" id="path5005" d="m195.205,136.8a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path5007" d="m199.993,136.8a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="197.599" cy="136.8" r="1.19679" id="circle5009"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -11.4, -0.000383215)">
       <g  id="pin27Y">
        <path  fill="#bfbfbf" id="path5012" d="m195.205,14.4a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path5014" d="m199.993,14.4a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="197.599" cy="14.4" r="1.19679" id="circle5016"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -11.4, -0.000383215)">
       <g  id="pin27Z">
        <path  fill="#bfbfbf" id="path5019" d="m195.205,7.2a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path5021" d="m199.993,7.2a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="197.599" cy="7.2" r="1.19679" id="circle5023"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -11.4, -0.000383215)">
       <g  id="pin28W">
        <path  fill="#bfbfbf" id="path5026" d="m202.405,144a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path5028" d="m207.193,144a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="204.799" cy="144" r="1.19679" id="circle5030"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -11.4, -0.000383215)">
       <g  id="pin28X">
        <path  fill="#bfbfbf" id="path5033" d="m202.405,136.8a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path5035" d="m207.193,136.8a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="204.799" cy="136.8" r="1.19679" id="circle5037"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -11.4, -0.000383215)">
       <g  id="pin28Y">
        <path  fill="#bfbfbf" id="path5040" d="m202.405,14.4a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path5042" d="m207.193,14.4a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="204.799" cy="14.4" r="1.19679" id="circle5044"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -11.4, -0.000383215)">
       <g  id="pin28Z">
        <path  fill="#bfbfbf" id="path5047" d="m202.405,7.2a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path5049" d="m207.193,7.2a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="204.799" cy="7.2" r="1.19679" id="circle5051"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -11.4, -0.000383215)">
       <g  id="pin29W">
        <path  fill="#bfbfbf" id="path5054" d="m209.605,144a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path5056" d="m214.393,144a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="211.999" cy="144" r="1.19679" id="circle5058"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -11.4, -0.000383215)">
       <g  id="pin29X">
        <path  fill="#bfbfbf" id="path5061" d="m209.605,136.8a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path5063" d="m214.393,136.8a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="211.999" cy="136.8" r="1.19679" id="circle5065"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -11.4, -0.000383215)">
       <g  id="pin29Y">
        <path  fill="#bfbfbf" id="path5068" d="m209.605,14.4a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path5070" d="m214.393,14.4a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="211.999" cy="14.4" r="1.19679" id="circle5072"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -11.4, -0.000383215)">
       <g  id="pin29Z">
        <path  fill="#bfbfbf" id="path5075" d="m209.605,7.2a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path5077" d="m214.393,7.2a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="211.999" cy="7.2" r="1.19679" id="circle5079"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -11.4, -0.000383215)">
       <g  id="pin30W">
        <path  fill="#bfbfbf" id="path5082" d="m216.805,144a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path5084" d="m221.592,144a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="219.199" cy="144" r="1.19679" id="circle5086"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -11.4, -0.000383215)">
       <g  id="pin30X">
        <path  fill="#bfbfbf" id="path5089" d="m216.805,136.8a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path5091" d="m221.592,136.8a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="219.199" cy="136.8" r="1.19679" id="circle5093"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -11.4, -0.000383215)">
       <g  id="pin30Y">
        <path  fill="#bfbfbf" id="path5096" d="m216.805,14.4a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path5098" d="m221.592,14.4a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="219.199" cy="14.4" r="1.19679" id="circle5100"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -11.4, -0.000383215)">
       <g  id="pin30Z">
        <path  fill="#bfbfbf" id="path5103" d="m216.805,7.2a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path5105" d="m221.592,7.2a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="219.199" cy="7.2" r="1.19679" id="circle5107"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -11.4, -0.000383215)">
       <g  id="pin31W">
        <path  fill="#bfbfbf" id="path5110" d="m224.005,144a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path5112" d="m228.792,144a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="226.399" cy="144" r="1.19679" id="circle5114"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -11.4, -0.000383215)">
       <g  id="pin31X">
        <path  fill="#bfbfbf" id="path5117" d="m224.005,136.8a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path5119" d="m228.792,136.8a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="226.399" cy="136.8" r="1.19679" id="circle5121"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -11.4, -0.000383215)">
       <g  id="pin31Y">
        <path  fill="#bfbfbf" id="path5124" d="m224.005,14.4a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path5126" d="m228.792,14.4a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="226.399" cy="14.4" r="1.19679" id="circle5128"/>
       </g>
      </g>
      <g transform="matrix(1, 0, 0, 1, -11.4, -0.000383215)">
       <g  id="pin31Z">
        <path  fill="#bfbfbf" id="path5131" d="m224.005,7.2a2.39359,2.3936,0,0,1,4.78718,0"/>
        <path  fill="#e6e6e6" id="path5133" d="m228.792,7.2a2.39359,2.3936,0,1,1,-4.78718,0"/>
        <circle  fill="#383838" cx="226.399" cy="7.2" r="1.19679" id="circle5135"/>
       </g>
      </g>
      <g transform="matrix(0,-1,1,0,0,0)">
       <text  x="-30.3995" y="12.6" fill="#b3b0b0" style="font-family:Droid Sans" id="text5838" font-size="4.60358">1</text>
      </g>
      <g transform="matrix(0,-1,1,0,0,0)">
       <text  x="-126.399" y="12.6" fill="#b3b0b0" style="font-family:Droid Sans" id="text5840" font-size="4.60358">1</text>
      </g>
      <g transform="matrix(0,-1,1,0,0,0)">
       <text  x="-30.3995" y="41.4" fill="#b3b0b0" style="font-family:Droid Sans" id="text5842" font-size="4.60358">5</text>
      </g>
      <g transform="matrix(0,-1,1,0,0,0)">
       <text  x="-126.399" y="41.4" fill="#b3b0b0" style="font-family:Droid Sans" id="text5844" font-size="4.60358">5</text>
      </g>
      <g transform="matrix(0,-1,1,0,0,0)">
       <text  x="-30.3995" y="77.4" fill="#b3b0b0" style="font-family:Droid Sans" id="text5846" font-size="4.60358">10</text>
      </g>
      <g transform="matrix(0,-1,1,0,0,0)">
       <text  x="-126.399" y="77.4" fill="#b3b0b0" style="font-family:Droid Sans" id="text5848" font-size="4.60358">10</text>
      </g>
      <g transform="matrix(0,-1,1,0,0,0)">
       <text  x="-30.3995" y="113.4" fill="#b3b0b0" style="font-family:Droid Sans" id="text5850" font-size="4.60358">15</text>
      </g>
      <g transform="matrix(0,-1,1,0,0,0)">
       <text  x="-126.399" y="113.4" fill="#b3b0b0" style="font-family:Droid Sans" id="text5852" font-size="4.60358">15</text>
      </g>
      <g transform="matrix(0,-1,1,0,0,0)">
       <text  x="-30.3995" y="149.4" fill="#b3b0b0" style="font-family:Droid Sans" id="text5854" font-size="4.60358">20</text>
      </g>
      <g transform="matrix(0,-1,1,0,0,0)">
       <text  x="-126.399" y="149.4" fill="#b3b0b0" style="font-family:Droid Sans" id="text5856" font-size="4.60358">20</text>
      </g>
      <g transform="matrix(0,-1,1,0,0,0)">
       <text  x="-30.3995" y="185.4" fill="#b3b0b0" style="font-family:Droid Sans" id="text5858" font-size="4.60358">25</text>
      </g>
      <g transform="matrix(0,-1,1,0,0,0)">
       <text  x="-126.399" y="185.4" fill="#b3b0b0" style="font-family:Droid Sans" id="text5860" font-size="4.60358">25</text>
      </g>
      <g transform="matrix(0,-1,1,0,0,0)">
       <text  x="-30.3995" y="221.4" fill="#b3b0b0" style="font-family:Droid Sans" id="text5862" font-size="4.60358">30</text>
      </g>
      <g transform="matrix(0,-1,1,0,0,0)">
       <text  x="-126.399" y="221.4" fill="#b3b0b0" style="font-family:Droid Sans" id="text5864" font-size="4.60358">30</text>
      </g>
      <g transform="matrix(0,-1,1,0,0,0)">
       <text  x="-116.799" y="5.4" fill="#b3b0b0" style="font-family:Droid Sans" id="text5890" font-size="4.60358">A</text>
      </g>
      <g transform="matrix(0,-1,1,0,0,0)">
       <text  x="-116.799" y="228.6" fill="#b3b0b0" style="font-family:Droid Sans" id="text5892" font-size="4.60358">A</text>
      </g>
      <g transform="matrix(0,-1,1,0,0,0)">
       <text  x="-109.599" y="5.4" fill="#b3b0b0" style="font-family:Droid Sans" id="text5894" font-size="4.60358">B</text>
      </g>
      <g transform="matrix(0,-1,1,0,0,0)">
       <text  x="-109.599" y="228.6" fill="#b3b0b0" style="font-family:Droid Sans" id="text5896" font-size="4.60358">B</text>
      </g>
      <g transform="matrix(0,-1,1,0,0,0)">
       <text  x="-102.399" y="5.4" fill="#b3b0b0" style="font-family:Droid Sans" id="text5898" font-size="4.60358">C</text>
      </g>
      <g transform="matrix(0,-1,1,0,0,0)">
       <text  x="-102.399" y="228.6" fill="#b3b0b0" style="font-family:Droid Sans" id="text5900" font-size="4.60358">C</text>
      </g>
      <g transform="matrix(0,-1,1,0,0,0)">
       <text  x="-95.1991" y="5.4" fill="#b3b0b0" style="font-family:Droid Sans" id="text5902" font-size="4.60358">D</text>
      </g>
      <g transform="matrix(0,-1,1,0,0,0)">
       <text  x="-95.1991" y="228.6" fill="#b3b0b0" style="font-family:Droid Sans" id="text5904" font-size="4.60358">D</text>
      </g>
      <g transform="matrix(0,-1,1,0,0,0)">
       <text  x="-87.9992" y="5.4" fill="#b3b0b0" style="font-family:Droid Sans" id="text5906" font-size="4.60358">E</text>
      </g>
      <g transform="matrix(0,-1,1,0,0,0)">
       <text  x="-87.9992" y="228.6" fill="#b3b0b0" style="font-family:Droid Sans" id="text5908" font-size="4.60358">E</text>
      </g>
      <g transform="matrix(0,-1,1,0,0,0)">
       <text  x="-66.3993" y="5.4" fill="#b3b0b0" style="font-family:Droid Sans" id="text5910" font-size="4.60358">F</text>
      </g>
      <g transform="matrix(0,-1,1,0,0,0)">
       <text  x="-66.3993" y="228.6" fill="#b3b0b0" style="font-family:Droid Sans" id="text5912" font-size="4.60358">F</text>
      </g>
      <g transform="matrix(0,-1,1,0,0,0)">
       <text  x="-59.1993" y="5.4" fill="#b3b0b0" style="font-family:Droid Sans" id="text5914" font-size="4.60358">G</text>
      </g>
      <g transform="matrix(0,-1,1,0,0,0)">
       <text  x="-59.1993" y="228.6" fill="#b3b0b0" style="font-family:Droid Sans" id="text5916" font-size="4.60358">G</text>
      </g>
      <g transform="matrix(0,-1,1,0,0,0)">
       <text  x="-51.9994" y="5.4" fill="#b3b0b0" style="font-family:Droid Sans" id="text5918" font-size="4.60358">H</text>
      </g>
      <g transform="matrix(0,-1,1,0,0,0)">
       <text  x="-51.9994" y="228.6" fill="#b3b0b0" style="font-family:Droid Sans" id="text5920" font-size="4.60358">H</text>
      </g>
      <g transform="matrix(0,-1,1,0,0,0)">
       <text  x="-43.9994" y="5.4" fill="#b3b0b0" style="font-family:Droid Sans" id="text5922" font-size="4.60358">I</text>
      </g>
      <g transform="matrix(0,-1,1,0,0,0)">
       <text  x="-43.9994" y="228.6" fill="#b3b0b0" style="font-family:Droid Sans" id="text5924" font-size="4.60358">I</text>
      </g>
      <g transform="matrix(0,-1,1,0,0,0)">
       <text  x="-36.7994" y="5.4" fill="#b3b0b0" style="font-family:Droid Sans" id="text5926" font-size="4.60358">J</text>
      </g>
      <g transform="matrix(0,-1,1,0,0,0)">
       <text  x="-36.7994" y="228.6" fill="#b3b0b0" style="font-family:Droid Sans" id="text5928" font-size="4.60358">J</text>
      </g>
     </g>
    </g>
    </g></g></g><g partID='56210'><g transform='translate(151.2,29.3817)' ><g transform='matrix(0,1,-1,0,0,0)'  ><g  gorn="0.2" id="breadboardbreadboard">
     <g  gorn="0.2.0" id="icon">
      <path  fill="#0F7391" gorn="0.2.0.0" id="_x30_.1.0.0" d="M200.852,0l4.32,4.32l0,32.4l7.199,7.2l0,92.879L205.172,144l0,4.36c0,1.565,-1.271,2.837,-2.834,2.837c-0.002,0,-0.002,0,-0.002,0L20.806,151.197c-1.565,0,-2.834,-1.271,-2.834,-2.834c0,0,0,0,0,-0.003L17.972,2.834C17.972,1.269,19.241,0,20.806,0l0,0L200.852,0M200.635,50.4c-0.004,2.505,2.023,4.539,4.527,4.543c2.506,0.004,4.539,-2.023,4.545,-4.528c0,-0.005,0,-0.01,0,-0.016c0.004,-2.505,-2.023,-4.539,-4.528,-4.543s-4.539,2.022,-4.544,4.527C200.635,50.39,200.635,50.395,200.635,50.4zM200.635,129.6c-0.004,2.505,2.023,4.539,4.527,4.543c2.506,0.004,4.539,-2.021,4.545,-4.527c0,-0.006,0,-0.011,0,-0.016c0.004,-2.505,-2.023,-4.539,-4.528,-4.543c-2.505,-0.006,-4.539,2.021,-4.544,4.527C200.635,129.588,200.635,129.594,200.635,129.6zM56.636,7.2c-0.004,2.504,2.023,4.539,4.528,4.543c2.504,0.004,4.539,-2.022,4.543,-4.527c0,-0.005,0,-0.011,0,-0.016c0.004,-2.505,-2.024,-4.539,-4.529,-4.542c-2.505,-0.003,-4.539,2.024,-4.542,4.529C56.636,7.191,56.636,7.196,56.636,7.2L56.636,7.2zM53.036,144c-0.003,2.504,2.024,4.537,4.529,4.541s4.539,-2.023,4.542,-4.528c0,-0.005,0,-0.009,0,-0.013c0.004,-2.506,-2.024,-4.539,-4.529,-4.543s-4.538,2.021,-4.542,4.525C53.036,143.991,53.036,143.997,53.036,144zM160.767,144c-0.001,0.664,0.536,1.205,1.202,1.207c0.664,0.002,1.205,-0.537,1.207,-1.203c0,-0.002,0,-0.004,0,-0.004c0.002,-0.666,-0.537,-1.207,-1.201,-1.209c-0.666,0,-1.207,0.537,-1.208,1.203C160.767,143.997,160.767,143.999,160.767,144zM167.967,144c-0.002,0.664,0.537,1.205,1.201,1.207c0.666,0.002,1.207,-0.537,1.207,-1.203c0,-0.002,0,-0.004,0,-0.004c0.002,-0.666,-0.535,-1.207,-1.201,-1.209c-0.666,0,-1.207,0.537,-1.207,1.203C167.967,143.997,167.967,143.999,167.967,144zM175.167,144c0,0.664,0.537,1.205,1.203,1.207s1.205,-0.537,1.207,-1.203c0,-0.002,0,-0.004,0,-0.004c0.002,-0.666,-0.537,-1.207,-1.201,-1.209c-0.666,0,-1.207,0.537,-1.209,1.203C175.167,143.997,175.167,143.999,175.167,144zM182.368,144c-0.002,0.664,0.536,1.205,1.201,1.207c0.666,0.002,1.206,-0.537,1.207,-1.203c0,-0.002,0,-0.004,0,-0.004c0.002,-0.666,-0.535,-1.207,-1.201,-1.209c-0.666,0,-1.205,0.537,-1.207,1.203C182.368,143.997,182.368,143.999,182.368,144zM189.567,144c-0.002,0.664,0.537,1.205,1.202,1.207s1.206,-0.537,1.208,-1.203c0,-0.002,0,-0.004,0,-0.004c0.001,-0.666,-0.537,-1.207,-1.203,-1.209c-0.665,0,-1.205,0.537,-1.207,1.203C189.567,143.997,189.567,143.999,189.567,144zM196.767,144c-0.001,0.664,0.536,1.205,1.202,1.207c0.664,0.002,1.205,-0.537,1.207,-1.203c0,-0.002,0,-0.004,0,-0.004c0.002,-0.666,-0.537,-1.207,-1.201,-1.209c-0.666,0,-1.207,0.537,-1.208,1.203C196.767,143.997,196.767,143.999,196.767,144zM196.986,64.8c-0.001,0.744,0.601,1.348,1.345,1.349s1.352,-0.601,1.352,-1.344c0,-0.001,0,-0.003,0,-0.004c0.002,-0.744,-0.604,-1.347,-1.348,-1.348s-1.348,0.601,-1.349,1.344C196.986,64.797,196.986,64.799,196.986,64.8zM204.186,64.8c-0.001,0.744,0.602,1.348,1.344,1.349c0.744,0.001,1.348,-0.601,1.35,-1.344c0,-0.001,0,-0.003,0,-0.004c0,-0.744,-0.602,-1.347,-1.344,-1.348c-0.744,-0.001,-1.349,0.601,-1.35,1.344C204.186,64.797,204.186,64.799,204.186,64.8zM196.986,72c-0.001,0.744,0.601,1.347,1.345,1.349c0.744,0.001,1.352,-0.601,1.352,-1.345c0,-0.001,0,-0.002,0,-0.004c0.002,-0.744,-0.604,-1.347,-1.348,-1.349c-0.744,-0.001,-1.348,0.601,-1.349,1.345C196.986,71.997,196.986,71.999,196.986,72zM204.186,72c-0.001,0.744,0.602,1.347,1.344,1.349c0.744,0.001,1.348,-0.601,1.35,-1.345c0,-0.001,0,-0.002,0,-0.004c0,-0.744,-0.602,-1.347,-1.344,-1.349c-0.744,-0.001,-1.349,0.601,-1.35,1.345C204.186,71.997,204.186,71.999,204.186,72zM196.986,79.2c-0.001,0.744,0.601,1.348,1.345,1.35c0.744,0,1.352,-0.602,1.352,-1.346c0,0,0,-0.002,0,-0.004c0.002,-0.742,-0.604,-1.348,-1.348,-1.348c-0.744,-0.002,-1.348,0.6,-1.349,1.344C196.986,79.198,196.986,79.2,196.986,79.2zM204.186,79.2c-0.001,0.744,0.602,1.348,1.344,1.35c0.744,0,1.348,-0.602,1.35,-1.346c0,0,0,-0.002,0,-0.004c0,-0.742,-0.602,-1.348,-1.344,-1.348c-0.744,-0.002,-1.349,0.6,-1.35,1.344C204.186,79.198,204.186,79.2,204.186,79.2zM75.666,16.56c-0.001,0.744,0.601,1.347,1.344,1.349c0.744,0.001,1.348,-0.601,1.349,-1.345c0,-0.001,0,-0.002,0,-0.004c0.001,-0.744,-0.601,-1.348,-1.344,-1.349c-0.743,-0.001,-1.348,0.601,-1.349,1.345C75.666,16.557,75.666,16.559,75.666,16.56zM75.666,23.76c-0.001,0.743,0.601,1.347,1.344,1.348c0.744,0.001,1.348,-0.601,1.349,-1.344c0,-0.001,0,-0.003,0,-0.004c0.001,-0.744,-0.601,-1.348,-1.344,-1.349c-0.744,-0.001,-1.348,0.601,-1.349,1.344C75.666,23.757,75.666,23.759,75.666,23.76zM68.465,16.56c-0.001,0.744,0.601,1.347,1.344,1.349c0.744,0.001,1.348,-0.601,1.349,-1.345c0,-0.001,0,-0.002,0,-0.004c0.001,-0.744,-0.601,-1.348,-1.345,-1.349c-0.743,-0.001,-1.347,0.601,-1.348,1.345C68.465,16.557,68.465,16.559,68.465,16.56zM68.465,23.76c-0.001,0.743,0.601,1.347,1.344,1.348c0.744,0.001,1.348,-0.601,1.349,-1.344c0,-0.001,0,-0.003,0,-0.004c0.001,-0.744,-0.601,-1.348,-1.345,-1.349c-0.743,-0.001,-1.347,0.601,-1.348,1.344C68.465,23.757,68.465,23.759,68.465,23.76zM61.265,16.56c0,0.744,0.603,1.346,1.347,1.346c0.744,0,1.346,-0.604,1.346,-1.346c0,-0.743,-0.603,-1.347,-1.346,-1.347C61.869,15.213,61.265,15.816,61.265,16.56zM61.265,23.76c0,0.743,0.603,1.346,1.347,1.346c0.744,0,1.346,-0.603,1.346,-1.346c0,-0.744,-0.603,-1.347,-1.346,-1.347C61.869,22.413,61.265,23.016,61.265,23.76zM134.847,7.2c-0.001,0.665,0.536,1.206,1.202,1.207c0.664,0.001,1.205,-0.537,1.207,-1.202c0,-0.001,0,-0.003,0,-0.005c0.002,-0.666,-0.537,-1.206,-1.202,-1.208c-0.665,-0.002,-1.206,0.537,-1.207,1.202C134.847,7.197,134.847,7.198,134.847,7.2zM127.647,7.2c-0.002,0.665,0.537,1.206,1.202,1.207c0.665,0.001,1.206,-0.537,1.208,-1.202c0,-0.001,0,-0.003,0,-0.005c0.002,-0.666,-0.536,-1.207,-1.201,-1.209c-0.666,-0.002,-1.207,0.536,-1.209,1.201C127.647,7.195,127.647,7.197,127.647,7.2L127.647,7.2zM120.448,7.2c-0.003,0.665,0.535,1.207,1.199,1.208c0.666,0.002,1.207,-0.535,1.209,-1.201c0,-0.002,0,-0.005,0,-0.008c0.002,-0.666,-0.535,-1.207,-1.199,-1.209c-0.666,-0.002,-1.207,0.536,-1.209,1.201C120.448,7.195,120.448,7.197,120.448,7.2zM113.247,7.2c-0.002,0.665,0.535,1.207,1.201,1.208c0.666,0.002,1.207,-0.535,1.209,-1.201c0,-0.002,0,-0.005,0,-0.008c0.002,-0.666,-0.535,-1.207,-1.201,-1.209c-0.664,-0.002,-1.207,0.536,-1.209,1.201C113.247,7.195,113.247,7.197,113.247,7.2zM106.047,7.2c-0.002,0.665,0.536,1.207,1.202,1.208c0.664,0.002,1.205,-0.535,1.209,-1.201c0,-0.002,0,-0.005,0,-0.008c0.002,-0.666,-0.537,-1.207,-1.201,-1.209c-0.666,-0.002,-1.207,0.536,-1.208,1.201C106.047,7.195,106.047,7.197,106.047,7.2zM98.847,7.2c-0.002,0.665,0.535,1.207,1.201,1.208c0.666,0.002,1.207,-0.535,1.208,-1.201c0,-0.002,0,-0.005,0,-0.008c0.002,-0.666,-0.535,-1.207,-1.201,-1.209c-0.665,-0.002,-1.207,0.536,-1.208,1.201C98.847,7.195,98.847,7.197,98.847,7.2zM91.646,7.2c-0.002,0.665,0.536,1.207,1.201,1.208c0.666,0.002,1.207,-0.535,1.209,-1.201c0,-0.002,0,-0.005,0,-0.008c0.002,-0.666,-0.536,-1.207,-1.201,-1.209c-0.666,-0.002,-1.207,0.536,-1.209,1.201C91.646,7.195,91.646,7.197,91.646,7.2zM84.447,7.2c-0.002,0.665,0.535,1.207,1.201,1.208c0.665,0.002,1.207,-0.535,1.208,-1.201c0,-0.002,0,-0.005,0,-0.008c0.002,-0.666,-0.535,-1.207,-1.201,-1.209c-0.665,-0.002,-1.207,0.536,-1.208,1.201C84.447,7.195,84.447,7.197,84.447,7.2zM77.247,7.2c-0.002,0.665,0.536,1.207,1.201,1.208c0.666,0.002,1.207,-0.535,1.209,-1.201c0,-0.002,0,-0.005,0,-0.008c0.002,-0.666,-0.536,-1.207,-1.201,-1.209c-0.665,-0.002,-1.206,0.536,-1.208,1.201C77.247,7.195,77.247,7.197,77.247,7.2zM70.047,7.2c-0.002,0.665,0.535,1.207,1.201,1.208c0.666,0.002,1.207,-0.535,1.209,-1.201c0,-0.002,0,-0.005,0,-0.008c0.002,-0.666,-0.536,-1.207,-1.201,-1.209c-0.666,-0.002,-1.207,0.536,-1.209,1.201C70.047,7.195,70.047,7.197,70.047,7.2zM196.767,7.2c-0.001,0.665,0.536,1.206,1.202,1.207c0.664,0.001,1.205,-0.537,1.207,-1.202c0,-0.001,0,-0.003,0,-0.005c0.002,-0.666,-0.537,-1.206,-1.201,-1.208c-0.666,-0.001,-1.207,0.537,-1.208,1.202C196.767,7.197,196.767,7.198,196.767,7.2zM189.567,7.2c-0.002,0.665,0.537,1.206,1.202,1.207c0.665,0.001,1.206,-0.537,1.208,-1.202c0,-0.001,0,-0.003,0,-0.005c0.001,-0.666,-0.537,-1.206,-1.203,-1.208c-0.665,-0.001,-1.205,0.537,-1.207,1.202C189.567,7.197,189.567,7.198,189.567,7.2zM182.368,7.2c-0.002,0.665,0.536,1.206,1.201,1.207c0.666,0.001,1.206,-0.537,1.207,-1.202c0,-0.001,0,-0.003,0,-0.005c0.002,-0.666,-0.535,-1.206,-1.201,-1.208c-0.666,-0.001,-1.205,0.537,-1.207,1.202C182.368,7.197,182.368,7.198,182.368,7.2zM175.167,7.2c0,0.665,0.537,1.206,1.203,1.207c0.666,0.001,1.205,-0.537,1.207,-1.202c0,-0.001,0,-0.003,0,-0.005c0.002,-0.666,-0.537,-1.206,-1.201,-1.208c-0.666,-0.002,-1.207,0.537,-1.209,1.202C175.167,7.197,175.167,7.198,175.167,7.2zM167.967,7.2c-0.002,0.665,0.537,1.206,1.201,1.207c0.666,0.001,1.207,-0.537,1.207,-1.202c0,-0.001,0,-0.003,0,-0.005c0.002,-0.666,-0.535,-1.206,-1.201,-1.208c-0.666,-0.002,-1.207,0.537,-1.207,1.202C167.967,7.197,167.967,7.198,167.967,7.2zM160.767,7.2c-0.001,0.665,0.536,1.206,1.202,1.207c0.664,0.001,1.205,-0.537,1.207,-1.202c0,-0.001,0,-0.003,0,-0.005c0.002,-0.666,-0.537,-1.206,-1.201,-1.208c-0.666,-0.001,-1.207,0.537,-1.208,1.202C160.767,7.197,160.767,7.198,160.767,7.2zM153.567,7.2c-0.002,0.665,0.537,1.206,1.202,1.207c0.665,0.001,1.206,-0.537,1.208,-1.202c0,-0.001,0,-0.003,0,-0.005c0.001,-0.666,-0.537,-1.206,-1.203,-1.208c-0.665,-0.001,-1.205,0.537,-1.207,1.202C153.567,7.197,153.567,7.198,153.567,7.2zM146.368,7.2c-0.002,0.665,0.536,1.206,1.201,1.207c0.666,0.001,1.206,-0.537,1.207,-1.202c0,-0.001,0,-0.003,0,-0.005c0.002,-0.666,-0.535,-1.206,-1.201,-1.208c-0.666,-0.001,-1.205,0.537,-1.207,1.202C146.368,7.197,146.368,7.198,146.368,7.2zM103.167,144c-0.002,0.664,0.535,1.205,1.201,1.207c0.666,0.004,1.207,-0.535,1.208,-1.199c0,-0.004,0,-0.006,0,-0.008c0.002,-0.666,-0.535,-1.207,-1.2,-1.209c-0.666,-0.002,-1.207,0.535,-1.209,1.201C103.167,143.995,103.167,143.999,103.167,144zM95.968,144c-0.002,0.664,0.535,1.205,1.201,1.207c0.666,0.004,1.207,-0.535,1.208,-1.199c0,-0.004,0,-0.006,0,-0.008c0.002,-0.666,-0.535,-1.207,-1.2,-1.209c-0.666,-0.002,-1.207,0.535,-1.209,1.201C95.968,143.995,95.968,143.999,95.968,144zM110.368,144c-0.002,0.664,0.535,1.205,1.2,1.207c0.665,0.004,1.206,-0.535,1.208,-1.199c0,-0.004,0,-0.006,0,-0.008c0.003,-0.666,-0.535,-1.207,-1.199,-1.209c-0.666,-0.002,-1.207,0.535,-1.209,1.201C110.368,143.995,110.368,143.999,110.368,144zM117.567,144c-0.002,0.664,0.535,1.205,1.201,1.207c0.665,0.004,1.206,-0.535,1.209,-1.199c0,-0.004,0,-0.006,0,-0.008c0.002,-0.666,-0.536,-1.207,-1.201,-1.209c-0.666,-0.002,-1.207,0.535,-1.209,1.201C117.567,143.995,117.567,143.999,117.567,144zM124.767,144c-0.003,0.664,0.534,1.205,1.2,1.207c0.666,0.004,1.207,-0.535,1.209,-1.199c0,-0.004,0,-0.006,0,-0.008c0.002,-0.666,-0.535,-1.207,-1.201,-1.209c-0.664,-0.002,-1.206,0.535,-1.208,1.201C124.767,143.995,124.767,143.999,124.767,144zM131.967,144c-0.002,0.664,0.537,1.205,1.201,1.207c0.666,0.002,1.207,-0.537,1.207,-1.203c0,-0.002,0,-0.004,0,-0.004c0.002,-0.666,-0.535,-1.207,-1.201,-1.209c-0.666,0,-1.207,0.537,-1.207,1.203C131.967,143.997,131.967,143.999,131.967,144zM139.167,144c0,0.664,0.537,1.205,1.203,1.207s1.205,-0.537,1.207,-1.203c0,-0.002,0,-0.004,0,-0.004c0.002,-0.666,-0.537,-1.207,-1.201,-1.209c-0.666,0,-1.207,0.537,-1.209,1.203C139.167,143.997,139.167,143.999,139.167,144zM146.368,144c-0.002,0.664,0.536,1.205,1.201,1.207c0.666,0.002,1.206,-0.537,1.207,-1.203c0,-0.002,0,-0.004,0,-0.004c0.002,-0.666,-0.535,-1.207,-1.201,-1.209c-0.666,0,-1.205,0.537,-1.207,1.203C146.368,143.997,146.368,143.999,146.368,144z"/>
      <g  gorn="0.2.0.1" id="_x30_.1.0.1">
       <title  id="0.1.0.1.0">layer 21</title>
       <circle  fill="none" cx="80.612" gorn="0.2.0.1.1" cy="12.96" stroke="#FFFFFF" id="_x30_.1.0.1.1" r="0.72" stroke-width="0.72"/>
       <g  gorn="0.2.0.1.2" id="_x30_.1.0.1.2">
        <title  id="0.1.0.1.2.0">text:MADE IN</title>
       </g>
       <g  gorn="0.2.0.1.3" id="_x30_.1.0.1.3">
        <title  id="0.1.0.1.3.0">text:ITALY</title>
       </g>
       <g  gorn="0.2.0.1.4" id="_x30_.1.0.1.4">
        <title  id="0.1.0.1.4.0">text:Prototype</title>
       </g>
       <g  gorn="0.2.0.1.5" id="_x30_.1.0.1.5">
        <title  id="0.1.0.1.5.0">text:Limited</title>
       </g>
       <g  gorn="0.2.0.1.6" id="_x30_.1.0.1.6">
        <title  id="0.1.0.1.6.0">text:Edition</title>
       </g>
       <g  gorn="0.2.0.1.7" id="_x30_.1.0.1.7">
        <g  gorn="0.2.0.1.7.0" id="_x30_.1.0.1.7.0">
         <g transform="matrix(1, 0, 0, 1, 102.569, 12.24)">
          <g >
           <g >
            <g >
             <g  gorn="0.2.0.1.7.0.0.0.0.0" id="_x30_.1.0.1.7.0.0">
              <g  gorn="0.2.0.1.7.0.0.0.0.0.0" id="_x30_.1.0.1.7.0.0.0">
               <g transform="rotate(-90)">
                <g >
                 <g >
                  <g >
                   <g  gorn="0.2.0.1.7.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.0.1.7.0.0.0.0">
                    <g  gorn="0.2.0.1.7.0.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.0.1.7.0.0.0.0.0">
                     <g transform="matrix(1, 0, 0, 1, -5.1472, -0.9391)">
                      <g >
                       <g >
                        <g >
                         <g  gorn="0.2.0.1.7.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.0.1.7.0.0.0.0.0.0">
                          <g transform="matrix(1, 0, 0, 1, -3.05176e-05, -3.05176e-05)">
                           <g >
                            <g >
                             <g >
                              <text  fill="#FFFFFF" font-family="'OCRA'" gorn="0.2.0.1.7.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.0.1.7.0.0.0.0.0.0.0" font-size="3.75">13</text>
                             </g>
                            </g>
                           </g>
                          </g>
                         </g>
                        </g>
                       </g>
                      </g>
                     </g>
                    </g>
                   </g>
                  </g>
                 </g>
                </g>
               </g>
              </g>
             </g>
            </g>
           </g>
          </g>
         </g>
        </g>
       </g>
       <g  gorn="0.2.0.1.8" id="_x30_.1.0.1.8">
        <g  gorn="0.2.0.1.8.0" id="_x30_.1.0.1.8.0">
         <g transform="matrix(1, 0, 0, 1, 109.769, 12.24)">
          <g >
           <g >
            <g >
             <g  gorn="0.2.0.1.8.0.0.0.0.0" id="_x30_.1.0.1.8.0.0">
              <g  gorn="0.2.0.1.8.0.0.0.0.0.0" id="_x30_.1.0.1.8.0.0.0">
               <g transform="rotate(-90)">
                <g >
                 <g >
                  <g >
                   <g  gorn="0.2.0.1.8.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.0.1.8.0.0.0.0">
                    <g  gorn="0.2.0.1.8.0.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.0.1.8.0.0.0.0.0">
                     <g transform="matrix(1, 0, 0, 1, -5.1472, -0.9384)">
                      <g >
                       <g >
                        <g >
                         <g  gorn="0.2.0.1.8.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.0.1.8.0.0.0.0.0.0">
                          <g transform="matrix(1, 0, 0, 1, -3.05176e-05, 0)">
                           <g >
                            <g >
                             <g >
                              <text  fill="#FFFFFF" font-family="'OCRA'" gorn="0.2.0.1.8.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.0.1.8.0.0.0.0.0.0.0" font-size="3.75">12</text>
                             </g>
                            </g>
                           </g>
                          </g>
                         </g>
                        </g>
                       </g>
                      </g>
                     </g>
                    </g>
                   </g>
                  </g>
                 </g>
                </g>
               </g>
              </g>
             </g>
            </g>
           </g>
          </g>
         </g>
        </g>
       </g>
       <g  gorn="0.2.0.1.9" id="_x30_.1.0.1.9">
        <g  gorn="0.2.0.1.9.0" id="_x30_.1.0.1.9.0">
         <g transform="matrix(1, 0, 0, 1, 116.969, 12.24)">
          <g >
           <g >
            <g >
             <g  gorn="0.2.0.1.9.0.0.0.0.0" id="_x30_.1.0.1.9.0.0">
              <g  gorn="0.2.0.1.9.0.0.0.0.0.0" id="_x30_.1.0.1.9.0.0.0">
               <g transform="rotate(-90)">
                <g >
                 <g >
                  <g >
                   <g  gorn="0.2.0.1.9.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.0.1.9.0.0.0.0">
                    <g  gorn="0.2.0.1.9.0.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.0.1.9.0.0.0.0.0">
                     <g transform="matrix(1, 0, 0, 1, -5.1472, -0.9392)">
                      <g >
                       <g >
                        <g >
                         <g  gorn="0.2.0.1.9.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.0.1.9.0.0.0.0.0.0">
                          <g transform="matrix(1, 0, 0, 1, -3.05176e-05, 0)">
                           <g >
                            <g >
                             <g >
                              <text  fill="#FFFFFF" font-family="'OCRA'" gorn="0.2.0.1.9.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.0.1.9.0.0.0.0.0.0.0" font-size="3.75">11</text>
                             </g>
                            </g>
                           </g>
                          </g>
                         </g>
                        </g>
                       </g>
                      </g>
                     </g>
                    </g>
                   </g>
                  </g>
                 </g>
                </g>
               </g>
              </g>
             </g>
            </g>
           </g>
          </g>
         </g>
        </g>
       </g>
       <g  gorn="0.2.0.1.10" id="_x30_.1.0.1.10">
        <g  gorn="0.2.0.1.10.0" id="_x30_.1.0.1.10.0">
         <g transform="matrix(1, 0, 0, 1, 124.169, 12.24)">
          <g >
           <g >
            <g >
             <g  gorn="0.2.0.1.10.0.0.0.0.0" id="_x30_.1.0.1.10.0.0">
              <g  gorn="0.2.0.1.10.0.0.0.0.0.0" id="_x30_.1.0.1.10.0.0.0">
               <g transform="rotate(-90)">
                <g >
                 <g >
                  <g >
                   <g  gorn="0.2.0.1.10.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.0.1.10.0.0.0.0">
                    <g  gorn="0.2.0.1.10.0.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.0.1.10.0.0.0.0.0">
                     <g transform="matrix(1, 0, 0, 1, -5.1472, -0.94)">
                      <g >
                       <g >
                        <g >
                         <g  gorn="0.2.0.1.10.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.0.1.10.0.0.0.0.0.0">
                          <g transform="matrix(1, 0, 0, 1, -3.05176e-05, 0)">
                           <g >
                            <g >
                             <g >
                              <text  fill="#FFFFFF" font-family="'OCRA'" gorn="0.2.0.1.10.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.0.1.10.0.0.0.0.0.0.0" font-size="3.75">10</text>
                             </g>
                            </g>
                           </g>
                          </g>
                         </g>
                        </g>
                       </g>
                      </g>
                     </g>
                    </g>
                   </g>
                  </g>
                 </g>
                </g>
               </g>
              </g>
             </g>
            </g>
           </g>
          </g>
         </g>
        </g>
       </g>
       <g  gorn="0.2.0.1.11" id="_x30_.1.0.1.11">
        <g  gorn="0.2.0.1.11.0" id="_x30_.1.0.1.11.0">
         <g transform="matrix(1, 0, 0, 1, 131.369, 12.24)">
          <g >
           <g >
            <g >
             <g  gorn="0.2.0.1.11.0.0.0.0.0" id="_x30_.1.0.1.11.0.0">
              <g  gorn="0.2.0.1.11.0.0.0.0.0.0" id="_x30_.1.0.1.11.0.0.0">
               <g transform="rotate(-90)">
                <g >
                 <g >
                  <g >
                   <g  gorn="0.2.0.1.11.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.0.1.11.0.0.0.0">
                    <g  gorn="0.2.0.1.11.0.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.0.1.11.0.0.0.0.0">
                     <g transform="matrix(1, 0, 0, 1, -2.4402, -0.9388)">
                      <g >
                       <g >
                        <g >
                         <g  gorn="0.2.0.1.11.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.0.1.11.0.0.0.0.0.0">
                          <g transform="matrix(1, 0, 0, 1, 0, -6.10352e-05)">
                           <g >
                            <g >
                             <g >
                              <text  fill="#FFFFFF" font-family="'OCRA'" gorn="0.2.0.1.11.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.0.1.11.0.0.0.0.0.0.0" font-size="3.75">9</text>
                             </g>
                            </g>
                           </g>
                          </g>
                         </g>
                        </g>
                       </g>
                      </g>
                     </g>
                    </g>
                   </g>
                  </g>
                 </g>
                </g>
               </g>
              </g>
             </g>
            </g>
           </g>
          </g>
         </g>
        </g>
       </g>
       <g  gorn="0.2.0.1.12" id="_x30_.1.0.1.12">
        <g  gorn="0.2.0.1.12.0" id="_x30_.1.0.1.12.0">
         <g transform="matrix(1, 0, 0, 1, 138.569, 12.24)">
          <g >
           <g >
            <g >
             <g  gorn="0.2.0.1.12.0.0.0.0.0" id="_x30_.1.0.1.12.0.0">
              <g  gorn="0.2.0.1.12.0.0.0.0.0.0" id="_x30_.1.0.1.12.0.0.0">
               <g transform="rotate(-90)">
                <g >
                 <g >
                  <g >
                   <g  gorn="0.2.0.1.12.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.0.1.12.0.0.0.0">
                    <g  gorn="0.2.0.1.12.0.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.0.1.12.0.0.0.0.0">
                     <g transform="matrix(1, 0, 0, 1, -2.4402, -0.9396)">
                      <g >
                       <g >
                        <g >
                         <g  gorn="0.2.0.1.12.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.0.1.12.0.0.0.0.0.0">
                          <text  fill="#FFFFFF" font-family="'OCRA'" gorn="0.2.0.1.12.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.0.1.12.0.0.0.0.0.0.0" font-size="3.75">8</text>
                         </g>
                        </g>
                       </g>
                      </g>
                     </g>
                    </g>
                   </g>
                  </g>
                 </g>
                </g>
               </g>
              </g>
             </g>
            </g>
           </g>
          </g>
         </g>
        </g>
       </g>
       <g  gorn="0.2.0.1.13" id="_x30_.1.0.1.13">
        <g  gorn="0.2.0.1.13.0" id="_x30_.1.0.1.13.0">
         <g transform="matrix(1, 0, 0, 1, 150.089, 12.24)">
          <g >
           <g >
            <g >
             <g  gorn="0.2.0.1.13.0.0.0.0.0" id="_x30_.1.0.1.13.0.0">
              <g  gorn="0.2.0.1.13.0.0.0.0.0.0" id="_x30_.1.0.1.13.0.0.0">
               <g transform="rotate(-90)">
                <g >
                 <g >
                  <g >
                   <g  gorn="0.2.0.1.13.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.0.1.13.0.0.0.0">
                    <g  gorn="0.2.0.1.13.0.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.0.1.13.0.0.0.0.0">
                     <g transform="matrix(1, 0, 0, 1, -2.4402, -0.9401)">
                      <g >
                       <g >
                        <g >
                         <g  gorn="0.2.0.1.13.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.0.1.13.0.0.0.0.0.0">
                          <g transform="matrix(1, 0, 0, 1, 0, 6.10352e-05)">
                           <g >
                            <g >
                             <g >
                              <text  fill="#FFFFFF" font-family="'OCRA'" gorn="0.2.0.1.13.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.0.1.13.0.0.0.0.0.0.0" font-size="3.75">7</text>
                             </g>
                            </g>
                           </g>
                          </g>
                         </g>
                        </g>
                       </g>
                      </g>
                     </g>
                    </g>
                   </g>
                  </g>
                 </g>
                </g>
               </g>
              </g>
             </g>
            </g>
           </g>
          </g>
         </g>
        </g>
       </g>
       <g  gorn="0.2.0.1.14" id="_x30_.1.0.1.14">
        <g  gorn="0.2.0.1.14.0" id="_x30_.1.0.1.14.0">
         <g transform="matrix(1, 0, 0, 1, 157.289, 12.24)">
          <g >
           <g >
            <g >
             <g  gorn="0.2.0.1.14.0.0.0.0.0" id="_x30_.1.0.1.14.0.0">
              <g  gorn="0.2.0.1.14.0.0.0.0.0.0" id="_x30_.1.0.1.14.0.0.0">
               <g transform="rotate(-90)">
                <g >
                 <g >
                  <g >
                   <g  gorn="0.2.0.1.14.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.0.1.14.0.0.0.0">
                    <g  gorn="0.2.0.1.14.0.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.0.1.14.0.0.0.0.0">
                     <g transform="matrix(1, 0, 0, 1, -2.4402, -0.9389)">
                      <g >
                       <g >
                        <g >
                         <g  gorn="0.2.0.1.14.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.0.1.14.0.0.0.0.0.0">
                          <text  fill="#FFFFFF" font-family="'OCRA'" gorn="0.2.0.1.14.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.0.1.14.0.0.0.0.0.0.0" font-size="3.75">6</text>
                         </g>
                        </g>
                       </g>
                      </g>
                     </g>
                    </g>
                   </g>
                  </g>
                 </g>
                </g>
               </g>
              </g>
             </g>
            </g>
           </g>
          </g>
         </g>
        </g>
       </g>
       <g  gorn="0.2.0.1.15" id="_x30_.1.0.1.15">
        <g  gorn="0.2.0.1.15.0" id="_x30_.1.0.1.15.0">
         <g transform="matrix(1, 0, 0, 1, 164.489, 12.24)">
          <g >
           <g >
            <g >
             <g  gorn="0.2.0.1.15.0.0.0.0.0" id="_x30_.1.0.1.15.0.0">
              <g  gorn="0.2.0.1.15.0.0.0.0.0.0" id="_x30_.1.0.1.15.0.0.0">
               <g transform="rotate(-90)">
                <g >
                 <g >
                  <g >
                   <g  gorn="0.2.0.1.15.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.0.1.15.0.0.0.0">
                    <g  gorn="0.2.0.1.15.0.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.0.1.15.0.0.0.0.0">
                     <g transform="matrix(1, 0, 0, 1, -2.4402, -0.9397)">
                      <g >
                       <g >
                        <g >
                         <g  gorn="0.2.0.1.15.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.0.1.15.0.0.0.0.0.0">
                          <text  fill="#FFFFFF" font-family="'OCRA'" gorn="0.2.0.1.15.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.0.1.15.0.0.0.0.0.0.0" font-size="3.75">5</text>
                         </g>
                        </g>
                       </g>
                      </g>
                     </g>
                    </g>
                   </g>
                  </g>
                 </g>
                </g>
               </g>
              </g>
             </g>
            </g>
           </g>
          </g>
         </g>
        </g>
       </g>
       <g  gorn="0.2.0.1.16" id="_x30_.1.0.1.16">
        <g  gorn="0.2.0.1.16.0" id="_x30_.1.0.1.16.0">
         <g transform="matrix(1, 0, 0, 1, 171.689, 12.24)">
          <g >
           <g >
            <g >
             <g  gorn="0.2.0.1.16.0.0.0.0.0" id="_x30_.1.0.1.16.0.0">
              <g  gorn="0.2.0.1.16.0.0.0.0.0.0" id="_x30_.1.0.1.16.0.0.0">
               <g transform="rotate(-90)">
                <g >
                 <g >
                  <g >
                   <g  gorn="0.2.0.1.16.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.0.1.16.0.0.0.0">
                    <g  gorn="0.2.0.1.16.0.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.0.1.16.0.0.0.0.0">
                     <g transform="matrix(1, 0, 0, 1, -2.4402, -0.9405)">
                      <g >
                       <g >
                        <g >
                         <g  gorn="0.2.0.1.16.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.0.1.16.0.0.0.0.0.0">
                          <g transform="matrix(1, 0, 0, 1, 0, 6.10352e-05)">
                           <g >
                            <g >
                             <g >
                              <text  fill="#FFFFFF" font-family="'OCRA'" gorn="0.2.0.1.16.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.0.1.16.0.0.0.0.0.0.0" font-size="3.75">4</text>
                             </g>
                            </g>
                           </g>
                          </g>
                         </g>
                        </g>
                       </g>
                      </g>
                     </g>
                    </g>
                   </g>
                  </g>
                 </g>
                </g>
               </g>
              </g>
             </g>
            </g>
           </g>
          </g>
         </g>
        </g>
       </g>
       <g  gorn="0.2.0.1.17" id="_x30_.1.0.1.17">
        <g  gorn="0.2.0.1.17.0" id="_x30_.1.0.1.17.0">
         <g transform="matrix(1, 0, 0, 1, 178.889, 12.24)">
          <g >
           <g >
            <g >
             <g  gorn="0.2.0.1.17.0.0.0.0.0" id="_x30_.1.0.1.17.0.0">
              <g  gorn="0.2.0.1.17.0.0.0.0.0.0" id="_x30_.1.0.1.17.0.0.0">
               <g transform="rotate(-90)">
                <g >
                 <g >
                  <g >
                   <g  gorn="0.2.0.1.17.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.0.1.17.0.0.0.0">
                    <g  gorn="0.2.0.1.17.0.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.0.1.17.0.0.0.0.0">
                     <g transform="matrix(1, 0, 0, 1, -2.4402, -0.9393)">
                      <g >
                       <g >
                        <g >
                         <g  gorn="0.2.0.1.17.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.0.1.17.0.0.0.0.0.0">
                          <text  fill="#FFFFFF" font-family="'OCRA'" gorn="0.2.0.1.17.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.0.1.17.0.0.0.0.0.0.0" font-size="3.75">3</text>
                         </g>
                        </g>
                       </g>
                      </g>
                     </g>
                    </g>
                   </g>
                  </g>
                 </g>
                </g>
               </g>
              </g>
             </g>
            </g>
           </g>
          </g>
         </g>
        </g>
       </g>
       <g  gorn="0.2.0.1.18" id="_x30_.1.0.1.18">
        <g  gorn="0.2.0.1.18.0" id="_x30_.1.0.1.18.0">
         <g transform="matrix(1, 0, 0, 1, 186.089, 12.24)">
          <g >
           <g >
            <g >
             <g  gorn="0.2.0.1.18.0.0.0.0.0" id="_x30_.1.0.1.18.0.0">
              <g  gorn="0.2.0.1.18.0.0.0.0.0.0" id="_x30_.1.0.1.18.0.0.0">
               <g transform="rotate(-90)">
                <g >
                 <g >
                  <g >
                   <g  gorn="0.2.0.1.18.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.0.1.18.0.0.0.0">
                    <g  gorn="0.2.0.1.18.0.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.0.1.18.0.0.0.0.0">
                     <g transform="matrix(1, 0, 0, 1, -2.4402, -0.9401)">
                      <g >
                       <g >
                        <g >
                         <g  gorn="0.2.0.1.18.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.0.1.18.0.0.0.0.0.0">
                          <g transform="matrix(1, 0, 0, 1, 0, 6.10352e-05)">
                           <g >
                            <g >
                             <g >
                              <text  fill="#FFFFFF" font-family="'OCRA'" gorn="0.2.0.1.18.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.0.1.18.0.0.0.0.0.0.0" font-size="3.75">2</text>
                             </g>
                            </g>
                           </g>
                          </g>
                         </g>
                        </g>
                       </g>
                      </g>
                     </g>
                    </g>
                   </g>
                  </g>
                 </g>
                </g>
               </g>
              </g>
             </g>
            </g>
           </g>
          </g>
         </g>
        </g>
       </g>
       <g  gorn="0.2.0.1.19" id="_x30_.1.0.1.20">
        <title  id="0.1.0.1.20.0">element:C1</title>
        <g  gorn="0.2.0.1.19.1" id="_x30_.1.0.1.20.1">
         <title  id="0.1.0.1.20.1.0">package:C0603-ROUND</title>
        </g>
       </g>
       <g  gorn="0.2.0.1.20" id="_x30_.1.0.1.21">
        <title  id="0.1.0.1.21.0">element:C2</title>
        <g  gorn="0.2.0.1.20.1" id="_x30_.1.0.1.21.1">
         <title  id="0.1.0.1.21.1.0">package:C0603-ROUND</title>
        </g>
       </g>
       <g  gorn="0.2.0.1.21" id="_x30_.1.0.1.22">
        <title  id="0.1.0.1.22.0">element:C3</title>
        <g  gorn="0.2.0.1.21.1" id="_x30_.1.0.1.22.1">
         <title  id="0.1.0.1.22.1.0">package:C0603-ROUND</title>
        </g>
       </g>
       <g  gorn="0.2.0.1.22" id="_x30_.1.0.1.23">
        <title  id="0.1.0.1.23.0">element:C4</title>
        <g  gorn="0.2.0.1.22.1" id="_x30_.1.0.1.23.1">
         <title  id="0.1.0.1.23.1.0">package:C0603-ROUND</title>
        </g>
       </g>
       <g  gorn="0.2.0.1.23" id="_x30_.1.0.1.24">
        <title  id="0.1.0.1.24.0">element:C5</title>
        <g  gorn="0.2.0.1.23.1" id="_x30_.1.0.1.24.1">
         <title  id="0.1.0.1.24.1.0">package:C0603-ROUND</title>
        </g>
       </g>
       <g  gorn="0.2.0.1.24" id="_x30_.1.0.1.25">
        <title  id="0.1.0.1.25.0">element:C6</title>
        <g  gorn="0.2.0.1.24.1" id="_x30_.1.0.1.25.1">
         <title  id="0.1.0.1.25.1.0">package:C0603-ROUND</title>
        </g>
       </g>
       <g  gorn="0.2.0.1.25" id="_x30_.1.0.1.26">
        <title  id="0.1.0.1.26.0">element:C7</title>
        <g  gorn="0.2.0.1.25.1" id="_x30_.1.0.1.26.1">
         <title  id="0.1.0.1.26.1.0">package:C0603-ROUND</title>
        </g>
       </g>
       <g  gorn="0.2.0.1.26" id="_x30_.1.0.1.27">
        <title  id="0.1.0.1.27.0">element:C8</title>
        <g  gorn="0.2.0.1.26.1" id="_x30_.1.0.1.27.1">
         <title  id="0.1.0.1.27.1.0">package:C0603-ROUND</title>
        </g>
       </g>
       <g  gorn="0.2.0.1.27" id="_x30_.1.0.1.28">
        <title  id="0.1.0.1.28.0">element:C9</title>
        <g  gorn="0.2.0.1.27.1" id="_x30_.1.0.1.28.1">
         <title  id="0.1.0.1.28.1.0">package:C0603-ROUND</title>
        </g>
       </g>
       <g  gorn="0.2.0.1.28" id="_x30_.1.0.1.29">
        <title  id="0.1.0.1.29.0">element:C11</title>
        <g  gorn="0.2.0.1.28.1" id="_x30_.1.0.1.29.1">
         <title  id="0.1.0.1.29.1.0">package:C0603-ROUND</title>
        </g>
       </g>
       <g  gorn="0.2.0.1.29" id="_x30_.1.0.1.31">
        <title  id="0.1.0.1.31.0">element:F1</title>
        <g  gorn="0.2.0.1.29.1" id="_x30_.1.0.1.31.1">
         <title  id="0.1.0.1.31.1.0">package:L1812</title>
        </g>
       </g>
       <g  gorn="0.2.0.1.30" id="_x30_.1.0.1.32">
        <title  id="0.1.0.1.32.0">element:FD1</title>
        <g  gorn="0.2.0.1.30.1" id="_x30_.1.0.1.32.1">
         <title  id="0.1.0.1.32.1.0">package:FIDUCIA-MOUNT</title>
        </g>
       </g>
       <g  gorn="0.2.0.1.31" id="_x30_.1.0.1.33">
        <title  id="0.1.0.1.33.0">element:FD2</title>
        <g  gorn="0.2.0.1.31.1" id="_x30_.1.0.1.33.1">
         <title  id="0.1.0.1.33.1.0">package:FIDUCIA-MOUNT</title>
        </g>
       </g>
       <g  gorn="0.2.0.1.32" id="_x30_.1.0.1.34">
        <title  id="0.1.0.1.34.0">element:FD3</title>
        <g  gorn="0.2.0.1.32.1" id="_x30_.1.0.1.34.1">
         <title  id="0.1.0.1.34.1.0">package:FIDUCIA-MOUNT</title>
        </g>
       </g>
       <g  gorn="0.2.0.1.33" id="_x30_.1.0.1.35">
        <title  id="0.1.0.1.35.0">element:GROUND</title>
        <g  gorn="0.2.0.1.33.1" id="_x30_.1.0.1.35.1">
         <title  id="0.1.0.1.35.1.0">package:SJ</title>
        </g>
       </g>
       <g  gorn="0.2.0.1.34" id="_x30_.1.0.1.40">
        <title  id="0.1.0.1.40.0">element:L</title>
        <g  gorn="0.2.0.1.34.1" id="_x30_.1.0.1.40.1">
         <title  id="0.1.0.1.40.1.0">text:L</title>
         <g transform="matrix(1, 0, 0, 1, 88.3521, 36.1958)">
          <g >
           <g >
            <g >
             <g  gorn="0.2.0.1.34.1.1.0.0.0" id="_x30_.1.0.1.40.1.1">
              <g transform="matrix(1, 0, 0, 1, -6.10351e-05, 0)">
               <g >
                <g >
                 <g >
                  <text  fill="#FFFFFF" font-family="'OCRA'" gorn="0.2.0.1.34.1.1.0.0.0.0.0.0.0" id="_x30_.1.0.1.40.1.1.0" font-size="4.6771">L</text>
                 </g>
                </g>
               </g>
              </g>
             </g>
            </g>
           </g>
          </g>
         </g>
        </g>
       </g>
       <g  gorn="0.2.0.1.35" id="_x30_.1.0.1.44">
        <title  id="0.1.0.1.44.0">element:R1</title>
        <g  gorn="0.2.0.1.35.1" id="_x30_.1.0.1.44.1">
         <title  id="0.1.0.1.44.1.0">package:R0603-ROUND</title>
        </g>
       </g>
       <g  gorn="0.2.0.1.36" id="_x30_.1.0.1.45">
        <title  id="0.1.0.1.45.0">element:R2</title>
        <g  gorn="0.2.0.1.36.1" id="_x30_.1.0.1.45.1">
         <title  id="0.1.0.1.45.1.0">package:R0603-ROUND</title>
        </g>
       </g>
       <g  gorn="0.2.0.1.37" id="_x30_.1.0.1.46">
        <title  id="0.1.0.1.46.0">element:RN1</title>
        <g  gorn="0.2.0.1.37.1" id="_x30_.1.0.1.46.1">
         <title  id="0.1.0.1.46.1.0">package:CAY16</title>
        </g>
       </g>
       <g  gorn="0.2.0.1.38" id="_x30_.1.0.1.47">
        <title  id="0.1.0.1.47.0">element:RN2</title>
        <g  gorn="0.2.0.1.38.1" id="_x30_.1.0.1.47.1">
         <title  id="0.1.0.1.47.1.0">package:CAY16</title>
        </g>
       </g>
       <g  gorn="0.2.0.1.39" id="_x30_.1.0.1.48">
        <title  id="0.1.0.1.48.0">element:RN3</title>
        <g  gorn="0.2.0.1.39.1" id="_x30_.1.0.1.48.1">
         <title  id="0.1.0.1.48.1.0">package:CAY16</title>
        </g>
       </g>
       <g  gorn="0.2.0.1.40" id="_x30_.1.0.1.49">
        <title  id="0.1.0.1.49.0">element:RN4</title>
        <g  gorn="0.2.0.1.40.1" id="_x30_.1.0.1.49.1">
         <title  id="0.1.0.1.49.1.0">package:CAY16</title>
        </g>
       </g>
       <g  gorn="0.2.0.1.41" id="_x30_.1.0.1.52">
        <title  id="0.1.0.1.52.0">element:Z1</title>
        <g  gorn="0.2.0.1.41.1" id="_x30_.1.0.1.52.1">
         <title  id="0.1.0.1.52.1.0">package:CT/CN0603</title>
        </g>
       </g>
       <g  gorn="0.2.0.1.42" id="_x30_.1.0.1.53">
        <title  id="0.1.0.1.53.0">element:Z2</title>
        <g  gorn="0.2.0.1.42.1" id="_x30_.1.0.1.53.1">
         <title  id="0.1.0.1.53.1.0">package:CT/CN0603</title>
        </g>
       </g>
      </g>
      <g  gorn="0.2.0.2" id="_x30_.1.0.2">
       <title  id="0.1.0.2.0">layer 25</title>
       <g  gorn="0.2.0.2.1" id="_x30_.1.0.2.1">
        <g  gorn="0.2.0.2.1.0" id="_x30_.1.0.2.1.0">
         <g transform="matrix(0, -1, 1, 0, 127.364, 138.997)">
          <g >
           <g >
            <g >
             <g  gorn="0.2.0.2.1.0.0.0.0.0" id="_x30_.1.0.2.1.0.0">
              <text  fill="#FFFFFF" font-family="'OCRA'" gorn="0.2.0.2.1.0.0.0.0.0.0" id="_x30_.1.0.2.1.0.0.0" font-size="3.3408">5V</text>
             </g>
            </g>
           </g>
          </g>
         </g>
        </g>
       </g>
       <g  gorn="0.2.0.2.2" id="_x30_.1.0.2.2">
        <title  id="0.1.0.2.2.0">text:A0</title>
        <g transform="matrix(-4.37114e-08, -1, 1, -4.37114e-08, 163.219, 138.997)">
         <g >
          <g >
           <g >
            <g  gorn="0.2.0.2.2.1.0.0.0" id="_x30_.1.0.2.2.1">
             <g transform="matrix(1, 0, 0, 1, 0, 6.10352e-05)">
              <g >
               <g >
                <g >
                 <text  fill="#FFFFFF" font-family="'OCRA'" gorn="0.2.0.2.2.1.0.0.0.0.0.0.0" id="_x30_.1.0.2.2.1.0" font-size="3.3408">A0</text>
                </g>
               </g>
              </g>
             </g>
            </g>
           </g>
          </g>
         </g>
        </g>
       </g>
       <g  gorn="0.2.0.2.3" id="_x30_.1.0.2.3">
        <g  gorn="0.2.0.2.3.0" id="_x30_.1.0.2.3.0">
         <g transform="matrix(1, 0, 0, 1, 175.672, 130.811)">
          <g >
           <g >
            <g >
             <g  gorn="0.2.0.2.3.0.0.0.0.0" id="_x30_.1.0.2.3.0.0">
              <g transform="matrix(1, 0, 0, 1, 0, 3.05176e-05)">
               <g >
                <g >
                 <g >
                  <text  fill="#FFFFFF" font-family="'OCRA'" gorn="0.2.0.2.3.0.0.0.0.0.0.0.0.0" id="_x30_.1.0.2.3.0.0.0" font-size="3.6749">ANALOG IN</text>
                 </g>
                </g>
               </g>
              </g>
             </g>
            </g>
           </g>
          </g>
         </g>
        </g>
       </g>
       <g  gorn="0.2.0.2.4" id="_x30_.1.0.2.4">
        <g  gorn="0.2.0.2.4.0" id="_x30_.1.0.2.4.0">
         <g transform="matrix(1, 0, 0, 1, 87.8933, 11.8426)">
          <g >
           <g >
            <g >
             <g  gorn="0.2.0.2.4.0.0.0.0.0" id="_x30_.1.0.2.4.0.0">
              <g  gorn="0.2.0.2.4.0.0.0.0.0.0" id="_x30_.1.0.2.4.0.0.0">
               <g transform="rotate(-90)">
                <g >
                 <g >
                  <g >
                   <g  gorn="0.2.0.2.4.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.0.2.4.0.0.0.0">
                    <g  gorn="0.2.0.2.4.0.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.0.2.4.0.0.0.0.0">
                     <g transform="matrix(1, 0, 0, 1, -11.0056, -0.9392)">
                      <g >
                       <g >
                        <g >
                         <g  gorn="0.2.0.2.4.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.0.2.4.0.0.0.0.0.0">
                          <g transform="matrix(1, 0, 0, 1, 6.10351e-05, 3.05176e-05)">
                           <g >
                            <g >
                             <g >
                              <text  fill="#FFFFFF" font-family="'OCRA'" gorn="0.2.0.2.4.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.0.2.4.0.0.0.0.0.0.0" font-size="3.75">AREF</text>
                             </g>
                            </g>
                           </g>
                          </g>
                         </g>
                        </g>
                       </g>
                      </g>
                     </g>
                    </g>
                   </g>
                  </g>
                 </g>
                </g>
               </g>
              </g>
             </g>
            </g>
           </g>
          </g>
         </g>
        </g>
       </g>
       <g  gorn="0.2.0.2.5" id="_x30_.1.0.2.5">
        <title  id="0.1.0.2.5.0">text:1</title>
        <g transform="matrix(1, 0, 0, 1, 191.131, 64.604)">
         <g >
          <g >
           <g >
            <g  gorn="0.2.0.2.5.1.0.0.0" id="_x30_.1.0.2.5.1">
             <g transform="matrix(1, 0, 0, 1, 6.10351e-05, 0)">
              <g >
               <g >
                <g >
                 <text  fill="#FFFFFF" font-family="'OCRA'" gorn="0.2.0.2.5.1.0.0.0.0.0.0.0" id="_x30_.1.0.2.5.1.0" font-size="4.176">1</text>
                </g>
               </g>
              </g>
             </g>
            </g>
           </g>
          </g>
         </g>
        </g>
       </g>
       <g  gorn="0.2.0.2.6" id="_x30_.1.0.2.6">
        <g  gorn="0.2.0.2.6.0" id="_x30_.1.0.2.6.0">
         <g transform="matrix(1, 0, 0, 1, 95.4223, 11.9146)">
          <g >
           <g >
            <g >
             <g  gorn="0.2.0.2.6.0.0.0.0.0" id="_x30_.1.0.2.6.0.0">
              <g  gorn="0.2.0.2.6.0.0.0.0.0.0" id="_x30_.1.0.2.6.0.0.0">
               <g transform="rotate(-90)">
                <g >
                 <g >
                  <g >
                   <g  gorn="0.2.0.2.6.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.0.2.6.0.0.0.0">
                    <g  gorn="0.2.0.2.6.0.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.0.2.6.0.0.0.0.0">
                     <g transform="matrix(1, 0, 0, 1, -8.246, -0.9399)">
                      <g >
                       <g >
                        <g >
                         <g  gorn="0.2.0.2.6.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.0.2.6.0.0.0.0.0.0">
                          <g transform="matrix(1, 0, 0, 1, -3.05176e-05, 3.05176e-05)">
                           <g >
                            <g >
                             <g >
                              <text  fill="#FFFFFF" font-family="'OCRA'" gorn="0.2.0.2.6.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.0.2.6.0.0.0.0.0.0.0" font-size="3.75">GND</text>
                             </g>
                            </g>
                           </g>
                          </g>
                         </g>
                        </g>
                       </g>
                      </g>
                     </g>
                    </g>
                   </g>
                  </g>
                 </g>
                </g>
               </g>
              </g>
             </g>
            </g>
           </g>
          </g>
         </g>
        </g>
       </g>
       <g  gorn="0.2.0.2.7" id="_x30_.1.0.2.7">
        <title  id="0.1.0.2.7.0">text:M.Banzi</title>
       </g>
       <g  gorn="0.2.0.2.8" id="_x30_.1.0.2.8">
        <title  id="0.1.0.2.8.0">text:D.Cuartielles</title>
       </g>
       <g  gorn="0.2.0.2.9" id="_x30_.1.0.2.9">
        <title  id="0.1.0.2.9.0">text:D.Mellis</title>
       </g>
       <g  gorn="0.2.0.2.10" id="_x30_.1.0.2.10">
        <title  id="0.1.0.2.10.0">text:TX</title>
        <g transform="matrix(1, 0, 0, 1, 84.5728, 49.3169)">
         <g >
          <g >
           <g >
            <g  gorn="0.2.0.2.10.1.0.0.0" id="_x30_.1.0.2.10.1">
             <g transform="matrix(1, 0, 0, 1, -6.10351e-05, 0)">
              <g >
               <g >
                <g >
                 <text  fill="#FFFFFF" font-family="'OCRA'" gorn="0.2.0.2.10.1.0.0.0.0.0.0.0" id="_x30_.1.0.2.10.1.0" font-size="4.6771">TX</text>
                </g>
               </g>
              </g>
             </g>
            </g>
           </g>
          </g>
         </g>
        </g>
       </g>
       <g  gorn="0.2.0.2.11" id="_x30_.1.0.2.11">
        <title  id="0.1.0.2.11.0">text:RX</title>
        <g transform="matrix(1, 0, 0, 1, 84.6489, 56.1567)">
         <g >
          <g >
           <g >
            <g  gorn="0.2.0.2.11.1.0.0.0" id="_x30_.1.0.2.11.1">
             <g transform="matrix(1, 0, 0, 1, 3.05176e-05, 3.05176e-05)">
              <g >
               <g >
                <g >
                 <text  fill="#FFFFFF" font-family="'OCRA'" gorn="0.2.0.2.11.1.0.0.0.0.0.0.0" id="_x30_.1.0.2.11.1.0" font-size="4.6771">RX</text>
                </g>
               </g>
              </g>
             </g>
            </g>
           </g>
          </g>
         </g>
        </g>
       </g>
       <g  gorn="0.2.0.2.12" id="_x30_.1.0.2.12">
        <title  id="0.1.0.2.12.0">text:G.Martino</title>
       </g>
       <g  gorn="0.2.0.2.13" id="_x30_.1.0.2.13">
        <title  id="0.1.0.2.13.0">text:T.Igoe</title>
       </g>
       <g  gorn="0.2.0.2.14" id="_x30_.1.0.2.14">
        <g  gorn="0.2.0.2.14.0" id="_x30_.1.0.2.14.0">
         <g transform="matrix(1, 0, 0, 1, 112.292, 138.6)">
          <g >
           <g >
            <g >
             <g  gorn="0.2.0.2.14.0.0.0.0.0" id="_x30_.1.0.2.14.0.0">
              <g  gorn="0.2.0.2.14.0.0.0.0.0.0" id="_x30_.1.0.2.14.0.0.0">
               <g transform="rotate(270)">
                <g >
                 <g >
                  <g >
                   <g  gorn="0.2.0.2.14.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.0.2.14.0.0.0.0">
                    <g  gorn="0.2.0.2.14.0.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.0.2.14.0.0.0.0.0">
                     <g transform="matrix(1, 0, 0, 1, -9.15527e-05, -0.000488281)">
                      <g >
                       <g >
                        <g >
                         <g  gorn="0.2.0.2.14.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.0.2.14.0.0.0.0.0.0">
                          <text  fill="#FFFFFF" font-family="'OCRA'" gorn="0.2.0.2.14.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.0.2.14.0.0.0.0.0.0.0" font-size="3.3408">RESET</text>
                         </g>
                        </g>
                       </g>
                      </g>
                     </g>
                    </g>
                   </g>
                  </g>
                 </g>
                </g>
               </g>
              </g>
             </g>
            </g>
           </g>
          </g>
         </g>
        </g>
       </g>
       <g  gorn="0.2.0.2.15" id="_x30_.1.0.2.15">
        <g  gorn="0.2.0.2.15.0" id="_x30_.1.0.2.15.0">
         <g transform="matrix(1, 0, 0, 1, 120.212, 138.96)">
          <g >
           <g >
            <g >
             <g  gorn="0.2.0.2.15.0.0.0.0.0" id="_x30_.1.0.2.15.0.0">
              <g  gorn="0.2.0.2.15.0.0.0.0.0.0" id="_x30_.1.0.2.15.0.0.0">
               <g transform="rotate(270)">
                <g >
                 <g >
                  <g >
                   <g  gorn="0.2.0.2.15.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.0.2.15.0.0.0.0">
                    <g  gorn="0.2.0.2.15.0.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.0.2.15.0.0.0.0.0">
                     <g transform="matrix(1, 0, 0, 1, 0.000534057, -0.000579834)">
                      <g >
                       <g >
                        <g >
                         <g  gorn="0.2.0.2.15.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.0.2.15.0.0.0.0.0.0">
                          <g transform="matrix(1, 0, 0, 1, 3.05176e-05, 6.10352e-05)">
                           <g >
                            <g >
                             <g >
                              <text  fill="#FFFFFF" font-family="'OCRA'" gorn="0.2.0.2.15.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.0.2.15.0.0.0.0.0.0.0" font-size="3.3408">3V3</text>
                             </g>
                            </g>
                           </g>
                          </g>
                         </g>
                        </g>
                       </g>
                      </g>
                     </g>
                    </g>
                   </g>
                  </g>
                 </g>
                </g>
               </g>
              </g>
             </g>
            </g>
           </g>
          </g>
         </g>
        </g>
       </g>
       <g  gorn="0.2.0.2.16" id="_x30_.1.0.2.16">
        <title  id="0.1.0.2.16.0">text:A1</title>
        <g transform="matrix(-4.37114e-08, -1, 1, -4.37114e-08, 170.418, 138.997)">
         <g >
          <g >
           <g >
            <g  gorn="0.2.0.2.16.1.0.0.0" id="_x30_.1.0.2.16.1">
             <text  fill="#FFFFFF" font-family="'OCRA'" gorn="0.2.0.2.16.1.0.0.0.0" id="_x30_.1.0.2.16.1.0" font-size="3.3408">A1</text>
            </g>
           </g>
          </g>
         </g>
        </g>
       </g>
       <g  gorn="0.2.0.2.17" id="_x30_.1.0.2.17">
        <title  id="0.1.0.2.17.0">text:A2</title>
        <g transform="matrix(-4.37114e-08, -1, 1, -4.37114e-08, 177.622, 138.997)">
         <g >
          <g >
           <g >
            <g  gorn="0.2.0.2.17.1.0.0.0" id="_x30_.1.0.2.17.1">
             <g transform="matrix(1, 0, 0, 1, 0, 6.10352e-05)">
              <g >
               <g >
                <g >
                 <text  fill="#FFFFFF" font-family="'OCRA'" gorn="0.2.0.2.17.1.0.0.0.0.0.0.0" id="_x30_.1.0.2.17.1.0" font-size="3.3408">A2</text>
                </g>
               </g>
              </g>
             </g>
            </g>
           </g>
          </g>
         </g>
        </g>
       </g>
       <g  gorn="0.2.0.2.18" id="_x30_.1.0.2.18">
        <title  id="0.1.0.2.18.0">text:A3</title>
        <g transform="matrix(-4.37114e-08, -1, 1, -4.37114e-08, 184.819, 138.997)">
         <g >
          <g >
           <g >
            <g  gorn="0.2.0.2.18.1.0.0.0" id="_x30_.1.0.2.18.1">
             <g transform="matrix(1, 0, 0, 1, 0, 0.00012207)">
              <g >
               <g >
                <g >
                 <text  fill="#FFFFFF" font-family="'OCRA'" gorn="0.2.0.2.18.1.0.0.0.0.0.0.0" id="_x30_.1.0.2.18.1.0" font-size="3.3408">A3</text>
                </g>
               </g>
              </g>
             </g>
            </g>
           </g>
          </g>
         </g>
        </g>
       </g>
       <g  gorn="0.2.0.2.19" id="_x30_.1.0.2.19">
        <title  id="0.1.0.2.19.0">text:A4</title>
        <g transform="matrix(-4.37114e-08, -1, 1, -4.37114e-08, 192.02, 138.997)">
         <g >
          <g >
           <g >
            <g  gorn="0.2.0.2.19.1.0.0.0" id="_x30_.1.0.2.19.1">
             <g transform="matrix(1, 0, 0, 1, 0, 6.10352e-05)">
              <g >
               <g >
                <g >
                 <text  fill="#FFFFFF" font-family="'OCRA'" gorn="0.2.0.2.19.1.0.0.0.0.0.0.0" id="_x30_.1.0.2.19.1.0" font-size="3.3408">A4</text>
                </g>
               </g>
              </g>
             </g>
            </g>
           </g>
          </g>
         </g>
        </g>
       </g>
       <g  gorn="0.2.0.2.20" id="_x30_.1.0.2.20">
        <title  id="0.1.0.2.20.0">text:A5</title>
        <g transform="matrix(-4.37114e-08, -1, 1, -4.37114e-08, 199.219, 138.997)">
         <g >
          <g >
           <g >
            <g  gorn="0.2.0.2.20.1.0.0.0" id="_x30_.1.0.2.20.1">
             <g transform="matrix(1, 0, 0, 1, 0, 0.00012207)">
              <g >
               <g >
                <g >
                 <text  fill="#FFFFFF" font-family="'OCRA'" gorn="0.2.0.2.20.1.0.0.0.0.0.0.0" id="_x30_.1.0.2.20.1.0" font-size="3.3408">A5</text>
                </g>
               </g>
              </g>
             </g>
            </g>
           </g>
          </g>
         </g>
        </g>
       </g>
       <g  gorn="0.2.0.2.21" id="_x30_.1.0.2.21">
        <g  gorn="0.2.0.2.21.0" id="_x30_.1.0.2.21.0">
         <g transform="matrix(-4.37114e-08, -1, 1, -4.37114e-08, 148.965, 138.997)">
          <g >
           <g >
            <g >
             <g  gorn="0.2.0.2.21.0.0.0.0.0" id="_x30_.1.0.2.21.0.0">
              <g transform="matrix(1, 0, 0, 1, 0, 0.00012207)">
               <g >
                <g >
                 <g >
                  <text  fill="#FFFFFF" font-family="'OCRA'" gorn="0.2.0.2.21.0.0.0.0.0.0.0.0.0" id="_x30_.1.0.2.21.0.0.0" font-size="3.3408">VIN</text>
                 </g>
                </g>
               </g>
              </g>
             </g>
            </g>
           </g>
          </g>
         </g>
        </g>
       </g>
       <g  gorn="0.2.0.2.22" id="_x30_.1.0.2.22">
        <g  gorn="0.2.0.2.22.0" id="_x30_.1.0.2.22.0">
         <g transform="matrix(-4.37114e-08, -1, 1, -4.37114e-08, 134.561, 138.997)">
          <g >
           <g >
            <g >
             <g  gorn="0.2.0.2.22.0.0.0.0.0" id="_x30_.1.0.2.22.0.0">
              <g transform="matrix(1, 0, 0, 1, 0, 0.00012207)">
               <g >
                <g >
                 <g >
                  <text  fill="#FFFFFF" font-family="'OCRA'" gorn="0.2.0.2.22.0.0.0.0.0.0.0.0.0" id="_x30_.1.0.2.22.0.0.0" font-size="3.3408">GND</text>
                 </g>
                </g>
               </g>
              </g>
             </g>
            </g>
           </g>
          </g>
         </g>
        </g>
       </g>
       <g  gorn="0.2.0.2.23" id="_x30_.1.0.2.23">
        <g  gorn="0.2.0.2.23.0" id="_x30_.1.0.2.23.0">
         <g transform="matrix(-4.37114e-08, -1, 1, -4.37114e-08, 141.557, 138.96)">
          <g >
           <g >
            <g >
             <g  gorn="0.2.0.2.23.0.0.0.0.0" id="_x30_.1.0.2.23.0.0">
              <g transform="matrix(1, 0, 0, 1, 3.05176e-05, 0.00012207)">
               <g >
                <g >
                 <g >
                  <text  fill="#FFFFFF" font-family="'OCRA'" gorn="0.2.0.2.23.0.0.0.0.0.0.0.0.0" id="_x30_.1.0.2.23.0.0.0" font-size="3.3408">GND</text>
                 </g>
                </g>
               </g>
              </g>
             </g>
            </g>
           </g>
          </g>
         </g>
        </g>
       </g>
       <g  gorn="0.2.0.2.24" id="_x30_.1.0.2.24">
        <title  id="0.1.0.2.24.0">text:[#=PWM]</title>
        <g transform="matrix(1, 0, 0, 1, 145.157, 27.2759)">
         <g >
          <g >
           <g >
            <g  gorn="0.2.0.2.24.1.0.0.0" id="_x30_.1.0.2.24.1">
             <g transform="matrix(1, 0, 0, 1, 0.00012207, -3.05176e-05)">
              <g >
               <g >
                <g >
                 <text  fill="#FFFFFF" font-family="'OCRA'" gorn="0.2.0.2.24.1.0.0.0.0.0.0.0" id="_x30_.1.0.2.24.1.0" font-size="3.6749">DIGITAL (PWM=</text>
                </g>
               </g>
              </g>
             </g>
            </g>
           </g>
          </g>
         </g>
        </g>
        <g transform="matrix(1, 0, 0, 1, 179.696, 27.2759)">
         <g >
          <g >
           <g >
            <g  gorn="0.2.0.2.24.2.0.0.0" id="_x30_.1.0.2.24.2"/>
           </g>
          </g>
         </g>
        </g>
        <g transform="matrix(1, 0, 0, 1, 182.028, 27.2759)">
         <g >
          <g >
           <g >
            <g  gorn="0.2.0.2.24.3.0.0.0" id="_x30_.1.0.2.24.3">
             <g transform="matrix(1, 0, 0, 1, 0.00012207, -3.05176e-05)">
              <g >
               <g >
                <g >
                 <text  fill="#FFFFFF" font-family="'OCRA'" gorn="0.2.0.2.24.3.0.0.0.0.0.0.0" id="_x30_.1.0.2.24.3.0" font-size="3.6749">)</text>
                </g>
               </g>
              </g>
             </g>
            </g>
           </g>
          </g>
         </g>
        </g>
       </g>
       <g  gorn="0.2.0.2.25" id="_x30_.1.0.2.25">
        <g  gorn="0.2.0.2.25.0" id="_x30_.1.0.2.25.0">
         <g transform="matrix(1, 0, 0, 1, 123.452, 22.68)">
          <g >
           <g >
            <g >
             <g  gorn="0.2.0.2.25.0.0.0.0.0" id="_x30_.1.0.2.25.0.0">
              <g  gorn="0.2.0.2.25.0.0.0.0.0.0" id="_x30_.1.0.2.25.0.0.0">
               <g transform="rotate(270)">
                <g >
                 <g >
                  <g >
                   <g  gorn="0.2.0.2.25.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.0.2.25.0.0.0.0">
                    <g  gorn="0.2.0.2.25.0.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.0.2.25.0.0.0.0.0">
                     <g  gorn="0.2.0.2.25.0.0.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.0.2.25.0.0.0.0.0.0" enable-background="new    ">
                      <path  fill="#FFFFFF" gorn="0.2.0.2.25.0.0.0.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.0.2.25.0.0.0.0.0.0.0" d="M1.565,-1.051c-0.021,-0.5,0.25,-0.756,0.596,-0.756c0.21,0,0.37,0.064,0.706,0.225c0.255,0.121,0.44,0.211,0.625,0.211c0.181,0,0.266,-0.145,0.271,-0.42l0.3,0C4.088,-1.23,3.798,-1.035,3.487,-1.035c-0.2,0,-0.38,-0.061,-0.726,-0.221C2.526,-1.371,2.341,-1.477,2.16,-1.477s-0.29,0.125,-0.3,0.426L1.565,-1.051z"/>
                     </g>
                    </g>
                   </g>
                  </g>
                 </g>
                </g>
               </g>
              </g>
             </g>
            </g>
           </g>
          </g>
         </g>
        </g>
       </g>
       <g  gorn="0.2.0.2.26" id="_x30_.1.0.2.26">
        <g  gorn="0.2.0.2.26.0" id="_x30_.1.0.2.26.0">
         <g transform="matrix(1, 0, 0, 1, 123.452, 22.68)">
          <g >
           <g >
            <g >
             <g  gorn="0.2.0.2.26.0.0.0.0.0" id="_x30_.1.0.2.26.0.0">
              <g  gorn="0.2.0.2.26.0.0.0.0.0.0" id="_x30_.1.0.2.26.0.0.0">
               <g transform="rotate(270)">
                <g >
                 <g >
                  <g >
                   <g  gorn="0.2.0.2.26.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.0.2.26.0.0.0.0">
                    <g  gorn="0.2.0.2.26.0.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.0.2.26.0.0.0.0.0">
                     <g  gorn="0.2.0.2.26.0.0.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.0.2.26.0.0.0.0.0.0" enable-background="new    ">
                      <path  fill="#FFFFFF" gorn="0.2.0.2.26.0.0.0.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.0.2.26.0.0.0.0.0.0.0" d="M1.565,-8.473c-0.021,-0.5,0.25,-0.756,0.596,-0.756c0.21,0,0.37,0.064,0.706,0.225c0.255,0.121,0.44,0.211,0.625,0.211c0.181,0,0.266,-0.145,0.271,-0.42l0.3,0c0.025,0.561,-0.265,0.756,-0.576,0.756c-0.2,0,-0.38,-0.061,-0.726,-0.221C2.526,-8.793,2.341,-8.899,2.16,-8.899s-0.29,0.125,-0.3,0.426L1.565,-8.473L1.565,-8.473z"/>
                     </g>
                    </g>
                   </g>
                  </g>
                 </g>
                </g>
               </g>
              </g>
             </g>
            </g>
           </g>
          </g>
         </g>
        </g>
       </g>
       <g  gorn="0.2.0.2.27" id="_x30_.1.0.2.27">
        <g  gorn="0.2.0.2.27.0" id="_x30_.1.0.2.27.0">
         <g transform="matrix(1, 0, 0, 1, 163.412, 19.08)">
          <g >
           <g >
            <g >
             <g  gorn="0.2.0.2.27.0.0.0.0.0" id="_x30_.1.0.2.27.0.0">
              <g  gorn="0.2.0.2.27.0.0.0.0.0.0" id="_x30_.1.0.2.27.0.0.0">
               <g transform="rotate(270)">
                <g >
                 <g >
                  <g >
                   <g  gorn="0.2.0.2.27.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.0.2.27.0.0.0.0">
                    <g  gorn="0.2.0.2.27.0.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.0.2.27.0.0.0.0.0">
                     <g  gorn="0.2.0.2.27.0.0.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.0.2.27.0.0.0.0.0.0" enable-background="new    ">
                      <path  fill="#FFFFFF" gorn="0.2.0.2.27.0.0.0.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.0.2.27.0.0.0.0.0.0.0" d="M0.994,-1.05c-0.02,-0.502,0.25,-0.756,0.596,-0.756c0.21,0,0.37,0.064,0.706,0.225C2.55,-1.46,2.735,-1.37,2.92,-1.37c0.181,0,0.266,-0.146,0.271,-0.422l0.3,0C3.516,-1.23,3.226,-1.036,2.915,-1.036c-0.2,0,-0.38,-0.059,-0.726,-0.219c-0.234,-0.115,-0.42,-0.221,-0.6,-0.221c-0.18,0,-0.29,0.125,-0.3,0.426L0.994,-1.05z"/>
                     </g>
                    </g>
                   </g>
                  </g>
                 </g>
                </g>
               </g>
              </g>
             </g>
            </g>
           </g>
          </g>
         </g>
        </g>
       </g>
       <g  gorn="0.2.0.2.28" id="_x30_.1.0.2.28">
        <title  id="0.1.0.2.28.0">text:#</title>
        <g transform="matrix(1, 0, 0, 1, 177.812, 19.08)">
         <g >
          <g >
           <g >
            <g  gorn="0.2.0.2.28.1.0.0.0" id="_x30_.1.0.2.28.1">
             <g  gorn="0.2.0.2.28.1.0.0.0.0" id="_x30_.1.0.2.28.1.0">
              <g transform="rotate(270)">
               <g >
                <g >
                 <g >
                  <g  gorn="0.2.0.2.28.1.0.0.0.0.0.0.0.0" id="_x30_.1.0.2.28.1.0.0">
                   <g  gorn="0.2.0.2.28.1.0.0.0.0.0.0.0.0.0" id="_x30_.1.0.2.28.1.0.0.0">
                    <g  gorn="0.2.0.2.28.1.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.0.2.28.1.0.0.0.0" enable-background="new    ">
                     <path  fill="#FFFFFF" gorn="0.2.0.2.28.1.0.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.0.2.28.1.0.0.0.0.0" d="M0.994,-1.051c-0.02,-0.501,0.25,-0.757,0.596,-0.757c0.21,0,0.37,0.063,0.706,0.226C2.55,-1.461,2.735,-1.371,2.92,-1.371c0.181,0,0.266,-0.146,0.271,-0.421l0.3,0c0.025,0.561,-0.265,0.756,-0.576,0.756c-0.2,0,-0.38,-0.061,-0.726,-0.22c-0.235,-0.115,-0.42,-0.222,-0.601,-0.222c-0.181,0,-0.29,0.125,-0.3,0.427L0.994,-1.051z"/>
                    </g>
                   </g>
                  </g>
                 </g>
                </g>
               </g>
              </g>
             </g>
            </g>
           </g>
          </g>
         </g>
        </g>
       </g>
       <g  gorn="0.2.0.2.29" id="_x30_.1.0.2.29">
        <g  gorn="0.2.0.2.29.0" id="_x30_.1.0.2.29.0">
         <g transform="matrix(1, 0, 0, 1, 156.572, 19.08)">
          <g >
           <g >
            <g >
             <g  gorn="0.2.0.2.29.0.0.0.0.0" id="_x30_.1.0.2.29.0.0">
              <g  gorn="0.2.0.2.29.0.0.0.0.0.0" id="_x30_.1.0.2.29.0.0.0">
               <g transform="rotate(270)">
                <g >
                 <g >
                  <g >
                   <g  gorn="0.2.0.2.29.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.0.2.29.0.0.0.0">
                    <g  gorn="0.2.0.2.29.0.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.0.2.29.0.0.0.0.0">
                     <g  gorn="0.2.0.2.29.0.0.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.0.2.29.0.0.0.0.0.0" enable-background="new    ">
                      <path  fill="#FFFFFF" gorn="0.2.0.2.29.0.0.0.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.0.2.29.0.0.0.0.0.0.0" d="M0.994,-1.05c-0.02,-0.502,0.25,-0.756,0.596,-0.756c0.21,0,0.37,0.064,0.706,0.225C2.55,-1.46,2.735,-1.37,2.92,-1.37c0.181,0,0.266,-0.146,0.271,-0.422l0.3,0c0.025,0.561,-0.265,0.756,-0.576,0.756c-0.2,0,-0.38,-0.059,-0.726,-0.219c-0.234,-0.115,-0.42,-0.221,-0.6,-0.221c-0.18,0,-0.29,0.125,-0.3,0.426L0.994,-1.05z"/>
                     </g>
                    </g>
                   </g>
                  </g>
                 </g>
                </g>
               </g>
              </g>
             </g>
            </g>
           </g>
          </g>
         </g>
        </g>
       </g>
       <g  gorn="0.2.0.2.30" id="_x30_.1.0.2.30">
        <g  gorn="0.2.0.2.30.0" id="_x30_.1.0.2.30.0">
         <g transform="matrix(1, 0, 0, 1, 130.292, 19.08)">
          <g >
           <g >
            <g >
             <g  gorn="0.2.0.2.30.0.0.0.0.0" id="_x30_.1.0.2.30.0.0">
              <g  gorn="0.2.0.2.30.0.0.0.0.0.0" id="_x30_.1.0.2.30.0.0.0">
               <g transform="rotate(270)">
                <g >
                 <g >
                  <g >
                   <g  gorn="0.2.0.2.30.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.0.2.30.0.0.0.0">
                    <g  gorn="0.2.0.2.30.0.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.0.2.30.0.0.0.0.0">
                     <g  gorn="0.2.0.2.30.0.0.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.0.2.30.0.0.0.0.0.0" enable-background="new    ">
                      <path  fill="#FFFFFF" gorn="0.2.0.2.30.0.0.0.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.0.2.30.0.0.0.0.0.0.0" d="M0.994,-1.051c-0.02,-0.5,0.25,-0.756,0.596,-0.756c0.21,0,0.37,0.064,0.706,0.225C2.55,-1.461,2.735,-1.372,2.92,-1.372c0.181,0,0.266,-0.146,0.271,-0.42l0.3,0c0.025,0.561,-0.265,0.756,-0.576,0.756c-0.2,0,-0.38,-0.063,-0.726,-0.221C1.954,-1.372,1.769,-1.48,1.588,-1.48c-0.181,0,-0.29,0.125,-0.3,0.429L0.994,-1.051L0.994,-1.051z"/>
                     </g>
                    </g>
                   </g>
                  </g>
                 </g>
                </g>
               </g>
              </g>
             </g>
            </g>
           </g>
          </g>
         </g>
        </g>
       </g>
       <g  gorn="0.2.0.2.31" id="_x30_.1.0.2.31">
        <g  gorn="0.2.0.2.31.0" id="_x30_.1.0.2.31.0">
         <title  id="0.1.0.2.31.0.0">text:Arduino</title>
         <g transform="matrix(1, 0, 0, 1, 109.016, 55.1792)">
          <g >
           <g >
            <g >
             <g  gorn="0.2.0.2.31.0.1.0.0.0" id="_x30_.1.0.2.31.0.1">
              <g transform="matrix(1, 0, 0, 1, 6.10351e-05, 0)">
               <g >
                <g >
                 <g >
                  <text  fill="#FFFFFF" font-family="'OCRA'" gorn="0.2.0.2.31.0.1.0.0.0.0.0.0.0" id="_x30_.1.0.2.31.0.1.0" font-size="6.1209">Arduino</text>
                 </g>
                </g>
               </g>
              </g>
             </g>
            </g>
           </g>
          </g>
         </g>
        </g>
        <g  gorn="0.2.0.2.31.1" id="_x30_.1.0.2.31.1">
         <title  id="0.1.0.2.31.1.0">text:TM</title>
         <g transform="matrix(1, 0, 0, 1, 138.998, 51.5815)">
          <g >
           <g >
            <g >
             <g  gorn="0.2.0.2.31.1.1.0.0.0" id="_x30_.1.0.2.31.1.1">
              <g transform="matrix(1, 0, 0, 1, 0, 3.05176e-05)">
               <g >
                <g >
                 <g >
                  <text  fill="#FFFFFF" font-family="'OCRA'" gorn="0.2.0.2.31.1.1.0.0.0.0.0.0.0" id="_x30_.1.0.2.31.1.1.0" font-size="2.2258">TM</text>
                 </g>
                </g>
               </g>
              </g>
             </g>
            </g>
           </g>
          </g>
         </g>
        </g>
       </g>
       <g  gorn="0.2.0.2.32" id="_x30_.1.0.2.32">
        <g  gorn="0.2.0.2.32.0" id="_x30_.1.0.2.32.0">
         <g transform="matrix(1, 0, 0, 1, 106.172, 138.6)">
          <g >
           <g >
            <g >
             <g  gorn="0.2.0.2.32.0.0.0.0.0" id="_x30_.1.0.2.32.0.0">
              <g  gorn="0.2.0.2.32.0.0.0.0.0.0" id="_x30_.1.0.2.32.0.0.0">
               <g transform="rotate(270)">
                <g >
                 <g >
                  <g >
                   <g  gorn="0.2.0.2.32.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.0.2.32.0.0.0.0">
                    <g  gorn="0.2.0.2.32.0.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.0.2.32.0.0.0.0.0">
                     <g transform="matrix(1, 0, 0, 1, -9.15527e-05, -0.00012207)">
                      <g >
                       <g >
                        <g >
                         <g  gorn="0.2.0.2.32.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.0.2.32.0.0.0.0.0.0">
                          <g transform="matrix(1, 0, 0, 1, 0, 6.10352e-05)">
                           <g >
                            <g >
                             <g >
                              <text  fill="#FFFFFF" font-family="'OCRA'" gorn="0.2.0.2.32.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.0.2.32.0.0.0.0.0.0.0" font-size="3.3408">IOREF</text>
                             </g>
                            </g>
                           </g>
                          </g>
                         </g>
                        </g>
                       </g>
                      </g>
                     </g>
                    </g>
                   </g>
                  </g>
                 </g>
                </g>
               </g>
              </g>
             </g>
            </g>
           </g>
          </g>
         </g>
        </g>
       </g>
       <g  gorn="0.2.0.2.33" id="_x30_.1.0.2.33">
        <title  id="0.1.0.2.33.0">text:SDA</title>
       </g>
       <g  gorn="0.2.0.2.34" id="_x30_.1.0.2.34">
        <title  id="0.1.0.2.34.0">text:SCL</title>
       </g>
       <g  gorn="0.2.0.2.35" id="_x30_.1.0.2.35">
        <title  id="0.1.0.2.35.0">element:AD</title>
        <g  gorn="0.2.0.2.35.1" id="_x30_.1.0.2.35.1">
         <title  id="0.1.0.2.35.1.0">package:1X06</title>
        </g>
       </g>
       <g  gorn="0.2.0.2.36" id="_x30_.1.0.2.36">
        <title  id="0.1.0.2.36.0">element:C1</title>
        <g  gorn="0.2.0.2.36.1" id="_x30_.1.0.2.36.1">
         <title  id="0.1.0.2.36.1.0">package:C0603-ROUND</title>
        </g>
       </g>
       <g  gorn="0.2.0.2.37" id="_x30_.1.0.2.37">
        <title  id="0.1.0.2.37.0">element:C2</title>
        <g  gorn="0.2.0.2.37.1" id="_x30_.1.0.2.37.1">
         <title  id="0.1.0.2.37.1.0">package:C0603-ROUND</title>
        </g>
       </g>
       <g  gorn="0.2.0.2.38" id="_x30_.1.0.2.38">
        <title  id="0.1.0.2.38.0">element:C3</title>
        <g  gorn="0.2.0.2.38.1" id="_x30_.1.0.2.38.1">
         <title  id="0.1.0.2.38.1.0">package:C0603-ROUND</title>
        </g>
       </g>
       <g  gorn="0.2.0.2.39" id="_x30_.1.0.2.39">
        <title  id="0.1.0.2.39.0">element:C4</title>
        <g  gorn="0.2.0.2.39.1" id="_x30_.1.0.2.39.1">
         <title  id="0.1.0.2.39.1.0">package:C0603-ROUND</title>
        </g>
       </g>
       <g  gorn="0.2.0.2.40" id="_x30_.1.0.2.40">
        <title  id="0.1.0.2.40.0">element:C5</title>
        <g  gorn="0.2.0.2.40.1" id="_x30_.1.0.2.40.1">
         <title  id="0.1.0.2.40.1.0">package:C0603-ROUND</title>
        </g>
       </g>
       <g  gorn="0.2.0.2.41" id="_x30_.1.0.2.41">
        <title  id="0.1.0.2.41.0">element:C6</title>
        <g  gorn="0.2.0.2.41.1" id="_x30_.1.0.2.41.1">
         <title  id="0.1.0.2.41.1.0">package:C0603-ROUND</title>
        </g>
       </g>
       <g  gorn="0.2.0.2.42" id="_x30_.1.0.2.42">
        <title  id="0.1.0.2.42.0">element:C7</title>
        <g  gorn="0.2.0.2.42.1" id="_x30_.1.0.2.42.1">
         <title  id="0.1.0.2.42.1.0">package:C0603-ROUND</title>
        </g>
       </g>
       <g  gorn="0.2.0.2.43" id="_x30_.1.0.2.43">
        <title  id="0.1.0.2.43.0">element:C8</title>
        <g  gorn="0.2.0.2.43.1" id="_x30_.1.0.2.43.1">
         <title  id="0.1.0.2.43.1.0">package:C0603-ROUND</title>
        </g>
       </g>
       <g  gorn="0.2.0.2.44" id="_x30_.1.0.2.44">
        <title  id="0.1.0.2.44.0">element:C9</title>
        <g  gorn="0.2.0.2.44.1" id="_x30_.1.0.2.44.1">
         <title  id="0.1.0.2.44.1.0">package:C0603-ROUND</title>
        </g>
       </g>
       <g  gorn="0.2.0.2.45" id="_x30_.1.0.2.45">
        <title  id="0.1.0.2.45.0">element:C11</title>
        <g  gorn="0.2.0.2.45.1" id="_x30_.1.0.2.45.1">
         <title  id="0.1.0.2.45.1.0">package:C0603-ROUND</title>
        </g>
       </g>
       <g  gorn="0.2.0.2.46" id="_x30_.1.0.2.46">
        <title  id="0.1.0.2.46.0">element:D1</title>
        <g  gorn="0.2.0.2.46.1" id="_x30_.1.0.2.46.1">
         <title  id="0.1.0.2.46.1.0">package:SMB</title>
        </g>
       </g>
       <g  gorn="0.2.0.2.47" id="_x30_.1.0.2.47">
        <title  id="0.1.0.2.47.0">element:D2</title>
        <g  gorn="0.2.0.2.47.1" id="_x30_.1.0.2.47.1">
         <title  id="0.1.0.2.47.1.0">package:MINIMELF</title>
        </g>
       </g>
       <g  gorn="0.2.0.2.48" id="_x30_.1.0.2.48">
        <title  id="0.1.0.2.48.0">element:D3</title>
        <g  gorn="0.2.0.2.48.1" id="_x30_.1.0.2.48.1">
         <title  id="0.1.0.2.48.1.0">package:MINIMELF</title>
        </g>
       </g>
       <g  gorn="0.2.0.2.49" id="_x30_.1.0.2.49">
        <title  id="0.1.0.2.49.0">element:F1</title>
        <g  gorn="0.2.0.2.49.1" id="_x30_.1.0.2.49.1">
         <title  id="0.1.0.2.49.1.0">package:L1812</title>
        </g>
       </g>
       <g  gorn="0.2.0.2.50" id="_x30_.1.0.2.50">
        <title  id="0.1.0.2.50.0">element:FD1</title>
        <g  gorn="0.2.0.2.50.1" id="_x30_.1.0.2.50.1">
         <title  id="0.1.0.2.50.1.0">package:FIDUCIA-MOUNT</title>
        </g>
       </g>
       <g  gorn="0.2.0.2.51" id="_x30_.1.0.2.51">
        <title  id="0.1.0.2.51.0">element:FD2</title>
        <g  gorn="0.2.0.2.51.1" id="_x30_.1.0.2.51.1">
         <title  id="0.1.0.2.51.1.0">package:FIDUCIA-MOUNT</title>
        </g>
       </g>
       <g  gorn="0.2.0.2.52" id="_x30_.1.0.2.52">
        <title  id="0.1.0.2.52.0">element:FD3</title>
        <g  gorn="0.2.0.2.52.1" id="_x30_.1.0.2.52.1">
         <title  id="0.1.0.2.52.1.0">package:FIDUCIA-MOUNT</title>
        </g>
       </g>
       <g  gorn="0.2.0.2.53" id="_x30_.1.0.2.53">
        <title  id="0.1.0.2.53.0">element:GROUND</title>
        <g  gorn="0.2.0.2.53.1" id="_x30_.1.0.2.53.1">
         <title  id="0.1.0.2.53.1.0">package:SJ</title>
        </g>
       </g>
       <g  gorn="0.2.0.2.54" id="_x30_.1.0.2.54">
        <title  id="0.1.0.2.54.0">element:ICSP</title>
        <g  gorn="0.2.0.2.54.1" id="_x30_.1.0.2.54.1">
         <title  id="0.1.0.2.54.1.0">text:ICSP</title>
         <g transform="matrix(1, 0, 0, 1, 194.553, 82.3349)">
          <g >
           <g >
            <g >
             <g  gorn="0.2.0.2.54.1.1.0.0.0" id="_x30_.1.0.2.54.1.1">
              <g  gorn="0.2.0.2.54.1.1.0.0.0.0" id="_x30_.1.0.2.54.1.1.0">
               <g transform="rotate(270)">
                <g >
                 <g >
                  <g >
                   <g  gorn="0.2.0.2.54.1.1.0.0.0.0.0.0.0.0" id="_x30_.1.0.2.54.1.1.0.0">
                    <g  gorn="0.2.0.2.54.1.1.0.0.0.0.0.0.0.0.0" id="_x30_.1.0.2.54.1.1.0.0.0">
                     <g transform="matrix(1, 0, 0, 1, -0.7808, -0.783)">
                      <g >
                       <g >
                        <g >
                         <g  gorn="0.2.0.2.54.1.1.0.0.0.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.0.2.54.1.1.0.0.0.0">
                          <g transform="matrix(1, 0, 0, 1, -3.05176e-05, 0.00012207)">
                           <g >
                            <g >
                             <g >
                              <text  fill="#FFFFFF" font-family="'OCRA'" gorn="0.2.0.2.54.1.1.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.0.2.54.1.1.0.0.0.0.0" font-size="4.176">ICSP</text>
                             </g>
                            </g>
                           </g>
                          </g>
                         </g>
                        </g>
                       </g>
                      </g>
                     </g>
                    </g>
                   </g>
                  </g>
                 </g>
                </g>
               </g>
              </g>
             </g>
            </g>
           </g>
          </g>
         </g>
        </g>
        <g  gorn="0.2.0.2.54.2" id="_x30_.1.0.2.54.2">
         <title  id="0.1.0.2.54.2.0">package:2X03</title>
        </g>
       </g>
       <g  gorn="0.2.0.2.55" id="_x30_.1.0.2.55">
        <title  id="0.1.0.2.55.0">element:ICSP</title>
        <g  gorn="0.2.0.2.55.1" id="_x30_.1.0.2.55.1">
         <title  id="0.1.0.2.55.1.0">text:ICSP</title>
         <g transform="matrix(1, 0, 0, 1, 194.553, 82.3349)">
          <g >
           <g >
            <g >
             <g  gorn="0.2.0.2.55.1.1.0.0.0" id="_x30_.1.0.2.55.1.1">
              <g  gorn="0.2.0.2.55.1.1.0.0.0.0" id="_x30_.1.0.2.55.1.1.0">
               <g transform="rotate(270)">
                <g >
                 <g >
                  <g >
                   <g  gorn="0.2.0.2.55.1.1.0.0.0.0.0.0.0.0" id="_x30_.1.0.2.55.1.1.0.0">
                    <g  gorn="0.2.0.2.55.1.1.0.0.0.0.0.0.0.0.0" id="_x30_.1.0.2.55.1.1.0.0.0">
                     <g transform="matrix(0, 1, -1, 0, 50.2719, -135.181)">
                      <g >
                       <g >
                        <g >
                         <g  gorn="0.2.0.2.55.1.1.0.0.0.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.0.2.55.1.1.0.0.0.0">
                          <g transform="matrix(1, 0, 0, 1, 6.10351e-05, 0)">
                           <g >
                            <g >
                             <g >
                              <text  fill="#FFFFFF" font-family="'OCRA'" gorn="0.2.0.2.55.1.1.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.0.2.55.1.1.0.0.0.0.0" font-size="4.176">ICSP2</text>
                             </g>
                            </g>
                           </g>
                          </g>
                         </g>
                        </g>
                       </g>
                      </g>
                     </g>
                    </g>
                   </g>
                  </g>
                 </g>
                </g>
               </g>
              </g>
             </g>
            </g>
           </g>
          </g>
         </g>
        </g>
        <g  gorn="0.2.0.2.55.2" id="_x30_.1.0.2.55.2">
         <title  id="0.1.0.2.55.2.0">package:2X03</title>
        </g>
       </g>
       <g  gorn="0.2.0.2.56" id="_x30_.1.0.2.56">
        <title  id="0.1.0.2.56.0">element:ICSP1</title>
        <g  gorn="0.2.0.2.56.1" id="_x30_.1.0.2.56.1">
         <title  id="0.1.0.2.56.1.0">package:2X03</title>
        </g>
       </g>
       <g  gorn="0.2.0.2.57" id="_x30_.1.0.2.57">
        <title  id="0.1.0.2.57.0">element:IOH</title>
        <g  gorn="0.2.0.2.57.1" id="_x30_.1.0.2.57.1">
         <title  id="0.1.0.2.57.1.0">package:1X10@1</title>
        </g>
       </g>
       <g  gorn="0.2.0.2.58" id="_x30_.1.0.2.58">
        <title  id="0.1.0.2.58.0">element:IOL</title>
        <g  gorn="0.2.0.2.58.1" id="_x30_.1.0.2.58.1">
         <title  id="0.1.0.2.58.1.0">package:1X08</title>
        </g>
       </g>
       <g  gorn="0.2.0.2.59" id="_x30_.1.0.2.59">
        <title  id="0.1.0.2.59.0">element:JP2</title>
        <g  gorn="0.2.0.2.59.1" id="_x30_.1.0.2.59.1">
         <title  id="0.1.0.2.59.1.0">package:2X02</title>
        </g>
       </g>
       <g  gorn="0.2.0.2.60" id="_x30_.1.0.2.60">
        <title  id="0.1.0.2.60.0">element:L</title>
        <g  gorn="0.2.0.2.60.1" id="_x30_.1.0.2.60.1">
         <title  id="0.1.0.2.60.1.0">package:CHIP-LED0805</title>
        </g>
       </g>
       <g  gorn="0.2.0.2.61" id="_x30_.1.0.2.61">
        <title  id="0.1.0.2.61.0">element:L1</title>
        <g  gorn="0.2.0.2.61.1" id="_x30_.1.0.2.61.1">
         <title  id="0.1.0.2.61.1.0">package:0805</title>
        </g>
       </g>
       <g  gorn="0.2.0.2.62" id="_x30_.1.0.2.62">
        <title  id="0.1.0.2.62.0">element:ON</title>
        <g  gorn="0.2.0.2.62.1" id="_x30_.1.0.2.62.1">
         <title  id="0.1.0.2.62.1.0">text:ON</title>
         <g transform="matrix(1, 0, 0, 1, 190.772, 49.3208)">
          <g >
           <g >
            <g >
             <g  gorn="0.2.0.2.62.1.1.0.0.0" id="_x30_.1.0.2.62.1.1">
              <text  fill="#FFFFFF" font-family="'OCRA'" gorn="0.2.0.2.62.1.1.0.0.0.0" id="_x30_.1.0.2.62.1.1.0" font-size="4.6771">ON</text>
             </g>
            </g>
           </g>
          </g>
         </g>
        </g>
        <g  gorn="0.2.0.2.62.2" id="_x30_.1.0.2.62.2">
         <title  id="0.1.0.2.62.2.0">package:CHIP-LED0805</title>
        </g>
       </g>
       <g  gorn="0.2.0.2.63" id="_x30_.1.0.2.63">
        <title  id="0.1.0.2.63.0">element:PC1</title>
        <g  gorn="0.2.0.2.63.1" id="_x30_.1.0.2.63.1">
         <title  id="0.1.0.2.63.1.0">package:PANASONIC_D</title>
        </g>
       </g>
       <g  gorn="0.2.0.2.64" id="_x30_.1.0.2.64">
        <title  id="0.1.0.2.64.0">element:PC2</title>
        <g  gorn="0.2.0.2.64.1" id="_x30_.1.0.2.64.1">
         <title  id="0.1.0.2.64.1.0">package:PANASONIC_D</title>
        </g>
       </g>
       <g  gorn="0.2.0.2.65" id="_x30_.1.0.2.65">
        <title  id="0.1.0.2.65.0">element:R1</title>
        <g  gorn="0.2.0.2.65.1" id="_x30_.1.0.2.65.1">
         <title  id="0.1.0.2.65.1.0">package:R0603-ROUND</title>
        </g>
       </g>
       <g  gorn="0.2.0.2.66" id="_x30_.1.0.2.66">
        <title  id="0.1.0.2.66.0">element:R2</title>
        <g  gorn="0.2.0.2.66.1" id="_x30_.1.0.2.66.1">
         <title  id="0.1.0.2.66.1.0">package:R0603-ROUND</title>
        </g>
       </g>
       <g  gorn="0.2.0.2.67" id="_x30_.1.0.2.67">
        <title  id="0.1.0.2.67.0">element:RESET</title>
        <g  gorn="0.2.0.2.67.1" id="_x30_.1.0.2.67.1">
         <title  id="0.1.0.2.67.1.0">package:TS42</title>
        </g>
       </g>
       <g  gorn="0.2.0.2.68" id="_x30_.1.0.2.68">
        <title  id="0.1.0.2.68.0">element:RESET-EN</title>
        <g  gorn="0.2.0.2.68.1" id="_x30_.1.0.2.68.1">
         <title  id="0.1.0.2.68.1.0">package:SJ</title>
        </g>
       </g>
       <g  gorn="0.2.0.2.69" id="_x30_.1.0.2.69">
        <title  id="0.1.0.2.69.0">element:RN1</title>
        <g  gorn="0.2.0.2.69.1" id="_x30_.1.0.2.69.1">
         <title  id="0.1.0.2.69.1.0">package:CAY16</title>
        </g>
       </g>
       <g  gorn="0.2.0.2.70" id="_x30_.1.0.2.70">
        <title  id="0.1.0.2.70.0">element:RN2</title>
        <g  gorn="0.2.0.2.70.1" id="_x30_.1.0.2.70.1">
         <title  id="0.1.0.2.70.1.0">package:CAY16</title>
        </g>
       </g>
       <g  gorn="0.2.0.2.71" id="_x30_.1.0.2.71">
        <title  id="0.1.0.2.71.0">element:RN3</title>
        <g  gorn="0.2.0.2.71.1" id="_x30_.1.0.2.71.1">
         <title  id="0.1.0.2.71.1.0">package:CAY16</title>
        </g>
       </g>
       <g  gorn="0.2.0.2.72" id="_x30_.1.0.2.72">
        <title  id="0.1.0.2.72.0">element:RN4</title>
        <g  gorn="0.2.0.2.72.1" id="_x30_.1.0.2.72.1">
         <title  id="0.1.0.2.72.1.0">package:CAY16</title>
        </g>
       </g>
       <g  gorn="0.2.0.2.73" id="_x30_.1.0.2.73">
        <title  id="0.1.0.2.73.0">element:RX</title>
        <g  gorn="0.2.0.2.73.1" id="_x30_.1.0.2.73.1">
         <title  id="0.1.0.2.73.1.0">package:CHIP-LED0805</title>
        </g>
       </g>
       <g  gorn="0.2.0.2.74" id="_x30_.1.0.2.74">
        <title  id="0.1.0.2.74.0">element:T1</title>
        <g  gorn="0.2.0.2.74.1" id="_x30_.1.0.2.74.1">
         <title  id="0.1.0.2.74.1.0">package:SOT-23</title>
        </g>
       </g>
       <g  gorn="0.2.0.2.75" id="_x30_.1.0.2.75">
        <title  id="0.1.0.2.75.0">element:TX</title>
        <g  gorn="0.2.0.2.75.1" id="_x30_.1.0.2.75.1">
         <title  id="0.1.0.2.75.1.0">package:CHIP-LED0805</title>
        </g>
       </g>
       <g  gorn="0.2.0.2.76" id="_x30_.1.0.2.76">
        <title  id="0.1.0.2.76.0">element:U1</title>
        <g  gorn="0.2.0.2.76.1" id="_x30_.1.0.2.76.1">
         <title  id="0.1.0.2.76.1.0">package:SOT223</title>
        </g>
       </g>
       <g  gorn="0.2.0.2.77" id="_x30_.1.0.2.77">
        <title  id="0.1.0.2.77.0">element:U2</title>
        <g  gorn="0.2.0.2.77.1" id="_x30_.1.0.2.77.1">
         <title  id="0.1.0.2.77.1.0">package:SOT23-DBV</title>
        </g>
       </g>
       <g  gorn="0.2.0.2.78" id="_x30_.1.0.2.78">
        <title  id="0.1.0.2.78.0">element:U3</title>
        <g  gorn="0.2.0.2.78.1" id="_x30_.1.0.2.78.1">
         <title  id="0.1.0.2.78.1.0">package:MLF32</title>
        </g>
       </g>
       <g  gorn="0.2.0.2.79" id="_x30_.1.0.2.79">
        <title  id="0.1.0.2.79.0">element:U5</title>
        <g  gorn="0.2.0.2.79.1" id="_x30_.1.0.2.79.1">
         <title  id="0.1.0.2.79.1.0">package:MSOP08</title>
        </g>
       </g>
       <g  gorn="0.2.0.2.80" id="_x30_.1.0.2.80">
        <title  id="0.1.0.2.80.0">element:X1</title>
        <g  gorn="0.2.0.2.80.1" id="_x30_.1.0.2.80.1">
         <title  id="0.1.0.2.80.1.0">package:POWERSUPPLY_DC-21MM</title>
        </g>
       </g>
       <g  gorn="0.2.0.2.81" id="_x30_.1.0.2.81">
        <title  id="0.1.0.2.81.0">element:X2</title>
        <g  gorn="0.2.0.2.81.1" id="_x30_.1.0.2.81.1">
         <title  id="0.1.0.2.81.1.0">package:PN61729</title>
        </g>
       </g>
       <g  gorn="0.2.0.2.82" id="_x30_.1.0.2.82">
        <title  id="0.1.0.2.82.0">element:Y1</title>
        <g  gorn="0.2.0.2.82.1" id="_x30_.1.0.2.82.1">
         <title  id="0.1.0.2.82.1.0">package:QS</title>
        </g>
       </g>
       <g  gorn="0.2.0.2.83" id="_x30_.1.0.2.83">
        <title  id="0.1.0.2.83.0">element:Y2</title>
        <g  gorn="0.2.0.2.83.1" id="_x30_.1.0.2.83.1">
         <title  id="0.1.0.2.83.1.0">package:RESONATOR</title>
        </g>
       </g>
       <g  gorn="0.2.0.2.84" id="_x30_.1.0.2.84">
        <title  id="0.1.0.2.84.0">element:Z1</title>
        <g  gorn="0.2.0.2.84.1" id="_x30_.1.0.2.84.1">
         <title  id="0.1.0.2.84.1.0">package:CT/CN0603</title>
        </g>
       </g>
       <g  gorn="0.2.0.2.85" id="_x30_.1.0.2.85">
        <title  id="0.1.0.2.85.0">element:Z2</title>
        <g  gorn="0.2.0.2.85.1" id="_x30_.1.0.2.85.1">
         <title  id="0.1.0.2.85.1.0">package:CT/CN0603</title>
        </g>
       </g>
       <g  gorn="0.2.0.2.86" id="_x30_.1.0.2.86">
        <title  id="0.1.0.2.86.0">element:ZU4</title>
        <g  gorn="0.2.0.2.86.1" id="_x30_.1.0.2.86.1">
         <title  id="0.1.0.2.86.1.0">package:DIL28-3</title>
        </g>
       </g>
      </g>
      <rect  width="14.173" x="67.405" y="45.833" fill="#333333" gorn="0.2.0.3" height="14.173" id="_x30_.1.0.6"/>
      <rect  width="105.12" x="96.812" y="96.84" fill="#333333" gorn="0.2.0.4" height="15.84" id="_x30_.1.0.8"/>
      <circle  fill="none" cx="161.972" gorn="0.2.0.5" cy="144" stroke="#9A916C" id="connector0pin" r="1.61" stroke-width="0.8113"/>
      <path  fill="#9A916C" gorn="0.2.0.6" id="_x30_.1.0.10" d="M160.361,140.295l3.222,0l0,7.408l-3.222,0L160.361,140.295M160.361,144c0,0.889,0.722,1.605,1.61,1.605c0.89,0,1.609,-0.721,1.609,-1.605l0,0c0,-0.894,-0.724,-1.611,-1.609,-1.611C161.083,142.389,160.361,143.111,160.361,144z"/>
      <circle  fill="none" cx="169.172" gorn="0.2.0.7" cy="144" stroke="#9A916C" id="connector1pin" r="1.61" stroke-width="0.8113"/>
      <path  fill="#9A916C" gorn="0.2.0.8" id="_x30_.1.0.12" d="M167.561,140.295l3.221,0l0,7.408l-3.221,0L167.561,140.295M167.561,144c0,0.889,0.721,1.605,1.609,1.605c0.89,0,1.608,-0.721,1.608,-1.605l0,0c0,-0.894,-0.722,-1.611,-1.608,-1.611C168.282,142.389,167.561,143.111,167.561,144z"/>
      <circle  fill="none" cx="176.372" gorn="0.2.0.9" cy="144" stroke="#9A916C" id="connector2pin" r="1.61" stroke-width="0.8113"/>
      <path  fill="#9A916C" gorn="0.2.0.10" id="_x30_.1.0.14" d="M174.76,140.295l3.222,0l0,7.408l-3.222,0L174.76,140.295M174.76,144c0,0.889,0.722,1.605,1.611,1.605c0.889,0,1.606,-0.721,1.606,-1.605l0,0c0,-0.894,-0.726,-1.611,-1.606,-1.611C175.482,142.389,174.76,143.111,174.76,144z"/>
      <circle  fill="none" cx="183.573" gorn="0.2.0.11" cy="144" stroke="#9A916C" id="connector3pin" r="1.61" stroke-width="0.8113"/>
      <path  fill="#9A916C" gorn="0.2.0.12" id="_x30_.1.0.16" d="M181.961,140.295l3.221,0l0,7.408l-3.221,0L181.961,140.295M181.961,144c0,0.889,0.721,1.605,1.605,1.605c0.895,0,1.611,-0.721,1.611,-1.605l0,0c0,-0.894,-0.725,-1.611,-1.611,-1.611C182.682,142.389,181.961,143.111,181.961,144z"/>
      <circle  fill="none" cx="190.772" gorn="0.2.0.13" cy="144" stroke="#9A916C" id="connector4pin" r="1.61" stroke-width="0.8113"/>
      <path  fill="#9A916C" gorn="0.2.0.14" id="_x30_.1.0.18" d="M189.161,140.295l3.221,0l0,7.408l-3.221,0L189.161,140.295M189.161,144c0,0.889,0.721,1.605,1.611,1.605c0.889,0,1.609,-0.721,1.609,-1.605l0,0c0,-0.894,-0.721,-1.611,-1.609,-1.611C189.881,142.389,189.161,143.111,189.161,144z"/>
      <circle  fill="none" cx="197.972" gorn="0.2.0.15" cy="144" stroke="#9A916C" id="connector5pin" r="1.61" stroke-width="0.8113"/>
      <path  fill="#9A916C" gorn="0.2.0.16" id="_x30_.1.0.20" d="M196.361,140.295l3.222,0l0,7.408l-3.222,0L196.361,140.295M196.361,144c0,0.889,0.722,1.605,1.61,1.605c0.89,0,1.609,-0.721,1.609,-1.605l0,0c0,-0.894,-0.724,-1.611,-1.609,-1.611C197.083,142.389,196.361,143.111,196.361,144z"/>
      <circle  fill="none" cx="198.333" gorn="0.2.0.17" cy="64.8" stroke="#9A916C" id="connector39pin" r="1.772" stroke-width="0.8504"/>
      <circle  fill="none" cx="205.532" gorn="0.2.0.18" cy="64.8" stroke="#9A916C" id="connector40pin" r="1.772" stroke-width="0.8504"/>
      <circle  fill="none" cx="198.333" gorn="0.2.0.19" cy="72" stroke="#9A916C" id="connector41pin" r="1.771" stroke-width="0.8504"/>
      <circle  fill="none" cx="205.532" gorn="0.2.0.20" cy="72" stroke="#9A916C" id="connector42pin" r="1.771" stroke-width="0.8504"/>
      <circle  fill="none" cx="198.333" gorn="0.2.0.21" cy="79.2" stroke="#9A916C" id="connector43pin" r="1.771" stroke-width="0.8504"/>
      <circle  fill="none" cx="205.532" gorn="0.2.0.22" cy="79.2" stroke="#9A916C" id="connector44pin" r="1.771" stroke-width="0.8504"/>
      <circle  fill="none" cx="77.012" gorn="0.2.0.23" cy="16.56" stroke="#9A916C" id="connector45pin" r="1.771" stroke-width="0.8504"/>
      <circle  fill="none" cx="77.012" gorn="0.2.0.24" cy="23.76" stroke="#9A916C" id="connector46pin" r="1.772" stroke-width="0.8504"/>
      <circle  fill="none" cx="69.812" gorn="0.2.0.25" cy="16.56" stroke="#9A916C" id="connector47pin" r="1.771" stroke-width="0.8504"/>
      <circle  fill="none" cx="69.812" gorn="0.2.0.26" cy="23.76" stroke="#9A916C" id="connector48pin" r="1.772" stroke-width="0.8504"/>
      <circle  fill="none" cx="62.611" gorn="0.2.0.27" cy="16.56" stroke="#9A916C" id="connector49pin" r="1.771" stroke-width="0.8504"/>
      <circle  fill="none" cx="62.611" gorn="0.2.0.28" cy="23.76" stroke="#9A916C" id="connector50pin" r="1.772" stroke-width="0.8504"/>
      <circle  fill="none" cx="136.051" gorn="0.2.0.29" cy="7.2" stroke="#9A916C" id="connector51pin" r="1.61" stroke-width="0.8113"/>
      <path  fill="#9A916C" gorn="0.2.0.30" id="_x30_.1.0.34" d="M134.441,3.496l3.222,0l0,7.408l-3.222,0L134.441,3.496M134.441,7.2c0,0.889,0.722,1.61,1.61,1.61c0.89,0,1.609,-0.721,1.609,-1.61c0,-0.89,-0.724,-1.61,-1.609,-1.61C135.163,5.59,134.441,6.311,134.441,7.2z"/>
      <circle  fill="none" cx="128.852" gorn="0.2.0.31" cy="7.2" stroke="#9A916C" id="connector52pin" r="1.61" stroke-width="0.8113"/>
      <path  fill="#9A916C" gorn="0.2.0.32" id="_x30_.1.0.36" d="M127.241,3.496l3.221,0l0,7.408l-3.221,0L127.241,3.496M127.241,7.2c0,0.889,0.721,1.61,1.611,1.61c0.889,0,1.609,-0.721,1.609,-1.61c0,-0.89,-0.721,-1.61,-1.609,-1.61C127.961,5.59,127.241,6.311,127.241,7.2z"/>
      <circle  fill="none" cx="121.652" gorn="0.2.0.33" cy="7.2" stroke="#9A916C" id="connector53pin" r="1.61" stroke-width="0.8113"/>
      <path  fill="#9A916C" gorn="0.2.0.34" id="_x30_.1.0.38" d="M120.042,3.496l3.225,0l0,7.408l-3.225,0L120.042,3.496M120.042,7.2c0,0.889,0.725,1.61,1.609,1.61c0.891,0,1.611,-0.721,1.611,-1.61c0,-0.89,-0.721,-1.61,-1.611,-1.61C120.762,5.59,120.042,6.311,120.042,7.2z"/>
      <circle  fill="none" cx="114.452" gorn="0.2.0.35" cy="7.2" stroke="#9A916C" id="connector54pin" r="1.61" stroke-width="0.8113"/>
      <path  fill="#9A916C" gorn="0.2.0.36" id="_x30_.1.0.40" d="M112.84,3.496l3.221,0l0,7.408l-3.221,0L112.84,3.496M112.84,7.2c0,0.889,0.722,1.61,1.611,1.61c0.889,0,1.605,-0.721,1.605,-1.61c0,-0.89,-0.725,-1.61,-1.605,-1.61C113.562,5.59,112.84,6.311,112.84,7.2z"/>
      <circle  fill="none" cx="107.252" gorn="0.2.0.37" cy="7.2" stroke="#9A916C" id="connector55pin" r="1.61" stroke-width="0.8113"/>
      <path  fill="#9A916C" gorn="0.2.0.38" id="_x30_.1.0.42" d="M105.641,3.496l3.221,0l0,7.408l-3.221,0L105.641,3.496M105.641,7.2c0,0.889,0.721,1.61,1.609,1.61c0.89,0,1.607,-0.721,1.607,-1.61c0,-0.89,-0.721,-1.61,-1.607,-1.61C106.362,5.59,105.641,6.311,105.641,7.2z"/>
      <circle  fill="none" cx="100.052" gorn="0.2.0.39" cy="7.2" stroke="#9A916C" id="connector56pin" r="1.61" stroke-width="0.8113"/>
      <path  fill="#9A916C" gorn="0.2.0.40" id="_x30_.1.0.44" d="M98.441,3.496l3.221,0l0,7.408l-3.221,0L98.441,3.496M98.441,7.2c0,0.889,0.721,1.61,1.61,1.61c0.889,0,1.61,-0.721,1.61,-1.61c0,-0.89,-0.721,-1.61,-1.61,-1.61C99.162,5.59,98.441,6.311,98.441,7.2z"/>
      <circle  fill="none" cx="92.852" gorn="0.2.0.41" cy="7.2" stroke="#9A916C" id="connector57pin" r="1.61" stroke-width="0.8113"/>
      <path  fill="#9A916C" gorn="0.2.0.42" id="_x30_.1.0.46" d="M91.241,3.496l3.221,0l0,7.408l-3.221,0L91.241,3.496M91.241,7.2c0,0.889,0.721,1.61,1.61,1.61c0.89,0,1.61,-0.721,1.61,-1.61c0,-0.89,-0.721,-1.61,-1.61,-1.61S91.241,6.311,91.241,7.2z"/>
      <circle  fill="none" cx="85.652" gorn="0.2.0.43" cy="7.2" stroke="#9A916C" id="connector58pin" r="1.61" stroke-width="0.8113"/>
      <path  fill="#9A916C" gorn="0.2.0.44" id="_x30_.1.0.48" d="M84.042,3.496l3.221,0l0,7.408l-3.221,0L84.042,3.496M84.042,7.2c0,0.889,0.721,1.61,1.61,1.61c0.889,0,1.61,-0.721,1.61,-1.61c0,-0.89,-0.721,-1.61,-1.61,-1.61C84.762,5.59,84.042,6.311,84.042,7.2z"/>
      <circle  fill="none" cx="78.452" gorn="0.2.0.45" cy="7.2" stroke="#9A916C" id="connector59pin" r="1.61" stroke-width="0.8113"/>
      <path  fill="#9A916C" gorn="0.2.0.46" id="_x30_.1.0.50" d="M76.841,3.496l3.221,0l0,7.408l-3.221,0L76.841,3.496M76.841,7.2c0,0.889,0.721,1.61,1.61,1.61c0.889,0,1.61,-0.721,1.61,-1.61c0,-0.89,-0.721,-1.61,-1.61,-1.61C77.562,5.59,76.841,6.311,76.841,7.2z"/>
      <circle  fill="none" cx="71.251" gorn="0.2.0.47" cy="7.2" stroke="#9A916C" id="connector60pin" r="1.61" stroke-width="0.8113"/>
      <path  fill="#9A916C" gorn="0.2.0.48" id="_x30_.1.0.52" d="M69.641,3.496l3.221,0l0,7.408l-3.221,0L69.641,3.496M69.641,7.2c0,0.889,0.721,1.61,1.61,1.61c0.89,0,1.611,-0.721,1.611,-1.61c0,-0.89,-0.721,-1.61,-1.611,-1.61C70.362,5.59,69.641,6.311,69.641,7.2z"/>
      <circle  fill="none" cx="197.972" gorn="0.2.0.49" cy="7.2" stroke="#9A916C" id="connector61pin" r="1.61" stroke-width="0.8113"/>
      <path  fill="#9A916C" gorn="0.2.0.50" id="_x30_.1.0.54" d="M196.361,3.496l3.222,0l0,7.408l-3.222,0L196.361,3.496M196.361,7.2c0,0.889,0.722,1.61,1.61,1.61c0.89,0,1.609,-0.721,1.609,-1.61c0,-0.89,-0.724,-1.61,-1.609,-1.61C197.083,5.59,196.361,6.311,196.361,7.2z"/>
      <circle  fill="none" cx="190.772" gorn="0.2.0.51" cy="7.2" stroke="#9A916C" id="connector62pin" r="1.61" stroke-width="0.8113"/>
      <path  fill="#9A916C" gorn="0.2.0.52" id="_x30_.1.0.56" d="M189.161,3.496l3.221,0l0,7.408l-3.221,0L189.161,3.496M189.161,7.2c0,0.889,0.721,1.61,1.611,1.61c0.889,0,1.609,-0.721,1.609,-1.61c0,-0.89,-0.721,-1.61,-1.609,-1.61C189.881,5.59,189.161,6.311,189.161,7.2z"/>
      <circle  fill="none" cx="183.573" gorn="0.2.0.53" cy="7.2" stroke="#9A916C" id="connector63pin" r="1.61" stroke-width="0.8113"/>
      <path  fill="#9A916C" gorn="0.2.0.54" id="_x30_.1.0.58" d="M181.961,3.496l3.221,0l0,7.408l-3.221,0L181.961,3.496M181.961,7.2c0,0.889,0.721,1.61,1.605,1.61c0.895,0,1.611,-0.721,1.611,-1.61c0,-0.89,-0.725,-1.61,-1.611,-1.61C182.682,5.59,181.961,6.311,181.961,7.2z"/>
      <circle  fill="none" cx="176.372" gorn="0.2.0.55" cy="7.2" stroke="#9A916C" id="connector64pin" r="1.61" stroke-width="0.8113"/>
      <path  fill="#9A916C" gorn="0.2.0.56" id="_x30_.1.0.60" d="M174.76,3.496l3.222,0l0,7.408l-3.222,0L174.76,3.496M174.76,7.2c0,0.889,0.722,1.61,1.611,1.61c0.889,0,1.606,-0.721,1.606,-1.61c0,-0.89,-0.726,-1.61,-1.606,-1.61C175.482,5.59,174.76,6.311,174.76,7.2z"/>
      <circle  fill="none" cx="169.172" gorn="0.2.0.57" cy="7.2" stroke="#9A916C" id="connector65pin" r="1.61" stroke-width="0.8113"/>
      <path  fill="#9A916C" gorn="0.2.0.58" id="_x30_.1.0.62" d="M167.561,3.496l3.221,0l0,7.408l-3.221,0L167.561,3.496M167.561,7.2c0,0.889,0.721,1.61,1.609,1.61c0.89,0,1.608,-0.721,1.608,-1.61c0,-0.89,-0.722,-1.61,-1.608,-1.61C168.282,5.59,167.561,6.311,167.561,7.2z"/>
      <circle  fill="none" cx="161.972" gorn="0.2.0.59" cy="7.2" stroke="#9A916C" id="connector66pin" r="1.61" stroke-width="0.8113"/>
      <path  fill="#9A916C" gorn="0.2.0.60" id="_x30_.1.0.64" d="M160.361,3.496l3.222,0l0,7.408l-3.222,0L160.361,3.496M160.361,7.2c0,0.889,0.722,1.61,1.61,1.61c0.89,0,1.609,-0.721,1.609,-1.61c0,-0.89,-0.724,-1.61,-1.609,-1.61C161.083,5.59,160.361,6.311,160.361,7.2z"/>
      <circle  fill="none" cx="154.772" gorn="0.2.0.61" cy="7.2" stroke="#9A916C" id="connector67pin" r="1.61" stroke-width="0.8113"/>
      <path  fill="#9A916C" gorn="0.2.0.62" id="_x30_.1.0.66" d="M153.161,3.496l3.221,0l0,7.408l-3.221,0L153.161,3.496M153.161,7.2c0,0.889,0.721,1.61,1.611,1.61c0.889,0,1.609,-0.721,1.609,-1.61c0,-0.89,-0.721,-1.61,-1.609,-1.61C153.881,5.59,153.161,6.311,153.161,7.2z"/>
      <circle  fill="none" cx="147.573" gorn="0.2.0.63" cy="7.2" stroke="#9A916C" id="connector68pin" r="1.61" stroke-width="0.8113"/>
      <path  fill="#9A916C" gorn="0.2.0.64" id="_x30_.1.0.68" d="M145.961,3.496l3.221,0l0,7.408l-3.221,0L145.961,3.496M145.961,7.2c0,0.889,0.721,1.61,1.605,1.61c0.895,0,1.611,-0.721,1.611,-1.61c0,-0.89,-0.725,-1.61,-1.611,-1.61C146.682,5.59,145.961,6.311,145.961,7.2z"/>
      <circle  fill="none" cx="104.372" gorn="0.2.0.65" cy="144" stroke="#9A916C" id="connector84pin" r="1.61" stroke-width="0.8113"/>
      <circle  fill="none" cx="97.172" gorn="0.2.0.66" cy="144" stroke="#9A916C" id="connector91pin" r="1.61" stroke-width="0.8113"/>
      <path  fill="#9A916C" gorn="0.2.0.67" id="_x30_.1.0.71" d="M102.761,140.295l3.221,0l0,7.408l-3.221,0L102.761,140.295M102.761,144c0,0.889,0.721,1.605,1.61,1.605c0.89,0,1.611,-0.721,1.611,-1.605l0,0c0,-0.894,-0.721,-1.611,-1.611,-1.611C103.482,142.389,102.761,143.111,102.761,144z"/>
      <path  fill="#9A916C" gorn="0.2.0.68" id="_x30_.1.0.72" d="M95.562,140.295l3.221,0l0,7.408l-3.221,0L95.562,140.295M95.562,144c0,0.889,0.721,1.605,1.61,1.605c0.89,0,1.611,-0.721,1.611,-1.605l0,0c0,-0.894,-0.721,-1.611,-1.611,-1.611C96.282,142.389,95.562,143.111,95.562,144z"/>
      <circle  fill="none" cx="111.573" gorn="0.2.0.69" cy="144" stroke="#9A916C" id="connector85pin" r="1.61" stroke-width="0.8113"/>
      <path  fill="#9A916C" gorn="0.2.0.70" id="_x30_.1.0.74" d="M109.961,140.295l3.221,0l0,7.408l-3.221,0L109.961,140.295M109.961,144c0,0.889,0.721,1.605,1.605,1.605c0.895,0,1.611,-0.721,1.611,-1.605l0,0c0,-0.894,-0.725,-1.611,-1.611,-1.611C110.682,142.389,109.961,143.111,109.961,144z"/>
      <circle  fill="none" cx="118.772" gorn="0.2.0.71" cy="144" stroke="#9A916C" id="connector86pin" r="1.61" stroke-width="0.8113"/>
      <path  fill="#9A916C" gorn="0.2.0.72" id="_x30_.1.0.76" d="M117.161,140.295l3.221,0l0,7.408l-3.221,0L117.161,140.295M117.161,144c0,0.889,0.721,1.605,1.611,1.605c0.889,0,1.609,-0.721,1.609,-1.605l0,0c0,-0.894,-0.721,-1.611,-1.609,-1.611C117.881,142.389,117.161,143.111,117.161,144z"/>
      <circle  fill="none" cx="125.972" gorn="0.2.0.73" cy="144" stroke="#9A916C" id="connector87pin" r="1.61" stroke-width="0.8113"/>
      <path  fill="#9A916C" gorn="0.2.0.74" id="_x30_.1.0.78" d="M124.361,140.295l3.222,0l0,7.408l-3.222,0L124.361,140.295M124.361,144c0,0.889,0.722,1.605,1.61,1.605c0.89,0,1.609,-0.721,1.609,-1.605l0,0c0,-0.894,-0.724,-1.611,-1.609,-1.611C125.083,142.389,124.361,143.111,124.361,144z"/>
      <circle  fill="none" cx="133.172" gorn="0.2.0.75" cy="144" stroke="#9A916C" id="connector88pin" r="1.61" stroke-width="0.8113"/>
      <path  fill="#9A916C" gorn="0.2.0.76" id="_x30_.1.0.80" d="M131.561,140.295l3.221,0l0,7.408l-3.221,0L131.561,140.295M131.561,144c0,0.889,0.721,1.605,1.609,1.605c0.89,0,1.608,-0.721,1.608,-1.605l0,0c0,-0.894,-0.722,-1.611,-1.608,-1.611C132.282,142.389,131.561,143.111,131.561,144z"/>
      <circle  fill="none" cx="140.372" gorn="0.2.0.77" cy="144" stroke="#9A916C" id="connector89pin" r="1.61" stroke-width="0.8113"/>
      <path  fill="#9A916C" gorn="0.2.0.78" id="_x30_.1.0.82" d="M138.76,140.295l3.222,0l0,7.408l-3.222,0L138.76,140.295M138.76,144c0,0.889,0.722,1.605,1.611,1.605c0.889,0,1.606,-0.721,1.606,-1.605l0,0c0,-0.894,-0.726,-1.611,-1.606,-1.611C139.482,142.389,138.76,143.111,138.76,144z"/>
      <circle  fill="none" cx="147.573" gorn="0.2.0.79" cy="144" stroke="#9A916C" id="connector90pin" r="1.61" stroke-width="0.8113"/>
      <path  fill="#9A916C" gorn="0.2.0.80" id="_x30_.1.0.84" d="M145.961,140.295l3.221,0l0,7.408l-3.221,0L145.961,140.295M145.961,144c0,0.889,0.721,1.605,1.605,1.605c0.895,0,1.611,-0.721,1.611,-1.605l0,0c0,-0.894,-0.725,-1.611,-1.611,-1.611C146.682,142.389,145.961,143.111,145.961,144z"/>
      <line  fill="none" gorn="0.2.0.81" stroke="#FFFFFF" id="_x30_.1.0.85" stroke-linecap="round" y1="29.16" stroke-width="0.864" x1="92.794" y2="29.16" x2="199.704"/>
      <line  fill="none" gorn="0.2.0.82" stroke="#FFFFFF" id="_x30_.1.0.86" stroke-linecap="round" y1="126.206" stroke-width="0.864" x1="160.068" y2="126.206" x2="199.704"/>
      <g  gorn="0.2.0.83" id="_x30_.1.0.87">
       <g  gorn="0.2.0.83.0" id="_x30_.1.0.87.0">
        <g transform="matrix(1, 0, 0, 1, 137.956, 130.811)">
         <g >
          <g >
           <g >
            <g  gorn="0.2.0.83.0.0.0.0.0" id="_x30_.1.0.87.0.0">
             <g transform="matrix(1, 0, 0, 1, 0, 3.05176e-05)">
              <g >
               <g >
                <g >
                 <text  fill="#FFFFFF" font-family="'OCRA'" gorn="0.2.0.83.0.0.0.0.0.0.0.0.0" id="_x30_.1.0.87.0.0.0" font-size="3.6749">POWER</text>
                </g>
               </g>
              </g>
             </g>
            </g>
           </g>
          </g>
         </g>
        </g>
       </g>
      </g>
      <line  fill="none" gorn="0.2.0.84" stroke="#FFFFFF" id="_x30_.1.0.88" stroke-linecap="round" y1="126.206" stroke-width="0.864" x1="115.172" y2="126.206" x2="151.085"/>
      <g  gorn="0.2.0.85" id="_x30_.1.0.89">
       <g  gorn="0.2.0.85.0" id="_x30_.1.0.89.0">
        <g transform="matrix(1, 0, 0, 1, 199.772, 16.2)">
         <g >
          <g >
           <g >
            <g  gorn="0.2.0.85.0.0.0.0.0" id="_x30_.1.0.89.0.0">
             <g  gorn="0.2.0.85.0.0.0.0.0.0" id="_x30_.1.0.89.0.0.0">
              <g transform="rotate(270)">
               <g >
                <g >
                 <g >
                  <g  gorn="0.2.0.85.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.0.89.0.0.0.0">
                   <g  gorn="0.2.0.85.0.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.0.89.0.0.0.0.0">
                    <g transform="matrix(1, 0, 0, 1, 1.5198, -0.0449)">
                     <g >
                      <g >
                       <g >
                        <g  gorn="0.2.0.85.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.0.89.0.0.0.0.0.0">
                         <g transform="matrix(1, 0, 0, 1, 3.05176e-05, 0)">
                          <g >
                           <g >
                            <g >
                             <text  fill="#FFFFFF" font-family="'OCRA'" gorn="0.2.0.85.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.0.89.0.0.0.0.0.0.0" font-size="3.75">0</text>
                            </g>
                           </g>
                          </g>
                         </g>
                        </g>
                       </g>
                      </g>
                     </g>
                    </g>
                   </g>
                  </g>
                 </g>
                </g>
               </g>
              </g>
             </g>
            </g>
           </g>
          </g>
         </g>
        </g>
       </g>
      </g>
      <g  gorn="0.2.0.86" id="_x30_.1.0.90">
       <g  gorn="0.2.0.86.0" id="_x30_.1.0.90.0">
        <g transform="matrix(1, 0, 0, 1, 192.572, 16.2)">
         <g >
          <g >
           <g >
            <g  gorn="0.2.0.86.0.0.0.0.0" id="_x30_.1.0.90.0.0">
             <g  gorn="0.2.0.86.0.0.0.0.0.0" id="_x30_.1.0.90.0.0.0">
              <g transform="rotate(270)">
               <g >
                <g >
                 <g >
                  <g  gorn="0.2.0.86.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.0.90.0.0.0.0">
                   <g  gorn="0.2.0.86.0.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.0.90.0.0.0.0.0">
                    <g transform="matrix(1, 0, 0, 1, 1.5198, -0.0441)">
                     <g >
                      <g >
                       <g >
                        <g  gorn="0.2.0.86.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.0.90.0.0.0.0.0.0">
                         <g transform="matrix(1, 0, 0, 1, 3.05176e-05, 0)">
                          <g >
                           <g >
                            <g >
                             <text  fill="#FFFFFF" font-family="'OCRA'" gorn="0.2.0.86.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.0.90.0.0.0.0.0.0.0" font-size="3.75">1</text>
                            </g>
                           </g>
                          </g>
                         </g>
                        </g>
                       </g>
                      </g>
                     </g>
                    </g>
                   </g>
                  </g>
                 </g>
                </g>
               </g>
              </g>
             </g>
            </g>
           </g>
          </g>
         </g>
        </g>
       </g>
      </g>
      <g  gorn="0.2.0.87" id="_x30_.1.0.91">
       <g  gorn="0.2.0.87.0" id="_x30_.1.0.91.0">
        <g transform="matrix(1, 0, 0, 1, 192.572, 30.96)">
         <g >
          <g >
           <g >
            <g  gorn="0.2.0.87.0.0.0.0.0" id="_x30_.1.0.91.0.0">
             <g  gorn="0.2.0.87.0.0.0.0.0.0" id="_x30_.1.0.91.0.0.0">
              <g transform="rotate(270)">
               <g >
                <g >
                 <g >
                  <g  gorn="0.2.0.87.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.0.91.0.0.0.0">
                   <g  gorn="0.2.0.87.0.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.0.91.0.0.0.0.0">
                    <g transform="matrix(1, 0, 0, 1, 3.524, -0.0441)">
                     <g >
                      <g >
                       <g >
                        <g  gorn="0.2.0.87.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.0.91.0.0.0.0.0.0">
                         <g transform="matrix(1, 0, 0, 1, -3.05176e-05, 0)">
                          <g >
                           <g >
                            <g >
                             <text  fill="#FFFFFF" font-family="'OCRA'" gorn="0.2.0.87.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.0.91.0.0.0.0.0.0.0" font-size="3.75">TX0</text>
                            </g>
                           </g>
                          </g>
                         </g>
                        </g>
                       </g>
                      </g>
                     </g>
                    </g>
                   </g>
                  </g>
                 </g>
                </g>
               </g>
              </g>
             </g>
            </g>
           </g>
          </g>
         </g>
        </g>
       </g>
      </g>
      <g  gorn="0.2.0.88" id="_x30_.1.0.92">
       <g  gorn="0.2.0.88.0" id="_x30_.1.0.92.0">
        <g transform="matrix(1, 0, 0, 1, 199.772, 30.96)">
         <g >
          <g >
           <g >
            <g  gorn="0.2.0.88.0.0.0.0.0" id="_x30_.1.0.92.0.0">
             <g  gorn="0.2.0.88.0.0.0.0.0.0" id="_x30_.1.0.92.0.0.0">
              <g transform="rotate(270)">
               <g >
                <g >
                 <g >
                  <g  gorn="0.2.0.88.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.0.92.0.0.0.0">
                   <g  gorn="0.2.0.88.0.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.0.92.0.0.0.0.0">
                    <g transform="matrix(1, 0, 0, 1, 3.524, -0.0449)">
                     <g >
                      <g >
                       <g >
                        <g  gorn="0.2.0.88.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.0.92.0.0.0.0.0.0">
                         <g transform="matrix(1, 0, 0, 1, -3.05176e-05, 0)">
                          <g >
                           <g >
                            <g >
                             <text  fill="#FFFFFF" font-family="'OCRA'" gorn="0.2.0.88.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.0.92.0.0.0.0.0.0.0" font-size="3.75">RX0</text>
                            </g>
                           </g>
                          </g>
                         </g>
                        </g>
                       </g>
                      </g>
                     </g>
                    </g>
                   </g>
                  </g>
                 </g>
                </g>
               </g>
              </g>
             </g>
            </g>
           </g>
          </g>
         </g>
        </g>
       </g>
      </g>
      <g  gorn="0.2.0.89" id="_x30_.1.0.93">
       <path  fill="#FFFFFF" gorn="0.2.0.89.0" id="_x30_.1.0.93.0" d="M192.11,18.007c-0.004,0,-0.01,0,-0.014,0l-1.945,0c-0.125,0,-0.236,-0.068,-0.297,-0.179c-0.061,-0.11,-0.053,-0.243,0.018,-0.347l0.978,-1.459c0.125,-0.188,0.438,-0.188,0.563,0l0.93,1.394c0.066,0.062,0.113,0.152,0.113,0.253C192.448,17.856,192.297,18.007,192.11,18.007z"/>
      </g>
      <g  gorn="0.2.0.90" id="_x30_.1.0.94">
       <path  fill="#FFFFFF" gorn="0.2.0.90.0" id="_x30_.1.0.94.0" d="M197.409,15.88c0.006,0,0.01,0,0.016,0l1.939,0c0.125,0,0.238,0.068,0.301,0.178c0.063,0.111,0.053,0.244,-0.02,0.348l-0.973,1.459c-0.125,0.188,-0.438,0.188,-0.563,0l-0.93,-1.396c-0.07,-0.063,-0.113,-0.151,-0.113,-0.252C197.07,16.032,197.222,15.88,197.409,15.88z"/>
      </g>
      <g  gorn="0.2.0.91" id="_x30_.1.0.95">
       <path  fill="#FFFFFF" gorn="0.2.0.91.0" id="_x30_.1.0.95.0" d="M179.901,26.121c-0.021,-0.549,0.273,-0.829,0.653,-0.829c0.229,0,0.405,0.071,0.774,0.247c0.276,0.132,0.479,0.23,0.687,0.23c0.198,0,0.291,-0.159,0.297,-0.461l0.329,0c0.027,0.615,-0.291,0.829,-0.631,0.829c-0.221,0,-0.418,-0.066,-0.797,-0.242c-0.258,-0.126,-0.461,-0.242,-0.659,-0.242s-0.318,0.138,-0.329,0.467L179.901,26.121L179.901,26.121z"/>
      </g>
      <g  gorn="0.2.0.92" id="_x30_.1.0.96">
       <g  gorn="0.2.0.92.0" id="_x30_.1.0.96.0">
        <g  gorn="0.2.0.92.0.0" id="_x30_.1.0.96.0.0">
         <path  fill="#FFFFFF" gorn="0.2.0.92.0.0.0" id="_x30_.1.0.96.0.0.0" d="M125.862,37.068c0.848,-0.93,1.498,-1.778,2.281,-2.478c2.966,-2.656,6.307,-3.641,10.131,-2.03c3.618,1.524,5.575,5.294,4.788,9.14c-0.726,3.549,-4.138,6.252,-7.864,6.379c-3.453,0.117,-6.047,-1.427,-8.21,-3.934c-0.331,-0.385,-0.646,-0.786,-1.063,-1.297c-0.299,0.351,-0.533,0.618,-0.758,0.899c-2.313,2.913,-5.187,4.567,-9.047,4.32c-3.785,-0.243,-7.248,-3.72,-7.48,-7.501c-0.301,-4.792,3.354,-8.726,8.432,-8.769c3.362,-0.029,5.991,1.707,8.042,4.321C125.336,36.405,125.563,36.69,125.862,37.068z"/>
         <path  fill="#0F7391" gorn="0.2.0.92.0.0.1" id="_x30_.1.0.96.0.0.1" d="M117.56,34.457c-3.496,-0.006,-6.05,2.237,-6.332,5.133c-0.251,2.569,1.789,5.137,4.597,5.746c2.766,0.6,4.977,-0.55,6.643,-2.557c2.558,-3.073,2.466,-2.542,0.031,-5.591C121.145,35.492,119.297,34.542,117.56,34.457z"/>
         <path  fill="#0F7391" gorn="0.2.0.92.0.0.2" id="_x30_.1.0.96.0.0.2" d="M134.883,34.434c-0.428,0.03,-0.74,0.019,-1.041,0.079c-2.965,0.599,-4.824,2.568,-6.221,5.082c-0.109,0.198,-0.113,0.564,-0.004,0.757c1.262,2.183,2.838,4.053,5.348,4.841c2.433,0.763,4.563,0.132,6.24,-1.735c1.504,-1.675,1.846,-3.656,0.852,-5.72C139.002,35.555,137.124,34.592,134.883,34.434z"/>
        </g>
        <g  gorn="0.2.0.92.0.1" id="_x30_.1.0.96.0.1">
         <path  fill="#FFFFFF" gorn="0.2.0.92.0.1.0" id="_x30_.1.0.96.0.1.0" d="M120.061,40.583c0,0.078,-0.063,0.142,-0.143,0.142l-5.168,0c-0.078,0,-0.145,-0.064,-0.145,-0.142l0,-1.561c0,-0.078,0.063,-0.142,0.145,-0.142l5.168,0c0.078,0,0.143,0.064,0.143,0.142L120.061,40.583z"/>
        </g>
        <g  gorn="0.2.0.92.0.2" id="_x30_.1.0.96.0.2">
         <path  fill="#FFFFFF" gorn="0.2.0.92.0.2.0" id="_x30_.1.0.96.0.2.0" d="M137.129,39.024c0,-0.078,-0.063,-0.142,-0.144,-0.142l-1.521,0c-0.077,0,-0.144,-0.064,-0.144,-0.142l0,-1.521c0,-0.078,-0.063,-0.142,-0.142,-0.142l-1.563,0c-0.078,0,-0.143,0.064,-0.143,0.142l0,1.521c0,0.078,-0.063,0.142,-0.143,0.142l-1.521,0c-0.078,0,-0.145,0.064,-0.145,0.142l0,1.561c0,0.078,0.063,0.142,0.145,0.142l1.521,0c0.078,0,0.143,0.064,0.143,0.142l0,1.52c0,0.078,0.063,0.142,0.143,0.142l1.563,0c0.076,0,0.142,-0.064,0.142,-0.142l0,-1.52c0,-0.078,0.063,-0.142,0.144,-0.142l1.521,0c0.078,0,0.144,-0.064,0.144,-0.142L137.129,39.024z"/>
        </g>
        <g  gorn="0.2.0.92.0.3" id="_x30_.1.0.96.0.3">
         <circle  fill="#FFFFFF" cx="172.388" gorn="0.2.0.92.0.3.0" cy="32.522" id="_x30_.1.0.96.0.3.0" r="0.568"/>
         <circle  fill="#FFFFFF" cx="170.971" gorn="0.2.0.92.0.3.1" cy="32.522" id="_x30_.1.0.96.0.3.1" r="0.568"/>
         <circle  fill="#FFFFFF" cx="169.554" gorn="0.2.0.92.0.3.2" cy="32.522" id="_x30_.1.0.96.0.3.2" r="0.568"/>
         <circle  fill="#FFFFFF" cx="168.137" gorn="0.2.0.92.0.3.3" cy="32.522" id="_x30_.1.0.96.0.3.3" r="0.568"/>
         <circle  fill="#FFFFFF" cx="166.72" gorn="0.2.0.92.0.3.4" cy="32.522" id="_x30_.1.0.96.0.3.4" r="0.568"/>
         <circle  fill="#FFFFFF" cx="165.303" gorn="0.2.0.92.0.3.5" cy="32.522" id="_x30_.1.0.96.0.3.5" r="0.568"/>
         <circle  fill="#FFFFFF" cx="163.886" gorn="0.2.0.92.0.3.6" cy="32.522" id="_x30_.1.0.96.0.3.6" r="0.568"/>
         <circle  fill="#FFFFFF" cx="162.469" gorn="0.2.0.92.0.3.7" cy="32.522" id="_x30_.1.0.96.0.3.7" r="0.568"/>
         <circle  fill="#FFFFFF" cx="161.051" gorn="0.2.0.92.0.3.8" cy="32.522" id="_x30_.1.0.96.0.3.8" r="0.568"/>
         <circle  fill="#FFFFFF" cx="159.635" gorn="0.2.0.92.0.3.9" cy="32.522" id="_x30_.1.0.96.0.3.9" r="0.568"/>
         <circle  fill="#FFFFFF" cx="158.217" gorn="0.2.0.92.0.3.10" cy="32.522" id="_x30_.1.0.96.0.3.10" r="0.568"/>
         <circle  fill="#FFFFFF" cx="156.801" gorn="0.2.0.92.0.3.11" cy="32.522" id="_x30_.1.0.96.0.3.11" r="0.568"/>
         <circle  fill="#FFFFFF" cx="155.383" gorn="0.2.0.92.0.3.12" cy="32.522" id="_x30_.1.0.96.0.3.12" r="0.568"/>
         <circle  fill="#FFFFFF" cx="153.967" gorn="0.2.0.92.0.3.13" cy="32.522" id="_x30_.1.0.96.0.3.13" r="0.568"/>
        </g>
        <g  gorn="0.2.0.92.0.4" id="_x30_.1.0.96.0.4">
         <circle  fill="#FFFFFF" cx="172.445" gorn="0.2.0.92.0.4.0" cy="47.404" id="_x30_.1.0.96.0.4.0" r="0.567"/>
         <circle  fill="#FFFFFF" cx="173.793" gorn="0.2.0.92.0.4.1" cy="47.137" id="_x30_.1.0.96.0.4.1" r="0.567"/>
         <circle  fill="#FFFFFF" cx="175.071" gorn="0.2.0.92.0.4.2" cy="46.628" id="_x30_.1.0.96.0.4.2" r="0.568"/>
         <circle  fill="#FFFFFF" cx="176.233" gorn="0.2.0.92.0.4.3" cy="45.894" id="_x30_.1.0.96.0.4.3" r="0.567"/>
         <circle  fill="#FFFFFF" cx="177.241" gorn="0.2.0.92.0.4.4" cy="44.959" id="_x30_.1.0.96.0.4.4" r="0.568"/>
         <circle  fill="#FFFFFF" cx="178.061" gorn="0.2.0.92.0.4.5" cy="43.855" id="_x30_.1.0.96.0.4.5" r="0.567"/>
         <circle  fill="#FFFFFF" cx="178.665" gorn="0.2.0.92.0.4.6" cy="42.62" id="_x30_.1.0.96.0.4.6" r="0.567"/>
         <circle  fill="#FFFFFF" cx="179.032" gorn="0.2.0.92.0.4.7" cy="41.295" id="_x30_.1.0.96.0.4.7" r="0.567"/>
         <circle  fill="#FFFFFF" cx="179.151" gorn="0.2.0.92.0.4.8" cy="39.925" id="_x30_.1.0.96.0.4.8" r="0.567"/>
         <circle  fill="#FFFFFF" cx="179.017" gorn="0.2.0.92.0.4.9" cy="38.557" id="_x30_.1.0.96.0.4.9" r="0.567"/>
         <circle  fill="#FFFFFF" cx="178.633" gorn="0.2.0.92.0.4.10" cy="37.236" id="_x30_.1.0.96.0.4.10" r="0.567"/>
         <circle  fill="#FFFFFF" cx="178.017" gorn="0.2.0.92.0.4.11" cy="36.008" id="_x30_.1.0.96.0.4.11" r="0.567"/>
         <circle  fill="#FFFFFF" cx="177.185" gorn="0.2.0.92.0.4.12" cy="34.914" id="_x30_.1.0.96.0.4.12" r="0.567"/>
         <circle  fill="#FFFFFF" cx="176.167" gorn="0.2.0.92.0.4.13" cy="33.99" id="_x30_.1.0.96.0.4.13" r="0.568"/>
         <circle  fill="#FFFFFF" cx="174.997" gorn="0.2.0.92.0.4.14" cy="33.269" id="_x30_.1.0.96.0.4.14" r="0.568"/>
         <circle  fill="#FFFFFF" cx="173.713" gorn="0.2.0.92.0.4.15" cy="32.774" id="_x30_.1.0.96.0.4.15" r="0.568"/>
         <circle  fill="#FFFFFF" cx="172.361" gorn="0.2.0.92.0.4.16" cy="32.522" id="_x30_.1.0.96.0.4.16" r="0.568"/>
         <circle  fill="#FFFFFF" cx="170.986" gorn="0.2.0.92.0.4.17" cy="32.522" id="_x30_.1.0.96.0.4.17" r="0.568"/>
        </g>
        <g  gorn="0.2.0.92.0.5" id="_x30_.1.0.96.0.5">
         <circle  fill="#FFFFFF" cx="152.413" gorn="0.2.0.92.0.5.0" cy="47.309" id="_x30_.1.0.96.0.5.0" r="0.568"/>
         <circle  fill="#FFFFFF" cx="151.083" gorn="0.2.0.92.0.5.1" cy="47.026" id="_x30_.1.0.96.0.5.1" r="0.568"/>
         <circle  fill="#FFFFFF" cx="149.825" gorn="0.2.0.92.0.5.2" cy="46.506" id="_x30_.1.0.96.0.5.2" r="0.568"/>
         <circle  fill="#FFFFFF" cx="148.684" gorn="0.2.0.92.0.5.3" cy="45.765" id="_x30_.1.0.96.0.5.3" r="0.568"/>
         <circle  fill="#FFFFFF" cx="147.697" gorn="0.2.0.92.0.5.4" cy="44.828" id="_x30_.1.0.96.0.5.4" r="0.568"/>
         <circle  fill="#FFFFFF" cx="146.897" gorn="0.2.0.92.0.5.5" cy="43.727" id="_x30_.1.0.96.0.5.5" r="0.568"/>
         <circle  fill="#FFFFFF" cx="146.312" gorn="0.2.0.92.0.5.6" cy="42.499" id="_x30_.1.0.96.0.5.6" r="0.568"/>
         <circle  fill="#FFFFFF" cx="145.96" gorn="0.2.0.92.0.5.7" cy="41.185" id="_x30_.1.0.96.0.5.7" r="0.568"/>
         <circle  fill="#FFFFFF" cx="145.853" gorn="0.2.0.92.0.5.8" cy="39.829" id="_x30_.1.0.96.0.5.8" r="0.568"/>
         <path  fill="#FFFFFF" gorn="0.2.0.92.0.5.9" id="_x30_.1.0.96.0.5.9" d="M146.054,37.911c0.31,0.033,0.538,0.313,0.505,0.623c-0.033,0.313,-0.313,0.54,-0.624,0.507c-0.312,-0.033,-0.537,-0.313,-0.505,-0.627C145.463,38.104,145.743,37.877,146.054,37.911z"/>
         <path  fill="#FFFFFF" gorn="0.2.0.92.0.5.10" id="_x30_.1.0.96.0.5.10" d="M146.543,36.626c0.299,0.089,0.472,0.406,0.383,0.705c-0.09,0.302,-0.405,0.474,-0.706,0.385c-0.3,-0.089,-0.472,-0.406,-0.382,-0.708C145.926,36.709,146.243,36.537,146.543,36.626z"/>
         <circle  fill="#FFFFFF" cx="146.999" gorn="0.2.0.92.0.5.11" cy="35.959" id="_x30_.1.0.96.0.5.11" r="0.568"/>
         <circle  fill="#FFFFFF" cx="147.827" gorn="0.2.0.92.0.5.12" cy="34.879" id="_x30_.1.0.96.0.5.12" r="0.568"/>
         <circle  fill="#FFFFFF" cx="148.836" gorn="0.2.0.92.0.5.13" cy="33.969" id="_x30_.1.0.96.0.5.13" r="0.568"/>
         <circle  fill="#FFFFFF" cx="149.999" gorn="0.2.0.92.0.5.14" cy="33.258" id="_x30_.1.0.96.0.5.14" r="0.568"/>
         <circle  fill="#FFFFFF" cx="151.268" gorn="0.2.0.92.0.5.15" cy="32.77" id="_x30_.1.0.96.0.5.15" r="0.568"/>
         <circle  fill="#FFFFFF" cx="152.606" gorn="0.2.0.92.0.5.16" cy="32.522" id="_x30_.1.0.96.0.5.16" r="0.568"/>
         <circle  fill="#FFFFFF" cx="153.967" gorn="0.2.0.92.0.5.17" cy="32.522" id="_x30_.1.0.96.0.5.17" r="0.568"/>
        </g>
        <g  gorn="0.2.0.92.0.6" id="_x30_.1.0.96.0.6">
         <circle  fill="#FFFFFF" cx="172.388" gorn="0.2.0.92.0.6.0" cy="47.454" id="_x30_.1.0.96.0.6.0" r="0.568"/>
         <circle  fill="#FFFFFF" cx="170.971" gorn="0.2.0.92.0.6.1" cy="47.454" id="_x30_.1.0.96.0.6.1" r="0.568"/>
         <circle  fill="#FFFFFF" cx="169.554" gorn="0.2.0.92.0.6.2" cy="47.454" id="_x30_.1.0.96.0.6.2" r="0.568"/>
         <circle  fill="#FFFFFF" cx="168.137" gorn="0.2.0.92.0.6.3" cy="47.454" id="_x30_.1.0.96.0.6.3" r="0.568"/>
         <circle  fill="#FFFFFF" cx="166.72" gorn="0.2.0.92.0.6.4" cy="47.454" id="_x30_.1.0.96.0.6.4" r="0.568"/>
         <circle  fill="#FFFFFF" cx="165.303" gorn="0.2.0.92.0.6.5" cy="47.454" id="_x30_.1.0.96.0.6.5" r="0.568"/>
         <circle  fill="#FFFFFF" cx="163.886" gorn="0.2.0.92.0.6.6" cy="47.454" id="_x30_.1.0.96.0.6.6" r="0.568"/>
         <circle  fill="#FFFFFF" cx="162.469" gorn="0.2.0.92.0.6.7" cy="47.454" id="_x30_.1.0.96.0.6.7" r="0.568"/>
         <circle  fill="#FFFFFF" cx="161.051" gorn="0.2.0.92.0.6.8" cy="47.454" id="_x30_.1.0.96.0.6.8" r="0.568"/>
         <circle  fill="#FFFFFF" cx="159.635" gorn="0.2.0.92.0.6.9" cy="47.454" id="_x30_.1.0.96.0.6.9" r="0.568"/>
         <circle  fill="#FFFFFF" cx="158.217" gorn="0.2.0.92.0.6.10" cy="47.454" id="_x30_.1.0.96.0.6.10" r="0.568"/>
         <circle  fill="#FFFFFF" cx="156.801" gorn="0.2.0.92.0.6.11" cy="47.454" id="_x30_.1.0.96.0.6.11" r="0.568"/>
         <circle  fill="#FFFFFF" cx="155.383" gorn="0.2.0.92.0.6.12" cy="47.454" id="_x30_.1.0.96.0.6.12" r="0.568"/>
         <circle  fill="#FFFFFF" cx="153.967" gorn="0.2.0.92.0.6.13" cy="47.454" id="_x30_.1.0.96.0.6.13" r="0.568"/>
        </g>
       </g>
       <g  gorn="0.2.0.92.1" id="_x30_.1.0.96.1">
        <path  fill="#FFFFFF" gorn="0.2.0.92.1.0" id="_x30_.1.0.96.1.0" d="M154.165,44.561c-0.994,0,-1.742,-0.206,-2.244,-0.618c-0.485,-0.401,-0.799,-0.879,-0.936,-1.434c-0.07,-0.28,-0.119,-0.58,-0.15,-0.899c-0.027,-0.319,-0.045,-0.661,-0.045,-1.025l0,-5.236l0.939,0l0,5.22c0,1.183,0.189,2.117,0.572,2.498c0.377,0.375,0.932,0.563,1.664,0.563c0.738,0,1.494,-0.188,1.871,-0.563c0.381,-0.38,0.572,-1.314,0.572,-2.498l0,-5.22l0.959,0l0,5.236c0,1.088,-0.125,1.896,-0.377,2.424C156.491,44.044,155.67,44.561,154.165,44.561z"/>
        <path  fill="#FFFFFF" gorn="0.2.0.92.1.1" id="_x30_.1.0.96.1.1" d="M166.251,44.39l-0.944,0l-4.742,-7.433l0,7.446l-0.797,0l0,-9.054l0.88,0l4.659,7.455l0,-7.455l0.944,0L166.251,44.39z"/>
        <path  fill="#FFFFFF" gorn="0.2.0.92.1.2" id="_x30_.1.0.96.1.2" d="M171.911,35.131c0.576,0,1.107,0.115,1.594,0.346c0.488,0.231,0.906,0.555,1.256,0.975c0.354,0.42,0.623,0.926,0.818,1.517c0.196,0.59,0.295,1.247,0.295,1.968c0,0.72,-0.099,1.376,-0.295,1.966c-0.195,0.592,-0.468,1.099,-0.818,1.521c-0.35,0.422,-0.77,0.749,-1.256,0.979c-0.483,0.23,-1.018,0.345,-1.594,0.345c-0.58,0,-1.113,-0.115,-1.602,-0.345c-0.484,-0.231,-0.904,-0.557,-1.258,-0.979c-0.354,-0.422,-0.629,-0.93,-0.823,-1.521c-0.194,-0.589,-0.294,-1.246,-0.294,-1.966c0,-0.721,0.1,-1.377,0.294,-1.968c0.194,-0.591,0.47,-1.097,0.823,-1.517c0.353,-0.42,0.773,-0.745,1.258,-0.975C170.795,35.247,171.331,35.131,171.911,35.131zM171.905,43.692c0.41,0,0.789,-0.085,1.135,-0.256s0.646,-0.418,0.896,-0.74c0.251,-0.323,0.447,-0.716,0.588,-1.179c0.141,-0.464,0.211,-0.991,0.211,-1.581c0,-0.591,-0.07,-1.118,-0.211,-1.582c-0.141,-0.463,-0.335,-0.856,-0.585,-1.179c-0.248,-0.322,-0.545,-0.568,-0.888,-0.736c-0.346,-0.167,-0.719,-0.252,-1.125,-0.252c-0.412,0,-0.793,0.084,-1.141,0.252c-0.352,0.168,-0.65,0.412,-0.904,0.732s-0.451,0.713,-0.596,1.178c-0.144,0.467,-0.216,0.995,-0.216,1.586c0,0.59,0.07,1.117,0.214,1.581c0.141,0.463,0.336,0.856,0.588,1.179c0.25,0.322,0.551,0.569,0.896,0.74C171.113,43.606,171.493,43.692,171.905,43.692z"/>
       </g>
      </g>
     </g>
     <g transform="matrix(1, 0, 0, 1, 157.652, 140.628)">
      <g >
       <g >
        <g >
         <g  gorn="0.2.1.0.0.0" id="_x30_.1.1">
          <g  gorn="0.2.1.0.0.0.0" id="_x31_x06">
           <rect  width="43.199" x="0.722" y="-0.228" fill="#404040" gorn="0.2.1.0.0.0.0.0" height="7.199" id="_x30_.1.1.0.0"/>
           <rect  width="2.781" x="2.931" y="1.981" gorn="0.2.1.0.0.0.0.1" height="2.783" id="_x30_.1.1.0.1"/>
           <polygon  fill="#2A2A29" points="1.905,0.956,2.929,1.981,5.714,1.981,6.737,0.956" gorn="0.2.1.0.0.0.0.2" id="_x30_.1.1.0.2"/>
           <polygon  fill="#474747" points="6.737,0.956,5.714,1.985,5.714,4.766,6.737,5.789" gorn="0.2.1.0.0.0.0.3" id="_x30_.1.1.0.3"/>
           <polygon  fill="#595959" points="6.737,5.789,5.712,4.766,2.929,4.766,1.905,5.789" gorn="0.2.1.0.0.0.0.4" id="_x30_.1.1.0.4"/>
           <polygon  fill="#373737" points="1.903,5.789,2.929,4.764,2.929,1.981,1.903,0.956" gorn="0.2.1.0.0.0.0.5" id="_x30_.1.1.0.5"/>
           <rect  width="2.781" x="10.132" y="1.981" gorn="0.2.1.0.0.0.0.6" height="2.783" id="_x30_.1.1.0.6"/>
           <polygon  fill="#2A2A29" points="9.104,0.956,10.13,1.981,12.911,1.981,13.936,0.956" gorn="0.2.1.0.0.0.0.7" id="_x30_.1.1.0.7"/>
           <polygon  fill="#474747" points="13.936,0.956,12.911,1.985,12.911,4.766,13.936,5.789" gorn="0.2.1.0.0.0.0.8" id="_x30_.1.1.0.8"/>
           <polygon  fill="#595959" points="13.936,5.789,12.911,4.766,10.13,4.766,9.104,5.789" gorn="0.2.1.0.0.0.0.9" id="_x30_.1.1.0.9"/>
           <polygon  fill="#373737" points="9.102,5.789,10.13,4.764,10.13,1.981,9.102,0.956" gorn="0.2.1.0.0.0.0.10" id="_x30_.1.1.0.10"/>
           <rect  width="2.781" x="17.331" y="1.981" gorn="0.2.1.0.0.0.0.11" height="2.783" id="_x30_.1.1.0.11"/>
           <polygon  fill="#2A2A29" points="16.306,0.956,17.329,1.981,20.112,1.981,21.138,0.956" gorn="0.2.1.0.0.0.0.12" id="_x30_.1.1.0.12"/>
           <polygon  fill="#474747" points="21.138,0.956,20.112,1.985,20.112,4.766,21.138,5.789" gorn="0.2.1.0.0.0.0.13" id="_x30_.1.1.0.13"/>
           <polygon  fill="#595959" points="21.138,5.789,20.112,4.766,17.329,4.766,16.306,5.789" gorn="0.2.1.0.0.0.0.14" id="_x30_.1.1.0.14"/>
           <polygon  fill="#373737" points="16.304,5.789,17.329,4.764,17.329,1.981,16.304,0.956" gorn="0.2.1.0.0.0.0.15" id="_x30_.1.1.0.15"/>
           <rect  width="2.781" x="24.532" y="1.981" gorn="0.2.1.0.0.0.0.16" height="2.783" id="_x30_.1.1.0.16"/>
           <polygon  fill="#2A2A29" points="23.507,0.956,24.53,1.981,27.313,1.981,28.339,0.956" gorn="0.2.1.0.0.0.0.17" id="_x30_.1.1.0.17"/>
           <polygon  fill="#474747" points="28.339,0.956,27.313,1.985,27.313,4.766,28.339,5.789" gorn="0.2.1.0.0.0.0.18" id="_x30_.1.1.0.18"/>
           <polygon  fill="#595959" points="28.337,5.789,27.311,4.766,24.53,4.766,23.507,5.789" gorn="0.2.1.0.0.0.0.19" id="_x30_.1.1.0.19"/>
           <polygon  fill="#373737" points="23.503,5.789,24.53,4.764,24.53,1.981,23.503,0.956" gorn="0.2.1.0.0.0.0.20" id="_x30_.1.1.0.20"/>
           <rect  width="2.779" x="31.731" y="1.981" gorn="0.2.1.0.0.0.0.21" height="2.783" id="_x30_.1.1.0.21"/>
           <polygon  fill="#2A2A29" points="30.706,0.956,31.729,1.981,34.513,1.981,35.538,0.956" gorn="0.2.1.0.0.0.0.22" id="_x30_.1.1.0.22"/>
           <polygon  fill="#474747" points="35.538,0.956,34.513,1.985,34.513,4.766,35.538,5.789" gorn="0.2.1.0.0.0.0.23" id="_x30_.1.1.0.23"/>
           <polygon  fill="#595959" points="35.536,5.789,34.513,4.766,31.729,4.766,30.706,5.789" gorn="0.2.1.0.0.0.0.24" id="_x30_.1.1.0.24"/>
           <polygon  fill="#373737" points="30.704,5.789,31.729,4.764,31.729,1.981,30.704,0.956" gorn="0.2.1.0.0.0.0.25" id="_x30_.1.1.0.25"/>
           <rect  width="2.781" x="38.931" y="1.981" gorn="0.2.1.0.0.0.0.26" height="2.783" id="_x30_.1.1.0.26"/>
           <polygon  fill="#2A2A29" points="37.905,0.956,38.929,1.981,41.714,1.981,42.737,0.956" gorn="0.2.1.0.0.0.0.27" id="_x30_.1.1.0.27"/>
           <polygon  fill="#474747" points="42.737,0.956,41.714,1.985,41.714,4.766,42.737,5.789" gorn="0.2.1.0.0.0.0.28" id="_x30_.1.1.0.28"/>
           <polygon  fill="#595959" points="42.737,5.789,41.712,4.766,38.929,4.766,37.905,5.789" gorn="0.2.1.0.0.0.0.29" id="_x30_.1.1.0.29"/>
           <polygon  fill="#373737" points="37.903,5.789,38.929,4.764,38.929,1.981,37.903,0.956" gorn="0.2.1.0.0.0.0.30" id="_x30_.1.1.0.30"/>
          </g>
         </g>
        </g>
       </g>
      </g>
     </g>
     <g transform="matrix(1, 0, 0, 1, 191.155, 64.2515)">
      <g >
       <g >
        <g >
         <g  gorn="0.2.2.0.0.0" id="_x30_.1.2">
          <g  gorn="0.2.2.0.0.0.0" id="_x32_x03">
           <g transform="matrix(0, -1, 1, 0, 3.52001, 17.793)">
            <g >
             <g >
              <g >
               <g  gorn="0.2.2.0.0.0.0.0.0.0.0" id="_x30_.1.2.0.0">
                <g  gorn="0.2.2.0.0.0.0.0.0.0.0.0" id="_x30_.1.2.0.0.0">
                 <g  gorn="0.2.2.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.2.0.0.0.0">
                  <polygon  fill="#404040" points="20.748,12.861,20.748,8.927,20.748,5.587,20.748,1.654,19.236,0.143,15.306,0.143,13.796,1.654,13.796,5.587,13.796,8.927,13.796,12.861,15.306,14.372,19.236,14.372" gorn="0.2.2.0.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.2.0.0.0.0.0"/>
                  <polygon  fill="#404040" points="13.566,12.861,13.566,8.927,13.566,5.587,13.566,1.654,12.057,0.143,8.125,0.143,6.611,1.654,6.611,5.587,6.611,8.927,6.611,12.861,8.125,14.372,12.057,14.372" gorn="0.2.2.0.0.0.0.0.0.0.0.0.0.1" id="_x30_.1.2.0.0.0.0.1"/>
                  <polygon  fill="#404040" points="6.389,12.861,6.389,8.927,6.389,5.587,6.389,1.654,4.877,0.143,0.942,0.143,-0.565,1.654,-0.565,5.587,-0.565,8.927,-0.565,12.861,0.942,14.372,4.877,14.372" gorn="0.2.2.0.0.0.0.0.0.0.0.0.0.2" id="_x30_.1.2.0.0.0.0.2"/>
                  <polygon  fill="#404040" points="20.748,12.861,20.748,8.927,20.748,5.587,20.748,1.654,19.236,0.143,15.306,0.143,13.796,1.654,13.796,5.587,13.796,8.927,13.796,12.861,15.306,14.372,19.236,14.372" gorn="0.2.2.0.0.0.0.0.0.0.0.0.0.3" id="_x30_.1.2.0.0.0.0.3"/>
                  <polygon  fill="#404040" points="13.566,12.861,13.566,8.927,13.566,5.587,13.566,1.654,12.057,0.143,8.125,0.143,6.611,1.654,6.611,5.587,6.611,8.927,6.611,12.861,8.125,14.372,12.057,14.372" gorn="0.2.2.0.0.0.0.0.0.0.0.0.0.4" id="_x30_.1.2.0.0.0.0.4"/>
                  <polygon  fill="#404040" points="6.389,12.861,6.389,8.927,6.389,5.587,6.389,1.654,4.877,0.143,0.942,0.143,-0.565,1.654,-0.565,5.587,-0.565,8.927,-0.565,12.861,0.942,14.372,4.877,14.372" gorn="0.2.2.0.0.0.0.0.0.0.0.0.0.5" id="_x30_.1.2.0.0.0.0.5"/>
                  <g transform="matrix(-2.54711e-06, -1, 1, -2.54711e-06, -0.656, 6.746)">
                   <g >
                    <g >
                     <g >
                      <g  gorn="0.2.2.0.0.0.0.0.0.0.0.0.0.6.0.0.0" id="_x30_.1.2.0.0.0.0.6">
                       <rect  width="2.298" x="1.898" y="2.555" fill="#8D8C8C" gorn="0.2.2.0.0.0.0.0.0.0.0.0.0.6.0.0.0.0" height="2.299" id="_x30_.1.2.0.0.0.0.6.0"/>
                      </g>
                     </g>
                    </g>
                   </g>
                  </g>
                  <g transform="matrix(-2.54711e-06, -1, 1, -2.54711e-06, -7.8547, 13.9447)">
                   <g >
                    <g >
                     <g >
                      <g  gorn="0.2.2.0.0.0.0.0.0.0.0.0.0.7.0.0.0" id="_x30_.1.2.0.0.0.0.7">
                       <rect  width="2.297" x="1.9" y="9.754" fill="#8D8C8C" gorn="0.2.2.0.0.0.0.0.0.0.0.0.0.7.0.0.0.0" height="2.299" id="_x30_.1.2.0.0.0.0.7.0"/>
                      </g>
                     </g>
                    </g>
                   </g>
                  </g>
                  <g transform="matrix(-2.54711e-06, -1, 1, -2.54711e-06, 6.5428, 13.9447)">
                   <g >
                    <g >
                     <g >
                      <g  gorn="0.2.2.0.0.0.0.0.0.0.0.0.0.8.0.0.0" id="_x30_.1.2.0.0.0.0.8">
                       <rect  width="2.299" x="9.097" y="2.556" fill="#8D8C8C" gorn="0.2.2.0.0.0.0.0.0.0.0.0.0.8.0.0.0.0" height="2.298" id="_x30_.1.2.0.0.0.0.8.0"/>
                      </g>
                     </g>
                    </g>
                   </g>
                  </g>
                  <g transform="matrix(-2.54711e-06, -1, 1, -2.54711e-06, -0.6552, 21.1442)">
                   <g >
                    <g >
                     <g >
                      <g  gorn="0.2.2.0.0.0.0.0.0.0.0.0.0.9.0.0.0" id="_x30_.1.2.0.0.0.0.9">
                       <rect  width="2.297" x="9.098" y="9.755" fill="#8D8C8C" gorn="0.2.2.0.0.0.0.0.0.0.0.0.0.9.0.0.0.0" height="2.298" id="_x30_.1.2.0.0.0.0.9.0"/>
                      </g>
                     </g>
                    </g>
                   </g>
                  </g>
                  <g transform="matrix(-2.54711e-06, -1, 1, -2.54711e-06, 13.7415, 21.1424)">
                   <g >
                    <g >
                     <g >
                      <g  gorn="0.2.2.0.0.0.0.0.0.0.0.0.0.10.0.0.0" id="_x30_.1.2.0.0.0.0.10">
                       <rect  width="2.297" x="16.297" y="2.556" fill="#8D8C8C" gorn="0.2.2.0.0.0.0.0.0.0.0.0.0.10.0.0.0.0" height="2.298" id="_x30_.1.2.0.0.0.0.10.0"/>
                      </g>
                     </g>
                    </g>
                   </g>
                  </g>
                  <g transform="matrix(-2.54711e-06, -1, 1, -2.54711e-06, 6.5423, 28.3417)">
                   <g >
                    <g >
                     <g >
                      <g  gorn="0.2.2.0.0.0.0.0.0.0.0.0.0.11.0.0.0" id="_x30_.1.2.0.0.0.0.11">
                       <rect  width="2.297" x="16.297" y="9.755" fill="#8D8455" gorn="0.2.2.0.0.0.0.0.0.0.0.0.0.11.0.0.0.0" height="2.298" id="_x30_.1.2.0.0.0.0.11.0"/>
                      </g>
                     </g>
                    </g>
                   </g>
                  </g>
                  <g transform="matrix(-2.54711e-06, -1, 1, -2.54711e-06, 6.5401, 28.3434)">
                   <g >
                    <g >
                     <g >
                      <g  gorn="0.2.2.0.0.0.0.0.0.0.0.0.0.12.0.0.0" id="_x30_.1.2.0.0.0.0.12">
                       <rect  width="1.185" x="16.852" y="10.314" fill="#8C8663" gorn="0.2.2.0.0.0.0.0.0.0.0.0.0.12.0.0.0.0" height="1.183" id="_x30_.1.2.0.0.0.0.12.0"/>
                      </g>
                     </g>
                    </g>
                   </g>
                  </g>
                  <polygon  fill="#B8AF82" points="18.594,9.748,18.035,10.306,18.035,11.486,18.594,12.046" gorn="0.2.2.0.0.0.0.0.0.0.0.0.0.13" id="_x30_.1.2.0.0.0.0.13"/>
                  <polygon  fill="#80795B" points="16.855,11.486,18.035,11.486,18.594,12.046,16.297,12.046" gorn="0.2.2.0.0.0.0.0.0.0.0.0.0.14" id="_x30_.1.2.0.0.0.0.14"/>
                  <polygon  fill="#5E5B43" points="16.855,10.306,16.855,11.486,16.297,12.046,16.297,9.748" gorn="0.2.2.0.0.0.0.0.0.0.0.0.0.15" id="_x30_.1.2.0.0.0.0.15"/>
                  <polygon  fill="#9A916C" points="18.594,9.748,18.035,10.306,16.855,10.306,16.297,9.748" gorn="0.2.2.0.0.0.0.0.0.0.0.0.0.16" id="_x30_.1.2.0.0.0.0.16"/>
                  <g transform="matrix(-2.54711e-06, -1, 1, -2.54711e-06, 13.7423, 21.1432)">
                   <g >
                    <g >
                     <g >
                      <g  gorn="0.2.2.0.0.0.0.0.0.0.0.0.0.17.0.0.0" id="_x30_.1.2.0.0.0.0.17">
                       <rect  width="1.185" x="16.853" y="3.113" fill="#8C8663" gorn="0.2.2.0.0.0.0.0.0.0.0.0.0.17.0.0.0.0" height="1.183" id="_x30_.1.2.0.0.0.0.17.0"/>
                      </g>
                     </g>
                    </g>
                   </g>
                  </g>
                  <polygon  fill="#B8AF82" points="18.594,2.55,18.035,3.107,18.035,4.287,18.594,4.845" gorn="0.2.2.0.0.0.0.0.0.0.0.0.0.18" id="_x30_.1.2.0.0.0.0.18"/>
                  <polygon  fill="#80795B" points="16.855,4.287,18.035,4.287,18.594,4.845,16.297,4.845" gorn="0.2.2.0.0.0.0.0.0.0.0.0.0.19" id="_x30_.1.2.0.0.0.0.19"/>
                  <polygon  fill="#5E5B43" points="16.855,3.107,16.855,4.287,16.297,4.845,16.297,2.55" gorn="0.2.2.0.0.0.0.0.0.0.0.0.0.20" id="_x30_.1.2.0.0.0.0.20"/>
                  <polygon  fill="#9A916C" points="18.594,2.55,18.035,3.107,16.855,3.107,16.297,2.55" gorn="0.2.2.0.0.0.0.0.0.0.0.0.0.21" id="_x30_.1.2.0.0.0.0.21"/>
                  <g transform="matrix(-2.54711e-06, -1, 1, -2.54711e-06, -0.6572, 21.1461)">
                   <g >
                    <g >
                     <g >
                      <g  gorn="0.2.2.0.0.0.0.0.0.0.0.0.0.22.0.0.0" id="_x30_.1.2.0.0.0.0.22">
                       <rect  width="1.185" x="9.656" y="10.314" fill="#8C8663" gorn="0.2.2.0.0.0.0.0.0.0.0.0.0.22.0.0.0.0" height="1.184" id="_x30_.1.2.0.0.0.0.22.0"/>
                      </g>
                     </g>
                    </g>
                   </g>
                  </g>
                  <polygon  fill="#B8AF82" points="11.396,9.748,10.839,10.306,10.839,11.486,11.396,12.046" gorn="0.2.2.0.0.0.0.0.0.0.0.0.0.23" id="_x30_.1.2.0.0.0.0.23"/>
                  <polygon  fill="#80795B" points="9.655,11.486,10.839,11.486,11.396,12.046,9.099,12.046" gorn="0.2.2.0.0.0.0.0.0.0.0.0.0.24" id="_x30_.1.2.0.0.0.0.24"/>
                  <polygon  fill="#5E5B43" points="9.655,10.306,9.655,11.486,9.099,12.046,9.099,9.748" gorn="0.2.2.0.0.0.0.0.0.0.0.0.0.25" id="_x30_.1.2.0.0.0.0.25"/>
                  <polygon  fill="#9A916C" points="11.396,9.748,10.839,10.306,9.655,10.306,9.099,9.748" gorn="0.2.2.0.0.0.0.0.0.0.0.0.0.26" id="_x30_.1.2.0.0.0.0.26"/>
                  <g transform="matrix(-2.54711e-06, -1, 1, -2.54711e-06, 6.543, 13.9439)">
                   <g >
                    <g >
                     <g >
                      <g  gorn="0.2.2.0.0.0.0.0.0.0.0.0.0.27.0.0.0" id="_x30_.1.2.0.0.0.0.27">
                       <rect  width="1.185" x="9.655" y="3.112" fill="#8C8663" gorn="0.2.2.0.0.0.0.0.0.0.0.0.0.27.0.0.0.0" height="1.184" id="_x30_.1.2.0.0.0.0.27.0"/>
                      </g>
                     </g>
                    </g>
                   </g>
                  </g>
                  <polygon  fill="#B8AF82" points="11.396,2.55,10.839,3.107,10.839,4.287,11.396,4.845" gorn="0.2.2.0.0.0.0.0.0.0.0.0.0.28" id="_x30_.1.2.0.0.0.0.28"/>
                  <polygon  fill="#80795B" points="9.655,4.287,10.839,4.287,11.396,4.845,9.099,4.845" gorn="0.2.2.0.0.0.0.0.0.0.0.0.0.29" id="_x30_.1.2.0.0.0.0.29"/>
                  <polygon  fill="#5E5B43" points="9.655,3.107,9.655,4.287,9.099,4.845,9.099,2.55" gorn="0.2.2.0.0.0.0.0.0.0.0.0.0.30" id="_x30_.1.2.0.0.0.0.30"/>
                  <polygon  fill="#9A916C" points="11.396,2.55,10.839,3.107,9.655,3.107,9.099,2.55" gorn="0.2.2.0.0.0.0.0.0.0.0.0.0.31" id="_x30_.1.2.0.0.0.0.31"/>
                  <g transform="matrix(-2.54711e-06, -1, 1, -2.54711e-06, -7.8591, 13.9442)">
                   <g >
                    <g >
                     <g >
                      <g  gorn="0.2.2.0.0.0.0.0.0.0.0.0.0.32.0.0.0" id="_x30_.1.2.0.0.0.0.32">
                       <rect  width="1.184" x="2.454" y="10.313" fill="#8C8663" gorn="0.2.2.0.0.0.0.0.0.0.0.0.0.32.0.0.0.0" height="1.185" id="_x30_.1.2.0.0.0.0.32.0"/>
                      </g>
                     </g>
                    </g>
                   </g>
                  </g>
                  <polygon  fill="#B8AF82" points="4.196,9.748,3.639,10.306,3.639,11.486,4.196,12.046" gorn="0.2.2.0.0.0.0.0.0.0.0.0.0.33" id="_x30_.1.2.0.0.0.0.33"/>
                  <polygon  fill="#80795B" points="2.454,11.486,3.639,11.486,4.196,12.046,1.899,12.046" gorn="0.2.2.0.0.0.0.0.0.0.0.0.0.34" id="_x30_.1.2.0.0.0.0.34"/>
                  <polygon  fill="#5E5B43" points="2.454,10.306,2.454,11.486,1.899,12.046,1.899,9.748" gorn="0.2.2.0.0.0.0.0.0.0.0.0.0.35" id="_x30_.1.2.0.0.0.0.35"/>
                  <polygon  fill="#9A916C" points="4.196,9.748,3.639,10.306,2.454,10.306,1.899,9.748" gorn="0.2.2.0.0.0.0.0.0.0.0.0.0.36" id="_x30_.1.2.0.0.0.0.36"/>
                  <g transform="matrix(-2.54711e-06, -1, 1, -2.54711e-06, -0.6574, 6.7435)">
                   <g >
                    <g >
                     <g >
                      <g  gorn="0.2.2.0.0.0.0.0.0.0.0.0.0.37.0.0.0" id="_x30_.1.2.0.0.0.0.37">
                       <rect  width="1.184" x="2.455" y="3.111" fill="#8C8663" gorn="0.2.2.0.0.0.0.0.0.0.0.0.0.37.0.0.0.0" height="1.187" id="_x30_.1.2.0.0.0.0.37.0"/>
                      </g>
                     </g>
                    </g>
                   </g>
                  </g>
                  <polygon  fill="#B8AF82" points="4.196,2.55,3.639,3.107,3.639,4.287,4.196,4.846" gorn="0.2.2.0.0.0.0.0.0.0.0.0.0.38" id="_x30_.1.2.0.0.0.0.38"/>
                  <polygon  fill="#80795B" points="2.454,4.287,3.639,4.287,4.196,4.846,1.899,4.846" gorn="0.2.2.0.0.0.0.0.0.0.0.0.0.39" id="_x30_.1.2.0.0.0.0.39"/>
                  <polygon  fill="#5E5B43" points="2.454,3.107,2.454,4.287,1.899,4.846,1.899,2.55" gorn="0.2.2.0.0.0.0.0.0.0.0.0.0.40" id="_x30_.1.2.0.0.0.0.40"/>
                  <polygon  fill="#9A916C" points="4.196,2.55,3.639,3.107,2.454,3.107,1.899,2.55" gorn="0.2.2.0.0.0.0.0.0.0.0.0.0.41" id="_x30_.1.2.0.0.0.0.41"/>
                 </g>
                </g>
               </g>
              </g>
             </g>
            </g>
           </g>
          </g>
         </g>
        </g>
       </g>
      </g>
     </g>
     <g transform="matrix(1, 0, 0, 1, 59.7671, 12.9035)">
      <g >
       <g >
        <g >
         <g  gorn="0.2.3.0.0.0" id="_x30_.1.3">
          <g  gorn="0.2.3.0.0.0.0" id="_x32_x03_1_">
           <g transform="matrix(-1, 0, 0, -1, 21.313, 14.273)">
            <g >
             <g >
              <g >
               <g  gorn="0.2.3.0.0.0.0.0.0.0.0" id="_x30_.1.3.0.0">
                <g  gorn="0.2.3.0.0.0.0.0.0.0.0.0" id="_x30_.1.3.0.0.0">
                 <g  gorn="0.2.3.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.3.0.0.0.0">
                  <polygon  fill="#404040" points="21.925,12.619,21.925,8.687,21.925,5.347,21.925,1.413,20.414,-0.098,16.483,-0.098,14.973,1.413,14.973,5.347,14.973,8.687,14.973,12.619,16.483,14.131,20.414,14.131" gorn="0.2.3.0.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.3.0.0.0.0.0"/>
                  <polygon  fill="#404040" points="14.743,12.619,14.743,8.687,14.743,5.347,14.743,1.413,13.234,-0.098,9.302,-0.098,7.789,1.413,7.789,5.347,7.789,8.687,7.789,12.619,9.302,14.131,13.234,14.131" gorn="0.2.3.0.0.0.0.0.0.0.0.0.0.1" id="_x30_.1.3.0.0.0.0.1"/>
                  <polygon  fill="#404040" points="7.566,12.619,7.566,8.687,7.566,5.347,7.566,1.413,6.054,-0.098,2.121,-0.098,0.612,1.413,0.612,5.347,0.612,8.687,0.612,12.619,2.121,14.131,6.054,14.131" gorn="0.2.3.0.0.0.0.0.0.0.0.0.0.2" id="_x30_.1.3.0.0.0.0.2"/>
                  <polygon  fill="#404040" points="21.925,12.619,21.925,8.687,21.925,5.347,21.925,1.413,20.414,-0.098,16.483,-0.098,14.973,1.413,14.973,5.347,14.973,8.687,14.973,12.619,16.483,14.131,20.414,14.131" gorn="0.2.3.0.0.0.0.0.0.0.0.0.0.3" id="_x30_.1.3.0.0.0.0.3"/>
                  <polygon  fill="#404040" points="14.743,12.619,14.743,8.687,14.743,5.347,14.743,1.413,13.234,-0.098,9.302,-0.098,7.789,1.413,7.789,5.347,7.789,8.687,7.789,12.619,9.302,14.131,13.234,14.131" gorn="0.2.3.0.0.0.0.0.0.0.0.0.0.4" id="_x30_.1.3.0.0.0.0.4"/>
                  <polygon  fill="#404040" points="7.566,12.619,7.566,8.687,7.566,5.347,7.566,1.413,6.054,-0.098,2.121,-0.098,0.612,1.413,0.612,5.347,0.612,8.687,0.612,12.619,2.121,14.131,6.054,14.131" gorn="0.2.3.0.0.0.0.0.0.0.0.0.0.5" id="_x30_.1.3.0.0.0.0.5"/>
                  <rect  width="2.299" x="3.073" y="2.311" fill="#8D8C8C" gorn="0.2.3.0.0.0.0.0.0.0.0.0.0.6" height="2.298" id="_x30_.1.3.0.0.0.0.6"/>
                  <rect  width="2.299" x="3.073" y="9.51" fill="#8D8C8C" gorn="0.2.3.0.0.0.0.0.0.0.0.0.0.7" height="2.298" id="_x30_.1.3.0.0.0.0.7"/>
                  <rect  width="2.298" x="10.272" y="2.311" fill="#8D8C8C" gorn="0.2.3.0.0.0.0.0.0.0.0.0.0.8" height="2.298" id="_x30_.1.3.0.0.0.0.8"/>
                  <rect  width="2.298" x="10.272" y="9.51" fill="#8D8C8C" gorn="0.2.3.0.0.0.0.0.0.0.0.0.0.9" height="2.298" id="_x30_.1.3.0.0.0.0.9"/>
                  <rect  width="2.298" x="17.47" y="2.311" fill="#8D8C8C" gorn="0.2.3.0.0.0.0.0.0.0.0.0.0.10" height="2.298" id="_x30_.1.3.0.0.0.0.10"/>
                  <rect  width="2.298" x="17.47" y="9.51" fill="#8D8455" gorn="0.2.3.0.0.0.0.0.0.0.0.0.0.11" height="2.298" id="_x30_.1.3.0.0.0.0.11"/>
                  <rect  width="1.183" x="18.028" y="10.069" fill="#8C8663" gorn="0.2.3.0.0.0.0.0.0.0.0.0.0.12" height="1.184" id="_x30_.1.3.0.0.0.0.12"/>
                  <polygon  fill="#B8AF82" points="19.769,9.51,19.209,10.069,19.209,11.25,19.769,11.808" gorn="0.2.3.0.0.0.0.0.0.0.0.0.0.13" id="_x30_.1.3.0.0.0.0.13"/>
                  <polygon  fill="#80795B" points="18.028,11.25,19.209,11.25,19.769,11.808,17.47,11.808" gorn="0.2.3.0.0.0.0.0.0.0.0.0.0.14" id="_x30_.1.3.0.0.0.0.14"/>
                  <polygon  fill="#5E5B43" points="18.028,10.069,18.028,11.25,17.47,11.808,17.47,9.51" gorn="0.2.3.0.0.0.0.0.0.0.0.0.0.15" id="_x30_.1.3.0.0.0.0.15"/>
                  <polygon  fill="#9A916C" points="19.769,9.51,19.209,10.069,18.028,10.069,17.47,9.51" gorn="0.2.3.0.0.0.0.0.0.0.0.0.0.16" id="_x30_.1.3.0.0.0.0.16"/>
                  <rect  width="1.183" x="18.028" y="2.869" fill="#8C8663" gorn="0.2.3.0.0.0.0.0.0.0.0.0.0.17" height="1.182" id="_x30_.1.3.0.0.0.0.17"/>
                  <polygon  fill="#B8AF82" points="19.769,2.311,19.209,2.869,19.209,4.05,19.769,4.608" gorn="0.2.3.0.0.0.0.0.0.0.0.0.0.18" id="_x30_.1.3.0.0.0.0.18"/>
                  <polygon  fill="#80795B" points="18.028,4.05,19.209,4.05,19.769,4.608,17.47,4.608" gorn="0.2.3.0.0.0.0.0.0.0.0.0.0.19" id="_x30_.1.3.0.0.0.0.19"/>
                  <polygon  fill="#5E5B43" points="18.028,2.869,18.028,4.05,17.47,4.608,17.47,2.311" gorn="0.2.3.0.0.0.0.0.0.0.0.0.0.20" id="_x30_.1.3.0.0.0.0.20"/>
                  <polygon  fill="#9A916C" points="19.769,2.311,19.209,2.869,18.028,2.869,17.47,2.311" gorn="0.2.3.0.0.0.0.0.0.0.0.0.0.21" id="_x30_.1.3.0.0.0.0.21"/>
                  <rect  width="1.184" x="10.829" y="10.069" fill="#8C8663" gorn="0.2.3.0.0.0.0.0.0.0.0.0.0.22" height="1.184" id="_x30_.1.3.0.0.0.0.22"/>
                  <polygon  fill="#B8AF82" points="12.569,9.51,12.012,10.069,12.012,11.25,12.569,11.808" gorn="0.2.3.0.0.0.0.0.0.0.0.0.0.23" id="_x30_.1.3.0.0.0.0.23"/>
                  <polygon  fill="#80795B" points="10.829,11.25,12.012,11.25,12.569,11.808,10.272,11.808" gorn="0.2.3.0.0.0.0.0.0.0.0.0.0.24" id="_x30_.1.3.0.0.0.0.24"/>
                  <polygon  fill="#5E5B43" points="10.829,10.069,10.829,11.25,10.272,11.808,10.272,9.51" gorn="0.2.3.0.0.0.0.0.0.0.0.0.0.25" id="_x30_.1.3.0.0.0.0.25"/>
                  <polygon  fill="#9A916C" points="12.569,9.51,12.012,10.069,10.829,10.069,10.272,9.51" gorn="0.2.3.0.0.0.0.0.0.0.0.0.0.26" id="_x30_.1.3.0.0.0.0.26"/>
                  <rect  width="1.184" x="10.829" y="2.869" fill="#8C8663" gorn="0.2.3.0.0.0.0.0.0.0.0.0.0.27" height="1.182" id="_x30_.1.3.0.0.0.0.27"/>
                  <polygon  fill="#B8AF82" points="12.569,2.311,12.012,2.869,12.012,4.05,12.569,4.608" gorn="0.2.3.0.0.0.0.0.0.0.0.0.0.28" id="_x30_.1.3.0.0.0.0.28"/>
                  <polygon  fill="#80795B" points="10.829,4.05,12.012,4.05,12.569,4.608,10.272,4.608" gorn="0.2.3.0.0.0.0.0.0.0.0.0.0.29" id="_x30_.1.3.0.0.0.0.29"/>
                  <polygon  fill="#5E5B43" points="10.829,2.869,10.829,4.05,10.272,4.608,10.272,2.311" gorn="0.2.3.0.0.0.0.0.0.0.0.0.0.30" id="_x30_.1.3.0.0.0.0.30"/>
                  <polygon  fill="#9A916C" points="12.569,2.311,12.012,2.869,10.829,2.869,10.272,2.311" gorn="0.2.3.0.0.0.0.0.0.0.0.0.0.31" id="_x30_.1.3.0.0.0.0.31"/>
                  <rect  width="1.185" x="3.628" y="10.069" fill="#8C8663" gorn="0.2.3.0.0.0.0.0.0.0.0.0.0.32" height="1.184" id="_x30_.1.3.0.0.0.0.32"/>
                  <polygon  fill="#B8AF82" points="5.371,9.51,4.813,10.069,4.813,11.25,5.371,11.808" gorn="0.2.3.0.0.0.0.0.0.0.0.0.0.33" id="_x30_.1.3.0.0.0.0.33"/>
                  <polygon  fill="#80795B" points="3.628,11.25,4.813,11.25,5.371,11.808,3.073,11.808" gorn="0.2.3.0.0.0.0.0.0.0.0.0.0.34" id="_x30_.1.3.0.0.0.0.34"/>
                  <polygon  fill="#5E5B43" points="3.628,10.069,3.628,11.25,3.073,11.808,3.073,9.51" gorn="0.2.3.0.0.0.0.0.0.0.0.0.0.35" id="_x30_.1.3.0.0.0.0.35"/>
                  <polygon  fill="#9A916C" points="5.371,9.51,4.813,10.069,3.628,10.069,3.073,9.51" gorn="0.2.3.0.0.0.0.0.0.0.0.0.0.36" id="_x30_.1.3.0.0.0.0.36"/>
                  <rect  width="1.185" x="3.628" y="2.869" fill="#8C8663" gorn="0.2.3.0.0.0.0.0.0.0.0.0.0.37" height="1.182" id="_x30_.1.3.0.0.0.0.37"/>
                  <polygon  fill="#B8AF82" points="5.371,2.311,4.813,2.869,4.813,4.05,5.371,4.608" gorn="0.2.3.0.0.0.0.0.0.0.0.0.0.38" id="_x30_.1.3.0.0.0.0.38"/>
                  <polygon  fill="#80795B" points="3.628,4.05,4.813,4.05,5.371,4.608,3.073,4.608" gorn="0.2.3.0.0.0.0.0.0.0.0.0.0.39" id="_x30_.1.3.0.0.0.0.39"/>
                  <polygon  fill="#5E5B43" points="3.628,2.869,3.628,4.05,3.073,4.608,3.073,2.311" gorn="0.2.3.0.0.0.0.0.0.0.0.0.0.40" id="_x30_.1.3.0.0.0.0.40"/>
                  <polygon  fill="#9A916C" points="5.371,2.311,4.813,2.869,3.628,2.869,3.073,2.311" gorn="0.2.3.0.0.0.0.0.0.0.0.0.0.41" id="_x30_.1.3.0.0.0.0.41"/>
                 </g>
                </g>
               </g>
              </g>
             </g>
            </g>
           </g>
          </g>
         </g>
        </g>
       </g>
      </g>
     </g>
     <g transform="matrix(1, 0, 0, 1, 144.692, 3.372)">
      <g >
       <g >
        <g >
         <g  gorn="0.2.4.0.0.0" id="_x30_.1.4">
          <g  gorn="0.2.4.0.0.0.0" id="_x31_x08">
           <g transform="matrix(-1, 0, 0, -1, 57.6, 7.2)">
            <g >
             <g >
              <g >
               <g  gorn="0.2.4.0.0.0.0.0.0.0.0" id="_x30_.1.4.0.0">
                <g  gorn="0.2.4.0.0.0.0.0.0.0.0.0" id="_x30_.1.4.0.0.0">
                 <rect  width="57.6" x="0.72" y="-0.228" fill="#404040" gorn="0.2.4.0.0.0.0.0.0.0.0.0.0" height="7.199" id="_x30_.1.4.0.0.0.0"/>
                 <rect  width="2.78" x="53.331" y="1.98" gorn="0.2.4.0.0.0.0.0.0.0.0.0.1" height="2.782" id="_x30_.1.4.0.0.0.1"/>
                 <polygon  fill="#2A2A29" points="57.135,5.787,56.113,4.762,53.331,4.762,52.303,5.787" gorn="0.2.4.0.0.0.0.0.0.0.0.0.2" id="_x30_.1.4.0.0.0.2"/>
                 <polygon  fill="#474747" points="52.303,5.787,53.331,4.759,53.331,1.978,52.303,0.955" gorn="0.2.4.0.0.0.0.0.0.0.0.0.3" id="_x30_.1.4.0.0.0.3"/>
                 <polygon  fill="#595959" points="52.304,0.955,53.331,1.978,56.113,1.978,57.135,0.955" gorn="0.2.4.0.0.0.0.0.0.0.0.0.4" id="_x30_.1.4.0.0.0.4"/>
                 <polygon  fill="#373737" points="57.137,0.955,56.113,1.98,56.113,4.762,57.137,5.787" gorn="0.2.4.0.0.0.0.0.0.0.0.0.5" id="_x30_.1.4.0.0.0.5"/>
                 <rect  width="2.779" x="46.13" y="1.98" gorn="0.2.4.0.0.0.0.0.0.0.0.0.6" height="2.782" id="_x30_.1.4.0.0.0.6"/>
                 <polygon  fill="#2A2A29" points="49.937,5.787,48.913,4.762,46.128,4.762,45.103,5.787" gorn="0.2.4.0.0.0.0.0.0.0.0.0.7" id="_x30_.1.4.0.0.0.7"/>
                 <polygon  fill="#474747" points="45.103,5.787,46.128,4.759,46.128,1.978,45.103,0.955" gorn="0.2.4.0.0.0.0.0.0.0.0.0.8" id="_x30_.1.4.0.0.0.8"/>
                 <polygon  fill="#595959" points="45.105,0.955,46.13,1.978,48.913,1.978,49.937,0.955" gorn="0.2.4.0.0.0.0.0.0.0.0.0.9" id="_x30_.1.4.0.0.0.9"/>
                 <polygon  fill="#373737" points="49.939,0.955,48.913,1.98,48.913,4.762,49.939,5.787" gorn="0.2.4.0.0.0.0.0.0.0.0.0.10" id="_x30_.1.4.0.0.0.10"/>
                 <rect  width="2.781" x="38.928" y="1.98" gorn="0.2.4.0.0.0.0.0.0.0.0.0.11" height="2.782" id="_x30_.1.4.0.0.0.11"/>
                 <polygon  fill="#2A2A29" points="42.736,5.787,41.712,4.762,38.928,4.762,37.904,5.787" gorn="0.2.4.0.0.0.0.0.0.0.0.0.12" id="_x30_.1.4.0.0.0.12"/>
                 <polygon  fill="#474747" points="37.904,5.787,38.928,4.759,38.928,1.978,37.904,0.955" gorn="0.2.4.0.0.0.0.0.0.0.0.0.13" id="_x30_.1.4.0.0.0.13"/>
                 <polygon  fill="#595959" points="37.907,0.955,38.929,1.978,41.712,1.978,42.736,0.955" gorn="0.2.4.0.0.0.0.0.0.0.0.0.14" id="_x30_.1.4.0.0.0.14"/>
                 <polygon  fill="#373737" points="42.738,0.955,41.712,1.98,41.712,4.762,42.738,5.787" gorn="0.2.4.0.0.0.0.0.0.0.0.0.15" id="_x30_.1.4.0.0.0.15"/>
                 <rect  width="2.78" x="31.728" y="1.98" gorn="0.2.4.0.0.0.0.0.0.0.0.0.16" height="2.782" id="_x30_.1.4.0.0.0.16"/>
                 <polygon  fill="#2A2A29" points="35.538,5.787,34.51,4.762,31.728,4.762,30.706,5.787" gorn="0.2.4.0.0.0.0.0.0.0.0.0.17" id="_x30_.1.4.0.0.0.17"/>
                 <polygon  fill="#474747" points="30.706,5.787,31.728,4.759,31.728,1.978,30.706,0.955" gorn="0.2.4.0.0.0.0.0.0.0.0.0.18" id="_x30_.1.4.0.0.0.18"/>
                 <polygon  fill="#595959" points="30.706,0.955,31.73,1.978,34.51,1.978,35.538,0.955" gorn="0.2.4.0.0.0.0.0.0.0.0.0.19" id="_x30_.1.4.0.0.0.19"/>
                 <polygon  fill="#373737" points="35.54,0.955,34.51,1.98,34.51,4.762,35.54,5.787" gorn="0.2.4.0.0.0.0.0.0.0.0.0.20" id="_x30_.1.4.0.0.0.20"/>
                 <rect  width="2.781" x="24.529" y="1.98" gorn="0.2.4.0.0.0.0.0.0.0.0.0.21" height="2.782" id="_x30_.1.4.0.0.0.21"/>
                 <polygon  fill="#2A2A29" points="28.335,5.787,27.312,4.762,24.529,4.762,23.503,5.787" gorn="0.2.4.0.0.0.0.0.0.0.0.0.22" id="_x30_.1.4.0.0.0.22"/>
                 <polygon  fill="#474747" points="23.503,5.787,24.529,4.759,24.529,1.978,23.503,0.955" gorn="0.2.4.0.0.0.0.0.0.0.0.0.23" id="_x30_.1.4.0.0.0.23"/>
                 <polygon  fill="#595959" points="23.505,0.955,24.532,1.978,27.312,1.978,28.335,0.955" gorn="0.2.4.0.0.0.0.0.0.0.0.0.24" id="_x30_.1.4.0.0.0.24"/>
                 <polygon  fill="#373737" points="28.337,0.955,27.312,1.98,27.312,4.762,28.337,5.787" gorn="0.2.4.0.0.0.0.0.0.0.0.0.25" id="_x30_.1.4.0.0.0.25"/>
                 <rect  width="2.78" x="17.331" y="1.98" gorn="0.2.4.0.0.0.0.0.0.0.0.0.26" height="2.782" id="_x30_.1.4.0.0.0.26"/>
                 <polygon  fill="#2A2A29" points="21.135,5.787,20.113,4.762,17.331,4.762,16.303,5.787" gorn="0.2.4.0.0.0.0.0.0.0.0.0.27" id="_x30_.1.4.0.0.0.27"/>
                 <polygon  fill="#474747" points="16.303,5.787,17.331,4.759,17.331,1.978,16.303,0.955" gorn="0.2.4.0.0.0.0.0.0.0.0.0.28" id="_x30_.1.4.0.0.0.28"/>
                 <polygon  fill="#595959" points="16.304,0.955,17.331,1.978,20.113,1.978,21.135,0.955" gorn="0.2.4.0.0.0.0.0.0.0.0.0.29" id="_x30_.1.4.0.0.0.29"/>
                 <polygon  fill="#373737" points="21.137,0.955,20.113,1.98,20.113,4.762,21.137,5.787" gorn="0.2.4.0.0.0.0.0.0.0.0.0.30" id="_x30_.1.4.0.0.0.30"/>
                 <rect  width="2.779" x="10.13" y="1.98" gorn="0.2.4.0.0.0.0.0.0.0.0.0.31" height="2.782" id="_x30_.1.4.0.0.0.31"/>
                 <polygon  fill="#2A2A29" points="13.937,5.787,12.913,4.762,10.128,4.762,9.103,5.787" gorn="0.2.4.0.0.0.0.0.0.0.0.0.32" id="_x30_.1.4.0.0.0.32"/>
                 <polygon  fill="#474747" points="9.103,5.787,10.128,4.759,10.128,1.978,9.103,0.955" gorn="0.2.4.0.0.0.0.0.0.0.0.0.33" id="_x30_.1.4.0.0.0.33"/>
                 <polygon  fill="#595959" points="9.105,0.955,10.13,1.978,12.913,1.978,13.937,0.955" gorn="0.2.4.0.0.0.0.0.0.0.0.0.34" id="_x30_.1.4.0.0.0.34"/>
                 <polygon  fill="#373737" points="13.939,0.955,12.913,1.98,12.913,4.762,13.939,5.787" gorn="0.2.4.0.0.0.0.0.0.0.0.0.35" id="_x30_.1.4.0.0.0.35"/>
                 <rect  width="2.781" x="2.928" y="1.98" gorn="0.2.4.0.0.0.0.0.0.0.0.0.36" height="2.782" id="_x30_.1.4.0.0.0.36"/>
                 <polygon  fill="#2A2A29" points="6.736,5.787,5.712,4.762,2.928,4.762,1.904,5.787" gorn="0.2.4.0.0.0.0.0.0.0.0.0.37" id="_x30_.1.4.0.0.0.37"/>
                 <polygon  fill="#474747" points="1.904,5.787,2.928,4.759,2.928,1.978,1.904,0.955" gorn="0.2.4.0.0.0.0.0.0.0.0.0.38" id="_x30_.1.4.0.0.0.38"/>
                 <polygon  fill="#595959" points="1.907,0.955,2.929,1.978,5.712,1.978,6.736,0.955" gorn="0.2.4.0.0.0.0.0.0.0.0.0.39" id="_x30_.1.4.0.0.0.39"/>
                 <polygon  fill="#373737" points="6.738,0.955,5.712,1.98,5.712,4.762,6.738,5.787" gorn="0.2.4.0.0.0.0.0.0.0.0.0.40" id="_x30_.1.4.0.0.0.40"/>
                </g>
               </g>
              </g>
             </g>
            </g>
           </g>
          </g>
         </g>
        </g>
       </g>
      </g>
     </g>
     <g transform="matrix(1, 0, 0, 1, 101.471, 28.0955)">
      <g >
       <g >
        <g >
         <g  gorn="0.2.5.0.0.0" id="_x30_.1.5">
          <g  gorn="0.2.5.0.0.0.0" id="chip-led0805">
           <g transform="matrix(0, -1, 1, 0, -1.77951, 5.62951)">
            <g >
             <g >
              <g >
               <g  gorn="0.2.5.0.0.0.0.0.0.0.0" id="_x30_.1.5.0.0">
                <g  gorn="0.2.5.0.0.0.0.0.0.0.0.0" id="_x30_.1.5.0.0.0">
                 <g transform="matrix(1, 0, 0, 1, 21.5539, 31.3385)">
                  <g >
                   <g >
                    <g >
                     <g  gorn="0.2.5.0.0.0.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.5.0.0.0.0">
                      <g  gorn="0.2.5.0.0.0.0.0.0.0.0.0.0.0.0.0.0" id="led-0603_1_">
                       <line  fill="none" gorn="0.2.5.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.5.0.0.0.0.0.0" y1="-37.873" x1="-23.902" y2="-30.637" x2="-23.902"/>
                       <g transform="matrix(-2.54711e-06, -1, 1, -2.54711e-06, 12.2098, -56.1861)">
                        <g >
                         <g >
                          <g >
                           <g  gorn="0.2.5.0.0.0.0.0.0.0.0.0.0.0.0.0.0.1.0.0.0" id="_x30_.1.5.0.0.0.0.0.1">
                            <rect  width="7.348" x="-25.658" y="-36.111" fill="#F2F2F2" gorn="0.2.5.0.0.0.0.0.0.0.0.0.0.0.0.0.0.1.0.0.0.0" height="3.833" id="_x30_.1.5.0.0.0.0.0.1.0"/>
                           </g>
                          </g>
                         </g>
                        </g>
                       </g>
                       <path  fill="#22B573" gorn="0.2.5.0.0.0.0.0.0.0.0.0.0.0.0.0.0.2" fill-opacity="0.7" id="_x30_.1.5.0.0.0.0.0.2" d="M-23.902,-33.129c0,0,0.467,0.645,0.426,0.867c-0.041,0.219,0.148,0.541,0,0.676l-0.424,-0.018L-23.902,-33.129z"/>
                       <g  gorn="0.2.5.0.0.0.0.0.0.0.0.0.0.0.0.0.0.3" id="_x30_.1.5.0.0.0.0.0.3">
                        <g transform="matrix(-2.54711e-06, -1, 1, -2.54711e-06, 12.3107, -56.2284)">
                         <g >
                          <g >
                           <g >
                            <g  gorn="0.2.5.0.0.0.0.0.0.0.0.0.0.0.0.0.0.3.0.0.0.0" id="_x30_.1.5.0.0.0.0.0.3.0">
                             <rect  width="0.854" x="-22.382" y="-34.748" fill="#FFFFFF" gorn="0.2.5.0.0.0.0.0.0.0.0.0.0.0.0.0.0.3.0.0.0.0.0" height="0.961" id="_x30_.1.5.0.0.0.0.0.3.0.0"/>
                            </g>
                           </g>
                          </g>
                         </g>
                        </g>
                        <g transform="matrix(-2.54711e-06, -1, 1, -2.54711e-06, 11.8297, -56.7093)">
                         <g >
                          <g >
                           <g >
                            <g  gorn="0.2.5.0.0.0.0.0.0.0.0.0.0.0.0.0.0.3.1.0.0.0" id="_x30_.1.5.0.0.0.0.0.3.1">
                             <rect  width="0.854" x="-22.863" y="-34.29" fill="#B3B3B3" gorn="0.2.5.0.0.0.0.0.0.0.0.0.0.0.0.0.0.3.1.0.0.0.0" height="0.049" id="_x30_.1.5.0.0.0.0.0.3.1.0"/>
                            </g>
                           </g>
                          </g>
                         </g>
                        </g>
                       </g>
                       <g  gorn="0.2.5.0.0.0.0.0.0.0.0.0.0.0.0.0.0.4" id="_x30_.1.5.0.0.0.0.0.4">
                        <polygon  fill="#D1C690" points="-23.476,-32.549,-23.582,-31.585,-22.849,-31.585,-22.954,-32.549" gorn="0.2.5.0.0.0.0.0.0.0.0.0.0.0.0.0.0.4.0" id="_x30_.1.5.0.0.0.0.0.4.0"/>
                        <g  gorn="0.2.5.0.0.0.0.0.0.0.0.0.0.0.0.0.0.4.1" id="_x30_.1.5.0.0.0.0.0.4.1">
                         <path  fill="#D1C690" gorn="0.2.5.0.0.0.0.0.0.0.0.0.0.0.0.0.0.4.1.0" id="_x30_.1.5.0.0.0.0.0.4.1.0" d="M-23.279,-32.488c0,-0.002,0,-0.004,0,-0.008c0.035,-0.266,0.104,-0.447,0.162,-0.598c0.08,-0.209,0.782,-0.559,0.696,-0.828c-0.012,-0.027,0.011,-0.06,0.043,-0.066c0.035,-0.008,0.068,0.01,0.078,0.039c0.095,0.305,-0.617,0.674,-0.701,0.893c-0.06,0.148,-0.123,0.318,-0.155,0.572c-0.004,0.029,-0.033,0.055,-0.068,0.049C-23.254,-32.436,-23.279,-32.46,-23.279,-32.488z"/>
                        </g>
                        <polygon  fill="#D1C690" points="-20.59,-35.969,-20.487,-36.933,-21.217,-36.933,-21.114,-35.969" gorn="0.2.5.0.0.0.0.0.0.0.0.0.0.0.0.0.0.4.2" id="_x30_.1.5.0.0.0.0.0.4.2"/>
                        <g  gorn="0.2.5.0.0.0.0.0.0.0.0.0.0.0.0.0.0.4.3" id="_x30_.1.5.0.0.0.0.0.4.3">
                         <path  fill="#D1C690" gorn="0.2.5.0.0.0.0.0.0.0.0.0.0.0.0.0.0.4.3.0" id="_x30_.1.5.0.0.0.0.0.4.3.0" d="M-22.111,-34.316c0,-0.025,0.02,-0.049,0.047,-0.055c0.292,-0.063,1.152,-1.088,1.152,-1.885c0,-0.033,0.026,-0.057,0.063,-0.057c0.034,0.002,0.063,0.025,0.063,0.057l0,0.002c0,0.749,-0.77,1.891,-1.245,1.993c-0.035,0.008,-0.068,-0.012,-0.078,-0.041C-22.111,-34.304,-22.111,-34.309,-22.111,-34.316z"/>
                        </g>
                        <path  fill="#D1C690" gorn="0.2.5.0.0.0.0.0.0.0.0.0.0.0.0.0.0.4.4" id="_x30_.1.5.0.0.0.0.0.4.4" d="M-22.127,-33.845c0,0,0.002,-0.356,-0.311,-0.383c0,0.07,0,0.383,0,0.383L-22.127,-33.845z"/>
                        <path  fill="#D1C690" gorn="0.2.5.0.0.0.0.0.0.0.0.0.0.0.0.0.0.4.5" id="_x30_.1.5.0.0.0.0.0.4.5" d="M-21.806,-34.281c0,0,-0.306,0.158,-0.351,0.053c-0.048,-0.107,-0.052,-0.178,0.028,-0.24C-22.047,-34.529,-21.806,-34.281,-21.806,-34.281z"/>
                        <path  fill="#9D956C" gorn="0.2.5.0.0.0.0.0.0.0.0.0.0.0.0.0.0.4.6" id="_x30_.1.5.0.0.0.0.0.4.6" d="M-22.474,-33.922c0.084,0.27,-0.618,0.619,-0.698,0.828c-0.06,0.145,-0.127,0.33,-0.162,0.598l0.059,0c0.035,-0.266,0.104,-0.447,0.162,-0.598c0.08,-0.209,0.782,-0.559,0.696,-0.828L-22.474,-33.922z"/>
                        <polygon  fill="#9D956C" points="-21.169,-35.969,-21.272,-36.933,-21.217,-36.933,-21.114,-35.969" gorn="0.2.5.0.0.0.0.0.0.0.0.0.0.0.0.0.0.4.7" id="_x30_.1.5.0.0.0.0.0.4.7"/>
                        <path  fill="#9D956C" gorn="0.2.5.0.0.0.0.0.0.0.0.0.0.0.0.0.0.4.8" id="_x30_.1.5.0.0.0.0.0.4.8" d="M-22.119,-34.371c0.291,-0.062,1.212,-1.07,1.149,-1.885l0.06,0c0.06,0.877,-0.86,1.826,-1.152,1.887L-22.119,-34.371z"/>
                        <path  fill="#9D956C" gorn="0.2.5.0.0.0.0.0.0.0.0.0.0.0.0.0.0.4.9" id="_x30_.1.5.0.0.0.0.0.4.9" d="M-22.492,-34.227c0,0.07,0,0.381,0,0.381l0.057,0c0,0,0,-0.311,0,-0.381L-22.492,-34.227z"/>
                        <path  fill="#9D956C" gorn="0.2.5.0.0.0.0.0.0.0.0.0.0.0.0.0.0.4.10" id="_x30_.1.5.0.0.0.0.0.4.10" d="M-22.181,-34.469c-0.08,0.063,-0.076,0.131,-0.031,0.238l0.06,0.002c-0.049,-0.107,-0.052,-0.179,0.028,-0.24L-22.181,-34.469L-22.181,-34.469z"/>
                       </g>
                       <g transform="matrix(-2.54711e-06, -1, 1, -2.54711e-06, 14.1869, -54.3814)">
                        <g >
                         <g >
                          <g >
                           <g  gorn="0.2.5.0.0.0.0.0.0.0.0.0.0.0.0.0.0.5.0.0.0" id="_x30_.1.5.0.0.0.0.0.5">
                            <rect  width="4.223" x="-22.205" opacity="0.5" y="-34.308" fill="#FFFFFF" gorn="0.2.5.0.0.0.0.0.0.0.0.0.0.0.0.0.0.5.0.0.0.0" height="0.051" id="_x30_.1.5.0.0.0.0.0.5.0" enable-background="new    "/>
                           </g>
                          </g>
                         </g>
                        </g>
                       </g>
                       <path  opacity="0.5" fill="#F2F2F2" gorn="0.2.5.0.0.0.0.0.0.0.0.0.0.0.0.0.0.6" id="_x30_.1.5.0.0.0.0.0.6" enable-background="new    " d="M-20.069,-36.916L-23.9,-36.916l0,5.317l3.831,0.004L-20.069,-36.916z"/>
                       <path  opacity="0.55" fill="#FFFFFF" gorn="0.2.5.0.0.0.0.0.0.0.0.0.0.0.0.0.0.7" id="_x30_.1.5.0.0.0.0.0.7" enable-background="new    " d="M-20.719,-36.866l0.271,0c0.151,0.018,0.271,-0.012,0.271,0.098c0,0.611,0,4.703,0,4.854c0,0.168,-0.065,0.176,-0.065,-0.012c0,-0.131,0,-3.893,0,-4.346c0,-0.457,-0.105,-0.518,-0.197,-0.518l-0.272,0.002C-20.893,-36.788,-20.893,-36.866,-20.719,-36.866z"/>
                       <path  opacity="0.03" gorn="0.2.5.0.0.0.0.0.0.0.0.0.0.0.0.0.0.8" id="_x30_.1.5.0.0.0.0.0.8" enable-background="new    " d="M-23.678,-31.74c-0.068,0,-0.138,0.012,-0.138,-0.098c0,-0.611,0,-4.667,0,-4.817c0,-0.168,0.065,-0.176,0.065,0.008c0,0.135,0.002,3.138,0.002,3.589C-23.75,-32.463,-23.678,-31.74,-23.678,-31.74z"/>
                       <path  fill="#D1C690" gorn="0.2.5.0.0.0.0.0.0.0.0.0.0.0.0.0.0.9" id="_x30_.1.5.0.0.0.0.0.9" d="M-23.902,-37.874l0,0.771l0.521,0c0.125,0,0.213,0.08,0.268,0.188l3.047,0l0,-1.01l-3.784,0l-0.05,0"/>
                       <g transform="matrix(-2.54711e-06, -1, 1, -2.54711e-06, 17.3219, -57.5155)">
                        <g >
                         <g >
                          <g >
                           <g  gorn="0.2.5.0.0.0.0.0.0.0.0.0.0.0.0.0.0.10.0.0.0" id="_x30_.1.5.0.0.0.0.0.10">
                            <rect  width="1.006" x="-20.596" opacity="0.5" y="-37.443" fill="#FFFFFF" gorn="0.2.5.0.0.0.0.0.0.0.0.0.0.0.0.0.0.10.0.0.0.0" height="0.052" id="_x30_.1.5.0.0.0.0.0.10.0" enable-background="new    "/>
                           </g>
                          </g>
                         </g>
                        </g>
                       </g>
                       <path  fill="#D1C690" gorn="0.2.5.0.0.0.0.0.0.0.0.0.0.0.0.0.0.11" id="_x30_.1.5.0.0.0.0.0.11" d="M-23.902,-30.529l0.049,0l3.784,0L-20.069,-31.6l-3.464,0c-0.056,0.104,-0.146,0.191,-0.271,0.191l-0.1,0l0,0.829"/>
                       <g transform="matrix(-2.54711e-06, -1, 1, -2.54711e-06, 10.966, -51.159)">
                        <g >
                         <g >
                          <g >
                           <g  gorn="0.2.5.0.0.0.0.0.0.0.0.0.0.0.0.0.0.12.0.0.0" id="_x30_.1.5.0.0.0.0.0.12">
                            <rect  width="1.072" x="-20.628" opacity="0.5" y="-31.084" fill="#FFFFFF" gorn="0.2.5.0.0.0.0.0.0.0.0.0.0.0.0.0.0.12.0.0.0.0" height="0.052" id="_x30_.1.5.0.0.0.0.0.12.0" enable-background="new    "/>
                           </g>
                          </g>
                         </g>
                        </g>
                       </g>
                      </g>
                     </g>
                    </g>
                   </g>
                  </g>
                 </g>
                </g>
               </g>
              </g>
             </g>
            </g>
           </g>
          </g>
         </g>
        </g>
       </g>
      </g>
     </g>
     <g transform="matrix(1, 0, 0, 1, 186.214, 43.9355)">
      <g >
       <g >
        <g >
         <g  gorn="0.2.6.0.0.0" id="_x30_.1.6">
          <g  gorn="0.2.6.0.0.0.0" id="chip-led0805_1_">
           <g transform="matrix(0, -1, 1, 0, -1.77951, 5.62951)">
            <g >
             <g >
              <g >
               <g  gorn="0.2.6.0.0.0.0.0.0.0.0" id="_x30_.1.6.0.0">
                <g  gorn="0.2.6.0.0.0.0.0.0.0.0.0" id="_x30_.1.6.0.0.0">
                 <g transform="matrix(1, 0, 0, 1, 21.5539, 31.3385)">
                  <g >
                   <g >
                    <g >
                     <g  gorn="0.2.6.0.0.0.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.6.0.0.0.0">
                      <g  gorn="0.2.6.0.0.0.0.0.0.0.0.0.0.0.0.0.0" id="led-0603_2_">
                       <line  fill="none" gorn="0.2.6.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.6.0.0.0.0.0.0" y1="-33.306" x1="-21.535" y2="-26.07" x2="-21.535"/>
                       <g transform="matrix(-2.54711e-06, -1, 1, -2.54711e-06, 10.012, -49.2526)">
                        <g >
                         <g >
                          <g >
                           <g  gorn="0.2.6.0.0.0.0.0.0.0.0.0.0.0.0.0.0.1.0.0.0" id="_x30_.1.6.0.0.0.0.0.1">
                            <rect  width="7.349" x="-23.291" y="-31.546" fill="#F2F2F2" gorn="0.2.6.0.0.0.0.0.0.0.0.0.0.0.0.0.0.1.0.0.0.0" height="3.833" id="_x30_.1.6.0.0.0.0.0.1.0"/>
                           </g>
                          </g>
                         </g>
                        </g>
                       </g>
                       <path  fill="#22B573" gorn="0.2.6.0.0.0.0.0.0.0.0.0.0.0.0.0.0.2" fill-opacity="0.7" id="_x30_.1.6.0.0.0.0.0.2" d="M-21.533,-28.561c0,0,0.467,0.646,0.426,0.865c-0.041,0.219,0.148,0.541,0,0.678l-0.424,-0.021L-21.533,-28.561z"/>
                       <g  gorn="0.2.6.0.0.0.0.0.0.0.0.0.0.0.0.0.0.3" id="_x30_.1.6.0.0.0.0.0.3">
                        <g transform="matrix(-2.54711e-06, -1, 1, -2.54711e-06, 10.1107, -49.2956)">
                         <g >
                          <g >
                           <g >
                            <g  gorn="0.2.6.0.0.0.0.0.0.0.0.0.0.0.0.0.0.3.0.0.0.0" id="_x30_.1.6.0.0.0.0.0.3.0">
                             <rect  width="0.854" x="-20.017" y="-30.18" fill="#FFFFFF" gorn="0.2.6.0.0.0.0.0.0.0.0.0.0.0.0.0.0.3.0.0.0.0.0" height="0.961" id="_x30_.1.6.0.0.0.0.0.3.0.0"/>
                            </g>
                           </g>
                          </g>
                         </g>
                        </g>
                        <g transform="matrix(-2.54711e-06, -1, 1, -2.54711e-06, 9.6297, -49.7766)">
                         <g >
                          <g >
                           <g >
                            <g  gorn="0.2.6.0.0.0.0.0.0.0.0.0.0.0.0.0.0.3.1.0.0.0" id="_x30_.1.6.0.0.0.0.0.3.1">
                             <rect  width="0.854" x="-20.497" y="-29.724" fill="#B3B3B3" gorn="0.2.6.0.0.0.0.0.0.0.0.0.0.0.0.0.0.3.1.0.0.0.0" height="0.049" id="_x30_.1.6.0.0.0.0.0.3.1.0"/>
                            </g>
                           </g>
                          </g>
                         </g>
                        </g>
                       </g>
                       <g  gorn="0.2.6.0.0.0.0.0.0.0.0.0.0.0.0.0.0.4" id="_x30_.1.6.0.0.0.0.0.4">
                        <polygon  fill="#D1C690" points="-21.109,-27.981,-21.213,-27.018,-20.482,-27.018,-20.586,-27.981" gorn="0.2.6.0.0.0.0.0.0.0.0.0.0.0.0.0.0.4.0" id="_x30_.1.6.0.0.0.0.0.4.0"/>
                        <g  gorn="0.2.6.0.0.0.0.0.0.0.0.0.0.0.0.0.0.4.1" id="_x30_.1.6.0.0.0.0.0.4.1">
                         <path  fill="#D1C690" gorn="0.2.6.0.0.0.0.0.0.0.0.0.0.0.0.0.0.4.1.0" id="_x30_.1.6.0.0.0.0.0.4.1.0" d="M-20.91,-27.919c0,-0.002,0,-0.004,0,-0.008c0.035,-0.269,0.104,-0.447,0.162,-0.601c0.08,-0.209,0.782,-0.561,0.696,-0.826c-0.012,-0.026,0.011,-0.063,0.043,-0.065c0.035,-0.008,0.068,0.011,0.078,0.039c0.095,0.306,-0.617,0.674,-0.701,0.894c-0.06,0.147,-0.123,0.317,-0.155,0.571c-0.004,0.029,-0.033,0.056,-0.068,0.05C-20.885,-27.871,-20.91,-27.893,-20.91,-27.919z"/>
                        </g>
                        <polygon  fill="#D1C690" points="-18.221,-31.401,-18.118,-32.368,-18.848,-32.368,-18.745,-31.401" gorn="0.2.6.0.0.0.0.0.0.0.0.0.0.0.0.0.0.4.2" id="_x30_.1.6.0.0.0.0.0.4.2"/>
                        <g  gorn="0.2.6.0.0.0.0.0.0.0.0.0.0.0.0.0.0.4.3" id="_x30_.1.6.0.0.0.0.0.4.3">
                         <path  fill="#D1C690" gorn="0.2.6.0.0.0.0.0.0.0.0.0.0.0.0.0.0.4.3.0" id="_x30_.1.6.0.0.0.0.0.4.3.0" d="M-19.742,-29.749c0,-0.025,0.021,-0.049,0.047,-0.055c0.292,-0.063,1.152,-1.088,1.152,-1.885c0,-0.033,0.026,-0.062,0.063,-0.062c0.034,0.002,0.063,0.022,0.063,0.062l0,0.002c0,0.748,-0.77,1.891,-1.245,1.992c-0.035,0.008,-0.068,-0.016,-0.078,-0.041C-19.742,-29.739,-19.742,-29.743,-19.742,-29.749z"/>
                        </g>
                        <path  fill="#D1C690" gorn="0.2.6.0.0.0.0.0.0.0.0.0.0.0.0.0.0.4.4" id="_x30_.1.6.0.0.0.0.0.4.4" d="M-19.758,-29.278c0,0,0.002,-0.354,-0.311,-0.383c0,0.068,0,0.383,0,0.383L-19.758,-29.278z"/>
                        <path  fill="#D1C690" gorn="0.2.6.0.0.0.0.0.0.0.0.0.0.0.0.0.0.4.5" id="_x30_.1.6.0.0.0.0.0.4.5" d="M-19.439,-29.712c0,0,-0.306,0.157,-0.351,0.054c-0.048,-0.107,-0.052,-0.179,0.028,-0.24C-19.678,-29.96,-19.439,-29.712,-19.439,-29.712z"/>
                        <path  fill="#9D956C" gorn="0.2.6.0.0.0.0.0.0.0.0.0.0.0.0.0.0.4.6" id="_x30_.1.6.0.0.0.0.0.4.6" d="M-20.107,-29.354c0.084,0.271,-0.618,0.617,-0.698,0.826c-0.06,0.146,-0.127,0.33,-0.162,0.601l0.059,0c0.035,-0.269,0.104,-0.447,0.162,-0.601c0.08,-0.209,0.782,-0.561,0.696,-0.826L-20.107,-29.354z"/>
                        <polygon  fill="#9D956C" points="-18.8,-31.401,-18.903,-32.368,-18.848,-32.368,-18.745,-31.401" gorn="0.2.6.0.0.0.0.0.0.0.0.0.0.0.0.0.0.4.7" id="_x30_.1.6.0.0.0.0.0.4.7"/>
                        <path  fill="#9D956C" gorn="0.2.6.0.0.0.0.0.0.0.0.0.0.0.0.0.0.4.8" id="_x30_.1.6.0.0.0.0.0.4.8" d="M-19.752,-29.805c0.291,-0.063,1.212,-1.069,1.149,-1.885l0.06,0c0.06,0.877,-0.86,1.824,-1.152,1.888L-19.752,-29.805z"/>
                        <path  fill="#9D956C" gorn="0.2.6.0.0.0.0.0.0.0.0.0.0.0.0.0.0.4.9" id="_x30_.1.6.0.0.0.0.0.4.9" d="M-20.125,-29.661c0,0.068,0,0.381,0,0.381l0.057,0c0,0,0,-0.313,0,-0.381L-20.125,-29.661z"/>
                        <path  fill="#9D956C" gorn="0.2.6.0.0.0.0.0.0.0.0.0.0.0.0.0.0.4.10" id="_x30_.1.6.0.0.0.0.0.4.10" d="M-19.814,-29.901c-0.08,0.063,-0.076,0.131,-0.031,0.237l0.06,0.003c-0.049,-0.107,-0.052,-0.18,0.028,-0.24L-19.814,-29.901z"/>
                       </g>
                       <g transform="matrix(-2.54711e-06, -1, 1, -2.54711e-06, 11.9871, -47.4465)">
                        <g >
                         <g >
                          <g >
                           <g  gorn="0.2.6.0.0.0.0.0.0.0.0.0.0.0.0.0.0.5.0.0.0" id="_x30_.1.6.0.0.0.0.0.5">
                            <rect  width="4.225" x="-19.839" opacity="0.5" y="-29.738" fill="#FFFFFF" gorn="0.2.6.0.0.0.0.0.0.0.0.0.0.0.0.0.0.5.0.0.0.0" height="0.051" id="_x30_.1.6.0.0.0.0.0.5.0" enable-background="new    "/>
                           </g>
                          </g>
                         </g>
                        </g>
                       </g>
                       <path  opacity="0.5" fill="#F2F2F2" gorn="0.2.6.0.0.0.0.0.0.0.0.0.0.0.0.0.0.6" id="_x30_.1.6.0.0.0.0.0.6" enable-background="new    " d="M-17.701,-32.35l-3.831,0l0,5.316l3.831,0.004L-17.701,-32.35z"/>
                       <path  opacity="0.55" fill="#FFFFFF" gorn="0.2.6.0.0.0.0.0.0.0.0.0.0.0.0.0.0.7" id="_x30_.1.6.0.0.0.0.0.7" enable-background="new    " d="M-18.352,-32.298l0.271,0c0.151,0.019,0.271,-0.013,0.271,0.099c0,0.61,0,4.702,0,4.854c0,0.168,-0.065,0.176,-0.065,-0.014c0,-0.131,0,-3.895,0,-4.348c0,-0.457,-0.105,-0.52,-0.197,-0.52l-0.272,0.004C-18.526,-32.223,-18.526,-32.298,-18.352,-32.298z"/>
                       <path  opacity="0.03" gorn="0.2.6.0.0.0.0.0.0.0.0.0.0.0.0.0.0.8" id="_x30_.1.6.0.0.0.0.0.8" enable-background="new    " d="M-21.311,-27.171c-0.068,0,-0.138,0.013,-0.138,-0.099c0,-0.61,0,-4.668,0,-4.817c0,-0.168,0.065,-0.177,0.065,0.009c0,0.137,0.002,3.139,0.002,3.59C-21.381,-27.895,-21.311,-27.171,-21.311,-27.171z"/>
                       <path  fill="#D1C690" gorn="0.2.6.0.0.0.0.0.0.0.0.0.0.0.0.0.0.9" id="_x30_.1.6.0.0.0.0.0.9" d="M-21.533,-33.309l0,0.771l0.521,0c0.125,0,0.213,0.08,0.268,0.188l3.047,0l0,-1.01l-3.784,0l-0.05,0"/>
                       <g transform="matrix(-2.54711e-06, -1, 1, -2.54711e-06, 15.1234, -50.5798)">
                        <g >
                         <g >
                          <g >
                           <g  gorn="0.2.6.0.0.0.0.0.0.0.0.0.0.0.0.0.0.10.0.0.0" id="_x30_.1.6.0.0.0.0.0.10">
                            <rect  width="1.007" x="-18.229" opacity="0.5" y="-32.873" fill="#FFFFFF" gorn="0.2.6.0.0.0.0.0.0.0.0.0.0.0.0.0.0.10.0.0.0.0" height="0.052" id="_x30_.1.6.0.0.0.0.0.10.0" enable-background="new    "/>
                           </g>
                          </g>
                         </g>
                        </g>
                       </g>
                       <path  fill="#D1C690" gorn="0.2.6.0.0.0.0.0.0.0.0.0.0.0.0.0.0.11" id="_x30_.1.6.0.0.0.0.0.11" d="M-21.533,-25.96l0.049,0l3.784,0l0,-1.071l-3.464,0c-0.056,0.104,-0.146,0.19,-0.271,0.19l-0.1,0l0,0.83"/>
                       <g transform="matrix(-2.54711e-06, -1, 1, -2.54711e-06, 8.7664, -44.2238)">
                        <g >
                         <g >
                          <g >
                           <g  gorn="0.2.6.0.0.0.0.0.0.0.0.0.0.0.0.0.0.12.0.0.0" id="_x30_.1.6.0.0.0.0.0.12">
                            <rect  width="1.07" x="-18.26" opacity="0.5" y="-26.517" fill="#FFFFFF" gorn="0.2.6.0.0.0.0.0.0.0.0.0.0.0.0.0.0.12.0.0.0.0" height="0.052" id="_x30_.1.6.0.0.0.0.0.12.0" enable-background="new    "/>
                           </g>
                          </g>
                         </g>
                        </g>
                       </g>
                      </g>
                     </g>
                    </g>
                   </g>
                  </g>
                 </g>
                </g>
               </g>
              </g>
             </g>
            </g>
           </g>
          </g>
         </g>
        </g>
       </g>
      </g>
     </g>
     <g transform="matrix(1, 0, 0, 1, 80.1173, 116.104)">
      <g >
       <g >
        <g >
         <g  gorn="0.2.7.0.0.0" id="_x30_.1.7">
          <g  gorn="0.2.7.0.0.0.0" id="panasonic_d">
           <g transform="matrix(0, 1, -1, 0, 19.39, -1.039)">
            <g >
             <g >
              <g >
               <g  gorn="0.2.7.0.0.0.0.0.0.0.0" id="_x30_.1.7.0.0">
                <g  gorn="0.2.7.0.0.0.0.0.0.0.0.0" id="_x30_.1.7.0.0.0">
                 <g  gorn="0.2.7.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.7.0.0.0.0">
                  <g transform="matrix(2.57889e-06, 1, -1, 2.57889e-06, 9.7242, 8.6814)">
                   <g >
                    <g >
                     <g >
                      <g  gorn="0.2.7.0.0.0.0.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.7.0.0.0.0.0">
                       <rect  width="1.272" x="-0.167" y="-10.702" fill="#CCCCCC" gorn="0.2.7.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0" height="1.039" id="_x30_.1.7.0.0.0.0.0.0"/>
                      </g>
                     </g>
                    </g>
                   </g>
                  </g>
                  <g transform="matrix(2.57889e-06, 1, -1, 2.57889e-06, 29.1148, -10.7073)">
                   <g >
                    <g >
                     <g >
                      <g  gorn="0.2.7.0.0.0.0.0.0.0.0.0.0.1.0.0.0" id="_x30_.1.7.0.0.0.0.1">
                       <rect  width="1.272" x="19.221" y="28.079" fill="#CCCCCC" gorn="0.2.7.0.0.0.0.0.0.0.0.0.0.1.0.0.0.0" height="1.037" id="_x30_.1.7.0.0.0.0.1.0"/>
                      </g>
                     </g>
                    </g>
                   </g>
                  </g>
                  <g transform="matrix(2.57889e-06, 1, -1, 2.57889e-06, 10.2611, 9.2182)">
                   <g >
                    <g >
                     <g >
                      <g  gorn="0.2.7.0.0.0.0.0.0.0.0.0.0.2.0.0.0" id="_x30_.1.7.0.0.0.0.2">
                       <rect  width="0.203" x="-0.706" opacity="0.1" y="-10.165" gorn="0.2.7.0.0.0.0.0.0.0.0.0.0.2.0.0.0.0" height="1.039" id="_x30_.1.7.0.0.0.0.2.0" enable-background="new    "/>
                      </g>
                     </g>
                    </g>
                   </g>
                  </g>
                  <g transform="matrix(2.57889e-06, 1, -1, 2.57889e-06, 29.6512, -10.1709)">
                   <g >
                    <g >
                     <g >
                      <g  gorn="0.2.7.0.0.0.0.0.0.0.0.0.0.3.0.0.0" id="_x30_.1.7.0.0.0.0.3">
                       <rect  width="0.203" x="18.682" opacity="0.1" y="28.616" gorn="0.2.7.0.0.0.0.0.0.0.0.0.0.3.0.0.0.0" height="1.037" id="_x30_.1.7.0.0.0.0.3.0" enable-background="new    "/>
                      </g>
                     </g>
                    </g>
                   </g>
                  </g>
                  <g transform="matrix(2.57889e-06, 1, -1, 2.57889e-06, 9.1903, 8.1474)">
                   <g >
                    <g >
                     <g >
                      <g  gorn="0.2.7.0.0.0.0.0.0.0.0.0.0.4.0.0.0" id="_x30_.1.7.0.0.0.0.4">
                       <rect  width="0.204" x="1.435" opacity="0.2" y="-11.236" fill="#FFFFFF" gorn="0.2.7.0.0.0.0.0.0.0.0.0.0.4.0.0.0.0" height="1.039" id="_x30_.1.7.0.0.0.0.4.0" enable-background="new    "/>
                      </g>
                     </g>
                    </g>
                   </g>
                  </g>
                  <g transform="matrix(2.57889e-06, 1, -1, 2.57889e-06, 28.5809, -11.2412)">
                   <g >
                    <g >
                     <g >
                      <g  gorn="0.2.7.0.0.0.0.0.0.0.0.0.0.5.0.0.0" id="_x30_.1.7.0.0.0.0.5">
                       <rect  width="0.204" x="20.822" opacity="0.2" y="27.545" fill="#FFFFFF" gorn="0.2.7.0.0.0.0.0.0.0.0.0.0.5.0.0.0.0" height="1.037" id="_x30_.1.7.0.0.0.0.5.0" enable-background="new    "/>
                      </g>
                     </g>
                    </g>
                   </g>
                  </g>
                  <path  fill="#1A1A1A" gorn="0.2.7.0.0.0.0.0.0.0.0.0.0.6" id="_x30_.1.7.0.0.0.0.6" d="M4.845,18.353l13.157,0c0.76,0,1.385,-0.623,1.385,-1.383l0,-15.58c0,-0.764,-0.625,-1.387,-1.385,-1.387l-13.157,0l-3.81,3.811l0,3.633l0,3.635l0,3.463L4.845,18.353z"/>
                  <circle  fill="#E6E6E6" cx="10.211" gorn="0.2.7.0.0.0.0.0.0.0.0.0.0.7" cy="9.178" id="_x30_.1.7.0.0.0.0.7" r="8.703"/>
                  <path  fill="#333333" gorn="0.2.7.0.0.0.0.0.0.0.0.0.0.8" id="_x30_.1.7.0.0.0.0.8" d="M4.845,18.353l13.157,0c0.76,0,1.385,-0.623,1.385,-1.383l0,-15.58c0,-0.764,-0.625,-1.387,-1.385,-1.387L15.25,0.003l-10.405,0l-3.81,3.811l0,3.633l0,3.635l0,3.463L4.845,18.353z"/>
                  <path  gorn="0.2.7.0.0.0.0.0.0.0.0.0.0.9" id="_x30_.1.7.0.0.0.0.9" d="M1.036,3.997l3.811,-3.811l10.404,0l2.752,0c0.76,0,1.385,0.623,1.385,1.387L19.388,1.389c0,-0.764,-0.625,-1.387,-1.385,-1.387L15.25,0.002l-10.405,0l-3.81,3.811L1.035,3.997L1.036,3.997z"/>
                  <path  opacity="0.1" fill="#FFFFFF" gorn="0.2.7.0.0.0.0.0.0.0.0.0.0.10" id="_x30_.1.7.0.0.0.0.10" enable-background="new    " d="M19.386,16.785c0,0.761,-0.625,1.384,-1.385,1.384l-13.157,0l-3.811,-3.807l0,0.183l3.811,3.808l13.157,0c0.76,0,1.385,-0.623,1.385,-1.383L19.386,16.785z"/>
                  <path  fill="#E6E6E6" gorn="0.2.7.0.0.0.0.0.0.0.0.0.0.11" id="_x30_.1.7.0.0.0.0.11" d="M10.211,0.354c1.881,0,3.615,0.604,5.039,1.614c2.215,1.579,3.664,4.163,3.664,7.088c0,2.927,-1.449,5.509,-3.664,7.087c-1.424,1.013,-3.158,1.615,-5.039,1.615c-4.805,0,-8.702,-3.896,-8.702,-8.703C1.509,4.251,5.407,0.354,10.211,0.354z"/>
                  <path  gorn="0.2.7.0.0.0.0.0.0.0.0.0.0.12" id="_x30_.1.7.0.0.0.0.12" d="M18.915,9.178c0,-2.926,-1.449,-5.509,-3.664,-7.088l0,14.175C17.465,14.688,18.915,12.105,18.915,9.178z"/>
                  <path  opacity="0.3" fill="#FFFFFF" gorn="0.2.7.0.0.0.0.0.0.0.0.0.0.13" id="_x30_.1.7.0.0.0.0.13" enable-background="new    " d="M1.509,8.934c0,4.807,3.897,8.703,8.702,8.703c1.881,0,3.615,-0.604,5.039,-1.616c2.215,-1.578,3.664,-4.161,3.664,-7.087l0,0.244c0,2.927,-1.449,5.51,-3.664,7.087c-1.424,1.014,-3.158,1.615,-5.039,1.615c-4.805,0,-8.702,-3.896,-8.702,-8.702L1.509,8.934z"/>
                  <path  opacity="0.5" fill="#FFFFFF" gorn="0.2.7.0.0.0.0.0.0.0.0.0.0.14" id="_x30_.1.7.0.0.0.0.14" enable-background="new    " d="M18.915,9.407c0,-2.925,-1.449,-5.508,-3.664,-7.088L15.251,2.09c2.215,1.579,3.664,4.162,3.664,7.088L18.915,9.407z"/>
                  <path  opacity="0.2" gorn="0.2.7.0.0.0.0.0.0.0.0.0.0.15" id="_x30_.1.7.0.0.0.0.15" enable-background="new    " d="M15.25,2.319c-1.424,-1.012,-3.158,-1.615,-5.039,-1.615c-4.805,0,-8.702,3.898,-8.702,8.703L1.509,9.178c0,-4.805,3.897,-8.703,8.702,-8.703c1.881,0,3.615,0.604,5.039,1.615L15.25,2.319z"/>
                 </g>
                </g>
               </g>
              </g>
             </g>
            </g>
           </g>
          </g>
         </g>
        </g>
       </g>
      </g>
     </g>
     <g transform="matrix(1, 0, 0, 1, 59.9571, 116.104)">
      <g >
       <g >
        <g >
         <g  gorn="0.2.8.0.0.0" id="_x30_.1.8">
          <g  gorn="0.2.8.0.0.0.0" id="panasonic_d_1_">
           <g transform="matrix(0, 1, -1, 0, 19.39, -1.039)">
            <g >
             <g >
              <g >
               <g  gorn="0.2.8.0.0.0.0.0.0.0.0" id="_x30_.1.8.0.0">
                <g  gorn="0.2.8.0.0.0.0.0.0.0.0.0" id="_x30_.1.8.0.0.0">
                 <g  gorn="0.2.8.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.8.0.0.0.0">
                  <g transform="matrix(2.57889e-06, 1, -1, 2.57889e-06, 9.7247, 8.6818)">
                   <g >
                    <g >
                     <g >
                      <g  gorn="0.2.8.0.0.0.0.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.8.0.0.0.0.0">
                       <rect  width="1.272" x="-0.168" y="-10.702" fill="#CCCCCC" gorn="0.2.8.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0" height="1.038" id="_x30_.1.8.0.0.0.0.0.0"/>
                      </g>
                     </g>
                    </g>
                   </g>
                  </g>
                  <g transform="matrix(2.57889e-06, 1, -1, 2.57889e-06, 29.1148, -10.7074)">
                   <g >
                    <g >
                     <g >
                      <g  gorn="0.2.8.0.0.0.0.0.0.0.0.0.0.1.0.0.0" id="_x30_.1.8.0.0.0.0.1">
                       <rect  width="1.272" x="19.22" y="28.078" fill="#CCCCCC" gorn="0.2.8.0.0.0.0.0.0.0.0.0.0.1.0.0.0.0" height="1.037" id="_x30_.1.8.0.0.0.0.1.0"/>
                      </g>
                     </g>
                    </g>
                   </g>
                  </g>
                  <g transform="matrix(2.57889e-06, 1, -1, 2.57889e-06, 10.261, 9.2182)">
                   <g >
                    <g >
                     <g >
                      <g  gorn="0.2.8.0.0.0.0.0.0.0.0.0.0.2.0.0.0" id="_x30_.1.8.0.0.0.0.2">
                       <rect  width="0.203" x="-0.707" opacity="0.1" y="-10.165" gorn="0.2.8.0.0.0.0.0.0.0.0.0.0.2.0.0.0.0" height="1.039" id="_x30_.1.8.0.0.0.0.2.0" enable-background="new    "/>
                      </g>
                     </g>
                    </g>
                   </g>
                  </g>
                  <g transform="matrix(2.57889e-06, 1, -1, 2.57889e-06, 29.6506, -10.1715)">
                   <g >
                    <g >
                     <g >
                      <g  gorn="0.2.8.0.0.0.0.0.0.0.0.0.0.3.0.0.0" id="_x30_.1.8.0.0.0.0.3">
                       <rect  width="0.203" x="18.683" opacity="0.1" y="28.615" gorn="0.2.8.0.0.0.0.0.0.0.0.0.0.3.0.0.0.0" height="1.037" id="_x30_.1.8.0.0.0.0.3.0" enable-background="new    "/>
                      </g>
                     </g>
                    </g>
                   </g>
                  </g>
                  <g transform="matrix(2.57889e-06, 1, -1, 2.57889e-06, 9.1902, 8.1474)">
                   <g >
                    <g >
                     <g >
                      <g  gorn="0.2.8.0.0.0.0.0.0.0.0.0.0.4.0.0.0" id="_x30_.1.8.0.0.0.0.4">
                       <rect  width="0.204" x="1.435" opacity="0.2" y="-11.237" fill="#FFFFFF" gorn="0.2.8.0.0.0.0.0.0.0.0.0.0.4.0.0.0.0" height="1.039" id="_x30_.1.8.0.0.0.0.4.0" enable-background="new    "/>
                      </g>
                     </g>
                    </g>
                   </g>
                  </g>
                  <g transform="matrix(2.57889e-06, 1, -1, 2.57889e-06, 28.5808, -11.2413)">
                   <g >
                    <g >
                     <g >
                      <g  gorn="0.2.8.0.0.0.0.0.0.0.0.0.0.5.0.0.0" id="_x30_.1.8.0.0.0.0.5">
                       <rect  width="0.204" x="20.822" opacity="0.2" y="27.544" fill="#FFFFFF" gorn="0.2.8.0.0.0.0.0.0.0.0.0.0.5.0.0.0.0" height="1.037" id="_x30_.1.8.0.0.0.0.5.0" enable-background="new    "/>
                      </g>
                     </g>
                    </g>
                   </g>
                  </g>
                  <path  fill="#1A1A1A" gorn="0.2.8.0.0.0.0.0.0.0.0.0.0.6" id="_x30_.1.8.0.0.0.0.6" d="M4.846,18.353l13.157,0c0.76,0,1.385,-0.623,1.385,-1.383l0,-15.58c0,-0.764,-0.625,-1.387,-1.385,-1.387l-13.157,0l-3.81,3.811l0,3.633l0,3.635l0,3.463L4.846,18.353z"/>
                  <circle  fill="#E6E6E6" cx="10.212" gorn="0.2.8.0.0.0.0.0.0.0.0.0.0.7" cy="9.178" id="_x30_.1.8.0.0.0.0.7" r="8.703"/>
                  <path  fill="#333333" gorn="0.2.8.0.0.0.0.0.0.0.0.0.0.8" id="_x30_.1.8.0.0.0.0.8" d="M4.846,18.353l13.157,0c0.76,0,1.385,-0.623,1.385,-1.383l0,-15.58c0,-0.764,-0.625,-1.387,-1.385,-1.387l-2.752,0l-10.405,0l-3.81,3.811l0,3.633l0,3.635l0,3.463L4.846,18.353z"/>
                  <path  gorn="0.2.8.0.0.0.0.0.0.0.0.0.0.9" id="_x30_.1.8.0.0.0.0.9" d="M1.037,3.997l3.811,-3.811l10.404,0l2.752,0c0.76,0,1.385,0.623,1.385,1.387l0,-0.184c0,-0.764,-0.625,-1.387,-1.385,-1.387l-2.752,0l-10.405,0l-3.81,3.811L1.037,3.997L1.037,3.997z"/>
                  <path  opacity="0.1" fill="#FFFFFF" gorn="0.2.8.0.0.0.0.0.0.0.0.0.0.10" id="_x30_.1.8.0.0.0.0.10" enable-background="new    " d="M19.387,16.785c0,0.761,-0.625,1.384,-1.385,1.384l-13.157,0l-3.811,-3.807l0,0.183l3.811,3.808l13.157,0c0.76,0,1.385,-0.623,1.385,-1.383L19.387,16.785z"/>
                  <path  fill="#E6E6E6" gorn="0.2.8.0.0.0.0.0.0.0.0.0.0.11" id="_x30_.1.8.0.0.0.0.11" d="M10.212,0.354c1.881,0,3.615,0.604,5.039,1.614c2.215,1.579,3.664,4.163,3.664,7.088c0,2.927,-1.449,5.509,-3.664,7.087c-1.424,1.013,-3.158,1.615,-5.039,1.615c-4.805,0,-8.702,-3.896,-8.702,-8.703C1.51,4.251,5.408,0.354,10.212,0.354z"/>
                  <path  gorn="0.2.8.0.0.0.0.0.0.0.0.0.0.12" id="_x30_.1.8.0.0.0.0.12" d="M18.915,9.178c0,-2.926,-1.449,-5.509,-3.664,-7.088l0,14.175C17.466,14.688,18.916,12.105,18.915,9.178z"/>
                  <path  opacity="0.3" fill="#FFFFFF" gorn="0.2.8.0.0.0.0.0.0.0.0.0.0.13" id="_x30_.1.8.0.0.0.0.13" enable-background="new    " d="M1.51,8.934c0,4.807,3.897,8.703,8.702,8.703c1.881,0,3.615,-0.604,5.039,-1.616c2.215,-1.578,3.664,-4.161,3.664,-7.087l0,0.244c0,2.927,-1.449,5.51,-3.664,7.087c-1.424,1.014,-3.158,1.615,-5.039,1.615c-4.805,0,-8.702,-3.896,-8.702,-8.702L1.51,8.934z"/>
                  <path  opacity="0.5" fill="#FFFFFF" gorn="0.2.8.0.0.0.0.0.0.0.0.0.0.14" id="_x30_.1.8.0.0.0.0.14" enable-background="new    " d="M18.915,9.407c0,-2.925,-1.449,-5.508,-3.664,-7.088L15.251,2.09c2.215,1.579,3.664,4.162,3.664,7.088L18.915,9.407z"/>
                  <path  opacity="0.2" gorn="0.2.8.0.0.0.0.0.0.0.0.0.0.15" id="_x30_.1.8.0.0.0.0.15" enable-background="new    " d="M15.251,2.319c-1.424,-1.012,-3.158,-1.615,-5.039,-1.615c-4.805,0,-8.702,3.898,-8.702,8.703L1.51,9.178c0,-4.805,3.897,-8.703,8.702,-8.703c1.881,0,3.615,0.604,5.039,1.615L15.251,2.319z"/>
                 </g>
                </g>
               </g>
              </g>
             </g>
            </g>
           </g>
          </g>
         </g>
        </g>
       </g>
      </g>
     </g>
     <g transform="matrix(1, 0, 0, 1, 92.8519, 140.628)">
      <g >
       <g >
        <g >
         <g  gorn="0.2.9.0.0.0" id="_x30_.1.9">
          <g  gorn="0.2.9.0.0.0.0" id="_x31_x08_1_">
           <rect  width="57.601" x="0.72" y="-0.228" fill="#404040" gorn="0.2.9.0.0.0.0.0" height="7.199" id="_x30_.1.9.0.0"/>
           <rect  width="2.781" x="2.93" y="1.981" gorn="0.2.9.0.0.0.0.1" height="2.783" id="_x30_.1.9.0.1"/>
           <polygon  fill="#2A2A29" points="1.905,0.956,2.928,1.981,5.711,1.981,6.737,0.956" gorn="0.2.9.0.0.0.0.2" id="_x30_.1.9.0.2"/>
           <polygon  fill="#474747" points="6.737,0.956,5.711,1.985,5.711,4.766,6.737,5.789" gorn="0.2.9.0.0.0.0.3" id="_x30_.1.9.0.3"/>
           <polygon  fill="#595959" points="6.736,5.789,5.71,4.766,2.928,4.766,1.905,5.789" gorn="0.2.9.0.0.0.0.4" id="_x30_.1.9.0.4"/>
           <polygon  fill="#373737" points="1.903,5.789,2.928,4.764,2.928,1.981,1.903,0.956" gorn="0.2.9.0.0.0.0.5" id="_x30_.1.9.0.5"/>
           <rect  width="2.781" x="10.13" y="1.981" gorn="0.2.9.0.0.0.0.6" height="2.783" id="_x30_.1.9.0.6"/>
           <polygon  fill="#2A2A29" points="9.104,0.956,10.128,1.981,12.912,1.981,13.938,0.956" gorn="0.2.9.0.0.0.0.7" id="_x30_.1.9.0.7"/>
           <polygon  fill="#474747" points="13.938,0.956,12.912,1.985,12.912,4.766,13.938,5.789" gorn="0.2.9.0.0.0.0.8" id="_x30_.1.9.0.8"/>
           <polygon  fill="#595959" points="13.936,5.789,12.911,4.766,10.128,4.766,9.104,5.789" gorn="0.2.9.0.0.0.0.9" id="_x30_.1.9.0.9"/>
           <polygon  fill="#373737" points="9.102,5.789,10.128,4.764,10.128,1.981,9.102,0.956" gorn="0.2.9.0.0.0.0.10" id="_x30_.1.9.0.10"/>
           <rect  width="2.78" x="17.331" y="1.981" gorn="0.2.9.0.0.0.0.11" height="2.783" id="_x30_.1.9.0.11"/>
           <polygon  fill="#2A2A29" points="16.304,0.956,17.328,1.981,20.112,1.981,21.136,0.956" gorn="0.2.9.0.0.0.0.12" id="_x30_.1.9.0.12"/>
           <polygon  fill="#474747" points="21.136,0.956,20.112,1.985,20.112,4.766,21.136,5.789" gorn="0.2.9.0.0.0.0.13" id="_x30_.1.9.0.13"/>
           <polygon  fill="#595959" points="21.135,5.789,20.11,4.766,17.328,4.766,16.304,5.789" gorn="0.2.9.0.0.0.0.14" id="_x30_.1.9.0.14"/>
           <polygon  fill="#373737" points="16.302,5.789,17.328,4.764,17.328,1.981,16.302,0.956" gorn="0.2.9.0.0.0.0.15" id="_x30_.1.9.0.15"/>
           <rect  width="2.781" x="24.53" y="1.981" gorn="0.2.9.0.0.0.0.16" height="2.783" id="_x30_.1.9.0.16"/>
           <polygon  fill="#2A2A29" points="23.503,0.956,24.528,1.981,27.313,1.981,28.335,0.956" gorn="0.2.9.0.0.0.0.17" id="_x30_.1.9.0.17"/>
           <polygon  fill="#474747" points="28.335,0.956,27.313,1.985,27.313,4.766,28.335,5.789" gorn="0.2.9.0.0.0.0.18" id="_x30_.1.9.0.18"/>
           <polygon  fill="#595959" points="28.335,5.789,27.311,4.766,24.528,4.766,23.503,5.789" gorn="0.2.9.0.0.0.0.19" id="_x30_.1.9.0.19"/>
           <polygon  fill="#373737" points="23.501,5.789,24.528,4.764,24.528,1.981,23.501,0.956" gorn="0.2.9.0.0.0.0.20" id="_x30_.1.9.0.20"/>
           <rect  width="2.78" x="31.731" y="1.981" gorn="0.2.9.0.0.0.0.21" height="2.783" id="_x30_.1.9.0.21"/>
           <polygon  fill="#2A2A29" points="30.703,0.956,31.729,1.981,34.511,1.981,35.535,0.956" gorn="0.2.9.0.0.0.0.22" id="_x30_.1.9.0.22"/>
           <polygon  fill="#474747" points="35.535,0.956,34.511,1.985,34.511,4.766,35.535,5.789" gorn="0.2.9.0.0.0.0.23" id="_x30_.1.9.0.23"/>
           <polygon  fill="#595959" points="35.535,5.789,34.51,4.766,31.729,4.766,30.703,5.789" gorn="0.2.9.0.0.0.0.24" id="_x30_.1.9.0.24"/>
           <polygon  fill="#373737" points="30.701,5.789,31.729,4.764,31.729,1.981,30.701,0.956" gorn="0.2.9.0.0.0.0.25" id="_x30_.1.9.0.25"/>
           <rect  width="2.78" x="38.93" y="1.981" gorn="0.2.9.0.0.0.0.26" height="2.783" id="_x30_.1.9.0.26"/>
           <polygon  fill="#2A2A29" points="37.905,0.956,38.928,1.981,41.71,1.981,42.737,0.956" gorn="0.2.9.0.0.0.0.27" id="_x30_.1.9.0.27"/>
           <polygon  fill="#474747" points="42.737,0.956,41.71,1.985,41.71,4.766,42.737,5.789" gorn="0.2.9.0.0.0.0.28" id="_x30_.1.9.0.28"/>
           <polygon  fill="#595959" points="42.735,5.789,41.71,4.766,38.928,4.766,37.905,5.789" gorn="0.2.9.0.0.0.0.29" id="_x30_.1.9.0.29"/>
           <polygon  fill="#373737" points="37.903,5.789,38.928,4.764,38.928,1.981,37.903,0.956" gorn="0.2.9.0.0.0.0.30" id="_x30_.1.9.0.30"/>
           <rect  width="2.78" x="46.13" y="1.981" gorn="0.2.9.0.0.0.0.31" height="2.783" id="_x30_.1.9.0.31"/>
           <polygon  fill="#2A2A29" points="45.104,0.956,46.128,1.981,48.91,1.981,49.938,0.956" gorn="0.2.9.0.0.0.0.32" id="_x30_.1.9.0.32"/>
           <polygon  fill="#474747" points="49.938,0.956,48.91,1.985,48.91,4.766,49.938,5.789" gorn="0.2.9.0.0.0.0.33" id="_x30_.1.9.0.33"/>
           <polygon  fill="#595959" points="49.936,5.789,48.91,4.766,46.128,4.766,45.104,5.789" gorn="0.2.9.0.0.0.0.34" id="_x30_.1.9.0.34"/>
           <polygon  fill="#373737" points="45.102,5.789,46.128,4.764,46.128,1.981,45.102,0.956" gorn="0.2.9.0.0.0.0.35" id="_x30_.1.9.0.35"/>
           <rect  width="2.78" x="53.331" y="1.981" gorn="0.2.9.0.0.0.0.36" height="2.783" id="_x30_.1.9.0.36"/>
           <polygon  fill="#2A2A29" points="52.304,0.956,53.328,1.981,56.112,1.981,57.136,0.956" gorn="0.2.9.0.0.0.0.37" id="_x30_.1.9.0.37"/>
           <polygon  fill="#474747" points="57.136,0.956,56.112,1.985,56.112,4.766,57.136,5.789" gorn="0.2.9.0.0.0.0.38" id="_x30_.1.9.0.38"/>
           <polygon  fill="#595959" points="57.135,5.789,56.11,4.766,53.328,4.766,52.304,5.789" gorn="0.2.9.0.0.0.0.39" id="_x30_.1.9.0.39"/>
           <polygon  fill="#373737" points="52.302,5.789,53.328,4.764,53.328,1.981,52.302,0.956" gorn="0.2.9.0.0.0.0.40" id="_x30_.1.9.0.40"/>
          </g>
         </g>
        </g>
       </g>
      </g>
     </g>
     <g transform="matrix(1, 0, 0, 1, 89.0222, 50.1755)">
      <g >
       <g >
        <g >
         <g  gorn="0.2.10.0.0.0" id="_x30_.1.10">
          <g  gorn="0.2.10.0.0.0.0" id="chip-led0805_2_">
           <g transform="matrix(0, 1, -1, 0, 5.62951, 1.77951)">
            <g >
             <g >
              <g >
               <g  gorn="0.2.10.0.0.0.0.0.0.0.0" id="_x30_.1.10.0.0">
                <g  gorn="0.2.10.0.0.0.0.0.0.0.0.0" id="_x30_.1.10.0.0.0">
                 <g transform="matrix(1, 0, 0, 1, 21.5539, 31.3385)">
                  <g >
                   <g >
                    <g >
                     <g  gorn="0.2.10.0.0.0.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.10.0.0.0.0">
                      <g  gorn="0.2.10.0.0.0.0.0.0.0.0.0.0.0.0.0.0" id="led-0603_3_">
                       <line  fill="none" gorn="0.2.10.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.10.0.0.0.0.0.0" y1="-37.083" x1="-21.535" y2="-29.847" x2="-21.535"/>
                       <g transform="matrix(2.57889e-06, 1, -1, 2.57889e-06, -53.0294, -13.7889)">
                        <g >
                         <g >
                          <g >
                           <g  gorn="0.2.10.0.0.0.0.0.0.0.0.0.0.0.0.0.0.1.0.0.0" id="_x30_.1.10.0.0.0.0.0.1">
                            <rect  width="7.348" x="-23.292" y="-35.322" fill="#F2F2F2" gorn="0.2.10.0.0.0.0.0.0.0.0.0.0.0.0.0.0.1.0.0.0.0" height="3.833" id="_x30_.1.10.0.0.0.0.0.1.0"/>
                           </g>
                          </g>
                         </g>
                        </g>
                       </g>
                       <path  fill="#22B573" gorn="0.2.10.0.0.0.0.0.0.0.0.0.0.0.0.0.0.2" fill-opacity="0.7" id="_x30_.1.10.0.0.0.0.0.2" d="M-21.541,-32.333c0,0,0.467,0.645,0.426,0.867c-0.041,0.219,0.148,0.541,0,0.676l-0.424,-0.018L-21.541,-32.333z"/>
                       <g  gorn="0.2.10.0.0.0.0.0.0.0.0.0.0.0.0.0.0.3" id="_x30_.1.10.0.0.0.0.0.3">
                        <g transform="matrix(2.57889e-06, 1, -1, 2.57889e-06, -53.0695, -13.8875)">
                         <g >
                          <g >
                           <g >
                            <g  gorn="0.2.10.0.0.0.0.0.0.0.0.0.0.0.0.0.0.3.0.0.0.0" id="_x30_.1.10.0.0.0.0.0.3.0">
                             <rect  width="0.854" x="-20.016" y="-33.957" fill="#FFFFFF" gorn="0.2.10.0.0.0.0.0.0.0.0.0.0.0.0.0.0.3.0.0.0.0.0" height="0.961" id="_x30_.1.10.0.0.0.0.0.3.0.0"/>
                            </g>
                           </g>
                          </g>
                         </g>
                        </g>
                        <g transform="matrix(2.57889e-06, 1, -1, 2.57889e-06, -53.5526, -13.4083)">
                         <g >
                          <g >
                           <g >
                            <g  gorn="0.2.10.0.0.0.0.0.0.0.0.0.0.0.0.0.0.3.1.0.0.0" id="_x30_.1.10.0.0.0.0.0.3.1">
                             <rect  width="0.854" x="-20.497" y="-33.503" fill="#B3B3B3" gorn="0.2.10.0.0.0.0.0.0.0.0.0.0.0.0.0.0.3.1.0.0.0.0" height="0.049" id="_x30_.1.10.0.0.0.0.0.3.1.0"/>
                            </g>
                           </g>
                          </g>
                         </g>
                        </g>
                       </g>
                       <g  gorn="0.2.10.0.0.0.0.0.0.0.0.0.0.0.0.0.0.4" id="_x30_.1.10.0.0.0.0.0.4">
                        <polygon  fill="#D1C690" points="-21.115,-31.753,-21.219,-30.79,-20.488,-30.79,-20.592,-31.753" gorn="0.2.10.0.0.0.0.0.0.0.0.0.0.0.0.0.0.4.0" id="_x30_.1.10.0.0.0.0.0.4.0"/>
                        <g  gorn="0.2.10.0.0.0.0.0.0.0.0.0.0.0.0.0.0.4.1" id="_x30_.1.10.0.0.0.0.0.4.1">
                         <path  fill="#D1C690" gorn="0.2.10.0.0.0.0.0.0.0.0.0.0.0.0.0.0.4.1.0" id="_x30_.1.10.0.0.0.0.0.4.1.0" d="M-20.918,-31.692c0,-0.002,0,-0.004,0,-0.008c0.035,-0.266,0.104,-0.447,0.162,-0.598c0.08,-0.209,0.782,-0.559,0.696,-0.828c-0.012,-0.027,0.011,-0.06,0.043,-0.066c0.035,-0.008,0.068,0.01,0.078,0.039c0.095,0.305,-0.617,0.674,-0.701,0.893c-0.06,0.148,-0.123,0.318,-0.155,0.572c-0.004,0.029,-0.033,0.055,-0.068,0.049C-20.893,-31.642,-20.918,-31.665,-20.918,-31.692z"/>
                        </g>
                        <polygon  fill="#D1C690" points="-18.229,-35.173,-18.126,-36.139,-18.856,-36.139,-18.753,-35.173" gorn="0.2.10.0.0.0.0.0.0.0.0.0.0.0.0.0.0.4.2" id="_x30_.1.10.0.0.0.0.0.4.2"/>
                        <g  gorn="0.2.10.0.0.0.0.0.0.0.0.0.0.0.0.0.0.4.3" id="_x30_.1.10.0.0.0.0.0.4.3">
                         <path  fill="#D1C690" gorn="0.2.10.0.0.0.0.0.0.0.0.0.0.0.0.0.0.4.3.0" id="_x30_.1.10.0.0.0.0.0.4.3.0" d="M-19.75,-33.52c0,-0.025,0.02,-0.049,0.047,-0.055c0.292,-0.063,1.152,-1.088,1.152,-1.885c0,-0.033,0.026,-0.057,0.063,-0.057c0.034,0.002,0.063,0.025,0.063,0.057l0,0.002c0,0.749,-0.77,1.891,-1.245,1.993c-0.035,0.008,-0.068,-0.012,-0.078,-0.041C-19.75,-33.511,-19.75,-33.515,-19.75,-33.52z"/>
                        </g>
                        <path  fill="#D1C690" gorn="0.2.10.0.0.0.0.0.0.0.0.0.0.0.0.0.0.4.4" id="_x30_.1.10.0.0.0.0.0.4.4" d="M-19.766,-33.05c0,0,0.002,-0.356,-0.311,-0.383c0,0.07,0,0.383,0,0.383L-19.766,-33.05z"/>
                        <path  fill="#D1C690" gorn="0.2.10.0.0.0.0.0.0.0.0.0.0.0.0.0.0.4.5" id="_x30_.1.10.0.0.0.0.0.4.5" d="M-19.446,-33.485c0,0,-0.306,0.158,-0.351,0.053c-0.048,-0.107,-0.052,-0.178,0.028,-0.24C-19.686,-33.733,-19.446,-33.485,-19.446,-33.485z"/>
                        <path  fill="#9D956C" gorn="0.2.10.0.0.0.0.0.0.0.0.0.0.0.0.0.0.4.6" id="_x30_.1.10.0.0.0.0.0.4.6" d="M-20.113,-33.126c0.084,0.27,-0.618,0.619,-0.698,0.828c-0.06,0.145,-0.127,0.33,-0.162,0.598l0.059,0c0.035,-0.266,0.104,-0.447,0.162,-0.598c0.08,-0.209,0.782,-0.559,0.696,-0.828L-20.113,-33.126z"/>
                        <polygon  fill="#9D956C" points="-18.808,-35.173,-18.909,-36.139,-18.856,-36.139,-18.753,-35.173" gorn="0.2.10.0.0.0.0.0.0.0.0.0.0.0.0.0.0.4.7" id="_x30_.1.10.0.0.0.0.0.4.7"/>
                        <path  fill="#9D956C" gorn="0.2.10.0.0.0.0.0.0.0.0.0.0.0.0.0.0.4.8" id="_x30_.1.10.0.0.0.0.0.4.8" d="M-19.759,-33.577c0.291,-0.062,1.212,-1.07,1.149,-1.885l0.06,0c0.06,0.877,-0.86,1.826,-1.152,1.887L-19.759,-33.577z"/>
                        <path  fill="#9D956C" gorn="0.2.10.0.0.0.0.0.0.0.0.0.0.0.0.0.0.4.9" id="_x30_.1.10.0.0.0.0.0.4.9" d="M-20.133,-33.433c0,0.07,0,0.381,0,0.381l0.057,0c0,0,0,-0.311,0,-0.381L-20.133,-33.433z"/>
                        <path  fill="#9D956C" gorn="0.2.10.0.0.0.0.0.0.0.0.0.0.0.0.0.0.4.10" id="_x30_.1.10.0.0.0.0.0.4.10" d="M-19.821,-33.673c-0.08,0.063,-0.076,0.131,-0.031,0.238l0.06,0.002c-0.049,-0.107,-0.052,-0.179,0.028,-0.24L-19.821,-33.673z"/>
                       </g>
                       <g transform="matrix(2.57889e-06, 1, -1, 2.57889e-06, -51.2218, -15.764)">
                        <g >
                         <g >
                          <g >
                           <g  gorn="0.2.10.0.0.0.0.0.0.0.0.0.0.0.0.0.0.5.0.0.0" id="_x30_.1.10.0.0.0.0.0.5">
                            <rect  width="4.223" x="-19.838" opacity="0.5" y="-33.517" fill="#FFFFFF" gorn="0.2.10.0.0.0.0.0.0.0.0.0.0.0.0.0.0.5.0.0.0.0" height="0.051" id="_x30_.1.10.0.0.0.0.0.5.0" enable-background="new    "/>
                           </g>
                          </g>
                         </g>
                        </g>
                       </g>
                       <path  opacity="0.5" fill="#F2F2F2" gorn="0.2.10.0.0.0.0.0.0.0.0.0.0.0.0.0.0.6" id="_x30_.1.10.0.0.0.0.0.6" enable-background="new    " d="M-17.708,-36.122l-3.831,0l0,5.317l3.831,0.004L-17.708,-36.122z"/>
                       <path  opacity="0.55" fill="#FFFFFF" gorn="0.2.10.0.0.0.0.0.0.0.0.0.0.0.0.0.0.7" id="_x30_.1.10.0.0.0.0.0.7" enable-background="new    " d="M-18.36,-36.071l0.271,0c0.151,0.018,0.271,-0.012,0.271,0.098c0,0.611,0,4.703,0,4.854c0,0.168,-0.065,0.176,-0.065,-0.012c0,-0.131,0,-3.893,0,-4.346c0,-0.457,-0.105,-0.518,-0.197,-0.518l-0.272,0.002C-18.532,-35.994,-18.532,-36.071,-18.36,-36.071z"/>
                       <path  opacity="0.03" gorn="0.2.10.0.0.0.0.0.0.0.0.0.0.0.0.0.0.8" id="_x30_.1.10.0.0.0.0.0.8" enable-background="new    " d="M-21.319,-30.944c-0.068,0,-0.138,0.012,-0.138,-0.098c0,-0.611,0,-4.667,0,-4.817c0,-0.168,0.065,-0.176,0.065,0.008c0,0.135,0.002,3.138,0.002,3.589C-21.387,-31.667,-21.319,-30.944,-21.319,-30.944z"/>
                       <path  fill="#D1C690" gorn="0.2.10.0.0.0.0.0.0.0.0.0.0.0.0.0.0.9" id="_x30_.1.10.0.0.0.0.0.9" d="M-21.541,-37.08l0,0.771l0.521,0c0.125,0,0.213,0.08,0.268,0.188l3.047,0l0,-1.01l-3.784,0l-0.05,0"/>
                       <g transform="matrix(2.57889e-06, 1, -1, 2.57889e-06, -54.3568, -18.9)">
                        <g >
                         <g >
                          <g >
                           <g  gorn="0.2.10.0.0.0.0.0.0.0.0.0.0.0.0.0.0.10.0.0.0" id="_x30_.1.10.0.0.0.0.0.10">
                            <rect  width="1.006" x="-18.23" opacity="0.5" y="-36.653" fill="#FFFFFF" gorn="0.2.10.0.0.0.0.0.0.0.0.0.0.0.0.0.0.10.0.0.0.0" height="0.052" id="_x30_.1.10.0.0.0.0.0.10.0" enable-background="new    "/>
                           </g>
                          </g>
                         </g>
                        </g>
                       </g>
                       <path  fill="#D1C690" gorn="0.2.10.0.0.0.0.0.0.0.0.0.0.0.0.0.0.11" id="_x30_.1.10.0.0.0.0.0.11" d="M-21.541,-29.733l0.049,0l3.784,0l0,-1.072l-3.464,0c-0.056,0.105,-0.146,0.191,-0.271,0.191l-0.1,0l0,0.83"/>
                       <g transform="matrix(2.57889e-06, 1, -1, 2.57889e-06, -47.9999, -12.5431)">
                        <g >
                         <g >
                          <g >
                           <g  gorn="0.2.10.0.0.0.0.0.0.0.0.0.0.0.0.0.0.12.0.0.0" id="_x30_.1.10.0.0.0.0.0.12">
                            <rect  width="1.072" x="-18.262" opacity="0.5" y="-30.296" fill="#FFFFFF" gorn="0.2.10.0.0.0.0.0.0.0.0.0.0.0.0.0.0.12.0.0.0.0" height="0.052" id="_x30_.1.10.0.0.0.0.0.12.0" enable-background="new    "/>
                           </g>
                          </g>
                         </g>
                        </g>
                       </g>
                      </g>
                     </g>
                    </g>
                   </g>
                  </g>
                 </g>
                </g>
               </g>
              </g>
             </g>
            </g>
           </g>
          </g>
         </g>
        </g>
       </g>
      </g>
     </g>
     <g transform="matrix(1, 0, 0, 1, 89.0222, 43.6955)">
      <g >
       <g >
        <g >
         <g  gorn="0.2.11.0.0.0" id="_x30_.1.11">
          <g  gorn="0.2.11.0.0.0.0" id="chip-led0805_3_">
           <g transform="matrix(0, 1, -1, 0, 5.62951, 1.77951)">
            <g >
             <g >
              <g >
               <g  gorn="0.2.11.0.0.0.0.0.0.0.0" id="_x30_.1.11.0.0">
                <g  gorn="0.2.11.0.0.0.0.0.0.0.0.0" id="_x30_.1.11.0.0.0">
                 <g transform="matrix(1, 0, 0, 1, 21.5539, 31.3385)">
                  <g >
                   <g >
                    <g >
                     <g  gorn="0.2.11.0.0.0.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.11.0.0.0.0">
                      <g  gorn="0.2.11.0.0.0.0.0.0.0.0.0.0.0.0.0.0" id="led-0603_4_">
                       <line  fill="none" gorn="0.2.11.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.11.0.0.0.0.0.0" y1="-37.083" x1="-21.535" y2="-29.847" x2="-21.535"/>
                       <g transform="matrix(2.57889e-06, 1, -1, 2.57889e-06, -53.0294, -13.788)">
                        <g >
                         <g >
                          <g >
                           <g  gorn="0.2.11.0.0.0.0.0.0.0.0.0.0.0.0.0.0.1.0.0.0" id="_x30_.1.11.0.0.0.0.0.1">
                            <rect  width="7.348" x="-23.292" y="-35.322" fill="#F2F2F2" gorn="0.2.11.0.0.0.0.0.0.0.0.0.0.0.0.0.0.1.0.0.0.0" height="3.833" id="_x30_.1.11.0.0.0.0.0.1.0"/>
                           </g>
                          </g>
                         </g>
                        </g>
                       </g>
                       <path  fill="#22B573" gorn="0.2.11.0.0.0.0.0.0.0.0.0.0.0.0.0.0.2" fill-opacity="0.7" id="_x30_.1.11.0.0.0.0.0.2" d="M-21.541,-32.333c0,0,0.467,0.645,0.426,0.867c-0.041,0.219,0.148,0.541,0,0.676l-0.424,-0.018L-21.541,-32.333z"/>
                       <g  gorn="0.2.11.0.0.0.0.0.0.0.0.0.0.0.0.0.0.3" id="_x30_.1.11.0.0.0.0.0.3">
                        <g transform="matrix(2.57889e-06, 1, -1, 2.57889e-06, -53.0694, -13.8876)">
                         <g >
                          <g >
                           <g >
                            <g  gorn="0.2.11.0.0.0.0.0.0.0.0.0.0.0.0.0.0.3.0.0.0.0" id="_x30_.1.11.0.0.0.0.0.3.0">
                             <rect  width="0.854" x="-20.016" y="-33.957" fill="#FFFFFF" gorn="0.2.11.0.0.0.0.0.0.0.0.0.0.0.0.0.0.3.0.0.0.0.0" height="0.961" id="_x30_.1.11.0.0.0.0.0.3.0.0"/>
                            </g>
                           </g>
                          </g>
                         </g>
                        </g>
                        <g transform="matrix(2.57889e-06, 1, -1, 2.57889e-06, -53.5514, -13.4056)">
                         <g >
                          <g >
                           <g >
                            <g  gorn="0.2.11.0.0.0.0.0.0.0.0.0.0.0.0.0.0.3.1.0.0.0" id="_x30_.1.11.0.0.0.0.0.3.1">
                             <rect  width="0.854" x="-20.498" y="-33.501" fill="#B3B3B3" gorn="0.2.11.0.0.0.0.0.0.0.0.0.0.0.0.0.0.3.1.0.0.0.0" height="0.049" id="_x30_.1.11.0.0.0.0.0.3.1.0"/>
                            </g>
                           </g>
                          </g>
                         </g>
                        </g>
                       </g>
                       <g  gorn="0.2.11.0.0.0.0.0.0.0.0.0.0.0.0.0.0.4" id="_x30_.1.11.0.0.0.0.0.4">
                        <polygon  fill="#D1C690" points="-21.115,-31.753,-21.219,-30.79,-20.488,-30.79,-20.592,-31.753" gorn="0.2.11.0.0.0.0.0.0.0.0.0.0.0.0.0.0.4.0" id="_x30_.1.11.0.0.0.0.0.4.0"/>
                        <g  gorn="0.2.11.0.0.0.0.0.0.0.0.0.0.0.0.0.0.4.1" id="_x30_.1.11.0.0.0.0.0.4.1">
                         <path  fill="#D1C690" gorn="0.2.11.0.0.0.0.0.0.0.0.0.0.0.0.0.0.4.1.0" id="_x30_.1.11.0.0.0.0.0.4.1.0" d="M-20.918,-31.692c0,-0.002,0,-0.004,0,-0.008c0.035,-0.266,0.104,-0.447,0.162,-0.598c0.08,-0.209,0.782,-0.559,0.696,-0.828c-0.012,-0.027,0.011,-0.06,0.043,-0.066c0.035,-0.008,0.068,0.01,0.078,0.039c0.095,0.305,-0.617,0.674,-0.701,0.893c-0.06,0.148,-0.123,0.318,-0.155,0.572c-0.004,0.029,-0.033,0.055,-0.068,0.049C-20.892,-31.642,-20.918,-31.665,-20.918,-31.692z"/>
                        </g>
                        <polygon  fill="#D1C690" points="-18.229,-35.173,-18.126,-36.139,-18.856,-36.139,-18.753,-35.173" gorn="0.2.11.0.0.0.0.0.0.0.0.0.0.0.0.0.0.4.2" id="_x30_.1.11.0.0.0.0.0.4.2"/>
                        <g  gorn="0.2.11.0.0.0.0.0.0.0.0.0.0.0.0.0.0.4.3" id="_x30_.1.11.0.0.0.0.0.4.3">
                         <path  fill="#D1C690" gorn="0.2.11.0.0.0.0.0.0.0.0.0.0.0.0.0.0.4.3.0" id="_x30_.1.11.0.0.0.0.0.4.3.0" d="M-19.75,-33.52c0,-0.025,0.02,-0.049,0.047,-0.055c0.292,-0.063,1.152,-1.088,1.152,-1.885c0,-0.033,0.026,-0.057,0.063,-0.057c0.034,0.002,0.063,0.025,0.063,0.057l0,0.002c0,0.749,-0.77,1.891,-1.245,1.993c-0.035,0.008,-0.068,-0.012,-0.078,-0.041C-19.75,-33.511,-19.75,-33.515,-19.75,-33.52z"/>
                        </g>
                        <path  fill="#D1C690" gorn="0.2.11.0.0.0.0.0.0.0.0.0.0.0.0.0.0.4.4" id="_x30_.1.11.0.0.0.0.0.4.4" d="M-19.764,-33.05c0,0,0.002,-0.356,-0.311,-0.383c0,0.07,0,0.383,0,0.383L-19.764,-33.05z"/>
                        <path  fill="#D1C690" gorn="0.2.11.0.0.0.0.0.0.0.0.0.0.0.0.0.0.4.5" id="_x30_.1.11.0.0.0.0.0.4.5" d="M-19.445,-33.485c0,0,-0.306,0.158,-0.351,0.053c-0.048,-0.107,-0.052,-0.178,0.028,-0.24C-19.686,-33.733,-19.445,-33.485,-19.445,-33.485z"/>
                        <path  fill="#9D956C" gorn="0.2.11.0.0.0.0.0.0.0.0.0.0.0.0.0.0.4.6" id="_x30_.1.11.0.0.0.0.0.4.6" d="M-20.113,-33.126c0.084,0.27,-0.618,0.619,-0.698,0.828c-0.06,0.145,-0.127,0.33,-0.162,0.598l0.059,0c0.035,-0.266,0.104,-0.447,0.162,-0.598c0.08,-0.209,0.782,-0.559,0.696,-0.828L-20.113,-33.126z"/>
                        <polygon  fill="#9D956C" points="-18.806,-35.173,-18.91,-36.139,-18.856,-36.139,-18.753,-35.173" gorn="0.2.11.0.0.0.0.0.0.0.0.0.0.0.0.0.0.4.7" id="_x30_.1.11.0.0.0.0.0.4.7"/>
                        <path  fill="#9D956C" gorn="0.2.11.0.0.0.0.0.0.0.0.0.0.0.0.0.0.4.8" id="_x30_.1.11.0.0.0.0.0.4.8" d="M-19.758,-33.577c0.291,-0.062,1.212,-1.07,1.149,-1.885l0.06,0c0.06,0.877,-0.86,1.826,-1.152,1.887L-19.758,-33.577z"/>
                        <path  fill="#9D956C" gorn="0.2.11.0.0.0.0.0.0.0.0.0.0.0.0.0.0.4.9" id="_x30_.1.11.0.0.0.0.0.4.9" d="M-20.131,-33.433c0,0.07,0,0.381,0,0.381l0.057,0c0,0,0,-0.311,0,-0.381L-20.131,-33.433z"/>
                        <path  fill="#9D956C" gorn="0.2.11.0.0.0.0.0.0.0.0.0.0.0.0.0.0.4.10" id="_x30_.1.11.0.0.0.0.0.4.10" d="M-19.82,-33.673c-0.08,0.063,-0.076,0.131,-0.031,0.238l0.06,0.002c-0.049,-0.107,-0.052,-0.179,0.028,-0.24L-19.82,-33.673z"/>
                       </g>
                       <g transform="matrix(2.57889e-06, 1, -1, 2.57889e-06, -51.2218, -15.7626)">
                        <g >
                         <g >
                          <g >
                           <g  gorn="0.2.11.0.0.0.0.0.0.0.0.0.0.0.0.0.0.5.0.0.0" id="_x30_.1.11.0.0.0.0.0.5">
                            <rect  width="4.223" x="-19.839" opacity="0.5" y="-33.516" fill="#FFFFFF" gorn="0.2.11.0.0.0.0.0.0.0.0.0.0.0.0.0.0.5.0.0.0.0" height="0.051" id="_x30_.1.11.0.0.0.0.0.5.0" enable-background="new    "/>
                           </g>
                          </g>
                         </g>
                        </g>
                       </g>
                       <path  opacity="0.5" fill="#F2F2F2" gorn="0.2.11.0.0.0.0.0.0.0.0.0.0.0.0.0.0.6" id="_x30_.1.11.0.0.0.0.0.6" enable-background="new    " d="M-17.708,-36.122l-3.831,0l0,5.317l3.831,0.004L-17.708,-36.122z"/>
                       <path  opacity="0.55" fill="#FFFFFF" gorn="0.2.11.0.0.0.0.0.0.0.0.0.0.0.0.0.0.7" id="_x30_.1.11.0.0.0.0.0.7" enable-background="new    " d="M-18.359,-36.071l0.271,0c0.151,0.018,0.271,-0.012,0.271,0.098c0,0.611,0,4.703,0,4.854c0,0.168,-0.065,0.176,-0.065,-0.012c0,-0.131,0,-3.893,0,-4.346c0,-0.457,-0.105,-0.518,-0.197,-0.518l-0.272,0.002C-18.532,-35.994,-18.532,-36.071,-18.359,-36.071z"/>
                       <path  opacity="0.03" gorn="0.2.11.0.0.0.0.0.0.0.0.0.0.0.0.0.0.8" id="_x30_.1.11.0.0.0.0.0.8" enable-background="new    " d="M-21.317,-30.944c-0.068,0,-0.138,0.012,-0.138,-0.098c0,-0.611,0,-4.667,0,-4.817c0,-0.168,0.065,-0.176,0.065,0.008c0,0.135,0.002,3.138,0.002,3.589C-21.387,-31.667,-21.317,-30.944,-21.317,-30.944z"/>
                       <path  fill="#D1C690" gorn="0.2.11.0.0.0.0.0.0.0.0.0.0.0.0.0.0.9" id="_x30_.1.11.0.0.0.0.0.9" d="M-21.541,-37.08l0,0.771l0.521,0c0.125,0,0.213,0.08,0.268,0.188l3.047,0l0,-1.01l-3.784,0l-0.05,0"/>
                       <g transform="matrix(2.57889e-06, 1, -1, 2.57889e-06, -54.3578, -18.8995)">
                        <g >
                         <g >
                          <g >
                           <g  gorn="0.2.11.0.0.0.0.0.0.0.0.0.0.0.0.0.0.10.0.0.0" id="_x30_.1.11.0.0.0.0.0.10">
                            <rect  width="1.006" x="-18.23" opacity="0.5" y="-36.653" fill="#FFFFFF" gorn="0.2.11.0.0.0.0.0.0.0.0.0.0.0.0.0.0.10.0.0.0.0" height="0.052" id="_x30_.1.11.0.0.0.0.0.10.0" enable-background="new    "/>
                           </g>
                          </g>
                         </g>
                        </g>
                       </g>
                       <path  fill="#D1C690" gorn="0.2.11.0.0.0.0.0.0.0.0.0.0.0.0.0.0.11" id="_x30_.1.11.0.0.0.0.0.11" d="M-21.541,-29.733l0.049,0l3.784,0l0,-1.072l-3.464,0c-0.056,0.105,-0.146,0.191,-0.271,0.191l-0.1,0l0,0.83"/>
                       <g transform="matrix(2.57889e-06, 1, -1, 2.57889e-06, -48.0001, -12.5429)">
                        <g >
                         <g >
                          <g >
                           <g  gorn="0.2.11.0.0.0.0.0.0.0.0.0.0.0.0.0.0.12.0.0.0" id="_x30_.1.11.0.0.0.0.0.12">
                            <rect  width="1.072" x="-18.262" opacity="0.5" y="-30.294" fill="#FFFFFF" gorn="0.2.11.0.0.0.0.0.0.0.0.0.0.0.0.0.0.12.0.0.0.0" height="0.052" id="_x30_.1.11.0.0.0.0.0.12.0" enable-background="new    "/>
                           </g>
                          </g>
                         </g>
                        </g>
                       </g>
                      </g>
                     </g>
                    </g>
                   </g>
                  </g>
                 </g>
                </g>
               </g>
              </g>
             </g>
            </g>
           </g>
          </g>
         </g>
        </g>
       </g>
      </g>
     </g>
     <g transform="matrix(1, 0, 0, 1, 31.1856, 77.2272)">
      <g >
       <g >
        <g >
         <g  gorn="0.2.12.0.0.0" id="_x30_.1.12">
          <g  gorn="0.2.12.0.0.0.0" id="sot223">
           <g transform="matrix(0, 1, -1, 0, 19.6385, 0.486504)">
            <g >
             <g >
              <g >
               <g  gorn="0.2.12.0.0.0.0.0.0.0.0" id="_x30_.1.12.0.0">
                <g  gorn="0.2.12.0.0.0.0.0.0.0.0.0" id="_x30_.1.12.0.0.0">
                 <g  gorn="0.2.12.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.12.0.0.0.0">
                  <g transform="matrix(2.57889e-06, 1, -1, 2.57889e-06, 34.358, -27.0816)">
                   <g >
                    <g >
                     <g >
                      <g  gorn="0.2.12.0.0.0.0.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.12.0.0.0.0.0">
                       <rect  width="4.896" x="28.274" y="1.913" fill="#999999" gorn="0.2.12.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0" height="3.458" id="_x30_.1.12.0.0.0.0.0.0"/>
                      </g>
                     </g>
                    </g>
                   </g>
                  </g>
                  <g transform="matrix(2.57889e-06, 1, -1, 2.57889e-06, 27.8034, -20.526)">
                   <g >
                    <g >
                     <g >
                      <g  gorn="0.2.12.0.0.0.0.0.0.0.0.0.0.1.0.0.0" id="_x30_.1.12.0.0.0.0.1">
                       <rect  width="4.896" x="21.719" y="1.913" fill="#999999" gorn="0.2.12.0.0.0.0.0.0.0.0.0.0.1.0.0.0.0" height="3.459" id="_x30_.1.12.0.0.0.0.1.0"/>
                      </g>
                     </g>
                    </g>
                   </g>
                  </g>
                  <g transform="matrix(2.57889e-06, 1, -1, 2.57889e-06, 21.2482, -13.9718)">
                   <g >
                    <g >
                     <g >
                      <g  gorn="0.2.12.0.0.0.0.0.0.0.0.0.0.2.0.0.0" id="_x30_.1.12.0.0.0.0.2">
                       <rect  width="4.896" x="15.164" y="1.914" fill="#999999" gorn="0.2.12.0.0.0.0.0.0.0.0.0.0.2.0.0.0.0" height="3.455" id="_x30_.1.12.0.0.0.0.2.0"/>
                      </g>
                     </g>
                    </g>
                   </g>
                  </g>
                  <g transform="matrix(2.57889e-06, 1, -1, 2.57889e-06, 31.983, -29.4566)">
                   <g >
                    <g >
                     <g >
                      <g  gorn="0.2.12.0.0.0.0.0.0.0.0.0.0.3.0.0.0" id="_x30_.1.12.0.0.0.0.3">
                       <rect  width="0.146" x="30.649" opacity="0.2" y="-0.462" fill="#FFFFFF" gorn="0.2.12.0.0.0.0.0.0.0.0.0.0.3.0.0.0.0" height="3.458" id="_x30_.1.12.0.0.0.0.3.0" enable-background="new    "/>
                      </g>
                     </g>
                    </g>
                   </g>
                  </g>
                  <g transform="matrix(2.57889e-06, 1, -1, 2.57889e-06, 25.4284, -22.901)">
                   <g >
                    <g >
                     <g >
                      <g  gorn="0.2.12.0.0.0.0.0.0.0.0.0.0.4.0.0.0" id="_x30_.1.12.0.0.0.0.4">
                       <rect  width="0.146" x="24.094" opacity="0.2" y="-0.462" fill="#FFFFFF" gorn="0.2.12.0.0.0.0.0.0.0.0.0.0.4.0.0.0.0" height="3.459" id="_x30_.1.12.0.0.0.0.4.0" enable-background="new    "/>
                      </g>
                     </g>
                    </g>
                   </g>
                  </g>
                  <g transform="matrix(2.57889e-06, 1, -1, 2.57889e-06, 18.8732, -16.3468)">
                   <g >
                    <g >
                     <g >
                      <g  gorn="0.2.12.0.0.0.0.0.0.0.0.0.0.5.0.0.0" id="_x30_.1.12.0.0.0.0.5">
                       <rect  width="0.146" x="17.539" opacity="0.2" y="-0.461" fill="#FFFFFF" gorn="0.2.12.0.0.0.0.0.0.0.0.0.0.5.0.0.0.0" height="3.455" id="_x30_.1.12.0.0.0.0.5.0" enable-background="new    "/>
                      </g>
                     </g>
                    </g>
                   </g>
                  </g>
                  <g transform="matrix(2.57889e-06, 1, -1, 2.57889e-06, 42.8349, -5.4926)">
                   <g >
                    <g >
                     <g >
                      <g  gorn="0.2.12.0.0.0.0.0.0.0.0.0.0.6.0.0.0" id="_x30_.1.12.0.0.0.0.6">
                       <rect  width="5.285" x="21.523" y="13.571" fill="#999999" gorn="0.2.12.0.0.0.0.0.0.0.0.0.0.6.0.0.0.0" height="10.207" id="_x30_.1.12.0.0.0.0.6.0"/>
                      </g>
                     </g>
                    </g>
                   </g>
                  </g>
                  <g transform="matrix(2.57889e-06, 1, -1, 2.57889e-06, 45.3969, -2.9306)">
                   <g >
                    <g >
                     <g >
                      <g  gorn="0.2.12.0.0.0.0.0.0.0.0.0.0.7.0.0.0" id="_x30_.1.12.0.0.0.0.7">
                       <rect  width="0.161" x="24.085" opacity="0.2" y="16.133" fill="#FFFFFF" gorn="0.2.12.0.0.0.0.0.0.0.0.0.0.7.0.0.0.0" height="10.207" id="_x30_.1.12.0.0.0.0.7.0" enable-background="new    "/>
                      </g>
                     </g>
                    </g>
                   </g>
                  </g>
                  <g transform="matrix(2.57889e-06, 1, -1, 2.57889e-06, 35.224, -13.1073)">
                   <g >
                    <g >
                     <g >
                      <g  gorn="0.2.12.0.0.0.0.0.0.0.0.0.0.8.0.0.0" id="_x30_.1.12.0.0.0.0.8">
                       <rect  width="9.943" x="19.196" y="1.482" fill="#303030" gorn="0.2.12.0.0.0.0.0.0.0.0.0.0.8.0.0.0.0" height="19.16" id="_x30_.1.12.0.0.0.0.8.0"/>
                      </g>
                     </g>
                    </g>
                   </g>
                  </g>
                  <polygon  fill="#1F1F1F" points="33.744,16.031,14.582,16.031,15.301,15.31,33.021,15.31" gorn="0.2.12.0.0.0.0.0.0.0.0.0.0.9" id="_x30_.1.12.0.0.0.0.9"/>
                  <polygon  fill="#1F1F1F" points="33.744,6.088,14.582,6.088,15.301,6.811,33.021,6.811" gorn="0.2.12.0.0.0.0.0.0.0.0.0.0.10" id="_x30_.1.12.0.0.0.0.10"/>
                  <polygon  points="33.744,16.031,33.744,6.088,33.021,6.811,33.021,15.31" gorn="0.2.12.0.0.0.0.0.0.0.0.0.0.11" id="_x30_.1.12.0.0.0.0.11"/>
                  <polygon  fill="#3D3D3D" points="14.582,16.031,14.582,6.088,15.301,6.811,15.301,15.31" gorn="0.2.12.0.0.0.0.0.0.0.0.0.0.12" id="_x30_.1.12.0.0.0.0.12"/>
                  <circle  fill="#1F1F1F" cx="31.582" gorn="0.2.12.0.0.0.0.0.0.0.0.0.0.13" cy="8.251" id="_x30_.1.12.0.0.0.0.13" r="0.72"/>
                 </g>
                </g>
               </g>
              </g>
             </g>
            </g>
           </g>
          </g>
         </g>
        </g>
       </g>
      </g>
     </g>
     <g transform="matrix(1, 0, 0, 1, -3.65847, 104.535)">
      <g >
       <g >
        <g >
         <g  gorn="0.2.13.0.0.0" id="_x30_.1.13">
          <g  gorn="0.2.13.0.0.0.0" id="powersupply_dc-21mm">
           <g transform="matrix(0, 1, -1, 0, 32.3005, 6.84151)">
            <g >
             <g >
              <g >
               <g  gorn="0.2.13.0.0.0.0.0.0.0.0" id="_x30_.1.13.0.0">
                <g  gorn="0.2.13.0.0.0.0.0.0.0.0.0" id="_x30_.1.13.0.0.0">
                 <g transform="matrix(1, 0, 0, 1, 16.998, 98.8718)">
                  <g >
                   <g >
                    <g >
                     <g  gorn="0.2.13.0.0.0.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.13.0.0.0.0">
                      <g  gorn="0.2.13.0.0.0.0.0.0.0.0.0.0.0.0.0.0" id="dc-21mm">
                       <g transform="matrix(0, 1, -1, 0, 38.6844, 13.1725)">
                        <g >
                         <g >
                          <g >
                           <g  gorn="0.2.13.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.13.0.0.0.0.0.0">
                            <g  gorn="0.2.13.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.13.0.0.0.0.0.0.0">
                             <g  gorn="0.2.13.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.13.0.0.0.0.0.0.0.0">
                              <g  gorn="0.2.13.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.13.0.0.0.0.0.0.0.0.0">
                               <rect  width="32.972" x="-134.003" y="26.131" fill="#232323" gorn="0.2.13.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0" height="23.732" id="_x30_.1.13.0.0.0.0.0.0.0.0.0.0"/>
                               <rect  width="31.937" x="-133.572" y="47.644" fill="#494949" gorn="0.2.13.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.1" height="1.646" id="_x30_.1.13.0.0.0.0.0.0.0.0.0.1"/>
                               <rect  width="31.936" x="-133.57" y="42.273" fill="#3D3D3D" gorn="0.2.13.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.2" height="5.369" fill-opacity="0.3" id="_x30_.1.13.0.0.0.0.0.0.0.0.0.2"/>
                               <rect  width="32.973" x="-133.572" y="26.648" gorn="0.2.13.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.3" height="1.619" id="_x30_.1.13.0.0.0.0.0.0.0.0.0.3"/>
                               <rect  width="32.973" x="-133.572" y="28.221" fill="#0F0F0F" gorn="0.2.13.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.4" height="5.826" fill-opacity="0.4" id="_x30_.1.13.0.0.0.0.0.0.0.0.0.4"/>
                              </g>
                              <rect  width="0.592" x="-134.003" opacity="0.2" y="26.133" gorn="0.2.13.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.1" height="23.73" id="_x30_.1.13.0.0.0.0.0.0.0.0.1" enable-background="new    "/>
                             </g>
                             <line  opacity="0.5" fill="none" gorn="0.2.13.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.1" stroke="#000000" id="_x30_.1.13.0.0.0.0.0.0.0.1" enable-background="new    " y1="26.131" stroke-width="0.25" x1="-131.193" y2="49.863" x2="-131.193" stroke-miterlimit="10"/>
                             <g  gorn="0.2.13.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.2" id="_x30_.1.13.0.0.0.0.0.0.0.2">
                              <rect  width="1.287" x="-104.529" opacity="0.25" y="26.109" gorn="0.2.13.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.2.0" height="23.729" id="_x30_.1.13.0.0.0.0.0.0.0.2.0" enable-background="new    "/>
                              <path  opacity="0.25" gorn="0.2.13.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.2.1" stroke="#565656" id="_x30_.1.13.0.0.0.0.0.0.0.2.1" enable-background="new    " stroke-width="0.25" d="M-103.525,45.54L-103.525,30.46l-13.296,0c-4.166,0,-7.541,3.375,-7.541,7.541c0,4.164,3.375,7.541,7.541,7.541L-103.525,45.54L-103.525,45.54z" stroke-miterlimit="10"/>
                             </g>
                             <g  gorn="0.2.13.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.3" id="_x30_.1.13.0.0.0.0.0.0.0.3">
                              <path  fill="#232323" gorn="0.2.13.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.3.0" id="_x30_.1.13.0.0.0.0.0.0.0.3.0" d="M-103.525,45.54L-103.525,30.46l-13.296,0c-4.166,0,-7.541,3.375,-7.541,7.541c0,4.164,3.375,7.541,7.541,7.541L-103.525,45.54L-103.525,45.54z"/>
                              <rect  width="7.688" x="-104.251" y="25.242" fill="#232323" gorn="0.2.13.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.3.1" height="25.514" id="_x30_.1.13.0.0.0.0.0.0.0.3.1"/>
                             </g>
                             <rect  width="1.701" x="-135.705" y="35.142" fill="#6D6D6D" gorn="0.2.13.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.4" height="5.713" id="_x30_.1.13.0.0.0.0.0.0.0.4"/>
                             <rect  width="0.976" x="-134.977" y="32.387" fill="#494949" gorn="0.2.13.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.5" height="11.226" id="_x30_.1.13.0.0.0.0.0.0.0.5"/>
                             <rect  width="6.266" x="-103.524" y="49.291" fill="#494949" gorn="0.2.13.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.6" height="1.051" id="_x30_.1.13.0.0.0.0.0.0.0.6"/>
                             <rect  width="6.267" x="-103.524" y="25.603" gorn="0.2.13.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.0.7" height="1.051" id="_x30_.1.13.0.0.0.0.0.0.0.7"/>
                            </g>
                           </g>
                          </g>
                         </g>
                        </g>
                       </g>
                      </g>
                     </g>
                    </g>
                   </g>
                  </g>
                 </g>
                </g>
               </g>
              </g>
             </g>
            </g>
           </g>
          </g>
         </g>
        </g>
       </g>
      </g>
     </g>
     <g transform="matrix(1, 0, 0, 1, 3.4818, 23.55)">
      <g >
       <g >
        <g >
         <g  gorn="0.2.14.0.0.0" id="_x30_.1.14">
          <g  gorn="0.2.14.0.0.0.0" id="pn61729">
           <g transform="matrix(0, -1, 1, 0, 1.809, 42.439)">
            <g >
             <g >
              <g >
               <g  gorn="0.2.14.0.0.0.0.0.0.0.0" id="_x30_.1.14.0.0">
                <g  gorn="0.2.14.0.0.0.0.0.0.0.0.0" id="_x30_.1.14.0.0.0">
                 <g  gorn="0.2.14.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.14.0.0.0.0">
                  <g  gorn="0.2.14.0.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.14.0.0.0.0.0">
                   <path  fill="#999999" gorn="0.2.14.0.0.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.14.0.0.0.0.0.0" d="M43.103,14.31l0,2.956l-2.039,0l-2.035,0l-0.002,-2.956l0,-1.928l3.17,0c0.502,0,0.908,0.406,0.908,0.907C43.105,13.289,43.105,14.31,43.103,14.31z"/>
                   <path  fill="#808080" gorn="0.2.14.0.0.0.0.0.0.0.0.0.0.0.1" id="_x30_.1.14.0.0.0.0.0.1" d="M43.103,13.189l-4.076,0l0,-0.807c0,0,3.049,0,3.318,0C42.748,12.382,43.103,12.942,43.103,13.189z"/>
                  </g>
                  <g  gorn="0.2.14.0.0.0.0.0.0.0.0.0.0.1" id="_x30_.1.14.0.0.0.0.1">
                   <g transform="matrix(-2.54711e-06, -1, 1, -2.54711e-06, 1.9763, 43.6033)">
                    <g >
                     <g >
                      <g >
                       <g  gorn="0.2.14.0.0.0.0.0.0.0.0.0.0.1.0.0.0.0" id="_x30_.1.14.0.0.0.0.1.0">
                        <rect  width="36.682" x="4.451" y="4.577" fill="#B3B3B3" gorn="0.2.14.0.0.0.0.0.0.0.0.0.0.1.0.0.0.0.0" height="32.479" id="_x30_.1.14.0.0.0.0.1.0.0"/>
                       </g>
                      </g>
                     </g>
                    </g>
                   </g>
                   <g transform="matrix(-2.54711e-06, -1, 1, -2.54711e-06, 24.0981, 21.481)">
                    <g >
                     <g >
                      <g >
                       <g  gorn="0.2.14.0.0.0.0.0.0.0.0.0.0.1.1.0.0.0" id="_x30_.1.14.0.0.0.0.1.1">
                        <rect  width="7.565" x="19.009" y="-17.546" fill="#999999" gorn="0.2.14.0.0.0.0.0.0.0.0.0.0.1.1.0.0.0.0" height="32.479" id="_x30_.1.14.0.0.0.0.1.1.0"/>
                       </g>
                      </g>
                     </g>
                    </g>
                   </g>
                   <g transform="matrix(-2.54711e-06, -1, 1, -2.54711e-06, -9.4585, 24.6065)">
                    <g >
                     <g >
                      <g >
                       <g  gorn="0.2.14.0.0.0.0.0.0.0.0.0.0.1.2.0.0.0" id="_x30_.1.14.0.0.0.0.1.2">
                        <rect  width="44.247" x="-14.548" opacity="0.5" y="16.012" fill="#CCCCCC" gorn="0.2.14.0.0.0.0.0.0.0.0.0.0.1.2.0.0.0.0" height="2.046" id="_x30_.1.14.0.0.0.0.1.2.0" enable-background="new    "/>
                       </g>
                      </g>
                     </g>
                    </g>
                   </g>
                   <g transform="matrix(-2.54711e-06, -1, 1, -2.54711e-06, 20.9742, 55.0381)">
                    <g >
                     <g >
                      <g >
                       <g  gorn="0.2.14.0.0.0.0.0.0.0.0.0.0.1.3.0.0.0" id="_x30_.1.14.0.0.0.0.1.3">
                        <rect  width="44.247" x="15.885" opacity="0.2" y="16.011" gorn="0.2.14.0.0.0.0.0.0.0.0.0.0.1.3.0.0.0.0" height="2.047" id="_x30_.1.14.0.0.0.0.1.3.0" enable-background="new    "/>
                       </g>
                      </g>
                     </g>
                    </g>
                   </g>
                  </g>
                  <g  gorn="0.2.14.0.0.0.0.0.0.0.0.0.0.2" id="_x30_.1.14.0.0.0.0.2">
                   <path  fill="#B3B3B3" gorn="0.2.14.0.0.0.0.0.0.0.0.0.0.2.0" id="_x30_.1.14.0.0.0.0.2.0" d="M2.476,14.308l0,2.956l2.039,0l2.038,0l0,-2.956L6.553,12.38L3.381,12.38c-0.502,0,-0.905,0.406,-0.905,0.907L2.476,14.308z"/>
                   <path  fill="#E6E6E6" gorn="0.2.14.0.0.0.0.0.0.0.0.0.0.2.1" id="_x30_.1.14.0.0.0.0.2.1" d="M2.476,13.187l4.077,0L6.553,12.38c0,0,-3.051,0,-3.319,0C2.83,12.38,2.476,12.94,2.476,13.187z"/>
                  </g>
                 </g>
                </g>
               </g>
              </g>
             </g>
            </g>
           </g>
          </g>
         </g>
        </g>
       </g>
      </g>
     </g>
     <g transform="matrix(1, 0, 0, 1, 8.7817, 8.95615)">
      <g >
       <g >
        <g >
         <g  gorn="0.2.15.0.0.0" id="_x30_.1.15">
          <g  gorn="0.2.15.0.0.0.0" id="smd_157sw">
           <g transform="matrix(0, -1, 1, 0, 0.777996, 13.82)">
            <g >
             <g >
              <g >
               <g  gorn="0.2.15.0.0.0.0.0.0.0.0" id="_x30_.1.15.0.0">
                <g  gorn="0.2.15.0.0.0.0.0.0.0.0.0" id="_x30_.1.15.0.0.0">
                 <polygon  fill="#CCCCCC" points="3.229,21.262,3.597,21.262,3.597,29.526,3.229,29.526,3.229,35.772,19.208,35.772,19.208,15.015,3.229,15.015" gorn="0.2.15.0.0.0.0.0.0.0.0.0.0" id="_x30_.1.15.0.0.0.0"/>
                 <polygon  fill="#CCCCCC" points="21.768,29.526,21.399,29.526,21.399,21.262,21.768,21.262,21.768,15.015,5.908,15.015,5.908,35.772,21.768,35.772" gorn="0.2.15.0.0.0.0.0.0.0.0.0.1" id="_x30_.1.15.0.0.0.1"/>
                 <circle  fill="#641D1C" cx="12.496" gorn="0.2.15.0.0.0.0.0.0.0.0.0.2" cy="25.395" id="_x30_.1.15.0.0.0.2" r="5.117"/>
                 <path  opacity="0.2" gorn="0.2.15.0.0.0.0.0.0.0.0.0.3" id="_x30_.1.15.0.0.0.3" enable-background="new    " d="M12.746,30.51c2.827,0,5.118,-2.289,5.118,-5.114c0,-2.826,-2.289,-5.12,-5.118,-5.12l-0.249,0c2.827,0,5.118,2.292,5.118,5.12c0,2.825,-2.291,5.114,-5.118,5.114L12.746,30.51z"/>
                 <circle  fill="#852725" cx="12.497" gorn="0.2.15.0.0.0.0.0.0.0.0.0.4" cy="25.395" id="_x30_.1.15.0.0.0.4" r="4.93"/>
                 <circle  fill="#852725" cx="12.381" gorn="0.2.15.0.0.0.0.0.0.0.0.0.5" cy="25.395" id="_x30_.1.15.0.0.0.5" r="4.929"/>
                 <g  gorn="0.2.15.0.0.0.0.0.0.0.0.0.6" id="_x30_.1.15.0.0.0.6">
                  <path  opacity="0.1" gorn="0.2.15.0.0.0.0.0.0.0.0.0.6.0" id="_x30_.1.15.0.0.0.6.0" enable-background="new    " d="M7.568,25.512c0,2.724,2.206,4.931,4.931,4.931c2.724,0,4.929,-2.207,4.929,-4.931l0,-0.233c0,2.724,-2.208,4.931,-4.929,4.931c-2.725,0,-4.931,-2.207,-4.931,-4.931L7.568,25.512z"/>
                  <path  opacity="0.2" fill="#FFFFFF" gorn="0.2.15.0.0.0.0.0.0.0.0.0.6.1" id="_x30_.1.15.0.0.0.6.1" enable-background="new    " d="M17.427,25.512c0,-2.725,-2.208,-4.93,-4.929,-4.93c-2.725,0,-4.931,2.205,-4.931,4.93l0,-0.233c0,-2.724,2.206,-4.931,4.931,-4.931c2.724,0,4.929,2.207,4.929,4.931L17.427,25.512z"/>
                 </g>
                 <g transform="matrix(-2.54711e-06, -1, 1, -2.54711e-06, -14.7248, 21.5506)">
                  <g >
                   <g >
                    <g >
                     <g  gorn="0.2.15.0.0.0.0.0.0.0.0.0.7.0.0.0" id="_x30_.1.15.0.0.0.7">
                      <rect  width="6.248" x="0.291" opacity="0.2" y="17.954" fill="#FFFFFF" gorn="0.2.15.0.0.0.0.0.0.0.0.0.7.0.0.0.0" height="0.371" id="_x30_.1.15.0.0.0.7.0" enable-background="new    "/>
                     </g>
                    </g>
                   </g>
                  </g>
                 </g>
                 <g transform="matrix(-2.54711e-06, -1, 1, -2.54711e-06, -29.2355, 36.0623)">
                  <g >
                   <g >
                    <g >
                     <g  gorn="0.2.15.0.0.0.0.0.0.0.0.0.8.0.0.0" id="_x30_.1.15.0.0.0.8">
                      <rect  width="6.244" x="0.293" opacity="0.2" y="32.465" fill="#FFFFFF" gorn="0.2.15.0.0.0.0.0.0.0.0.0.8.0.0.0.0" height="0.371" id="_x30_.1.15.0.0.0.8.0" enable-background="new    "/>
                     </g>
                    </g>
                   </g>
                  </g>
                 </g>
                 <g transform="matrix(-2.54711e-06, -1, 1, -2.54711e-06, -21.6146, 29.1724)">
                  <g >
                   <g >
                    <g >
                     <g  gorn="0.2.15.0.0.0.0.0.0.0.0.0.9.0.0.0" id="_x30_.1.15.0.0.0.9">
                      <rect  width="8.266" x="-0.352" opacity="0.2" y="25.212" fill="#FFFFFF" gorn="0.2.15.0.0.0.0.0.0.0.0.0.9.0.0.0.0" height="0.368" id="_x30_.1.15.0.0.0.9.0" enable-background="new    "/>
                     </g>
                    </g>
                   </g>
                  </g>
                 </g>
                 <g transform="matrix(-2.54711e-06, -1, 1, -2.54711e-06, 3.4298, 39.7056)">
                  <g >
                   <g >
                    <g >
                     <g  gorn="0.2.15.0.0.0.0.0.0.0.0.0.10.0.0.0" id="_x30_.1.15.0.0.0.10">
                      <rect  width="6.248" x="18.446" opacity="0.2" y="17.957" gorn="0.2.15.0.0.0.0.0.0.0.0.0.10.0.0.0.0" height="0.368" id="_x30_.1.15.0.0.0.10.0" enable-background="new    "/>
                     </g>
                    </g>
                   </g>
                  </g>
                 </g>
                 <g transform="matrix(-2.54711e-06, -1, 1, -2.54711e-06, -11.0816, 54.2142)">
                  <g >
                   <g >
                    <g >
                     <g  gorn="0.2.15.0.0.0.0.0.0.0.0.0.11.0.0.0" id="_x30_.1.15.0.0.0.11">
                      <rect  width="6.244" x="18.446" opacity="0.2" y="32.465" gorn="0.2.15.0.0.0.0.0.0.0.0.0.11.0.0.0.0" height="0.369" id="_x30_.1.15.0.0.0.11.0" enable-background="new    "/>
                     </g>
                    </g>
                   </g>
                  </g>
                 </g>
                 <g transform="matrix(-2.54711e-06, -1, 1, -2.54711e-06, -4.1966, 46.5918)">
                  <g >
                   <g >
                    <g >
                     <g  gorn="0.2.15.0.0.0.0.0.0.0.0.0.12.0.0.0" id="_x30_.1.15.0.0.0.12">
                      <rect  width="8.267" x="17.066" opacity="0.2" y="25.212" gorn="0.2.15.0.0.0.0.0.0.0.0.0.12.0.0.0.0" height="0.369" id="_x30_.1.15.0.0.0.12.0" enable-background="new    "/>
                     </g>
                    </g>
                   </g>
                  </g>
                 </g>
                </g>
               </g>
              </g>
             </g>
            </g>
           </g>
           <g  gorn="0.2.15.0.0.0.0.1" id="_x30_.1.15.0.1">
            <rect  width="2.75" x="36.573" y="6.322" fill="#E6E6E6" gorn="0.2.15.0.0.0.0.1.0" height="2.251" id="_x30_.1.15.0.1.0"/>
            <rect  width="2.75" x="36.573" y="-5.929" fill="#E6E6E6" gorn="0.2.15.0.0.0.0.1.1" height="2.252" id="_x30_.1.15.0.1.1"/>
            <rect  width="2.75" x="13.198" y="-0.47" fill="#E6E6E6" gorn="0.2.15.0.0.0.0.1.2" height="3.417" id="_x30_.1.15.0.1.2"/>
            <rect  width="2.75" x="13.198" y="6.322" fill="#E6E6E6" gorn="0.2.15.0.0.0.0.1.3" height="2.251" id="_x30_.1.15.0.1.3"/>
            <rect  width="2.75" x="13.198" y="-5.929" fill="#E6E6E6" gorn="0.2.15.0.0.0.0.1.4" height="2.252" id="_x30_.1.15.0.1.4"/>
            <rect  width="0.334" x="13.198" opacity="0.2" y="-0.47" fill="#FFFFFF" gorn="0.2.15.0.0.0.0.1.5" height="3.417" id="_x30_.1.15.0.1.5" enable-background="new    "/>
            <rect  width="0.334" x="13.198" opacity="0.2" y="6.322" fill="#FFFFFF" gorn="0.2.15.0.0.0.0.1.6" height="2.251" id="_x30_.1.15.0.1.6" enable-background="new    "/>
            <rect  width="0.334" x="13.198" opacity="0.2" y="-5.929" fill="#FFFFFF" gorn="0.2.15.0.0.0.0.1.7" height="2.252" id="_x30_.1.15.0.1.7" enable-background="new    "/>
            <rect  width="0.104" x="39.263" opacity="0.2" y="6.303" gorn="0.2.15.0.0.0.0.1.8" height="2.251" id="_x30_.1.15.0.1.8" enable-background="new    "/>
            <rect  width="0.104" x="39.263" opacity="0.2" y="-5.948" gorn="0.2.15.0.0.0.0.1.9" height="2.252" id="_x30_.1.15.0.1.9" enable-background="new    "/>
            <rect  width="0.334" x="36.589" opacity="0.1" y="6.335" gorn="0.2.15.0.0.0.0.1.10" height="2.251" id="_x30_.1.15.0.1.10" enable-background="new    "/>
            <rect  width="0.334" x="36.589" opacity="0.1" y="-5.916" gorn="0.2.15.0.0.0.0.1.11" height="2.252" id="_x30_.1.15.0.1.11" enable-background="new    "/>
           </g>
          </g>
         </g>
        </g>
       </g>
      </g>
     </g>
     <g  gorn="0.2.16" id="_x30_.1.16">
      <title  id="0.1.16.0">text:RESET</title>
      <g transform="matrix(1, 0, 0, 1, 27.4678, 23.4009)">
       <g >
        <g >
         <g >
          <g  gorn="0.2.16.1.0.0.0" id="_x30_.1.16.1">
           <g transform="matrix(1, 0, 0, 1, -9.15527e-05, -6.10352e-05)">
            <g >
             <g >
              <g >
               <text  fill="#FFFFFF" font-family="'OCRA'" gorn="0.2.16.1.0.0.0.0.0.0.0" id="_x30_.1.16.1.0" font-size="4.176">RESET</text>
              </g>
             </g>
            </g>
           </g>
          </g>
         </g>
        </g>
       </g>
      </g>
     </g>
     <g transform="matrix(1, 0, 0, 1, 67.6403, 3.60123)">
      <g >
       <g >
        <g >
         <g  gorn="0.2.17.0.0.0" id="_x30_.1.17">
          <g  gorn="0.2.17.0.0.0.0" id="_x31_x10">
           <rect  width="72" x="-0.049" y="-0.001" fill="#404040" gorn="0.2.17.0.0.0.0.0" height="7.199" id="_x30_.1.17.0.0"/>
           <rect  width="2.779" x="2.162" y="2.208" gorn="0.2.17.0.0.0.0.1" height="2.782" id="_x30_.1.17.0.1"/>
           <polygon  fill="#2A2A29" points="1.137,1.183,2.16,2.208,4.943,2.208,5.969,1.183" gorn="0.2.17.0.0.0.0.2" id="_x30_.1.17.0.2"/>
           <polygon  fill="#474747" points="5.969,1.183,4.943,2.211,4.943,4.992,5.969,6.015" gorn="0.2.17.0.0.0.0.3" id="_x30_.1.17.0.3"/>
           <polygon  fill="#595959" points="5.969,6.015,4.943,4.992,2.16,4.992,1.137,6.015" gorn="0.2.17.0.0.0.0.4" id="_x30_.1.17.0.4"/>
           <polygon  fill="#373737" points="1.135,6.015,2.16,4.99,2.16,2.208,1.135,1.183" gorn="0.2.17.0.0.0.0.5" id="_x30_.1.17.0.5"/>
           <rect  width="2.781" x="9.363" y="2.208" gorn="0.2.17.0.0.0.0.6" height="2.782" id="_x30_.1.17.0.6"/>
           <polygon  fill="#2A2A29" points="8.336,1.183,9.359,2.208,12.142,2.208,13.168,1.183" gorn="0.2.17.0.0.0.0.7" id="_x30_.1.17.0.7"/>
           <polygon  fill="#474747" points="13.168,1.183,12.142,2.211,12.142,4.992,13.168,6.015" gorn="0.2.17.0.0.0.0.8" id="_x30_.1.17.0.8"/>
           <polygon  fill="#595959" points="13.168,6.015,12.14,4.992,9.359,4.992,8.336,6.015" gorn="0.2.17.0.0.0.0.9" id="_x30_.1.17.0.9"/>
           <polygon  fill="#373737" points="8.334,6.015,9.359,4.99,9.359,2.208,8.334,1.183" gorn="0.2.17.0.0.0.0.10" id="_x30_.1.17.0.10"/>
           <rect  width="2.779" x="16.562" y="2.208" gorn="0.2.17.0.0.0.0.11" height="2.782" id="_x30_.1.17.0.11"/>
           <polygon  fill="#2A2A29" points="15.535,1.183,16.558,2.208,19.344,2.208,20.369,1.183" gorn="0.2.17.0.0.0.0.12" id="_x30_.1.17.0.12"/>
           <polygon  fill="#474747" points="20.369,1.183,19.344,2.211,19.344,4.992,20.369,6.015" gorn="0.2.17.0.0.0.0.13" id="_x30_.1.17.0.13"/>
           <polygon  fill="#595959" points="20.367,6.015,19.344,4.992,16.558,4.992,15.535,6.015" gorn="0.2.17.0.0.0.0.14" id="_x30_.1.17.0.14"/>
           <polygon  fill="#373737" points="15.535,6.015,16.558,4.99,16.558,2.208,15.535,1.183" gorn="0.2.17.0.0.0.0.15" id="_x30_.1.17.0.15"/>
           <rect  width="2.781" x="23.763" y="2.208" gorn="0.2.17.0.0.0.0.16" height="2.782" id="_x30_.1.17.0.16"/>
           <polygon  fill="#2A2A29" points="22.736,1.183,23.762,2.208,26.545,2.208,27.568,1.183" gorn="0.2.17.0.0.0.0.17" id="_x30_.1.17.0.17"/>
           <polygon  fill="#474747" points="27.568,1.183,26.545,2.211,26.545,4.992,27.568,6.015" gorn="0.2.17.0.0.0.0.18" id="_x30_.1.17.0.18"/>
           <polygon  fill="#595959" points="27.568,6.015,26.543,4.992,23.762,4.992,22.736,6.015" gorn="0.2.17.0.0.0.0.19" id="_x30_.1.17.0.19"/>
           <polygon  fill="#373737" points="22.734,6.015,23.762,4.99,23.762,2.208,22.734,1.183" gorn="0.2.17.0.0.0.0.20" id="_x30_.1.17.0.20"/>
           <rect  width="2.779" x="30.963" y="2.208" gorn="0.2.17.0.0.0.0.21" height="2.782" id="_x30_.1.17.0.21"/>
           <polygon  fill="#2A2A29" points="29.935,1.183,30.961,2.208,33.744,2.208,34.767,1.183" gorn="0.2.17.0.0.0.0.22" id="_x30_.1.17.0.22"/>
           <polygon  fill="#474747" points="34.767,1.183,33.744,2.211,33.744,4.992,34.767,6.015" gorn="0.2.17.0.0.0.0.23" id="_x30_.1.17.0.23"/>
           <polygon  fill="#595959" points="34.765,6.015,33.742,4.992,30.961,4.992,29.935,6.015" gorn="0.2.17.0.0.0.0.24" id="_x30_.1.17.0.24"/>
           <polygon  fill="#373737" points="29.933,6.015,30.961,4.99,30.961,2.208,29.933,1.183" gorn="0.2.17.0.0.0.0.25" id="_x30_.1.17.0.25"/>
           <rect  width="2.779" x="38.164" y="2.208" gorn="0.2.17.0.0.0.0.26" height="2.782" id="_x30_.1.17.0.26"/>
           <polygon  fill="#2A2A29" points="37.137,1.183,38.16,2.208,40.943,2.208,41.97,1.183" gorn="0.2.17.0.0.0.0.27" id="_x30_.1.17.0.27"/>
           <polygon  fill="#474747" points="41.97,1.183,40.943,2.211,40.943,4.992,41.97,6.015" gorn="0.2.17.0.0.0.0.28" id="_x30_.1.17.0.28"/>
           <polygon  fill="#595959" points="41.97,6.015,40.94,4.992,38.16,4.992,37.137,6.015" gorn="0.2.17.0.0.0.0.29" id="_x30_.1.17.0.29"/>
           <polygon  fill="#373737" points="37.135,6.015,38.16,4.99,38.16,2.208,37.135,1.183" gorn="0.2.17.0.0.0.0.30" id="_x30_.1.17.0.30"/>
           <rect  width="2.78" x="45.361" y="2.208" gorn="0.2.17.0.0.0.0.31" height="2.782" id="_x30_.1.17.0.31"/>
           <polygon  fill="#2A2A29" points="44.339,1.183,45.359,2.208,48.141,2.208,49.17,1.183" gorn="0.2.17.0.0.0.0.32" id="_x30_.1.17.0.32"/>
           <polygon  fill="#474747" points="49.17,1.183,48.141,2.211,48.141,4.992,49.17,6.015" gorn="0.2.17.0.0.0.0.33" id="_x30_.1.17.0.33"/>
           <polygon  fill="#595959" points="49.168,6.015,48.139,4.992,45.359,4.992,44.339,6.015" gorn="0.2.17.0.0.0.0.34" id="_x30_.1.17.0.34"/>
           <polygon  fill="#373737" points="44.336,6.015,45.359,4.99,45.359,2.208,44.336,1.183" gorn="0.2.17.0.0.0.0.35" id="_x30_.1.17.0.35"/>
           <rect  width="2.779" x="52.561" y="2.208" gorn="0.2.17.0.0.0.0.36" height="2.782" id="_x30_.1.17.0.36"/>
           <polygon  fill="#2A2A29" points="51.535,1.183,52.557,2.208,55.345,2.208,56.367,1.183" gorn="0.2.17.0.0.0.0.37" id="_x30_.1.17.0.37"/>
           <polygon  fill="#474747" points="56.367,1.183,55.345,2.211,55.345,4.992,56.367,6.015" gorn="0.2.17.0.0.0.0.38" id="_x30_.1.17.0.38"/>
           <polygon  fill="#595959" points="56.367,6.015,55.345,4.992,52.557,4.992,51.535,6.015" gorn="0.2.17.0.0.0.0.39" id="_x30_.1.17.0.39"/>
           <polygon  fill="#373737" points="51.533,6.015,52.557,4.99,52.557,2.208,51.533,1.183" gorn="0.2.17.0.0.0.0.40" id="_x30_.1.17.0.40"/>
           <rect  width="2.78" x="59.762" y="2.208" gorn="0.2.17.0.0.0.0.41" height="2.782" id="_x30_.1.17.0.41"/>
           <polygon  fill="#2A2A29" points="58.736,1.183,59.762,2.208,62.546,2.208,63.568,1.183" gorn="0.2.17.0.0.0.0.42" id="_x30_.1.17.0.42"/>
           <polygon  fill="#474747" points="63.568,1.183,62.546,2.211,62.546,4.992,63.568,6.015" gorn="0.2.17.0.0.0.0.43" id="_x30_.1.17.0.43"/>
           <polygon  fill="#595959" points="63.565,6.015,62.543,4.992,59.762,4.992,58.736,6.015" gorn="0.2.17.0.0.0.0.44" id="_x30_.1.17.0.44"/>
           <polygon  fill="#373737" points="58.734,6.015,59.762,4.99,59.762,2.208,58.734,1.183" gorn="0.2.17.0.0.0.0.45" id="_x30_.1.17.0.45"/>
           <rect  width="2.778" x="66.964" y="2.208" gorn="0.2.17.0.0.0.0.46" height="2.782" id="_x30_.1.17.0.46"/>
           <polygon  fill="#2A2A29" points="65.934,1.183,66.961,2.208,69.742,2.208,70.766,1.183" gorn="0.2.17.0.0.0.0.47" id="_x30_.1.17.0.47"/>
           <polygon  fill="#474747" points="70.766,1.183,69.742,2.211,69.742,4.992,70.766,6.015" gorn="0.2.17.0.0.0.0.48" id="_x30_.1.17.0.48"/>
           <polygon  fill="#595959" points="70.764,6.015,69.742,4.992,66.961,4.992,65.934,6.015" gorn="0.2.17.0.0.0.0.49" id="_x30_.1.17.0.49"/>
           <polygon  fill="#373737" points="65.932,6.015,66.961,4.99,66.961,2.208,65.932,1.183" gorn="0.2.17.0.0.0.0.50" id="_x30_.1.17.0.50"/>
          </g>
         </g>
        </g>
       </g>
      </g>
     </g>
    </g>
    </g></g></g><g partID='56270'><g transform='translate(154.633,30.6533)' ><g transform='matrix(0,1,-1,0,0,0)'  ><g  id="breadboard">
     <g  id="icon">
      <path  fill="#0F7391" d="M202.627,144l7.201,-7.201L209.828,43.2l-7.201,-7.2L202.627,3.6l-3.6,-3.6L18.263,0c-1.565,0,-2.834,1.269,-2.834,2.835l0,145.531c0,1.564,1.269,2.834,2.834,2.834l0,0l181.53,0c1.564,0,2.834,-1.269,2.834,-2.834l0,0L202.627,144M29.452,26.28c0,-2.544,2.062,-4.606,4.606,-4.606s4.606,2.063,4.606,4.606c0,2.543,-2.063,4.605,-4.606,4.605S29.452,28.824,29.452,26.28L29.452,26.28zM29.452,58.68c0,-2.544,2.062,-4.606,4.606,-4.606s4.606,2.063,4.606,4.606s-2.063,4.606,-4.606,4.606S29.452,61.224,29.452,58.68zM198.092,50.4c-0.004,-2.505,2.023,-4.539,4.527,-4.543c2.506,-0.004,4.539,2.022,4.545,4.527c0,0.005,0,0.011,0,0.016c0.004,2.505,-2.022,4.539,-4.528,4.543c-2.505,0.004,-4.539,-2.023,-4.544,-4.528C198.092,50.411,198.092,50.405,198.092,50.4zM198.092,129.6c-0.004,-2.505,2.023,-4.539,4.527,-4.543c2.506,-0.004,4.539,2.021,4.545,4.527c0,0.006,0,0.01,0,0.016c0.004,2.505,-2.022,4.539,-4.528,4.543c-2.505,0.004,-4.539,-2.021,-4.544,-4.527C198.092,129.61,198.092,129.606,198.092,129.6zM54.093,7.56c-0.004,-2.505,2.024,-4.539,4.529,-4.542c2.505,-0.004,4.538,2.024,4.542,4.529c0,0.004,0,0.009,0,0.013c0.003,2.505,-2.024,4.539,-4.529,4.542c-2.505,0.004,-4.539,-2.024,-4.542,-4.529C54.093,7.569,54.093,7.564,54.093,7.56zM50.493,144c-0.004,-2.506,2.024,-4.539,4.529,-4.543s4.538,2.023,4.542,4.528c0,0.005,0,0.009,0,0.015c0.003,2.504,-2.024,4.537,-4.529,4.541c-2.505,0.004,-4.539,-2.023,-4.542,-4.528C50.493,144.008,50.493,144.004,50.493,144zM194.708,64.8c0,-0.795,0.646,-1.44,1.439,-1.44c0.796,0,1.439,0.645,1.439,1.44l0,0c0,0.795,-0.645,1.44,-1.439,1.44C195.353,66.24,194.708,65.595,194.708,64.8zM201.909,64.8c0,-0.795,0.646,-1.44,1.44,-1.44s1.438,0.645,1.438,1.44l0,0c0,0.795,-0.645,1.44,-1.438,1.44C202.553,66.24,201.909,65.595,201.909,64.8zM194.708,72c0,-0.795,0.646,-1.44,1.439,-1.44c0.796,0,1.439,0.645,1.439,1.44s-0.645,1.44,-1.439,1.44C195.353,73.44,194.708,72.795,194.708,72zM201.909,72c0,-0.795,0.646,-1.44,1.44,-1.44s1.438,0.645,1.438,1.44s-0.645,1.44,-1.438,1.44C202.553,73.44,201.909,72.795,201.909,72zM194.708,79.2c0,-0.795,0.646,-1.439,1.439,-1.439c0.796,0,1.439,0.646,1.439,1.439c0,0.795,-0.645,1.44,-1.439,1.44C195.353,80.64,194.708,79.995,194.708,79.2zM201.909,79.2c0,-0.795,0.646,-1.439,1.44,-1.439s1.438,0.646,1.438,1.439c0,0.795,-0.645,1.44,-1.438,1.44C202.553,80.64,201.909,79.995,201.909,79.2zM132.068,7.2c0,-0.795,0.646,-1.44,1.44,-1.44c0.796,0,1.439,0.646,1.439,1.44s-0.645,1.44,-1.439,1.44S132.068,7.995,132.068,7.2zM124.87,7.2c-0.002,-0.795,0.643,-1.441,1.438,-1.442s1.441,0.643,1.441,1.438c0,0.001,0,0.002,0,0.004c0.002,0.795,-0.643,1.441,-1.438,1.442s-1.439,-0.643,-1.441,-1.438C124.87,7.203,124.87,7.201,124.87,7.2zM117.668,7.2c-0.002,-0.795,0.643,-1.441,1.438,-1.442s1.439,0.643,1.441,1.438c0,0.001,0,0.002,0,0.004c0.002,0.795,-0.644,1.441,-1.438,1.442s-1.44,-0.642,-1.44,-1.438C117.668,7.203,117.668,7.201,117.668,7.2zM110.467,7.2c0,-0.795,0.644,-1.441,1.439,-1.442c0.795,-0.001,1.44,0.643,1.442,1.438c0,0.001,0,0.002,0,0.004c0,0.795,-0.644,1.441,-1.438,1.442s-1.439,-0.643,-1.441,-1.438C110.467,7.203,110.467,7.201,110.467,7.2zM103.269,7.2c-0.001,-0.795,0.643,-1.441,1.438,-1.442c0.795,-0.001,1.44,0.643,1.442,1.438c0,0.001,0,0.002,0,0.004c0,0.795,-0.643,1.441,-1.438,1.442c-0.795,0.001,-1.441,-0.643,-1.442,-1.438C103.269,7.203,103.269,7.201,103.269,7.2zM96.068,7.2c-0.001,-0.795,0.643,-1.441,1.438,-1.442s1.441,0.643,1.442,1.438c0,0.001,0,0.002,0,0.004c0.001,0.795,-0.643,1.441,-1.438,1.442C96.715,8.643,96.069,8,96.068,7.204C96.068,7.203,96.068,7.201,96.068,7.2zM88.869,7.2c-0.001,-0.795,0.643,-1.441,1.438,-1.442s1.441,0.643,1.442,1.438c0,0.001,0,0.002,0,0.004c0.001,0.795,-0.643,1.441,-1.438,1.442S88.87,8,88.869,7.204C88.869,7.203,88.869,7.201,88.869,7.2zM81.668,7.2c-0.001,-0.795,0.643,-1.441,1.438,-1.442s1.441,0.643,1.442,1.438c0,0.001,0,0.002,0,0.004c0.001,0.795,-0.643,1.441,-1.438,1.442S81.669,8,81.668,7.204C81.668,7.203,81.668,7.201,81.668,7.2zM74.408,7.201c-0.001,-0.795,0.643,-1.441,1.438,-1.442c0.795,-0.001,1.441,0.643,1.442,1.438c0,0.001,0,0.002,0,0.004c0.001,0.795,-0.643,1.441,-1.438,1.442S74.409,8,74.408,7.205C74.408,7.203,74.408,7.202,74.408,7.201zM67.219,7.2c-0.001,-0.795,0.643,-1.441,1.438,-1.442c0.795,-0.001,1.441,0.643,1.442,1.438c0,0.001,0,0.002,0,0.004c0.001,0.795,-0.643,1.441,-1.438,1.442S67.22,8,67.219,7.204C67.219,7.203,67.219,7.201,67.219,7.2zM157.988,144c0,-0.797,0.646,-1.44,1.441,-1.44c0.795,0,1.438,0.646,1.438,1.44s-0.645,1.438,-1.438,1.438C158.633,145.44,157.988,144.795,157.988,144zM165.189,144c0,-0.797,0.646,-1.44,1.438,-1.44c0.795,0,1.439,0.646,1.439,1.44s-0.645,1.438,-1.439,1.438C165.834,145.439,165.189,144.795,165.189,144zM172.388,144c0,-0.797,0.646,-1.44,1.44,-1.44s1.439,0.646,1.439,1.44s-0.646,1.438,-1.439,1.438C173.034,145.44,172.388,144.795,172.388,144zM179.588,144c0,-0.797,0.646,-1.44,1.439,-1.44s1.439,0.646,1.439,1.44s-0.646,1.438,-1.439,1.438S179.588,144.795,179.588,144zM186.79,144c0,-0.797,0.645,-1.44,1.438,-1.44c0.796,0,1.44,0.646,1.44,1.44s-0.646,1.438,-1.44,1.438C187.433,145.44,186.79,144.795,186.79,144zM193.988,144c0,-0.797,0.646,-1.44,1.441,-1.44c0.795,0,1.438,0.646,1.438,1.44s-0.645,1.438,-1.438,1.438C194.633,145.44,193.988,144.795,193.988,144zM193.988,7.2c0,-0.795,0.646,-1.44,1.441,-1.44c0.795,0,1.438,0.646,1.438,1.44s-0.645,1.44,-1.438,1.44C194.633,8.64,193.988,7.995,193.988,7.2zM186.79,7.2c0,-0.795,0.645,-1.44,1.438,-1.44c0.796,0,1.44,0.646,1.44,1.44s-0.646,1.44,-1.44,1.44S186.79,7.995,186.79,7.2zM179.588,7.2c0,-0.795,0.646,-1.44,1.439,-1.44s1.439,0.646,1.439,1.44s-0.646,1.44,-1.439,1.44S179.588,7.995,179.588,7.2zM172.388,7.2c0,-0.795,0.646,-1.44,1.44,-1.44s1.439,0.646,1.439,1.44s-0.646,1.44,-1.439,1.44C173.034,8.64,172.388,7.995,172.388,7.2zM165.189,7.2c0,-0.795,0.646,-1.44,1.438,-1.44c0.795,0,1.439,0.646,1.439,1.44s-0.645,1.44,-1.439,1.44C165.834,8.64,165.189,7.995,165.189,7.2zM157.988,7.2c0,-0.795,0.646,-1.44,1.441,-1.44c0.795,0,1.438,0.646,1.438,1.44s-0.645,1.44,-1.438,1.44C158.633,8.64,157.988,7.995,157.988,7.2zM150.79,7.2c0,-0.795,0.645,-1.44,1.438,-1.44c0.796,0,1.44,0.646,1.44,1.44s-0.646,1.44,-1.44,1.44S150.79,7.995,150.79,7.2zM143.588,7.2c0,-0.795,0.646,-1.44,1.439,-1.44s1.439,0.646,1.439,1.44s-0.646,1.44,-1.439,1.44S143.588,7.995,143.588,7.2zM107.588,144c-0.002,-0.797,0.643,-1.441,1.438,-1.442s1.439,0.644,1.441,1.438c0,0,0,0.002,0,0.004c0.002,0.795,-0.643,1.439,-1.438,1.44c-0.795,0.002,-1.44,-0.644,-1.442,-1.438C107.588,144.002,107.588,144,107.588,144zM114.79,144c-0.002,-0.797,0.643,-1.441,1.438,-1.442c0.796,-0.001,1.441,0.644,1.441,1.438c0,0,0,0.002,0,0.004c0.002,0.795,-0.643,1.439,-1.438,1.44c-0.795,0.002,-1.439,-0.644,-1.441,-1.438L114.79,144zM93.197,144c-0.001,-0.797,0.643,-1.441,1.438,-1.442c0.795,-0.001,1.44,0.644,1.441,1.438c0,0,0,0.002,0,0.004c0.002,0.795,-0.643,1.439,-1.438,1.44c-0.795,0.002,-1.441,-0.644,-1.442,-1.438C93.197,144.002,93.197,144,93.197,144zM100.397,144c-0.001,-0.797,0.643,-1.441,1.438,-1.442c0.796,-0.001,1.441,0.644,1.442,1.438c0,0,0,0.002,0,0.004c0.001,0.795,-0.643,1.439,-1.438,1.44c-0.795,0.002,-1.44,-0.644,-1.441,-1.438C100.397,144.002,100.397,144,100.397,144zM121.988,144c0,-0.797,0.644,-1.441,1.438,-1.442c0.796,-0.001,1.439,0.644,1.441,1.438c0,0,0,0.002,0,0.004c0.002,0.795,-0.643,1.439,-1.438,1.44c-0.797,0.002,-1.441,-0.644,-1.443,-1.438C121.988,144.002,121.988,144,121.988,144zM129.189,144c0,-0.797,0.646,-1.44,1.438,-1.44c0.795,0,1.439,0.646,1.439,1.44c0.002,0.795,-0.643,1.439,-1.438,1.44c-0.795,0.002,-1.441,-0.644,-1.441,-1.438C129.189,144.002,129.189,144,129.189,144zM136.388,144c0,-0.797,0.646,-1.44,1.44,-1.44s1.439,0.646,1.439,1.44s-0.646,1.438,-1.439,1.438C137.034,145.44,136.388,144.795,136.388,144zM143.588,144c0,-0.797,0.646,-1.44,1.439,-1.44s1.439,0.646,1.439,1.44s-0.646,1.438,-1.439,1.438S143.588,144.795,143.588,144z"/>
      <circle  fill="none" cx="196.148" cy="64.8" stroke="#9A916C" id="connector162pin" r="1.8" stroke-width="0.72"/>
      <circle  fill="none" cx="203.349" cy="64.8" stroke="#9A916C" id="connector163pin" r="1.8" stroke-width="0.72"/>
      <circle  fill="none" cx="196.148" cy="72" stroke="#9A916C" id="connector164pin" r="1.8" stroke-width="0.72"/>
      <circle  fill="none" cx="203.349" cy="72" stroke="#9A916C" id="connector165pin" r="1.8" stroke-width="0.72"/>
      <circle  fill="none" cx="196.148" cy="79.2" stroke="#9A916C" id="connector166pin" r="1.8" stroke-width="0.72"/>
      <circle  fill="none" cx="203.349" cy="79.2" stroke="#9A916C" id="connector167pin" r="1.8" stroke-width="0.72"/>
      <circle  fill="none" cx="133.508" cy="7.2" stroke="#9A916C" id="connector170pin" r="1.8" stroke-width="0.72"/>
      <circle  fill="none" cx="126.308" cy="7.2" stroke="#9A916C" id="connector171pin" r="1.8" stroke-width="0.72"/>
      <circle  fill="none" cx="119.109" cy="7.2" stroke="#9A916C" id="connector172pin" r="1.8" stroke-width="0.72"/>
      <circle  fill="none" cx="111.909" cy="7.2" stroke="#9A916C" id="connector173pin" r="1.8" stroke-width="0.72"/>
      <circle  fill="none" cx="104.708" cy="7.2" stroke="#9A916C" id="connector174pin" r="1.8" stroke-width="0.72"/>
      <circle  fill="none" cx="97.508" cy="7.2" stroke="#9A916C" id="connector175pin" r="1.8" stroke-width="0.72"/>
      <circle  fill="none" cx="90.309" cy="7.2" stroke="#9A916C" id="connector176pin" r="1.8" stroke-width="0.72"/>
      <circle  fill="none" cx="83.108" cy="7.2" stroke="#9A916C" id="connector177pin" r="1.8" stroke-width="0.72"/>
      <circle  fill="none" cx="75.85" cy="7.2" stroke="#9A916C" id="connector1760pin" r="1.8" stroke-width="0.72"/>
      <circle  fill="none" cx="68.649" cy="7.199" stroke="#9A916C" id="connector1770pin" r="1.8" stroke-width="0.72"/>
      <circle  fill="none" cx="159.429" cy="144" stroke="#9A916C" id="connector178pin" r="1.8" stroke-width="0.72"/>
      <circle  fill="none" cx="166.627" cy="144" stroke="#9A916C" id="connector179pin" r="1.8" stroke-width="0.72"/>
      <circle  fill="none" cx="173.829" cy="144" stroke="#9A916C" id="connector180pin" r="1.8" stroke-width="0.72"/>
      <circle  fill="none" cx="181.029" cy="144" stroke="#9A916C" id="connector181pin" r="1.8" stroke-width="0.72"/>
      <circle  fill="none" cx="188.228" cy="144" stroke="#9A916C" id="connector182pin" r="1.8" stroke-width="0.72"/>
      <circle  fill="none" cx="195.429" cy="144" stroke="#9A916C" id="connector183pin" r="1.8" stroke-width="0.72"/>
      <circle  fill="none" cx="195.429" cy="7.2" stroke="#9A916C" id="connector184pin" r="1.8" stroke-width="0.72"/>
      <circle  fill="none" cx="188.228" cy="7.2" stroke="#9A916C" id="connector185pin" r="1.8" stroke-width="0.72"/>
      <circle  fill="none" cx="181.029" cy="7.2" stroke="#9A916C" id="connector186pin" r="1.8" stroke-width="0.72"/>
      <circle  fill="none" cx="173.829" cy="7.2" stroke="#9A916C" id="connector187pin" r="1.8" stroke-width="0.72"/>
      <circle  fill="none" cx="166.627" cy="7.2" stroke="#9A916C" id="connector188pin" r="1.8" stroke-width="0.72"/>
      <circle  fill="none" cx="159.429" cy="7.2" stroke="#9A916C" id="connector189pin" r="1.8" stroke-width="0.72"/>
      <circle  fill="none" cx="152.228" cy="7.2" stroke="#9A916C" id="connector190pin" r="1.8" stroke-width="0.72"/>
      <circle  fill="none" cx="145.029" cy="7.2" stroke="#9A916C" id="connector191pin" r="1.8" stroke-width="0.72"/>
      <circle  fill="none" cx="109.029" cy="144" stroke="#9A916C" id="connector204pin" r="1.8" stroke-width="0.72"/>
      <circle  fill="none" cx="116.228" cy="144" stroke="#9A916C" id="connector205pin" r="1.8" stroke-width="0.72"/>
      <circle  fill="none" cx="94.629" cy="144" stroke="#9A916C" id="connector1831pin" r="1.8" stroke-width="0.72"/>
      <circle  fill="none" cx="101.834" cy="144" stroke="#9A916C" id="connector1830pin" r="1.8" stroke-width="0.72"/>
      <circle  fill="none" cx="123.429" cy="144" stroke="#9A916C" id="connector206pin" r="1.8" stroke-width="0.72"/>
      <circle  fill="none" cx="130.627" cy="144" stroke="#9A916C" id="connector207pin" r="1.8" stroke-width="0.72"/>
      <circle  fill="none" cx="137.829" cy="144" stroke="#9A916C" id="connector208pin" r="1.8" stroke-width="0.72"/>
      <circle  fill="none" cx="145.029" cy="144" stroke="#9A916C" id="connector209pin" r="1.8" stroke-width="0.72"/>
     </g>
     <g transform="matrix(1, 0, 0, 1, 13.7627, 64.5755)">
      <g  id="chipled_0805">
       <g transform="matrix(0, 1, -1, 0, 5.62951, 1.77951)">
        <g >
         <g transform="matrix(1, 0, 0, 1, 21.5539, 31.3385)">
          <g  id="led-0603_1_">
           <line  fill="none" y1="-38.465" x1="-22.535" y2="-31.229" x2="-22.535"/>
           <g transform="matrix(2.57889e-06, 1, -1, 2.57889e-06, -55.4115, -14.1708)">
            <rect  width="7.348" x="-24.294" y="-36.708" fill="#F2F2F2" height="3.833"/>
           </g>
           <path  fill="#22B573" fill-opacity="0.7" d="M-22.537,-33.717c0,0,0.467,0.645,0.426,0.867c-0.041,0.219,0.148,0.541,0,0.676l-0.424,-0.018L-22.537,-33.717z"/>
           <g >
            <g transform="matrix(2.57889e-06, 1, -1, 2.57889e-06, -55.9345, -13.7895)">
             <rect  width="0.854" x="-21.499" y="-34.886" fill="#B3B3B3" height="0.049"/>
            </g>
           </g>
           <g >
            <polygon  fill="#D1C690" points="-22.113,-33.138,-22.217,-32.174,-21.486,-32.174,-21.59,-33.138"/>
            <g >
             <path  fill="#D1C690" d="M-21.914,-33.077c0,-0.002,0,-0.004,0,-0.008c0.035,-0.266,0.104,-0.447,0.162,-0.598c0.08,-0.209,0.782,-0.559,0.696,-0.828c-0.012,-0.027,0.011,-0.06,0.043,-0.066c0.035,-0.008,0.068,0.01,0.078,0.039c0.095,0.305,-0.617,0.674,-0.701,0.893c-0.06,0.148,-0.123,0.318,-0.155,0.572c-0.004,0.029,-0.033,0.055,-0.068,0.049C-21.889,-33.026,-21.914,-33.049,-21.914,-33.077z"/>
            </g>
            <polygon  fill="#D1C690" points="-19.225,-36.558,-19.122,-37.523,-19.852,-37.523,-19.749,-36.558"/>
            <g >
             <path  fill="#D1C690" d="M-20.746,-34.904c0,-0.025,0.02,-0.049,0.047,-0.055c0.292,-0.063,1.152,-1.088,1.152,-1.885c0,-0.033,0.026,-0.057,0.063,-0.057c0.034,0.002,0.063,0.025,0.063,0.057l0,0.002c0,0.749,-0.77,1.891,-1.245,1.993c-0.035,0.008,-0.068,-0.012,-0.078,-0.041C-20.746,-34.896,-20.746,-34.899,-20.746,-34.904z"/>
            </g>
            <path  fill="#D1C690" d="M-20.762,-34.435c0,0,0.002,-0.356,-0.311,-0.383c0,0.07,0,0.383,0,0.383L-20.762,-34.435z"/>
            <path  fill="#D1C690" d="M-20.443,-34.87c0,0,-0.306,0.158,-0.351,0.053c-0.048,-0.107,-0.052,-0.178,0.028,-0.24C-20.682,-35.118,-20.443,-34.87,-20.443,-34.87z"/>
            <path  fill="#9D956C" d="M-21.111,-34.51c0.084,0.27,-0.618,0.619,-0.698,0.828c-0.06,0.145,-0.127,0.33,-0.162,0.598l0.059,0c0.035,-0.266,0.104,-0.447,0.162,-0.598c0.08,-0.209,0.782,-0.559,0.696,-0.828L-21.111,-34.51z"/>
            <polygon  fill="#9D956C" points="-19.804,-36.558,-19.907,-37.523,-19.852,-37.523,-19.749,-36.558"/>
            <path  fill="#9D956C" d="M-20.756,-34.961c0.291,-0.062,1.212,-1.07,1.149,-1.885l0.06,0c0.06,0.877,-0.86,1.826,-1.152,1.887L-20.756,-34.961z"/>
            <path  fill="#9D956C" d="M-21.129,-34.817c0,0.07,0,0.381,0,0.381l0.057,0c0,0,0,-0.311,0,-0.381L-21.129,-34.817z"/>
            <path  fill="#9D956C" d="M-20.818,-35.058c-0.08,0.063,-0.076,0.131,-0.031,0.238l0.06,0.002c-0.049,-0.107,-0.052,-0.179,0.028,-0.24L-20.818,-35.058z"/>
           </g>
           <path  opacity="0.5" fill="#F2F2F2" enable-background="new    " d="M-18.704,-37.506l-3.831,0l0,5.317l3.831,0.004L-18.704,-37.506z"/>
           <path  opacity="0.03" enable-background="new    " d="M-22.315,-32.329c-0.068,0,-0.138,0.012,-0.138,-0.098c0,-0.611,0,-4.667,0,-4.817c0,-0.168,0.065,-0.176,0.065,0.008c0,0.135,0.002,3.138,0.002,3.589C-22.385,-33.051,-22.315,-32.329,-22.315,-32.329z"/>
           <path  fill="#D1C690" d="M-22.537,-38.464l0,0.771l0.521,0c0.125,0,0.213,0.08,0.268,0.188l3.047,0l0,-1.01l-3.784,0l-0.05,0"/>
           <path  fill="#D1C690" d="M-22.537,-31.118l0.049,0l3.784,0l0,-1.072l-3.464,0c-0.056,0.105,-0.146,0.191,-0.271,0.191l-0.1,0l0,0.83"/>
          </g>
         </g>
        </g>
       </g>
      </g>
     </g>
     <g transform="matrix(1, 0, 0, 1, 81.2254, 125.824)">
      <g  id="panasonic_d">
       <g transform="matrix(0, 1, -1, 0, 19.39, -1.039)">
        <g >
         <g >
          <g transform="matrix(2.57889e-06, 1, -1, 2.57889e-06, 41.6216, 7.3195)">
           <rect  width="1.272" x="16.515" y="23.951" fill="#CCCCCC" height="1.039"/>
          </g>
          <g transform="matrix(2.57889e-06, 1, -1, 2.57889e-06, 22.234, 26.7082)">
           <rect  width="1.272" x="-2.873" y="23.953" fill="#CCCCCC" height="1.036"/>
          </g>
          <g transform="matrix(2.57889e-06, 1, -1, 2.57889e-06, 41.0857, 6.7837)">
           <rect  width="0.203" x="17.049" opacity="0.1" y="23.415" height="1.039" enable-background="new    "/>
          </g>
          <g transform="matrix(2.57889e-06, 1, -1, 2.57889e-06, 21.6976, 26.1718)">
           <rect  width="0.203" x="-2.339" opacity="0.1" y="23.417" height="1.036" enable-background="new    "/>
          </g>
          <path  fill="#1A1A1A" d="M2.09,33.674l13.156,0c0.76,0,1.385,-0.623,1.385,-1.383l0,-15.58c0,-0.764,-0.625,-1.387,-1.385,-1.387L2.09,15.324l-3.811,3.811l0,3.634l0,3.635l0,3.463L2.09,33.674z"/>
          <circle  fill="#E6E6E6" cx="7.458" cy="24.5" r="8.703"/>
          <path  fill="#333333" d="M2.09,33.674l13.156,0c0.76,0,1.385,-0.623,1.385,-1.383l0,-15.58c0,-0.764,-0.625,-1.387,-1.385,-1.387l-2.753,0L2.09,15.324l-3.811,3.811l0,3.634l0,3.635l0,3.463L2.09,33.674z"/>
          <path  d="M-1.719,19.319l3.81,-3.812l10.404,0l2.752,0c0.76,0,1.385,0.623,1.385,1.388L16.632,16.71c0,-0.764,-0.625,-1.387,-1.385,-1.387l-2.752,0L2.09,15.323l-3.811,3.811L-1.719,19.319L-1.719,19.319z"/>
          <path  fill="#E6E6E6" d="M7.458,15.675c1.879,0,3.614,0.604,5.037,1.614c2.215,1.579,3.664,4.163,3.664,7.088c0,2.928,-1.449,5.51,-3.664,7.087c-1.423,1.014,-3.158,1.615,-5.037,1.615c-4.807,0,-8.703,-3.896,-8.703,-8.703C-1.245,19.573,2.652,15.675,7.458,15.675z"/>
          <path  d="M16.159,24.5c0,-2.926,-1.449,-5.509,-3.664,-7.088l0,14.175C14.71,30.009,16.159,27.426,16.159,24.5z"/>
          <path  opacity="0.2" enable-background="new    " d="M12.495,17.641c-1.423,-1.013,-3.158,-1.615,-5.037,-1.615c-4.807,0,-8.703,3.897,-8.703,8.703L-1.245,24.5c0,-4.805,3.896,-8.703,8.703,-8.703c1.879,0,3.614,0.604,5.037,1.615L12.495,17.641z"/>
         </g>
        </g>
       </g>
      </g>
     </g>
     <g transform="matrix(1, 0, 0, 1, 59.6255, 125.824)">
      <g  id="panasonic_d_1_">
       <g transform="matrix(0, 1, -1, 0, 19.39, -1.039)">
        <g >
         <g >
          <g transform="matrix(2.57889e-06, 1, -1, 2.57889e-06, -22.0966, 27.9528)">
           <rect  width="1.272" x="-25.661" y="2.409" fill="#CCCCCC" height="1.039"/>
          </g>
          <g transform="matrix(2.57889e-06, 1, -1, 2.57889e-06, -2.7082, 8.5639)">
           <rect  width="1.272" x="-6.272" y="2.41" fill="#CCCCCC" height="1.035"/>
          </g>
          <g transform="matrix(2.57889e-06, 1, -1, 2.57889e-06, -21.5607, 28.4887)">
           <rect  width="0.203" x="-25.126" opacity="0.1" y="2.944" height="1.039" enable-background="new    "/>
          </g>
          <g transform="matrix(2.57889e-06, 1, -1, 2.57889e-06, -2.1728, 9.1003)">
           <rect  width="0.203" x="-5.738" opacity="0.1" y="2.946" height="1.036" enable-background="new    "/>
          </g>
          <path  fill="#1A1A1A" d="M-9.964,-6.276L-23.12,-6.276c-0.76,0,-1.385,0.623,-1.385,1.383l0,15.58c0,0.764,0.625,1.387,1.385,1.387l13.156,0l3.811,-3.811L-6.153,4.63L-6.153,0.995l0,-3.463L-9.964,-6.276z"/>
          <circle  fill="#E6E6E6" cx="-15.331" cy="2.899" r="8.703"/>
          <path  fill="#333333" d="M-9.964,-6.276L-23.12,-6.276c-0.76,0,-1.385,0.623,-1.385,1.383l0,15.58c0,0.764,0.625,1.387,1.385,1.387l2.752,0l10.404,0l3.811,-3.811L-6.153,4.63L-6.153,0.995l0,-3.463L-9.964,-6.276z"/>
          <path  d="M-6.156,8.08l-3.81,3.811l-10.403,0l-2.752,0c-0.761,0,-1.386,-0.623,-1.386,-1.387l0,0.184c0,0.764,0.625,1.387,1.386,1.387l2.752,0l10.403,0l3.81,-3.811L-6.156,8.08z"/>
          <path  fill="#E6E6E6" d="M-15.331,11.723c-1.879,0,-3.613,-0.604,-5.037,-1.614c-2.215,-1.579,-3.664,-4.163,-3.664,-7.088c0,-2.927,1.449,-5.509,3.664,-7.087c1.424,-1.013,3.158,-1.615,5.037,-1.615c4.808,0,8.703,3.896,8.703,8.703C-6.628,7.826,-10.527,11.723,-15.331,11.723z"/>
          <path  d="M-24.033,2.899c0,2.926,1.449,5.509,3.664,7.088L-20.369,-4.188C-22.583,-2.611,-24.033,-0.028,-24.033,2.899z"/>
          <path  opacity="0.2" enable-background="new    " d="M-20.368,9.758c1.424,1.012,3.158,1.615,5.037,1.615c4.808,0,8.703,-3.898,8.703,-8.703l0,0.229c0,4.805,-3.896,8.703,-8.703,8.703c-1.879,0,-3.613,-0.604,-5.037,-1.615L-20.368,9.758z"/>
         </g>
        </g>
       </g>
      </g>
     </g>
     <g transform="matrix(1, 0, 0, 1, 115.785, 109.624)">
      <g  id="panasonic_d_2_">
       <g transform="matrix(-1, 0, 0, -1, 20.429, 18.351)">
        <g >
         <g >
          <rect  width="1.039" x="-2.531" y="11.031" fill="#CCCCCC" height="1.271"/>
          <rect  width="1.036" x="16.86" y="11.031" fill="#CCCCCC" height="1.271"/>
          <rect  width="1.039" x="-2.531" opacity="0.1" y="12.101" height="0.201" enable-background="new    "/>
          <rect  width="1.036" x="16.86" opacity="0.1" y="12.101" height="0.201" enable-background="new    "/>
          <path  fill="#1A1A1A" d="M13.049,2.463L-0.106,2.463c-0.761,0,-1.386,0.623,-1.386,1.383l0,15.58c0,0.764,0.625,1.387,1.386,1.387l13.155,0l3.811,-3.811l0,-3.633L16.86,9.734L16.86,6.271L13.049,2.463z"/>
          <circle  fill="#E6E6E6" cx="7.682" cy="11.639" r="8.703"/>
          <path  fill="#333333" d="M13.049,2.463L-0.106,2.463c-0.761,0,-1.386,0.623,-1.386,1.383l0,15.58c0,0.764,0.625,1.387,1.386,1.387l2.752,0l10.403,0l3.811,-3.811l0,-3.633L16.86,9.734L16.86,6.271L13.049,2.463z"/>
          <path  d="M16.86,16.818l-3.811,3.812L2.646,20.63l-2.752,0c-0.761,0,-1.386,-0.622,-1.386,-1.388l0,0.186c0,0.764,0.625,1.387,1.386,1.387l2.752,0l10.403,0l3.811,-3.812L16.86,16.818z"/>
          <path  fill="#E6E6E6" d="M7.682,20.462c-1.879,0,-3.613,-0.604,-5.036,-1.614c-2.216,-1.578,-3.664,-4.162,-3.664,-7.088c0,-2.927,1.448,-5.509,3.664,-7.086C4.069,3.66,5.803,3.058,7.682,3.058c4.808,0,8.703,3.896,8.703,8.701C16.385,16.564,12.489,20.462,7.682,20.462z"/>
          <path  d="M-1.018,11.639c0,2.926,1.448,5.508,3.664,7.088L2.646,4.551C0.43,6.128,-1.018,8.711,-1.018,11.639z"/>
          <path  opacity="0.2" enable-background="new    " d="M2.646,18.497c1.423,1.013,3.157,1.614,5.036,1.614c4.808,0,8.703,-3.897,8.703,-8.703l0,0.229c0,4.807,-3.896,8.703,-8.703,8.703c-1.879,0,-3.613,-0.604,-5.036,-1.613L2.646,18.497z"/>
         </g>
        </g>
       </g>
      </g>
     </g>
     <g transform="matrix(1, 0, 0, 1, 208.744, 13.8259)">
      <g  id="chipled_0805_1_">
       <g transform="matrix(0, -1, 1, 0, -1.77951, 5.62951)">
        <g >
         <g transform="matrix(1, 0, 0, 1, 21.5539, 31.3385)">
          <g  id="led-0603_2_">
           <line  fill="none" y1="-162.422" x1="-48.398" y2="-157.81" x2="-48.398"/>
           <g transform="matrix(-2.54711e-06, -1, 1, -2.54711e-06, 112.904, -207.259)">
            <rect  width="4.683" x="-49.519" y="-161.302" fill="#F2F2F2" height="2.443"/>
           </g>
           <path  fill="#22B573" fill-opacity="0.7" d="M-48.399,-159.396c0,0,0.297,0.411,0.271,0.553c-0.026,0.14,0.094,0.345,0,0.431l-0.271,-0.011L-48.399,-159.396z"/>
           <g >
            <g transform="matrix(-2.54711e-06, -1, 1, -2.54711e-06, 112.66, -207.593)">
             <rect  width="0.544" x="-47.738" y="-160.142" fill="#B3B3B3" height="0.031"/>
            </g>
           </g>
           <g >
            <polygon  fill="#D1C690" points="-48.129,-159.027,-48.195,-158.413,-47.729,-158.413,-47.795,-159.027"/>
            <g >
             <path  fill="#D1C690" d="M-48.002,-158.988c0,-0.001,0,-0.002,0,-0.005c0.022,-0.169,0.066,-0.285,0.103,-0.381c0.051,-0.133,0.499,-0.356,0.444,-0.528c-0.008,-0.017,0.007,-0.039,0.027,-0.042c0.022,-0.005,0.043,0.006,0.05,0.025c0.061,0.194,-0.394,0.429,-0.447,0.569c-0.039,0.094,-0.079,0.202,-0.099,0.364c-0.003,0.019,-0.021,0.035,-0.044,0.031C-47.986,-158.955,-48.002,-158.97,-48.002,-158.988z"/>
            </g>
            <polygon  fill="#D1C690" points="-46.288,-161.206,-46.223,-161.822,-46.688,-161.822,-46.622,-161.206"/>
            <g >
             <path  fill="#D1C690" d="M-47.257,-160.153c0,-0.016,0.013,-0.031,0.03,-0.035c0.186,-0.04,0.734,-0.693,0.734,-1.201c0,-0.021,0.017,-0.036,0.04,-0.036c0.022,0.001,0.041,0.016,0.041,0.036l0,0.001c0,0.478,-0.491,1.205,-0.793,1.271c-0.022,0.005,-0.043,-0.008,-0.05,-0.026C-47.257,-160.147,-47.257,-160.149,-47.257,-160.153z"/>
            </g>
            <path  fill="#D1C690" d="M-47.267,-159.853c0,0,0.001,-0.227,-0.198,-0.244c0,0.045,0,0.244,0,0.244L-47.267,-159.853z"/>
            <path  fill="#D1C690" d="M-47.064,-160.131c0,0,-0.195,0.101,-0.224,0.034c-0.03,-0.068,-0.033,-0.113,0.018,-0.152C-47.217,-160.289,-47.064,-160.131,-47.064,-160.131z"/>
            <path  fill="#9D956C" d="M-47.49,-159.902c0.053,0.172,-0.394,0.395,-0.445,0.528c-0.038,0.092,-0.081,0.21,-0.103,0.381L-48,-158.993c0.022,-0.169,0.066,-0.285,0.103,-0.381c0.051,-0.133,0.499,-0.356,0.443,-0.528L-47.49,-159.902z"/>
            <polygon  fill="#9D956C" points="-46.657,-161.206,-46.723,-161.822,-46.688,-161.822,-46.622,-161.206"/>
            <path  fill="#9D956C" d="M-47.264,-160.189c0.186,-0.04,0.772,-0.682,0.732,-1.201l0.038,0c0.039,0.559,-0.548,1.164,-0.734,1.203L-47.264,-160.189z"/>
            <path  fill="#9D956C" d="M-47.502,-160.097c0,0.045,0,0.243,0,0.243l0.037,0c0,0,0,-0.198,0,-0.243L-47.502,-160.097z"/>
            <path  fill="#9D956C" d="M-47.304,-160.25c-0.051,0.04,-0.048,0.083,-0.02,0.152l0.039,0.001c-0.032,-0.068,-0.034,-0.115,0.018,-0.153L-47.304,-160.25z"/>
           </g>
           <path  opacity="0.5" fill="#F2F2F2" enable-background="new    " d="M-45.956,-161.811l-2.442,0l0,3.388l2.442,0.003L-45.956,-161.811z"/>
           <path  opacity="0.03" enable-background="new    " d="M-48.258,-158.511c-0.043,0,-0.087,0.007,-0.087,-0.063c0,-0.39,0,-2.974,0,-3.069c0,-0.107,0.041,-0.113,0.041,0.005c0,0.086,0.001,2,0.001,2.287C-48.302,-158.971,-48.258,-158.511,-48.258,-158.511z"/>
           <path  fill="#D1C690" d="M-48.399,-162.422l0,0.491l0.332,0c0.08,0,0.136,0.051,0.171,0.12l1.942,0l0,-0.644l-2.412,0l-0.032,0"/>
           <path  fill="#D1C690" d="M-48.399,-157.74l0.031,0l2.412,0l0,-0.683l-2.208,0c-0.036,0.067,-0.093,0.122,-0.173,0.122L-48.4,-158.301l0,0.529"/>
          </g>
         </g>
        </g>
       </g>
      </g>
     </g>
     <g transform="matrix(1, 0, 0, 1, 208.744, 13.8259)">
      <g  id="chipled_0805_7_">
       <g transform="matrix(0, -1, 1, 0, -1.77951, 5.62951)">
        <g >
         <g transform="matrix(1, 0, 0, 1, 21.5539, 31.3385)">
          <g  id="led-0603_8_">
           <line  fill="none" y1="-162.422" x1="-53.504" y2="-157.81" x2="-53.504"/>
           <g transform="matrix(-2.54711e-06, -1, 1, -2.54711e-06, 107.798, -212.366)">
            <rect  width="4.683" x="-54.625" y="-161.303" fill="#F2F2F2" height="2.443"/>
           </g>
           <path  fill="#22B573" fill-opacity="0.7" d="M-53.505,-159.396c0,0,0.297,0.411,0.271,0.553c-0.026,0.14,0.094,0.345,0,0.431l-0.271,-0.011L-53.505,-159.396z"/>
           <g >
            <g transform="matrix(-2.54711e-06, -1, 1, -2.54711e-06, 107.553, -212.7)">
             <rect  width="0.544" x="-52.845" y="-160.142" fill="#B3B3B3" height="0.031"/>
            </g>
           </g>
           <g >
            <polygon  fill="#D1C690" points="-53.235,-159.027,-53.302,-158.413,-52.836,-158.413,-52.902,-159.027"/>
            <g >
             <path  fill="#D1C690" d="M-53.108,-158.988c0,-0.001,0,-0.002,0,-0.005c0.022,-0.169,0.066,-0.285,0.103,-0.381c0.051,-0.133,0.499,-0.356,0.444,-0.528c-0.008,-0.017,0.007,-0.039,0.027,-0.042c0.022,-0.005,0.043,0.006,0.05,0.025c0.061,0.194,-0.394,0.429,-0.447,0.569c-0.039,0.094,-0.079,0.202,-0.099,0.364c-0.003,0.019,-0.021,0.035,-0.044,0.031C-53.092,-158.955,-53.108,-158.97,-53.108,-158.988z"/>
            </g>
            <polygon  fill="#D1C690" points="-51.394,-161.206,-51.329,-161.822,-51.794,-161.822,-51.728,-161.206"/>
            <g >
             <path  fill="#D1C690" d="M-52.364,-160.153c0,-0.016,0.013,-0.031,0.03,-0.035c0.186,-0.04,0.734,-0.693,0.734,-1.201c0,-0.021,0.017,-0.036,0.04,-0.036c0.022,0.001,0.041,0.016,0.041,0.036l0,0.001c0,0.478,-0.491,1.205,-0.793,1.271c-0.022,0.005,-0.043,-0.008,-0.05,-0.026C-52.364,-160.147,-52.364,-160.149,-52.364,-160.153z"/>
            </g>
            <path  fill="#D1C690" d="M-52.374,-159.853c0,0,0.001,-0.227,-0.198,-0.244c0,0.045,0,0.244,0,0.244L-52.374,-159.853z"/>
            <path  fill="#D1C690" d="M-52.171,-160.131c0,0,-0.195,0.101,-0.224,0.034c-0.03,-0.068,-0.033,-0.113,0.018,-0.152C-52.323,-160.289,-52.171,-160.131,-52.171,-160.131z"/>
            <path  fill="#9D956C" d="M-52.597,-159.902c0.053,0.172,-0.394,0.395,-0.445,0.528c-0.038,0.092,-0.081,0.21,-0.103,0.381l0.038,0c0.022,-0.169,0.066,-0.285,0.103,-0.381c0.051,-0.133,0.499,-0.356,0.443,-0.528L-52.597,-159.902z"/>
            <polygon  fill="#9D956C" points="-51.764,-161.206,-51.829,-161.822,-51.794,-161.822,-51.728,-161.206"/>
            <path  fill="#9D956C" d="M-52.37,-160.189c0.186,-0.04,0.772,-0.682,0.732,-1.201l0.038,0c0.039,0.559,-0.548,1.164,-0.734,1.203L-52.37,-160.189z"/>
            <path  fill="#9D956C" d="M-52.608,-160.097c0,0.045,0,0.243,0,0.243l0.037,0c0,0,0,-0.198,0,-0.243L-52.608,-160.097z"/>
            <path  fill="#9D956C" d="M-52.41,-160.25c-0.051,0.04,-0.048,0.083,-0.02,0.152l0.039,0.001c-0.032,-0.068,-0.034,-0.115,0.018,-0.153L-52.41,-160.25z"/>
           </g>
           <path  opacity="0.5" fill="#F2F2F2" enable-background="new    " d="M-51.062,-161.811l-2.442,0l0,3.388l2.442,0.003L-51.062,-161.811z"/>
           <path  opacity="0.03" enable-background="new    " d="M-53.364,-158.511c-0.043,0,-0.087,0.007,-0.087,-0.063c0,-0.39,0,-2.974,0,-3.069c0,-0.107,0.041,-0.113,0.041,0.005c0,0.086,0.001,2,0.001,2.287C-53.409,-158.971,-53.364,-158.511,-53.364,-158.511z"/>
           <path  fill="#D1C690" d="M-53.505,-162.422l0,0.491l0.332,0c0.08,0,0.136,0.051,0.171,0.12l1.942,0l0,-0.644l-2.412,0l-0.032,0"/>
           <path  fill="#D1C690" d="M-53.505,-157.74l0.031,0l2.412,0l0,-0.683l-2.208,0c-0.036,0.067,-0.093,0.122,-0.173,0.122l-0.063,0l0,0.529"/>
          </g>
         </g>
        </g>
       </g>
      </g>
     </g>
     <g transform="matrix(1, 0, 0, 1, 27.326, 98.3995)">
      <g  id="sot223">
       <g transform="matrix(0, 1, -1, 0, 19.6385, 0.486504)">
        <g >
         <g >
          <g transform="matrix(2.57889e-06, 1, -1, 2.57889e-06, 24.9126, -23.9179)">
           <rect  width="4.896" x="21.967" y="-1.231" fill="#999999" height="3.457"/>
          </g>
          <g transform="matrix(2.57889e-06, 1, -1, 2.57889e-06, 18.3598, -17.3632)">
           <rect  width="4.896" x="15.414" y="-1.231" fill="#999999" height="3.459"/>
          </g>
          <g transform="matrix(2.57889e-06, 1, -1, 2.57889e-06, 11.8047, -10.809)">
           <rect  width="4.896" x="8.859" y="-1.23" fill="#999999" height="3.455"/>
          </g>
          <g transform="matrix(2.57889e-06, 1, -1, 2.57889e-06, 33.3911, -2.3281)">
           <rect  width="5.285" x="15.217" y="10.427" fill="#999999" height="10.209"/>
          </g>
          <g transform="matrix(2.57889e-06, 1, -1, 2.57889e-06, 25.7798, -9.9443)">
           <rect  width="9.943" x="12.891" y="-1.663" fill="#303030" height="19.161"/>
          </g>
          <polygon  fill="#1F1F1F" points="27.443,12.889,8.28,12.889,9,12.168,26.718,12.168"/>
          <polygon  fill="#1F1F1F" points="27.443,2.946,8.28,2.946,9,3.669,26.718,3.669"/>
          <polygon  points="27.443,12.889,27.443,2.946,26.718,3.669,26.718,12.168"/>
          <polygon  fill="#3D3D3D" points="8.28,12.889,8.28,2.946,9,3.669,9,12.168"/>
          <circle  fill="#1F1F1F" cx="25.28" cy="5.109" r="0.72"/>
         </g>
        </g>
       </g>
      </g>
     </g>
     <g transform="matrix(1, 0, 0, 1, 87.5282, 89.7559)">
      <g  id="sot23-5_3_">
       <g transform="matrix(0, 1, -1, 0, 8.26704, 0.203004)">
        <g >
         <g >
          <g transform="matrix(2.57889e-06, 1, -1, 2.57889e-06, 17.1285, -18.9664)">
           <rect  width="2.061" x="17.017" y="-1.647" fill="#999999" height="1.457"/>
          </g>
          <g transform="matrix(2.57889e-06, 1, -1, 2.57889e-06, 23.3736, -12.7213)">
           <rect  width="2.061" x="17.017" y="4.598" fill="#999999" height="1.457"/>
          </g>
          <g transform="matrix(2.57889e-06, 1, -1, 2.57889e-06, 14.3697, -16.2076)">
           <rect  width="2.061" x="14.258" y="-1.646" fill="#999999" height="1.455"/>
          </g>
          <g transform="matrix(2.57889e-06, 1, -1, 2.57889e-06, 11.6114, -13.4503)">
           <rect  width="2.061" x="11.5" y="-1.647" fill="#999999" height="1.455"/>
          </g>
          <g transform="matrix(2.57889e-06, 1, -1, 2.57889e-06, 17.8565, -7.2052)">
           <rect  width="2.061" x="11.5" y="4.598" fill="#999999" height="1.455"/>
          </g>
          <g transform="matrix(2.57889e-06, 1, -1, 2.57889e-06, 17.4957, -13.0865)">
           <rect  width="4.185" x="13.199" y="-1.827" fill="#303030" height="8.063"/>
          </g>
          <polygon  fill="#1F1F1F" points="19.322,4.296,11.258,4.296,11.559,3.993,19.018,3.993"/>
          <polygon  fill="#1F1F1F" points="19.322,0.112,11.258,0.112,11.559,0.416,19.018,0.416"/>
          <polygon  points="19.322,4.296,19.322,0.112,19.018,0.416,19.018,3.993"/>
          <polygon  fill="#3D3D3D" points="11.258,4.296,11.258,0.112,11.559,0.416,11.559,3.993"/>
          <circle  fill="#1F1F1F" cx="18.413" cy="1.021" r="0.303"/>
         </g>
        </g>
       </g>
      </g>
     </g>
     <g transform="matrix(1, 0, 0, 1, 87.5282, 89.7559)">
      <g  id="sot23-5_1_">
       <g transform="matrix(0, 1, -1, 0, 8.26704, 0.203004)">
        <g >
         <g >
          <g transform="matrix(2.57889e-06, 1, -1, 2.57889e-06, -47.9128, -54.7126)">
           <rect  width="1.445" x="2.677" y="-51.823" fill="#999999" height="1.021"/>
          </g>
          <g transform="matrix(2.57889e-06, 1, -1, 2.57889e-06, -43.5363, -50.3362)">
           <rect  width="1.444" x="2.678" y="-47.447" fill="#999999" height="1.021"/>
          </g>
          <g transform="matrix(2.57889e-06, 1, -1, 2.57889e-06, -49.8483, -52.7771)">
           <rect  width="1.445" x="0.742" y="-51.823" fill="#999999" height="1.021"/>
          </g>
          <g transform="matrix(2.57889e-06, 1, -1, 2.57889e-06, -51.7804, -50.8449)">
           <rect  width="1.445" x="-1.19" y="-51.823" fill="#999999" height="1.021"/>
          </g>
          <g transform="matrix(2.57889e-06, 1, -1, 2.57889e-06, -47.404, -46.4695)">
           <rect  width="1.443" x="-1.189" y="-47.448" fill="#999999" height="1.021"/>
          </g>
          <g transform="matrix(2.57889e-06, 1, -1, 2.57889e-06, -47.6564, -50.5901)">
           <rect  width="2.934" x="0" y="-51.949" fill="#303030" height="5.651"/>
          </g>
          <polygon  fill="#1F1F1F" points="4.294,-47.658,-1.36,-47.658,-1.149,-47.869,4.081,-47.869"/>
          <polygon  fill="#1F1F1F" points="4.294,-50.59,-1.36,-50.59,-1.149,-50.377,4.081,-50.377"/>
          <polygon  points="4.294,-47.658,4.294,-50.59,4.081,-50.377,4.081,-47.869"/>
          <polygon  fill="#3D3D3D" points="-1.36,-47.658,-1.36,-50.59,-1.149,-50.377,-1.149,-47.869"/>
          <circle  fill="#1F1F1F" cx="3.654" cy="-49.953" r="0.212"/>
         </g>
        </g>
       </g>
      </g>
     </g>
     <g transform="matrix(1, 0, 0, 1, 87.5282, 89.7559)">
      <g  id="sot23-5_2_">
       <g transform="matrix(0, 1, -1, 0, 8.26704, 0.203004)">
        <g >
         <g >
          <g transform="matrix(2.57889e-06, 1, -1, 2.57889e-06, -37.8503, -64.7751)">
           <rect  width="1.445" x="12.74" y="-51.823" fill="#999999" height="1.021"/>
          </g>
          <g transform="matrix(2.57889e-06, 1, -1, 2.57889e-06, -33.4743, -60.3991)">
           <rect  width="1.443" x="12.741" y="-47.448" fill="#999999" height="1.021"/>
          </g>
          <g transform="matrix(2.57889e-06, 1, -1, 2.57889e-06, -39.7858, -62.8396)">
           <rect  width="1.445" x="10.804" y="-51.823" fill="#999999" height="1.021"/>
          </g>
          <g transform="matrix(2.57889e-06, 1, -1, 2.57889e-06, -41.7179, -60.9074)">
           <rect  width="1.445" x="8.872" y="-51.823" fill="#999999" height="1.021"/>
          </g>
          <g transform="matrix(2.57889e-06, 1, -1, 2.57889e-06, -37.341, -56.5315)">
           <rect  width="1.444" x="8.873" y="-47.447" fill="#999999" height="1.021"/>
          </g>
          <g transform="matrix(2.57889e-06, 1, -1, 2.57889e-06, -37.5939, -60.6526)">
           <rect  width="2.934" x="10.063" y="-51.949" fill="#303030" height="5.651"/>
          </g>
          <polygon  fill="#1F1F1F" points="14.355,-47.658,8.704,-47.658,8.915,-47.869,14.142,-47.869"/>
          <polygon  fill="#1F1F1F" points="14.355,-50.59,8.704,-50.59,8.915,-50.377,14.142,-50.377"/>
          <polygon  points="14.355,-47.658,14.355,-50.59,14.142,-50.377,14.142,-47.869"/>
          <polygon  fill="#3D3D3D" points="8.704,-47.658,8.704,-50.59,8.915,-50.377,8.915,-47.869"/>
          <circle  fill="#1F1F1F" cx="13.715" cy="-49.953" r="0.212"/>
         </g>
        </g>
       </g>
      </g>
     </g>
     <g transform="matrix(1, 0, 0, 1, 87.5282, 89.7559)">
      <g  id="sot23-5_4_">
       <g transform="matrix(0, 1, -1, 0, 8.26704, 0.203004)">
        <g >
         <g >
          <g transform="matrix(2.57889e-06, 1, -1, 2.57889e-06, -26.0588, -76.5666)">
           <rect  width="1.445" x="24.531" y="-51.823" fill="#999999" height="1.021"/>
          </g>
          <g transform="matrix(2.57889e-06, 1, -1, 2.57889e-06, -21.6819, -72.1916)">
           <rect  width="1.443" x="24.533" y="-47.447" fill="#999999" height="1.021"/>
          </g>
          <g transform="matrix(2.57889e-06, 1, -1, 2.57889e-06, -27.9934, -74.632)">
           <rect  width="1.445" x="22.597" y="-51.823" fill="#999999" height="1.021"/>
          </g>
          <g transform="matrix(2.57889e-06, 1, -1, 2.57889e-06, -29.9265, -72.6989)">
           <rect  width="1.445" x="20.664" y="-51.823" fill="#999999" height="1.021"/>
          </g>
          <g transform="matrix(2.57889e-06, 1, -1, 2.57889e-06, -25.5495, -68.323)">
           <rect  width="1.444" x="20.665" y="-47.447" fill="#999999" height="1.021"/>
          </g>
          <g transform="matrix(2.57889e-06, 1, -1, 2.57889e-06, -25.8025, -72.4441)">
           <rect  width="2.934" x="21.854" y="-51.949" fill="#303030" height="5.652"/>
          </g>
          <polygon  fill="#1F1F1F" points="26.147,-47.658,20.495,-47.658,20.706,-47.869,25.934,-47.869"/>
          <polygon  fill="#1F1F1F" points="26.147,-50.59,20.495,-50.59,20.706,-50.377,25.934,-50.377"/>
          <polygon  points="26.147,-47.658,26.147,-50.59,25.934,-50.377,25.934,-47.869"/>
          <polygon  fill="#3D3D3D" points="20.495,-47.658,20.495,-50.59,20.706,-50.377,20.706,-47.869"/>
          <circle  fill="#1F1F1F" cx="25.508" cy="-49.953" r="0.212"/>
         </g>
        </g>
       </g>
      </g>
     </g>
     <g transform="matrix(1, 0, 0, 1, 96.1474, 28.8155)">
      <g  id="chipled_0805_2_">
       <g transform="matrix(0, -1, 1, 0, -1.77951, 5.62951)">
        <g >
         <g transform="matrix(1, 0, 0, 1, 21.5539, 31.3385)">
          <g  id="led-0603_3_">
           <line  fill="none" y1="-32.089" x1="-13.436" y2="-24.852" x2="-13.436"/>
           <g transform="matrix(-2.54711e-06, -1, 1, -2.54711e-06, 16.8926, -39.9356)">
            <rect  width="7.348" x="-15.196" y="-30.331" fill="#F2F2F2" height="3.833"/>
           </g>
           <path  fill="#22B573" fill-opacity="0.7" d="M-13.438,-27.341c0,0,0.467,0.645,0.426,0.867c-0.041,0.219,0.148,0.541,0,0.676l-0.424,-0.018L-13.438,-27.341z"/>
           <g >
            <g transform="matrix(-2.54711e-06, -1, 1, -2.54711e-06, 16.5125, -40.4593)">
             <rect  width="0.854" x="-12.4" y="-28.511" fill="#B3B3B3" height="0.049"/>
            </g>
           </g>
           <g >
            <polygon  fill="#D1C690" points="-13.014,-26.761,-13.118,-25.798,-12.387,-25.798,-12.491,-26.761"/>
            <g >
             <path  fill="#D1C690" d="M-12.815,-26.699c0,-0.002,0,-0.004,0,-0.008c0.035,-0.266,0.104,-0.447,0.162,-0.598c0.08,-0.209,0.782,-0.559,0.696,-0.828c-0.012,-0.027,0.011,-0.06,0.043,-0.066c0.035,-0.008,0.068,0.01,0.078,0.039c0.095,0.305,-0.617,0.674,-0.701,0.893c-0.06,0.148,-0.123,0.318,-0.155,0.572c-0.004,0.029,-0.033,0.055,-0.068,0.049C-12.79,-26.65,-12.815,-26.673,-12.815,-26.699z"/>
            </g>
            <polygon  fill="#D1C690" points="-10.126,-30.18,-10.023,-31.146,-10.753,-31.146,-10.65,-30.18"/>
            <g >
             <path  fill="#D1C690" d="M-11.647,-28.528c0,-0.025,0.02,-0.049,0.047,-0.055c0.292,-0.063,1.152,-1.088,1.152,-1.885c0,-0.033,0.026,-0.057,0.063,-0.057c0.034,0.002,0.063,0.025,0.063,0.057l0,0.002c0,0.749,-0.77,1.891,-1.245,1.993c-0.035,0.008,-0.068,-0.012,-0.078,-0.041C-11.647,-28.518,-11.647,-28.522,-11.647,-28.528z"/>
            </g>
            <path  fill="#D1C690" d="M-11.663,-28.057c0,0,0.002,-0.356,-0.311,-0.383c0,0.07,0,0.383,0,0.383L-11.663,-28.057z"/>
            <path  fill="#D1C690" d="M-11.344,-28.492c0,0,-0.306,0.158,-0.351,0.053c-0.048,-0.107,-0.052,-0.178,0.028,-0.24C-11.583,-28.741,-11.344,-28.492,-11.344,-28.492z"/>
            <path  fill="#9D956C" d="M-12.012,-28.134c0.084,0.27,-0.618,0.619,-0.698,0.828c-0.06,0.145,-0.127,0.33,-0.162,0.598l0.059,0c0.035,-0.266,0.104,-0.447,0.162,-0.598c0.08,-0.209,0.782,-0.559,0.696,-0.828L-12.012,-28.134z"/>
            <polygon  fill="#9D956C" points="-10.705,-30.18,-10.808,-31.146,-10.753,-31.146,-10.65,-30.18"/>
            <path  fill="#9D956C" d="M-11.657,-28.584c0.291,-0.062,1.212,-1.07,1.149,-1.885l0.06,0c0.06,0.877,-0.86,1.826,-1.152,1.887L-11.657,-28.584z"/>
            <path  fill="#9D956C" d="M-12.03,-28.441c0,0.07,0,0.381,0,0.381l0.057,0c0,0,0,-0.311,0,-0.381L-12.03,-28.441z"/>
            <path  fill="#9D956C" d="M-11.719,-28.68c-0.08,0.063,-0.076,0.131,-0.031,0.238l0.06,0.002c-0.049,-0.107,-0.052,-0.179,0.028,-0.24L-11.719,-28.68z"/>
           </g>
           <path  opacity="0.5" fill="#F2F2F2" enable-background="new    " d="M-9.605,-31.13l-3.831,0l0,5.317l3.831,0.004L-9.605,-31.13z"/>
           <path  opacity="0.03" enable-background="new    " d="M-13.216,-25.951c-0.068,0,-0.138,0.012,-0.138,-0.098c0,-0.611,0,-4.667,0,-4.817c0,-0.168,0.065,-0.176,0.065,0.008c0,0.135,0.002,3.138,0.002,3.589C-13.286,-26.675,-13.216,-25.951,-13.216,-25.951z"/>
           <path  fill="#D1C690" d="M-13.438,-32.088l0,0.771l0.521,0c0.125,0,0.213,0.08,0.268,0.188l3.047,0l0,-1.01l-3.784,0l-0.05,0"/>
           <path  fill="#D1C690" d="M-13.438,-24.741l0.049,0l3.784,0l0,-1.072l-3.464,0c-0.056,0.105,-0.146,0.191,-0.271,0.191l-0.1,0l0,0.83"/>
          </g>
         </g>
        </g>
       </g>
      </g>
     </g>
     <g transform="matrix(1, 0, 0, 1, 96.9761, 35.2955)">
      <g  id="chipled_0805_5_">
       <g transform="matrix(0, -1, 1, 0, -1.77951, 5.62951)">
        <g >
         <g transform="matrix(1, 0, 0, 1, 21.5539, 31.3385)">
          <g  id="led-0603_6_">
           <line  fill="none" y1="-32.881" x1="-12.921" y2="-25.645" x2="-12.921"/>
           <g transform="matrix(-2.54711e-06, -1, 1, -2.54711e-06, 18.2013, -40.2131)">
            <rect  width="7.348" x="-14.68" y="-31.124" fill="#F2F2F2" height="3.833"/>
           </g>
           <path  fill="#22B573" fill-opacity="0.7" d="M-12.923,-28.133c0,0,0.467,0.645,0.426,0.867c-0.041,0.219,0.148,0.541,0,0.676l-0.424,-0.018L-12.923,-28.133z"/>
           <g >
            <g transform="matrix(-2.54711e-06, -1, 1, -2.54711e-06, 17.8195, -40.7375)">
             <rect  width="0.854" x="-11.886" y="-29.303" fill="#B3B3B3" height="0.049"/>
            </g>
           </g>
           <g >
            <polygon  fill="#D1C690" points="-12.499,-27.553,-12.603,-26.59,-11.872,-26.59,-11.976,-27.553"/>
            <g >
             <path  fill="#D1C690" d="M-12.3,-27.492c0,-0.002,0,-0.004,0,-0.008c0.035,-0.266,0.104,-0.447,0.162,-0.598c0.08,-0.209,0.782,-0.559,0.696,-0.828c-0.012,-0.027,0.011,-0.06,0.043,-0.066c0.035,-0.008,0.068,0.01,0.078,0.039c0.095,0.305,-0.617,0.674,-0.701,0.893c-0.06,0.148,-0.123,0.318,-0.155,0.572c-0.004,0.029,-0.033,0.055,-0.068,0.049C-12.275,-27.442,-12.3,-27.465,-12.3,-27.492z"/>
            </g>
            <polygon  fill="#D1C690" points="-9.611,-30.973,-9.508,-31.939,-10.238,-31.939,-10.135,-30.973"/>
            <g >
             <path  fill="#D1C690" d="M-11.132,-29.32c0,-0.025,0.02,-0.049,0.047,-0.055c0.292,-0.063,1.152,-1.088,1.152,-1.885c0,-0.033,0.026,-0.057,0.063,-0.057c0.034,0.002,0.063,0.025,0.063,0.057l0,0.002c0,0.749,-0.77,1.891,-1.245,1.993c-0.035,0.008,-0.068,-0.012,-0.078,-0.041C-11.132,-29.311,-11.132,-29.315,-11.132,-29.32z"/>
            </g>
            <path  fill="#D1C690" d="M-11.148,-28.85c0,0,0.002,-0.356,-0.311,-0.383c0,0.07,0,0.383,0,0.383L-11.148,-28.85z"/>
            <path  fill="#D1C690" d="M-10.829,-29.285c0,0,-0.306,0.158,-0.351,0.053c-0.048,-0.107,-0.052,-0.178,0.028,-0.24C-11.068,-29.533,-10.829,-29.285,-10.829,-29.285z"/>
            <path  fill="#9D956C" d="M-11.497,-28.926c0.084,0.27,-0.618,0.619,-0.698,0.828c-0.06,0.145,-0.127,0.33,-0.162,0.598l0.059,0c0.035,-0.266,0.104,-0.447,0.162,-0.598c0.08,-0.209,0.782,-0.559,0.696,-0.828L-11.497,-28.926z"/>
            <polygon  fill="#9D956C" points="-10.19,-30.973,-10.293,-31.939,-10.238,-31.939,-10.135,-30.973"/>
            <path  fill="#9D956C" d="M-11.142,-29.377c0.291,-0.062,1.212,-1.07,1.149,-1.885l0.06,0c0.06,0.877,-0.86,1.826,-1.152,1.887L-11.142,-29.377z"/>
            <path  fill="#9D956C" d="M-11.515,-29.233c0,0.07,0,0.381,0,0.381l0.057,0c0,0,0,-0.311,0,-0.381L-11.515,-29.233z"/>
            <path  fill="#9D956C" d="M-11.204,-29.473c-0.08,0.063,-0.076,0.131,-0.031,0.238l0.06,0.002c-0.049,-0.107,-0.052,-0.179,0.028,-0.24L-11.204,-29.473z"/>
           </g>
           <path  opacity="0.5" fill="#F2F2F2" enable-background="new    " d="M-9.09,-31.922l-3.831,0l0,5.317l3.831,0.004L-9.09,-31.922z"/>
           <path  opacity="0.03" enable-background="new    " d="M-12.701,-26.744c-0.068,0,-0.138,0.012,-0.138,-0.098c0,-0.611,0,-4.667,0,-4.817c0,-0.168,0.065,-0.176,0.065,0.008c0,0.135,0.002,3.138,0.002,3.589C-12.771,-27.467,-12.701,-26.744,-12.701,-26.744z"/>
           <path  fill="#D1C690" d="M-12.923,-32.88l0,0.771l0.521,0c0.125,0,0.213,0.08,0.268,0.188l3.047,0l0,-1.01l-3.784,0l-0.05,0"/>
           <path  fill="#D1C690" d="M-12.923,-25.533l0.049,0l3.784,0l0,-1.072l-3.464,0c-0.056,0.105,-0.146,0.191,-0.271,0.191l-0.1,0l0,0.83"/>
          </g>
         </g>
        </g>
       </g>
      </g>
     </g>
     <g transform="matrix(1, 0, 0, 1, 96.9761, 41.7755)">
      <g  id="chipled_0805_6_">
       <g transform="matrix(0, -1, 1, 0, -1.77951, 5.62951)">
        <g >
         <g transform="matrix(1, 0, 0, 1, 21.5539, 31.3385)">
          <g  id="led-0603_7_">
           <line  fill="none" y1="-32.892" x1="-12.471" y2="-25.656" x2="-12.471"/>
           <g transform="matrix(-2.54711e-06, -1, 1, -2.54711e-06, 18.6618, -39.775)">
            <rect  width="7.348" x="-14.231" y="-31.135" fill="#F2F2F2" height="3.833"/>
           </g>
           <path  fill="#22B573" fill-opacity="0.7" d="M-12.473,-28.144c0,0,0.467,0.645,0.426,0.867c-0.041,0.219,0.148,0.541,0,0.676l-0.424,-0.018L-12.473,-28.144z"/>
           <g >
            <g transform="matrix(-2.54711e-06, -1, 1, -2.54711e-06, 18.2809, -40.2985)">
             <rect  width="0.854" x="-11.436" y="-29.314" fill="#B3B3B3" height="0.049"/>
            </g>
           </g>
           <g >
            <polygon  fill="#D1C690" points="-12.049,-27.564,-12.153,-26.601,-11.422,-26.601,-11.526,-27.564"/>
            <g >
             <path  fill="#D1C690" d="M-11.85,-27.503c0,-0.002,0,-0.004,0,-0.008c0.035,-0.266,0.104,-0.447,0.162,-0.598c0.08,-0.209,0.782,-0.559,0.696,-0.828c-0.012,-0.027,0.011,-0.06,0.043,-0.066c0.035,-0.008,0.068,0.01,0.078,0.039c0.095,0.305,-0.617,0.674,-0.701,0.893c-0.06,0.148,-0.123,0.318,-0.155,0.572c-0.004,0.029,-0.033,0.055,-0.068,0.049C-11.825,-27.453,-11.85,-27.476,-11.85,-27.503z"/>
            </g>
            <polygon  fill="#D1C690" points="-9.161,-30.984,-9.058,-31.95,-9.788,-31.95,-9.685,-30.984"/>
            <g >
             <path  fill="#D1C690" d="M-10.682,-29.331c0,-0.025,0.02,-0.049,0.047,-0.055c0.292,-0.063,1.152,-1.088,1.152,-1.885c0,-0.033,0.026,-0.057,0.063,-0.057c0.034,0.002,0.063,0.025,0.063,0.057l0,0.002c0,0.749,-0.77,1.891,-1.245,1.993c-0.035,0.008,-0.068,-0.012,-0.078,-0.041C-10.682,-29.322,-10.682,-29.326,-10.682,-29.331z"/>
            </g>
            <path  fill="#D1C690" d="M-10.698,-28.861c0,0,0.002,-0.356,-0.311,-0.383c0,0.07,0,0.383,0,0.383L-10.698,-28.861z"/>
            <path  fill="#D1C690" d="M-10.378,-29.296c0,0,-0.306,0.158,-0.351,0.053c-0.048,-0.107,-0.052,-0.178,0.028,-0.24C-10.618,-29.544,-10.378,-29.296,-10.378,-29.296z"/>
            <path  fill="#9D956C" d="M-11.047,-28.937c0.084,0.27,-0.618,0.619,-0.698,0.828c-0.06,0.145,-0.127,0.33,-0.162,0.598l0.059,0c0.035,-0.266,0.104,-0.447,0.162,-0.598c0.08,-0.209,0.782,-0.559,0.696,-0.828L-11.047,-28.937z"/>
            <polygon  fill="#9D956C" points="-9.74,-30.984,-9.843,-31.95,-9.788,-31.95,-9.685,-30.984"/>
            <path  fill="#9D956C" d="M-10.692,-29.388c0.291,-0.062,1.212,-1.07,1.149,-1.885l0.06,0c0.06,0.877,-0.86,1.826,-1.152,1.887L-10.692,-29.388z"/>
            <path  fill="#9D956C" d="M-11.065,-29.244c0,0.07,0,0.381,0,0.381l0.057,0c0,0,0,-0.311,0,-0.381L-11.065,-29.244z"/>
            <path  fill="#9D956C" d="M-10.753,-29.484c-0.08,0.063,-0.076,0.131,-0.031,0.238l0.06,0.002c-0.049,-0.107,-0.052,-0.179,0.028,-0.24L-10.753,-29.484z"/>
           </g>
           <path  opacity="0.5" fill="#F2F2F2" enable-background="new    " d="M-8.64,-31.933l-3.831,0l0,5.317l3.831,0.004L-8.64,-31.933z"/>
           <path  opacity="0.03" enable-background="new    " d="M-12.25,-26.755c-0.068,0,-0.138,0.012,-0.138,-0.098c0,-0.611,0,-4.667,0,-4.817c0,-0.168,0.065,-0.176,0.065,0.008c0,0.135,0.002,3.138,0.002,3.589C-12.321,-27.478,-12.25,-26.755,-12.25,-26.755z"/>
           <path  fill="#D1C690" d="M-12.473,-32.891l0,0.771l0.521,0c0.125,0,0.213,0.08,0.268,0.188l3.047,0l0,-1.01l-3.784,0l-0.05,0"/>
           <path  fill="#D1C690" d="M-12.473,-25.544l0.049,0l3.784,0l0,-1.072l-3.464,0c-0.056,0.105,-0.146,0.191,-0.271,0.191l-0.1,0l0,0.83"/>
          </g>
         </g>
        </g>
       </g>
      </g>
     </g>
     <g transform="matrix(1, 0, 0, 1, -0.0552163, 20.585)">
      <g  id="poe-rj45_1_">
       <g transform="matrix(1, 0, 0, 1, 7.74281, 14.064)">
        <g  id="poe-rj45">
         <g >
          <rect  width="54.427" x="-6.851" y="-15.051" fill="#1A1A1A" height="43.774"/>
          <g >
           <path  fill="#B3B3B3" d="M2.48,-4.216c0.396,0,0.719,0.324,0.719,0.725l0,2.648c0,0.396,-0.324,0.725,-0.719,0.725l-9.449,0c-0.396,0,-0.719,-0.324,-0.719,-0.725l0,-2.648c0,-0.396,0.323,-0.725,0.719,-0.725L2.48,-4.216z"/>
           <path  fill="#B3B3B3" d="M2.48,13.792c0.396,0,0.719,0.324,0.719,0.725l0,2.648c0,0.395,-0.324,0.725,-0.719,0.725l-9.449,0c-0.396,0,-0.719,-0.324,-0.719,-0.725l0,-2.648c0,-0.396,0.323,-0.725,0.719,-0.725L2.48,13.792z"/>
           <path  fill="#CCCCCC" d="M2.48,-4.216c0.396,0,0.719,0.324,0.719,0.725l0,2.648c0,0.396,-0.324,0.725,-0.719,0.725L1.312,-0.118l0,-4.098L2.48,-4.216L2.48,-4.216z"/>
           <path  fill="#CCCCCC" d="M2.48,13.792c0.396,0,0.719,0.324,0.719,0.725l0,2.648c0,0.395,-0.324,0.725,-0.719,0.725L1.312,17.89l0,-4.098L2.48,13.792z"/>
           <rect  width="4.063" x="-2.565" y="-4.216" fill="#999999" height="4.098"/>
           <rect  width="4.063" x="-2.565" y="13.792" fill="#999999" height="4.098"/>
           <rect  width="3.875" x="-4.938" y="-4.216" fill="#B3B3B3" height="4.098"/>
           <rect  width="3.875" x="-4.938" y="13.792" fill="#B3B3B3" height="4.098"/>
           <rect  width="1.469" x="-4.314" y="-4.216" fill="#CCCCCC" height="4.098"/>
           <rect  width="1.469" x="-4.314" y="13.792" fill="#CCCCCC" height="4.098"/>
           <rect  width="0.311" x="1.342" y="-4.216" fill="#E6E6E6" height="4.098"/>
           <rect  width="0.489" x="1.711" y="-4.212" fill="#F2F2F2" height="4.098"/>
           <path  fill="#CCCCCC" d="M3.578,28.726l49.777,0l0.721,0l0,-0.721l0,-42.334l0,-0.722l-0.721,0L3.578,-15.051l0,0.288L-6.851,-14.763l0,0.436L-6.851,-5.7l0,0.721l0.717,0.047l5.104,0.336L4.074,-4.26c0.395,0.025,0.719,0.371,0.719,0.771l0,2.666c0,0.396,-0.324,0.738,-0.719,0.768L-1.03,0.28l-5.104,0.336l0,0l-0.717,0.049l0,0.723l0,10.918l0,0.721l0.717,0.051l0,0l5.104,0.346l5.105,0.348c0.396,0.023,0.718,0.373,0.718,0.768l0,2.629c0,0.396,-0.322,0.74,-0.718,0.771l-5.105,0.346l-5.104,0.344l0,0l-0.717,0.049l0,0.719l0,8.627l0,0.432l10.43,0L3.578,28.726L3.578,28.726z"/>
          </g>
          <rect  width="60.926" x="-6.85" opacity="0.37" y="-15.051" fill="#E6E6E6" height="3.475" enable-background="new    "/>
          <rect  width="60.926" x="-6.85" opacity="0.37" y="25.255" fill="#808080" height="3.473" enable-background="new    "/>
          <path  opacity="0.45" fill="#E6E6E6" enable-background="new    " d="M-6.85,-2.169l0,-2.047c0,0,8.854,0,9.33,0c0.479,0,0.721,0.434,0.721,0.725s0,1.322,0,1.322L-6.85,-2.169z"/>
          <path  opacity="0.45" fill="#E6E6E6" enable-background="new    " d="M-6.85,15.837l0,-2.043c0,0,8.854,0,9.33,0c0.479,0,0.721,0.428,0.721,0.719s0,1.324,0,1.324L-6.85,15.837L-6.85,15.837z"/>
          <path  opacity="0.45" fill="#B3B3B3" enable-background="new    " d="M-6.85,15.841l0,2.049c0,0,8.854,0,9.33,0c0.479,0,0.721,-0.436,0.721,-0.727s0,-1.322,0,-1.322L-6.85,15.841z"/>
          <path  opacity="0.45" fill="#B3B3B3" enable-background="new    " d="M-6.85,-2.169l0,2.051c0,0,8.854,0,9.33,0c0.479,0,0.721,-0.432,0.721,-0.723s0,-1.328,0,-1.328L-6.85,-2.169z"/>
          <rect  width="0.813" x="-3.876" opacity="0.76" y="-4.216" fill="#E6E6E6" height="4.098" enable-background="new    "/>
          <rect  width="0.813" x="-3.876" opacity="0.76" y="13.792" fill="#E6E6E6" height="4.098" enable-background="new    "/>
          <rect  width="0.311" x="1.342" opacity="0.76" y="13.792" fill="#E6E6E6" height="4.098" enable-background="new    "/>
          <rect  width="0.411" x="1.685" opacity="0.76" y="13.796" fill="#F2F2F2" height="4.094" enable-background="new    "/>
          <g >
           <g >
            <rect  width="1.699" x="4.276" y="-16.236" fill="#999999" height="0.386"/>
            <rect  width="1.699" x="4.276" y="-16.236" fill="#999999" height="0.386"/>
           </g>
           <path  fill="#999999" d="M-0.466,-15.055c0,0,2.991,-0.657,4.741,-0.782l0,-0.398c-1.75,0.125,-4.741,0.783,-4.741,0.783s-1.497,0.254,-1.903,0.396C-1.4,-15.055,-0.466,-15.055,-0.466,-15.055z"/>
           <path  fill="#CCCCCC" d="M1.222,-15.055c0,0,3.003,-0.669,4.753,-0.794l0,-0.396c-1.75,0.125,-4.753,0.794,-4.753,0.794s-1.497,0.254,-1.903,0.396C0.287,-15.055,1.222,-15.055,1.222,-15.055z"/>
          </g>
          <g >
           <g >
            <rect  width="1.699" x="4.276" y="29.525" fill="#999999" height="0.387"/>
            <rect  width="1.699" x="4.276" y="29.525" fill="#999999" height="0.387"/>
           </g>
           <path  fill="#999999" d="M-0.466,28.73c0,0,2.991,0.656,4.741,0.781l0,0.398c-1.75,-0.125,-4.741,-0.783,-4.741,-0.783s-1.497,-0.254,-1.903,-0.396C-1.4,28.73,-0.466,28.73,-0.466,28.73z"/>
           <path  fill="#CCCCCC" d="M1.222,28.73c0,0,3.003,0.67,4.753,0.795l0,0.396c-1.75,-0.125,-4.753,-0.795,-4.753,-0.795s-1.497,-0.254,-1.903,-0.396C0.287,28.73,1.222,28.73,1.222,28.73z"/>
          </g>
         </g>
        </g>
       </g>
      </g>
     </g>
     <g transform="matrix(1, 0, 0, 1, 169.863, 76.0248)">
      <g  id="sdcard-15tw-8821_1_">
       <g transform="matrix(0, -1, 1, 0, -2.17051, 40.1935)">
        <g >
         <g transform="matrix(1, 0, 0, 1, 169.844, 75.5201)">
          <g  id="sdcard-15tw-8821">
           <g transform="matrix(0, -1, 1, 0, -1.60729, 40.7503)">
            <g >
             <rect  width="29.041" x="87.841" y="-144.845" height="8.864"/>
             <rect  width="20.677" x="95.862" y="-172.033" height="23.59"/>
             <path  fill="#404040" d="M116.884,-151.077l-1.033,0c-0.43,0,-0.78,-0.24,-0.78,-0.531l0,-2.076c0,-0.291,0.354,-0.525,0.78,-0.525l1.033,0"/>
             <path  opacity="0.1" enable-background="new    " d="M113.494,-154.034l2.053,0.104c0.361,0.019,0.656,0.25,0.656,0.519c0,0.266,0,1.262,0,1.526s-0.295,0.5,-0.656,0.521l-2.159,0.111"/>
             <path  fill="#404040" d="M116.884,-166.639l-1.033,0c-0.43,0,-0.78,-0.237,-0.78,-0.528l0,-2.076c0,-0.293,0.354,-0.527,0.78,-0.527l1.033,0"/>
             <path  opacity="0.1" enable-background="new    " d="M113.494,-169.596l2.053,0.104c0.361,0.021,0.656,0.25,0.656,0.519s0,1.263,0,1.526c0,0.269,-0.295,0.5,-0.656,0.521l-2.159,0.111"/>
             <rect  width="3.521" x="89.767" y="-172.033" fill="#404040" height="24.563"/>
             <g >
              <g >
               <rect  width="4.305" x="85.199" y="-158.755" fill="#B7B7B7" height="0.977"/>
               <rect  width="4.307" x="85.199" y="-155.794" fill="#B7B7B7" height="0.977"/>
               <rect  width="4.307" x="85.201" y="-152.835" fill="#B7B7B7" height="0.977"/>
               <rect  width="4.307" x="85.199" y="-149.876" fill="#B7B7B7" height="0.979"/>
              </g>
             </g>
             <g >
              <g >
               <rect  width="4.307" x="85.201" y="-171.074" fill="#B7B7B7" height="0.978"/>
               <rect  width="4.307" x="85.201" y="-168.115" fill="#B7B7B7" height="0.979"/>
               <rect  width="4.307" x="85.199" y="-165.154" fill="#B7B7B7" height="0.978"/>
               <rect  width="4.307" x="85.201" y="-162.193" fill="#B7B7B7" height="0.978"/>
              </g>
             </g>
             <g  opacity="0.15">
              <polygon  points="89.273,-159.089,89.017,-159.089,89.017,-157.434,89.273,-157.434,89.273,-156.135,89.017,-156.135,89.017,-154.479,89.273,-154.479,89.273,-153.176,89.017,-153.176,89.017,-151.52,89.273,-151.52,89.273,-150.193,89.017,-150.193,89.017,-148.534,89.273,-148.534,89.273,-148.283,91.628,-148.283,91.628,-159.449,89.273,-159.449"/>
             </g>
             <g  opacity="0.15">
              <polygon  points="89.273,-171.456,89.017,-171.456,89.017,-169.801,89.273,-169.801,89.273,-168.501,89.017,-168.501,89.017,-166.846,89.273,-166.846,89.273,-165.542,89.017,-165.542,89.017,-163.887,89.273,-163.887,89.273,-162.557,89.017,-162.557,89.017,-160.904,89.273,-160.904,89.273,-160.649,91.628,-160.649,91.628,-171.815,89.273,-171.815"/>
             </g>
             <g >
              <g >
               <rect  width="0.28" x="89.455" y="-150.096" fill="#B7B7B7" height="1.418"/>
               <rect  width="0.28" x="89.455" y="-153.055" fill="#B7B7B7" height="1.418"/>
               <rect  width="0.28" x="89.453" y="-156.016" fill="#B7B7B7" height="1.418"/>
               <rect  width="0.28" x="89.455" y="-158.977" fill="#B7B7B7" height="1.418"/>
               <rect  width="2" x="89.593" y="-158.755" fill="#B7B7B7" height="0.977"/>
               <rect  width="2" x="89.593" y="-155.794" fill="#B7B7B7" height="0.977"/>
               <rect  width="2" x="89.593" y="-152.837" fill="#B7B7B7" height="0.979"/>
               <rect  width="2" x="89.593" y="-149.876" fill="#B7B7B7" height="0.979"/>
              </g>
              <rect  width="1.809" x="90.996" opacity="0.15" y="-160.079" height="11.901" enable-background="new    "/>
             </g>
             <g >
              <g >
               <rect  width="0.278" x="89.456" y="-162.411" fill="#B7B7B7" height="1.418"/>
               <rect  width="0.28" x="89.455" y="-165.372" fill="#B7B7B7" height="1.418"/>
               <rect  width="0.28" x="89.455" y="-168.331" fill="#B7B7B7" height="1.418"/>
               <rect  width="0.28" x="89.453" y="-171.292" fill="#B7B7B7" height="1.418"/>
               <rect  width="2" x="89.593" y="-171.074" fill="#B7B7B7" height="0.978"/>
               <rect  width="2" x="89.593" y="-168.115" fill="#B7B7B7" height="0.979"/>
               <rect  width="2" x="89.593" y="-165.154" fill="#B7B7B7" height="0.978"/>
               <rect  width="2" x="89.593" y="-162.193" fill="#B7B7B7" height="0.978"/>
              </g>
              <rect  width="1.809" x="90.996" opacity="0.15" y="-172.397" height="11.901" enable-background="new    "/>
             </g>
             <g  opacity="0.2">
              <path  fill="#666666" d="M76.775,-171.971l2.338,1.472l0,23.684l-2.148,1.375l0,2.213l-2.438,1.412l0,4.838l2.601,0c0,0,0,-1.449,0,-1.875c0,-0.275,0.479,-0.275,0.479,0l0,0.301c0,0.375,0.078,0.5,0.313,0.5l0.985,0c0.234,0,0.313,-0.125,0.313,-0.5l0,-0.301c0,-0.275,0.479,-0.275,0.479,0l0,2.875l3.16,0l0,-38.029l-6.076,0l0,2.037L76.775,-171.971L76.775,-171.971z"/>
             </g>
             <g >
              <path  fill="#606060" d="M77.091,-171.971l2.34,1.472l0,23.684l-2.15,1.375l0,2.213l-2.438,1.412l0,4.838l2.601,0c0,0,0,-1.449,0,-1.875c0,-0.275,0.479,-0.275,0.479,0l0,0.301c0,0.375,0.078,0.5,0.313,0.5l0.986,0c0.232,0,0.313,-0.125,0.313,-0.5l0,-0.301c0,-0.275,0.479,-0.275,0.479,0l0,2.875l36.872,0l0,-2.684l-0.619,-0.08c-0.153,-0.021,-0.28,-0.164,-0.28,-0.318l0,-0.172c0,-0.152,0.127,-0.301,0.28,-0.316l0.619,-0.08l0,-10.703L98.32,-149.81c-0.313,0.01,-0.566,-0.174,-0.566,-0.4c0,-0.229,0.259,-0.434,0.565,-0.447l17.125,-0.881c0.313,-0.02,0.565,-0.219,0.565,-0.444l0,-1.316c0,-0.229,-0.258,-0.43,-0.565,-0.444l-17.125,-0.881c-0.312,-0.019,-0.565,-0.218,-0.565,-0.447c0,-0.229,0.259,-0.41,0.566,-0.4l18.566,0.521l0,-10.938l-18.566,0.521c-0.313,0.01,-0.566,-0.172,-0.566,-0.401s0.259,-0.433,0.565,-0.447l17.125,-0.881c0.313,-0.017,0.565,-0.217,0.565,-0.442l0,-1.316c0,-0.229,-0.258,-0.43,-0.565,-0.445l-17.125,-0.881c-0.312,-0.016,-0.565,-0.217,-0.565,-0.443c0,-0.229,0.259,-0.412,0.566,-0.404l18.566,0.521l0,-3.482L77.093,-173.987l0,2.031l-0.002,0L77.091,-171.971zM91.298,-141.538l0,-0.375c0,-0.154,0.117,-0.283,0.266,-0.283c0.146,0,0.264,0.053,0.264,0.117c0,0.065,0.127,0.119,0.283,0.119l12.479,0c0.156,0,0.283,0.127,0.283,0.282l0,5.615L89.106,-136.063l0,-0.44c0,-0.154,0.127,-0.302,0.278,-0.324l7.675,-1.137c0.153,-0.021,0.373,0.049,0.483,0.155l0.467,0.448c0.113,0.105,0.332,0.195,0.488,0.195l2.588,0c0.156,0,0.285,-0.129,0.285,-0.281l0,-3.471c0,-0.154,-0.129,-0.281,-0.285,-0.281l-2.433,0c-0.155,0,-0.364,0.099,-0.468,0.218l-0.82,0.981c-0.104,0.119,-0.313,0.229,-0.466,0.24l-7.517,0.607c-0.154,0.016,-0.281,-0.104,-0.281,-0.26c0,0,0,-2.515,0,-2.613c0,-0.098,0.115,-0.18,0.261,-0.18c0.142,0,0.259,0.129,0.259,0.283l0,0.379c0,0.155,0.127,0.282,0.282,0.282l1.109,0C91.171,-141.255,91.298,-141.383,91.298,-141.538zM90.732,-159.122c0.313,0,0.566,0.254,0.566,0.563l0,9.451c0,0.313,-0.256,0.563,-0.566,0.563l-5.779,0c-0.313,0,-0.566,-0.254,-0.566,-0.563l0,-9.447c0,-0.313,0.254,-0.567,0.566,-0.567L90.732,-159.122L90.732,-159.122zM90.732,-171.467c0.313,0,0.566,0.255,0.566,0.565l0,9.449c0,0.313,-0.256,0.564,-0.566,0.564l-5.779,0c-0.313,0,-0.566,-0.256,-0.566,-0.564l0,-9.449c0,-0.313,0.254,-0.565,0.566,-0.565L90.732,-171.467z"/>
             </g>
             <line  opacity="0.77" fill="none" stroke="#353535" stroke-linecap="round" enable-background="new    " y1="-149.106" stroke-width="0.2" x1="84.273" y2="-158.693" x2="84.273"/>
             <line  opacity="0.77" fill="none" stroke="#353535" stroke-linecap="round" enable-background="new    " y1="-161.452" stroke-width="0.2" x1="84.273" y2="-171.038" x2="84.273"/>
            </g>
           </g>
          </g>
         </g>
        </g>
       </g>
      </g>
     </g>
     <g transform="matrix(1, 0, 0, 1, 157.652, 140.628)">
      <g  id="_x30_.1.1">
       <g  id="_x31_x06">
        <rect  width="43.198" x="-1.821" y="-0.228" fill="#404040" height="7.199" id="_x30_.1.1.0.0"/>
        <rect  width="2.78" x="0.388" y="1.981" height="2.783" id="_x30_.1.1.0.1"/>
        <polygon  fill="#2A2A29" points="-0.639,0.956,0.386,1.981,3.17,1.981,4.193,0.956" id="_x30_.1.1.0.2"/>
        <polygon  fill="#474747" points="4.193,0.956,3.17,1.985,3.17,4.766,4.193,5.788" id="_x30_.1.1.0.3"/>
        <polygon  fill="#595959" points="4.193,5.788,3.168,4.766,0.386,4.766,-0.639,5.788" id="_x30_.1.1.0.4"/>
        <polygon  fill="#373737" points="-0.642,5.788,0.386,4.764,0.386,1.981,-0.642,0.956" id="_x30_.1.1.0.5"/>
        <rect  width="2.78" x="7.589" y="1.981" height="2.783" id="_x30_.1.1.0.6"/>
        <polygon  fill="#2A2A29" points="6.56,0.956,7.586,1.981,10.367,1.981,11.393,0.956" id="_x30_.1.1.0.7"/>
        <polygon  fill="#474747" points="11.393,0.956,10.367,1.985,10.367,4.766,11.393,5.788" id="_x30_.1.1.0.8"/>
        <polygon  fill="#595959" points="11.393,5.788,10.367,4.766,7.586,4.766,6.56,5.788" id="_x30_.1.1.0.9"/>
        <polygon  fill="#373737" points="6.56,5.788,7.586,4.764,7.586,1.981,6.56,0.956" id="_x30_.1.1.0.10"/>
        <rect  width="2.781" x="14.787" y="1.981" height="2.783" id="_x30_.1.1.0.11"/>
        <polygon  fill="#2A2A29" points="13.763,0.956,14.785,1.981,17.568,1.981,18.595,0.956" id="_x30_.1.1.0.12"/>
        <polygon  fill="#474747" points="18.595,0.956,17.568,1.985,17.568,4.766,18.595,5.788" id="_x30_.1.1.0.13"/>
        <polygon  fill="#595959" points="18.595,5.788,17.568,4.766,14.785,4.766,13.763,5.788" id="_x30_.1.1.0.14"/>
        <polygon  fill="#373737" points="13.761,5.788,14.785,4.764,14.785,1.981,13.761,0.956" id="_x30_.1.1.0.15"/>
        <rect  width="2.78" x="21.988" y="1.981" height="2.783" id="_x30_.1.1.0.16"/>
        <polygon  fill="#2A2A29" points="20.964,0.956,21.986,1.981,24.768,1.981,25.795,0.956" id="_x30_.1.1.0.17"/>
        <polygon  fill="#474747" points="25.795,0.956,24.768,1.985,24.768,4.766,25.795,5.788" id="_x30_.1.1.0.18"/>
        <polygon  fill="#595959" points="25.793,5.788,24.768,4.766,21.986,4.766,20.964,5.788" id="_x30_.1.1.0.19"/>
        <polygon  fill="#373737" points="20.959,5.788,21.986,4.764,21.986,1.981,20.959,0.956" id="_x30_.1.1.0.20"/>
        <rect  width="2.779" x="29.186" y="1.981" height="2.783" id="_x30_.1.1.0.21"/>
        <polygon  fill="#2A2A29" points="28.162,0.956,29.185,1.981,31.97,1.981,32.994,0.956" id="_x30_.1.1.0.22"/>
        <polygon  fill="#474747" points="32.994,0.956,31.97,1.985,31.97,4.766,32.994,5.788" id="_x30_.1.1.0.23"/>
        <polygon  fill="#595959" points="32.992,5.788,31.97,4.766,29.185,4.766,28.162,5.788" id="_x30_.1.1.0.24"/>
        <polygon  fill="#373737" points="28.16,5.788,29.185,4.764,29.185,1.981,28.16,0.956" id="_x30_.1.1.0.25"/>
        <rect  width="2.78" x="36.388" y="1.981" height="2.783" id="_x30_.1.1.0.26"/>
        <polygon  fill="#2A2A29" points="35.361,0.956,36.386,1.981,39.17,1.981,40.193,0.956" id="_x30_.1.1.0.27"/>
        <polygon  fill="#474747" points="40.193,0.956,39.17,1.985,39.17,4.766,40.193,5.788" id="_x30_.1.1.0.28"/>
        <polygon  fill="#595959" points="40.193,5.788,39.168,4.766,36.386,4.766,35.361,5.788" id="_x30_.1.1.0.29"/>
        <polygon  fill="#373737" points="35.358,5.788,36.386,4.764,36.386,1.981,35.358,0.956" id="_x30_.1.1.0.30"/>
       </g>
      </g>
     </g>
     <g transform="matrix(1, 0, 0, 1, 144.692, 3.372)">
      <g  id="_x30_.1.4">
       <g  id="_x31_x08">
        <g transform="matrix(-1, 0, 0, -1, 57.6, 7.2)">
         <g  id="_x30_.1.4.0.0">
          <g  id="_x30_.1.4.0.0.0">
           <rect  width="57.6" x="3.264" y="-0.228" fill="#404040" height="7.199" id="_x30_.1.4.0.0.0.0"/>
           <rect  width="2.78" x="55.873" y="1.98" height="2.782" id="_x30_.1.4.0.0.0.1"/>
           <polygon  fill="#2A2A29" points="59.679,5.787,58.657,4.762,55.873,4.762,54.847,5.787" id="_x30_.1.4.0.0.0.2"/>
           <polygon  fill="#474747" points="54.847,5.787,55.873,4.759,55.873,1.978,54.847,0.955" id="_x30_.1.4.0.0.0.3"/>
           <polygon  fill="#595959" points="54.848,0.955,55.873,1.978,58.657,1.978,59.679,0.955" id="_x30_.1.4.0.0.0.4"/>
           <polygon  fill="#373737" points="59.681,0.955,58.657,1.98,58.657,4.762,59.681,5.787" id="_x30_.1.4.0.0.0.5"/>
           <rect  width="2.779" x="48.672" y="1.98" height="2.782" id="_x30_.1.4.0.0.0.6"/>
           <polygon  fill="#2A2A29" points="52.481,5.787,51.456,4.762,48.67,4.762,47.647,5.787" id="_x30_.1.4.0.0.0.7"/>
           <polygon  fill="#474747" points="47.647,5.787,48.67,4.759,48.67,1.978,47.647,0.955" id="_x30_.1.4.0.0.0.8"/>
           <polygon  fill="#595959" points="47.649,0.955,48.672,1.978,51.456,1.978,52.481,0.955" id="_x30_.1.4.0.0.0.9"/>
           <polygon  fill="#373737" points="52.483,0.955,51.456,1.98,51.456,4.762,52.483,5.787" id="_x30_.1.4.0.0.0.10"/>
           <rect  width="2.78" x="41.472" y="1.98" height="2.782" id="_x30_.1.4.0.0.0.11"/>
           <polygon  fill="#2A2A29" points="45.28,5.787,44.254,4.762,41.472,4.762,40.448,5.787" id="_x30_.1.4.0.0.0.12"/>
           <polygon  fill="#474747" points="40.448,5.787,41.472,4.759,41.472,1.978,40.448,0.955" id="_x30_.1.4.0.0.0.13"/>
           <polygon  fill="#595959" points="40.452,0.955,41.473,1.978,44.254,1.978,45.28,0.955" id="_x30_.1.4.0.0.0.14"/>
           <polygon  fill="#373737" points="45.282,0.955,44.254,1.98,44.254,4.762,45.282,5.787" id="_x30_.1.4.0.0.0.15"/>
           <rect  width="2.779" x="34.272" y="1.98" height="2.782" id="_x30_.1.4.0.0.0.16"/>
           <polygon  fill="#2A2A29" points="38.081,5.787,37.054,4.762,34.272,4.762,33.248,5.787" id="_x30_.1.4.0.0.0.17"/>
           <polygon  fill="#474747" points="33.248,5.787,34.272,4.759,34.272,1.978,33.248,0.955" id="_x30_.1.4.0.0.0.18"/>
           <polygon  fill="#595959" points="33.248,0.955,34.274,1.978,37.054,1.978,38.081,0.955" id="_x30_.1.4.0.0.0.19"/>
           <polygon  fill="#373737" points="38.082,0.955,37.054,1.98,37.054,4.762,38.082,5.787" id="_x30_.1.4.0.0.0.20"/>
           <rect  width="2.781" x="27.073" y="1.98" height="2.782" id="_x30_.1.4.0.0.0.21"/>
           <polygon  fill="#2A2A29" points="30.877,5.787,29.856,4.762,27.073,4.762,26.045,5.787" id="_x30_.1.4.0.0.0.22"/>
           <polygon  fill="#474747" points="26.045,5.787,27.073,4.759,27.073,1.978,26.045,0.955" id="_x30_.1.4.0.0.0.23"/>
           <polygon  fill="#595959" points="26.047,0.955,27.077,1.978,29.856,1.978,30.877,0.955" id="_x30_.1.4.0.0.0.24"/>
           <polygon  fill="#373737" points="30.879,0.955,29.856,1.98,29.856,4.762,30.879,5.787" id="_x30_.1.4.0.0.0.25"/>
           <rect  width="2.78" x="19.873" y="1.98" height="2.782" id="_x30_.1.4.0.0.0.26"/>
           <polygon  fill="#2A2A29" points="23.679,5.787,22.657,4.762,19.873,4.762,18.847,5.787" id="_x30_.1.4.0.0.0.27"/>
           <polygon  fill="#474747" points="18.847,5.787,19.873,4.759,19.873,1.978,18.847,0.955" id="_x30_.1.4.0.0.0.28"/>
           <polygon  fill="#595959" points="18.848,0.955,19.873,1.978,22.657,1.978,23.679,0.955" id="_x30_.1.4.0.0.0.29"/>
           <polygon  fill="#373737" points="23.681,0.955,22.657,1.98,22.657,4.762,23.681,5.787" id="_x30_.1.4.0.0.0.30"/>
           <rect  width="2.779" x="12.672" y="1.98" height="2.782" id="_x30_.1.4.0.0.0.31"/>
           <polygon  fill="#2A2A29" points="16.481,5.787,15.456,4.762,12.67,4.762,11.647,5.787" id="_x30_.1.4.0.0.0.32"/>
           <polygon  fill="#474747" points="11.647,5.787,12.67,4.759,12.67,1.978,11.647,0.955" id="_x30_.1.4.0.0.0.33"/>
           <polygon  fill="#595959" points="11.649,0.955,12.672,1.978,15.456,1.978,16.481,0.955" id="_x30_.1.4.0.0.0.34"/>
           <polygon  fill="#373737" points="16.483,0.955,15.456,1.98,15.456,4.762,16.483,5.787" id="_x30_.1.4.0.0.0.35"/>
           <rect  width="2.78" x="5.472" y="1.98" height="2.782" id="_x30_.1.4.0.0.0.36"/>
           <polygon  fill="#2A2A29" points="9.28,5.787,8.254,4.762,5.472,4.762,4.448,5.787" id="_x30_.1.4.0.0.0.37"/>
           <polygon  fill="#474747" points="4.448,5.787,5.472,4.759,5.472,1.978,4.448,0.955" id="_x30_.1.4.0.0.0.38"/>
           <polygon  fill="#595959" points="4.452,0.955,5.473,1.978,8.254,1.978,9.28,0.955" id="_x30_.1.4.0.0.0.39"/>
           <polygon  fill="#373737" points="9.282,0.955,8.254,1.98,8.254,4.762,9.282,5.787" id="_x30_.1.4.0.0.0.40"/>
          </g>
         </g>
        </g>
       </g>
      </g>
     </g>
     <g transform="matrix(1, 0, 0, 1, 92.8519, 140.628)">
      <g  id="_x30_.1.9">
       <g  id="_x31_x08_1_">
        <rect  width="57.602" x="-1.824" y="-0.228" fill="#404040" height="7.199" id="_x30_.1.9.0.0"/>
        <rect  width="2.781" x="0.386" y="1.981" height="2.783" id="_x30_.1.9.0.1"/>
        <polygon  fill="#2A2A29" points="-0.639,0.956,0.384,1.981,3.167,1.981,4.193,0.956" id="_x30_.1.9.0.2"/>
        <polygon  fill="#474747" points="4.193,0.956,3.167,1.985,3.167,4.766,4.193,5.788" id="_x30_.1.9.0.3"/>
        <polygon  fill="#595959" points="4.192,5.788,3.166,4.766,0.384,4.766,-0.639,5.788" id="_x30_.1.9.0.4"/>
        <polygon  fill="#373737" points="-0.641,5.788,0.384,4.764,0.384,1.981,-0.641,0.956" id="_x30_.1.9.0.5"/>
        <rect  width="2.78" x="7.586" y="1.981" height="2.783" id="_x30_.1.9.0.6"/>
        <polygon  fill="#2A2A29" points="6.56,0.956,7.584,1.981,10.368,1.981,11.394,0.956" id="_x30_.1.9.0.7"/>
        <polygon  fill="#474747" points="11.394,0.956,10.368,1.985,10.368,4.766,11.394,5.788" id="_x30_.1.9.0.8"/>
        <polygon  fill="#595959" points="11.392,5.788,10.366,4.766,7.584,4.766,6.56,5.788" id="_x30_.1.9.0.9"/>
        <polygon  fill="#373737" points="6.558,5.788,7.584,4.764,7.584,1.981,6.558,0.956" id="_x30_.1.9.0.10"/>
        <rect  width="2.779" x="14.787" y="1.981" height="2.783" id="_x30_.1.9.0.11"/>
        <polygon  fill="#2A2A29" points="13.76,0.956,14.783,1.981,17.569,1.981,18.592,0.956" id="_x30_.1.9.0.12"/>
        <polygon  fill="#474747" points="18.592,0.956,17.569,1.985,17.569,4.766,18.592,5.788" id="_x30_.1.9.0.13"/>
        <polygon  fill="#595959" points="18.591,5.788,17.567,4.766,14.783,4.766,13.76,5.788" id="_x30_.1.9.0.14"/>
        <polygon  fill="#373737" points="13.758,5.788,14.783,4.764,14.783,1.981,13.758,0.956" id="_x30_.1.9.0.15"/>
        <rect  width="2.781" x="21.987" y="1.981" height="2.783" id="_x30_.1.9.0.16"/>
        <polygon  fill="#2A2A29" points="20.959,0.956,21.985,1.981,24.77,1.981,25.791,0.956" id="_x30_.1.9.0.17"/>
        <polygon  fill="#474747" points="25.791,0.956,24.77,1.985,24.77,4.766,25.791,5.788" id="_x30_.1.9.0.18"/>
        <polygon  fill="#595959" points="25.791,5.788,24.768,4.766,21.985,4.766,20.959,5.788" id="_x30_.1.9.0.19"/>
        <polygon  fill="#373737" points="20.957,5.788,21.985,4.764,21.985,1.981,20.957,0.956" id="_x30_.1.9.0.20"/>
        <rect  width="2.779" x="29.188" y="1.981" height="2.783" id="_x30_.1.9.0.21"/>
        <polygon  fill="#2A2A29" points="28.158,0.956,29.186,1.981,31.967,1.981,32.99,0.956" id="_x30_.1.9.0.22"/>
        <polygon  fill="#474747" points="32.99,0.956,31.967,1.985,31.967,4.766,32.99,5.788" id="_x30_.1.9.0.23"/>
        <polygon  fill="#595959" points="32.99,5.788,31.966,4.766,29.186,4.766,28.158,5.788" id="_x30_.1.9.0.24"/>
        <polygon  fill="#373737" points="28.156,5.788,29.186,4.764,29.186,1.981,28.156,0.956" id="_x30_.1.9.0.25"/>
        <rect  width="2.78" x="36.386" y="1.981" height="2.783" id="_x30_.1.9.0.26"/>
        <polygon  fill="#2A2A29" points="35.362,0.956,36.384,1.981,39.166,1.981,40.194,0.956" id="_x30_.1.9.0.27"/>
        <polygon  fill="#474747" points="40.194,0.956,39.166,1.985,39.166,4.766,40.194,5.788" id="_x30_.1.9.0.28"/>
        <polygon  fill="#595959" points="40.192,5.788,39.166,4.766,36.384,4.766,35.362,5.788" id="_x30_.1.9.0.29"/>
        <polygon  fill="#373737" points="35.36,5.788,36.384,4.764,36.384,1.981,35.36,0.956" id="_x30_.1.9.0.30"/>
        <rect  width="2.779" x="43.586" y="1.981" height="2.783" id="_x30_.1.9.0.31"/>
        <polygon  fill="#2A2A29" points="42.561,0.956,43.584,1.981,46.365,1.981,47.395,0.956" id="_x30_.1.9.0.32"/>
        <polygon  fill="#474747" points="47.395,0.956,46.365,1.985,46.365,4.766,47.395,5.788" id="_x30_.1.9.0.33"/>
        <polygon  fill="#595959" points="47.393,5.788,46.365,4.766,43.584,4.766,42.561,5.788" id="_x30_.1.9.0.34"/>
        <polygon  fill="#373737" points="42.558,5.788,43.584,4.764,43.584,1.981,42.558,0.956" id="_x30_.1.9.0.35"/>
        <rect  width="2.779" x="50.787" y="1.981" height="2.783" id="_x30_.1.9.0.36"/>
        <polygon  fill="#2A2A29" points="49.76,0.956,50.783,1.981,53.569,1.981,54.592,0.956" id="_x30_.1.9.0.37"/>
        <polygon  fill="#474747" points="54.592,0.956,53.569,1.985,53.569,4.766,54.592,5.788" id="_x30_.1.9.0.38"/>
        <polygon  fill="#595959" points="54.591,5.788,53.567,4.766,50.783,4.766,49.76,5.788" id="_x30_.1.9.0.39"/>
        <polygon  fill="#373737" points="49.758,5.788,50.783,4.764,50.783,1.981,49.758,0.956" id="_x30_.1.9.0.40"/>
       </g>
      </g>
     </g>
     <g transform="matrix(1, 0, 0, 1, 67.6403, 3.60123)">
      <g  id="_x30_.1.17">
       <g  id="_x31_x10">
        <rect  width="72" x="-2.593" y="-0.001" fill="#404040" height="7.199" id="_x30_.1.17.0.0"/>
        <rect  width="2.779" x="-0.382" y="2.208" height="2.782" id="_x30_.1.17.0.1"/>
        <polygon  fill="#2A2A29" points="-1.407,1.183,-0.384,2.208,2.399,2.208,3.425,1.183" id="_x30_.1.17.0.2"/>
        <polygon  fill="#474747" points="3.425,1.183,2.399,2.211,2.399,4.992,3.425,6.015" id="_x30_.1.17.0.3"/>
        <polygon  fill="#595959" points="3.425,6.015,2.399,4.992,-0.384,4.992,-1.407,6.015" id="_x30_.1.17.0.4"/>
        <polygon  fill="#373737" points="-1.409,6.015,-0.384,4.99,-0.384,2.208,-1.409,1.183" id="_x30_.1.17.0.5"/>
        <rect  width="2.781" x="6.819" y="2.208" height="2.782" id="_x30_.1.17.0.6"/>
        <polygon  fill="#2A2A29" points="5.792,1.183,6.815,2.208,9.598,2.208,10.624,1.183" id="_x30_.1.17.0.7"/>
        <polygon  fill="#474747" points="10.624,1.183,9.598,2.211,9.598,4.992,10.624,6.015" id="_x30_.1.17.0.8"/>
        <polygon  fill="#595959" points="10.624,6.015,9.596,4.992,6.815,4.992,5.792,6.015" id="_x30_.1.17.0.9"/>
        <polygon  fill="#373737" points="5.79,6.015,6.815,4.99,6.815,2.208,5.79,1.183" id="_x30_.1.17.0.10"/>
        <rect  width="2.779" x="14.018" y="2.208" height="2.782" id="_x30_.1.17.0.11"/>
        <polygon  fill="#2A2A29" points="12.991,1.183,14.014,2.208,16.8,2.208,17.825,1.183" id="_x30_.1.17.0.12"/>
        <polygon  fill="#474747" points="17.825,1.183,16.8,2.211,16.8,4.992,17.825,6.015" id="_x30_.1.17.0.13"/>
        <polygon  fill="#595959" points="17.823,6.015,16.8,4.992,14.014,4.992,12.991,6.015" id="_x30_.1.17.0.14"/>
        <polygon  fill="#373737" points="12.991,6.015,14.014,4.99,14.014,2.208,12.991,1.183" id="_x30_.1.17.0.15"/>
        <rect  width="2.781" x="21.219" y="2.208" height="2.782" id="_x30_.1.17.0.16"/>
        <polygon  fill="#2A2A29" points="20.192,1.183,21.218,2.208,24.001,2.208,25.024,1.183" id="_x30_.1.17.0.17"/>
        <polygon  fill="#474747" points="25.024,1.183,24.001,2.211,24.001,4.992,25.024,6.015" id="_x30_.1.17.0.18"/>
        <polygon  fill="#595959" points="25.024,6.015,23.999,4.992,21.218,4.992,20.192,6.015" id="_x30_.1.17.0.19"/>
        <polygon  fill="#373737" points="20.19,6.015,21.218,4.99,21.218,2.208,20.19,1.183" id="_x30_.1.17.0.20"/>
        <rect  width="2.779" x="28.419" y="2.208" height="2.782" id="_x30_.1.17.0.21"/>
        <polygon  fill="#2A2A29" points="27.391,1.183,28.417,2.208,31.2,2.208,32.223,1.183" id="_x30_.1.17.0.22"/>
        <polygon  fill="#474747" points="32.223,1.183,31.2,2.211,31.2,4.992,32.223,6.015" id="_x30_.1.17.0.23"/>
        <polygon  fill="#595959" points="32.221,6.015,31.198,4.992,28.417,4.992,27.391,6.015" id="_x30_.1.17.0.24"/>
        <polygon  fill="#373737" points="27.389,6.015,28.417,4.99,28.417,2.208,27.389,1.183" id="_x30_.1.17.0.25"/>
        <rect  width="2.779" x="35.62" y="2.208" height="2.782" id="_x30_.1.17.0.26"/>
        <polygon  fill="#2A2A29" points="34.593,1.183,35.616,2.208,38.399,2.208,39.427,1.183" id="_x30_.1.17.0.27"/>
        <polygon  fill="#474747" points="39.427,1.183,38.399,2.211,38.399,4.992,39.427,6.015" id="_x30_.1.17.0.28"/>
        <polygon  fill="#595959" points="39.427,6.015,38.395,4.992,35.616,4.992,34.593,6.015" id="_x30_.1.17.0.29"/>
        <polygon  fill="#373737" points="34.591,6.015,35.616,4.99,35.616,2.208,34.591,1.183" id="_x30_.1.17.0.30"/>
        <rect  width="2.779" x="42.817" y="2.208" height="2.782" id="_x30_.1.17.0.31"/>
        <polygon  fill="#2A2A29" points="41.795,1.183,42.815,2.208,45.599,2.208,46.626,1.183" id="_x30_.1.17.0.32"/>
        <polygon  fill="#474747" points="46.626,1.183,45.599,2.211,45.599,4.992,46.626,6.015" id="_x30_.1.17.0.33"/>
        <polygon  fill="#595959" points="46.624,6.015,45.597,4.992,42.815,4.992,41.795,6.015" id="_x30_.1.17.0.34"/>
        <polygon  fill="#373737" points="41.792,6.015,42.815,4.99,42.815,2.208,41.792,1.183" id="_x30_.1.17.0.35"/>
        <rect  width="2.779" x="50.017" y="2.208" height="2.782" id="_x30_.1.17.0.36"/>
        <polygon  fill="#2A2A29" points="48.991,1.183,50.015,2.208,52.802,2.208,53.823,1.183" id="_x30_.1.17.0.37"/>
        <polygon  fill="#474747" points="53.823,1.183,52.802,2.211,52.802,4.992,53.823,6.015" id="_x30_.1.17.0.38"/>
        <polygon  fill="#595959" points="53.823,6.015,52.802,4.992,50.015,4.992,48.991,6.015" id="_x30_.1.17.0.39"/>
        <polygon  fill="#373737" points="48.989,6.015,50.015,4.99,50.015,2.208,48.989,1.183" id="_x30_.1.17.0.40"/>
        <rect  width="2.778" x="57.22" y="2.208" height="2.782" id="_x30_.1.17.0.41"/>
        <polygon  fill="#2A2A29" points="56.192,1.183,57.22,2.208,60.002,2.208,61.024,1.183" id="_x30_.1.17.0.42"/>
        <polygon  fill="#474747" points="61.024,1.183,60.002,2.211,60.002,4.992,61.024,6.015" id="_x30_.1.17.0.43"/>
        <polygon  fill="#595959" points="61.02,6.015,59.999,4.992,57.22,4.992,56.192,6.015" id="_x30_.1.17.0.44"/>
        <polygon  fill="#373737" points="56.19,6.015,57.22,4.99,57.22,2.208,56.19,1.183" id="_x30_.1.17.0.45"/>
        <rect  width="2.777" x="64.421" y="2.208" height="2.782" id="_x30_.1.17.0.46"/>
        <polygon  fill="#2A2A29" points="63.392,1.183,64.417,2.208,67.198,2.208,68.224,1.183" id="_x30_.1.17.0.47"/>
        <polygon  fill="#474747" points="68.224,1.183,67.198,2.211,67.198,4.992,68.224,6.015" id="_x30_.1.17.0.48"/>
        <polygon  fill="#595959" points="68.222,6.015,67.198,4.992,64.417,4.992,63.392,6.015" id="_x30_.1.17.0.49"/>
        <polygon  fill="#373737" points="63.39,6.015,64.417,4.99,64.417,2.208,63.39,1.183" id="_x30_.1.17.0.50"/>
       </g>
      </g>
     </g>
     <g transform="matrix(1, 0, 0, 1, 8.7817, 8.95615)">
      <g  id="_x30_.1.15">
       <g  id="smd_157sw">
        <g transform="matrix(0, -1, 1, 0, 0.777996, 13.82)">
         <g  id="_x30_.1.15.0.0">
          <g  id="_x30_.1.15.0.0.0">
           <polygon  fill="#CCCCCC" points="-34.509,180.854,-34.509,180.486,-26.244,180.486,-26.244,180.854,-19.999,180.854,-19.999,164.874,-40.756,164.874,-40.756,180.854" id="_x30_.1.15.0.0.0.0"/>
           <polygon  fill="#CCCCCC" points="-26.244,162.315,-26.244,162.683,-34.509,162.683,-34.509,162.315,-40.756,162.315,-40.756,178.174,-19.999,178.174,-19.999,162.315" id="_x30_.1.15.0.0.0.1"/>
           <circle  fill="#641D1C" cx="-30.376" cy="171.586" id="_x30_.1.15.0.0.0.2" r="5.117"/>
           <path  opacity="0.2" id="_x30_.1.15.0.0.0.3" enable-background="new    " d="M-25.261,171.335c0,-2.826,-2.289,-5.117,-5.114,-5.117c-2.826,0,-5.119,2.289,-5.119,5.117l0,0.25c0,-2.827,2.291,-5.118,5.119,-5.118c2.825,0,5.114,2.291,5.114,5.118L-25.261,171.335z"/>
           <circle  fill="#852725" cx="-30.376" cy="171.585" id="_x30_.1.15.0.0.0.4" r="4.93"/>
           <circle  fill="#852725" cx="-30.376" cy="171.702" id="_x30_.1.15.0.0.0.5" r="4.929"/>
           <g  id="_x30_.1.15.0.0.0.6">
            <path  opacity="0.1" id="_x30_.1.15.0.0.0.6.0" enable-background="new    " d="M-30.259,176.514c2.724,0,4.931,-2.206,4.931,-4.931s-2.207,-4.93,-4.931,-4.93l-0.233,0c2.725,0,4.932,2.209,4.932,4.93c0,2.725,-2.207,4.931,-4.932,4.931L-30.259,176.514z"/>
           </g>
           <g transform="matrix(-2.54711e-06, -1, 1, -2.54711e-06, 3.4298, 39.7056)">
            <g  id="_x30_.1.15.0.0.0.10">
             <rect  width="0.368" x="-122.988" opacity="0.2" y="-44.188" height="6.248" id="_x30_.1.15.0.0.0.10.0" enable-background="new    "/>
            </g>
           </g>
           <g transform="matrix(-2.54711e-06, -1, 1, -2.54711e-06, -11.0816, 54.2142)">
            <g  id="_x30_.1.15.0.0.0.11">
             <rect  width="0.367" x="-108.482" opacity="0.2" y="-15.163" height="6.244" id="_x30_.1.15.0.0.0.11.0" enable-background="new    "/>
            </g>
           </g>
           <g transform="matrix(-2.54711e-06, -1, 1, -2.54711e-06, -4.1966, 46.5918)">
            <g  id="_x30_.1.15.0.0.0.12">
             <rect  width="0.369" x="-116.473" opacity="0.2" y="-30.313" height="8.267" id="_x30_.1.15.0.0.0.12.0" enable-background="new    "/>
            </g>
           </g>
          </g>
         </g>
        </g>
        <g  id="_x30_.1.15.0.1">
         <rect  width="2.252" x="177.361" y="31.047" fill="#E6E6E6" height="2.75" id="_x30_.1.15.0.1.0"/>
         <rect  width="2.252" x="165.111" y="31.047" fill="#E6E6E6" height="2.75" id="_x30_.1.15.0.1.1"/>
         <rect  width="3.416" x="170.57" y="54.422" fill="#E6E6E6" height="2.75" id="_x30_.1.15.0.1.2"/>
         <rect  width="2.252" x="177.361" y="54.422" fill="#E6E6E6" height="2.75" id="_x30_.1.15.0.1.3"/>
         <rect  width="2.252" x="165.111" y="54.422" fill="#E6E6E6" height="2.75" id="_x30_.1.15.0.1.4"/>
         <rect  width="2.252" x="177.344" opacity="0.2" y="31.002" height="0.104" id="_x30_.1.15.0.1.8" enable-background="new    "/>
         <rect  width="2.253" x="165.093" opacity="0.2" y="31.002" height="0.104" id="_x30_.1.15.0.1.9" enable-background="new    "/>
         <rect  width="2.251" x="177.375" opacity="0.1" y="33.446" height="0.334" id="_x30_.1.15.0.1.10" enable-background="new    "/>
         <rect  width="2.252" x="165.124" opacity="0.1" y="33.446" height="0.334" id="_x30_.1.15.0.1.11" enable-background="new    "/>
        </g>
       </g>
      </g>
     </g>
     <rect  width="28.678" x="101.623" y="74.6" fill="#1A1A1A" height="27.801"/>
     <g  id="_x30_.1.0.1">
      <title  id="0.1.0.1.0">layer 21</title>
      <g  id="_x30_.1.0.1.2">
       <title  id="0.1.0.1.2.0">text:MADE IN</title>
      </g>
      <g  id="_x30_.1.0.1.3">
       <title  id="0.1.0.1.3.0">text:ITALY</title>
      </g>
      <g  id="_x30_.1.0.1.4">
       <title  id="0.1.0.1.4.0">text:Prototype</title>
      </g>
      <g  id="_x30_.1.0.1.5">
       <title  id="0.1.0.1.5.0">text:Limited</title>
      </g>
      <g  id="_x30_.1.0.1.6">
       <title  id="0.1.0.1.6.0">text:Edition</title>
      </g>
      <g  id="_x30_.1.0.1.7">
       <g  id="_x30_.1.0.1.7.0">
        <g transform="matrix(1, 0, 0, 1, 102.569, 12.24)">
         <g  id="_x30_.1.0.1.7.0.0">
          <g  id="_x30_.1.0.1.7.0.0.0">
           <g transform="rotate(-90)">
            <g  id="_x30_.1.0.1.7.0.0.0.0">
             <g  id="_x30_.1.0.1.7.0.0.0.0.0">
              <g transform="matrix(1, 0, 0, 1, -5.1472, -0.9391)">
               <g  id="_x30_.1.0.1.7.0.0.0.0.0.0">
                <g transform="matrix(1, 0, 0, 1, -0.4473, -2.6767)">
                 <text  fill="#FFFFFF" font-family="'OCRA'" id="_x30_.1.0.1.7.0.0.0.0.0.0.0" font-size="3.75">13</text>
                </g>
               </g>
              </g>
             </g>
            </g>
           </g>
          </g>
         </g>
        </g>
       </g>
      </g>
      <g  id="_x30_.1.0.1.8">
       <g  id="_x30_.1.0.1.8.0">
        <g transform="matrix(1, 0, 0, 1, 109.769, 12.24)">
         <g  id="_x30_.1.0.1.8.0.0">
          <g  id="_x30_.1.0.1.8.0.0.0">
           <g transform="rotate(-90)">
            <g  id="_x30_.1.0.1.8.0.0.0.0">
             <g  id="_x30_.1.0.1.8.0.0.0.0.0">
              <g transform="matrix(1, 0, 0, 1, -5.1472, -0.9384)">
               <g  id="_x30_.1.0.1.8.0.0.0.0.0.0">
                <g transform="matrix(1, 0, 0, 1, -0.4473, -2.6758)">
                 <text  fill="#FFFFFF" font-family="'OCRA'" id="_x30_.1.0.1.8.0.0.0.0.0.0.0" font-size="3.75">12</text>
                </g>
               </g>
              </g>
             </g>
            </g>
           </g>
          </g>
         </g>
        </g>
       </g>
      </g>
      <g  id="_x30_.1.0.1.9">
       <g  id="_x30_.1.0.1.9.0">
        <g transform="matrix(1, 0, 0, 1, 116.969, 12.24)">
         <g  id="_x30_.1.0.1.9.0.0">
          <g  id="_x30_.1.0.1.9.0.0.0">
           <g transform="rotate(-90)">
            <g  id="_x30_.1.0.1.9.0.0.0.0">
             <g  id="_x30_.1.0.1.9.0.0.0.0.0">
              <g transform="matrix(1, 0, 0, 1, -5.1472, -0.9392)">
               <g  id="_x30_.1.0.1.9.0.0.0.0.0.0">
                <g transform="matrix(1, 0, 0, 1, -0.4473, -2.6757)">
                 <text  fill="#FFFFFF" font-family="'OCRA'" id="_x30_.1.0.1.9.0.0.0.0.0.0.0" font-size="3.75">11</text>
                </g>
               </g>
              </g>
             </g>
            </g>
           </g>
          </g>
         </g>
        </g>
       </g>
      </g>
      <g  id="_x30_.1.0.1.10">
       <g  id="_x30_.1.0.1.10.0">
        <g transform="matrix(1, 0, 0, 1, 124.169, 12.24)">
         <g  id="_x30_.1.0.1.10.0.0">
          <g  id="_x30_.1.0.1.10.0.0.0">
           <g transform="rotate(-90)">
            <g  id="_x30_.1.0.1.10.0.0.0.0">
             <g  id="_x30_.1.0.1.10.0.0.0.0.0">
              <g transform="matrix(1, 0, 0, 1, -5.1472, -0.94)">
               <g  id="_x30_.1.0.1.10.0.0.0.0.0.0">
                <g transform="matrix(1, 0, 0, 1, -0.9942, -3.8437)">
                 <text  fill="#FFFFFF" font-family="'OCRA'" id="_x30_.1.0.1.10.0.0.0.0.0.0.0" font-size="2.75">ETH</text>
                </g>
               </g>
              </g>
             </g>
            </g>
           </g>
          </g>
         </g>
        </g>
       </g>
      </g>
      <g  id="_x30_.1.0.1.11">
       <g  id="_x30_.1.0.1.11.0">
        <g transform="matrix(1, 0, 0, 1, 131.369, 12.24)">
         <g  id="_x30_.1.0.1.11.0.0">
          <g  id="_x30_.1.0.1.11.0.0.0">
           <g transform="rotate(-90)">
            <g  id="_x30_.1.0.1.11.0.0.0.0">
             <g  id="_x30_.1.0.1.11.0.0.0.0.0">
              <g transform="matrix(1, 0, 0, 1, -2.4402, -0.9388)">
               <g  id="_x30_.1.0.1.11.0.0.0.0.0.0">
                <g transform="matrix(1, 0, 0, 1, -0.4473, -2.6777)">
                 <text  fill="#FFFFFF" font-family="'OCRA'" id="_x30_.1.0.1.11.0.0.0.0.0.0.0" font-size="3.75">9</text>
                </g>
               </g>
              </g>
             </g>
            </g>
           </g>
          </g>
         </g>
        </g>
       </g>
      </g>
      <g  id="_x30_.1.0.1.12">
       <g  id="_x30_.1.0.1.12.0">
        <g transform="matrix(1, 0, 0, 1, 138.569, 12.24)">
         <g  id="_x30_.1.0.1.12.0.0">
          <g  id="_x30_.1.0.1.12.0.0.0">
           <g transform="rotate(-90)">
            <g  id="_x30_.1.0.1.12.0.0.0.0">
             <g  id="_x30_.1.0.1.12.0.0.0.0.0">
              <g transform="matrix(1, 0, 0, 1, -2.4402, -0.9396)">
               <g  id="_x30_.1.0.1.12.0.0.0.0.0.0">
                <g transform="matrix(1, 0, 0, 1, -0.4473, -2.6777)">
                 <text  fill="#FFFFFF" font-family="'OCRA'" id="_x30_.1.0.1.12.0.0.0.0.0.0.0" font-size="3.75">8</text>
                </g>
               </g>
              </g>
             </g>
            </g>
           </g>
          </g>
         </g>
        </g>
       </g>
      </g>
      <g  id="_x30_.1.0.1.13">
       <g  id="_x30_.1.0.1.13.0">
        <g transform="matrix(1, 0, 0, 1, 150.089, 12.24)">
         <g  id="_x30_.1.0.1.13.0.0">
          <g  id="_x30_.1.0.1.13.0.0.0">
           <g transform="rotate(-90)">
            <g  id="_x30_.1.0.1.13.0.0.0.0">
             <g  id="_x30_.1.0.1.13.0.0.0.0.0">
              <g transform="matrix(1, 0, 0, 1, -2.4402, -0.9401)">
               <g  id="_x30_.1.0.1.13.0.0.0.0.0.0">
                <g transform="matrix(1, 0, 0, 1, -0.4473, -2.6757)">
                 <text  fill="#FFFFFF" font-family="'OCRA'" id="_x30_.1.0.1.13.0.0.0.0.0.0.0" font-size="3.75">7</text>
                </g>
               </g>
              </g>
             </g>
            </g>
           </g>
          </g>
         </g>
        </g>
       </g>
      </g>
      <g  id="_x30_.1.0.1.14">
       <g  id="_x30_.1.0.1.14.0">
        <g transform="matrix(1, 0, 0, 1, 157.289, 12.24)">
         <g  id="_x30_.1.0.1.14.0.0">
          <g  id="_x30_.1.0.1.14.0.0.0">
           <g transform="rotate(-90)">
            <g  id="_x30_.1.0.1.14.0.0.0.0">
             <g  id="_x30_.1.0.1.14.0.0.0.0.0">
              <g transform="matrix(1, 0, 0, 1, -2.4402, -0.9389)">
               <g  id="_x30_.1.0.1.14.0.0.0.0.0.0">
                <g transform="matrix(1, 0, 0, 1, -0.4473, -2.6777)">
                 <text  fill="#FFFFFF" font-family="'OCRA'" id="_x30_.1.0.1.14.0.0.0.0.0.0.0" font-size="3.75">6</text>
                </g>
               </g>
              </g>
             </g>
            </g>
           </g>
          </g>
         </g>
        </g>
       </g>
      </g>
      <g  id="_x30_.1.0.1.15">
       <g  id="_x30_.1.0.1.15.0">
        <g transform="matrix(1, 0, 0, 1, 164.489, 12.24)">
         <g  id="_x30_.1.0.1.15.0.0">
          <g  id="_x30_.1.0.1.15.0.0.0">
           <g transform="rotate(-90)">
            <g  id="_x30_.1.0.1.15.0.0.0.0">
             <g  id="_x30_.1.0.1.15.0.0.0.0.0">
              <g transform="matrix(1, 0, 0, 1, -2.4402, -0.9397)">
               <g  id="_x30_.1.0.1.15.0.0.0.0.0.0">
                <g transform="matrix(1, 0, 0, 1, -0.4473, -2.6777)">
                 <text  fill="#FFFFFF" font-family="'OCRA'" id="_x30_.1.0.1.15.0.0.0.0.0.0.0" font-size="3.75">5</text>
                </g>
               </g>
              </g>
             </g>
            </g>
           </g>
          </g>
         </g>
        </g>
       </g>
      </g>
      <g  id="_x30_.1.0.1.16">
       <g  id="_x30_.1.0.1.16.0">
        <g transform="matrix(1, 0, 0, 1, 171.689, 12.24)">
         <g  id="_x30_.1.0.1.16.0.0">
          <g  id="_x30_.1.0.1.16.0.0.0">
           <g transform="rotate(-90)">
            <g  id="_x30_.1.0.1.16.0.0.0.0">
             <g  id="_x30_.1.0.1.16.0.0.0.0.0">
              <g transform="matrix(1, 0, 0, 1, -2.4402, -0.9405)">
               <g  id="_x30_.1.0.1.16.0.0.0.0.0.0">
                <g transform="matrix(1, 0, 0, 1, -8.5801, -2.6757)">
                 <text  fill="#FFFFFF" font-family="'OCRA'" id="_x30_.1.0.1.16.0.0.0.0.0.0.0" font-size="3.75">SDCS</text>
                </g>
               </g>
              </g>
             </g>
            </g>
           </g>
          </g>
         </g>
        </g>
       </g>
      </g>
      <g  id="_x30_.1.0.1.17">
       <g  id="_x30_.1.0.1.17.0">
        <g transform="matrix(1, 0, 0, 1, 178.889, 12.24)">
         <g  id="_x30_.1.0.1.17.0.0">
          <g  id="_x30_.1.0.1.17.0.0.0">
           <g transform="rotate(-90)">
            <g  id="_x30_.1.0.1.17.0.0.0.0">
             <g  id="_x30_.1.0.1.17.0.0.0.0.0">
              <g transform="matrix(1, 0, 0, 1, -2.4402, -0.9393)">
               <g  id="_x30_.1.0.1.17.0.0.0.0.0.0">
                <g transform="matrix(1, 0, 0, 1, -0.4473, -2.6777)">
                 <text  fill="#FFFFFF" font-family="'OCRA'" id="_x30_.1.0.1.17.0.0.0.0.0.0.0" font-size="3.75">3</text>
                </g>
               </g>
              </g>
             </g>
            </g>
           </g>
          </g>
         </g>
        </g>
       </g>
      </g>
      <g  id="_x30_.1.0.1.18">
       <g  id="_x30_.1.0.1.18.0">
        <g transform="matrix(1, 0, 0, 1, 186.089, 12.24)">
         <g  id="_x30_.1.0.1.18.0.0">
          <g  id="_x30_.1.0.1.18.0.0.0">
           <g transform="rotate(-90)">
            <g  id="_x30_.1.0.1.18.0.0.0.0">
             <g  id="_x30_.1.0.1.18.0.0.0.0.0">
              <g transform="matrix(1, 0, 0, 1, -2.4402, -0.9401)">
               <g  id="_x30_.1.0.1.18.0.0.0.0.0.0">
                <g transform="matrix(1, 0, 0, 1, -0.4473, -2.6757)">
                 <text  fill="#FFFFFF" font-family="'OCRA'" id="_x30_.1.0.1.18.0.0.0.0.0.0.0" font-size="3.75">2</text>
                </g>
               </g>
              </g>
             </g>
            </g>
           </g>
          </g>
         </g>
        </g>
       </g>
      </g>
      <g  id="_x30_.1.0.1.20">
       <title  id="0.1.0.1.20.0">element:C1</title>
       <g  id="_x30_.1.0.1.20.1">
        <title  id="0.1.0.1.20.1.0">package:C0603-ROUND</title>
       </g>
      </g>
      <g  id="_x30_.1.0.1.21">
       <title  id="0.1.0.1.21.0">element:C2</title>
       <g  id="_x30_.1.0.1.21.1">
        <title  id="0.1.0.1.21.1.0">package:C0603-ROUND</title>
       </g>
      </g>
      <g  id="_x30_.1.0.1.22">
       <title  id="0.1.0.1.22.0">element:C3</title>
       <g  id="_x30_.1.0.1.22.1">
        <title  id="0.1.0.1.22.1.0">package:C0603-ROUND</title>
       </g>
      </g>
      <g  id="_x30_.1.0.1.23">
       <title  id="0.1.0.1.23.0">element:C4</title>
       <g  id="_x30_.1.0.1.23.1">
        <title  id="0.1.0.1.23.1.0">package:C0603-ROUND</title>
       </g>
      </g>
      <g  id="_x30_.1.0.1.24">
       <title  id="0.1.0.1.24.0">element:C5</title>
       <g  id="_x30_.1.0.1.24.1">
        <title  id="0.1.0.1.24.1.0">package:C0603-ROUND</title>
       </g>
      </g>
      <g  id="_x30_.1.0.1.25">
       <title  id="0.1.0.1.25.0">element:C6</title>
       <g  id="_x30_.1.0.1.25.1">
        <title  id="0.1.0.1.25.1.0">package:C0603-ROUND</title>
       </g>
      </g>
      <g  id="_x30_.1.0.1.26">
       <title  id="0.1.0.1.26.0">element:C7</title>
       <g  id="_x30_.1.0.1.26.1">
        <title  id="0.1.0.1.26.1.0">package:C0603-ROUND</title>
       </g>
      </g>
      <g  id="_x30_.1.0.1.27">
       <title  id="0.1.0.1.27.0">element:C8</title>
       <g  id="_x30_.1.0.1.27.1">
        <title  id="0.1.0.1.27.1.0">package:C0603-ROUND</title>
       </g>
      </g>
      <g  id="_x30_.1.0.1.28">
       <title  id="0.1.0.1.28.0">element:C9</title>
       <g  id="_x30_.1.0.1.28.1">
        <title  id="0.1.0.1.28.1.0">package:C0603-ROUND</title>
       </g>
      </g>
      <g  id="_x30_.1.0.1.29">
       <title  id="0.1.0.1.29.0">element:C11</title>
       <g  id="_x30_.1.0.1.29.1">
        <title  id="0.1.0.1.29.1.0">package:C0603-ROUND</title>
       </g>
      </g>
      <g  id="_x30_.1.0.1.31">
       <title  id="0.1.0.1.31.0">element:F1</title>
       <g  id="_x30_.1.0.1.31.1">
        <title  id="0.1.0.1.31.1.0">package:L1812</title>
       </g>
      </g>
      <g  id="_x30_.1.0.1.32">
       <title  id="0.1.0.1.32.0">element:FD1</title>
       <g  id="_x30_.1.0.1.32.1">
        <title  id="0.1.0.1.32.1.0">package:FIDUCIA-MOUNT</title>
       </g>
      </g>
      <g  id="_x30_.1.0.1.33">
       <title  id="0.1.0.1.33.0">element:FD2</title>
       <g  id="_x30_.1.0.1.33.1">
        <title  id="0.1.0.1.33.1.0">package:FIDUCIA-MOUNT</title>
       </g>
      </g>
      <g  id="_x30_.1.0.1.34">
       <title  id="0.1.0.1.34.0">element:FD3</title>
       <g  id="_x30_.1.0.1.34.1">
        <title  id="0.1.0.1.34.1.0">package:FIDUCIA-MOUNT</title>
       </g>
      </g>
      <g  id="_x30_.1.0.1.35">
       <title  id="0.1.0.1.35.0">element:GROUND</title>
       <g  id="_x30_.1.0.1.35.1">
        <title  id="0.1.0.1.35.1.0">package:SJ</title>
       </g>
      </g>
      <g  id="_x30_.1.0.1.44">
       <title  id="0.1.0.1.44.0">element:R1</title>
       <g  id="_x30_.1.0.1.44.1">
        <title  id="0.1.0.1.44.1.0">package:R0603-ROUND</title>
       </g>
      </g>
      <g  id="_x30_.1.0.1.45">
       <title  id="0.1.0.1.45.0">element:R2</title>
       <g  id="_x30_.1.0.1.45.1">
        <title  id="0.1.0.1.45.1.0">package:R0603-ROUND</title>
       </g>
      </g>
      <g  id="_x30_.1.0.1.46">
       <title  id="0.1.0.1.46.0">element:RN1</title>
       <g  id="_x30_.1.0.1.46.1">
        <title  id="0.1.0.1.46.1.0">package:CAY16</title>
       </g>
      </g>
      <g  id="_x30_.1.0.1.47">
       <title  id="0.1.0.1.47.0">element:RN2</title>
       <g  id="_x30_.1.0.1.47.1">
        <title  id="0.1.0.1.47.1.0">package:CAY16</title>
       </g>
      </g>
      <g  id="_x30_.1.0.1.48">
       <title  id="0.1.0.1.48.0">element:RN3</title>
       <g  id="_x30_.1.0.1.48.1">
        <title  id="0.1.0.1.48.1.0">package:CAY16</title>
       </g>
      </g>
      <g  id="_x30_.1.0.1.49">
       <title  id="0.1.0.1.49.0">element:RN4</title>
       <g  id="_x30_.1.0.1.49.1">
        <title  id="0.1.0.1.49.1.0">package:CAY16</title>
       </g>
      </g>
      <g  id="_x30_.1.0.1.52">
       <title  id="0.1.0.1.52.0">element:Z1</title>
       <g  id="_x30_.1.0.1.52.1">
        <title  id="0.1.0.1.52.1.0">package:CT/CN0603</title>
       </g>
      </g>
      <g  id="_x30_.1.0.1.53">
       <title  id="0.1.0.1.53.0">element:Z2</title>
       <g  id="_x30_.1.0.1.53.1">
        <title  id="0.1.0.1.53.1.0">package:CT/CN0603</title>
       </g>
      </g>
      <g  id="_x30_.1.0.89">
       <g  id="_x30_.1.0.89.0">
        <g transform="matrix(1, 0, 0, 1, 199.772, 16.2)">
         <g  id="_x30_.1.0.89.0.0">
          <g  id="_x30_.1.0.89.0.0.0">
           <g transform="rotate(270)">
            <g  id="_x30_.1.0.89.0.0.0.0">
             <g  id="_x30_.1.0.89.0.0.0.0.0">
              <g transform="matrix(1, 0, 0, 1, 1.5198, -0.0449)">
               <g  id="_x30_.1.0.89.0.0.0.0.0.0">
                <g transform="matrix(1, 0, 0, 1, -0.4472, -2.6758)">
                 <text  fill="#FFFFFF" font-family="'OCRA'" id="_x30_.1.0.89.0.0.0.0.0.0.0" font-size="3.75">0</text>
                </g>
               </g>
              </g>
             </g>
            </g>
           </g>
          </g>
         </g>
        </g>
       </g>
      </g>
      <g  id="_x30_.1.0.90">
       <g  id="_x30_.1.0.90.0">
        <g transform="matrix(1, 0, 0, 1, 192.572, 16.2)">
         <g  id="_x30_.1.0.90.0.0">
          <g  id="_x30_.1.0.90.0.0.0">
           <g transform="rotate(270)">
            <g  id="_x30_.1.0.90.0.0.0.0">
             <g  id="_x30_.1.0.90.0.0.0.0.0">
              <g transform="matrix(1, 0, 0, 1, 1.5198, -0.0441)">
               <g  id="_x30_.1.0.90.0.0.0.0.0.0">
                <g transform="matrix(1, 0, 0, 1, -0.4472, -2.6758)">
                 <text  fill="#FFFFFF" font-family="'OCRA'" id="_x30_.1.0.90.0.0.0.0.0.0.0" font-size="3.75">1</text>
                </g>
               </g>
              </g>
             </g>
            </g>
           </g>
          </g>
         </g>
        </g>
       </g>
      </g>
      <g  id="_x30_.1.0.91">
       <g  id="_x30_.1.0.91.0">
        <g transform="matrix(1, 0, 0, 1, 192.572, 30.96)">
         <g  id="_x30_.1.0.91.0.0">
          <g  id="_x30_.1.0.91.0.0.0">
           <g transform="rotate(270)">
            <g  id="_x30_.1.0.91.0.0.0.0">
             <g  id="_x30_.1.0.91.0.0.0.0.0">
              <g transform="matrix(1, 0, 0, 1, 3.524, -0.0441)">
               <g  id="_x30_.1.0.91.0.0.0.0.0.0">
                <g transform="matrix(1, 0, 0, 1, 4.6152, -2.6758)">
                 <text  fill="#FFFFFF" font-family="'OCRA'" id="_x30_.1.0.91.0.0.0.0.0.0.0" font-size="3.75">TX</text>
                </g>
               </g>
              </g>
             </g>
            </g>
           </g>
          </g>
         </g>
        </g>
       </g>
      </g>
      <g  id="_x30_.1.0.92">
       <g  id="_x30_.1.0.92.0">
        <g transform="matrix(1, 0, 0, 1, 199.772, 30.96)">
         <g  id="_x30_.1.0.92.0.0">
          <g  id="_x30_.1.0.92.0.0.0">
           <g transform="rotate(270)">
            <g  id="_x30_.1.0.92.0.0.0.0">
             <g  id="_x30_.1.0.92.0.0.0.0.0">
              <g transform="matrix(1, 0, 0, 1, 3.524, -0.0449)">
               <g  id="_x30_.1.0.92.0.0.0.0.0.0">
                <g transform="matrix(1, 0, 0, 1, 4.6152, -2.6758)">
                 <text  fill="#FFFFFF" font-family="'OCRA'" id="_x30_.1.0.92.0.0.0.0.0.0.0" font-size="3.75">RX</text>
                </g>
               </g>
              </g>
             </g>
            </g>
           </g>
          </g>
         </g>
        </g>
       </g>
      </g>
      <g  id="_x30_.1.0.2.4">
       <g  id="_x30_.1.0.2.4.0">
        <g transform="matrix(1, 0, 0, 1, 87.8933, 11.8426)">
         <g  id="_x30_.1.0.2.4.0.0">
          <g  id="_x30_.1.0.2.4.0.0.0">
           <g transform="rotate(-90)">
            <g  id="_x30_.1.0.2.4.0.0.0.0">
             <g  id="_x30_.1.0.2.4.0.0.0.0.0">
              <g transform="matrix(1, 0, 0, 1, -11.0056, -0.9392)">
               <g  id="_x30_.1.0.2.4.0.0.0.0.0.0">
                <g transform="matrix(1, 0, 0, 1, -0.4472, -2.6767)">
                 <text  fill="#FFFFFF" font-family="'OCRA'" id="_x30_.1.0.2.4.0.0.0.0.0.0.0" font-size="3.75">AREF</text>
                </g>
               </g>
              </g>
             </g>
            </g>
           </g>
          </g>
         </g>
        </g>
       </g>
      </g>
      <g  id="_x30_.1.0.2.6">
       <g  id="_x30_.1.0.2.6.0">
        <g transform="matrix(1, 0, 0, 1, 95.4223, 11.9146)">
         <g  id="_x30_.1.0.2.6.0.0">
          <g  id="_x30_.1.0.2.6.0.0.0">
           <g transform="rotate(-90)">
            <g  id="_x30_.1.0.2.6.0.0.0.0">
             <g  id="_x30_.1.0.2.6.0.0.0.0.0">
              <g transform="matrix(1, 0, 0, 1, -8.246, -0.9399)">
               <g  id="_x30_.1.0.2.6.0.0.0.0.0.0">
                <g transform="matrix(1, 0, 0, 1, -0.4473, -2.6767)">
                 <text  fill="#FFFFFF" font-family="'OCRA'" id="_x30_.1.0.2.6.0.0.0.0.0.0.0" font-size="3.75">GND</text>
                </g>
               </g>
              </g>
             </g>
            </g>
           </g>
          </g>
         </g>
        </g>
       </g>
      </g>
     </g>
     <g  id="_x30_.1.0.2">
      <title  id="0.1.0.2.0">layer 25</title>
      <g  id="_x30_.1.0.2.1">
       <g  id="_x30_.1.0.2.1.0">
        <g transform="matrix(0, -1, 1, 0, 127.364, 138.997)">
         <g  id="_x30_.1.0.2.1.0.0">
          <g transform="matrix(1, 0, 0, 1, -0.4473, -2.6758)">
           <text  fill="#FFFFFF" font-family="'OCRA'" id="_x30_.1.0.2.1.0.0.0" font-size="3.3408">5V</text>
          </g>
         </g>
        </g>
       </g>
      </g>
      <g  id="_x30_.1.0.2.2">
       <title  id="0.1.0.2.2.0">text:A0</title>
       <g transform="matrix(-4.37114e-08, -1, 1, -4.37114e-08, 163.219, 138.997)">
        <g  id="_x30_.1.0.2.2.1">
         <g transform="matrix(1, 0, 0, 1, -0.4473, -2.6757)">
          <text  fill="#FFFFFF" font-family="'OCRA'" id="_x30_.1.0.2.2.1.0" font-size="3.3408">A0</text>
         </g>
        </g>
       </g>
      </g>
      <g  id="_x30_.1.0.2.3">
       <g  id="_x30_.1.0.2.3.0">
        <g transform="matrix(1, 0, 0, 1, 175.672, 130.811)">
         <g  id="_x30_.1.0.2.3.0.0">
          <g transform="matrix(1, 0, 0, 1, -2.6768, 0.4473)">
           <text  fill="#FFFFFF" font-family="'OCRA'" id="_x30_.1.0.2.3.0.0.0" font-size="3.6749">ANALOG IN</text>
          </g>
         </g>
        </g>
       </g>
      </g>
      <g  id="_x30_.1.0.2.7">
       <title  id="0.1.0.2.7.0">text:M.Banzi</title>
      </g>
      <g  id="_x30_.1.0.2.8">
       <title  id="0.1.0.2.8.0">text:D.Cuartielles</title>
      </g>
      <g  id="_x30_.1.0.2.9">
       <title  id="0.1.0.2.9.0">text:D.Mellis</title>
      </g>
      <g  id="_x30_.1.0.2.10">
       <g >
        <g transform="matrix(1, 0, 0, 1, 84.5728, 49.3169)">
         <g  id="_x30_.1.0.2.10.1_8_">
          <g transform="matrix(1, 0, 0, 1, -3.6768, -3.2793)">
           <text  fill="#FFFFFF" font-family="'OCRA'" id="_x30_.1.0.2.10.1.0_8_" font-size="2.5">TX</text>
          </g>
         </g>
        </g>
       </g>
      </g>
      <g  id="_x30_.1.0.2.11">
       <g >
        <g transform="matrix(1, 0, 0, 1, 84.6489, 56.1567)">
         <g  id="_x30_.1.0.2.11.1_8_">
          <g transform="matrix(1, 0, 0, 1, -3.6767, -4.7793)">
           <text  fill="#FFFFFF" font-family="'OCRA'" id="_x30_.1.0.2.11.1.0_8_" font-size="2.5">RX</text>
          </g>
         </g>
        </g>
       </g>
      </g>
      <g  id="_x30_.1.0.2.12">
       <title  id="0.1.0.2.12.0">text:G.Martino</title>
      </g>
      <g  id="_x30_.1.0.2.13">
       <title  id="0.1.0.2.13.0">text:T.Igoe</title>
      </g>
      <g  id="_x30_.1.0.2.14">
       <g  id="_x30_.1.0.2.14.0">
        <g transform="matrix(1, 0, 0, 1, 112.292, 138.6)">
         <g  id="_x30_.1.0.2.14.0.0">
          <g  id="_x30_.1.0.2.14.0.0.0">
           <g transform="rotate(270)">
            <g  id="_x30_.1.0.2.14.0.0.0.0">
             <g  id="_x30_.1.0.2.14.0.0.0.0.0">
              <g transform="matrix(1, 0, 0, 1, -9.15527e-05, -0.000488281)">
               <g  id="_x30_.1.0.2.14.0.0.0.0.0.0">
                <g transform="matrix(1, 0, 0, 1, -0.4473, -2.6758)">
                 <text  fill="#FFFFFF" font-family="'OCRA'" id="_x30_.1.0.2.14.0.0.0.0.0.0.0" font-size="3.3408">RESET</text>
                </g>
               </g>
              </g>
             </g>
            </g>
           </g>
          </g>
         </g>
        </g>
       </g>
      </g>
      <g  id="_x30_.1.0.2.15">
       <g  id="_x30_.1.0.2.15.0">
        <g transform="matrix(1, 0, 0, 1, 120.212, 138.96)">
         <g  id="_x30_.1.0.2.15.0.0">
          <g  id="_x30_.1.0.2.15.0.0.0">
           <g transform="rotate(270)">
            <g  id="_x30_.1.0.2.15.0.0.0.0">
             <g  id="_x30_.1.0.2.15.0.0.0.0.0">
              <g transform="matrix(1, 0, 0, 1, 0.000534058, -0.000579834)">
               <g  id="_x30_.1.0.2.15.0.0.0.0.0.0">
                <g transform="matrix(1, 0, 0, 1, -0.4473, -2.6758)">
                 <text  fill="#FFFFFF" font-family="'OCRA'" id="_x30_.1.0.2.15.0.0.0.0.0.0.0" font-size="3.3408">3V3</text>
                </g>
               </g>
              </g>
             </g>
            </g>
           </g>
          </g>
         </g>
        </g>
       </g>
      </g>
      <g  id="_x30_.1.0.2.16">
       <title  id="0.1.0.2.16.0">text:A1</title>
       <g transform="matrix(-4.37114e-08, -1, 1, -4.37114e-08, 170.418, 138.997)">
        <g  id="_x30_.1.0.2.16.1">
         <g transform="matrix(1, 0, 0, 1, -0.4473, -2.6758)">
          <text  fill="#FFFFFF" font-family="'OCRA'" id="_x30_.1.0.2.16.1.0" font-size="3.3408">A1</text>
         </g>
        </g>
       </g>
      </g>
      <g  id="_x30_.1.0.2.17">
       <title  id="0.1.0.2.17.0">text:A2</title>
       <g transform="matrix(-4.37114e-08, -1, 1, -4.37114e-08, 177.622, 138.997)">
        <g  id="_x30_.1.0.2.17.1">
         <g transform="matrix(1, 0, 0, 1, -0.4473, -2.6758)">
          <text  fill="#FFFFFF" font-family="'OCRA'" id="_x30_.1.0.2.17.1.0" font-size="3.3408">A2</text>
         </g>
        </g>
       </g>
      </g>
      <g  id="_x30_.1.0.2.18">
       <title  id="0.1.0.2.18.0">text:A3</title>
       <g transform="matrix(-4.37114e-08, -1, 1, -4.37114e-08, 184.819, 138.997)">
        <g  id="_x30_.1.0.2.18.1">
         <g transform="matrix(1, 0, 0, 1, -0.4473, -2.6757)">
          <text  fill="#FFFFFF" font-family="'OCRA'" id="_x30_.1.0.2.18.1.0" font-size="3.3408">A3</text>
         </g>
        </g>
       </g>
      </g>
      <g  id="_x30_.1.0.2.19">
       <title  id="0.1.0.2.19.0">text:A4</title>
       <g transform="matrix(-4.37114e-08, -1, 1, -4.37114e-08, 192.02, 138.997)">
        <g  id="_x30_.1.0.2.19.1">
         <g transform="matrix(1, 0, 0, 1, -0.4473, -2.6758)">
          <text  fill="#FFFFFF" font-family="'OCRA'" id="_x30_.1.0.2.19.1.0" font-size="3.3408">A4</text>
         </g>
        </g>
       </g>
      </g>
      <g  id="_x30_.1.0.2.20">
       <title  id="0.1.0.2.20.0">text:A5</title>
       <g transform="matrix(-4.37114e-08, -1, 1, -4.37114e-08, 199.219, 138.997)">
        <g  id="_x30_.1.0.2.20.1">
         <g transform="matrix(1, 0, 0, 1, -0.4473, -2.6757)">
          <text  fill="#FFFFFF" font-family="'OCRA'" id="_x30_.1.0.2.20.1.0" font-size="3.3408">A5</text>
         </g>
        </g>
       </g>
      </g>
      <g  id="_x30_.1.0.2.21">
       <g  id="_x30_.1.0.2.21.0">
        <g transform="matrix(-4.37114e-08, -1, 1, -4.37114e-08, 148.965, 138.997)">
         <g  id="_x30_.1.0.2.21.0.0">
          <g transform="matrix(1, 0, 0, 1, -0.4473, -2.6758)">
           <text  fill="#FFFFFF" font-family="'OCRA'" id="_x30_.1.0.2.21.0.0.0" font-size="3.3408">VIN</text>
          </g>
         </g>
        </g>
       </g>
      </g>
      <g  id="_x30_.1.0.2.22">
       <g  id="_x30_.1.0.2.22.0">
        <g transform="matrix(-4.37114e-08, -1, 1, -4.37114e-08, 134.561, 138.997)">
         <g  id="_x30_.1.0.2.22.0.0">
          <g transform="matrix(1, 0, 0, 1, -0.4473, -2.6758)">
           <text  fill="#FFFFFF" font-family="'OCRA'" id="_x30_.1.0.2.22.0.0.0" font-size="3.3408">GND</text>
          </g>
         </g>
        </g>
       </g>
      </g>
      <g  id="_x30_.1.0.2.23">
       <g  id="_x30_.1.0.2.23.0">
        <g transform="matrix(-4.37114e-08, -1, 1, -4.37114e-08, 141.557, 138.959)">
         <g  id="_x30_.1.0.2.23.0.0">
          <g transform="matrix(1, 0, 0, 1, -0.4472, -2.6758)">
           <text  fill="#FFFFFF" font-family="'OCRA'" id="_x30_.1.0.2.23.0.0.0" font-size="3.3408">GND</text>
          </g>
         </g>
        </g>
       </g>
      </g>
      <g  id="_x30_.1.0.2.24">
       <title  id="0.1.0.2.24.0">text:[#=PWM]</title>
       <g transform="matrix(1, 0, 0, 1, 145.157, 27.2759)">
        <g  id="_x30_.1.0.2.24.1">
         <g transform="matrix(1, 0, 0, 1, -41.5263, -0.5567)">
          <text  fill="#FFFFFF" font-family="'OCRA'" id="_x30_.1.0.2.24.1.0" font-size="3.5">DIGITAL (PWM  SPI )</text>
         </g>
        </g>
       </g>
       <g transform="matrix(1, 0, 0, 1, 145.157, 27.2759)">
        <g  id="_x30_.1.0.2.24.1_4_">
         <g transform="matrix(1, 0, 0, 1, -79.1093, -13.3828)">
          <text  fill="#FFFFFF" font-family="'OCRA'" id="_x30_.1.0.2.24.1.0_4_" font-size="2.5">SCL</text>
         </g>
        </g>
       </g>
       <g transform="matrix(1, 0, 0, 1, 145.157, 27.2759)">
        <g  id="_x30_.1.0.2.24.1_5_">
         <g transform="matrix(1, 0, 0, 1, -72.1093, -13.3828)">
          <text  fill="#FFFFFF" font-family="'OCRA'" id="_x30_.1.0.2.24.1.0_5_" font-size="2.5">SDA</text>
         </g>
        </g>
       </g>
       <g transform="matrix(1, 0, 0, 1, 179.696, 27.2759)">
        <g  id="_x30_.1.0.2.24.2"/>
       </g>
       <g transform="matrix(-4.37114e-08, 1, -1, -4.37114e-08, 147.288, 23.7207)">
        <text  fill="#FFFFFF" font-family="'OCRA'" font-size="2.5">&lt;</text>
       </g>
      </g>
      <g  id="_x30_.1.0.2.26">
       <g  id="_x30_.1.0.2.26.0">
        <g transform="matrix(1, 0, 0, 1, 123.452, 22.68)">
         <g  id="_x30_.1.0.2.26.0.0">
          <g  id="_x30_.1.0.2.26.0.0.0">
           <g transform="rotate(270)">
            <g  id="_x30_.1.0.2.26.0.0.0.0">
             <g  id="_x30_.1.0.2.26.0.0.0.0.0">
              <g  id="_x30_.1.0.2.26.0.0.0.0.0.0" enable-background="new    ">
               <path  fill="#FFFFFF" id="_x30_.1.0.2.26.0.0.0.0.0.0.0" d="M1.117,-11.151c-0.021,-0.5,0.25,-0.756,0.596,-0.756c0.21,0,0.37,0.064,0.706,0.226c0.255,0.121,0.44,0.211,0.625,0.211c0.181,0,0.266,-0.146,0.271,-0.42l0.3,0c0.025,0.562,-0.265,0.756,-0.576,0.756c-0.2,0,-0.38,-0.062,-0.726,-0.221c-0.235,-0.115,-0.42,-0.222,-0.601,-0.222c-0.181,0,-0.29,0.125,-0.3,0.426L1.117,-11.151L1.117,-11.151z"/>
              </g>
             </g>
            </g>
           </g>
          </g>
         </g>
        </g>
       </g>
      </g>
      <g  id="_x30_.1.0.2.27">
       <g  id="_x30_.1.0.2.27.0">
        <g transform="matrix(1, 0, 0, 1, 163.412, 19.08)">
         <g  id="_x30_.1.0.2.27.0.0">
          <g  id="_x30_.1.0.2.27.0.0.0">
           <g transform="rotate(270)">
            <g  id="_x30_.1.0.2.27.0.0.0.0">
             <g  id="_x30_.1.0.2.27.0.0.0.0.0">
              <g  id="_x30_.1.0.2.27.0.0.0.0.0.0" enable-background="new    ">
               <path  fill="#FFFFFF" id="_x30_.1.0.2.27.0.0.0.0.0.0.0" d="M0.547,-3.727c-0.02,-0.502,0.25,-0.756,0.596,-0.756c0.21,0,0.37,0.063,0.706,0.225c0.254,0.121,0.439,0.212,0.624,0.212c0.181,0,0.266,-0.146,0.271,-0.423l0.3,0c0.025,0.563,-0.265,0.757,-0.576,0.757c-0.2,0,-0.38,-0.06,-0.726,-0.22c-0.234,-0.114,-0.42,-0.222,-0.6,-0.222s-0.29,0.125,-0.3,0.427L0.547,-3.727z"/>
              </g>
             </g>
            </g>
           </g>
          </g>
         </g>
        </g>
       </g>
      </g>
      <g  id="_x30_.1.0.2.28">
       <title  id="0.1.0.2.28.0">text:#</title>
       <g transform="matrix(1, 0, 0, 1, 177.812, 19.08)">
        <g  id="_x30_.1.0.2.28.1">
         <g  id="_x30_.1.0.2.28.1.0">
          <g transform="rotate(270)">
           <g  id="_x30_.1.0.2.28.1.0.0">
            <g  id="_x30_.1.0.2.28.1.0.0.0">
             <g  id="_x30_.1.0.2.28.1.0.0.0.0" enable-background="new    ">
              <path  fill="#FFFFFF" id="_x30_.1.0.2.28.1.0.0.0.0.0" d="M0.547,-3.728c-0.02,-0.502,0.25,-0.758,0.596,-0.758c0.21,0,0.37,0.063,0.706,0.227c0.254,0.121,0.439,0.211,0.624,0.211c0.181,0,0.266,-0.146,0.271,-0.422l0.3,0c0.025,0.562,-0.265,0.757,-0.576,0.757c-0.2,0,-0.38,-0.062,-0.726,-0.22c-0.235,-0.115,-0.42,-0.223,-0.601,-0.223s-0.29,0.125,-0.3,0.428L0.547,-3.728z"/>
             </g>
            </g>
           </g>
          </g>
         </g>
        </g>
       </g>
      </g>
      <g  id="_x30_.1.0.2.29">
       <g  id="_x30_.1.0.2.29.0">
        <g transform="matrix(1, 0, 0, 1, 156.572, 19.08)">
         <g  id="_x30_.1.0.2.29.0.0">
          <g  id="_x30_.1.0.2.29.0.0.0">
           <g transform="rotate(270)">
            <g  id="_x30_.1.0.2.29.0.0.0.0">
             <g  id="_x30_.1.0.2.29.0.0.0.0.0">
              <g  id="_x30_.1.0.2.29.0.0.0.0.0.0" enable-background="new    ">
               <path  fill="#FFFFFF" id="_x30_.1.0.2.29.0.0.0.0.0.0.0" d="M0.547,-3.727c-0.02,-0.503,0.25,-0.757,0.596,-0.757c0.21,0,0.37,0.064,0.706,0.226c0.254,0.121,0.439,0.211,0.624,0.211c0.181,0,0.266,-0.146,0.271,-0.422l0.3,0c0.025,0.562,-0.265,0.756,-0.576,0.756c-0.2,0,-0.38,-0.06,-0.726,-0.219c-0.234,-0.115,-0.42,-0.222,-0.6,-0.222s-0.29,0.125,-0.3,0.427L0.547,-3.727z"/>
              </g>
             </g>
            </g>
           </g>
          </g>
         </g>
        </g>
       </g>
      </g>
      <g  id="_x30_.1.0.2.30">
       <g  id="_x30_.1.0.2.30.0">
        <g transform="matrix(1, 0, 0, 1, 130.292, 19.08)">
         <g  id="_x30_.1.0.2.30.0.0">
          <g  id="_x30_.1.0.2.30.0.0.0">
           <g transform="rotate(270)">
            <g  id="_x30_.1.0.2.30.0.0.0.0">
             <g  id="_x30_.1.0.2.30.0.0.0.0.0">
              <g  id="_x30_.1.0.2.30.0.0.0.0.0.0" enable-background="new    ">
               <path  fill="#FFFFFF" id="_x30_.1.0.2.30.0.0.0.0.0.0.0" d="M0.547,-3.728c-0.02,-0.5,0.25,-0.756,0.596,-0.756c0.21,0,0.37,0.063,0.706,0.226c0.254,0.12,0.439,0.211,0.624,0.211c0.181,0,0.266,-0.146,0.271,-0.42l0.3,0c0.025,0.561,-0.265,0.756,-0.576,0.756c-0.2,0,-0.38,-0.063,-0.726,-0.222c-0.235,-0.114,-0.42,-0.224,-0.601,-0.224s-0.29,0.125,-0.3,0.429L0.547,-3.728L0.547,-3.728z"/>
              </g>
             </g>
            </g>
           </g>
          </g>
         </g>
        </g>
       </g>
      </g>
      <g  id="_x30_.1.0.2.32">
       <g  id="_x30_.1.0.2.32.0">
        <g transform="matrix(1, 0, 0, 1, 106.172, 138.6)">
         <g  id="_x30_.1.0.2.32.0.0">
          <g  id="_x30_.1.0.2.32.0.0.0">
           <g transform="rotate(270)">
            <g  id="_x30_.1.0.2.32.0.0.0.0">
             <g  id="_x30_.1.0.2.32.0.0.0.0.0">
              <g transform="matrix(1, 0, 0, 1, -9.15527e-05, -0.00012207)">
               <g  id="_x30_.1.0.2.32.0.0.0.0.0.0">
                <g transform="matrix(1, 0, 0, 1, -0.4473, -2.6768)">
                 <text  fill="#FFFFFF" font-family="'OCRA'" id="_x30_.1.0.2.32.0.0.0.0.0.0.0" font-size="3.3408">IOREF</text>
                </g>
               </g>
              </g>
             </g>
            </g>
           </g>
          </g>
         </g>
        </g>
       </g>
      </g>
      <g  id="_x30_.1.0.2.33">
       <title  id="0.1.0.2.33.0">text:SDA</title>
      </g>
      <g  id="_x30_.1.0.2.34">
       <title  id="0.1.0.2.34.0">text:SCL</title>
      </g>
      <g  id="_x30_.1.0.2.35">
       <title  id="0.1.0.2.35.0">element:AD</title>
       <g  id="_x30_.1.0.2.35.1">
        <title  id="0.1.0.2.35.1.0">package:1X06</title>
       </g>
      </g>
      <g  id="_x30_.1.0.2.36">
       <title  id="0.1.0.2.36.0">element:C1</title>
       <g  id="_x30_.1.0.2.36.1">
        <title  id="0.1.0.2.36.1.0">package:C0603-ROUND</title>
       </g>
      </g>
      <g  id="_x30_.1.0.2.37">
       <title  id="0.1.0.2.37.0">element:C2</title>
       <g  id="_x30_.1.0.2.37.1">
        <title  id="0.1.0.2.37.1.0">package:C0603-ROUND</title>
       </g>
      </g>
      <g  id="_x30_.1.0.2.38">
       <title  id="0.1.0.2.38.0">element:C3</title>
       <g  id="_x30_.1.0.2.38.1">
        <title  id="0.1.0.2.38.1.0">package:C0603-ROUND</title>
       </g>
      </g>
      <g  id="_x30_.1.0.2.39">
       <title  id="0.1.0.2.39.0">element:C4</title>
       <g  id="_x30_.1.0.2.39.1">
        <title  id="0.1.0.2.39.1.0">package:C0603-ROUND</title>
       </g>
      </g>
      <g  id="_x30_.1.0.2.40">
       <title  id="0.1.0.2.40.0">element:C5</title>
       <g  id="_x30_.1.0.2.40.1">
        <title  id="0.1.0.2.40.1.0">package:C0603-ROUND</title>
       </g>
      </g>
      <g  id="_x30_.1.0.2.41">
       <title  id="0.1.0.2.41.0">element:C6</title>
       <g  id="_x30_.1.0.2.41.1">
        <title  id="0.1.0.2.41.1.0">package:C0603-ROUND</title>
       </g>
      </g>
      <g  id="_x30_.1.0.2.42">
       <title  id="0.1.0.2.42.0">element:C7</title>
       <g  id="_x30_.1.0.2.42.1">
        <title  id="0.1.0.2.42.1.0">package:C0603-ROUND</title>
       </g>
      </g>
      <g  id="_x30_.1.0.2.43">
       <title  id="0.1.0.2.43.0">element:C8</title>
       <g  id="_x30_.1.0.2.43.1">
        <title  id="0.1.0.2.43.1.0">package:C0603-ROUND</title>
       </g>
      </g>
      <g  id="_x30_.1.0.2.44">
       <title  id="0.1.0.2.44.0">element:C9</title>
       <g  id="_x30_.1.0.2.44.1">
        <title  id="0.1.0.2.44.1.0">package:C0603-ROUND</title>
       </g>
      </g>
      <g  id="_x30_.1.0.2.45">
       <title  id="0.1.0.2.45.0">element:C11</title>
       <g  id="_x30_.1.0.2.45.1">
        <title  id="0.1.0.2.45.1.0">package:C0603-ROUND</title>
       </g>
      </g>
      <g  id="_x30_.1.0.2.46">
       <title  id="0.1.0.2.46.0">element:D1</title>
       <g  id="_x30_.1.0.2.46.1">
        <title  id="0.1.0.2.46.1.0">package:SMB</title>
       </g>
      </g>
      <g  id="_x30_.1.0.2.47">
       <title  id="0.1.0.2.47.0">element:D2</title>
       <g  id="_x30_.1.0.2.47.1">
        <title  id="0.1.0.2.47.1.0">package:MINIMELF</title>
       </g>
      </g>
      <g  id="_x30_.1.0.2.48">
       <title  id="0.1.0.2.48.0">element:D3</title>
       <g  id="_x30_.1.0.2.48.1">
        <title  id="0.1.0.2.48.1.0">package:MINIMELF</title>
       </g>
      </g>
      <g  id="_x30_.1.0.2.49">
       <title  id="0.1.0.2.49.0">element:F1</title>
       <g  id="_x30_.1.0.2.49.1">
        <title  id="0.1.0.2.49.1.0">package:L1812</title>
       </g>
      </g>
      <g  id="_x30_.1.0.2.50">
       <title  id="0.1.0.2.50.0">element:FD1</title>
       <g  id="_x30_.1.0.2.50.1">
        <title  id="0.1.0.2.50.1.0">package:FIDUCIA-MOUNT</title>
       </g>
      </g>
      <g  id="_x30_.1.0.2.51">
       <title  id="0.1.0.2.51.0">element:FD2</title>
       <g  id="_x30_.1.0.2.51.1">
        <title  id="0.1.0.2.51.1.0">package:FIDUCIA-MOUNT</title>
       </g>
      </g>
      <g  id="_x30_.1.0.2.52">
       <title  id="0.1.0.2.52.0">element:FD3</title>
       <g  id="_x30_.1.0.2.52.1">
        <title  id="0.1.0.2.52.1.0">package:FIDUCIA-MOUNT</title>
       </g>
      </g>
      <g  id="_x30_.1.0.2.53">
       <title  id="0.1.0.2.53.0">element:GROUND</title>
       <g  id="_x30_.1.0.2.53.1">
        <title  id="0.1.0.2.53.1.0">package:SJ</title>
       </g>
      </g>
      <g  id="_x30_.1.0.2.54">
       <title  id="0.1.0.2.54.0">element:ICSP</title>
       <g  id="_x30_.1.0.2.54.1">
        <title  id="0.1.0.2.54.1.0">text:ICSP</title>
        <g transform="matrix(1, 0, 0, 1, 194.553, 82.3349)">
         <g  id="_x30_.1.0.2.54.1.1">
          <g  id="_x30_.1.0.2.54.1.1.0">
           <g transform="rotate(270)">
            <g  id="_x30_.1.0.2.54.1.1.0.0">
             <g  id="_x30_.1.0.2.54.1.1.0.0.0">
              <g transform="matrix(1, 0, 0, 1, -0.7808, -0.783)">
               <g  id="_x30_.1.0.2.54.1.1.0.0.0.0">
                <g transform="matrix(1, 0, 0, 1, -0.4473, -2.6758)">
                 <text  fill="#FFFFFF" font-family="'OCRA'" id="_x30_.1.0.2.54.1.1.0.0.0.0.0" font-size="4.176">ICSP</text>
                </g>
               </g>
              </g>
             </g>
            </g>
           </g>
          </g>
         </g>
        </g>
       </g>
       <g  id="_x30_.1.0.2.54.2">
        <title  id="0.1.0.2.54.2.0">package:2X03</title>
       </g>
      </g>
      <g  id="_x30_.1.0.2.56">
       <title  id="0.1.0.2.56.0">element:ICSP1</title>
       <g  id="_x30_.1.0.2.56.1">
        <title  id="0.1.0.2.56.1.0">package:2X03</title>
       </g>
      </g>
      <g  id="_x30_.1.0.2.57">
       <title  id="0.1.0.2.57.0">element:IOH</title>
       <g  id="_x30_.1.0.2.57.1">
        <title  id="0.1.0.2.57.1.0">package:1X10@1</title>
       </g>
      </g>
      <g  id="_x30_.1.0.2.58">
       <title  id="0.1.0.2.58.0">element:IOL</title>
       <g  id="_x30_.1.0.2.58.1">
        <title  id="0.1.0.2.58.1.0">package:1X08</title>
       </g>
      </g>
      <g  id="_x30_.1.0.2.59">
       <title  id="0.1.0.2.59.0">element:JP2</title>
       <g  id="_x30_.1.0.2.59.1">
        <title  id="0.1.0.2.59.1.0">package:2X02</title>
       </g>
      </g>
      <g  id="_x30_.1.0.2.60">
       <title  id="0.1.0.2.60.0">element:L</title>
       <g  id="_x30_.1.0.2.60.1">
        <title  id="0.1.0.2.60.1.0">package:CHIP-LED0805</title>
       </g>
      </g>
      <g  id="_x30_.1.0.2.61">
       <title  id="0.1.0.2.61.0">element:L1</title>
       <g  id="_x30_.1.0.2.61.1">
        <title  id="0.1.0.2.61.1.0">package:0805</title>
       </g>
      </g>
      <g  id="_x30_.1.0.2.63">
       <title  id="0.1.0.2.63.0">element:PC1</title>
       <g  id="_x30_.1.0.2.63.1">
        <title  id="0.1.0.2.63.1.0">package:PANASONIC_D</title>
       </g>
      </g>
      <g  id="_x30_.1.0.2.64">
       <title  id="0.1.0.2.64.0">element:PC2</title>
       <g  id="_x30_.1.0.2.64.1">
        <title  id="0.1.0.2.64.1.0">package:PANASONIC_D</title>
       </g>
      </g>
      <g  id="_x30_.1.0.2.65">
       <title  id="0.1.0.2.65.0">element:R1</title>
       <g  id="_x30_.1.0.2.65.1">
        <title  id="0.1.0.2.65.1.0">package:R0603-ROUND</title>
       </g>
      </g>
      <g  id="_x30_.1.0.2.66">
       <title  id="0.1.0.2.66.0">element:R2</title>
       <g  id="_x30_.1.0.2.66.1">
        <title  id="0.1.0.2.66.1.0">package:R0603-ROUND</title>
       </g>
      </g>
      <g  id="_x30_.1.0.2.67">
       <title  id="0.1.0.2.67.0">element:RESET</title>
       <g  id="_x30_.1.0.2.67.1">
        <title  id="0.1.0.2.67.1.0">package:TS42</title>
       </g>
      </g>
      <g  id="_x30_.1.0.2.68">
       <title  id="0.1.0.2.68.0">element:RESET-EN</title>
       <g  id="_x30_.1.0.2.68.1">
        <title  id="0.1.0.2.68.1.0">package:SJ</title>
       </g>
      </g>
      <g  id="_x30_.1.0.2.69">
       <title  id="0.1.0.2.69.0">element:RN1</title>
       <g  id="_x30_.1.0.2.69.1">
        <title  id="0.1.0.2.69.1.0">package:CAY16</title>
       </g>
      </g>
      <g  id="_x30_.1.0.2.70">
       <title  id="0.1.0.2.70.0">element:RN2</title>
       <g  id="_x30_.1.0.2.70.1">
        <title  id="0.1.0.2.70.1.0">package:CAY16</title>
       </g>
      </g>
      <g  id="_x30_.1.0.2.71">
       <title  id="0.1.0.2.71.0">element:RN3</title>
       <g  id="_x30_.1.0.2.71.1">
        <title  id="0.1.0.2.71.1.0">package:CAY16</title>
       </g>
      </g>
      <g  id="_x30_.1.0.2.72">
       <title  id="0.1.0.2.72.0">element:RN4</title>
       <g  id="_x30_.1.0.2.72.1">
        <title  id="0.1.0.2.72.1.0">package:CAY16</title>
       </g>
      </g>
      <g  id="_x30_.1.0.2.73">
       <title  id="0.1.0.2.73.0">element:RX</title>
       <g  id="_x30_.1.0.2.73.1">
        <title  id="0.1.0.2.73.1.0">package:CHIP-LED0805</title>
       </g>
      </g>
      <g  id="_x30_.1.0.2.74">
       <title  id="0.1.0.2.74.0">element:T1</title>
       <g  id="_x30_.1.0.2.74.1">
        <title  id="0.1.0.2.74.1.0">package:SOT-23</title>
       </g>
      </g>
      <g  id="_x30_.1.0.2.75">
       <title  id="0.1.0.2.75.0">element:TX</title>
       <g  id="_x30_.1.0.2.75.1">
        <title  id="0.1.0.2.75.1.0">package:CHIP-LED0805</title>
       </g>
      </g>
      <g  id="_x30_.1.0.2.76">
       <title  id="0.1.0.2.76.0">element:U1</title>
       <g  id="_x30_.1.0.2.76.1">
        <title  id="0.1.0.2.76.1.0">package:SOT223</title>
       </g>
      </g>
      <g  id="_x30_.1.0.2.77">
       <title  id="0.1.0.2.77.0">element:U2</title>
       <g  id="_x30_.1.0.2.77.1">
        <title  id="0.1.0.2.77.1.0">package:SOT23-DBV</title>
       </g>
      </g>
      <g  id="_x30_.1.0.2.78">
       <title  id="0.1.0.2.78.0">element:U3</title>
       <g  id="_x30_.1.0.2.78.1">
        <title  id="0.1.0.2.78.1.0">package:MLF32</title>
       </g>
      </g>
      <g  id="_x30_.1.0.2.79">
       <title  id="0.1.0.2.79.0">element:U5</title>
       <g  id="_x30_.1.0.2.79.1">
        <title  id="0.1.0.2.79.1.0">package:MSOP08</title>
       </g>
      </g>
      <g  id="_x30_.1.0.2.80">
       <title  id="0.1.0.2.80.0">element:X1</title>
       <g  id="_x30_.1.0.2.80.1">
        <title  id="0.1.0.2.80.1.0">package:POWERSUPPLY_DC-21MM</title>
       </g>
      </g>
      <g  id="_x30_.1.0.2.81">
       <title  id="0.1.0.2.81.0">element:X2</title>
       <g  id="_x30_.1.0.2.81.1">
        <title  id="0.1.0.2.81.1.0">package:PN61729</title>
       </g>
      </g>
      <g  id="_x30_.1.0.2.82">
       <title  id="0.1.0.2.82.0">element:Y1</title>
       <g  id="_x30_.1.0.2.82.1">
        <title  id="0.1.0.2.82.1.0">package:QS</title>
       </g>
      </g>
      <g  id="_x30_.1.0.2.83">
       <title  id="0.1.0.2.83.0">element:Y2</title>
       <g  id="_x30_.1.0.2.83.1">
        <title  id="0.1.0.2.83.1.0">package:RESONATOR</title>
       </g>
      </g>
      <g  id="_x30_.1.0.2.84">
       <title  id="0.1.0.2.84.0">element:Z1</title>
       <g  id="_x30_.1.0.2.84.1">
        <title  id="0.1.0.2.84.1.0">package:CT/CN0603</title>
       </g>
      </g>
      <g  id="_x30_.1.0.2.85">
       <title  id="0.1.0.2.85.0">element:Z2</title>
       <g  id="_x30_.1.0.2.85.1">
        <title  id="0.1.0.2.85.1.0">package:CT/CN0603</title>
       </g>
      </g>
      <g  id="_x30_.1.0.2.86">
       <title  id="0.1.0.2.86.0">element:ZU4</title>
       <g  id="_x30_.1.0.2.86.1">
        <title  id="0.1.0.2.86.1.0">package:DIL28-3</title>
       </g>
      </g>
      <g  id="_x30_.1.0.2.30_1_">
       <g  id="_x30_.1.0.2.30.0_1_">
        <g transform="matrix(1, 0, 0, 1, 130.292, 19.08)">
         <g  id="_x30_.1.0.2.30.0.0_1_">
          <g  id="_x30_.1.0.2.30.0.0.0_1_">
           <g transform="rotate(270)">
            <g  id="_x30_.1.0.2.30.0.0.0.0_1_">
             <g  id="_x30_.1.0.2.30.0.0.0.0.0_1_">
              <g  id="_x30_.1.0.2.30.0.0.0.0.0.0_1_" enable-background="new    ">
               <path  fill="#FFFFFF" id="_x30_.1.0.2.30.0.0.0.0.0.0.0_1_" d="M-6.626,4.392c0.5,-0.02,0.756,0.25,0.756,0.596c0,0.211,-0.065,0.37,-0.225,0.706c-0.121,0.255,-0.211,0.438,-0.211,0.624c0,0.182,0.146,0.268,0.42,0.271l0,0.3c-0.561,0.024,-0.756,-0.265,-0.756,-0.576c0,-0.2,0.063,-0.38,0.221,-0.726c0.115,-0.235,0.224,-0.42,0.224,-0.603c0,-0.181,-0.125,-0.29,-0.429,-0.3L-6.626,4.392L-6.626,4.392z"/>
              </g>
             </g>
            </g>
           </g>
          </g>
         </g>
        </g>
       </g>
      </g>
     </g>
     <g transform="matrix(-4.37114e-08, -1, 1, -4.37114e-08, 121.651, 16.3936)">
      <text  fill="#FFFFFF" font-family="'OCRA'" font-size="2.75">CS</text>
     </g>
     <g transform="matrix(1, 0, 0, 1, 95.7085, 20.1606)">
      <text  fill="#FFFFFF" font-family="'OCRA'" font-size="2.75">&lt;</text>
     </g>
     <g transform="matrix(1, 0, 0, 1, 102.909, 20.1606)">
      <text  fill="#FFFFFF" font-family="'OCRA'" font-size="2.75">&lt;</text>
     </g>
    </g>
    </g></g></g><path stroke='#8c8c8c' stroke-width='2.15998' stroke-linecap='round' stroke-linejoin='round' fill='none' d='M269.811,61.2015L262.633,61.2015' />
    <path stroke='#8c8c8c' stroke-width='2.15998' stroke-linecap='round' stroke-linejoin='round' fill='none' d='M269.811,68.3825L262.633,68.3825' />
    <path stroke='#8c8c8c' stroke-width='2.15998' stroke-linecap='round' stroke-linejoin='round' fill='none' d='M269.811,75.5684L262.633,75.5684' />
    <g partID='18452720'><g transform='translate(293.892,60.1215)' ><g transform='matrix(0,1,-1,0,0,0)'  ><g xmlns="http://www.w3.org/2000/svg" id="breadboard">
     <rect xmlns="http://www.w3.org/2000/svg" width="2.15998" x="0" y="22.081" fill="none" height="1" id="connector0pin"/>
     <rect xmlns="http://www.w3.org/2000/svg" width="2.15998" x="7.18095" y="22.081" fill="none" height="1" id="connector1pin"/>
     <rect xmlns="http://www.w3.org/2000/svg" width="2.15998" x="14.3669" y="22.081" fill="none" height="1" id="connector2pin"/>
     <g xmlns="http://www.w3.org/2000/svg" fill="none" stroke="#8C8C8C" id="connector0leg" stroke-linecap="round" y1="24.081" x1="1.08" y2="31.259" stroke-width="2.15998" x2="1.08"/>
     <g xmlns="http://www.w3.org/2000/svg" fill="none" stroke="#8C8C8C" id="connector1leg" stroke-linecap="round" y1="24.081" x1="8.261" y2="31.259" stroke-width="2.15998" x2="8.261"/>
     <g xmlns="http://www.w3.org/2000/svg" fill="none" stroke="#8C8C8C" id="connector2leg" stroke-linecap="round" y1="24.081" x1="15.447" y2="31.259" stroke-width="2.15998" x2="15.447"/>
     <rect xmlns="http://www.w3.org/2000/svg" width="2.15398" x="7.17795" y="14.731" fill="#8C8C8C" height="9.351" id="rect9506"/>
     <path xmlns="http://www.w3.org/2000/svg" fill="#8C8C8C" id="path9510" d="M3.28698,14.731l0,3.316c0,0.424,-0.781994,1.059,-1.19799,1.425c-1.02499,0.891,-2.08798,1.819,-2.08798,2.992l0,1.619l2.15398,0c0,0,0,-1,0,-1.21c0,-0.517,0.903993,-1.389,1.34999,-1.769c0.996993,-0.87,1.94499,-1.69,1.94499,-2.749l0,-3.625L3.28698,14.73L3.28698,14.731z"/>
     <path xmlns="http://www.w3.org/2000/svg" fill="#8C8C8C" id="path9514" d="M13.2209,14.731l0,3.316c0,0.424,0.780994,1.059,1.19899,1.425c1.02699,0.891,2.08898,1.819,2.08898,2.992l0,1.619l-2.15398,0c0,0,0,-1,0,-1.21c0,-0.517,-0.903993,-1.389,-1.34999,-1.769c-0.997993,-0.87,-1.94499,-1.69,-1.94499,-2.749l0,-3.625L13.2209,14.73L13.2209,14.731z"/>
     <rect xmlns="http://www.w3.org/2000/svg" width="13.2779" x="1.61499" y="4.659" fill="#1A1A1A" height="10.07" id="rect9553"/>
     <path xmlns="http://www.w3.org/2000/svg" fill="#141414" id="path9555" d="M13.8889,4.659l0,2.453l0,8.228l0,1.842c0.631995,-0.713,1.00399,-1.553,1.00399,-2.453l0,0L14.8929,4.659L13.8889,4.659z"/>
     <path xmlns="http://www.w3.org/2000/svg" fill="#242424" id="path9557" d="M2.62098,4.659L1.61599,4.659l0,10.07l0,0c0,0.899,0.372997,1.74,1.00499,2.453L2.62098,15.34L2.62098,7.112L2.62098,4.659z"/>
     <path xmlns="http://www.w3.org/2000/svg" fill="#1F1F1F" id="path9559" d="M1.61499,4.659L1.61499,4.659c0,0.899,0.372997,1.74,1.00499,2.453l11.2759,0c0.631995,-0.713,1.00499,-1.554,1.00499,-2.453l0,0L1.61499,4.659z"/>
     <path xmlns="http://www.w3.org/2000/svg" fill="#141414" id="path9561" d="M8.25494,0C4.58697,0,1.61499,2.086,1.61499,4.661l13.2779,0C14.8929,2.086,11.9229,0,8.25494,0z"/>
     <rect xmlns="http://www.w3.org/2000/svg" width="11.2759" x="2.62098" y="7.112" height="10.07" id="rect9563"/>
     <path xmlns="http://www.w3.org/2000/svg" fill="#999999" d="M4.98996,14.359l0,-5.4l2.15998,0l0,1.079l1.07999,0l0,1.08l1.08099,0L9.31093,8.958l2.15898,0l0,5.4L9.31193,14.358l0,-1.079L8.23094,13.279l0,-1.08l-1.07999,0l0,2.161L4.98996,14.36z"/>
    </g>
    </g></g></g><g partID='18457280'><g transform='translate(230.751,220.116)' ><g transform='matrix(0,-1,1,0,0,0)'  ><g xmlns="http://www.w3.org/2000/svg" id="breadboard">
     <path xmlns="http://www.w3.org/2000/svg" fill="#1A1A1A" d="M58.115,9.27L58.115,8.625L7.658,8.625L7.658,9.27L0,9.27l0,38.646l65.771,0L65.771,9.27L58.115,9.27zM32.886,25.545c-2.212,0,-4.004,-1.793,-4.004,-4.004s1.792,-4.004,4.004,-4.004c2.211,0,4.004,1.793,4.004,4.004S35.097,25.545,32.886,25.545z"/>
     <g xmlns="http://www.w3.org/2000/svg">
      <rect xmlns="http://www.w3.org/2000/svg" width="65.772" x="0.001" y="0.5" fill="#333333" height="8.77"/>
      <rect xmlns="http://www.w3.org/2000/svg" width="65.772" x="0.001" opacity="0.2" y="0.5" fill="#FFFFFF" height="0.75"/>
      <path xmlns="http://www.w3.org/2000/svg" d="M40.359,24.916c-1.289,2.848,-4.146,4.832,-7.473,4.832c-3.328,0,-6.187,-1.984,-7.474,-4.832L0,24.916l0,23l65.771,0l0,-23L40.359,24.916z"/>
      <g xmlns="http://www.w3.org/2000/svg" id="breadboard">
       <circle xmlns="http://www.w3.org/2000/svg" fill="none" cx="7.716" cy="60.682" id="connector0pin" r="2.22"/>
       <circle xmlns="http://www.w3.org/2000/svg" fill="none" cx="22.116" cy="60.682" id="connector1pin" r="2.22"/>
       <circle xmlns="http://www.w3.org/2000/svg" fill="none" cx="50.916" cy="60.682" id="connector2pin" r="2.22"/>
       <circle xmlns="http://www.w3.org/2000/svg" fill="none" cx="58.115" cy="60.682" id="connector3pin" r="2.22"/>
      </g>
      <path xmlns="http://www.w3.org/2000/svg" fill="#333333" d="M32.886,22.213c-1.615,0,-2.998,-0.961,-3.631,-2.338c-0.234,0.508,-0.374,1.07,-0.374,1.666c0,2.211,1.792,4.004,4.004,4.004c2.211,0,4.004,-1.793,4.004,-4.004c0,-0.596,-0.141,-1.158,-0.373,-1.666C35.883,21.252,34.5,22.213,32.886,22.213z"/>
      <path xmlns="http://www.w3.org/2000/svg" fill="#1A1A1A" d="M40.359,26.123c-1.289,2.846,-4.146,4.83,-7.473,4.83c-3.328,0,-6.187,-1.984,-7.474,-4.83L0,26.123l0,21.793l34.386,0l0,2.334l11.625,0l0,-2.334l19.76,0L65.771,26.123L40.359,26.123z"/>
      <rect xmlns="http://www.w3.org/2000/svg" width="50.456" x="7.659" y="0" fill="#4D4D4D" height="8.625"/>
      <g xmlns="http://www.w3.org/2000/svg">
       <rect xmlns="http://www.w3.org/2000/svg" width="7.656" x="58.115" y="9.27" height="0.417"/>
       <rect xmlns="http://www.w3.org/2000/svg" width="7.659" x="0" y="9.27" height="0.417"/>
       <rect xmlns="http://www.w3.org/2000/svg" width="19.76" x="46.011" y="47.499" height="0.417"/>
       <rect xmlns="http://www.w3.org/2000/svg" width="11.625" x="34.386" y="49.833" height="0.417"/>
       <rect xmlns="http://www.w3.org/2000/svg" width="34.386" x="0" y="47.499" height="0.417"/>
       <rect xmlns="http://www.w3.org/2000/svg" width="50.456" x="7.659" y="8.625" height="0.417"/>
      </g>
      <rect xmlns="http://www.w3.org/2000/svg" width="2.5" x="6.512" y="47.916" fill="#CCCCCC" height="12.766"/>
      <rect xmlns="http://www.w3.org/2000/svg" width="0.5" x="6.512" y="47.916" fill="#E6E6E6" height="12.766"/>
      <rect xmlns="http://www.w3.org/2000/svg" width="2.5" x="20.866" y="47.916" fill="#CCCCCC" height="12.766"/>
      <rect xmlns="http://www.w3.org/2000/svg" width="2.5" x="49.666" y="47.916" fill="#CCCCCC" height="12.766"/>
      <rect xmlns="http://www.w3.org/2000/svg" width="2.5" x="56.865" y="47.916" fill="#CCCCCC" height="12.766"/>
      <rect xmlns="http://www.w3.org/2000/svg" width="0.5" x="20.866" y="47.916" fill="#E6E6E6" height="12.766"/>
      <rect xmlns="http://www.w3.org/2000/svg" width="0.5" x="49.666" y="47.916" fill="#E6E6E6" height="12.766"/>
      <rect xmlns="http://www.w3.org/2000/svg" width="0.5" x="56.865" y="47.916" fill="#E6E6E6" height="12.766"/>
      <g xmlns="http://www.w3.org/2000/svg">
       <path xmlns="http://www.w3.org/2000/svg" fill="#808080" d="M49.39,47.094l0,-1.768l-1.752,0l0,-0.738l1.752,0l0,-1.753l0.748,0l0,1.753l1.754,0l0,0.738l-1.754,0l0,1.768L49.39,47.094z"/>
      </g>
      <g xmlns="http://www.w3.org/2000/svg">
       <path xmlns="http://www.w3.org/2000/svg" fill="#808080" d="M57.15,45.326l0,-0.795l2.432,0l0,0.795L57.15,45.326z"/>
      </g>
      <g xmlns="http://www.w3.org/2000/svg">
       <path xmlns="http://www.w3.org/2000/svg" fill="#808080" d="M9.395,46.125l0,-0.901c0.31,-0.352,0.717,-0.527,1.221,-0.527c0.176,0,0.361,0.025,0.555,0.077c0.193,0.051,0.468,0.153,0.826,0.305c0.201,0.086,0.354,0.141,0.454,0.168c0.102,0.025,0.203,0.039,0.306,0.039c0.19,0,0.388,-0.057,0.591,-0.172c0.204,-0.113,0.385,-0.257,0.543,-0.43l0,0.932c-0.188,0.176,-0.377,0.303,-0.569,0.382c-0.191,0.079,-0.408,0.118,-0.648,0.118c-0.176,0,-0.343,-0.02,-0.503,-0.061c-0.159,-0.041,-0.413,-0.14,-0.76,-0.295c-0.348,-0.155,-0.637,-0.232,-0.868,-0.232c-0.188,0,-0.364,0.04,-0.529,0.12C9.846,45.729,9.641,45.887,9.395,46.125z"/>
      </g>
      <g xmlns="http://www.w3.org/2000/svg">
       <path xmlns="http://www.w3.org/2000/svg" fill="#808080" d="M1.854,33.509l0.844,-0.062c0.051,0.215,0.154,0.373,0.309,0.474c0.156,0.102,0.365,0.151,0.629,0.151c0.279,0,0.489,-0.045,0.631,-0.135s0.213,-0.194,0.213,-0.314c0,-0.077,-0.03,-0.144,-0.09,-0.197c-0.06,-0.055,-0.163,-0.102,-0.312,-0.142c-0.102,-0.026,-0.333,-0.074,-0.694,-0.143c-0.465,-0.087,-0.791,-0.195,-0.979,-0.322c-0.264,-0.18,-0.396,-0.398,-0.396,-0.657c0,-0.166,0.062,-0.321,0.187,-0.467c0.123,-0.145,0.302,-0.255,0.535,-0.33c0.233,-0.076,0.516,-0.113,0.846,-0.113c0.539,0,0.945,0.09,1.217,0.269c0.273,0.18,0.416,0.42,0.43,0.72l-0.867,0.028c-0.037,-0.167,-0.117,-0.288,-0.238,-0.361c-0.123,-0.073,-0.306,-0.11,-0.55,-0.11c-0.252,0,-0.449,0.039,-0.592,0.118c-0.092,0.051,-0.138,0.118,-0.138,0.202c0,0.077,0.043,0.144,0.129,0.198c0.109,0.07,0.375,0.143,0.797,0.219c0.422,0.075,0.734,0.154,0.936,0.234c0.203,0.081,0.361,0.191,0.475,0.332c0.115,0.141,0.172,0.313,0.172,0.52c0,0.188,-0.068,0.362,-0.205,0.526c-0.137,0.163,-0.33,0.284,-0.58,0.363C4.311,34.59,4,34.629,3.627,34.629c-0.543,0,-0.96,-0.095,-1.251,-0.286C2.085,34.153,1.911,33.874,1.854,33.509z"/>
       <path xmlns="http://www.w3.org/2000/svg" fill="#808080" d="M6.079,34.572l0,-3.264l0.867,0l0,1.284l1.699,0l0,-1.284l0.867,0l0,3.264L8.645,34.572l0,-1.427L6.946,33.145l0,1.427L6.079,34.572z"/>
       <path xmlns="http://www.w3.org/2000/svg" fill="#808080" d="M14.282,34.572l-0.943,0l-0.375,-0.741l-1.717,0l-0.354,0.741l-0.92,0l1.673,-3.264l0.917,0L14.282,34.572zM12.685,33.281l-0.592,-1.212l-0.58,1.212L12.685,33.281z"/>
       <path xmlns="http://www.w3.org/2000/svg" fill="#808080" d="M14.745,34.572l0,-3.264l1.825,0c0.459,0,0.792,0.029,1.001,0.088c0.207,0.059,0.374,0.162,0.499,0.313c0.125,0.149,0.188,0.321,0.188,0.515c0,0.244,-0.095,0.447,-0.284,0.606s-0.473,0.26,-0.85,0.302c0.188,0.083,0.342,0.174,0.465,0.273c0.121,0.1,0.286,0.276,0.493,0.53l0.524,0.637l-1.037,0l-0.627,-0.71c-0.223,-0.254,-0.375,-0.414,-0.457,-0.48c-0.082,-0.065,-0.169,-0.111,-0.261,-0.136s-0.237,-0.036,-0.437,-0.036l-0.176,0l0,1.362L14.745,34.572zM15.612,32.688l0.642,0c0.416,0,0.676,-0.014,0.779,-0.04s0.185,-0.072,0.243,-0.138s0.088,-0.147,0.088,-0.245c0,-0.11,-0.039,-0.198,-0.115,-0.267c-0.078,-0.067,-0.187,-0.109,-0.327,-0.128c-0.07,-0.007,-0.281,-0.011,-0.633,-0.011l-0.677,0L15.612,32.688z"/>
       <path xmlns="http://www.w3.org/2000/svg" fill="#808080" d="M19.075,34.572l0,-3.264l1.392,0c0.527,0,0.871,0.016,1.031,0.049c0.246,0.049,0.452,0.155,0.618,0.319s0.249,0.376,0.249,0.636c0,0.2,-0.048,0.369,-0.144,0.505c-0.096,0.137,-0.218,0.244,-0.365,0.322s-0.297,0.129,-0.449,0.154C21.2,33.324,20.9,33.34,20.508,33.34l-0.565,0l0,1.231L19.075,34.571zM19.942,31.86l0,0.926l0.475,0c0.342,0,0.57,-0.017,0.686,-0.051s0.205,-0.088,0.271,-0.16c0.064,-0.073,0.098,-0.157,0.098,-0.254c0,-0.119,-0.046,-0.217,-0.138,-0.294s-0.208,-0.125,-0.349,-0.145c-0.104,-0.015,-0.312,-0.022,-0.624,-0.022L19.942,31.86z"/>
      </g>
      <g xmlns="http://www.w3.org/2000/svg">
       <path xmlns="http://www.w3.org/2000/svg" fill="#808080" d="M6.693,38.772l0.703,-0.068c0.042,0.235,0.128,0.409,0.258,0.52c0.129,0.11,0.304,0.166,0.523,0.166c0.232,0,0.408,-0.049,0.526,-0.147s0.177,-0.214,0.177,-0.346c0,-0.085,-0.024,-0.156,-0.074,-0.216s-0.137,-0.111,-0.261,-0.155c-0.084,-0.029,-0.277,-0.081,-0.578,-0.156c-0.388,-0.096,-0.659,-0.214,-0.815,-0.354c-0.22,-0.196,-0.329,-0.437,-0.329,-0.72c0,-0.183,0.051,-0.353,0.154,-0.512c0.104,-0.158,0.253,-0.279,0.447,-0.362s0.429,-0.125,0.704,-0.125c0.449,0,0.787,0.099,1.015,0.296c0.227,0.197,0.346,0.46,0.357,0.788l-0.723,0.032c-0.031,-0.184,-0.098,-0.316,-0.199,-0.396c-0.102,-0.081,-0.254,-0.121,-0.457,-0.121c-0.211,0,-0.375,0.043,-0.494,0.13c-0.076,0.055,-0.114,0.129,-0.114,0.222c0,0.085,0.036,0.157,0.107,0.218c0.091,0.076,0.313,0.156,0.664,0.238c0.352,0.084,0.611,0.169,0.78,0.258c0.168,0.089,0.3,0.21,0.396,0.364c0.095,0.153,0.143,0.344,0.143,0.569c0,0.205,-0.057,0.397,-0.171,0.576c-0.114,0.18,-0.275,0.313,-0.483,0.399s-0.468,0.131,-0.778,0.131c-0.453,0,-0.801,-0.104,-1.043,-0.313S6.74,39.172,6.693,38.772z"/>
       <path xmlns="http://www.w3.org/2000/svg" fill="#808080" d="M14.815,39.936L14.13,39.936L14.13,37.35c-0.251,0.234,-0.547,0.408,-0.887,0.521l0,-0.622c0.179,-0.059,0.373,-0.17,0.584,-0.334c0.209,-0.163,0.354,-0.354,0.432,-0.572l0.557,0L14.816,39.936z"/>
       <path xmlns="http://www.w3.org/2000/svg" fill="#808080" d="M20,36.342c0.347,0,0.618,0.124,0.813,0.371c0.232,0.293,0.349,0.779,0.349,1.457s-0.117,1.164,-0.352,1.461c-0.193,0.244,-0.464,0.365,-0.811,0.365c-0.349,0,-0.629,-0.134,-0.843,-0.401c-0.213,-0.268,-0.319,-0.745,-0.319,-1.432c0,-0.674,0.117,-1.159,0.352,-1.455C19.383,36.464,19.653,36.342,20,36.342zM20,36.91c-0.083,0,-0.157,0.027,-0.222,0.08c-0.065,0.053,-0.116,0.147,-0.152,0.284c-0.047,0.178,-0.07,0.476,-0.07,0.896s0.021,0.709,0.063,0.866s0.096,0.262,0.16,0.313s0.138,0.078,0.221,0.078s0.157,-0.026,0.222,-0.079c0.065,-0.053,0.116,-0.147,0.152,-0.284c0.047,-0.176,0.07,-0.475,0.07,-0.895s-0.021,-0.708,-0.063,-0.865s-0.096,-0.262,-0.16,-0.314S20.083,36.91,20,36.91z"/>
       <path xmlns="http://www.w3.org/2000/svg" fill="#808080" d="M25.21,38.004c-0.178,-0.074,-0.307,-0.178,-0.387,-0.309c-0.081,-0.131,-0.121,-0.274,-0.121,-0.431c0,-0.267,0.093,-0.487,0.279,-0.661c0.187,-0.175,0.451,-0.262,0.795,-0.262c0.34,0,0.604,0.087,0.792,0.262c0.188,0.174,0.282,0.395,0.282,0.661c0,0.166,-0.043,0.313,-0.129,0.443c-0.087,0.129,-0.208,0.228,-0.364,0.296c0.198,0.08,0.35,0.196,0.453,0.35s0.155,0.33,0.155,0.529c0,0.331,-0.105,0.6,-0.316,0.807c-0.211,0.206,-0.491,0.31,-0.842,0.31c-0.325,0,-0.596,-0.085,-0.813,-0.257c-0.256,-0.201,-0.383,-0.479,-0.383,-0.83c0,-0.193,0.048,-0.371,0.144,-0.533S25.003,38.092,25.21,38.004zM25.288,38.847c0,0.188,0.049,0.336,0.146,0.442c0.097,0.105,0.218,0.158,0.362,0.158c0.142,0,0.259,-0.051,0.352,-0.152s0.139,-0.249,0.139,-0.441c0,-0.167,-0.047,-0.302,-0.141,-0.403c-0.095,-0.102,-0.215,-0.153,-0.359,-0.153c-0.168,0,-0.293,0.059,-0.375,0.174S25.288,38.712,25.288,38.847zM25.351,37.314c0,0.137,0.039,0.243,0.116,0.319c0.077,0.077,0.18,0.115,0.309,0.115c0.13,0,0.234,-0.039,0.313,-0.116s0.117,-0.185,0.117,-0.321c0,-0.128,-0.039,-0.231,-0.116,-0.309s-0.179,-0.115,-0.306,-0.115c-0.133,0,-0.237,0.039,-0.315,0.117S25.351,37.185,25.351,37.314z"/>
       <path xmlns="http://www.w3.org/2000/svg" fill="#808080" d="M31.36,39.936l0,-2.974l-1.063,0l0,-0.605l2.844,0l0,0.605l-1.059,0l0,2.974L31.36,39.936z"/>
       <path xmlns="http://www.w3.org/2000/svg" fill="#808080" d="M37.615,36.342c0.348,0,0.617,0.124,0.813,0.371c0.234,0.293,0.35,0.779,0.35,1.457s-0.117,1.164,-0.352,1.461c-0.193,0.244,-0.463,0.365,-0.811,0.365s-0.629,-0.134,-0.842,-0.401s-0.32,-0.745,-0.32,-1.432c0,-0.674,0.117,-1.159,0.352,-1.455C36.998,36.464,37.269,36.342,37.615,36.342zM37.615,36.91c-0.082,0,-0.156,0.027,-0.223,0.08c-0.064,0.053,-0.115,0.147,-0.15,0.284c-0.047,0.178,-0.07,0.476,-0.07,0.896s0.021,0.709,0.063,0.866c0.043,0.157,0.096,0.262,0.16,0.313s0.139,0.078,0.221,0.078c0.084,0,0.158,-0.026,0.223,-0.079s0.115,-0.147,0.15,-0.284c0.049,-0.176,0.072,-0.475,0.072,-0.895s-0.021,-0.708,-0.064,-0.865c-0.041,-0.157,-0.096,-0.262,-0.16,-0.314S37.699,36.91,37.615,36.91z"/>
       <path xmlns="http://www.w3.org/2000/svg" fill="#808080" d="M44.552,39.299l0,0.637l-2.404,0c0.025,-0.241,0.104,-0.469,0.234,-0.685s0.387,-0.502,0.771,-0.858c0.309,-0.288,0.498,-0.483,0.568,-0.586c0.096,-0.142,0.143,-0.281,0.143,-0.42c0,-0.153,-0.041,-0.271,-0.123,-0.353S43.545,36.91,43.4,36.91c-0.143,0,-0.256,0.044,-0.342,0.13c-0.084,0.086,-0.133,0.229,-0.146,0.43l-0.684,-0.068c0.041,-0.378,0.168,-0.648,0.383,-0.813c0.215,-0.164,0.484,-0.246,0.807,-0.246c0.354,0,0.631,0.096,0.832,0.285c0.203,0.191,0.303,0.428,0.303,0.711c0,0.161,-0.029,0.314,-0.086,0.46c-0.059,0.146,-0.15,0.299,-0.275,0.458c-0.082,0.105,-0.232,0.258,-0.449,0.457c-0.217,0.198,-0.354,0.33,-0.41,0.395c-0.059,0.065,-0.105,0.129,-0.141,0.191L44.552,39.3z"/>
       <path xmlns="http://www.w3.org/2000/svg" fill="#808080" d="M6.993,42.377c-0.106,-0.045,-0.184,-0.107,-0.232,-0.186c-0.048,-0.079,-0.072,-0.165,-0.072,-0.259c0,-0.16,0.056,-0.292,0.168,-0.397c0.111,-0.104,0.271,-0.156,0.477,-0.156c0.204,0,0.362,0.053,0.476,0.156c0.112,0.105,0.169,0.237,0.169,0.397c0,0.1,-0.026,0.188,-0.078,0.266c-0.052,0.078,-0.124,0.138,-0.218,0.179c0.119,0.048,0.21,0.117,0.271,0.209c0.063,0.092,0.093,0.197,0.093,0.318c0,0.198,-0.063,0.359,-0.189,0.482c-0.126,0.125,-0.295,0.187,-0.504,0.187c-0.196,0,-0.358,-0.052,-0.488,-0.153c-0.153,-0.121,-0.23,-0.287,-0.23,-0.498c0,-0.116,0.029,-0.224,0.087,-0.32C6.778,42.504,6.869,42.43,6.993,42.377zM7.04,42.882c0,0.113,0.029,0.202,0.087,0.265c0.059,0.064,0.131,0.096,0.218,0.096c0.085,0,0.155,-0.03,0.211,-0.092c0.056,-0.061,0.084,-0.148,0.084,-0.264c0,-0.101,-0.029,-0.182,-0.086,-0.243c-0.057,-0.061,-0.128,-0.091,-0.215,-0.091c-0.101,0,-0.176,0.034,-0.225,0.104C7.064,42.726,7.04,42.801,7.04,42.882zM7.078,41.962c0,0.082,0.023,0.146,0.069,0.192c0.047,0.046,0.108,0.068,0.186,0.068c0.078,0,0.141,-0.023,0.188,-0.069c0.047,-0.047,0.07,-0.11,0.07,-0.192c0,-0.077,-0.023,-0.14,-0.069,-0.186c-0.047,-0.047,-0.108,-0.07,-0.185,-0.07c-0.078,0,-0.142,0.023,-0.188,0.07S7.078,41.885,7.078,41.962z"/>
       <path xmlns="http://www.w3.org/2000/svg" fill="#808080" d="M12.135,43.535l-0.471,0l-0.188,-0.488l-0.859,0l-0.177,0.488l-0.46,0l0.836,-2.147l0.459,0L12.135,43.535zM11.338,42.686l-0.296,-0.797l-0.29,0.797L11.338,42.686z"/>
       <path xmlns="http://www.w3.org/2000/svg" fill="#808080" d="M15.128,43.535l-0.412,0l0,-1.551c-0.15,0.141,-0.327,0.244,-0.531,0.312l0,-0.374c0.107,-0.035,0.225,-0.102,0.35,-0.199c0.127,-0.099,0.213,-0.213,0.26,-0.344l0.334,0L15.129,43.535z"/>
       <path xmlns="http://www.w3.org/2000/svg" fill="#808080" d="M18.933,43.153l0,0.383l-1.442,0c0.015,-0.145,0.062,-0.281,0.141,-0.411c0.077,-0.129,0.231,-0.301,0.463,-0.515c0.185,-0.173,0.299,-0.29,0.341,-0.352c0.057,-0.085,0.085,-0.169,0.085,-0.252c0,-0.092,-0.024,-0.162,-0.074,-0.212c-0.049,-0.049,-0.117,-0.073,-0.204,-0.073c-0.086,0,-0.154,0.025,-0.205,0.077s-0.08,0.138,-0.088,0.258l-0.41,-0.041c0.024,-0.227,0.101,-0.389,0.229,-0.487s0.291,-0.148,0.484,-0.148c0.211,0,0.378,0.057,0.499,0.172c0.121,0.113,0.182,0.256,0.182,0.426c0,0.097,-0.018,0.188,-0.052,0.276c-0.035,0.087,-0.09,0.179,-0.165,0.274c-0.05,0.063,-0.14,0.155,-0.27,0.273c-0.13,0.12,-0.212,0.199,-0.247,0.238c-0.034,0.039,-0.063,0.077,-0.084,0.113L18.933,43.152z"/>
       <path xmlns="http://www.w3.org/2000/svg" fill="#808080" d="M21.018,42.983l0.41,-0.042c0.012,0.093,0.046,0.166,0.104,0.221c0.058,0.054,0.124,0.081,0.199,0.081c0.086,0,0.158,-0.035,0.219,-0.104c0.059,-0.07,0.089,-0.175,0.089,-0.315c0,-0.133,-0.029,-0.231,-0.089,-0.297c-0.059,-0.066,-0.136,-0.1,-0.23,-0.1c-0.118,0,-0.225,0.053,-0.318,0.157l-0.334,-0.048l0.211,-1.118l1.089,0l0,0.386l-0.776,0l-0.064,0.364c0.092,-0.046,0.186,-0.069,0.281,-0.069c0.183,0,0.337,0.067,0.465,0.199c0.126,0.134,0.189,0.306,0.189,0.518c0,0.177,-0.051,0.335,-0.153,0.473c-0.14,0.19,-0.334,0.285,-0.581,0.285c-0.199,0,-0.36,-0.054,-0.485,-0.16S21.042,43.163,21.018,42.983z"/>
       <path xmlns="http://www.w3.org/2000/svg" fill="#808080" d="M25.118,43.535l-0.768,-2.147l0.471,0l0.543,1.589l0.526,-1.589l0.46,0l-0.77,2.147L25.118,43.535z"/>
       <path xmlns="http://www.w3.org/2000/svg" fill="#808080" d="M29.747,42.746l0.42,0.133c-0.064,0.234,-0.172,0.408,-0.321,0.522c-0.15,0.113,-0.341,0.171,-0.571,0.171c-0.285,0,-0.52,-0.098,-0.703,-0.293c-0.184,-0.194,-0.275,-0.461,-0.275,-0.799c0,-0.357,0.093,-0.635,0.277,-0.833c0.185,-0.197,0.427,-0.296,0.729,-0.296c0.262,0,0.476,0.077,0.64,0.232c0.098,0.092,0.171,0.224,0.22,0.396l-0.43,0.103c-0.025,-0.111,-0.078,-0.199,-0.158,-0.264c-0.081,-0.064,-0.179,-0.097,-0.294,-0.097c-0.159,0,-0.288,0.058,-0.388,0.171c-0.099,0.115,-0.148,0.3,-0.148,0.556c0,0.271,0.049,0.465,0.146,0.58s0.225,0.173,0.381,0.173c0.115,0,0.214,-0.037,0.297,-0.109C29.65,43.018,29.71,42.904,29.747,42.746z"/>
       <path xmlns="http://www.w3.org/2000/svg" fill="#808080" d="M34.273,43.535l-0.471,0l-0.188,-0.488l-0.858,0l-0.177,0.488l-0.46,0l0.836,-2.147l0.458,0L34.273,43.535zM33.476,42.686l-0.296,-0.797l-0.29,0.797L33.476,42.686z"/>
       <path xmlns="http://www.w3.org/2000/svg" fill="#808080" d="M39.131,43.535l-0.512,-2.147l0.443,0l0.324,1.476l0.393,-1.476l0.516,0l0.377,1.5l0.328,-1.5l0.438,0l-0.521,2.147l-0.461,0l-0.428,-1.605l-0.426,1.605L39.131,43.535z"/>
       <path xmlns="http://www.w3.org/2000/svg" fill="#808080" d="M43.371,42.475c0,-0.219,0.033,-0.402,0.098,-0.551c0.049,-0.109,0.115,-0.207,0.201,-0.295c0.084,-0.086,0.176,-0.15,0.277,-0.193c0.133,-0.056,0.287,-0.084,0.463,-0.084c0.316,0,0.568,0.098,0.76,0.294c0.189,0.196,0.283,0.47,0.283,0.819c0,0.347,-0.094,0.617,-0.281,0.813c-0.189,0.195,-0.441,0.294,-0.756,0.294c-0.32,0,-0.574,-0.098,-0.762,-0.293C43.465,43.085,43.371,42.817,43.371,42.475zM43.818,42.46c0,0.243,0.055,0.428,0.168,0.553c0.111,0.126,0.254,0.188,0.428,0.188c0.172,0,0.314,-0.063,0.426,-0.187c0.111,-0.125,0.166,-0.312,0.166,-0.561c0,-0.246,-0.055,-0.43,-0.162,-0.551s-0.252,-0.182,-0.43,-0.182c-0.18,0,-0.322,0.062,-0.432,0.184C43.873,42.029,43.818,42.213,43.818,42.46z"/>
      </g>
      <circle xmlns="http://www.w3.org/2000/svg" cx="62.631" cy="28.369" r="1.631"/>
      <circle xmlns="http://www.w3.org/2000/svg" cx="3.269" cy="28.369" r="1.631"/>
      <g xmlns="http://www.w3.org/2000/svg">
       <path xmlns="http://www.w3.org/2000/svg" opacity="0.2" fill="#FFFFFF" d="M0,26.422l25.412,0c1.288,2.846,4.146,4.83,7.474,4.83c3.327,0,6.184,-1.984,7.473,-4.83l25.412,0l0,-0.299L40.359,26.123c-1.289,2.846,-4.146,4.83,-7.473,4.83c-3.328,0,-6.187,-1.984,-7.474,-4.83L0,26.123L0,26.422z"/>
       <path xmlns="http://www.w3.org/2000/svg" opacity="0.2" fill="#FFFFFF" d="M29.172,20.069c0.633,1.377,2.099,2.52,3.714,2.52c1.613,0,3.08,-1.143,3.713,-2.52l-0.082,-0.193c-0.635,1.377,-2.018,2.338,-3.631,2.338c-1.615,0,-2.998,-0.961,-3.631,-2.338L29.172,20.069z"/>
       <rect xmlns="http://www.w3.org/2000/svg" width="50.456" x="7.659" opacity="0.2" y="0" fill="#FFFFFF" height="0.75"/>
      </g>
      <path xmlns="http://www.w3.org/2000/svg" d="M28.882,21.854c0,2.211,1.792,4.004,4.004,4.004c2.211,0,4.004,-1.793,4.004,-4.004l0,-0.313c0,2.211,-1.793,4.004,-4.004,4.004c-2.212,0,-4.004,-1.793,-4.004,-4.004L28.882,21.854z"/>
     </g>
    </g>
    </g></g></g><path stroke='#8c8c8c' stroke-width='2.15136' stroke-linecap='round' stroke-linejoin='round' fill='none' d='M280.049,46.8016L255.433,46.8016' />
    <path stroke='#8c8c8c' stroke-width='2.15136' stroke-linecap='round' stroke-linejoin='round' fill='none' d='M280.049,54.0037L255.433,54.0037' />
    <g partID='18458240'><g transform='translate(309.256,42.2749)' ><g transform='matrix(0,1,-1,0,0,0)'  ><g xmlns="http://www.w3.org/2000/svg" id="breadboard">
     <rect xmlns="http://www.w3.org/2000/svg" width="2.15208" x="3.45096" y="25.421" fill="none" height="0.72" id="connector0pin"/>
     <rect xmlns="http://www.w3.org/2000/svg" width="2.15424" x="10.651" y="25.421" fill="none" height="0.72" id="connector1pin"/>
     <g xmlns="http://www.w3.org/2000/svg" fill="none" stroke="#8C8C8C" id="connector0leg" stroke-linecap="round" y1="40.565" x1="6.287" y2="74.754" stroke-width="2.15136" x2="6.287"/>
     <g xmlns="http://www.w3.org/2000/svg" fill="none" stroke="#8C8C8C" id="connector1leg" stroke-linecap="round" y1="40.565" x1="16.29" y2="74.754" stroke-width="2.15136" x2="16.29"/>
     <rect xmlns="http://www.w3.org/2000/svg" width="2.15136" x="3.45096" y="19.3795" fill="#8C8C8C" height="9.82728"/>
     <path xmlns="http://www.w3.org/2000/svg" fill="#8C8C8C" d="M12.8045,29.2068c0,-1.1736,-1.06488,-2.1024,-2.088,-2.9916c-0.41616,-0.3672,-1.19952,-1.00152,-1.19952,-1.42488l0,-5.47056l-2.16144,0l0,5.78016c0,1.0584,0.94752,1.87848,1.94616,2.74824c0.44424,0.37584,1.34856,1.24992,1.34856,1.76976"/>
     <g xmlns="http://www.w3.org/2000/svg" id="g12">
      <path xmlns="http://www.w3.org/2000/svg" opacity="0.3" fill="#e60000" id="color_path14" d="M14.1732,13.001L14.1732,7.0884C14.1732,3.1752,11.0052,0,7.08768,0C3.1752,0,0,3.16944,0,7.0884l0,13.649c1.47384,1.65096,4.0968,2.75256,7.08768,2.75256c4.61952,0,8.36856,-2.61792,8.36856,-5.85936l0,-1.52352C15.4555,14.9645,14.9818,13.9032,14.1732,13.001z"/>
      <path xmlns="http://www.w3.org/2000/svg" opacity="0.5" fill="#E6E6E6" id="path16" d="M14.1732,13.001L14.1732,7.0884C14.1732,3.1752,11.0052,0,7.08768,0C3.1752,0,0,3.16944,0,7.0884l0,13.649c1.47384,1.65096,4.0968,2.75256,7.08768,2.75256c4.61952,0,8.36856,-2.61792,8.36856,-5.85936l0,-1.52352C15.4555,14.9645,14.9818,13.9032,14.1732,13.001z"/>
      <path xmlns="http://www.w3.org/2000/svg" opacity="0.9" fill="#D1D1D1" id="path18" d="M14.1732,13.001l0,3.10536c0,2.73888,-3.16584,4.96512,-7.08552,4.96512C3.1752,21.0715,0,18.8525,0,16.1064l0,3.10536L0,20.736c1.47384,1.65168,4.0968,2.75256,7.08768,2.75256c4.61952,0,8.36856,-2.61792,8.36856,-5.85864L15.4562,16.1064C15.4555,14.9645,14.9818,13.9032,14.1732,13.001z"/>
      <path xmlns="http://www.w3.org/2000/svg" opacity="0.7" fill="#e60000" id="color_path20" d="M14.1732,13.001l0,3.10536c0,2.73888,-3.16584,4.96512,-7.08552,4.96512C3.1752,21.0715,0,18.8525,0,16.1064l0,3.10536L0,20.736c1.47384,1.65168,4.0968,2.75256,7.08768,2.75256c4.61952,0,8.36856,-2.61792,8.36856,-5.85864L15.4562,16.1064C15.4555,14.9645,14.9818,13.9032,14.1732,13.001z"/>
      <path xmlns="http://www.w3.org/2000/svg" opacity="0.25" fill="#e60000" id="color_path22" d="M14.1732,13.001l0,3.10536c0,2.73888,-3.16584,4.96512,-7.08552,4.96512C3.1752,21.0715,0,18.8525,0,16.1064l0,3.10536c1.47384,1.65024,4.0968,2.75256,7.08768,2.75256c4.61952,0,8.36856,-2.61792,8.36856,-5.85864C15.4555,14.9645,14.9818,13.9032,14.1732,13.001z"/>
      <ellipse xmlns="http://www.w3.org/2000/svg" opacity="0.25" fill="#E6E6E6" cx="7.08768" cy="16.1064" rx="7.08696" ry="4.9608" id="ellipse24"/>
      <ellipse xmlns="http://www.w3.org/2000/svg" opacity="0.25" fill="#e60000" cx="7.08768" cy="16.1064" rx="7.08696" ry="4.9608" id="color_ellipse26"/>
      <polygon xmlns="http://www.w3.org/2000/svg" fill="#666666" points="2.2032,9.648,2.2032,16.1071,3.19608,16.1071,3.19608,13.0946,6.0156,13.0946,10.0123,8.80488,3.40704,8.80488" id="polygon28"/>
      <polygon xmlns="http://www.w3.org/2000/svg" fill="#666666" points="10.7784,8.52408,11.2147,9.03384,7.41168,13.0946,11.0599,13.0946,11.0599,16.1071,11.9736,16.1071,11.9736,8.52408" id="polygon30"/>
      <path xmlns="http://www.w3.org/2000/svg" opacity="0.65" fill="#e60000" id="color_path32" d="M14.1732,13.001L14.1732,7.0884C14.1732,3.1752,11.0052,0,7.08768,0C3.1752,0,0,3.16944,0,7.0884l0,13.649c1.47384,1.65096,4.0968,2.75256,7.08768,2.75256c4.61952,0,8.36856,-2.61792,8.36856,-5.85936l0,-1.52352C15.4555,14.9645,14.9818,13.9032,14.1732,13.001z"/>
      <path xmlns="http://www.w3.org/2000/svg" opacity="0.5" fill="#FFFFFF" id="path34" d="M10.3882,3.75408l1.4364,-0.2736c-0.84168,-1.13184,-2.08224,-1.95768,-3.54168,-2.23848l0.25416,1.08072C9.30096,2.59344,9.94392,3.1032,10.3882,3.75408z"/>
      <path xmlns="http://www.w3.org/2000/svg" opacity="0.5" fill="#FFFFFF" id="path36" d="M0.76824,19.926l0,1.51992c0.64872,0.5292,1.43352,0.97632,2.3076,1.31688l0,-1.52496C2.19744,20.9016,1.41912,20.4559,0.76824,19.926z"/>
      <path xmlns="http://www.w3.org/2000/svg" opacity="0.5" fill="#FFFFFF" id="path38" d="M11.0729,20.2097c-0.2556,0.1224,-0.52992,0.22968,-0.80568,0.32976c-0.05832,0.01944,-0.11736,0.04032,-0.17784,0.05832c-0.56376,0.17928,-1.16136,0.31896,-1.79496,0.39456c-0.07488,0.00936,-0.1512,0.01872,-0.22464,0.01944c-0.3204,0.03024,-0.64368,0.05832,-0.97056,0.05832c-0.14832,0,-0.30744,-0.01512,-0.4716,-0.02376c-1.20024,-0.05688,-2.33064,-0.31464,-3.2976,-0.73944L3.33,11.9174L3.33,7.092c0,-1.47096,0.84816,-2.72952,2.0736,-3.34944L5.38128,3.68928l-1.24776,-1.512c-1.66968,1.00296,-2.79,2.8224,-2.79,4.91184l0,11.9052c-0.04968,-0.04968,-0.30816,-0.30888,-0.48024,-0.52992l-0.30744,0.6876c1.40112,1.48176,3.8088,2.46168,6.54264,2.46168c1.67976,0,3.23712,-0.37368,4.51152,-1.00224l-0.52704,-0.40896C11.0729,20.2097,11.0729,20.2097,11.0729,20.2097z"/>
     </g>
    </g>
    </g></g></g><g partID='18459930'><g transform='translate(375.627,176.482)' ><g xmlns="http://www.w3.org/2000/svg" id="breadboard">
     <text xmlns="http://www.w3.org/2000/svg" xml:space="preserve" xmlns:xml="http://www.w3.org/XML/1998/namespace" x="39.6" y="6.48" fill="#787878" font-family="Droid Sans" text-anchor="middle" id="label" stroke-width="0" font-size="7.2">Door buzzer</text>
    </g>
    </g></g><g partID='18458460'><line stroke-linecap='round' stroke='#8c0000' x1='233.854' y1='3.47087' x2='176.21' y2='3.47087' stroke-width='3.2' /><line stroke-linecap='round' stroke='#cc1414' x1='233.854' y1='3.47087' x2='176.21' y2='3.47087' stroke-width='1.6' /></g><g partID='18452900'><line stroke-linecap='round' stroke='#8c0000' x1='176.21' y1='3.47087' x2='147.433' y2='156.961' stroke-width='3.2' /><line stroke-linecap='round' stroke='#cc1414' x1='176.21' y1='3.47087' x2='147.433' y2='156.961' stroke-width='1.6' /></g><g partID='18452830'><line stroke-linecap='round' stroke='#8c0000' x1='233.833' y1='46.8021' x2='233.853' y2='3.47103' stroke-width='3.2' /><line stroke-linecap='round' stroke='#cc1414' x1='233.833' y1='46.8021' x2='233.853' y2='3.47103' stroke-width='1.6' /></g><g partID='18457700'><line stroke-linecap='round' stroke='#00a527' x1='10.7656' y1='111.272' x2='10.6328' y2='154.082' stroke-width='3.2' /><line stroke-linecap='round' stroke='#25cc35' x1='10.7656' y1='111.272' x2='10.6328' y2='154.082' stroke-width='1.6' /></g><g partID='18457640'><line stroke-linecap='round' stroke='#00a527' x1='212.233' y1='195.321' x2='10.7656' y2='111.272' stroke-width='3.2' /><line stroke-linecap='round' stroke='#25cc35' x1='212.233' y1='195.321' x2='10.7656' y2='111.272' stroke-width='1.6' /></g><g partID='18457770'><line stroke-linecap='round' stroke='#000000' x1='10.7656' y1='183.887' x2='10.6328' y2='161.28' stroke-width='3.2' /><line stroke-linecap='round' stroke='#404040' x1='10.7656' y1='183.887' x2='10.6328' y2='161.28' stroke-width='1.6' /></g><g partID='18457670'><line stroke-linecap='round' stroke='#000000' x1='205.033' y1='209.721' x2='10.7656' y2='183.887' stroke-width='3.2' /><line stroke-linecap='round' stroke='#404040' x1='205.033' y1='209.721' x2='10.7656' y2='183.887' stroke-width='1.6' /></g><g partID='18457790'><line stroke-linecap='round' stroke='#00a527' x1='248.233' y1='61.2021' x2='212.233' y2='51.3221' stroke-width='3.2' /><line stroke-linecap='round' stroke='#25cc35' x1='248.233' y1='61.2021' x2='212.233' y2='51.3221' stroke-width='1.6' /></g><g partID='18458000'><line stroke-linecap='round' stroke='#1b5bb3' x1='305.721' y1='82.8245' x2='255.433' y2='75.6021' stroke-width='3.2' /><line stroke-linecap='round' stroke='#418dd9' x1='305.721' y1='82.8245' x2='255.433' y2='75.6021' stroke-width='1.6' /></g><g partID='18457860'><line stroke-linecap='round' stroke='#1b5bb3' x1='305.833' y1='162.001' x2='305.72' y2='82.8242' stroke-width='3.2' /><line stroke-linecap='round' stroke='#418dd9' x1='305.833' y1='162.001' x2='305.72' y2='82.8242' stroke-width='1.6' /></g><g partID='18458100'><line stroke-linecap='round' stroke='#000000' x1='298.983' y1='104.534' x2='298.633' y2='169.201' stroke-width='3.2' /><line stroke-linecap='round' stroke='#404040' x1='298.983' y1='104.534' x2='298.633' y2='169.201' stroke-width='1.6' /></g><g partID='18457930'><line stroke-linecap='round' stroke='#000000' x1='205.033' y1='101.722' x2='298.983' y2='104.534' stroke-width='3.2' /><line stroke-linecap='round' stroke='#404040' x1='205.033' y1='101.722' x2='298.983' y2='104.534' stroke-width='1.6' /></g><g partID='18458520'><line stroke-linecap='round' stroke='#8c0000' x1='241.033' y1='68.4021' x2='241.033' y2='54.0021' stroke-width='3.2' /><line stroke-linecap='round' stroke='#cc1414' x1='241.033' y1='68.4021' x2='241.033' y2='54.0021' stroke-width='1.6' /></g><g partID='18459990'><line stroke-linecap='round' stroke='#1b5bb3' x1='428.111' y1='212.445' x2='313.033' y2='212.401' stroke-width='3.2' /><line stroke-linecap='round' stroke='#418dd9' x1='428.111' y1='212.445' x2='313.033' y2='212.401' stroke-width='1.6' /></g><g partID='18459960'><line stroke-linecap='round' stroke='#1b5bb3' x1='428.111' y1='193.403' x2='428.111' y2='212.445' stroke-width='3.2' /><line stroke-linecap='round' stroke='#418dd9' x1='428.111' y1='193.403' x2='428.111' y2='212.445' stroke-width='1.6' /></g><g partID='18460070'><line stroke-linecap='round' stroke='#1b5bb3' x1='400.228' y1='192.043' x2='400.908' y2='198.164' stroke-width='3.2' /><line stroke-linecap='round' stroke='#418dd9' x1='400.228' y1='192.043' x2='400.908' y2='198.164' stroke-width='1.6' /></g><g partID='18460100'><line stroke-linecap='round' stroke='#1b5bb3' x1='400.908' y1='198.164' x2='313.033' y2='198.001' stroke-width='3.2' /><line stroke-linecap='round' stroke='#418dd9' x1='400.908' y1='198.164' x2='313.033' y2='198.001' stroke-width='1.6' /></g></svg>
