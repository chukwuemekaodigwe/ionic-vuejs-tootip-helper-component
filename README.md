# ionic-vuejs-tootip-helper-component
This is a helper vue component to enable vue developers easily add tootip feature to their Ionic site. Ionic Developers didn't create the feature

It can easily be customized using props;

Here the props definitions:
fontSize: {
      type: String,
      default: '1em'
    },
    iconColor: {
      type: String,
      default: 'blue'
    },

    isOutline: {
      default: true,
      type: Boolean
      /* To select the type of icon to use: either information-circle-outline or information-circle-sharp */
    },
    bgColor: {
      default: '#000',
      type: String
    },
    textColor: {
      type: String,
      default: 'red'
    },
    message: {
      type: String
    },
    for:{
      type: String,
      /* This is an identifier for that specofic tooltiip. It enables the use of multiple tooltips on this same page*/
    }

** Usage Below

-- Import to page as 

[import tooltip from "./ionic-tooltip.vue";]


[<tooltip for="email" font-size="36px" bg-color="darkblue" icon-color="blue" text-color="white"
                        message="write on the company address" :is-outline="false"></tooltip>]
                        
                        
***Refer to the sample page on this repo to see use cases ***

Thanks
