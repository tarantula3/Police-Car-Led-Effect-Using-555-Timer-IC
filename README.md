# Police Car Led Effect Using 555 Timer IC
In this tutorial I am going to create a Police Light themed LED Flashing circuit using the 555 timer IC.

[![4vDtWafMF0M](https://img.youtube.com/vi/4vDtWafMF0M/0.jpg)](https://www.youtube.com/watch?v=4vDtWafMF0M)

My 5-year old son asked me to create a Police Car like flashing light that he can put on top of his nerf-gun, while playing around with his mates. No worries mate, sounds like a plan to me. Bang, weekend sorted.

In this tutorial I am going to create a Police Light themed LED Flashing circuit using the 555 timer IC. This circuit alternatively flashes between the Red and the Blue LED's while blinking each of them individually similar to the police strobe lights. To add some spice to this project you can also add a police siren to this circuit. However, I just wanted to keep it simple.

Watch this video for detailed step by step instructions on how to build this circuit and for a complete instruction on how the circuit works.
Disclaimer: This tutorial and the linked video are for educational purposes only.


Components Required
-------------------
![image](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEiwO1yn9ZcLeXeB45VwveELjOVI1NdodMC3st6vpNJLU0UszvPWu8V-_uf884cueHoafQ4rqz7dg5Qd1VGCxwPLTv8hvi8Mirz1Kq86122i2y1wSESWsnoBgLK0MtiZNgy-h6BDUYrXMCDsAtoQ5Md5HtcH53HfGK_P0cltvwb_ADrI-fiiYJjPQLHN/w640-h360/4.png)

For this project we need:

6 x RED LEDs
6 x Blue LEDs
2 x 555 Timer ICs
2 x 1K Resistors
1 x 680K Resistor
1 x 100K Resistor
1 x 10uf Capacitor and
1 x 100nF Ceramic Capacitor (104)

Depending upon the input voltage and the way you connect the LEDs (series or parallel) you will have to use different values of resistors in series with your LED’s. Please checkout http://ledcalc.com/ to calculate the resistor values based on your LED arrangements.


How The Circuit Works
---------------------
Now, let's try to understand how this circuit works.

This circuit has 2 parts.
	Part 1: Where the Blue and Red LEDs alternate and flash at a regular interval
	Part 2: Where a cluster of similar color LEDs flash like a strobe light

In my previous tutorial "Adjustable Single/Dual LED Flasher Using 555 Timer IC", I showed you guys how to configure 555 timer IC to operate in an astable mode. In astable mode, the 555 timer IC acts as an oscillator (re-triggering itself) generating square waves [PWM Signals] from the output pin no. 3. Later I also showed you guys how to connect 2 LED’s in opposite polarity at the output pin Pin-3 so that they toggle ON and OFF at regular intervals of time.

![image](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgEe29HWqrMZczpDeBNCSeYr_8SkwF1ykBHWFws0v6CnZCpOfuFP_dn7WvyVYa2I40dJQGNwwSSSaJBslwYqtvU35NLGO5wm7U5wWVLyCJqf-cNOA2q9fSoG44h6huhUGIEztVtEgANlqlEqVaPzMrk-59ilodth6fe9YQVXeHWKKj0cVT8yyaNONyC/w640-h360/5.png)

In this tutorial, I am using two copies of the previously shown "astable circuit" configured at different frequencies. 
	The first 555 timer IC, uses a higher value capacitor and hence it takes more time to toggle the output. 
	The second 555 timer IC uses a lower value capacitor and hence it toggles the output very fast.
So, pretty much that's exactly what we want. The 1st 555 timer IC will help us in toggling between the LED clusters and the 2nd 555 timer IC will produce the strobe light effect. 

![image](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEiGCY5V8soBr8BklxFZi37nRVNCjexSdKICZaOq2c9oPe9E5WT91x98MskkSBtEF3wJLCUKRrQhMNjJ6pgW7c3hiDSca3bJkt045UQ_yJ_MWGa8zzsgx7Bc8EB8Y-ccGmEwv_K8T7v3m7WN73dmLxHV9sOzUlQwDZjGbxmcoVoDxqUhXIyuXzdwJaK4/w640-h360/7.png)

Now, lets connect the LED clusters to this circuit. The first LED cluster of the Red LED’s turns ON when the anode receives a positive voltage and the cathode is grounded. This happens when the output of first 555 timer IC is ON and at the same time the output of second 555 timer IC is OFF.

![image](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEiDXzjWU8bkMnVFbLG5LsS3WfaWugtxb3-p38YrdGT1QLz_Z5dOFODVN36w12ETwQbS10XMY1r_mai9WqWIyrvcoZkKEfCXpSa1VqBzf90DELpJHnTWe_UpHL1PHae4L0yOM0NA2z2YCBiz9TW-x4tBLB_KoAu2XafDinayXb7JsB9OP7ClUVcLW6h9/w640-h360/8.png)

Similarly, the second cluster of the Blue LED’s turn ON only when the output of the first 555 timer IC is OFF and the output of the second 555 timer IC is ON.

![image](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjU-clCajS0LsrGm-sFV79CABdWKpUUO7d_VOkRFsLIaiynoWlnQLFP_-yceWccG0dK62x_j6I-R-CUyz3F6Dgh3FdU8js_ThCf126iQipjuR3Kjmkt4hE5XyovSrmAHTUiNkQXmbZGVS0W64gg7TpBHbOvwVyzF7QsWQXvyShfOKlXD9r9Enr_F-DA/s320/9.png)
![image](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgeoyTry7nvtqatGxOOYMTlS7PhfB2r4M8bXe0TBtROLBbNQ-uJU_zP4AmT3unCz4Re2y0vtJlrtLHlyyEnNk7J8VTZJDEB-zU_b75hHm4fN97KTzdYpJRcqjNlis7UcK-nLt-sGJe63LrTN3ip-KXKWo0M40RcQGbwmgevmAcdUGpr3-MG1hT254PU/s320/10.png)

Now, when the first 555 timer IC is ON it turns on the first cluster of Red LED’s and they blink at the speed at which the second 555 timer IC oscillates the output.
Similarly when the first 555 timer IC turns OFF, the second cluster of Blue LED’s turns ON and blinks at the speed at which the second 555 timer IC oscillates the output.

This cycle continues as long as there is power in the circuit creating a cool LED flashing effect similar to the flashing lights used on police cars.

You can change the frequency of "toggling" between the successive LED groups by changing the higher value capacitor. Increasing its value will increase the time between the successive toggling between the two LED clusters and vice versa. 
Similarly, changing the value of the lower value capacitor will change the "blinking rate" of the LED clusters.


Demo On Breadboard
------------------
![image](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEikCQ7WdXr3Vdnx9d2U5CudUbjxhaEN1yUPI7dhVH8zaMP-Z-614X9lpzZ47oatD6v1sFwscKfSuKCsXkpcUgy5AVte8j0EDXTwQyKP5SnSQD85EzX6ggcS8pFzFnu3C5WJLqRquPz_8Ab3-FLaQh8kQ_RuT-BEm1yCuWxWtQ0BSKh4pUIIgQoUd8hy/w640-h360/1.png)


The Board
---------
![image](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEiE0L1D5nHT69saFDFTnaGVkLmAsTBSBt2GaIGlEMPy_ER1S4xxBfpAyflfVCWKwVVXM3ZpCrDr9C1vNSgSVWUebpHWYB_9h5-2LvSEv4qeAdzXFeC05cXpCEDilewDMdMw5VcQcnTXbKJ6oNqZ2PaRFiQDr_qh3uFmaR2IWqEcJ36AGnfaLGw2oWui/w640-h360/13.png)

So, this is how my board looks like in 2D and 3D. 
I have placed both ICs and all other electronics components to the middle of the board.
To give the assembly a bit nicer look, I have placed the LED clusters on both sides of the board.
Alright, now lets start soldering the components to the board.


Soldering
---------
![image](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjM9MMV0r4tT-wKwrhQnUFHCe3vVDK3sROjuj0EyrjHAy5wxKFkXT9GlRSzZxVkUi158A_-OpHC0giafytfA9JjpVbAOpPsZcIE8itclm0XZ7hksBMneMc0na3mhAV20TY8lL8prjp2oKmFr2sqhMuAgrUx2FyFtdW39ew_7Fy0wGvr-6EcHjf3vI6D/w640-h360/14.png)

Since I care a lot about my ICs and microcontrollers I never solder them directly to the board. 
In case of ICs, I always try to use IC bases or if a base is not available I use female pin headers. 

![image](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjayeFlD_UmIyrPYmkjFuLG1IRyV0neSu4rVqcg_aW-mDeQG2sDk6lsn6DiQ4H4D2RTrxEslSuFJvW2GT_hqwgXcx1suwzRjfMs7WIEYpaqz2Kc7vpSYfceLtj4Hd67T3eDHcYN0zOIDppFY7UwsOzUPIU8HrSRHUixMEn2qukzrkKXL5W3srCB6RQy/w640-h360/16.png)

After soldering the IC bases, I am soldering all the resistances to the board. 

![image](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjotPkzzEVgjEXHBmb9nOVuJnDCMH3PFdi6ZdBFDsoa0f2BUWDKs_k5eqndh86O55aPVSLJT_vqM51X3CjBvh1LBqP5X9xxb2MBi4G7p_jP4m-15UO1ZuK_FhHC-tFG_eZeSz6QGFiex_BY5VeH9Fyzz_N0VBBOs_RUhA58p3p1b33DKAsVDxi9AiNd/w640-h360/19.png)

Next, I am soldering the capacitors to the board followed by all the LEDs to the board.

I am also soldering a female micro USB port to power this circuit board. 
Always check the polarity before soldering the socket to your board.

![image](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEg3tJDuoyGg9N51AhFTIuHBdpSIAYPqLJnieaAecHMPVjIyZVeQ3BJmUQfG29y5VuQhPqU9edYqIk0QJOt0c--xfP6kVVh_dbGOPi3WPYJwuXD6BA3po_HQKCTbuqASXvnZsEB8QRNgQOOggKdZZ_cE9CinkAj-oZ53uPN0oAo8TgXymMl_7Sc8TYTH/w640-h360/20.png)

To conclude the setup, I am installing the ICs to the IC bases.


Final Demo
----------
![image](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgf0Jc6cvFLjIFx4sZ2_n7ZqzE3Nfg1Zh7IKlhQQ6G2D9DbtUGu_X_0YWM2_MhkzHDYhNTcrPS8LQxi9jQKphYYSAveap8lBIon206kTEGA7xzEKz17FKkJQwc3sFF5zxrOoXsiwy5Oxlu4auZILiAtGTe4UmFBy6izNxkBJLnL6Z83VoiE83wEOoZA/w640-h360/21.png)

So, this is how my final setup looks like.
Do comment and let me know if there are any scopes of improvement.


Thanks
------
[![4vDtWafMF0M](https://img.youtube.com/vi/4vDtWafMF0M/0.jpg)](https://www.youtube.com/watch?v=4vDtWafMF0M)

Thanks again for checking my post. I hope it helps you.
If you want to support me subscribe to my YouTube Channel: https://www.youtube.com/user/tarantula3

Full Blog Post: Blog Post
https://diyfactory007.blogspot.com/2022/07/Police-Car-Led-Effect%20v1.0.1.html
Video: https://youtu.be/4vDtWafMF0M

Related Videos
1. Adjustable Single/Dual LED Flasher: Video Link
https://youtu.be/B1URFJywtcI
2. 555 Pulse Generator Module, How it Works: Video Link
https://youtu.be/bMAnipPOjFo

Gerber File: Download
https://github.com/tarantula3/Police-Car-Led-Effect-Using-555-Timer-IC/blob/main/Gerber_Police%20Car%20Like%20LED%20effect_2022-06-26.zip
Schema: Download
https://github.com/tarantula3/Police-Car-Led-Effect-Using-555-Timer-IC/blob/main/Schema.png
Resistor Value Calculator: Open Website
http://ledcalc.com/


Support My Work
BTC:  1M1PdxVxSTPLoMK91XnvEPksVuAa4J4dDp
LTC:  MQFkVkWimYngMwp5SMuSbMP4ADStjysstm
DOGE: DDe7Fws24zf7acZevoT8uERnmisiHwR5st
ETH:  0x939aa4e13ecb4b46663c8017986abc0d204cde60
BAT:  0x939aa4e13ecb4b46663c8017986abc0d204cde60
LBC:  bZ8ANEJFsd2MNFfpoxBhtFNPboh7PmD7M2
Thanks, ca again in my next tutorial.
