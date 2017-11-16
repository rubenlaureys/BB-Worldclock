# BB-Worldclock

1. Execute the following commands to install the module:

cd ~/MagicMirror/modules # navigate to module folder
git clone https://github.com/rubenlaureys/BB-Worldclock # clone this repository

2. Then, add the following into the modules section of your config/config.js file:

{
  module: 'worldclock',
  
  position: 'top_left', // This can be any of the regions, best results in top_left or top_right regions
  
  config: {
    // See 'Configuration options' for more information.

    timeFormat: 'HH:mm A', //defined in moment.js format()
    style: 'top', //predefined 4 styles; 'top', 'left','right','bottom'
    clocks: [
      {
        title: "Home",
      },
      {
        title: "HOLLYWOOD", // Too long title could cause ugly text align.
        timezone: "America/Los_Angeles", //When omitted, Localtime will be displayed. It might be not your purporse, I bet.
        flag: "us",
      },
      {
        timezone: "Asia/Seoul",
      },
    ]
  }
},
