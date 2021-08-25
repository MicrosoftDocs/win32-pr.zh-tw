---
description: FONTSIGNATURE 和 LOCALESIGNATURE 結構中會使用 Unicode 子集位欄位 (USBs) 。
ms.assetid: f897dfc7-3e78-48dc-8d3d-6929e2f4ec4d
title: Unicode 子集位欄位
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06f0fa4791e62f397e62a99a78d41dbcdc67c55299a650b1bc78bea685205399
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119787988"
---
# <a name="unicode-subset-bitfields"></a>Unicode 子集位欄位

[**FONTSIGNATURE**](/windows/win32/api/wingdi/ns-wingdi-fontsignature)和 [**LOCALESIGNATURE**](/windows/win32/api/wingdi/ns-wingdi-localesignature)結構中會使用 Unicode 子集位欄位 (USBs) 。



<table>
<thead>
<tr class="header">
<th>bit</th>
<th>Unicode 子範圍</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>0</td>
<td>0000 - 007F</td>
<td>基本拉丁</td>
</tr>
<tr class="even">
<td>1</td>
<td>0080 - 00FF</td>
<td>拉丁文1補充</td>
</tr>
<tr class="odd">
<td>2</td>
<td>0100 - 017F</td>
<td>拉丁文擴充-A</td>
</tr>
<tr class="even">
<td>3</td>
<td>0180 - 024F</td>
<td>拉丁文擴充-B</td>
</tr>
<tr class="odd">
<td rowspan="3">4 $ {REMOVE} $<br />
</td>
<td>0250 - 02AF</td>
<td>IPA 延伸模組</td>
</tr>
<tr class="even">
<td>1D00 - 1D7F</td>
<td>拼音延伸模組</td>

</tr>
<tr class="odd">
<td>1D80 - 1DBF</td>
<td>注音擴充功能補充</td>

</tr>
<tr class="even">
<td rowspan="2">5 $ {REMOVE} $<br />
</td>
<td>02B0 - 02FF</td>
<td>間距修飾詞字母</td>
</tr>
<tr class="odd">
<td>A700 - A71F</td>
<td>修飾詞音調字母</td>

</tr>
<tr class="even">
<td rowspan="2">6 $ {REMOVE} $<br />
</td>
<td>0300 - 036F</td>
<td>結合變音符號標記</td>
</tr>
<tr class="odd">
<td>1DC0 - 1DFF</td>
<td>結合變音符號補充符號</td>

</tr>
<tr class="even">
<td>7</td>
<td>0370 - 03FF</td>
<td>希臘文和哥普特文</td>
</tr>
<tr class="odd">
<td>8</td>
<td>2C80 - 2CFF</td>
<td>科普特文</td>
</tr>
<tr class="even">
<td rowspan="4">9 $ {REMOVE} $<br />
</td>
<td>0400 - 04FF</td>
<td>古斯拉夫文</td>
</tr>
<tr class="odd">
<td>0500 - 052F</td>
<td>斯拉夫文增補</td>

</tr>
<tr class="even">
<td>2DE0 - 2DFF</td>
<td>斯拉夫文擴充-A</td>

</tr>
<tr class="odd">
<td>A640 - A69F</td>
<td>斯拉夫文擴充-B</td>

</tr>
<tr class="even">
<td>10</td>
<td>0530 - 058F</td>
<td>亞美尼亞文</td>
</tr>
<tr class="odd">
<td>11</td>
<td>0590 - 05FF</td>
<td>Hebrew</td>
</tr>
<tr class="even">
<td>12</td>
<td>A500-A63F</td>
<td>范文</td>
</tr>
<tr class="odd">
<td rowspan="2">13 $ {REMOVE} $<br />
</td>
<td>0600 - 06FF</td>
<td>阿拉伯文</td>
</tr>
<tr class="even">
<td>0750-077F</td>
<td>阿拉伯文增補</td>

</tr>
<tr class="odd">
<td>14</td>
<td>07C0 - 07FF</td>
<td>NKo</td>
</tr>
<tr class="even">
<td>15</td>
<td>0900 - 097F</td>
<td>梵文字母</td>
</tr>
<tr class="odd">
<td>16</td>
<td>0980 - 09FF</td>
<td>孟加拉文</td>
</tr>
<tr class="even">
<td>17</td>
<td>0A00 - 0A7F</td>
<td>古木基文</td>
</tr>
<tr class="odd">
<td>18</td>
<td>0A80 - 0AFF</td>
<td>古吉拉特文</td>
</tr>
<tr class="even">
<td>19</td>
<td>0B00 - 0B7F</td>
<td>歐迪亞文</td>
</tr>
<tr class="odd">
<td>20</td>
<td>0B80 - 0BFF</td>
<td>坦米爾文</td>
</tr>
<tr class="even">
<td>21</td>
<td>0C00 - 0C7F</td>
<td>泰盧固文</td>
</tr>
<tr class="odd">
<td>22</td>
<td>0C80 - 0CFF</td>
<td>坎那達文</td>
</tr>
<tr class="even">
<td>23</td>
<td>0D00 - 0D7F</td>
<td>馬來亞拉姆文</td>
</tr>
<tr class="odd">
<td>24</td>
<td>0E00 - 0E7F</td>
<td>泰文</td>
</tr>
<tr class="even">
<td>25</td>
<td>0E80 - 0EFF</td>
<td>寮文</td>
</tr>
<tr class="odd">
<td rowspan="2">26 $ {REMOVE} $<br />
</td>
<td>10A0 - 10FF</td>
<td>喬治亞文</td>
</tr>
<tr class="even">
<td>2D00 - 2D2F</td>
<td>格魯吉亞文補充</td>

</tr>
<tr class="odd">
<td>27</td>
<td>1B00 - 1B7F</td>
<td>峇里文</td>
</tr>
<tr class="even">
<td>28</td>
<td>1100 - 11FF</td>
<td>韓文拼音字母</td>
</tr>
<tr class="odd">
<td rowspan="3">29 $ {REMOVE} $<br />
</td>
<td>1E00 - 1EFF</td>
<td>其他拉丁文擴充</td>
</tr>
<tr class="even">
<td>2C60 - 2C7F</td>
<td>拉丁擴充-C</td>

</tr>
<tr class="odd">
<td>A720 - A7FF</td>
<td>拉丁文擴充-D</td>

</tr>
<tr class="even">
<td>30</td>
<td>1F00 - 1FFF</td>
<td>希臘文擴充</td>
</tr>
<tr class="odd">
<td rowspan="2">31 $ {REMOVE} $<br />
</td>
<td>2000 - 206F</td>
<td>一般標點符號</td>
</tr>
<tr class="even">
<td>2E00 - 2E7F</td>
<td>補充標點符號</td>

</tr>
<tr class="odd">
<td>32</td>
<td>2070 - 209F</td>
<td>上標和下標</td>
</tr>
<tr class="even">
<td>33</td>
<td>20A0 - 20CF</td>
<td>貨幣符號</td>
</tr>
<tr class="odd">
<td>34</td>
<td>20D0 - 20FF</td>
<td>合併符號的變音符號</td>
</tr>
<tr class="even">
<td>35</td>
<td>2100 - 214F</td>
<td>字母符號</td>
</tr>
<tr class="odd">
<td>36</td>
<td>2150 - 218F</td>
<td>數位形式</td>
</tr>
<tr class="even">
<td rowspan="4">37 $ {REMOVE} $<br />
</td>
<td>2190 - 21FF</td>
<td>箭頭</td>
</tr>
<tr class="odd">
<td>27F0 - 27FF</td>
<td>補充箭號-A</td>

</tr>
<tr class="even">
<td>2900 - 297F</td>
<td>補充箭號-B</td>

</tr>
<tr class="odd">
<td>2B00 - 2BFF</td>
<td>其他符號和箭號</td>

</tr>
<tr class="even">
<td rowspan="4">38 $ {REMOVE} $<br />
</td>
<td>2200 - 22FF</td>
<td>數學運算子</td>
</tr>
<tr class="odd">
<td>27C0 - 27EF</td>
<td>其他數學符號-A</td>

</tr>
<tr class="even">
<td>2980 - 29FF</td>
<td>其他數學符號-B</td>

</tr>
<tr class="odd">
<td>2A00 - 2AFF</td>
<td>補充的數學運算子</td>

</tr>
<tr class="even">
<td>39</td>
<td>2300 - 23FF</td>
<td>其他技術</td>
</tr>
<tr class="odd">
<td>40</td>
<td>2400 - 243F</td>
<td>控制圖片</td>
</tr>
<tr class="even">
<td>41</td>
<td>2440 - 245F</td>
<td>光學字元辨識</td>
</tr>
<tr class="odd">
<td>42</td>
<td>2460 - 24FF</td>
<td>包含英數位元</td>
</tr>
<tr class="even">
<td>43</td>
<td>2500 - 257F</td>
<td>盒繪圖</td>
</tr>
<tr class="odd">
<td>44</td>
<td>2580 - 259F</td>
<td>Block 元素</td>
</tr>
<tr class="even">
<td>45</td>
<td>25A0 - 25FF</td>
<td>幾何圖形</td>
</tr>
<tr class="odd">
<td>46</td>
<td>2600 - 26FF</td>
<td>其他符號</td>
</tr>
<tr class="even">
<td>47</td>
<td>2700 - 27BF</td>
<td>Dingbats</td>
</tr>
<tr class="odd">
<td>48</td>
<td>3000 - 303F</td>
<td>CJK 符號和標點符號</td>
</tr>
<tr class="even">
<td>49</td>
<td>3040 - 309F</td>
<td>平假名</td>
</tr>
<tr class="odd">
<td rowspan="2">50 $ {REMOVE} $<br />
</td>
<td>30A0 - 30FF</td>
<td>片假名</td>
</tr>
<tr class="even">
<td>31F0 - 31FF</td>
<td>片假名注音延伸模組</td>

</tr>
<tr class="odd">
<td rowspan="2">51 $ {REMOVE} $<br />
</td>
<td>3100 - 312F</td>
<td>符號</td>
</tr>
<tr class="even">
<td>31A0 - 31BF</td>
<td>注音擴充</td>

</tr>
<tr class="odd">
<td>52</td>
<td>3130 - 318F</td>
<td>韓文相容性拼音字母</td>
</tr>
<tr class="even">
<td>53</td>
<td>A840 - A87F</td>
<td>八位 pa</td>
</tr>
<tr class="odd">
<td>54</td>
<td>3200 - 32FF</td>
<td>包含 CJK 字母和月</td>
</tr>
<tr class="even">
<td>55</td>
<td>3300 - 33FF</td>
<td>CJK 相容性</td>
</tr>
<tr class="odd">
<td>56</td>
<td>AC00 - D7AF</td>
<td>韓文音節</td>
</tr>
<tr class="even">
<td>57</td>
<td>D800-DFFF</td>
<td>非平面0。 請注意，設定這個位表示至少有一個增補程式碼點超出這個字型所支援的基本多語系平面 (BMP) 。 請參閱 <a href="surrogates-and-supplementary-characters.md">代理和補充字元</a>。</td>
</tr>
<tr class="odd">
<td>58</td>
<td>10900-1091F</td>
<td>腓 尼 基</td>
</tr>
<tr class="even">
<td rowspan="7">59 $ {REMOVE} $<br />
</td>
<td>2E80 - 2EFF</td>
<td>CJK 根式補充</td>
</tr>
<tr class="odd">
<td>2F00 - 2FDF</td>
<td>康熙字根裡</td>

</tr>
<tr class="even">
<td>2FF0 - 2FFF</td>
<td>表意字元描述字元</td>

</tr>
<tr class="odd">
<td>3190 - 319F</td>
<td>漢文</td>

</tr>
<tr class="even">
<td>3400 - 4DBF</td>
<td>CJK 整合漢字擴充功能 A</td>

</tr>
<tr class="odd">
<td>4E00 - 9FFF</td>
<td>CJK 統一的表意文字</td>

</tr>
<tr class="even">
<td>20000-2A6DF</td>
<td>CJK 統一的表意文字擴充功能 B</td>

</tr>
<tr class="odd">
<td>60</td>
<td>E000 - F8FF</td>
<td>私用區域</td>
</tr>
<tr class="even">
<td rowspan="3">61 $ {REMOVE} $<br />
</td>
<td>31C0 - 31EF</td>
<td>CJK 筆觸</td>
</tr>
<tr class="odd">
<td>F900 - FAFF</td>
<td>CJK 相容性表意文字</td>

</tr>
<tr class="even">
<td>2F800 - 2FA1F</td>
<td>CJK 相容性表意文字補充</td>

</tr>
<tr class="odd">
<td>62</td>
<td>FB00 - FB4F</td>
<td>字母簡報形式</td>
</tr>
<tr class="even">
<td>63</td>
<td>FB50 - FDFF</td>
<td>阿拉伯文簡報表單-A</td>
</tr>
<tr class="odd">
<td>64</td>
<td>FE20 - FE2F</td>
<td>組合半標記</td>
</tr>
<tr class="even">
<td rowspan="2">65 $ {REMOVE} $<br />
</td>
<td>FE10 - FE1F</td>
<td>垂直表單</td>
</tr>
<tr class="odd">
<td>FE30 - FE4F</td>
<td>CJK 相容性表單</td>

</tr>
<tr class="even">
<td>66</td>
<td>FE50 - FE6F</td>
<td>小型表單變體</td>
</tr>
<tr class="odd">
<td>67</td>
<td>FE70 - FEFF</td>
<td>阿拉伯文簡報表單-B</td>
</tr>
<tr class="even">
<td>68</td>
<td>FF00 - FFEF</td>
<td>半形和全形形式</td>
</tr>
<tr class="odd">
<td>69</td>
<td>FFF0 - FFFF</td>
<td>特價</td>
</tr>
<tr class="even">
<td>70</td>
<td>0F00 - 0FFF</td>
<td>西藏文</td>
</tr>
<tr class="odd">
<td>71</td>
<td>0700 - 074F</td>
<td>敘利亞文</td>
</tr>
<tr class="even">
<td>72</td>
<td>0780 - 07BF</td>
<td>塔安那文</td>
</tr>
<tr class="odd">
<td>73</td>
<td>0D80 - 0DFF</td>
<td>僧伽羅文</td>
</tr>
<tr class="even">
<td>74</td>
<td>1000 - 109F</td>
<td>緬甸</td>
</tr>
<tr class="odd">
<td rowspan="3">75 $ {REMOVE} $<br />
</td>
<td>1200 - 137F</td>
<td>文</td>
</tr>
<tr class="even">
<td>1380-139F</td>
<td>埃塞俄比亞文補充</td>

</tr>
<tr class="odd">
<td>2D80 - 2DDF</td>
<td>埃塞俄比亞文擴充</td>

</tr>
<tr class="even">
<td>76</td>
<td>13A0 - 13FF</td>
<td>卻洛奇文</td>
</tr>
<tr class="odd">
<td>77</td>
<td>1400 - 167F</td>
<td>整合加拿大土著音節</td>
</tr>
<tr class="even">
<td>78</td>
<td>1680 - 169F</td>
<td>豎</td>
</tr>
<tr class="odd">
<td>79</td>
<td>16A0 - 16FF</td>
<td>符文</td>
</tr>
<tr class="even">
<td rowspan="2">80 $ {REMOVE} $<br />
</td>
<td>1780 - 17FF</td>
<td>高棉文</td>
</tr>
<tr class="odd">
<td>19E0 - 19FF</td>
<td>高棉符號</td>

</tr>
<tr class="even">
<td>81</td>
<td>1800 - 18AF</td>
<td>蒙古文</td>
</tr>
<tr class="odd">
<td>82</td>
<td>2800 - 28FF</td>
<td>盲文模式</td>
</tr>
<tr class="even">
<td rowspan="2">83 $ {REMOVE} $<br />
</td>
<td>A000 - A48F</td>
<td>彝語音節</td>
</tr>
<tr class="odd">
<td>A490 - A4CF</td>
<td>Yi 根式</td>

</tr>
<tr class="even">
<td rowspan="4">84 $ {REMOVE} $<br />
</td>
<td>1700 - 171F</td>
<td>他加祿文</td>
</tr>
<tr class="odd">
<td>1720 - 173F</td>
<td>族</td>

</tr>
<tr class="even">
<td>1740 - 175F</td>
<td>布錫文</td>

</tr>
<tr class="odd">
<td>1760 - 177F</td>
<td>塔班瓦文</td>

</tr>
<tr class="even">
<td>85</td>
<td>10300-1032F</td>
<td>舊的斜體</td>
</tr>
<tr class="odd">
<td>86</td>
<td>10330-1034F</td>
<td>哥 特 式</td>
</tr>
<tr class="even">
<td>87</td>
<td>10400-1044F</td>
<td>萊特</td>
</tr>
<tr class="odd">
<td rowspan="3">88 $ {REMOVE} $<br />
</td>
<td>1D000 - 1D0FF</td>
<td>拜占庭音樂符號</td>
</tr>
<tr class="even">
<td>1D100 - 1D1FF</td>
<td>音樂符號</td>

</tr>
<tr class="odd">
<td>1D200 - 1D24F</td>
<td>古希臘文音樂標記法</td>

</tr>
<tr class="even">
<td>89</td>
<td>1D400 - 1D7FF</td>
<td>數學英數位元符號</td>
</tr>
<tr class="odd">
<td rowspan="2">90 $ {REMOVE} $<br />
</td>
<td>FF000 - FFFFD</td>
<td>私用 (平面 15) </td>
</tr>
<tr class="even">
<td>100000-10FFFD</td>
<td>私用 (平面 16) </td>

</tr>
<tr class="odd">
<td rowspan="2">91 $ {REMOVE} $<br />
</td>
<td>FE00 - FE0F</td>
<td>變化選取器</td>
</tr>
<tr class="even">
<td>E0100 - E01EF</td>
<td>變化選取器補充</td>

</tr>
<tr class="odd">
<td>92</td>
<td>E0000 - E007F</td>
<td>標籤</td>
</tr>
<tr class="even">
<td>93</td>
<td>1900 - 194F</td>
<td>林布文</td>
</tr>
<tr class="odd">
<td>94</td>
<td>1950 - 197F</td>
<td>泰 Le</td>
</tr>
<tr class="even">
<td>95</td>
<td>1980-19DF</td>
<td>新傣文</td>
</tr>
<tr class="odd">
<td>96</td>
<td>1A00 - 1A1F</td>
<td>布吉斯文</td>
</tr>
<tr class="even">
<td>97</td>
<td>2C00 - 2C5F</td>
<td>文</td>
</tr>
<tr class="odd">
<td>98</td>
<td>2D30 - 2D7F</td>
<td>納</td>
</tr>
<tr class="even">
<td>99</td>
<td>4DC0 - 4DFF</td>
<td>易經帶字元符號</td>
</tr>
<tr class="odd">
<td>100</td>
<td>A800 - A82F</td>
<td>的</td>
</tr>
<tr class="even">
<td rowspan="3">101 $ {REMOVE} $<br />
</td>
<td>10000-1007F</td>
<td>線性 B 音節</td>
</tr>
<tr class="odd">
<td>10080-100FF</td>
<td>線性 B 表意文字</td>

</tr>
<tr class="even">
<td>10100-1013F</td>
<td>希臘愛琴大學號碼</td>

</tr>
<tr class="odd">
<td>102</td>
<td>10140-1018F</td>
<td>古希臘文數位</td>
</tr>
<tr class="even">
<td>103</td>
<td>10380-1039F</td>
<td>烏加里特文</td>
</tr>
<tr class="odd">
<td>104</td>
<td>103A0 - 103DF</td>
<td>舊的波斯</td>
</tr>
<tr class="even">
<td>105</td>
<td>10450-1047F</td>
<td>Shavian</td>
</tr>
<tr class="odd">
<td>106</td>
<td>10480-104AF</td>
<td>文</td>
</tr>
<tr class="even">
<td>107</td>
<td>10800-1083F</td>
<td>Cypriot 音節</td>
</tr>
<tr class="odd">
<td>108</td>
<td>10A00 - 10A5F</td>
<td>須</td>
</tr>
<tr class="even">
<td>109</td>
<td>1D300 - 1D35F</td>
<td>泰 Xuan Jing 符號</td>
</tr>
<tr class="odd">
<td rowspan="2">110 $ {REMOVE} $<br />
</td>
<td>12000-123FF</td>
<td>楔 形</td>
</tr>
<tr class="even">
<td>12400-1247F</td>
<td>Cuneiform 數位和標點符號</td>

</tr>
<tr class="odd">
<td>111</td>
<td>1D360 - 1D37F</td>
<td>計算杆數位</td>
</tr>
<tr class="even">
<td>112</td>
<td>1B80 - 1BBF</td>
<td>巽丹文</td>
</tr>
<tr class="odd">
<td>113</td>
<td>1C00 - 1C4F</td>
<td>雷布查文</td>
</tr>
<tr class="even">
<td>114</td>
<td>1C50 - 1C7F</td>
<td>桑塔爾文</td>
</tr>
<tr class="odd">
<td>115</td>
<td>A880 - A8DF</td>
<td>紹拉斯徹文</td>
</tr>
<tr class="even">
<td>116</td>
<td>A900 - A92F</td>
<td>開亞里文</td>
</tr>
<tr class="odd">
<td>117</td>
<td>A930 - A95F</td>
<td>拉讓文</td>
</tr>
<tr class="even">
<td>118</td>
<td>AA00 - AA5F</td>
<td>Cham</td>
</tr>
<tr class="odd">
<td>119</td>
<td>10190-101CF</td>
<td>古符號</td>
</tr>
<tr class="even">
<td>120</td>
<td>101D0 - 101FF</td>
<td>Phaistos 光碟</td>
</tr>
<tr class="odd">
<td rowspan="3">121 $ {REMOVE} $<br />
</td>
<td>10280-1029F</td>
<td>呂西亞文</td>
</tr>
<tr class="even">
<td>102A0 - 102DF</td>
<td>卡里亞文</td>

</tr>
<tr class="odd">
<td>10920-1093F</td>
<td>利底亞文</td>

</tr>
<tr class="even">
<td rowspan="2">122 $ {REMOVE} $<br />
</td>
<td>1F000 - 1F02F</td>
<td>麻將底圖</td>
</tr>
<tr class="odd">
<td>1F030 - 1F09F</td>
<td>Domino 磚</td>

</tr>
<tr class="even">
<td>123</td>

<td><strong>Windows 2000 和更新版本：</strong>版面配置進度，從右至左水準</td>
</tr>
<tr class="odd">
<td>124</td>

<td><strong>Windows 2000 和更新版本：</strong>版面配置進度、水準垂直</td>
</tr>
<tr class="even">
<td>125</td>

<td><strong>Windows 2000 和更新版本：</strong>版面配置進度，垂直靠上</td>
</tr>
<tr class="odd">
<td>126-127</td>

<td>保留給進程-內部使用</td>
</tr>
</tbody>
</table>



 

 

 



