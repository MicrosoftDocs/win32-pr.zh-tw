---
description: 在某些情況下，應用程式必須能夠列舉可用的字型，並選取最適合特定操作的字型。
ms.assetid: 18db1b03-6e3c-4be3-b637-a21bf41cc080
title: 列舉已安裝的字型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4dee38ccf9807371181388536f1230d222d448bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191947"
---
# <a name="enumerating-the-installed-fonts"></a>列舉已安裝的字型

在某些情況下，應用程式必須能夠列舉可用的字型，並選取最適合特定操作的字型。 應用程式可以藉由呼叫 [EnumFonts](/windows/desktop/api/Wingdi/nf-wingdi-enumfontsa) 或 [>enumfontfamilies](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesa) 函數來列舉可用的字型。 這些函式會將可用字型的相關資訊傳送至應用程式所提供的回呼函式。 回呼函數會接收 [LOGFONT](/windows/win32/api/wingdi/ns-wingdi-logfonta) 和 [NEWTEXTMETRIC](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica) 結構中的資訊。  ([**NEWTEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica) 結構包含 TrueType 字型的相關資訊。 當回呼函式收到非 TrueType 字型的相關資訊時，此資訊會包含在 [TEXTMETRIC](/windows/win32/api/wingdi/ns-wingdi-textmetrica) 結構中。 ) 使用這項資訊，應用程式可以將使用者的選擇限制為只有可用的字型。

[**>enumfontfamilies**](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesa)函式與 [**EnumFonts**](/windows/win32/api/wingdi/nf-wingdi-enumfontsa)函數類似，但包含一些額外的功能。 **>enumfontfamilies** 可讓應用程式利用 TrueType 字型提供的樣式。 新的和升級的應用程式應該使用 **>enumfontfamilies** ，而不是 **EnumFonts**。

TrueType 字型是根據字樣名稱來組織 (例如，新的) 和樣式名稱 (例如，斜體、粗體和粗體) 。 [**>enumfontfamilies**](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesa)函式會列舉與指定系列名稱相關聯的所有樣式，而不只是粗體和斜體屬性。 例如，當系統包含的 TrueType 字型稱為「新的新粗體」時， **>enumfontfamilies** 會使用其他的新字型來列出該字型。 **>enumfontfamilies** 的功能對於具有許多或不尋常樣式的字型，以及跨國際框線的字型很有用。

如果應用程式未提供字樣名稱， [EnumFonts](/windows/desktop/api/Wingdi/nf-wingdi-enumfontsa) 和 [>enumfontfamilies](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesa) 函式會提供每個可用系列中某個字型的相關資訊。 若要列舉裝置內容中的所有字型，應用程式可以針對字樣名稱指定 **Null** 、編譯可用字體的清單，然後列舉每個字型中的每個字型。

下列範例會使用 [**>enumfontfamilies**](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesa) 函式來取得可用的點陣、向量和 TrueType 字型系列的數目。


```C++
    UINT uAlignPrev; 
    int aFontCount[] = { 0, 0, 0 }; 
    char szCount[8];
        HRESULT hr;
        size_t * pcch; 
 
    EnumFontFamilies(hdc, (LPCTSTR) NULL, 
        (FONTENUMPROC) EnumFamCallBack, (LPARAM) aFontCount); 
 
    uAlignPrev = SetTextAlign(hdc, TA_UPDATECP); 
 
    MoveToEx(hdc, 10, 50, (LPPOINT)NULL); 
    TextOut(hdc, 0, 0, "Number of raster fonts: ", 24); 
    itoa(aFontCount[0], szCount, 10); 
        
        hr = StringCchLength(szCount, 9, pcch);
        if (FAILED(hr))
        {
        // TODO: write error handler 
        }
    TextOut(hdc, 0, 0, szCount, *pcch); 
 
    MoveToEx(hdc, 10, 75, (LPPOINT)NULL); 
    TextOut(hdc, 0, 0, "Number of vector fonts: ", 24); 
    itoa(aFontCount[1], szCount, 10);
        hr = StringCchLength(szCount, 9, pcch);
        if (FAILED(hr))
        {
        // TODO: write error handler 
        } 
    TextOut(hdc, 0, 0, szCount, *pcch); 
 
    MoveToEx(hdc, 10, 100, (LPPOINT)NULL); 
    TextOut(hdc, 0, 0, "Number of TrueType fonts: ", 26); 
    itoa(aFontCount[2], szCount, 10);
        hr = StringCchLength(szCount, 9, pcch);
        if (FAILED(hr))
        {
        // TODO: write error handler 
        }
    TextOut(hdc, 0, 0, szCount, *pcch); 
 
    SetTextAlign(hdc, uAlignPrev); 
 
BOOL CALLBACK EnumFamCallBack(LPLOGFONT lplf, LPNEWTEXTMETRIC lpntm, DWORD FontType, LPVOID aFontCount) 
{ 
    int far * aiFontCount = (int far *) aFontCount; 
 
    // Record the number of raster, TrueType, and vector  
    // fonts in the font-count array.  
 
    if (FontType & RASTER_FONTTYPE) 
        aiFontCount[0]++; 
    else if (FontType & TRUETYPE_FONTTYPE) 
        aiFontCount[2]++; 
    else 
        aiFontCount[1]++; 
 
    if (aiFontCount[0] || aiFontCount[1] || aiFontCount[2]) 
        return TRUE; 
    else 
        return FALSE; 
 
    UNREFERENCED_PARAMETER( lplf ); 
    UNREFERENCED_PARAMETER( lpntm ); 
} 
```



這個範例會使用兩個遮罩（點陣 \_ FONTTYPE 和 TRUETYPE \_ FONTTYPE）來判斷所列舉的字型類型。 如果設定了點陣 \_ FONTTYPE 位，字型就是點陣字型。 如果設定了 TRUETYPE \_ FONTTYPE 位，字型就是 truetype 字型。 如果兩個位都未設定，字型就是向量字型。 第三個遮罩（裝置 \_ FONTTYPE）是在裝置 (例如，雷射印表機) 支援下載 TrueType 字型時設定; 如果裝置是顯示介面卡、點矩陣印表機或其他點陣裝置，則為零。 應用程式也可以使用裝置 \_ FONTTYPE 遮罩來區別 GDI 提供的點陣字型與裝置提供的字型。 系統可以模擬 GDI 提供之點陣字型的粗體、斜體、底線和刪除線屬性，但不能用於裝置提供的字型。

應用程式也可以檢查 [NEWTEXTMETRIC](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica)結構之 **tmPitchAndFamily** 成員中的位1和2，以識別 TrueType 字型。 如果位1是0，而位2是1，則字型是 TrueType 字型。

向量字型會分類為 OEM \_ 字元集，而不是 ANSI \_ 字元集。 有些應用程式會使用這項資訊來識別向量字型，檢查 [**NEWTEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica)結構的 **tmCharSet** 成員。 除非特別要求，否則此分類通常會防止字型對應工具選擇向量字型。  (大部分的應用程式不會再使用向量字型，因為它們的筆觸是一行，而且需要較長的時間來繪製比 TrueType 字型更長的文字，以提供許多需要向量字型的相同縮放和旋轉功能。 ) 

 

 
