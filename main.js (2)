let leds = document.querySelectorAll(".led"); // यह सभी 7 LEDs की एक लिस्ट (NodeList) बना देगा

let allOn=document.querySelector(".allOn");
let allOff=document.querySelector(".allOff");
let blink=document.querySelector(".blink");


allOn.addEventListener("click",function () {
  leds.forEach(function(singleLed){singleLed.style.backgroundColor="red";
});
});

allOff.addEventListener("click",function () {
  leds.forEach(function(singleLed){singleLed.style.backgroundColor="#444";
  clearInterval(blinkTimer);

});
});


// यह वेरिएबल याद रखेगा कि इस समय LED ऑन है या ऑफ
let isOn = false; 
let blinkTimer=null;
blink.addEventListener("click", function () {
  
  // setInterval कंप्यूटर को बोलेगा कि हर 500ms (आधे सेकंड) बाद अंदर का काम करो
 blinkTimer=setInterval(function () {
    
    if (isOn === false) {
      // अगर LEDs बंद हैं, तो सबको एक साथ चालू (लाल) कर दो
      leds.forEach(function (singleLed) {
        singleLed.style.backgroundColor = "red";
      });
      isOn = true; // कंप्यूटर को याद दिलाओ कि अब LEDs चालू हो चुकी हैं
    } 
    else {
      // अगर LEDs चालू हैं, तो सबको एक साथ बंद (गहरा ग्रे) कर दो
      leds.forEach(function (singleLed) {
        singleLed.style.backgroundColor = "#444";
      });
      isOn = false; // कंप्यूटर को याद दिलाओ कि अब LEDs बंद हो चुकी हैं
    }

  }, 100); // 500 मिलीसेकंड का मतलब है आधा सेकंड का डिले (Delay)

});
