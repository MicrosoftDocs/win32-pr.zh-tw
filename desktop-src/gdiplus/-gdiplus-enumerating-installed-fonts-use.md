---
description: InstalledFontCollection 類別繼承自 FontCollection 抽象基類。
ms.assetid: 59598f66-4241-4766-a2f0-5de736de959e
title: 列舉已安裝的字型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f41242522c2575ffb08e53f7100380ac9a849d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192330"
---
# <a name="enumerating-installed-fonts"></a><span data-ttu-id="b3842-103">列舉已安裝的字型</span><span class="sxs-lookup"><span data-stu-id="b3842-103">Enumerating Installed Fonts</span></span>

<span data-ttu-id="b3842-104">[**InstalledFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-installedfontcollection)類別繼承自 [**FontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontcollection)抽象基類。</span><span class="sxs-lookup"><span data-stu-id="b3842-104">The [**InstalledFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-installedfontcollection) class inherits from the [**FontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontcollection) abstract base class.</span></span> <span data-ttu-id="b3842-105">您可以使用 **InstalledFontCollection** 物件來列舉電腦上所安裝的字型。</span><span class="sxs-lookup"><span data-stu-id="b3842-105">You can use an **InstalledFontCollection** object to enumerate the fonts installed on the computer.</span></span> <span data-ttu-id="b3842-106">**InstalledFontCollection** 物件的 [**FontCollection：： GetFamilies**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilies)方法會傳回 [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily)物件的陣列。</span><span class="sxs-lookup"><span data-stu-id="b3842-106">The [**FontCollection::GetFamilies**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilies) method of an **InstalledFontCollection** object returns an array of [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) objects.</span></span> <span data-ttu-id="b3842-107">在呼叫 **FontCollection：： GetFamilies** 之前，您必須配置夠大的緩衝區來保存該陣列。</span><span class="sxs-lookup"><span data-stu-id="b3842-107">Before you call **FontCollection::GetFamilies**, you must allocate a buffer large enough to hold that array.</span></span> <span data-ttu-id="b3842-108">若要判斷所需的緩衝區大小，請呼叫 [**FontCollection：： GetFamilyCount**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilycount) 方法，並將傳回值乘以 **sizeof** (**FontFamily**) 。</span><span class="sxs-lookup"><span data-stu-id="b3842-108">To determine the size of the required buffer, call the [**FontCollection::GetFamilyCount**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilycount) method and multiply the return value by **sizeof**(**FontFamily**).</span></span>

<span data-ttu-id="b3842-109">下列範例會列出電腦上安裝的所有字型系列名稱。</span><span class="sxs-lookup"><span data-stu-id="b3842-109">The following example lists the names of all the font families installed on the computer.</span></span> <span data-ttu-id="b3842-110">程式碼會藉由呼叫 [**FontCollection：： GetFamilies**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilies)所傳回之陣列中每個 [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily)物件的 [**FontFamily：： GetFamilyName**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontfamily-getfamilyname)方法，以抓取字型系列名稱。</span><span class="sxs-lookup"><span data-stu-id="b3842-110">The code retrieves the font family names by calling the [**FontFamily::GetFamilyName**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontfamily-getfamilyname) method of each [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) object in the array returned by [**FontCollection::GetFamilies**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilies).</span></span> <span data-ttu-id="b3842-111">在抓取系列名稱時，它們會串連以形成以逗號分隔的清單。</span><span class="sxs-lookup"><span data-stu-id="b3842-111">As the family names are retrieved, they are concatenated to form a comma-separated list.</span></span> <span data-ttu-id="b3842-112">然後， [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics)類別的 [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush))方法會在矩形中繪製以逗號分隔的清單。</span><span class="sxs-lookup"><span data-stu-id="b3842-112">Then the [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) method of the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class draws the comma-separated list in a rectangle.</span></span>


```
FontFamily   fontFamily(L"Arial");
Font         font(&fontFamily, 8, FontStyleRegular, UnitPoint);
RectF        rectF(10.0f, 10.0f, 500.0f, 500.0f);
SolidBrush   solidBrush(Color(255, 0, 0, 0));

INT          count = 0;
INT          found = 0;
WCHAR        familyName[LF_FACESIZE];  // enough space for one family name
WCHAR*       familyList = NULL;
FontFamily*  pFontFamily = NULL;

InstalledFontCollection installedFontCollection;

// How many font families are installed?
count = installedFontCollection.GetFamilyCount();

// Allocate a buffer to hold the array of FontFamily
// objects returned by GetFamilies.
pFontFamily = new FontFamily[count];

// Get the array of FontFamily objects.
installedFontCollection.GetFamilies(count, pFontFamily, &found);

// The loop below creates a large string that is a comma-separated
// list of all font family names.
// Allocate a buffer large enough to hold that string.
familyList = new WCHAR[count*(sizeof(familyName)+ 3)];
StringCchCopy(familyList, 1, L"");

for(INT j = 0; j < count; ++j)
{
   pFontFamily[j].GetFamilyName(familyName);  
   StringCchCatW(familyList, count*(sizeof(familyName)+ 3), familyName);
   StringCchCatW(familyList, count*(sizeof(familyName)+ 3), L",  ");
}

// Draw the large string (list of all families) in a rectangle.
graphics.DrawString(
   familyList, -1, &font, rectF, NULL, &solidBrush);

delete [] pFontFamily;
delete [] familyList;
            
```



<span data-ttu-id="b3842-113">下圖顯示上述程式碼的可能輸出。</span><span class="sxs-lookup"><span data-stu-id="b3842-113">The following illustration shows a possible output of the preceding code.</span></span> <span data-ttu-id="b3842-114">如果您執行程式碼，則輸出可能會不同，視您電腦上安裝的字型而定。</span><span class="sxs-lookup"><span data-stu-id="b3842-114">If you run the code, the output might be different, depending on the fonts installed on your computer.</span></span>

![視窗的螢幕擷取畫面，其中包含以逗號分隔的已安裝字型系列清單](images/fontstext6.png)

 

 



