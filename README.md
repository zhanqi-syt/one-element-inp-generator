![3D Model](https://github.com/zhanqi-syt/one-element-inp-generator/assets/116877222/c4b35dfa-d239-4f86-bcd7-fc8742586634)# One Element INP Generator: Turbocharge Modeling with Abaqus Python Script

## Overview

This repository contains a powerful Abaqus Python script designed to simplify and accelerate the creation of 3D finite element models with a single element.  
The script automates the process, allowing users to effortlessly set up and generate complex models with minimal manual intervention. Abaqus CAE models are shown in Fig. 1.

![Uploading 3D<?xml version="1.0" encoding="utf-8"?>
<!-- Generator: Adobe Illustrator 23.1.0, SVG Export Plug-In . SVG Version: 6.00 Build 0)  -->
<svg version="1.1" id="图层_1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px"
	 viewBox="0 0 595.28 841.89" style="enable-background:new 0 0 595.28 841.89;" xml:space="preserve">
<style type="text/css">
	.st0{fill:none;stroke:#FF7A00;stroke-width:0.4994;stroke-miterlimit:10;}
	.st1{fill:#1C7DDB;stroke:#1C7DDB;stroke-width:0;stroke-miterlimit:10;}
	.st2{fill:#1C82E5;stroke:#1C82E5;stroke-width:0;stroke-miterlimit:10;}
	.st3{fill:#125494;stroke:#125494;stroke-width:0;stroke-miterlimit:10;}
	.st4{fill:none;stroke:#000000;stroke-width:0.4994;stroke-miterlimit:10;}
	.st5{fill:#800000;stroke:#800000;stroke-width:0;stroke-miterlimit:10;}
	.st6{fill:#8B0000;stroke:#8B0000;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st7{fill:#980000;stroke:#980000;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st8{fill:#900000;stroke:#900000;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st9{fill:#A50000;stroke:#A50000;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st10{fill:#B20000;stroke:#B20000;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st11{fill:#A90000;stroke:#A90000;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st12{fill:#9C0000;stroke:#9C0000;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st13{fill:#B60000;stroke:#B60000;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st14{fill:#BF0000;stroke:#BF0000;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st15{fill:#CF0202;stroke:#CF0202;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st16{fill:#C40101;stroke:#C40101;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st17{fill:#D40202;stroke:#D40202;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st18{fill:#D60202;stroke:#D60202;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st19{fill:#D40101;stroke:#D40101;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st20{fill:#CE0000;stroke:#CE0000;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st21{fill:#C50000;stroke:#C50000;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st22{fill:#CB0000;stroke:#CB0000;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st23{fill:#BC0000;stroke:#BC0000;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st24{fill:#B30000;stroke:#B30000;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st25{fill:#B90000;stroke:#B90000;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st26{fill:#C20000;stroke:#C20000;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st27{fill:#B00000;stroke:#B00000;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st28{fill:#AA0000;stroke:#AA0000;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st29{fill:#9E0000;stroke:#9E0000;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st30{fill:#A60000;stroke:#A60000;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st31{fill:#930000;stroke:#930000;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st32{fill:#870000;stroke:#870000;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st33{fill:#8F0000;stroke:#8F0000;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st34{fill:#9A0000;stroke:#9A0000;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st35{fill:#830000;stroke:#830000;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st36{fill:#8D0000;stroke:#8D0000;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st37{fill:#860000;stroke:#860000;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st38{fill:#970000;stroke:#970000;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st39{fill:#A10000;stroke:#A10000;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st40{fill:#9B0000;stroke:#9B0000;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st41{fill:#8E0000;stroke:#8E0000;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st42{fill:#940000;stroke:#940000;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st43{fill:#890000;stroke:#890000;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st44{fill:#840000;stroke:#840000;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st45{fill:#A00000;stroke:#A00000;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st46{fill:#920000;stroke:#920000;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st47{fill:#990000;stroke:#990000;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st48{fill:#A20000;stroke:#A20000;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st49{fill:#9D0000;stroke:#9D0000;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st50{fill:#A30000;stroke:#A30000;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st51{fill:#A80000;stroke:#A80000;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st52{fill:#AC0000;stroke:#AC0000;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st53{fill:#AB0000;stroke:#AB0000;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st54{fill:#B40000;stroke:#B40000;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st55{fill:#A70000;stroke:#A70000;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st56{fill:#AE0000;stroke:#AE0000;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st57{fill:#BD0000;stroke:#BD0000;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st58{fill:#B80000;stroke:#B80000;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st59{fill:#C10000;stroke:#C10000;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st60{fill:#B70000;stroke:#B70000;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st61{fill:#AF0000;stroke:#AF0000;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st62{fill:#9A0101;stroke:#9A0101;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st63{fill:#A30101;stroke:#A30101;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st64{fill:#A80505;stroke:#A80505;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st65{fill:#A20202;stroke:#A20202;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st66{fill:#910101;stroke:#910101;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st67{fill:#870101;stroke:#870101;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st68{fill:#960505;stroke:#960505;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st69{fill:#8F0202;stroke:#8F0202;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st70{fill:#AD0808;stroke:#AD0808;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st71{fill:#A40808;stroke:#A40808;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st72{fill:#B20C0C;stroke:#B20C0C;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st73{fill:#AC0909;stroke:#AC0909;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st74{fill:#980202;stroke:#980202;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st75{fill:#9E0606;stroke:#9E0606;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st76{fill:#A70606;stroke:#A70606;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st77{fill:#9F0505;stroke:#9F0505;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st78{fill:#B60101;stroke:#B60101;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st79{fill:#AC0101;stroke:#AC0101;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st80{fill:#BB0505;stroke:#BB0505;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st81{fill:#B40202;stroke:#B40202;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st82{fill:#BF0101;stroke:#BF0101;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st83{fill:#C80101;stroke:#C80101;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st84{fill:#CD0505;stroke:#CD0505;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st85{fill:#C70202;stroke:#C70202;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st86{fill:#C90808;stroke:#C90808;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st87{fill:#D20808;stroke:#D20808;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st88{fill:#D70C0C;stroke:#D70C0C;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st89{fill:#D10909;stroke:#D10909;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st90{fill:#BD0202;stroke:#BD0202;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st91{fill:#CC0606;stroke:#CC0606;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st92{fill:#C30606;stroke:#C30606;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st93{fill:#C40505;stroke:#C40505;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st94{fill:#CA0F0F;stroke:#CA0F0F;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st95{fill:#C10F0F;stroke:#C10F0F;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st96{fill:#CF1313;stroke:#CF1313;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st97{fill:#C91010;stroke:#C91010;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st98{fill:#D30F0F;stroke:#D30F0F;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st99{fill:#DC0F0F;stroke:#DC0F0F;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st100{fill:#E21313;stroke:#E21313;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st101{fill:#DB1010;stroke:#DB1010;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st102{fill:#DD1616;stroke:#DD1616;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st103{fill:#E71616;stroke:#E71616;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st104{fill:#EC1A1A;stroke:#EC1A1A;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st105{fill:#E51717;stroke:#E51717;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st106{fill:#D21010;stroke:#D21010;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st107{fill:#E01414;stroke:#E01414;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st108{fill:#D71414;stroke:#D71414;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st109{fill:#D81313;stroke:#D81313;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st110{fill:#B90606;stroke:#B90606;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st111{fill:#AB0202;stroke:#AB0202;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st112{fill:#B00606;stroke:#B00606;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st113{fill:#B10505;stroke:#B10505;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st114{fill:#C80909;stroke:#C80909;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st115{fill:#D60D0D;stroke:#D60D0D;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st116{fill:#CD0D0D;stroke:#CD0D0D;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st117{fill:#CE0C0C;stroke:#CE0C0C;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st118{fill:#B50909;stroke:#B50909;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st119{fill:#C40D0D;stroke:#C40D0D;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st120{fill:#BA0D0D;stroke:#BA0D0D;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st121{fill:#BC0C0C;stroke:#BC0C0C;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st122{fill:#C00808;stroke:#C00808;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st123{fill:#C50C0C;stroke:#C50C0C;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st124{fill:#B70808;stroke:#B70808;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st125{fill:#BE0909;stroke:#BE0909;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st126{fill:#A30808;stroke:#A30808;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st127{fill:#AA0808;stroke:#AA0808;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st128{fill:#AA0909;stroke:#AA0909;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st129{fill:#950505;stroke:#950505;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st130{fill:#8D0101;stroke:#8D0101;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st131{fill:#8E0202;stroke:#8E0202;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st132{fill:#A20505;stroke:#A20505;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st133{fill:#940101;stroke:#940101;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st134{fill:#9B0101;stroke:#9B0101;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st135{fill:#9B0202;stroke:#9B0202;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st136{fill:#9C0606;stroke:#9C0606;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st137{fill:#940202;stroke:#940202;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st138{fill:#A30606;stroke:#A30606;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st139{fill:#9C0505;stroke:#9C0505;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st140{fill:#CE1313;stroke:#CE1313;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st141{fill:#C00F0F;stroke:#C00F0F;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st142{fill:#C70F0F;stroke:#C70F0F;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st143{fill:#C71010;stroke:#C71010;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st144{fill:#EB1A1A;stroke:#EB1A1A;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st145{fill:#E31616;stroke:#E31616;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st146{fill:#E41717;stroke:#E41717;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st147{fill:#CD0F0F;stroke:#CD0F0F;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st148{fill:#DC1313;stroke:#DC1313;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st149{fill:#D40F0F;stroke:#D40F0F;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st150{fill:#D41010;stroke:#D41010;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st151{fill:#D51414;stroke:#D51414;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st152{fill:#DC1414;stroke:#DC1414;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st153{fill:#CE1010;stroke:#CE1010;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st154{fill:#D51313;stroke:#D51313;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st155{fill:#B00505;stroke:#B00505;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st156{fill:#A10101;stroke:#A10101;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st157{fill:#A80101;stroke:#A80101;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st158{fill:#A80202;stroke:#A80202;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st159{fill:#BE0808;stroke:#BE0808;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st160{fill:#CC0C0C;stroke:#CC0C0C;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st161{fill:#C50808;stroke:#C50808;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st162{fill:#C50909;stroke:#C50909;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st163{fill:#AF0101;stroke:#AF0101;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st164{fill:#BD0505;stroke:#BD0505;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st165{fill:#B50101;stroke:#B50101;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st166{fill:#B60202;stroke:#B60202;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st167{fill:#B70606;stroke:#B70606;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st168{fill:#BD0606;stroke:#BD0606;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st169{fill:#AF0202;stroke:#AF0202;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st170{fill:#B60505;stroke:#B60505;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st171{fill:#BF0D0D;stroke:#BF0D0D;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st172{fill:#B90D0D;stroke:#B90D0D;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st173{fill:#B10909;stroke:#B10909;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st174{fill:#B80C0C;stroke:#B80C0C;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st175{fill:#C60D0D;stroke:#C60D0D;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st176{fill:#C60C0C;stroke:#C60C0C;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st177{fill:#A90606;stroke:#A90606;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st178{fill:#A90505;stroke:#A90505;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st179{fill:#BF0C0C;stroke:#BF0C0C;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st180{fill:#B10808;stroke:#B10808;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st181{fill:#B80909;stroke:#B80909;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st182{fill:#850000;stroke:#850000;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st183{fill:#8A0000;stroke:#8A0000;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st184{fill:#9F0000;stroke:#9F0000;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st185{fill:#AD0000;stroke:#AD0000;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st186{fill:#A40000;stroke:#A40000;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st187{fill:#880000;stroke:#880000;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st188{fill:#960000;stroke:#960000;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st189{fill:#8C0000;stroke:#8C0000;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st190{fill:#820000;stroke:#820000;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st191{fill:#00C200;stroke:#00C200;stroke-width:0;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st192{fill:#008200;stroke:#008200;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st193{fill:#008B00;stroke:#008B00;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st194{fill:#008500;stroke:#008500;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st195{fill:#009300;stroke:#009300;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st196{fill:#009B00;stroke:#009B00;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st197{fill:#009600;stroke:#009600;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st198{fill:#008D00;stroke:#008D00;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st199{fill:#009E00;stroke:#009E00;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st200{fill:#00A400;stroke:#00A400;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st201{fill:#00B000;stroke:#00B000;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st202{fill:#00A800;stroke:#00A800;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st203{fill:#00B400;stroke:#00B400;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st204{fill:#00B800;stroke:#00B800;stroke-width:0;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st205{fill:#008000;stroke:#008000;stroke-width:0;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st206{fill:#00B900;stroke:#00B900;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st207{fill:#00BD00;stroke:#00BD00;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st208{fill:#00B500;stroke:#00B500;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st209{fill:#00AD00;stroke:#00AD00;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st210{fill:#00A500;stroke:#00A500;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st211{fill:#00A900;stroke:#00A900;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st212{fill:#00A600;stroke:#00A600;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st213{fill:#00AA00;stroke:#00AA00;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st214{fill:#00A200;stroke:#00A200;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st215{fill:#00A100;stroke:#00A100;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st216{fill:#009C00;stroke:#009C00;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st217{fill:#009800;stroke:#009800;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st218{fill:#009A00;stroke:#009A00;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st219{fill:#009500;stroke:#009500;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st220{fill:#009100;stroke:#009100;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st221{fill:#009900;stroke:#009900;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st222{fill:#009D00;stroke:#009D00;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st223{fill:#009400;stroke:#009400;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st224{fill:#008E00;stroke:#008E00;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st225{fill:#008C00;stroke:#008C00;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st226{fill:#008700;stroke:#008700;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st227{fill:#008300;stroke:#008300;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st228{fill:#008F00;stroke:#008F00;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st229{fill:#00AB00;stroke:#00AB00;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st230{fill:#00A700;stroke:#00A700;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st231{fill:#009200;stroke:#009200;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st232{fill:#009700;stroke:#009700;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st233{fill:#00A000;stroke:#00A000;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st234{fill:#009F00;stroke:#009F00;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st235{fill:#00A300;stroke:#00A300;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st236{fill:#00AC00;stroke:#00AC00;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st237{fill:#00BC00;stroke:#00BC00;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st238{fill:#00B700;stroke:#00B700;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st239{fill:#00AE00;stroke:#00AE00;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st240{fill:#00C300;stroke:#00C300;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st241{fill:#00BF00;stroke:#00BF00;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st242{fill:#00C900;stroke:#00C900;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st243{fill:#01CB01;stroke:#01CB01;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st244{fill:#02CB02;stroke:#02CB02;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st245{fill:#01C401;stroke:#01C401;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st246{fill:#00BE00;stroke:#00BE00;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st247{fill:#00BA00;stroke:#00BA00;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st248{fill:#00B800;stroke:#00B800;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st249{fill:#00B100;stroke:#00B100;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st250{fill:#00B600;stroke:#00B600;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st251{fill:#00AF00;stroke:#00AF00;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st252{fill:#00B200;stroke:#00B200;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st253{fill:#0000BA;stroke:#0000BA;stroke-width:0;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st254{fill:#000080;stroke:#000080;stroke-width:0;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st255{fill:#0000AA;stroke:#0000AA;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st256{fill:#0000B7;stroke:#0000B7;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st257{fill:#0000AE;stroke:#0000AE;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st258{fill:#0000BB;stroke:#0000BB;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st259{fill:#0000BF;stroke:#0000BF;stroke-width:0;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st260{fill:#0000A3;stroke:#0000A3;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st261{fill:#000099;stroke:#000099;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st262{fill:#00009F;stroke:#00009F;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st263{fill:#00008F;stroke:#00008F;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st264{fill:#000086;stroke:#000086;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st265{fill:#00008C;stroke:#00008C;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st266{fill:#000096;stroke:#000096;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st267{fill:#000083;stroke:#000083;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st268{fill:#0000AF;stroke:#0000AF;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st269{fill:#0000B8;stroke:#0000B8;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st270{fill:#0000B5;stroke:#0000B5;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st271{fill:#0000A7;stroke:#0000A7;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st272{fill:#0000A8;stroke:#0000A8;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st273{fill:#0000A4;stroke:#0000A4;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st274{fill:#0000B9;stroke:#0000B9;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st275{fill:#0000B1;stroke:#0000B1;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st276{fill:#0000BA;stroke:#0000BA;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st277{fill:#0000B6;stroke:#0000B6;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st278{fill:#0000AD;stroke:#0000AD;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st279{fill:#0000B0;stroke:#0000B0;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st280{fill:#0101BE;stroke:#0101BE;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st281{fill:#0303C7;stroke:#0303C7;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st282{fill:#0202C1;stroke:#0202C1;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st283{fill:#0101BF;stroke:#0101BF;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st284{fill:#0303C8;stroke:#0303C8;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st285{fill:#0202C2;stroke:#0202C2;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st286{fill:#0606D1;stroke:#0606D1;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st287{fill:#0909DA;stroke:#0909DA;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st288{fill:#0707D4;stroke:#0707D4;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st289{fill:#0404CB;stroke:#0404CB;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st290{fill:#0303C9;stroke:#0303C9;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st291{fill:#0101C5;stroke:#0101C5;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st292{fill:#0202C4;stroke:#0202C4;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st293{fill:#0606D2;stroke:#0606D2;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st294{fill:#0909DC;stroke:#0909DC;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st295{fill:#0606D8;stroke:#0606D8;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st296{fill:#0707D7;stroke:#0707D7;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st297{fill:#0101CB;stroke:#0101CB;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st298{fill:#0303D4;stroke:#0303D4;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st299{fill:#0101D0;stroke:#0101D0;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st300{fill:#0202D0;stroke:#0202D0;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st301{fill:#0404CE;stroke:#0404CE;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st302{fill:#0404D4;stroke:#0404D4;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st303{fill:#0202CA;stroke:#0202CA;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st304{fill:#0303CF;stroke:#0303CF;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st305{fill:#0000BE;stroke:#0000BE;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st306{fill:#0000CA;stroke:#0000CA;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st307{fill:#0000C0;stroke:#0000C0;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st308{fill:#0000C3;stroke:#0000C3;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st309{fill:#0000A2;stroke:#0000A2;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st310{fill:#000093;stroke:#000093;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st311{fill:#000084;stroke:#000084;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st312{fill:#000089;stroke:#000089;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st313{fill:#000098;stroke:#000098;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st314{fill:#0000B2;stroke:#0000B2;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st315{fill:#0000AB;stroke:#0000AB;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st316{fill:#000095;stroke:#000095;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st317{fill:#000087;stroke:#000087;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st318{fill:#00008D;stroke:#00008D;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st319{fill:#00008E;stroke:#00008E;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st320{fill:#00009A;stroke:#00009A;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st321{fill:#00009C;stroke:#00009C;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st322{fill:#000094;stroke:#000094;stroke-width:0.4802;stroke-linejoin:bevel;stroke-miterlimit:10;}
	.st323{font-family:'ArialMT';}
	.st324{font-size:12.0005px;}
	.st325{fill:none;stroke:#000000;stroke-width:0.5;stroke-miterlimit:10;}
	.st326{fill:none;stroke:#000000;stroke-width:0.499;stroke-miterlimit:10;}
	.st327{font-family:'Arial-ItalicMT';}
	.st328{font-size:10px;}
</style>
<font horiz-adv-x="2048">
<!-- Arial is a trademark of The Monotype Corporation. -->
<!-- Copyright: Copyright 2023 Adobe System Incorporated. All rights reserved. -->
<font-face font-family="ArialMT" units-per-em="2048" underline-position="-217" underline-thickness="150"/>
<missing-glyph horiz-adv-x="1536" d="M256,0l0,1280l1024,0l0,-1280M288,32l960,0l0,1216l-960,0z"/>
<glyph unicode="X" horiz-adv-x="1366" d="M9,0l567,764l-500,702l231,0l266,-376C628,1012 668,952 691,910C724,963 762,1019 807,1077l295,389l211,0l-515,-691l555,-775l-240,0l-369,523C723,553 702,586 680,621C647,568 624,531 610,511l-368,-511z"/>
<glyph unicode="Y" horiz-adv-x="1366" d="M571,0l0,621l-565,845l236,0l289,-442C584,941 634,859 680,776C724,853 777,939 840,1035l284,431l226,0l-585,-845l0,-621z"/>
<glyph unicode="Z" horiz-adv-x="1251" d="M41,0l0,180l751,939C845,1186 896,1244 944,1293l-818,0l0,173l1050,0l0,-173l-823,-1017l-89,-103l936,0l0,-173z"/>
</font>

	<font horiz-adv-x="2048">
<!-- Arial is a trademark of The Monotype Corporation. -->
<!-- Copyright: Copyright 2023 Adobe System Incorporated. All rights reserved. -->
<font-face font-family="Arial-ItalicMT" units-per-em="2048" underline-position="-217" underline-thickness="150"/>
<missing-glyph horiz-adv-x="1536" d="M256,0l0,1280l1024,0l0,-1280M288,32l960,0l0,1216l-960,0z"/>
<glyph unicode=" " horiz-adv-x="569"/>
<glyph unicode="M" horiz-adv-x="1706" d="M90,0l306,1466l241,0l148,-950C804,391 817,272 823,157C864,256 932,389 1027,558l514,908l245,0l-306,-1466l-193,0l153,713C1475,878 1526,1062 1592,1267C1550,1172 1498,1069 1436,959l-546,-959l-189,0l-147,940C541,1026 531,1126 525,1241C508,1112 492,1010 476,935l-195,-935z"/>
<glyph unicode="S" horiz-adv-x="1366" d="M144,474l192,18l-2,-51C334,384 347,333 373,286C399,239 442,202 502,177C562,151 633,138 716,138C833,138 923,164 985,215C1046,266 1077,325 1077,391C1077,437 1061,479 1028,517C995,554 904,605 755,669C640,719 561,757 519,784C453,827 404,875 373,926C342,977 326,1035 326,1100C326,1175 347,1243 388,1304C429,1365 490,1411 570,1443C649,1475 739,1491 839,1491C958,1491 1059,1471 1141,1431C1223,1391 1283,1338 1320,1271C1357,1204 1375,1141 1375,1080C1375,1074 1375,1064 1374,1050l-189,-15C1185,1076 1181,1109 1174,1132C1161,1173 1140,1207 1112,1235C1084,1263 1046,1286 997,1303C948,1320 893,1328 832,1328C725,1328 642,1304 583,1256C538,1219 515,1171 515,1110C515,1074 524,1042 543,1014C562,985 595,957 644,930C679,911 761,872 891,815C996,768 1069,732 1109,705C1162,670 1203,627 1232,577C1261,526 1275,469 1275,405C1275,326 1251,253 1203,186C1154,119 1087,67 1002,30C917,-7 819,-25 709,-25C543,-25 408,11 303,84C198,156 145,286 144,474z"/>
<glyph unicode="e" horiz-adv-x="1139" d="M848,361l176,-18C999,256 941,173 850,94C759,15 650,-24 524,-24C445,-24 373,-6 308,31C242,67 192,120 158,189C123,258 106,337 106,426C106,542 133,655 187,764C240,873 310,954 395,1007C480,1060 573,1086 672,1086C799,1086 900,1047 976,968C1051,889 1089,782 1089,646C1089,594 1084,541 1075,486l-782,0C290,465 289,447 289,430C289,331 312,255 358,203C403,150 459,124 525,124C587,124 648,144 708,185C768,226 815,284 848,361M322,624l596,0C919,643 919,656 919,664C919,755 896,824 851,873C806,921 747,945 676,945C599,945 528,918 465,865C401,812 353,731 322,624z"/>
<glyph unicode="h" horiz-adv-x="1139" d="M68,0l306,1466l181,0l-117,-563C505,968 568,1015 626,1044C684,1072 744,1086 805,1086C893,1086 961,1063 1010,1017C1059,970 1083,909 1083,833C1083,796 1072,727 1051,627l-131,-627l-181,0l135,643C893,736 903,795 903,819C903,854 891,882 867,904C843,926 808,937 763,937C698,937 635,920 576,886C517,851 470,804 437,745C403,685 372,589 344,456l-95,-456z"/>
<glyph unicode="i" horiz-adv-x="455" d="M325,1261l43,205l180,0l-43,-205M61,0l222,1062l181,0l-222,-1062z"/>
<glyph unicode="s" horiz-adv-x="1024" d="M85,363l181,11C266,322 274,278 290,241C306,204 336,174 379,151C422,128 472,116 529,116C609,116 669,132 709,164C749,196 769,234 769,277C769,308 757,338 733,366C708,394 648,429 553,470C457,511 396,539 369,556C324,583 291,616 268,653C245,690 234,732 234,780C234,864 267,936 334,996C401,1056 494,1086 614,1086C747,1086 849,1055 919,994C988,932 1024,851 1027,750l-177,-12C847,802 825,853 782,890C739,927 679,946 601,946C538,946 490,932 455,903C420,874 403,843 403,810C403,777 418,747 448,722C468,705 520,678 603,642C742,582 829,535 865,500C922,445 951,377 951,298C951,245 935,194 903,143C870,92 821,52 755,22C688,-9 610,-24 520,-24C397,-24 293,6 207,67C121,128 80,226 85,363z"/>
<glyph unicode="z" horiz-adv-x="1024" d="M40,0l29,140l571,643C681,828 726,875 776,924C690,915 628,911 591,911l-395,0l32,151l821,0l-24,-114l-576,-647C416,264 368,214 303,150C404,156 473,159 510,159l418,0l-33,-159z"/>
</font>

	<path class="st0" d="M137.44,68l-5.08-6.18l-2.24,2.08 M137.44,68l-7.31-4.1l-0.85,3.26 M137.44,68l-8.16-0.84l1.04,2.51
	 M137.44,68l-7.13,1.67l2.29,0.29 M137.44,68l-4.84,1.95l2.2-2.06 M137.44,68l-2.64-0.11l0.85-3.22L137.44,68 M119.33,75.2
	l-2.62-5.91L114.32,69 M119.33,75.2l-5-6.2l-2.28,2.09 M119.33,75.2l-7.28-4.11l-0.81,3.24 M119.33,75.2l-8.09-0.86l1.13,2.46
	 M119.33,75.2l-6.95,1.6l2.38,0.25 M119.33,75.2l-4.57,1.85l2.24-2.08 M119.33,75.2L117,74.97l0.81-3.2L119.33,75.2 M98.81,79.32
	l-1.2-2.44 M100.06,82.85l-2.44-5.98l-2.5-0.25 M100.06,82.85l-4.94-6.23l-2.32,2.11 M100.06,82.85l-7.26-4.12l-0.76,3.23
	 M100.06,82.85l-8.02-0.89l1.23,2.43 M100.06,82.85l-6.79,1.53l2.49,0.21 M100.06,82.85l-4.3,1.74l2.29-2.1 M100.06,82.85
	l-2.01-0.36l0.77-3.18L100.06,82.85 M78.56,87.35l-1.32-2.4 M79.51,91.02l-2.27-6.07l-2.61-0.21 M79.51,91.02l-4.88-6.28l-2.38,2.14
	 M79.51,91.02l-7.26-4.14l-0.72,3.22 M79.51,91.02l-7.98-0.93l1.35,2.39 M79.51,91.02l-6.62,1.46l2.61,0.17 M79.51,91.02l-4.01,1.63
	l2.33-2.12 M79.51,91.02l-1.68-0.49l0.73-3.18L79.51,91.02 M154.49,157.45l-2.88-6.52l-2.15,0.15 M154.49,157.45l-5.03-6.37
	l-2.15,2.23 M154.49,157.45l-7.18-4.13l-0.87,3 M154.49,157.45l-8.05-1.14l0.92,1.97 M154.49,157.45l-7.13,0.84l2.15-0.18
	 M154.49,157.45l-4.98,0.65l2.12-2.21 M154.49,157.45l-2.86-1.56l0.87-2.96L154.49,157.45 M154.49,140.22l-2.88-6.37l-2.16,0.06
	 M154.49,140.22l-5.04-6.31l-2.16,2.19 M154.49,140.22l-7.19-4.12l-0.87,3.04 M154.49,140.22l-8.06-1.08l0.93,2.07 M154.49,140.22
	l-7.14,0.99l2.15-0.1 M154.49,140.22l-4.98,0.9l2.12-2.18 M154.49,140.22l-2.86-1.28l0.87-3L154.49,140.22 M154.49,122.06
	l-2.89-6.23l-2.16-0.04 M154.49,122.06l-5.05-6.27l-2.16,2.17 M154.49,122.06l-7.21-4.1l-0.87,3.08 M154.49,122.06l-8.08-1.02
	l0.93,2.17 M154.49,122.06l-7.16,1.15h2.16 M154.49,122.06l-5,1.15l2.13-2.14 M154.49,122.06l-2.87-0.99l0.87-3.05L154.49,122.06
	 M152.49,99.12l-0.9-2.3 M154.49,102.9l-2.91-6.08l-2.17-0.14 M154.49,102.9l-5.07-6.22l-2.17,2.13 M154.49,102.9l-7.24-4.09
	l-0.88,3.14 M154.49,102.9l-8.12-0.95l0.93,2.29 M154.49,102.9l-7.19,1.33l2.17,0.1 M154.49,102.9l-5.02,1.44l2.14-2.11
	 M154.49,102.9l-2.88-0.68l0.87-3.1L154.49,102.9 M152.48,79.14l-0.9-2.43 M154.49,82.66l-2.92-5.94l-2.18-0.25 M154.49,82.66
	l-5.1-6.19l-2.18,2.1 M154.49,82.66l-7.29-4.09l-0.88,3.21 M154.49,82.66l-8.17-0.88l0.94,2.41 M154.49,82.66l-7.24,1.52l2.18,0.21
	 M154.49,82.66l-5.05,1.73l2.15-2.08 M154.49,82.66l-2.9-0.35l0.88-3.16L154.49,82.66 M139.67,165.85l-2.75-6.59l-2.23,0.19
	 M139.67,165.85l-4.98-6.4l-2.19,2.25 M139.67,165.85l-7.17-4.15l-0.84,2.98 M139.67,165.85l-8.01-1.17l1,1.94l2.23-0.23
	 M139.67,165.85l-4.77,0.53l2.15-2.23 M139.67,165.85l-2.62-1.7l0.84-2.94L139.67,165.85 M122.5,169.94l-1.05-1.91 M124.06,174.71
	l-2.61-6.68l-2.32,0.24 M124.06,174.71l-4.93-6.44l-2.23,2.28 M124.06,174.71l-7.16-4.17l-0.8,2.96 M124.06,174.71l-7.96-1.21
	l1.09,1.89l2.32-0.28 M124.06,174.71l-4.56,0.41l2.19-2.26 M124.06,174.71l-2.37-1.85l0.81-2.92L124.06,174.71 M106.25,179.14
	l-1.14-1.87 M107.58,184.06l-2.47-6.79l-2.42,0.29 M107.58,184.06l-4.89-6.5l-2.27,2.31 M107.58,184.06l-7.16-4.2l-0.77,2.96
	 M107.58,184.06l-7.93-1.24l1.18,1.84 M107.58,184.06l-6.75,0.61l2.42-0.33 M107.58,184.06l-4.34,0.28l2.23-2.29 M107.58,184.06
	l-2.1-2.01l0.77-2.92L107.58,184.06 M89.07,188.85l-1.24-1.82 M90.16,193.95l-2.33-6.92l-2.52,0.35 M90.16,193.95l-4.85-6.57
	l-2.32,2.34 M90.16,193.95l-7.18-4.24l-0.73,2.95 M90.16,193.95l-7.91-1.29l1.28,1.81 M90.16,193.95l-6.64,0.52l2.52-0.38
	L90.16,193.95l-4.12,0.14l2.29-2.32 M90.16,193.95l-1.83-2.18l0.74-2.91L90.16,193.95 M245.16,203.07l-0.7-2.95 M237.25,204.41
	l7.21-4.28l-2.38-2.38 M237.25,204.41l4.83-6.67l-2.64-0.4 M237.25,204.41l2.18-7.07l-1.35,1.79 M237.25,204.41l0.84-5.28l0.71,2.91
	 M237.25,204.41l1.54-2.37l2.34,2.36 M237.25,204.41l3.88-0.01l2.64,0.44 M237.25,204.41l6.52,0.43l1.39-1.77L237.25,204.41
	 M226.73,192.66l-0.73-2.95 M218.82,193.95l7.18-4.24l-2.32-2.34 M218.82,193.95l4.86-6.57l-2.53-0.35 M218.82,193.95l2.33-6.92
	l-1.24,1.82 M218.82,193.95l1.09-5.1l0.74,2.91 M218.82,193.95l1.83-2.18l2.28,2.32 M218.82,193.95l4.12,0.14 M218.82,193.95
	l6.64,0.52l1.28-1.81L218.82,193.95 M209.33,182.82l-0.77-2.96 M201.4,184.06l7.16-4.2l-2.27-2.31 M201.4,184.06l4.89-6.5
	l-2.42-0.29 M201.4,184.06l2.48-6.79l-1.14,1.87 M201.4,184.06l1.33-4.93l0.77,2.92 M201.4,184.06l2.11-2.01l2.24,2.29l2.41,0.33
	 M201.4,184.06l6.76,0.61l1.18-1.84L201.4,184.06 M192.89,173.51l-0.8-2.96 M184.92,174.71l7.16-4.17l-2.23-2.28 M184.92,174.71
	l4.93-6.44l-2.32-0.24 M184.92,174.71l2.61-6.68l-1.05,1.91 M184.92,174.71l1.56-4.77l0.81,2.92 M184.92,174.71l2.37-1.85l2.19,2.26
	 M184.92,174.71l6.88,0.69l1.09-1.89L184.92,174.71 M177.31,164.68l-0.84-2.98 M169.31,165.85l7.16-4.15l-2.18-2.25 M169.31,165.85
	l4.98-6.4l-2.23-0.19 M169.31,165.85l2.75-6.59l-0.97,1.95 M169.31,165.85l1.78-4.64l0.84,2.94 M169.31,165.85l2.62-1.7l2.15,2.23
	 M169.31,165.85l4.77,0.53 M169.31,165.85l7,0.76l1-1.94L169.31,165.85 M162.54,156.31l-0.87-3 M154.49,157.45l7.18-4.13l-2.15-2.23
	 M154.49,157.45l5.03-6.37l-2.15-0.15l-0.89,2 M154.49,157.45l1.98-4.52l0.87,2.96 M154.49,157.45l2.85-1.56l2.12,2.21
	 M154.49,157.45l4.97,0.65l2.15,0.18 M154.49,157.45l7.13,0.84l0.92-1.97L154.49,157.45 M162.55,139.14l-0.87-3.04 M154.49,140.22
	l7.19-4.12l-2.16-2.19 M154.49,140.22l5.03-6.31l-2.16-0.06 M154.49,140.22l2.88-6.37l-0.89,2.09 M154.49,140.22l1.99-4.28l0.87,3
	 M154.49,140.22l2.86-1.28l2.12,2.18 M154.49,140.22l4.98,0.9 M154.49,140.22l7.13,0.99l0.93-2.07L154.49,140.22 M162.57,121.05
	l-0.87-3.08l-7.21,4.1l7.21-4.1l-2.16-2.17 M154.49,122.06l5.05-6.27l-2.16,0.04 M154.49,122.06l2.89-6.23l-0.89,2.19
	 M154.49,122.06l1.99-4.04l0.87,3.05 M154.49,122.06l2.86-0.99l2.13,2.14 M154.49,122.06l4.99,1.15h2.16 M154.49,122.06l7.15,1.15
	l0.93-2.17L154.49,122.06 M162.61,101.95l-0.88-3.14 M154.49,102.9l7.24-4.09l-2.17-2.13 M154.49,102.9l5.07-6.22l-2.17,0.14
	 M154.49,102.9l2.9-6.08l-0.9,2.3 M154.49,102.9l2-3.78l0.88,3.1 M154.49,102.9l2.88-0.68l2.14,2.11 M154.49,102.9l5.01,1.44
	l2.17-0.1 M154.49,102.9l7.18,1.33l0.93-2.29L154.49,102.9 M162.66,81.77l-0.88-3.21 M154.49,82.66l7.28-4.09l-2.18-2.1
	 M154.49,82.66l5.1-6.19l-2.18,0.25 M154.49,82.66l2.91-5.94l-0.9,2.43 M154.49,82.66l2.01-3.52l0.88,3.16l2.15,2.08 M154.49,82.66
	l5.05,1.73l2.18-0.21 M154.49,82.66l7.23,1.52l0.94-2.41L154.49,82.66 M162.73,60.41l-0.89-3.28 M154.49,61.23l7.35-4.1l-2.2-2.07
	 M154.49,61.23l5.15-6.17l-2.2,0.37 M154.49,61.23l2.94-5.8l-0.91,2.56 M154.49,61.23l2.03-3.24l0.89,3.24 M154.49,61.23h2.92
	l2.17,2.06 M154.49,61.23l5.09,2.06l2.2-0.32 M154.49,61.23l7.29,1.73l0.95-2.55L154.49,61.23 M179.7,67.16l-0.85-3.26 M171.54,68
	l7.31-4.1l-2.24-2.08 M171.54,68l5.08-6.18l-2.29,0.33 M171.54,68l2.79-5.84l-1,2.52 M171.54,68l1.78-3.33l0.85,3.22 M171.54,68
	l2.63-0.11l2.2,2.06 M171.54,68l4.84,1.95l2.29-0.29 M171.54,68l7.13,1.67l1.04-2.51L171.54,68 M197.74,74.34l-0.81-3.24
	 M189.65,75.2l7.28-4.11L194.66,69 M189.65,75.2l5.01-6.2l-2.39,0.29l-1.1,2.47 M189.65,75.2l1.52-3.43l0.81,3.2 M189.65,75.2
	l2.33-0.23l2.24,2.08 M189.65,75.2l4.58,1.85l2.38-0.25 M189.65,75.2l6.96,1.6l1.13-2.46L189.65,75.2 M216.95,81.96l-0.76-3.23
	 M208.92,82.85l7.26-4.12l-2.32-2.11 M208.92,82.85l4.94-6.23l-2.5,0.25 M208.92,82.85l2.44-5.98l-1.2,2.44 M208.92,82.85l1.24-3.54
	l0.77,3.18 M208.92,82.85l2.01-0.36l2.29,2.1 M208.92,82.85l4.3,1.74l2.49-0.21 M208.92,82.85l6.79,1.53l1.24-2.43L208.92,82.85"/>
<path class="st0" d="M154.49,267.45l4.36,4.97l-1.29-2.36 M154.49,267.45l3.06,2.6l-3.06-0.97l-3.07,0.97 M154.49,267.45l-3.07,2.6
	l-1.29,2.36 M154.49,267.45l-4.36,4.97l1.26,2.39 M154.49,267.45l-3.1,7.35l3.1,1 M154.49,267.45v8.35l3.1-1L154.49,267.45
	 M138.9,260.54l1.35-2.3 M135.75,253.17l4.5,5.07l-1.19-2.28 M135.75,253.17l3.32,2.79l-3.01-0.93l-3.09,0.93 M135.75,253.17
	l-2.78,2.79l-1.39,2.28 M135.75,253.17l-4.17,5.07l1.15,2.3 M135.75,253.17l-3.02,7.37l3.04,0.96 M135.75,253.17l0.02,8.32
	l3.13-0.96L135.75,253.17 M121.41,247.2l1.44-2.22 M118.2,239.81l4.64,5.17l-1.09-2.19 M118.2,239.81l3.56,2.98l-2.96-0.9l-3.12,0.9
	 M118.2,239.81l-2.52,2.98l-1.48,2.19 M118.2,239.81l-4,5.17l1.06,2.22 M118.2,239.81l-2.94,7.39l2.99,0.93 M118.2,239.81l0.05,8.32
	l3.15-0.93L118.2,239.81 M105.01,234.7l1.53-2.15 M101.75,227.27l4.79,5.28l-1-2.13 M101.75,227.27l3.79,3.16l-2.92-0.87l-3.15,0.87
	 M101.75,227.27l-3.84,5.28l0.97,2.15 M101.75,227.27l-2.88,7.43l2.95,0.9 M101.75,227.27l0.07,8.33l3.19-0.9L101.75,227.27
	 M89.61,222.98l1.62-2.09 M86.29,215.49l4.94,5.39l-0.92-2.06 M86.29,215.49l4.01,3.33l-2.89-0.85 M86.29,215.49l1.12,2.48
	l-3.19,0.85 M86.29,215.49l-2.06,3.33 M86.29,215.49l-3.71,5.39l0.88,2.09 M86.29,215.49l-2.83,7.48l2.92,0.87 M86.29,215.49
	l0.09,8.36l3.23-0.87L86.29,215.49 M75.11,211.94l1.7-2.03 M71.73,204.41l5.08,5.51l-0.84-2.02 M71.73,204.41l4.24,3.49l-2.87-0.83
	 M71.73,204.41l1.37,2.67l-3.23,0.83 M71.73,204.41l-1.86,3.49l-1.73,2.02 M71.73,204.41l-3.59,5.51l0.81,2.03 M71.73,204.41
	l-2.78,7.54l2.9,0.85 M71.73,204.41l0.12,8.39l3.27-0.85L71.73,204.41 M157.51,165l1.23-1.74l-1.26-1.73 M154.49,157.45l2.99,4.09
	l-2.99-0.71l-2.99,0.71 M154.49,157.45l-4.25,5.82l1.23,1.74 M154.49,157.45l-3.03,7.56l3.03,0.73 M154.49,157.45v8.29l3.02-0.73
	L154.49,157.45 M139.67,165.85l3.07,7.53l1.31-1.79 M139.67,165.85l4.38,5.74l-1.19-1.77 M139.67,165.85l3.2,3.97l-2.96-0.73
	l-3.03,0.73 M139.67,165.85l-2.79,3.97 M139.67,165.85l-4.13,5.74l1.15,1.79 M139.67,165.85l-2.97,7.53l2.99,0.75 M139.67,165.85
	l0.02,8.28l3.05-0.75L139.67,165.85 M127.19,182.23l1.39-1.84 M124.06,174.71l4.53,5.68l-1.1-1.82 M124.06,174.71l3.43,3.86
	l-2.93-0.75 M124.06,174.71l0.49,3.1l-3.06,0.75 M120.07,180.39l3.99-5.68L120.07,180.39l1.07,1.84 M124.06,174.71l-2.92,7.52
	l2.96,0.77 M124.06,174.71l0.04,8.29l3.09-0.77L124.06,174.71 M110.78,191.57l1.49-1.9 M107.58,184.06l4.7,5.61l-1.02-1.88
	 M107.58,184.06l3.67,3.74l-2.91-0.77 M107.58,184.06l0.77,2.96l-3.11,0.77 M107.58,184.06l-2.34,3.74l-1.52,1.88 M107.58,184.06
	l-3.86,5.61l0.98,1.9 M107.58,184.06l-2.87,7.51l2.94,0.79 M107.58,184.06l0.07,8.3l3.14-0.79L107.58,184.06 M93.45,201.47
	l1.58-1.96 M90.16,193.95l4.87,5.56l-0.93-1.94 M90.16,193.95l3.94,3.62l-2.89-0.8 M90.16,193.95l1.06,2.82l-3.16,0.8 M90.16,193.95
	l-2.11,3.62l-1.62,1.94 M90.16,193.95l-3.73,5.56l0.9,1.96 M90.16,193.95l-2.82,7.52l2.91,0.82 M90.16,193.95l0.09,8.34l3.2-0.82
	L90.16,193.95 M240.03,211.94l0.81-2.03 M237.25,204.41l3.59,5.51l-1.73-2.02 M237.25,204.41l1.86,3.49l-3.23-0.83l-2.86,0.83
	 M237.25,204.41l-4.24,3.49l-0.85,2.02 M237.25,204.41l-5.08,5.51l1.7,2.03 M237.25,204.41l-3.38,7.54l3.27,0.85 M237.25,204.41
	l-0.12,8.39l2.9-0.85L237.25,204.41 M221.65,201.47l0.9-1.96 M218.82,193.95l3.73,5.56l-1.62-1.94 M218.82,193.95l2.11,3.62
	l-3.16-0.8 M218.82,193.95l-1.06,2.82l-2.89,0.8 M218.82,193.95l-3.94,3.62l-0.93,1.94 M218.82,193.95l-4.87,5.56l1.58,1.96
	 M218.82,193.95l-3.29,7.52l3.2,0.82 M218.82,193.95l-0.09,8.34l2.91-0.82L218.82,193.95 M204.28,191.57l0.98-1.9 M201.4,184.06
	l3.86,5.61l-1.51-1.88 M201.4,184.06l2.35,3.74l-3.11-0.77 M201.4,184.06l-0.76,2.96l-2.91,0.77 M201.4,184.06l-3.67,3.74
	l-1.02,1.88 M201.4,184.06l-4.69,5.61l1.48,1.9 M201.4,184.06l-3.21,7.51l3.15,0.79 M201.4,184.06l-0.06,8.3l2.94-0.79L201.4,184.06
	 M187.84,182.23l1.07-1.84 M184.92,174.71l3.99,5.68l-1.42-1.82 M184.92,174.71l2.57,3.86l-3.06-0.75 M184.92,174.71l-0.49,3.1
	l-2.93,0.75 M184.92,174.71l-3.43,3.86l-1.1,1.82 M184.92,174.71l-4.53,5.68l1.4,1.84 M184.92,174.71l-3.14,7.52l3.09,0.77
	 M184.92,174.71l-0.04,8.29l2.96-0.77L184.92,174.71 M172.28,173.39l1.15-1.79 M169.31,165.85l4.13,5.74l-1.34-1.77 M169.31,165.85
	l2.79,3.97l-3.03-0.73l-2.96,0.73 M169.31,165.85l-3.2,3.97 M169.31,165.85l-4.38,5.74l1.31,1.79 M169.31,165.85l-3.07,7.53
	l3.05,0.75 M169.31,165.85l-0.02,8.28l2.99-0.75L169.31,165.85 M225.52,222.98l0.88-2.09 M222.69,215.49l3.71,5.39l-1.65-2.06
	 M222.69,215.49l2.06,3.33l-3.19-0.85l-2.89,0.85 M222.69,215.49l-4.01,3.33l-0.92,2.06 M222.69,215.49l-4.94,5.39l1.62,2.09
	 M222.69,215.49l-3.32,7.48l3.23,0.87 M222.69,215.49l-0.09,8.36l2.92-0.87L222.69,215.49 M210.11,234.7l0.97-2.15l-1.56-2.13
	 M207.23,227.27l2.28,3.16l-3.15-0.87 M207.23,227.27l-0.87,2.28l-2.92,0.87 M207.23,227.27l-3.79,3.16l-1,2.13 M207.23,227.27
	l-4.79,5.28l1.53,2.15 M207.23,227.27l-3.27,7.43l3.19,0.9 M207.23,227.27l-0.07,8.33l2.95-0.9L207.23,227.27 M193.72,247.2
	l1.05-2.22 M190.78,239.81l4,5.17l-1.47-2.19 M190.78,239.81l2.52,2.98l-3.12-0.9l-2.96,0.9 M190.78,239.81l-3.56,2.98l-1.09,2.19
	 M190.78,239.81l-4.64,5.17l1.44,2.22 M190.78,239.81l-3.2,7.39l3.15,0.93 M190.78,239.81l-0.05,8.32l2.99-0.93L190.78,239.81
	 M176.25,260.54l1.15-2.3 M173.24,253.17l4.17,5.07l-1.39-2.28 M173.24,253.17l2.78,2.79l-3.09-0.93l-3.01,0.93 M173.24,253.17
	l-3.32,2.79l-1.19,2.28 M173.24,253.17l-4.5,5.07l1.35,2.3 M173.24,253.17l-3.15,7.37l3.13,0.96 M173.24,253.17l-0.02,8.32
	l3.04-0.96L173.24,253.17 M70.89,199.12l-1.35-1.79 M71.73,204.41l-2.18-7.07l-2.64,0.4 M71.73,204.41l-4.83-6.67l-2.38,2.38
	 M71.73,204.41l-7.21-4.28l-0.7,2.95L71.73,204.41l-7.91-1.33l1.39,1.77 M71.73,204.41l-6.52,0.43l2.64-0.44 M71.73,204.41
	l-3.88-0.01l2.34-2.36 M71.73,204.41l-1.54-2.37l0.71-2.91L71.73,204.41 M68.43,180.99l-1.36-1.88 M69.24,185.99l-2.16-6.89
	l-2.65,0.3 M69.24,185.99l-4.81-6.58l-2.38,2.34 M69.24,185.99l-7.19-4.25l-0.7,2.98 M69.24,185.99l-7.89-1.26l1.4,1.86
	 M69.24,185.99l-6.49,0.6l2.65-0.35 M69.24,185.99l-3.84,0.25l2.34-2.31 M69.24,185.99l-1.5-2.06l0.7-2.95L69.24,185.99
	 M65.83,161.71l-1.38-1.98 M66.59,166.44l-2.14-6.71l-2.67,0.2 M66.59,166.44l-4.8-6.52l-2.39,2.3 M66.59,166.44l-7.19-4.22
	l-0.69,3.03 M66.59,166.44l-7.88-1.19l1.41,1.96 M66.59,166.44l-6.46,0.77l2.66-0.24 M66.59,166.44l-3.8,0.53l2.35-2.27
	 M66.59,166.44l-1.45-1.74l0.69-2.99L66.59,166.44 M63.05,141.2l-1.39-2.1 M63.77,145.64l-2.11-6.54l-2.68,0.09 M63.77,145.64
	l-4.8-6.45l-2.4,2.25 M63.77,145.64l-7.2-4.2l-0.68,3.08 M63.77,145.64l-7.88-1.12l1.43,2.08 M63.77,145.64l-6.45,0.96l2.68-0.12
	 M63.77,145.64L60,146.47l2.36-2.23 M63.77,145.64l-1.41-1.4l0.69-3.04L63.77,145.64 M60.08,119.32l-1.41-2.23 M60.77,123.45
	l-2.1-6.36l-2.71-0.03 M60.77,123.45l-4.81-6.39l-2.42,2.2 M60.77,123.45l-7.23-4.19l-0.68,3.15 M60.77,123.45l-7.9-1.04l1.46,2.21
	 M60.77,123.45l-6.45,1.17l2.7-0.01 M60.77,123.45l-3.75,1.16l2.38-2.19 M60.77,123.45l-1.37-1.03l0.68-3.1L60.77,123.45
	 M56.91,95.93l-1.44-2.37 M57.55,99.75l-2.08-6.19l-2.75-0.16 M57.55,99.75l-4.83-6.35l-2.44,2.17 M57.55,99.75l-7.27-4.18
	l-0.67,3.22 M57.55,99.75l-7.94-0.97l1.48,2.35 M57.55,99.75l-6.46,1.39l2.74,0.12 M57.55,99.75l-3.72,1.51l2.4-2.15 M57.55,99.75
	l-1.33-0.64l0.68-3.18L57.55,99.75 M152.46,57.99l-0.91-2.56 M154.49,61.23l-2.95-5.8l-2.2-0.37 M154.49,61.23l-5.15-6.17l-2.2,2.07
	 M154.49,61.23l-7.36-4.1l-0.89,3.28 M154.49,61.23l-8.25-0.81l0.95,2.55 M154.49,61.23l-7.3,1.73l2.2,0.32 M154.49,61.23l-5.1,2.06
	l2.17-2.06 M154.49,61.23h-2.92l0.89-3.24L154.49,61.23 M135.66,64.67l-1-2.52 M137.44,68l-2.79-5.84l-2.29-0.33"/>
<g>
	<polygon class="st1" points="57.55,99.75 154.49,267.45 71.73,204.41 	"/>
	<polygon class="st2" points="154.49,61.23 154.49,154.19 57.55,99.75 	"/>
	<polygon class="st3" points="237.25,204.41 154.49,267.45 251.43,99.75 	"/>
	<g>
		<polygon class="st1" points="154.49,154.19 154.49,267.45 57.55,99.75 		"/>
		<polygon class="st3" points="251.43,99.75 154.49,267.45 154.49,154.19 		"/>
		<polygon class="st2" points="251.43,99.75 154.49,154.19 154.49,61.23 		"/>
	</g>
</g>
<line class="st4" x1="71.73" y1="204.41" x2="57.56" y2="99.81"/>
<line class="st4" x1="154.49" y1="267.45" x2="71.73" y2="204.41"/>
<line class="st4" x1="57.55" y1="99.75" x2="154.49" y2="61.23"/>
<line class="st4" x1="237.25" y1="204.41" x2="251.42" y2="99.81"/>
<line class="st4" x1="154.49" y1="267.45" x2="237.25" y2="204.41"/>
<path class="st4" d="M251.43,99.75l-96.94-38.52 M57.55,99.75L57.55,99.75 M251.43,99.75L251.43,99.75 M154.49,154.19l96.94-54.45
	 M154.49,154.19v113.26 M57.55,99.75l96.94,54.45"/>
<line class="st0" x1="157.59" y1="274.8" x2="158.85" y2="272.42"/>
<polygon class="st5" points="264.62,258.4 264.46,257.92 264.03,257.81 "/>
<polygon class="st5" points="264.62,258.4 264.03,257.81 263.52,258.11 "/>
<polygon class="st5" points="264.62,258.4 263.52,258.11 263.1,258.71 "/>
<polygon class="st5" points="264.62,258.4 263.1,258.71 262.94,259.37 "/>
<polygon class="st5" points="264.62,258.4 262.94,259.37 263.1,259.85 "/>
<polygon class="st5" points="264.62,258.4 263.1,259.85 263.52,259.96 "/>
<polygon class="st5" points="264.62,258.4 263.52,259.96 264.03,259.66 "/>
<polygon class="st5" points="264.62,258.4 264.03,259.66 264.46,259.06 "/>
<polygon class="st6" points="258.69,257.21 258.73,257.33 256.55,256.07 "/>
<polygon class="st6" points="256.51,255.95 254.36,254.81 256.55,256.07 "/>
<polygon class="st7" points="258.65,257.09 256.51,255.95 258.69,257.21 "/>
<polygon class="st8" points="258.69,257.21 256.51,255.95 256.55,256.07 "/>
<polygon class="st6" points="260.87,258.47 258.73,257.33 260.91,258.59 "/>
<polygon class="st6" points="263.06,259.73 263.1,259.85 260.91,258.59 "/>
<polygon class="st7" points="263.02,259.61 263.06,259.73 260.87,258.47 "/>
<polygon class="st8" points="260.87,258.47 263.06,259.73 260.91,258.59 "/>
<polygon class="st9" points="260.8,258.23 258.65,257.09 260.84,258.35 "/>
<polygon class="st9" points="262.98,259.49 263.02,259.61 260.84,258.35 "/>
<polygon class="st10" points="262.94,259.37 262.98,259.49 260.8,258.23 "/>
<polygon class="st11" points="260.8,258.23 262.98,259.49 260.84,258.35 "/>
<polygon class="st8" points="258.69,257.21 258.73,257.33 260.87,258.47 "/>
<polygon class="st12" points="260.84,258.35 263.02,259.61 260.87,258.47 "/>
<polygon class="st12" points="258.65,257.09 260.84,258.35 258.69,257.21 "/>
<polygon class="st7" points="258.69,257.21 260.84,258.35 260.87,258.47 "/>
<polygon class="st13" points="258.61,256.97 258.57,256.85 260.75,258.11 "/>
<polygon class="st13" points="260.8,258.23 262.94,259.37 260.75,258.11 "/>
<polygon class="st11" points="258.65,257.09 260.8,258.23 258.61,256.97 "/>
<polygon class="st10" points="258.61,256.97 260.8,258.23 260.75,258.11 "/>
<polygon class="st13" points="256.43,255.71 258.57,256.85 256.38,255.59 "/>
<polygon class="st13" points="254.24,254.45 254.2,254.33 256.38,255.59 "/>
<polygon class="st11" points="254.28,254.57 254.24,254.45 256.43,255.71 "/>
<polygon class="st10" points="256.43,255.71 254.24,254.45 256.38,255.59 "/>
<polygon class="st12" points="256.51,255.95 258.65,257.09 256.47,255.83 "/>
<polygon class="st12" points="254.32,254.69 254.28,254.57 256.47,255.83 "/>
<polygon class="st8" points="254.36,254.81 254.32,254.69 256.51,255.95 "/>
<polygon class="st7" points="256.51,255.95 254.32,254.69 256.47,255.83 "/>
<polygon class="st10" points="258.61,256.97 258.57,256.85 256.43,255.71 "/>
<polygon class="st9" points="256.47,255.83 254.28,254.57 256.43,255.71 "/>
<polygon class="st9" points="258.65,257.09 256.47,255.83 258.61,256.97 "/>
<polygon class="st11" points="258.61,256.97 256.47,255.83 256.43,255.71 "/>
<polygon class="st14" points="258.65,256.52 254.2,254.33 258.57,256.85 "/>
<polygon class="st14" points="263.02,259.04 262.94,259.37 258.57,256.85 "/>
<polygon class="st15" points="263.1,258.71 263.02,259.04 258.65,256.52 "/>
<polygon class="st16" points="258.65,256.52 263.02,259.04 258.57,256.85 "/>
<polygon class="st17" points="258.65,256.52 263.1,258.71 258.73,256.19 "/>
<polygon class="st17" points="254.28,254 254.36,253.67 258.73,256.19 "/>
<polygon class="st16" points="254.2,254.33 254.28,254 258.65,256.52 "/>
<polygon class="st15" points="258.65,256.52 254.28,254 258.73,256.19 "/>
<polygon class="st18" points="263.52,258.11 263.1,258.71 254.36,253.67 "/>
<polygon class="st19" points="254.36,253.67 254.78,253.07 263.52,258.11 "/>
<polygon class="st20" points="259.28,255.52 259.15,255.59 256.96,254.33 "/>
<polygon class="st20" points="257.09,254.26 254.78,253.07 256.96,254.33 "/>
<polygon class="st21" points="259.41,255.44 257.09,254.26 259.28,255.52 "/>
<polygon class="st22" points="259.28,255.52 257.09,254.26 256.96,254.33 "/>
<polygon class="st20" points="261.46,256.78 259.15,255.59 261.33,256.85 "/>
<polygon class="st20" points="263.65,258.04 263.52,258.11 261.33,256.85 "/>
<polygon class="st21" points="263.78,257.96 263.65,258.04 261.46,256.78 "/>
<polygon class="st22" points="261.46,256.78 263.65,258.04 261.33,256.85 "/>
<polygon class="st23" points="261.72,256.63 259.41,255.44 261.59,256.7 "/>
<polygon class="st23" points="263.9,257.89 263.78,257.96 261.59,256.7 "/>
<polygon class="st24" points="264.03,257.81 263.9,257.89 261.72,256.63 "/>
<polygon class="st25" points="261.72,256.63 263.9,257.89 261.59,256.7 "/>
<polygon class="st22" points="259.28,255.52 259.15,255.59 261.46,256.78 "/>
<polygon class="st26" points="261.59,256.7 263.78,257.96 261.46,256.78 "/>
<polygon class="st26" points="259.41,255.44 261.59,256.7 259.28,255.52 "/>
<polygon class="st21" points="259.28,255.52 261.59,256.7 261.46,256.78 "/>
<polygon class="st27" points="259.54,255.37 259.67,255.3 261.85,256.55 "/>
<polygon class="st27" points="261.72,256.63 264.03,257.81 261.85,256.55 "/>
<polygon class="st25" points="259.41,255.44 261.72,256.63 259.54,255.37 "/>
<polygon class="st24" points="259.54,255.37 261.72,256.63 261.85,256.55 "/>
<polygon class="st27" points="257.35,254.11 259.67,255.3 257.48,254.04 "/>
<polygon class="st27" points="255.17,252.85 255.3,252.78 257.48,254.04 "/>
<polygon class="st25" points="255.04,252.93 255.17,252.85 257.35,254.11 "/>
<polygon class="st24" points="257.35,254.11 255.17,252.85 257.48,254.04 "/>
<polygon class="st26" points="257.09,254.26 259.41,255.44 257.22,254.18 "/>
<polygon class="st26" points="254.91,253 255.04,252.93 257.22,254.18 "/>
<polygon class="st22" points="254.78,253.07 254.91,253 257.09,254.26 "/>
<polygon class="st21" points="257.09,254.26 254.91,253 257.22,254.18 "/>
<polygon class="st24" points="259.54,255.37 259.67,255.3 257.35,254.11 "/>
<polygon class="st23" points="257.22,254.18 255.04,252.93 257.35,254.11 "/>
<polygon class="st23" points="259.41,255.44 257.22,254.18 259.54,255.37 "/>
<polygon class="st25" points="259.54,255.37 257.22,254.18 257.35,254.11 "/>
<polygon class="st28" points="259.77,255.32 259.67,255.3 257.48,254.04 "/>
<polygon class="st28" points="257.59,254.06 255.3,252.78 257.48,254.04 "/>
<polygon class="st29" points="259.88,255.35 257.59,254.06 259.77,255.32 "/>
<polygon class="st30" points="259.77,255.32 257.59,254.06 257.48,254.04 "/>
<polygon class="st28" points="261.96,256.58 259.67,255.3 261.85,256.55 "/>
<polygon class="st28" points="264.14,257.84 264.03,257.81 261.85,256.55 "/>
<polygon class="st29" points="264.25,257.87 264.14,257.84 261.96,256.58 "/>
<polygon class="st30" points="261.96,256.58 264.14,257.84 261.85,256.55 "/>
<polygon class="st31" points="262.17,256.64 259.88,255.35 262.06,256.61 "/>
<polygon class="st31" points="264.35,257.9 264.25,257.87 262.06,256.61 "/>
<polygon class="st32" points="264.46,257.92 264.35,257.9 262.17,256.64 "/>
<polygon class="st33" points="262.17,256.64 264.35,257.9 262.06,256.61 "/>
<polygon class="st30" points="259.77,255.32 259.67,255.3 261.96,256.58 "/>
<polygon class="st34" points="262.06,256.61 264.25,257.87 261.96,256.58 "/>
<polygon class="st34" points="259.88,255.35 262.06,256.61 259.77,255.32 "/>
<polygon class="st29" points="259.77,255.32 262.06,256.61 261.96,256.58 "/>
<polygon class="st35" points="259.98,255.38 260.09,255.4 262.27,256.66 "/>
<polygon class="st35" points="262.17,256.64 264.46,257.92 262.27,256.66 "/>
<polygon class="st33" points="259.88,255.35 262.17,256.64 259.98,255.38 "/>
<polygon class="st32" points="259.98,255.38 262.17,256.64 262.27,256.66 "/>
<polygon class="st35" points="257.8,254.12 260.09,255.4 257.9,254.14 "/>
<polygon class="st35" points="255.61,252.86 255.72,252.88 257.9,254.14 "/>
<polygon class="st33" points="255.51,252.83 255.61,252.86 257.8,254.12 "/>
<polygon class="st32" points="257.8,254.12 255.61,252.86 257.9,254.14 "/>
<polygon class="st34" points="257.59,254.06 259.88,255.35 257.69,254.09 "/>
<polygon class="st34" points="255.4,252.8 255.51,252.83 257.69,254.09 "/>
<polygon class="st30" points="255.3,252.78 255.4,252.8 257.59,254.06 "/>
<polygon class="st29" points="257.59,254.06 255.4,252.8 257.69,254.09 "/>
<polygon class="st32" points="259.98,255.38 260.09,255.4 257.8,254.12 "/>
<polygon class="st31" points="257.69,254.09 255.51,252.83 257.8,254.12 "/>
<polygon class="st31" points="259.88,255.35 257.69,254.09 259.98,255.38 "/>
<polygon class="st33" points="259.98,255.38 257.69,254.09 257.8,254.12 "/>
<polygon class="st35" points="266.76,258.89 267.04,258.96 267.76,260.28 "/>
<polygon class="st35" points="267.48,260.21 268.48,261.6 267.76,260.28 "/>
<polygon class="st36" points="266.48,258.81 267.48,260.21 266.76,258.89 "/>
<polygon class="st37" points="266.76,258.89 267.48,260.21 267.76,260.28 "/>
<polygon class="st35" points="266.03,257.57 267.04,258.96 266.31,257.64 "/>
<polygon class="st35" points="265.31,256.25 265.59,256.32 266.31,257.64 "/>
<polygon class="st36" points="265.03,256.17 265.31,256.25 266.03,257.57 "/>
<polygon class="st37" points="266.03,257.57 265.31,256.25 266.31,257.64 "/>
<polygon class="st38" points="265.47,257.42 266.48,258.81 265.75,257.49 "/>
<polygon class="st38" points="264.75,256.1 265.03,256.17 265.75,257.49 "/>
<polygon class="st39" points="264.47,256.03 264.75,256.1 265.47,257.42 "/>
<polygon class="st40" points="265.47,257.42 264.75,256.1 265.75,257.49 "/>
<polygon class="st37" points="266.76,258.89 267.04,258.96 266.03,257.57 "/>
<polygon class="st8" points="265.75,257.49 265.03,256.17 266.03,257.57 "/>
<polygon class="st8" points="266.48,258.81 265.75,257.49 266.76,258.89 "/>
<polygon class="st36" points="266.76,258.89 265.75,257.49 266.03,257.57 "/>
<polygon class="st41" points="266.8,259.61 267.48,260.21 266.98,259.51 "/>
<polygon class="st42" points="266.3,258.91 266.48,258.81 266.98,259.51 "/>
<polygon class="st7" points="266.13,259.01 266.3,258.91 266.8,259.61 "/>
<polygon class="st31" points="266.8,259.61 266.3,258.91 266.98,259.51 "/>
<polygon class="st43" points="267.31,260.31 267.48,260.21 267.98,260.9 "/>
<polygon class="st44" points="267.81,261 268.48,261.6 267.98,260.9 "/>
<polygon class="st41" points="267.13,260.4 267.81,261 267.31,260.31 "/>
<polygon class="st43" points="267.31,260.31 267.81,261 267.98,260.9 "/>
<polygon class="st12" points="265.96,259.11 266.13,259.01 266.63,259.71 "/>
<polygon class="st38" points="266.46,259.81 267.13,260.4 266.63,259.71 "/>
<polygon class="st45" points="265.78,259.21 266.46,259.81 265.96,259.11 "/>
<polygon class="st12" points="265.96,259.11 266.46,259.81 266.63,259.71 "/>
<polygon class="st41" points="266.8,259.61 267.48,260.21 267.31,260.31 "/>
<polygon class="st46" points="266.63,259.71 267.13,260.4 267.31,260.31 "/>
<polygon class="st38" points="266.13,259.01 266.63,259.71 266.8,259.61 "/>
<polygon class="st31" points="266.8,259.61 266.63,259.71 267.31,260.31 "/>
<polygon class="st29" points="265.3,257.52 265.47,257.42 265.98,258.12 "/>
<polygon class="st47" points="265.8,258.22 266.48,258.81 265.98,258.12 "/>
<polygon class="st48" points="265.13,257.62 265.8,258.22 265.3,257.52 "/>
<polygon class="st49" points="265.3,257.52 265.8,258.22 265.98,258.12 "/>
<polygon class="st50" points="264.8,256.82 265.47,257.42 264.97,256.72 "/>
<polygon class="st51" points="264.3,256.13 264.47,256.03 264.97,256.72 "/>
<polygon class="st52" points="264.12,256.23 264.3,256.13 264.8,256.82 "/>
<polygon class="st51" points="264.8,256.82 264.3,256.13 264.97,256.72 "/>
<polygon class="st53" points="264.45,257.02 265.13,257.62 264.63,256.92 "/>
<polygon class="st27" points="263.95,256.33 264.12,256.23 264.63,256.92 "/>
<polygon class="st54" points="263.78,256.43 263.95,256.33 264.45,257.02 "/>
<polygon class="st27" points="264.45,257.02 263.95,256.33 264.63,256.92 "/>
<polygon class="st50" points="265.3,257.52 265.47,257.42 264.8,256.82 "/>
<polygon class="st52" points="264.63,256.92 264.12,256.23 264.8,256.82 "/>
<polygon class="st55" points="265.13,257.62 264.63,256.92 265.3,257.52 "/>
<polygon class="st55" points="265.3,257.52 264.63,256.92 264.8,256.82 "/>
<polygon class="st56" points="264.61,257.92 264.78,257.82 265.28,258.52 "/>
<polygon class="st11" points="265.11,258.61 265.78,259.21 265.28,258.52 "/>
<polygon class="st10" points="264.43,258.02 265.11,258.61 264.61,257.92 "/>
<polygon class="st56" points="264.61,257.92 265.11,258.61 265.28,258.52 "/>
<polygon class="st24" points="264.11,257.22 264.78,257.82 264.28,257.12 "/>
<polygon class="st25" points="263.6,256.53 263.78,256.43 264.28,257.12 "/>
<polygon class="st57" points="263.43,256.63 263.6,256.53 264.11,257.22 "/>
<polygon class="st58" points="264.11,257.22 263.6,256.53 264.28,257.12 "/>
<polygon class="st23" points="263.76,257.42 264.43,258.02 263.93,257.32 "/>
<polygon class="st59" points="263.26,256.73 263.43,256.63 263.93,257.32 "/>
<polygon class="st21" points="263.08,256.82 263.26,256.73 263.76,257.42 "/>
<polygon class="st59" points="263.76,257.42 263.26,256.73 263.93,257.32 "/>
<polygon class="st24" points="264.61,257.92 264.78,257.82 264.11,257.22 "/>
<polygon class="st23" points="263.93,257.32 263.43,256.63 264.11,257.22 "/>
<polygon class="st60" points="264.43,258.02 263.93,257.32 264.61,257.92 "/>
<polygon class="st58" points="264.61,257.92 263.93,257.32 264.11,257.22 "/>
<polygon class="st48" points="265.63,258.32 265.13,257.62 265.8,258.22 "/>
<polygon class="st7" points="266.3,258.91 266.48,258.81 265.8,258.22 "/>
<polygon class="st49" points="266.13,259.01 266.3,258.91 265.63,258.32 "/>
<polygon class="st49" points="265.63,258.32 266.3,258.91 265.8,258.22 "/>
<polygon class="st53" points="264.95,257.72 265.13,257.62 264.45,257.02 "/>
<polygon class="st54" points="264.28,257.12 263.78,256.43 264.45,257.02 "/>
<polygon class="st61" points="264.78,257.82 264.28,257.12 264.95,257.72 "/>
<polygon class="st61" points="264.95,257.72 264.28,257.12 264.45,257.02 "/>
<polygon class="st39" points="265.96,259.11 266.13,259.01 265.45,258.42 "/>
<polygon class="st28" points="265.28,258.52 264.78,257.82 265.45,258.42 "/>
<polygon class="st9" points="265.78,259.21 265.28,258.52 265.96,259.11 "/>
<polygon class="st9" points="265.96,259.11 265.28,258.52 265.45,258.42 "/>
<polygon class="st30" points="265.63,258.32 265.13,257.62 264.95,257.72 "/>
<polygon class="st28" points="265.45,258.42 264.78,257.82 264.95,257.72 "/>
<polygon class="st39" points="266.13,259.01 265.45,258.42 265.63,258.32 "/>
<polygon class="st30" points="265.63,258.32 265.45,258.42 264.95,257.72 "/>
<polygon class="st62" points="266.32,260.01 267.13,260.4 266.46,259.81 "/>
<polygon class="st63" points="265.64,259.41 265.78,259.21 266.46,259.81 "/>
<polygon class="st64" points="265.5,259.61 265.64,259.41 266.32,260.01 "/>
<polygon class="st65" points="266.32,260.01 265.64,259.41 266.46,259.81 "/>
<polygon class="st66" points="266.99,260.6 267.13,260.4 267.81,261 "/>
<polygon class="st67" points="267.67,261.2 268.48,261.6 267.81,261 "/>
<polygon class="st68" points="266.85,260.8 267.67,261.2 266.99,260.6 "/>
<polygon class="st69" points="266.99,260.6 267.67,261.2 267.81,261 "/>
<polygon class="st70" points="265.36,259.81 265.5,259.61 266.18,260.2 "/>
<polygon class="st71" points="266.04,260.4 266.85,260.8 266.18,260.2 "/>
<polygon class="st72" points="265.22,260 266.04,260.4 265.36,259.81 "/>
<polygon class="st73" points="265.36,259.81 266.04,260.4 266.18,260.2 "/>
<polygon class="st74" points="266.32,260.01 267.13,260.4 266.99,260.6 "/>
<polygon class="st75" points="266.18,260.2 266.85,260.8 266.99,260.6 "/>
<polygon class="st76" points="265.5,259.61 266.18,260.2 266.32,260.01 "/>
<polygon class="st77" points="266.32,260.01 266.18,260.2 266.99,260.6 "/>
<polygon class="st78" points="264.29,258.22 264.43,258.02 265.11,258.61 "/>
<polygon class="st79" points="264.97,258.81 265.78,259.21 265.11,258.61 "/>
<polygon class="st80" points="264.15,258.41 264.97,258.81 264.29,258.22 "/>
<polygon class="st81" points="264.29,258.22 264.97,258.81 265.11,258.61 "/>
<polygon class="st82" points="263.62,257.62 264.43,258.02 263.76,257.42 "/>
<polygon class="st83" points="262.94,257.02 263.08,256.82 263.76,257.42 "/>
<polygon class="st84" points="262.8,257.22 262.94,257.02 263.62,257.62 "/>
<polygon class="st85" points="263.62,257.62 262.94,257.02 263.76,257.42 "/>
<polygon class="st86" points="263.34,258.02 264.15,258.41 263.48,257.82 "/>
<polygon class="st87" points="262.66,257.42 262.8,257.22 263.48,257.82 "/>
<polygon class="st88" points="262.52,257.62 262.66,257.42 263.34,258.02 "/>
<polygon class="st89" points="263.34,258.02 262.66,257.42 263.48,257.82 "/>
<polygon class="st90" points="264.29,258.22 264.43,258.02 263.62,257.62 "/>
<polygon class="st91" points="263.48,257.82 262.8,257.22 263.62,257.62 "/>
<polygon class="st92" points="264.15,258.41 263.48,257.82 264.29,258.22 "/>
<polygon class="st93" points="264.29,258.22 263.48,257.82 263.62,257.62 "/>
<polygon class="st94" points="263.73,259.01 263.87,258.81 264.55,259.41 "/>
<polygon class="st95" points="264.41,259.61 265.22,260 264.55,259.41 "/>
<polygon class="st96" points="263.59,259.21 264.41,259.61 263.73,259.01 "/>
<polygon class="st97" points="263.73,259.01 264.41,259.61 264.55,259.41 "/>
<polygon class="st98" points="263.06,258.41 263.87,258.81 263.2,258.21 "/>
<polygon class="st99" points="262.38,257.82 262.52,257.62 263.2,258.21 "/>
<polygon class="st100" points="262.24,258.01 262.38,257.82 263.06,258.41 "/>
<polygon class="st101" points="263.06,258.41 262.38,257.82 263.2,258.21 "/>
<polygon class="st102" points="262.78,258.81 263.59,259.21 262.92,258.61 "/>
<polygon class="st103" points="262.1,258.21 262.24,258.01 262.92,258.61 "/>
<polygon class="st104" points="261.96,258.41 262.1,258.21 262.78,258.81 "/>
<polygon class="st105" points="262.78,258.81 262.1,258.21 262.92,258.61 "/>
<polygon class="st106" points="263.73,259.01 263.87,258.81 263.06,258.41 "/>
<polygon class="st107" points="262.92,258.61 262.24,258.01 263.06,258.41 "/>
<polygon class="st108" points="263.59,259.21 262.92,258.61 263.73,259.01 "/>
<polygon class="st109" points="263.73,259.01 262.92,258.61 263.06,258.41 "/>
<polygon class="st110" points="264.83,259.01 264.15,258.41 264.97,258.81 "/>
<polygon class="st111" points="265.64,259.41 265.78,259.21 264.97,258.81 "/>
<polygon class="st112" points="265.5,259.61 265.64,259.41 264.83,259.01 "/>
<polygon class="st113" points="264.83,259.01 265.64,259.41 264.97,258.81 "/>
<polygon class="st114" points="264.01,258.61 264.15,258.41 263.34,258.02 "/>
<polygon class="st115" points="263.2,258.21 262.52,257.62 263.34,258.02 "/>
<polygon class="st116" points="263.87,258.81 263.2,258.21 264.01,258.61 "/>
<polygon class="st117" points="264.01,258.61 263.2,258.21 263.34,258.02 "/>
<polygon class="st118" points="265.36,259.81 265.5,259.61 264.69,259.21 "/>
<polygon class="st119" points="264.55,259.41 263.87,258.81 264.69,259.21 "/>
<polygon class="st120" points="265.22,260 264.55,259.41 265.36,259.81 "/>
<polygon class="st121" points="265.36,259.81 264.55,259.41 264.69,259.21 "/>
<polygon class="st122" points="264.83,259.01 264.15,258.41 264.01,258.61 "/>
<polygon class="st123" points="264.69,259.21 263.87,258.81 264.01,258.61 "/>
<polygon class="st124" points="265.5,259.61 264.69,259.21 264.83,259.01 "/>
<polygon class="st125" points="264.83,259.01 264.69,259.21 264.01,258.61 "/>
<polygon class="st126" points="265.98,260.62 266.85,260.8 266.04,260.4 "/>
<polygon class="st72" points="265.17,260.22 265.22,260 266.04,260.4 "/>
<polygon class="st127" points="265.12,260.45 265.17,260.22 265.98,260.62 "/>
<polygon class="st128" points="265.98,260.62 265.17,260.22 266.04,260.4 "/>
<polygon class="st129" points="266.8,261.02 266.85,260.8 267.67,261.2 "/>
<polygon class="st67" points="267.61,261.42 268.48,261.6 267.67,261.2 "/>
<polygon class="st130" points="266.75,261.24 267.61,261.42 266.8,261.02 "/>
<polygon class="st131" points="266.8,261.02 267.61,261.42 267.67,261.2 "/>
<polygon class="st132" points="265.06,260.67 265.12,260.45 265.93,260.84 "/>
<polygon class="st133" points="265.88,261.07 266.75,261.24 265.93,260.84 "/>
<polygon class="st134" points="265.01,260.89 265.88,261.07 265.06,260.67 "/>
<polygon class="st135" points="265.06,260.67 265.88,261.07 265.93,260.84 "/>
<polygon class="st136" points="265.98,260.62 266.85,260.8 266.8,261.02 "/>
<polygon class="st137" points="265.93,260.84 266.75,261.24 266.8,261.02 "/>
<polygon class="st138" points="265.12,260.45 265.93,260.84 265.98,260.62 "/>
<polygon class="st139" points="265.98,260.62 265.93,260.84 266.8,261.02 "/>
<polygon class="st140" points="263.54,259.43 263.59,259.21 264.41,259.61 "/>
<polygon class="st141" points="264.35,259.83 265.22,260 264.41,259.61 "/>
<polygon class="st142" points="263.49,259.65 264.35,259.83 263.54,259.43 "/>
<polygon class="st143" points="263.54,259.43 264.35,259.83 264.41,259.61 "/>
<polygon class="st102" points="262.73,259.03 263.59,259.21 262.78,258.81 "/>
<polygon class="st144" points="261.91,258.63 261.96,258.41 262.78,258.81 "/>
<polygon class="st145" points="261.86,258.85 261.91,258.63 262.73,259.03 "/>
<polygon class="st146" points="262.73,259.03 261.91,258.63 262.78,258.81 "/>
<polygon class="st147" points="262.62,259.47 263.49,259.65 262.67,259.25 "/>
<polygon class="st148" points="261.8,259.07 261.86,258.85 262.67,259.25 "/>
<polygon class="st149" points="261.75,259.29 261.8,259.07 262.62,259.47 "/>
<polygon class="st150" points="262.62,259.47 261.8,259.07 262.67,259.25 "/>
<polygon class="st151" points="263.54,259.43 263.59,259.21 262.73,259.03 "/>
<polygon class="st152" points="262.67,259.25 261.86,258.85 262.73,259.03 "/>
<polygon class="st153" points="263.49,259.65 262.67,259.25 263.54,259.43 "/>
<polygon class="st154" points="263.54,259.43 262.67,259.25 262.73,259.03 "/>
<polygon class="st155" points="263.33,260.31 263.38,260.09 264.19,260.49 "/>
<polygon class="st156" points="264.14,260.71 265.01,260.89 264.19,260.49 "/>
<polygon class="st157" points="263.27,260.53 264.14,260.71 263.33,260.31 "/>
<polygon class="st158" points="263.33,260.31 264.14,260.71 264.19,260.49 "/>
<polygon class="st159" points="262.51,259.91 263.38,260.09 262.57,259.69 "/>
<polygon class="st160" points="261.7,259.51 261.75,259.29 262.57,259.69 "/>
<polygon class="st161" points="261.64,259.73 261.7,259.51 262.51,259.91 "/>
<polygon class="st162" points="262.51,259.91 261.7,259.51 262.57,259.69 "/>
<polygon class="st163" points="262.41,260.35 263.27,260.53 262.46,260.13 "/>
<polygon class="st164" points="261.59,259.96 261.64,259.73 262.46,260.13 "/>
<polygon class="st165" points="261.54,260.18 261.59,259.96 262.41,260.35 "/>
<polygon class="st166" points="262.41,260.35 261.59,259.96 262.46,260.13 "/>
<polygon class="st167" points="263.33,260.31 263.38,260.09 262.51,259.91 "/>
<polygon class="st168" points="262.46,260.13 261.64,259.73 262.51,259.91 "/>
<polygon class="st169" points="263.27,260.53 262.46,260.13 263.33,260.31 "/>
<polygon class="st170" points="263.33,260.31 262.46,260.13 262.51,259.91 "/>
<polygon class="st171" points="264.3,260.05 263.49,259.65 264.35,259.83 "/>
<polygon class="st172" points="265.17,260.22 265.22,260 264.35,259.83 "/>
<polygon class="st173" points="265.12,260.45 265.17,260.22 264.3,260.05 "/>
<polygon class="st174" points="264.3,260.05 265.17,260.22 264.35,259.83 "/>
<polygon class="st175" points="263.43,259.87 263.49,259.65 262.62,259.47 "/>
<polygon class="st116" points="262.57,259.69 261.75,259.29 262.62,259.47 "/>
<polygon class="st125" points="263.38,260.09 262.57,259.69 263.43,259.87 "/>
<polygon class="st176" points="263.43,259.87 262.57,259.69 262.62,259.47 "/>
<polygon class="st177" points="265.06,260.67 265.12,260.45 264.25,260.27 "/>
<polygon class="st112" points="264.19,260.49 263.38,260.09 264.25,260.27 "/>
<polygon class="st65" points="265.01,260.89 264.19,260.49 265.06,260.67 "/>
<polygon class="st178" points="265.06,260.67 264.19,260.49 264.25,260.27 "/>
<polygon class="st179" points="264.3,260.05 263.49,259.65 263.43,259.87 "/>
<polygon class="st124" points="264.25,260.27 263.38,260.09 263.43,259.87 "/>
<polygon class="st180" points="265.12,260.45 264.25,260.27 264.3,260.05 "/>
<polygon class="st181" points="264.3,260.05 264.25,260.27 263.43,259.87 "/>
<polygon class="st46" points="265.12,261.21 265.01,260.89 266.75,261.24 "/>
<polygon class="st182" points="266.85,261.56 268.48,261.6 266.75,261.24 "/>
<polygon class="st32" points="265.22,261.52 266.85,261.56 265.12,261.21 "/>
<polygon class="st183" points="265.12,261.21 266.85,261.56 266.75,261.24 "/>
<polygon class="st184" points="263.38,260.85 265.01,260.89 263.27,260.53 "/>
<polygon class="st185" points="261.64,260.49 261.54,260.18 263.27,260.53 "/>
<polygon class="st39" points="261.75,260.81 261.64,260.49 263.38,260.85 "/>
<polygon class="st186" points="263.38,260.85 261.64,260.49 263.27,260.53 "/>
<polygon class="st187" points="263.59,261.49 265.22,261.52 263.49,261.17 "/>
<polygon class="st188" points="261.86,261.13 261.75,260.81 263.49,261.17 "/>
<polygon class="st183" points="261.96,261.45 261.86,261.13 263.59,261.49 "/>
<polygon class="st41" points="263.59,261.49 261.86,261.13 263.49,261.17 "/>
<polygon class="st38" points="265.12,261.21 265.01,260.89 263.38,260.85 "/>
<polygon class="st47" points="263.49,261.17 261.75,260.81 263.38,260.85 "/>
<polygon class="st189" points="265.22,261.52 263.49,261.17 265.12,261.21 "/>
<polygon class="st42" points="265.12,261.21 263.49,261.17 263.38,260.85 "/>
<polygon class="st190" points="263.08,261.74 261.96,261.45 268.48,261.6 "/>
<polygon class="st191" points="255.88,244.25 256.22,243.88 256.1,243.46 "/>
<polygon class="st191" points="255.88,244.25 256.1,243.46 255.58,243.16 "/>
<polygon class="st191" points="255.88,244.25 255.58,243.16 254.85,243.09 "/>
<polygon class="st191" points="255.88,244.25 254.85,243.09 254.2,243.29 "/>
<polygon class="st191" points="255.88,244.25 254.2,243.29 253.86,243.66 "/>
<polygon class="st191" points="255.88,244.25 253.86,243.66 253.98,244.08 "/>
<polygon class="st191" points="255.88,244.25 253.98,244.08 254.5,244.38 "/>
<polygon class="st191" points="255.88,244.25 254.5,244.38 255.23,244.45 "/>
<polygon class="st192" points="255.72,249.34 255.88,249.29 255.88,251.81 "/>
<polygon class="st192" points="255.72,251.86 255.88,254.33 255.88,251.81 "/>
<polygon class="st193" points="255.55,249.39 255.72,251.86 255.72,249.34 "/>
<polygon class="st194" points="255.72,249.34 255.72,251.86 255.88,251.81 "/>
<polygon class="st192" points="255.72,246.82 255.88,249.29 255.88,246.77 "/>
<polygon class="st192" points="255.72,244.3 255.88,244.25 255.88,246.77 "/>
<polygon class="st193" points="255.55,244.35 255.72,244.3 255.72,246.82 "/>
<polygon class="st194" points="255.72,246.82 255.72,244.3 255.88,246.77 "/>
<polygon class="st195" points="255.39,246.92 255.55,249.39 255.55,246.87 "/>
<polygon class="st195" points="255.39,244.4 255.55,244.35 255.55,246.87 "/>
<polygon class="st196" points="255.23,244.45 255.39,244.4 255.39,246.92 "/>
<polygon class="st197" points="255.39,246.92 255.39,244.4 255.55,246.87 "/>
<polygon class="st194" points="255.72,249.34 255.88,249.29 255.72,246.82 "/>
<polygon class="st198" points="255.55,246.87 255.55,244.35 255.72,246.82 "/>
<polygon class="st198" points="255.55,249.39 255.55,246.87 255.72,249.34 "/>
<polygon class="st193" points="255.72,249.34 255.55,246.87 255.72,246.82 "/>
<polygon class="st199" points="255.39,249.44 255.23,249.48 255.23,246.96 "/>
<polygon class="st199" points="255.39,246.92 255.23,244.45 255.23,246.96 "/>
<polygon class="st197" points="255.55,249.39 255.39,246.92 255.39,249.44 "/>
<polygon class="st196" points="255.39,249.44 255.39,246.92 255.23,246.96 "/>
<polygon class="st199" points="255.39,251.96 255.23,249.48 255.23,252 "/>
<polygon class="st199" points="255.39,254.48 255.23,254.52 255.23,252 "/>
<polygon class="st197" points="255.55,254.43 255.39,254.48 255.39,251.96 "/>
<polygon class="st196" points="255.39,251.96 255.39,254.48 255.23,252 "/>
<polygon class="st198" points="255.72,251.86 255.55,249.39 255.55,251.91 "/>
<polygon class="st198" points="255.72,254.38 255.55,254.43 255.55,251.91 "/>
<polygon class="st194" points="255.88,254.33 255.72,254.38 255.72,251.86 "/>
<polygon class="st193" points="255.72,251.86 255.72,254.38 255.55,251.91 "/>
<polygon class="st196" points="255.39,249.44 255.23,249.48 255.39,251.96 "/>
<polygon class="st195" points="255.55,251.91 255.55,254.43 255.39,251.96 "/>
<polygon class="st195" points="255.55,249.39 255.55,251.91 255.39,249.44 "/>
<polygon class="st197" points="255.39,249.44 255.55,251.91 255.39,251.96 "/>
<polygon class="st200" points="254.86,249.45 255.23,254.52 255.23,249.48 "/>
<polygon class="st200" points="254.86,244.41 255.23,244.45 255.23,249.48 "/>
<polygon class="st201" points="254.5,244.38 254.86,244.41 254.86,249.45 "/>
<polygon class="st202" points="254.86,249.45 254.86,244.41 255.23,249.48 "/>
<polygon class="st203" points="254.86,249.45 254.5,244.38 254.5,249.42 "/>
<polygon class="st203" points="254.86,254.49 254.5,254.46 254.5,249.42 "/>
<polygon class="st202" points="255.23,254.52 254.86,254.49 254.86,249.45 "/>
<polygon class="st201" points="254.86,249.45 254.86,254.49 254.5,249.42 "/>
<polygon class="st204" points="254.5,254.46 254.5,244.38 253.98,244.08 "/>
<polygon class="st204" points="253.98,244.08 253.98,254.16 254.5,254.46 "/>
<polygon class="st203" points="253.92,248.91 253.98,254.16 253.98,249.12 "/>
<polygon class="st203" points="253.92,243.87 253.98,244.08 253.98,249.12 "/>
<polygon class="st202" points="253.86,243.66 253.92,243.87 253.92,248.91 "/>
<polygon class="st201" points="253.92,248.91 253.92,243.87 253.98,249.12 "/>
<polygon class="st200" points="253.92,248.91 253.86,243.66 253.86,248.7 "/>
<polygon class="st200" points="253.92,253.95 253.86,253.74 253.86,248.7 "/>
<polygon class="st201" points="253.98,254.16 253.92,253.95 253.92,248.91 "/>
<polygon class="st202" points="253.92,248.91 253.92,253.95 253.86,248.7 "/>
<polygon class="st205" points="256.22,253.95 256.22,243.88 255.88,244.25 "/>
<polygon class="st205" points="255.88,244.25 255.88,254.33 256.22,253.95 "/>
<polygon class="st201" points="256.38,241.45 256.16,241.7 255.6,240.02 "/>
<polygon class="st206" points="255.71,239.9 255.6,240.02 255.32,239.18 "/>
<polygon class="st207" points="255.43,239.06 255.04,238.34 255.32,239.18 "/>
<polygon class="st208" points="255.82,239.77 255.43,239.06 255.71,239.9 "/>
<polygon class="st206" points="255.71,239.9 255.43,239.06 255.32,239.18 "/>
<polygon class="st202" points="256.49,241.32 256.38,241.45 256.1,240.61 "/>
<polygon class="st209" points="256.21,240.48 255.82,239.77 256.1,240.61 "/>
<polygon class="st210" points="256.61,241.2 256.21,240.48 256.49,241.32 "/>
<polygon class="st211" points="256.49,241.32 256.21,240.48 256.1,240.61 "/>
<polygon class="st201" points="256.38,241.45 255.82,239.77 255.6,240.02 "/>
<polygon class="st212" points="256.83,243.25 256.72,243.38 256.44,242.54 "/>
<polygon class="st213" points="256.55,242.41 256.16,241.7 256.44,242.54 "/>
<polygon class="st214" points="256.94,243.13 256.55,242.41 256.83,243.25 "/>
<polygon class="st212" points="256.83,243.25 256.55,242.41 256.44,242.54 "/>
<polygon class="st215" points="257.11,244.09 256.72,243.38 257,244.22 "/>
<polygon class="st216" points="257.39,244.93 257.28,245.06 257,244.22 "/>
<polygon class="st217" points="257.5,244.81 257.39,244.93 257.11,244.09 "/>
<polygon class="st216" points="257.11,244.09 257.39,244.93 257,244.22 "/>
<polygon class="st218" points="257.33,243.84 256.94,243.13 257.22,243.97 "/>
<polygon class="st219" points="257.61,244.68 257.5,244.81 257.22,243.97 "/>
<polygon class="st220" points="257.72,244.56 257.61,244.68 257.33,243.84 "/>
<polygon class="st219" points="257.33,243.84 257.61,244.68 257.22,243.97 "/>
<polygon class="st215" points="256.83,243.25 256.72,243.38 257.11,244.09 "/>
<polygon class="st221" points="257.22,243.97 257.5,244.81 257.11,244.09 "/>
<polygon class="st199" points="256.94,243.13 257.22,243.97 256.83,243.25 "/>
<polygon class="st222" points="256.83,243.25 257.22,243.97 257.11,244.09 "/>
<polygon class="st217" points="257.28,242.75 257.17,242.88 256.89,242.04 "/>
<polygon class="st216" points="257,241.91 256.61,241.2 256.89,242.04 "/>
<polygon class="st223" points="257.39,242.63 257,241.91 257.28,242.75 "/>
<polygon class="st217" points="257.28,242.75 257,241.91 256.89,242.04 "/>
<polygon class="st224" points="257.95,244.31 257.72,244.56 257.17,242.88 "/>
<polygon class="st225" points="257.78,243.34 257.39,242.63 257.67,243.47 "/>
<polygon class="st226" points="258.06,244.18 257.95,244.31 257.67,243.47 "/>
<polygon class="st227" points="258.17,244.06 258.06,244.18 257.78,243.34 "/>
<polygon class="st226" points="257.78,243.34 258.06,244.18 257.67,243.47 "/>
<polygon class="st228" points="257.39,242.63 257.95,244.31 257.17,242.88 "/>
<polygon class="st214" points="256.66,242.29 256.94,243.13 256.55,242.41 "/>
<polygon class="st229" points="256.27,241.58 256.16,241.7 256.55,242.41 "/>
<polygon class="st230" points="256.38,241.45 256.27,241.58 256.66,242.29 "/>
<polygon class="st230" points="256.66,242.29 256.27,241.58 256.55,242.41 "/>
<polygon class="st218" points="257.05,243 256.94,243.13 257.33,243.84 "/>
<polygon class="st231" points="257.44,243.72 257.72,244.56 257.33,243.84 "/>
<polygon class="st232" points="257.17,242.88 257.44,243.72 257.05,243 "/>
<polygon class="st197" points="257.05,243 257.44,243.72 257.33,243.84 "/>
<polygon class="st200" points="256.49,241.32 256.38,241.45 256.77,242.16 "/>
<polygon class="st196" points="256.89,242.04 257.17,242.88 256.77,242.16 "/>
<polygon class="st233" points="256.61,241.2 256.89,242.04 256.49,241.32 "/>
<polygon class="st233" points="256.49,241.32 256.89,242.04 256.77,242.16 "/>
<polygon class="st234" points="256.66,242.29 256.94,243.13 257.05,243 "/>
<polygon class="st196" points="256.77,242.16 257.17,242.88 257.05,243 "/>
<polygon class="st235" points="256.38,241.45 256.77,242.16 256.66,242.29 "/>
<polygon class="st234" points="256.66,242.29 256.77,242.16 257.05,243 "/>
<polygon class="st236" points="256.18,240.35 255.82,239.77 256.21,240.48 "/>
<polygon class="st235" points="256.57,241.06 256.61,241.2 256.21,240.48 "/>
<polygon class="st235" points="256.53,240.92 256.57,241.06 256.18,240.35 "/>
<polygon class="st212" points="256.18,240.35 256.57,241.06 256.21,240.48 "/>
<polygon class="st203" points="255.78,239.63 255.82,239.77 255.43,239.06 "/>
<polygon class="st237" points="255.39,238.92 255.04,238.34 255.43,239.06 "/>
<polygon class="st203" points="255.75,239.49 255.39,238.92 255.78,239.63 "/>
<polygon class="st238" points="255.78,239.63 255.39,238.92 255.43,239.06 "/>
<polygon class="st235" points="256.49,240.78 256.53,240.92 256.14,240.21 "/>
<polygon class="st236" points="256.1,240.07 255.75,239.49 256.14,240.21 "/>
<polygon class="st235" points="256.45,240.64 256.1,240.07 256.49,240.78 "/>
<polygon class="st212" points="256.49,240.78 256.1,240.07 256.14,240.21 "/>
<polygon class="st239" points="256.18,240.35 255.82,239.77 255.78,239.63 "/>
<polygon class="st239" points="256.14,240.21 255.75,239.49 255.78,239.63 "/>
<polygon class="st212" points="256.53,240.92 256.14,240.21 256.18,240.35 "/>
<polygon class="st236" points="256.18,240.35 256.14,240.21 255.78,239.63 "/>
<polygon class="st195" points="257.35,242.49 257.39,242.63 257,241.91 "/>
<polygon class="st196" points="256.96,241.77 256.61,241.2 257,241.91 "/>
<polygon class="st195" points="257.31,242.35 256.96,241.77 257.35,242.49 "/>
<polygon class="st197" points="257.35,242.49 256.96,241.77 257,241.91 "/>
<polygon class="st193" points="257.74,243.2 257.39,242.63 257.78,243.34 "/>
<polygon class="st192" points="258.13,243.92 258.17,244.06 257.78,243.34 "/>
<polygon class="st192" points="258.09,243.78 258.13,243.92 257.74,243.2 "/>
<polygon class="st194" points="257.74,243.2 258.13,243.92 257.78,243.34 "/>
<polygon class="st193" points="257.66,242.92 257.31,242.35 257.7,243.06 "/>
<polygon class="st192" points="258.06,243.64 258.09,243.78 257.7,243.06 "/>
<polygon class="st192" points="258.02,243.5 258.06,243.64 257.66,242.92 "/>
<polygon class="st194" points="257.66,242.92 258.06,243.64 257.7,243.06 "/>
<polygon class="st198" points="257.35,242.49 257.39,242.63 257.74,243.2 "/>
<polygon class="st194" points="257.7,243.06 258.09,243.78 257.74,243.2 "/>
<polygon class="st198" points="257.31,242.35 257.7,243.06 257.35,242.49 "/>
<polygon class="st193" points="257.35,242.49 257.7,243.06 257.74,243.2 "/>
<polygon class="st195" points="257.2,241.93 257.23,242.07 256.84,241.36 "/>
<polygon class="st196" points="256.8,241.22 256.45,240.64 256.84,241.36 "/>
<polygon class="st195" points="257.16,241.79 256.8,241.22 257.2,241.93 "/>
<polygon class="st197" points="257.2,241.93 256.8,241.22 256.84,241.36 "/>
<polygon class="st193" points="257.59,242.65 257.23,242.07 257.63,242.78 "/>
<polygon class="st192" points="257.98,243.36 258.02,243.5 257.63,242.78 "/>
<polygon class="st192" points="257.94,243.22 257.98,243.36 257.59,242.65 "/>
<polygon class="st194" points="257.59,242.65 257.98,243.36 257.63,242.78 "/>
<polygon class="st193" points="257.51,242.37 257.16,241.79 257.55,242.51 "/>
<polygon class="st192" points="257.9,243.08 257.94,243.22 257.55,242.51 "/>
<polygon class="st192" points="257.86,242.94 257.9,243.08 257.51,242.37 "/>
<polygon class="st194" points="257.51,242.37 257.9,243.08 257.55,242.51 "/>
<polygon class="st198" points="257.2,241.93 257.23,242.07 257.59,242.65 "/>
<polygon class="st194" points="257.55,242.51 257.94,243.22 257.59,242.65 "/>
<polygon class="st198" points="257.16,241.79 257.55,242.51 257.2,241.93 "/>
<polygon class="st193" points="257.2,241.93 257.55,242.51 257.59,242.65 "/>
<polygon class="st197" points="256.92,241.63 257.31,242.35 256.96,241.77 "/>
<polygon class="st199" points="256.57,241.06 256.61,241.2 256.96,241.77 "/>
<polygon class="st199" points="256.53,240.92 256.57,241.06 256.92,241.63 "/>
<polygon class="st196" points="256.92,241.63 256.57,241.06 256.96,241.77 "/>
<polygon class="st198" points="257.27,242.21 257.31,242.35 257.66,242.92 "/>
<polygon class="st194" points="257.63,242.78 258.02,243.5 257.66,242.92 "/>
<polygon class="st198" points="257.23,242.07 257.63,242.78 257.27,242.21 "/>
<polygon class="st193" points="257.27,242.21 257.63,242.78 257.66,242.92 "/>
<polygon class="st199" points="256.49,240.78 256.53,240.92 256.88,241.5 "/>
<polygon class="st197" points="256.84,241.36 257.23,242.07 256.88,241.5 "/>
<polygon class="st199" points="256.45,240.64 256.84,241.36 256.49,240.78 "/>
<polygon class="st196" points="256.49,240.78 256.84,241.36 256.88,241.5 "/>
<polygon class="st195" points="256.92,241.63 257.31,242.35 257.27,242.21 "/>
<polygon class="st195" points="256.88,241.5 257.23,242.07 257.27,242.21 "/>
<polygon class="st196" points="256.53,240.92 256.88,241.5 256.92,241.63 "/>
<polygon class="st197" points="256.92,241.63 256.88,241.5 257.27,242.21 "/>
<polygon class="st240" points="253.63,241.47 255.04,238.34 253.47,240.91 "/>
<polygon class="st241" points="252.06,244.04 251.91,243.48 253.47,240.91 "/>
<polygon class="st242" points="252.22,244.6 252.06,244.04 253.63,241.47 "/>
<polygon class="st240" points="253.63,241.47 252.06,244.04 253.47,240.91 "/>
<polygon class="st243" points="253.6,245.4 252.22,244.6 255.04,238.34 "/>
<polygon class="st240" points="255.29,241.96 255.04,238.34 254.32,241.87 "/>
<polygon class="st244" points="254.57,245.48 253.6,245.4 254.32,241.87 "/>
<polygon class="st241" points="255.53,245.57 254.57,245.48 255.29,241.96 "/>
<polygon class="st245" points="255.29,241.96 254.57,245.48 254.32,241.87 "/>
<polygon class="st237" points="255.72,241.83 255.29,241.96 255.16,240.15 "/>
<polygon class="st246" points="255.6,240.02 255.04,238.34 255.16,240.15 "/>
<polygon class="st203" points="256.16,241.7 255.6,240.02 255.72,241.83 "/>
<polygon class="st247" points="255.72,241.83 255.6,240.02 255.16,240.15 "/>
<polygon class="st247" points="255.85,243.64 255.29,241.96 255.41,243.77 "/>
<polygon class="st248" points="255.97,245.45 255.53,245.57 255.41,243.77 "/>
<polygon class="st249" points="256.41,245.32 255.97,245.45 255.85,243.64 "/>
<polygon class="st250" points="255.85,243.64 255.97,245.45 255.41,243.77 "/>
<polygon class="st229" points="256.72,243.38 256.16,241.7 256.28,243.51 "/>
<polygon class="st211" points="256.84,245.19 256.41,245.32 256.28,243.51 "/>
<polygon class="st215" points="257.28,245.06 256.84,245.19 256.72,243.38 "/>
<polygon class="st230" points="256.72,243.38 256.84,245.19 256.28,243.51 "/>
<polygon class="st248" points="255.72,241.83 255.29,241.96 255.85,243.64 "/>
<polygon class="st251" points="256.28,243.51 256.41,245.32 255.85,243.64 "/>
<polygon class="st249" points="256.16,241.7 256.28,243.51 255.72,241.83 "/>
<polygon class="st252" points="255.72,241.83 256.28,243.51 255.85,243.64 "/>
<polygon class="st253" points="247.14,259.37 246.98,258.71 246.56,258.11 "/>
<polygon class="st253" points="247.14,259.37 246.56,258.11 246.05,257.81 "/>
<polygon class="st253" points="247.14,259.37 246.05,257.81 245.62,257.92 "/>
<polygon class="st253" points="247.14,259.37 245.62,257.92 245.46,258.4 "/>
<polygon class="st253" points="247.14,259.37 245.46,258.4 245.62,259.06 "/>
<polygon class="st253" points="247.14,259.37 245.62,259.06 246.05,259.66 "/>
<polygon class="st253" points="247.14,259.37 246.05,259.66 246.56,259.96 "/>
<polygon class="st253" points="247.14,259.37 246.56,259.96 246.98,259.85 "/>
<polygon class="st254" points="255.88,254.33 247.14,259.37 246.98,259.85 "/>
<polygon class="st254" points="246.98,259.85 255.72,254.81 255.88,254.33 "/>
<polygon class="st255" points="250.2,255.35 254.36,252.88 249.99,255.4 "/>
<polygon class="st255" points="245.83,257.87 245.62,257.92 249.99,255.4 "/>
<polygon class="st256" points="246.05,257.81 245.83,257.87 250.2,255.35 "/>
<polygon class="st257" points="250.2,255.35 245.83,257.87 249.99,255.4 "/>
<polygon class="st258" points="250.2,255.35 246.05,257.81 250.41,255.3 "/>
<polygon class="st258" points="254.57,252.83 254.78,252.78 250.41,255.3 "/>
<polygon class="st257" points="254.36,252.88 254.57,252.83 250.2,255.35 "/>
<polygon class="st256" points="250.2,255.35 254.57,252.83 250.41,255.3 "/>
<polygon class="st259" points="254.78,252.78 246.05,257.81 246.56,258.11 "/>
<polygon class="st259" points="246.56,258.11 255.3,253.07 254.78,252.78 "/>
<polygon class="st258" points="251.14,255.89 255.3,253.07 250.93,255.59 "/>
<polygon class="st258" points="246.77,258.41 246.56,258.11 250.93,255.59 "/>
<polygon class="st257" points="246.98,258.71 246.77,258.41 251.14,255.89 "/>
<polygon class="st256" points="251.14,255.89 246.77,258.41 250.93,255.59 "/>
<polygon class="st255" points="251.14,255.89 246.98,258.71 251.35,256.19 "/>
<polygon class="st255" points="255.51,253.37 255.72,253.67 251.35,256.19 "/>
<polygon class="st256" points="255.3,253.07 255.51,253.37 251.14,255.89 "/>
<polygon class="st257" points="251.14,255.89 255.51,253.37 251.35,256.19 "/>
<polygon class="st260" points="251.39,256.35 251.35,256.19 253.53,254.93 "/>
<polygon class="st260" points="253.57,255.09 255.72,253.67 253.53,254.93 "/>
<polygon class="st261" points="251.43,256.52 253.57,255.09 251.39,256.35 "/>
<polygon class="st262" points="251.39,256.35 253.57,255.09 253.53,254.93 "/>
<polygon class="st260" points="249.21,257.61 251.35,256.19 249.17,257.45 "/>
<polygon class="st260" points="247.02,258.87 246.98,258.71 249.17,257.45 "/>
<polygon class="st261" points="247.06,259.04 247.02,258.87 249.21,257.61 "/>
<polygon class="st262" points="249.21,257.61 247.02,258.87 249.17,257.45 "/>
<polygon class="st263" points="249.28,257.95 251.43,256.52 249.25,257.78 "/>
<polygon class="st263" points="247.1,259.2 247.06,259.04 249.25,257.78 "/>
<polygon class="st264" points="247.14,259.37 247.1,259.2 249.28,257.95 "/>
<polygon class="st265" points="249.28,257.95 247.1,259.2 249.25,257.78 "/>
<polygon class="st262" points="251.39,256.35 251.35,256.19 249.21,257.61 "/>
<polygon class="st266" points="249.25,257.78 247.06,259.04 249.21,257.61 "/>
<polygon class="st266" points="251.43,256.52 249.25,257.78 251.39,256.35 "/>
<polygon class="st261" points="251.39,256.35 249.25,257.78 249.21,257.61 "/>
<polygon class="st267" points="251.47,256.69 251.51,256.85 249.33,258.11 "/>
<polygon class="st267" points="249.28,257.95 247.14,259.37 249.33,258.11 "/>
<polygon class="st265" points="251.43,256.52 249.28,257.95 251.47,256.69 "/>
<polygon class="st264" points="251.47,256.69 249.28,257.95 249.33,258.11 "/>
<polygon class="st267" points="253.65,255.43 251.51,256.85 253.7,255.59 "/>
<polygon class="st267" points="255.84,254.17 255.88,254.33 253.7,255.59 "/>
<polygon class="st265" points="255.8,254 255.84,254.17 253.65,255.43 "/>
<polygon class="st264" points="253.65,255.43 255.84,254.17 253.7,255.59 "/>
<polygon class="st266" points="253.57,255.09 251.43,256.52 253.61,255.26 "/>
<polygon class="st266" points="255.76,253.84 255.8,254 253.61,255.26 "/>
<polygon class="st262" points="255.72,253.67 255.76,253.84 253.57,255.09 "/>
<polygon class="st261" points="253.57,255.09 255.76,253.84 253.61,255.26 "/>
<polygon class="st264" points="251.47,256.69 251.51,256.85 253.65,255.43 "/>
<polygon class="st263" points="253.61,255.26 255.8,254 253.65,255.43 "/>
<polygon class="st263" points="251.43,256.52 253.61,255.26 251.47,256.69 "/>
<polygon class="st265" points="251.47,256.69 253.61,255.26 253.65,255.43 "/>
<polygon class="st268" points="244.96,260.45 245.07,260.89 243.33,261.24 "/>
<polygon class="st269" points="243.23,260.8 241.6,261.6 243.33,261.24 "/>
<polygon class="st269" points="244.86,260 243.23,260.8 244.96,260.45 "/>
<polygon class="st270" points="244.96,260.45 243.23,260.8 243.33,261.24 "/>
<polygon class="st271" points="246.7,260.09 245.07,260.89 246.81,260.53 "/>
<polygon class="st262" points="248.44,259.73 248.54,260.18 246.81,260.53 "/>
<polygon class="st272" points="248.33,259.29 248.44,259.73 246.7,260.09 "/>
<polygon class="st273" points="246.7,260.09 248.44,259.73 246.81,260.53 "/>
<polygon class="st274" points="246.49,259.21 244.86,260 246.59,259.65 "/>
<polygon class="st275" points="248.22,258.85 248.33,259.29 246.59,259.65 "/>
<polygon class="st276" points="248.12,258.41 248.22,258.85 246.49,259.21 "/>
<polygon class="st277" points="246.49,259.21 248.22,258.85 246.59,259.65 "/>
<polygon class="st278" points="244.96,260.45 245.07,260.89 246.7,260.09 "/>
<polygon class="st278" points="246.59,259.65 248.33,259.29 246.7,260.09 "/>
<polygon class="st277" points="244.86,260 246.59,259.65 244.96,260.45 "/>
<polygon class="st279" points="244.96,260.45 246.59,259.65 246.7,260.09 "/>
<polygon class="st280" points="244.58,259.61 244.86,260 243.23,260.8 "/>
<polygon class="st280" points="242.95,260.4 241.6,261.6 243.23,260.8 "/>
<polygon class="st281" points="244.3,259.21 242.95,260.4 244.58,259.61 "/>
<polygon class="st282" points="244.58,259.61 242.95,260.4 243.23,260.8 "/>
<polygon class="st283" points="246.21,258.81 244.86,260 246.49,259.21 "/>
<polygon class="st283" points="247.84,258.01 248.12,258.41 246.49,259.21 "/>
<polygon class="st284" points="247.56,257.62 247.84,258.01 246.21,258.81 "/>
<polygon class="st285" points="246.21,258.81 247.84,258.01 246.49,259.21 "/>
<polygon class="st286" points="245.65,258.02 244.3,259.21 245.93,258.41 "/>
<polygon class="st286" points="247.28,257.22 247.56,257.62 245.93,258.41 "/>
<polygon class="st287" points="247,256.82 247.28,257.22 245.65,258.02 "/>
<polygon class="st288" points="245.65,258.02 247.28,257.22 245.93,258.41 "/>
<polygon class="st285" points="244.58,259.61 244.86,260 246.21,258.81 "/>
<polygon class="st289" points="245.93,258.41 247.56,257.62 246.21,258.81 "/>
<polygon class="st289" points="244.3,259.21 245.93,258.41 244.58,259.61 "/>
<polygon class="st284" points="244.58,259.61 245.93,258.41 246.21,258.81 "/>
<polygon class="st290" points="243.95,259.01 244.3,259.21 242.95,260.4 "/>
<polygon class="st283" points="242.6,260.21 241.6,261.6 242.95,260.4 "/>
<polygon class="st291" points="243.6,258.81 242.6,260.21 243.95,259.01 "/>
<polygon class="st292" points="243.95,259.01 242.6,260.21 242.95,260.4 "/>
<polygon class="st293" points="245.3,257.82 244.3,259.21 245.65,258.02 "/>
<polygon class="st294" points="246.65,256.63 247,256.82 245.65,258.02 "/>
<polygon class="st295" points="246.3,256.43 246.65,256.63 245.3,257.82 "/>
<polygon class="st296" points="245.3,257.82 246.65,256.63 245.65,258.02 "/>
<polygon class="st297" points="244.61,257.42 243.6,258.81 244.95,257.62 "/>
<polygon class="st298" points="245.96,256.23 246.3,256.43 244.95,257.62 "/>
<polygon class="st299" points="245.61,256.03 245.96,256.23 244.61,257.42 "/>
<polygon class="st300" points="244.61,257.42 245.96,256.23 244.95,257.62 "/>
<polygon class="st301" points="243.95,259.01 244.3,259.21 245.3,257.82 "/>
<polygon class="st302" points="244.95,257.62 246.3,256.43 245.3,257.82 "/>
<polygon class="st303" points="243.6,258.81 244.95,257.62 243.95,259.01 "/>
<polygon class="st304" points="243.95,259.01 244.95,257.62 245.3,257.82 "/>
<polygon class="st305" points="243.04,258.96 241.6,261.6 243.6,258.81 "/>
<polygon class="st306" points="245.05,256.17 245.61,256.03 243.6,258.81 "/>
<polygon class="st307" points="244.49,256.32 245.05,256.17 243.04,258.96 "/>
<polygon class="st308" points="243.04,258.96 245.05,256.17 243.6,258.81 "/>
<polygon class="st309" points="244.58,261.6 244.3,261.67 242.95,261.63 "/>
<polygon class="st279" points="243.23,261.56 241.6,261.6 242.95,261.63 "/>
<polygon class="st309" points="244.86,261.52 243.23,261.56 244.58,261.6 "/>
<polygon class="st271" points="244.58,261.6 243.23,261.56 242.95,261.63 "/>
<polygon class="st310" points="245.93,261.63 244.3,261.67 245.65,261.71 "/>
<polygon class="st311" points="247.28,261.67 247,261.74 245.65,261.71 "/>
<polygon class="st311" points="247.56,261.6 247.28,261.67 245.93,261.63 "/>
<polygon class="st312" points="245.93,261.63 247.28,261.67 245.65,261.71 "/>
<polygon class="st310" points="246.49,261.49 244.86,261.52 246.21,261.56 "/>
<polygon class="st311" points="247.84,261.52 247.56,261.6 246.21,261.56 "/>
<polygon class="st311" points="248.12,261.45 247.84,261.52 246.49,261.49 "/>
<polygon class="st312" points="246.49,261.49 247.84,261.52 246.21,261.56 "/>
<polygon class="st313" points="244.58,261.6 244.3,261.67 245.93,261.63 "/>
<polygon class="st312" points="246.21,261.56 247.56,261.6 245.93,261.63 "/>
<polygon class="st313" points="244.86,261.52 246.21,261.56 244.58,261.6 "/>
<polygon class="st310" points="244.58,261.6 246.21,261.56 245.93,261.63 "/>
<polygon class="st273" points="244.96,261.21 244.86,261.52 243.23,261.56 "/>
<polygon class="st314" points="243.33,261.24 241.6,261.6 243.23,261.56 "/>
<polygon class="st255" points="245.07,260.89 243.33,261.24 244.96,261.21 "/>
<polygon class="st315" points="244.96,261.21 243.33,261.24 243.23,261.56 "/>
<polygon class="st316" points="246.59,261.17 244.86,261.52 246.49,261.49 "/>
<polygon class="st317" points="248.22,261.13 248.12,261.45 246.49,261.49 "/>
<polygon class="st318" points="248.33,260.81 248.22,261.13 246.59,261.17 "/>
<polygon class="st319" points="246.59,261.17 248.22,261.13 246.49,261.49 "/>
<polygon class="st309" points="246.81,260.53 245.07,260.89 246.7,260.85 "/>
<polygon class="st310" points="248.44,260.49 248.33,260.81 246.7,260.85 "/>
<polygon class="st320" points="248.54,260.18 248.44,260.49 246.81,260.53 "/>
<polygon class="st320" points="246.81,260.53 248.44,260.49 246.7,260.85 "/>
<polygon class="st321" points="244.96,261.21 244.86,261.52 246.59,261.17 "/>
<polygon class="st322" points="246.7,260.85 248.33,260.81 246.59,261.17 "/>
<polygon class="st260" points="245.07,260.89 246.7,260.85 244.96,261.21 "/>
<polygon class="st321" points="244.96,261.21 246.7,260.85 246.59,261.17 "/>
<text transform="matrix(1 0 0 1 271.7197 269.4535)" class="st323 st324">X</text>
<text transform="matrix(1 0 0 1 250.7197 232.7113)" class="st323 st324">Y</text>
<text transform="matrix(1 0 0 1 229.7197 269.4535)" class="st323 st324">Z</text>
<g>
	<path class="st0" d="M237.45,90.1l-0.72-3.22 M229.47,91.02l7.26-4.14l-2.38-2.14 M229.47,91.02l4.88-6.28l-2.61,0.21
		 M229.47,91.02l2.27-6.07l-1.32,2.4 M229.47,91.02l0.95-3.67l0.73,3.18 M229.47,91.02l1.68-0.49l2.33,2.12 M229.47,91.02l4.01,1.63
		l2.61-0.17 M229.47,91.02l6.62,1.46l1.35-2.39L229.47,91.02 M259.38,98.78l-0.68-3.22 M251.43,99.75l7.27-4.18l-2.44-2.17
		 M251.43,99.75l4.83-6.35l-2.75,0.16 M251.43,99.75l2.08-6.19l-1.45,2.37l0.68,3.18 M251.43,99.75l1.32-0.64l2.4,2.15
		 M251.43,99.75l3.72,1.51l2.74-0.12 M251.43,99.75l6.46,1.39l1.48-2.35L251.43,99.75 M256.12,122.41l-0.68-3.15 M248.22,123.45
		l7.22-4.19l-2.42-2.2 M248.22,123.45l4.81-6.39l-2.71,0.03 M248.22,123.45l2.09-6.36l-1.41,2.23 M248.22,123.45l0.68-4.13l0.68,3.1
		 M248.22,123.45l1.36-1.03l2.38,2.19 M248.22,123.45l3.74,1.16l2.7,0.01 M248.22,123.45l6.44,1.17l1.46-2.21L248.22,123.45
		 M253.09,144.52l-0.68-3.08 M245.21,145.64l7.2-4.2l-2.4-2.25 M245.21,145.64l4.8-6.45l-2.68-0.09 M245.21,145.64l2.11-6.54
		l-1.39,2.1 M245.21,145.64l0.72-4.44l0.69,3.04 M245.21,145.64l1.41-1.4l2.36,2.23 M245.21,145.64l3.77,0.84l2.68,0.12
		 M245.21,145.64l6.45,0.96l1.43-2.08L245.21,145.64 M250.27,165.25l-0.69-3.03 M242.4,166.44l7.19-4.22l-2.39-2.3L242.4,166.44
		l4.8-6.52l-2.67-0.2 M242.4,166.44l2.14-6.71l-1.38,1.98 M242.4,166.44l0.76-4.73l0.69,2.99 M242.4,166.44l1.45-1.74l2.35,2.27
		l2.66,0.24 M242.4,166.44l6.46,0.77l1.41-1.96L242.4,166.44 M247.63,184.73l-0.69-2.98 M239.74,185.99l7.2-4.25l-2.39-2.34
		 M239.74,185.99l4.81-6.58l-2.65-0.3 M239.74,185.99l2.16-6.89l-1.36,1.88 M239.74,185.99l0.8-5.01l0.7,2.95 M239.74,185.99
		l1.5-2.06l2.34,2.31l2.65,0.35 M239.74,185.99l6.49,0.6l1.4-1.86L239.74,185.99 M56.62,74.47l1.91-1.36 M52.97,65.96l5.56,7.15
		l-0.79-1.35 M52.97,65.96l4.77,5.8l-2.99-0.55 M52.97,65.96l1.78,5.24l-3.46,0.55 M52.97,65.96l-1.68,5.8l-1.94,1.35 M52.97,65.96
		l-3.62,7.15l0.74,1.36 M52.97,65.96l-2.87,8.51l3.02,0.57 M52.97,65.96l0.15,9.08l3.5-0.57L52.97,65.96 M73.98,84.44l1.79-1.41
		 M70.43,76.05l5.34,6.98l-0.88-1.39 M70.43,76.05l4.46,5.59l-3-0.57 M70.43,76.05l1.46,5.02l-3.39,0.57l-1.82,1.39 M70.43,76.05
		l-3.75,6.98l0.84,1.41 M70.43,76.05l-2.91,8.39l3.03,0.59 M70.43,76.05l0.12,8.98l3.43-0.59L70.43,76.05 M92.6,95.1l1.67-1.46
		 M89.15,86.83l5.12,6.82l-0.97-1.44 M89.15,86.83l4.14,5.38l-3.02-0.59 M89.15,86.83l1.12,4.79l-3.32,0.59 M89.15,86.83l-2.19,5.38
		l-1.7,1.44 M89.15,86.83l-3.89,6.82l0.94,1.46 M89.15,86.83l-2.96,8.28l3.05,0.61 M89.15,86.83l0.09,8.89l3.36-0.61L89.15,86.83
		 M112.63,106.52l1.54-1.51l-4.89-6.67 M114.17,105.01l-1.08-1.49 M109.28,98.34l3.82,5.18l-3.04-0.61 M109.28,98.34l0.77,4.56
		l-3.25,0.61 M109.28,98.34l-2.48,5.18l-1.58,1.49 M109.28,98.34l-4.05,6.67l1.04,1.51 M109.28,98.34l-3.02,8.18l3.08,0.63
		 M109.28,98.34l0.06,8.81l3.29-0.63L109.28,98.34 M134.25,118.78l1.42-1.57 M130.99,110.68l4.67,6.53l-1.19-1.56 M130.99,110.68
		l3.48,4.97l-3.08-0.64l-3.18,0.64 M130.99,110.68l-2.78,4.97l-1.46,1.56 M130.99,110.68l-4.24,6.53l1.16,1.57 M130.99,110.68
		l-3.08,8.1l3.11,0.66 M130.99,110.68l0.03,8.75l3.22-0.66L130.99,110.68 M157.65,131.98l1.29-1.64 M154.49,123.95l4.44,6.39
		l-1.32-1.62 M154.49,123.95l3.12,4.76l-3.12-0.67l-3.13,0.67 M154.49,123.95l-3.13,4.76l-1.32,1.62 M154.49,123.95l-4.45,6.39
		l1.28,1.64 M154.49,123.95l-3.16,8.03l3.16,0.69l3.15-0.69L154.49,123.95 M258.88,74.47l0.74-1.36 M256.01,65.96l3.62,7.15
		l-1.94-1.35 M256.01,65.96l1.68,5.8l-3.46-0.55 M256.01,65.96l-1.78,5.24l-2.99,0.55 M256.01,65.96l-4.76,5.8 M256.01,65.96
		l-5.56,7.15l1.91,1.36 M256.01,65.96l-3.65,8.51l3.5,0.57 M256.01,65.96l-0.15,9.08l3.02-0.57L256.01,65.96 M241.46,84.44
		l0.84-1.41 M238.55,76.05l3.75,6.98l-1.82-1.39l-3.39-0.57 M238.55,76.05l-1.46,5.02l-3,0.57 M238.55,76.05l-4.46,5.59l-0.88,1.39
		 M238.55,76.05l-5.34,6.98l1.79,1.41 M238.55,76.05L235,84.44l3.43,0.59 M238.55,76.05l-0.12,8.98l3.03-0.59L238.55,76.05
		 M222.79,95.1l0.94-1.46 M219.83,86.83l3.89,6.82l-1.7-1.44 M219.83,86.83l2.19,5.38l-3.32-0.59 M219.83,86.83l-1.12,4.79
		l-3.02,0.59 M219.83,86.83l-4.14,5.38l-0.97,1.44 M219.83,86.83l-5.12,6.82l1.67,1.46 M219.83,86.83l-3.45,8.28l3.36,0.61
		 M219.83,86.83l-0.09,8.89l3.05-0.61L219.83,86.83 M202.72,106.52l1.04-1.51 M199.7,98.34l4.05,6.67l-1.58-1.49 M199.7,98.34
		l2.48,5.18l-3.25-0.61 M199.7,98.34l-0.77,4.56l-3.04,0.61 M199.7,98.34l-4.9,6.67l1.55,1.51 M199.7,98.34l-3.35,8.18l3.29,0.63
		 M199.7,98.34l-0.06,8.81l3.08-0.63L199.7,98.34 M181.07,118.78l1.16-1.57 M177.99,110.68l4.24,6.53l-1.45-1.56 M177.99,110.68
		l2.79,4.97l-3.19-0.64l-3.08,0.64 M177.99,110.68l-3.48,4.97 M177.99,110.68l-4.67,6.53l1.42,1.57 M177.99,110.68l-3.26,8.1
		l3.22,0.66 M177.99,110.68l-0.03,8.75l3.11-0.66L177.99,110.68 M157.73,34.47l1.32-1.13 M154.49,25.87l4.55,7.47l-1.35-1.11
		 M154.49,25.87l3.2,6.36l-3.2-0.46l-3.2,0.46 M154.49,25.87l-3.2,6.36l-1.35,1.11 M154.49,25.87l-4.55,7.47l1.31,1.13
		 M154.49,25.87l-3.24,8.6l3.24,0.47l3.24-0.47L154.49,25.87 M175.5,41.6l1.21-1.16 M172.34,33.05l4.37,7.39l-1.45-1.15
		 M172.34,33.05l2.92,6.24l-3.23-0.48l-3.15,0.48 M172.34,33.05l-3.46,6.24l-1.25,1.15 M172.34,33.05l-4.71,7.39l1.42,1.16
		 M172.34,33.05l-3.29,8.55l3.27,0.49L172.34,33.05l-0.02,9.04l3.19-0.49L172.34,33.05 M194.38,49.13l1.1-1.21 M191.3,40.61
		l4.19,7.31l-1.56-1.19 M191.3,40.61l2.64,6.12l-3.28-0.49 M191.3,40.61l-0.64,5.63l-3.11,0.49 M191.3,40.61l-3.75,6.12l-1.14,1.19
		 M191.3,40.61l-4.89,7.31l1.52,1.21 M191.3,40.61l-3.37,8.52l3.31,0.5 M191.3,40.61l-0.05,9.02l3.14-0.5L191.3,40.61 M214.49,57.09
		l0.99-1.25 M211.47,48.59l4,7.25l-1.67-1.24 M211.47,48.59l2.34,6.01l-3.33-0.51 M211.47,48.59l-0.99,5.5l-3.06,0.51 M211.47,48.59
		l-4.05,6.01l-1.03,1.24 M211.47,48.59l-5.08,7.25l1.63,1.25 M211.47,48.59l-3.45,8.5l3.37,0.52 M211.47,48.59l-0.08,9.02l3.1-0.52
		L211.47,48.59 M235.94,65.51l0.87-1.3 M232.99,57.02l3.81,7.19l-1.79-1.29l-3.39-0.53 M232.99,57.02l-1.37,5.37l-3.02,0.53
		 M232.99,57.02l-4.39,5.9 M232.99,57.02l-5.3,7.19l1.76,1.3 M232.99,57.02l-3.54,8.49l3.42,0.55 M232.99,57.02l-0.12,9.04
		l3.06-0.55L232.99,57.02 M139.94,41.6l1.42-1.16 M136.64,33.05l4.71,7.39l-1.25-1.15 M136.64,33.05l3.46,6.24l-3.15-0.48
		 M136.64,33.05l0.31,5.76l-3.24,0.48 M136.64,33.05l-2.93,6.24l-1.45,1.15 M136.64,33.05l-4.37,7.39l1.21,1.16 M136.64,33.05
		l-3.16,8.55l3.19,0.49 M136.64,33.05l0.02,9.04l3.27-0.49L136.64,33.05 M121.05,49.13l1.52-1.21 M117.68,40.61l4.89,7.31
		l-1.14-1.19 M117.68,40.61l3.75,6.12l-3.11-0.49 M117.68,40.61l0.64,5.63l-3.28,0.49 M117.68,40.61l-2.64,6.12l-1.56,1.19
		 M117.68,40.61l-4.19,7.31l1.1,1.21 M117.68,40.61l-3.09,8.52l3.14,0.5 M117.68,40.61l0.05,9.02l3.31-0.5L117.68,40.61
		 M100.96,57.09l1.63-1.25 M97.51,48.59l5.08,7.25l-1.03-1.24 M97.51,48.59l4.05,6.01l-3.06-0.51 M97.51,48.59l0.99,5.5l-3.33,0.51
		 M97.51,48.59l-2.34,6.01l-1.67,1.24 M97.51,48.59l-4,7.25l0.99,1.25 M97.51,48.59l-3.02,8.5l3.1,0.52 M97.51,48.59l0.08,9.02
		l3.37-0.52L97.51,48.59 M79.53,65.51l1.76-1.3 M75.99,57.02l5.3,7.19l-0.91-1.29 M75.99,57.02l4.39,5.9l-3.03-0.53 M75.99,57.02
		l1.36,5.37l-3.39,0.53l-1.79,1.29 M75.99,57.02l-3.81,7.19l0.87,1.3L75.99,57.02l-2.94,8.49l3.06,0.55 M75.99,57.02l0.12,9.04
		l3.42-0.55L75.99,57.02 M57.55,99.75l-4.58-33.79 M74.19,109.09l-3.76-33.04 M92.05,119.12l-2.9-32.3 M111.27,129.92l-1.99-31.58
		 M132.02,141.57l-1.03-30.89 M154.49,154.19v-30.25 M251.43,99.75l4.58-33.79 M234.79,109.09l3.76-33.04 M216.93,119.12l2.9-32.3
		 M197.71,129.92l1.99-31.58"/>
	<path class="st0" d="M176.96,141.57l1.03-30.89 M154.49,61.23V25.87 M171.54,68l0.8-34.95 M189.65,75.2l1.65-34.59 M208.92,82.85
		l2.55-34.27 M229.47,91.02l3.52-34 M137.44,68l-0.8-34.95 M119.33,75.2l-1.64-34.59 M100.06,82.85l-2.55-34.27 M79.51,91.02
		l-3.52-34"/>
</g>
<line class="st325" x1="249.97" y1="99.18" x2="286.03" y2="114.42"/>
<g>
	<g>
		<line class="st326" x1="279.61" y1="114.96" x2="264.62" y2="212.19"/>
		<g>
			<path d="M280.06,111.98c-0.74,1.32-1.89,2.92-2.99,3.85l2.48-0.49l2.21,1.21C280.99,115.33,280.37,113.46,280.06,111.98z"/>
		</g>
		<g>
			<path d="M264.17,215.16c-0.3-1.48-0.92-3.35-1.7-4.58l2.21,1.21l2.48-0.49C266.05,212.24,264.9,213.84,264.17,215.16z"/>
		</g>
	</g>
</g>
<line class="st325" x1="236.96" y1="204.6" x2="270.28" y2="218.07"/>
<line class="st325" x1="249.97" y1="99.18" x2="286.03" y2="114.42"/>
<text transform="matrix(0.9848 0.1736 -0.1736 0.9848 275.3708 174.457)" class="st327 st328">Mesh Size</text>
</svg>
 Model.svg…]()


## File Structure

- **`one_element_generator.py`**: The main Abaqus Python script file responsible for generating 3D models with a single element.
- **`README.md`**: Project documentation providing detailed information on the script and instructions for use.
- **`examples/`**: Directory containing sample files demonstrating different configurations and use cases.

## Usage

1. **Install Abaqus**: Ensure that Abaqus is installed on your system and that the environment variables are properly configured.

2. **Clone the Repository**:

    ```bash
    git clone https://github.com/your-username/3d-one-element-generator.git
    cd 3d-one-element-generator
    ```

3. **Run the Script**:

    ```bash
    abaqus cae noGUI=one_element_generator.py
    ```

    Replace `one_element_generator.py` with the actual script filename.

## Configuration Parameters

In the `one_element_generator.py` file, users can customize the following parameters:

- `material_properties`: Define material properties such as elastic modulus, Poisson's ratio, etc.
- `geometry_parameters`: Set geometric parameters, including dimensions and shape.
- `boundary_conditions`: Specify boundary conditions, including constraints and loads.

Ensure that you have appropriately configured these parameters based on the specific requirements of your model before running the script.

## Examples

Explore the `examples/` directory to see sample files showcasing how to configure the script for different types of single-element models. Each example includes corresponding documentation.

## Important Notes

- Before running the script, carefully read the `README.md` file to ensure all prerequisites are met.
- For any issues or suggestions, feel free to raise an issue on GitHub.

## License

This project is licensed under the [MIT License](LICENSE).
