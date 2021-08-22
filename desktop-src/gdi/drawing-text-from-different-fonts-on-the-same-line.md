---
description: 字型家族內的不同類型樣式可以有不同的寬度。
ms.assetid: d21613ef-1ba4-40bb-b922-afe287556441
title: 在同一行上繪製不同字型的文字
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad28f13c94e568073504f07e8722e5d688cb12aa1b376b0f52fad752574e6f8c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119038046"
---
# <a name="drawing-text-from-different-fonts-on-the-same-line"></a>在同一行上繪製不同字型的文字

字型家族內的不同類型樣式可以有不同的寬度。 例如，系列的粗體和斜體樣式一律會比指定的點大小的羅馬樣式更寬。 當您在同一行上顯示或列印數種類型的樣式時，您必須追蹤線的寬度，以避免在彼此上方顯示或列印字元。

您可以使用兩個函式，以目前的字型來取得文字 (或範圍) 的寬度。 [GetTabbedTextExtent](/windows/desktop/api/Winuser/nf-winuser-gettabbedtextextenta)函數會計算字元字串的寬度和高度。 如果字串包含一或多個定位字元，則字串的寬度會以指定的定位點-停用位置陣列為基礎。 [GetTextExtentPoint32](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentpoint32a)函式會計算文字行的寬度和高度。

必要時，系統會變更字元點陣圖以會合成字型。 若要合成粗體字的字元，系統會繪製字元兩次：在起始點，然後再繪製一個圖元到起點的右邊。 若要以斜體字型合成字元，系統會在字元資料格的底部繪製兩個數據列，將起點向右移動一個圖元、繪製接下來的兩個數據列，然後繼續直到繪製該字元為止。 藉由移動圖元，每個字元會顯示為向右切變。 切變數是字元高度的函式。

撰寫包含多個字型之文字行的其中一種方式，是在每次呼叫 [TextOut](/windows/desktop/api/Wingdi/nf-wingdi-textouta)之後使用 [**GetTextExtentPoint32**](/windows/win32/api/wingdi/nf-wingdi-gettextextentpoint32a)函式，並將長度新增至目前的位置。 下列範例會寫入「這是範例字串」這一行。 針對 "This a" 使用粗體字元，為 "sample" 切換為斜體字元，然後針對 "string" 傳回粗體字字元。 列印所有字串之後，它會還原系統預設字元。


```C++
int XIncrement; 
int YStart; 
TEXTMETRIC tm; 
HFONT hfntDefault, hfntItalic, hfntBold; 
SIZE sz; 
LPSTR lpszString1 = "This is a "; 
LPSTR lpszString2 = "sample "; 
LPSTR lpszString3 = "string."; 
HRESULT hr;
size_t * pcch;
 
// Create a bold and an italic logical font.  
 
hfntItalic = MyCreateFont(); 
hfntBold = MyCreateFont(); 
 
 
// Select the bold font and draw the first string  
// beginning at the specified point (XIncrement, YStart).  
 
XIncrement = 10; 
YStart = 50; 
hfntDefault = SelectObject(hdc, hfntBold); 
hr = StringCchLength(lpszString1, 11, pcch);
        if (FAILED(hr))
        {
        // TODO: write error handler 
        }
TextOut(hdc, XIncrement, YStart, lpszString1, *pcch); 
 
// Compute the length of the first string and add  
// this value to the x-increment that is used for the  
// text-output operation.  

hr = StringCchLength(lpszString1, 11, pcch);
        if (FAILED(hr))
        {
        // TODO: write error handler 
        } 
GetTextExtentPoint32(hdc, lpszString1, *pcch, &sz); 
XIncrement += sz.cx; 
 
// Retrieve the overhang value from the TEXTMETRIC  
// structure and subtract it from the x-increment.  
// (This is only necessary for non-TrueType raster  
// fonts.)  
 
GetTextMetrics(hdc, &tm); 
XIncrement -= tm.tmOverhang; 
 
// Select an italic font and draw the second string  
// beginning at the point (XIncrement, YStart).  
 
hfntBold = SelectObject(hdc, hfntItalic); 
GetTextMetrics(hdc, &tm); 
XIncrement -= tm.tmOverhang;
hr = StringCchLength(lpszString2, 8, pcch);
        if (FAILED(hr))
        {
        // TODO: write error handler 
        } 
TextOut(hdc, XIncrement, YStart, lpszString2, *pcch); 
 
// Compute the length of the second string and add  
// this value to the x-increment that is used for the  
// text-output operation.  

hr = StringCchLength(lpszString2, 8, pcch);
        if (FAILED(hr))
        {
        // TODO: write error handler 
        }  
GetTextExtentPoint32(hdc, lpszString2, *pcch, &sz); 
XIncrement += sz.cx; 
 
// Reselect the bold font and draw the third string  
// beginning at the point (XIncrement, YStart).  
 
SelectObject(hdc, hfntBold);
hr = StringCchLength(lpszString3, 8, pcch);
        if (FAILED(hr))
        {
        // TODO: write error handler 
        }  
TextOut(hdc, XIncrement - tm.tmOverhang, YStart, lpszString3, 
            *pcch); 
 
// Reselect the original font.  
 
SelectObject(hdc, hfntDefault); 
 
// Delete the bold and italic fonts.  
 
DeleteObject(hfntItalic); 
DeleteObject(hfntBold); 
```



在此範例中， [GetTextExtentPoint32](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentpoint32a) 函式會使用指定字串的長度和高度，初始化 [大小](/previous-versions//dd145106(v=vs.85)) 結構的成員。 [GetTextMetrics](/windows/desktop/api/Wingdi/nf-wingdi-gettextmetrics)函式會捕獲目前字型的懸垂。 因為如果字型是 TrueType 字型，所以懸垂為零，而懸垂值不會變更字串位置。 但是對於點陣字型而言，使用懸垂值是很重要的。

懸垂會從粗體字串減去一次，如果字型是點陣字型，則會將後續字元放在接近字串結尾的字元。 因為懸垂會影響點陣字型中的斜體字串開頭和結尾，所以字元會從指定位置的右邊開始，並在最後一個字元資料格的端點左邊結束。  ([**GetTextExtentPoint32**](/windows/win32/api/wingdi/nf-wingdi-gettextextentpoint32a) 函式會抓取字元資料格的範圍，而不是字元的範圍。 ) 若要考慮點陣斜體字串中的懸垂，範例會先減去懸垂再放置字串，然後再將它重新減去，然後再放置後續字元。

[SetTextJustification](/windows/desktop/api/Wingdi/nf-wingdi-settextjustification)函式會在文字行中將額外的空格新增至分行符號。 您可以使用 [GetTextExtentPoint](/windows/desktop/api/WinGdi/nf-wingdi-gettextextentpointa) 函式來判斷字串的範圍，然後從該行應該佔用的總空間量減去該範圍，並使用 [**SetTextJustification**](/windows/win32/api/wingdi/nf-wingdi-settextjustification) 函式將額外的空間分配給字串中的分隔字元。 [SetTextCharacterExtra](/windows/desktop/api/Wingdi/nf-wingdi-settextcharacterextra)函式會在所選字型中的每個字元資料格加上額外的空間，包括 break 字元。  (您可以使用 [GetTextCharacterExtra](/windows/desktop/api/Wingdi/nf-wingdi-gettextcharacterextra) 函式來判斷目前新增至字元資料格的額外空間量;預設設定為零。 ) 

您可以使用 [GetCharWidth32](/windows/desktop/api/Wingdi/nf-wingdi-getcharwidth32a) 或 [GetCharABCWidths](/windows/desktop/api/Wingdi/nf-wingdi-getcharabcwidthsa) 函式來取得字型中的個別字元寬度，以較大的精確度來放置字元。 [**GetCharABCWidths**](/windows/win32/api/wingdi/nf-wingdi-getcharabcwidthsa)函式比 [**GetCharWidth32**](/windows/win32/api/wingdi/nf-wingdi-getcharwidth32a)函數更為精確，但只能搭配 TrueType 字型使用。

ABC 間距也可讓應用程式執行非常精確的文字對齊。 例如，當應用程式靠右對齊點陣羅馬字型但未使用 ABC 間距時，會將前進寬度計算為字元寬度。 這表示點陣圖中圖像右邊的空白字元會對齊，而非圖像本身。 藉由使用 ABC 寬度，當對齊文字時，應用程式的放置和移除空白字元會有更大的彈性，因為它們具有可讓它們精確控制 intercharacter 間距的資訊。

 

 
