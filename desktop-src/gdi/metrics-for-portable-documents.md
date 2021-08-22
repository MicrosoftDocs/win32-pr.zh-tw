---
description: 下錶針對需要可移植檔的應用程式，以及允許應用程式抓取這些標準的函式，指定最重要的字型指標。
ms.assetid: 61f6d244-7397-42af-af58-0ab9d07bf19e
title: 便攜檔的計量
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3762846e6d8280c2680f47f3cb32cd847ea4e664dab47a8a0995f5505c393da3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119558498"
---
# <a name="metrics-for-portable-documents"></a>便攜檔的計量

下錶針對需要可移植檔的應用程式，以及允許應用程式抓取這些標準的函式，指定最重要的字型指標。



| 函數                                               | 計量                | 使用                                                                                                          |
|--------------------------------------------------------|-----------------------|--------------------------------------------------------------------------------------------------------------|
| [**>enumfontfamilies**](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesa)           | **ntmSizeEM**         | 設計計量的抓取;轉換成裝置計量。                                                   |
| [**GetCharABCWidths**](/windows/desktop/api/Wingdi/nf-wingdi-getcharabcwidthsa)           | **ABCWidths**         | 在邊界的開頭和結尾、圖片邊界和其他文字分隔字元的精確位置。 |
| [**GetCharWidth32**](/windows/desktop/api/Wingdi/nf-wingdi-getcharwidth32a)               | **AdvanceWidths**     | 字元在行上的位置。                                                                           |
| [**GetOutlineTextMetrics**](/windows/desktop/api/Wingdi/nf-wingdi-getoutlinetextmetricsa) | **otmfsType**         | 字型內嵌位。                                                                                         |
|                                                        | **otmsCharSlopeRise** | 傾斜字型之游標斜率的 Y 元件。                                                            |
|                                                        | **otmsCharSlopeRun**  | 傾斜字型之游標斜率的 X 元件。                                                            |
|                                                        | **otmAscent**         | 行距。                                                                                                |
|                                                        | **otmDescent**        | 行距。                                                                                                |
|                                                        | **otmLineGap**        | 行距。                                                                                                |
|                                                        | **otmpFamilyName**    | 字型識別。                                                                                         |
|                                                        | **otmpStyleName**     | 字型識別。                                                                                         |
|                                                        | **otmpFullName**      | 字型識別 (通常是) 的系列和樣式名稱。                                                      |



 

[OtmLineGap](/windows/desktop/api/Wingdi/ns-wingdi-outlinetextmetrica)結構的 **otmsCharSlopeRise**、 **otmsCharSlopeRun**、 **otmAscent**、 **otmDescent** 和 **OUTLINETEXTMETRIC** 成員會進行縮放或轉換，以對應到目前的裝置模式和物理高度 (如 [tmHeight](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica)結構) 的 **NEWTEXTMETRIC** 成員所指定。

當應用程式必須選取相同的字型時（例如，當檔重新開啟或移至不同的作業系統時），字型識別在這些實例中相當重要。 當應用程式以完整名稱要求字型時，字型對應程式一律會選取正確的字型。 系列和樣式名稱提供 [標準字型] 對話方塊的輸入，以確保正確放置選取列。

**OtmsCharSlopeRise** 和 **otmsCharSlopeRun** 值會用來產生字型之主要斜體角度的相近近似值。 針對典型的羅馬字型， **otmsCharSlopeRise** 是1，而 **otmsCharSlopeRun** 是0。 若為斜體字型，這些值會嘗試近似字型之主要斜體角度的正弦和余弦 (以逆時針度為單位的) ;請注意，直立字型的斜體角度是0。 因為這些值不會以設計單位表示，所以不應轉換成裝置單位。

字元位置和行距計量可讓應用程式計算跨螢幕、印表機、typesetters 或甚至平臺可移植的裝置獨立分行符號。

**執行與裝置無關的頁面配置**

1.  將所有設計計量正規化為常見的超高解析度 (UHR) 值 (例如 65536 DPI) ;這可防止發生舍入錯誤。
2.  根據 UHR 計量和實體頁面寬度計算分行符號;這會產生文字資料流程內線條的起始點和結束點。
3.  以裝置單位計算裝置頁面寬度 (例如，圖元) 。
4.  使用步驟2中計算出來的分行符號，將每一行文字放入裝置頁面寬度。
5.  使用 UHR 計量和實體頁面長度來計算分頁符號;這會產生每個頁面的行數。
6.  以裝置單位計算線條高度。
7.  使用步驟5中的每頁行和步驟6的線條高度，將文字行放到頁面上。

如果所有應用程式都採用這些技術，開發人員可以確保從某個應用程式移到另一個應用程式的檔，將會保留其原始外觀和格式。

 

 



