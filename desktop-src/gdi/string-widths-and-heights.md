---
description: 除了針對個別字元抓取字元寬度的資料之外，應用程式也需要計算整個字串的寬度和高度。
ms.assetid: 0c1d9142-258a-447f-8950-8d684645383b
title: 字串寬度和高度
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f57846d0588c518f445523361ae186e4b966bf93
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848895"
---
# <a name="string-widths-and-heights"></a>字串寬度和高度

除了針對個別字元抓取字元寬度的資料之外，應用程式也需要計算整個字串的寬度和高度。 兩個函式會取出字串寬度和高度測量： [**GetTextExtentPoint32**](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentpoint32a)和 [**GetTabbedTextExtent**](/windows/desktop/api/Winuser/nf-winuser-gettabbedtextextenta)。 如果字串不包含定位字元，則應用程式可以使用 **GetTextExtentPoint32** 函式來取得指定之字串的寬度和高度。 如果字串包含定位字元，則應用程式應該呼叫 GetTabbedTextExtent 函數。

應用程式可以使用 [**GetTextExtentExPoint**](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentexpointa) 函式進行自動換行作業。 此函式會從指定的字串中傳回符合指定空間的字元數。

## <a name="font-ascenders-and-descenders"></a>字型 Ascenders 和下行

有些應用程式會使用字型的最大 ascender 和下行，來決定不同大小的文字行間距。 應用程式可以藉由呼叫 [**GetTextMetrics**](/windows/desktop/api/Wingdi/nf-wingdi-gettextmetrics)函數，然後檢查 [**TEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-textmetrica)的 **tmAscent** 和 **tmDescent** 成員，來取得這些值。

最大升高和下降與印刷樣式升高和下降不同。 在 TrueType 和 OpenType 字型中，印刷樣式升高和下降通常是 g 字元的 f 圖像和底部的頂端。 應用程式可以透過呼叫 [**GetOutlineTextMetrics**](/windows/desktop/api/Wingdi/nf-wingdi-getoutlinetextmetricsa)函式並檢查 [**OUTLINETEXTMETRIC**](/windows/desktop/api/Wingdi/ns-wingdi-outlinetextmetrica)結構的 **otmMacAscent** 和 **otmMacDescent** 成員中的值，來取得 TrueType 或 OpenType 字型的印刷樣式 ascender 和下行。

下圖顯示 [**NEWTEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica) 和 [**OUTLINETEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-outlinetextmetrica) 結構中所傳回之垂直文字度量值之間的差異。  (開頭為 otm 的名稱是 **OUTLINETEXTMETRIC** 結構的成員。 ) 

![顯示文字度量值與外框文字度量值對比的圖例](images/csftx-03.png)

## <a name="font-dimensions"></a>字型維度

應用程式可以藉由呼叫 [**GetOutlineTextMetrics**](/windows/desktop/api/Wingdi/nf-wingdi-getoutlinetextmetricsa) 函式來取得 TrueType 或 OpenType 字型的實體維度。 應用程式可以藉由呼叫 [**GetTextMetrics**](/windows/desktop/api/Wingdi/nf-wingdi-gettextmetrics) 函式來取出任何其他字型的實體維度。 若要判斷輸出裝置的維度，應用程式可以呼叫 [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) 函數。 **GetDeviceCaps** 會傳回實體和邏輯維度。

邏輯英寸是系統用來在螢幕上呈現清晰清晰字型的量值，大約30到40% 的百分比大於實體英寸。 使用邏輯英寸可在螢幕和印表機的輸出之間排除完全相符的結果。 開發人員應該要注意的是，畫面上的文字並不只是頁面上顯示的文字縮放版本，尤其是將圖形併入文字時。

 

 
