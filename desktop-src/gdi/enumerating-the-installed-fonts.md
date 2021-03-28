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
# <a name="enumerating-the-installed-fonts"></a><span data-ttu-id="7f208-103">列舉已安裝的字型</span><span class="sxs-lookup"><span data-stu-id="7f208-103">Enumerating the Installed Fonts</span></span>

<span data-ttu-id="7f208-104">在某些情況下，應用程式必須能夠列舉可用的字型，並選取最適合特定操作的字型。</span><span class="sxs-lookup"><span data-stu-id="7f208-104">In some instances, an application must be able to enumerate the available fonts and select the one most appropriate for a particular operation.</span></span> <span data-ttu-id="7f208-105">應用程式可以藉由呼叫 [EnumFonts](/windows/desktop/api/Wingdi/nf-wingdi-enumfontsa) 或 [>enumfontfamilies](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesa) 函數來列舉可用的字型。</span><span class="sxs-lookup"><span data-stu-id="7f208-105">An application can enumerate the available fonts by calling the [EnumFonts](/windows/desktop/api/Wingdi/nf-wingdi-enumfontsa) or [EnumFontFamilies](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesa) function.</span></span> <span data-ttu-id="7f208-106">這些函式會將可用字型的相關資訊傳送至應用程式所提供的回呼函式。</span><span class="sxs-lookup"><span data-stu-id="7f208-106">These functions send information about the available fonts to a callback function that the application supplies.</span></span> <span data-ttu-id="7f208-107">回呼函數會接收 [LOGFONT](/windows/win32/api/wingdi/ns-wingdi-logfonta) 和 [NEWTEXTMETRIC](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica) 結構中的資訊。</span><span class="sxs-lookup"><span data-stu-id="7f208-107">The callback function receives information in [LOGFONT](/windows/win32/api/wingdi/ns-wingdi-logfonta) and [NEWTEXTMETRIC](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica) structures.</span></span> <span data-ttu-id="7f208-108"> ([**NEWTEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica) 結構包含 TrueType 字型的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="7f208-108">(The [**NEWTEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica) structure contains information about a TrueType font.</span></span> <span data-ttu-id="7f208-109">當回呼函式收到非 TrueType 字型的相關資訊時，此資訊會包含在 [TEXTMETRIC](/windows/win32/api/wingdi/ns-wingdi-textmetrica) 結構中。 ) 使用這項資訊，應用程式可以將使用者的選擇限制為只有可用的字型。</span><span class="sxs-lookup"><span data-stu-id="7f208-109">When the callback function receives information about a non-TrueType font, the information is contained in a [TEXTMETRIC](/windows/win32/api/wingdi/ns-wingdi-textmetrica) structure.) By using this information, an application can limit the user's choices to only those fonts that are available.</span></span>

<span data-ttu-id="7f208-110">[**>enumfontfamilies**](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesa)函式與 [**EnumFonts**](/windows/win32/api/wingdi/nf-wingdi-enumfontsa)函數類似，但包含一些額外的功能。</span><span class="sxs-lookup"><span data-stu-id="7f208-110">The [**EnumFontFamilies**](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesa) function is similar to the [**EnumFonts**](/windows/win32/api/wingdi/nf-wingdi-enumfontsa) function but includes some extra functionality.</span></span> <span data-ttu-id="7f208-111">**>enumfontfamilies** 可讓應用程式利用 TrueType 字型提供的樣式。</span><span class="sxs-lookup"><span data-stu-id="7f208-111">**EnumFontFamilies** allows an application to take advantage of styles available with TrueType fonts.</span></span> <span data-ttu-id="7f208-112">新的和升級的應用程式應該使用 **>enumfontfamilies** ，而不是 **EnumFonts**。</span><span class="sxs-lookup"><span data-stu-id="7f208-112">New and upgraded applications should use **EnumFontFamilies** instead of **EnumFonts**.</span></span>

<span data-ttu-id="7f208-113">TrueType 字型是根據字樣名稱來組織 (例如，新的) 和樣式名稱 (例如，斜體、粗體和粗體) 。</span><span class="sxs-lookup"><span data-stu-id="7f208-113">TrueType fonts are organized around a typeface name (for example, Courier New) and style names (for example, italic, bold, and extra-bold).</span></span> <span data-ttu-id="7f208-114">[**>enumfontfamilies**](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesa)函式會列舉與指定系列名稱相關聯的所有樣式，而不只是粗體和斜體屬性。</span><span class="sxs-lookup"><span data-stu-id="7f208-114">The [**EnumFontFamilies**](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesa) function enumerates all the styles associated with a specified family name, not simply the bold and italic attributes.</span></span> <span data-ttu-id="7f208-115">例如，當系統包含的 TrueType 字型稱為「新的新粗體」時， **>enumfontfamilies** 會使用其他的新字型來列出該字型。</span><span class="sxs-lookup"><span data-stu-id="7f208-115">For example, when the system includes a TrueType font called Courier New Extra-Bold, **EnumFontFamilies** lists it with the other Courier New fonts.</span></span> <span data-ttu-id="7f208-116">**>enumfontfamilies** 的功能對於具有許多或不尋常樣式的字型，以及跨國際框線的字型很有用。</span><span class="sxs-lookup"><span data-stu-id="7f208-116">The capabilities of **EnumFontFamilies** are helpful for fonts with many or unusual styles and for fonts that cross international borders.</span></span>

<span data-ttu-id="7f208-117">如果應用程式未提供字樣名稱， [EnumFonts](/windows/desktop/api/Wingdi/nf-wingdi-enumfontsa) 和 [>enumfontfamilies](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesa) 函式會提供每個可用系列中某個字型的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="7f208-117">If an application does not supply a typeface name, the [EnumFonts](/windows/desktop/api/Wingdi/nf-wingdi-enumfontsa) and [EnumFontFamilies](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesa) functions supply information about one font in each available family.</span></span> <span data-ttu-id="7f208-118">若要列舉裝置內容中的所有字型，應用程式可以針對字樣名稱指定 **Null** 、編譯可用字體的清單，然後列舉每個字型中的每個字型。</span><span class="sxs-lookup"><span data-stu-id="7f208-118">To enumerate all the fonts in a device context, the application can specify **NULL** for the typeface name, compile a list of the available typefaces, and then enumerate each font in each typeface.</span></span>

<span data-ttu-id="7f208-119">下列範例會使用 [**>enumfontfamilies**](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesa) 函式來取得可用的點陣、向量和 TrueType 字型系列的數目。</span><span class="sxs-lookup"><span data-stu-id="7f208-119">The following example uses the [**EnumFontFamilies**](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesa) function to retrieve the number of available raster, vector, and TrueType font families.</span></span>


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



<span data-ttu-id="7f208-120">這個範例會使用兩個遮罩（點陣 \_ FONTTYPE 和 TRUETYPE \_ FONTTYPE）來判斷所列舉的字型類型。</span><span class="sxs-lookup"><span data-stu-id="7f208-120">This example uses two masks, RASTER\_FONTTYPE and TRUETYPE\_FONTTYPE, to determine the type of font being enumerated.</span></span> <span data-ttu-id="7f208-121">如果設定了點陣 \_ FONTTYPE 位，字型就是點陣字型。</span><span class="sxs-lookup"><span data-stu-id="7f208-121">If the RASTER\_FONTTYPE bit is set, the font is a raster font.</span></span> <span data-ttu-id="7f208-122">如果設定了 TRUETYPE \_ FONTTYPE 位，字型就是 truetype 字型。</span><span class="sxs-lookup"><span data-stu-id="7f208-122">If the TRUETYPE\_FONTTYPE bit is set, the font is a TrueType font.</span></span> <span data-ttu-id="7f208-123">如果兩個位都未設定，字型就是向量字型。</span><span class="sxs-lookup"><span data-stu-id="7f208-123">If neither bit is set, the font is a vector font.</span></span> <span data-ttu-id="7f208-124">第三個遮罩（裝置 \_ FONTTYPE）是在裝置 (例如，雷射印表機) 支援下載 TrueType 字型時設定; 如果裝置是顯示介面卡、點矩陣印表機或其他點陣裝置，則為零。</span><span class="sxs-lookup"><span data-stu-id="7f208-124">A third mask, DEVICE\_FONTTYPE, is set when a device (for example, a laser printer) supports downloading TrueType fonts; it is zero if the device is a display adapter, dot-matrix printer, or other raster device.</span></span> <span data-ttu-id="7f208-125">應用程式也可以使用裝置 \_ FONTTYPE 遮罩來區別 GDI 提供的點陣字型與裝置提供的字型。</span><span class="sxs-lookup"><span data-stu-id="7f208-125">An application can also use the DEVICE\_FONTTYPE mask to distinguish GDI-supplied raster fonts from device-supplied fonts.</span></span> <span data-ttu-id="7f208-126">系統可以模擬 GDI 提供之點陣字型的粗體、斜體、底線和刪除線屬性，但不能用於裝置提供的字型。</span><span class="sxs-lookup"><span data-stu-id="7f208-126">The system can simulate bold, italic, underline, and strikeout attributes for GDI-supplied raster fonts, but not for device-supplied fonts.</span></span>

<span data-ttu-id="7f208-127">應用程式也可以檢查 [NEWTEXTMETRIC](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica)結構之 **tmPitchAndFamily** 成員中的位1和2，以識別 TrueType 字型。</span><span class="sxs-lookup"><span data-stu-id="7f208-127">An application can also check bits 1 and 2 in the **tmPitchAndFamily** member of the [NEWTEXTMETRIC](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica) structure to identify a TrueType font.</span></span> <span data-ttu-id="7f208-128">如果位1是0，而位2是1，則字型是 TrueType 字型。</span><span class="sxs-lookup"><span data-stu-id="7f208-128">If bit 1 is 0 and bit 2 is 1, the font is a TrueType font.</span></span>

<span data-ttu-id="7f208-129">向量字型會分類為 OEM \_ 字元集，而不是 ANSI \_ 字元集。</span><span class="sxs-lookup"><span data-stu-id="7f208-129">Vector fonts are categorized as OEM\_CHARSET instead of ANSI\_CHARSET.</span></span> <span data-ttu-id="7f208-130">有些應用程式會使用這項資訊來識別向量字型，檢查 [**NEWTEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica)結構的 **tmCharSet** 成員。</span><span class="sxs-lookup"><span data-stu-id="7f208-130">Some applications identify vector fonts by using this information, checking the **tmCharSet** member of the [**NEWTEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica) structure.</span></span> <span data-ttu-id="7f208-131">除非特別要求，否則此分類通常會防止字型對應工具選擇向量字型。</span><span class="sxs-lookup"><span data-stu-id="7f208-131">This categorization usually prevents the font mapper from choosing vector fonts unless they are specifically requested.</span></span> <span data-ttu-id="7f208-132"> (大部分的應用程式不會再使用向量字型，因為它們的筆觸是一行，而且需要較長的時間來繪製比 TrueType 字型更長的文字，以提供許多需要向量字型的相同縮放和旋轉功能。 ) </span><span class="sxs-lookup"><span data-stu-id="7f208-132">(Most applications no longer use vector fonts because their strokes are single lines and they take longer to draw than TrueType fonts, which offer many of the same scaling and rotation features that required vector fonts.)</span></span>

 

 
