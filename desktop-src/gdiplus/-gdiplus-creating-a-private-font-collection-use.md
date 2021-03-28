---
description: PrivateFontCollection 類別繼承自 FontCollection 抽象基類。 您可以使用 PrivateFontCollection 物件來為您的應用程式維護一組字型。
ms.assetid: ae12afcf-12cc-4c84-9aba-de56fc39437b
title: 建立私人字型集合
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 084e8a2d6f79f60e0719f04fbabb778b9483bd80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192335"
---
# <a name="creating-a-private-font-collection"></a><span data-ttu-id="1ae08-104">建立私人字型集合</span><span class="sxs-lookup"><span data-stu-id="1ae08-104">Creating a Private Font Collection</span></span>

<span data-ttu-id="1ae08-105">[**PrivateFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection)類別繼承自 [**FontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontcollection)抽象基類。</span><span class="sxs-lookup"><span data-stu-id="1ae08-105">The [**PrivateFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection) class inherits from the [**FontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontcollection) abstract base class.</span></span> <span data-ttu-id="1ae08-106">您可以使用 **PrivateFontCollection** 物件來為您的應用程式維護一組字型。</span><span class="sxs-lookup"><span data-stu-id="1ae08-106">You can use a **PrivateFontCollection** object to maintain a set of fonts specifically for your application.</span></span>

<span data-ttu-id="1ae08-107">私用字型集合可以包含已安裝的系統字型，以及尚未安裝在電腦上的字型。</span><span class="sxs-lookup"><span data-stu-id="1ae08-107">A private font collection can include installed system fonts as well as fonts that have not been installed on the computer.</span></span> <span data-ttu-id="1ae08-108">若要將字型檔案加入至私用字型集合，請呼叫 [**PrivateFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection)物件的 [**PrivateFontCollection：： AddFontFile**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-privatefontcollection-addfontfile)方法。</span><span class="sxs-lookup"><span data-stu-id="1ae08-108">To add a font file to a private font collection, call the [**PrivateFontCollection::AddFontFile**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-privatefontcollection-addfontfile) method of a [**PrivateFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection) object.</span></span>

> [!Note]  
> <span data-ttu-id="1ae08-109">當您使用 GDI + API 時，您絕不能讓應用程式從不受信任的來源下載任意字型。</span><span class="sxs-lookup"><span data-stu-id="1ae08-109">When you use the GDI+ API, you must never allow your application to download arbitrary fonts from untrusted sources.</span></span> <span data-ttu-id="1ae08-110">作業系統需要較高的許可權，以確保所有已安裝的字型都受到信任。</span><span class="sxs-lookup"><span data-stu-id="1ae08-110">The operating system requires elevated privileges to assure that all installed fonts are trusted.</span></span>

 

<span data-ttu-id="1ae08-111">[**PrivateFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection)物件的 [**FontCollection：： GetFamilies**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilies)方法會傳回 [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily)物件的陣列。</span><span class="sxs-lookup"><span data-stu-id="1ae08-111">The [**FontCollection::GetFamilies**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilies) method of a [**PrivateFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection) object returns an array of [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) objects.</span></span> <span data-ttu-id="1ae08-112">在呼叫 **FontCollection：： GetFamilies** 之前，您必須配置夠大的緩衝區來保存該陣列。</span><span class="sxs-lookup"><span data-stu-id="1ae08-112">Before you call **FontCollection::GetFamilies**, you must allocate a buffer large enough to hold that array.</span></span> <span data-ttu-id="1ae08-113">若要判斷所需的緩衝區大小，請呼叫 [**FontCollection：： GetFamilyCount**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilycount) 方法，並將傳回值乘以 **sizeof** (**FontFamily**) 。</span><span class="sxs-lookup"><span data-stu-id="1ae08-113">To determine the size of the required buffer, call the [**FontCollection::GetFamilyCount**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilycount) method and multiply the return value by **sizeof**(**FontFamily**).</span></span>

<span data-ttu-id="1ae08-114">私用字型集合中的字型系列數目不一定與已新增至集合的字型檔案數目相同。</span><span class="sxs-lookup"><span data-stu-id="1ae08-114">The number of font families in a private font collection is not necessarily the same as the number of font files that have been added to the collection.</span></span> <span data-ttu-id="1ae08-115">例如，假設您將 ArialBd. tff、tff 和 TimesBd 等檔案新增至集合。</span><span class="sxs-lookup"><span data-stu-id="1ae08-115">For example, suppose you add the files ArialBd.tff, Times.tff, and TimesBd.tff to a collection.</span></span> <span data-ttu-id="1ae08-116">有三個檔案，但集合中只有兩個系列，因為 tff 和 TimesBd 都屬於相同的系列。</span><span class="sxs-lookup"><span data-stu-id="1ae08-116">There will be three files but only two families in the collection because Times.tff and TimesBd.tff belong to the same family.</span></span>

<span data-ttu-id="1ae08-117">下列範例會將下列三個字型檔案新增至 [**PrivateFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection) 物件：</span><span class="sxs-lookup"><span data-stu-id="1ae08-117">The following example adds the following three font files to a [**PrivateFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection) object:</span></span>

-   <span data-ttu-id="1ae08-118">C： \\ WINNT \\ 字型 \\ Arial. tff (Arial、regular) </span><span class="sxs-lookup"><span data-stu-id="1ae08-118">C:\\WINNT\\Fonts\\Arial.tff (Arial, regular)</span></span>
-   <span data-ttu-id="1ae08-119">C： \\ WINNT \\ 字型 \\ CourBI. tff (新的粗體斜體) </span><span class="sxs-lookup"><span data-stu-id="1ae08-119">C:\\WINNT\\Fonts\\CourBI.tff (Courier New, bold italic)</span></span>
-   <span data-ttu-id="1ae08-120">C： \\ WINNT \\ 字型 \\ TimesBd. Tff (次 New 羅馬，bold) </span><span class="sxs-lookup"><span data-stu-id="1ae08-120">C:\\WINNT\\Fonts\\TimesBd.tff (Times New Roman, bold)</span></span>

<span data-ttu-id="1ae08-121">程式碼會呼叫 [**PrivateFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection)物件的 [**FontCollection：： GetFamilyCount**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilycount)方法，以判斷私用集合中的系列數目，然後呼叫 [**FontCollection：： GetFamilies**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilies)來取出 [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily)物件的陣列。</span><span class="sxs-lookup"><span data-stu-id="1ae08-121">The code calls the [**FontCollection::GetFamilyCount**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilycount) method of the [**PrivateFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection) object to determine the number of families in the private collection, and then calls [**FontCollection::GetFamilies**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilies) to retrieve an array of [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) objects.</span></span>

<span data-ttu-id="1ae08-122">針對集合中的每個 [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) 物件，程式碼會呼叫 [**FontFamily：： IsStyleAvailable**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontfamily-isstyleavailable) 方法，以判斷是否可以使用各種樣式 (一般、粗體、斜體、粗體斜體、底線和刪除線) 。</span><span class="sxs-lookup"><span data-stu-id="1ae08-122">For each [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) object in the collection, the code calls the [**FontFamily::IsStyleAvailable**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontfamily-isstyleavailable) method to determine whether various styles (regular, bold, italic, bold italic, underline, and strikeout) are available.</span></span> <span data-ttu-id="1ae08-123">傳遞給 **FontFamily：： IsStyleAvailable** 方法的引數是 [**FontStyle**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-fontstyle) 列舉的成員，其宣告于 Gdiplusenums .h 中。</span><span class="sxs-lookup"><span data-stu-id="1ae08-123">The arguments passed to the **FontFamily::IsStyleAvailable** method are members of the [**FontStyle**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-fontstyle) enumeration, which is declared in Gdiplusenums.h.</span></span>

<span data-ttu-id="1ae08-124">如果有特定的系列/樣式組合可用，則會使用該家族和樣式來構成 [**字型**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font) 物件。</span><span class="sxs-lookup"><span data-stu-id="1ae08-124">If a particular family/style combination is available, a [**Font**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font) object is constructed using that family and style.</span></span> <span data-ttu-id="1ae08-125">傳遞至 **字型** 函式的第一個引數是字型系列名稱 (不是 [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) 物件，就像 **字型** 的其他變化) 的情況一樣，最後一個引數是 [**PrivateFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection) 物件的位址。</span><span class="sxs-lookup"><span data-stu-id="1ae08-125">The first argument passed to the **Font** constructor is the font family name (not a [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) object as is the case for other variations of the **Font** constructor), and the final argument is the address of the [**PrivateFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection) object.</span></span> <span data-ttu-id="1ae08-126">在建立 **字型** 物件之後，會將其位址傳遞至 [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics)類別的 [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush))方法，以顯示該系列名稱以及樣式的名稱。</span><span class="sxs-lookup"><span data-stu-id="1ae08-126">After the **Font** object is constructed, its address is passed to the [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) method of the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class to display the family name along with the name of the style.</span></span>


```
#define MAX_STYLE_SIZE 20
#define MAX_FACEANDSTYLE_SIZE (LF_FACESIZE + MAX_STYLE_SIZE + 2)

PointF      pointF(10.0f, 0.0f);
SolidBrush  solidBrush(Color(255, 0, 0, 0));
INT                   count = 0;
INT                   found = 0;
WCHAR                 familyName[LF_FACESIZE];
WCHAR                 familyNameAndStyle[MAX_FACEANDSTYLE_SIZE]; 
FontFamily*           pFontFamily;
PrivateFontCollection privateFontCollection;

// Add three font files to the private collection.
privateFontCollection.AddFontFile(L"c:\\Winnt\\Fonts\\Arial.ttf");
privateFontCollection.AddFontFile(L"c:\\Winnt\\Fonts\\CourBI.ttf");
privateFontCollection.AddFontFile(L"c:\\Winnt\\Fonts\\TimesBd.ttf");

// How many font families are in the private collection?
count = privateFontCollection.GetFamilyCount();

// Allocate a buffer to hold the array of FontFamily
// objects returned by GetFamilies.
pFontFamily = new FontFamily[count];

// Get the array of FontFamily objects.
privateFontCollection.GetFamilies(count, pFontFamily, &found);

// Display the name of each font family in the private collection
// along with the available styles for that font family.
for(INT j = 0; j < count; ++j)
{
   // Get the font family name.
   pFontFamily[j].GetFamilyName(familyName);
   
   // Is the regular style available?
   if(pFontFamily[j].IsStyleAvailable(FontStyleRegular))
   {
      StringCchCopyW(familyNameAndStyle, LF_FACESIZE, familyName);
      StringCchCatW(familyNameAndStyle, MAX_FACEANDSTYLE_SIZE, L" Regular");

      Font* pFont = new Font(
         familyName, 16, FontStyleRegular, UnitPixel, &privateFontCollection);

      graphics.DrawString(familyNameAndStyle, -1, pFont, pointF, &solidBrush);

      pointF.Y += pFont->GetHeight(0.0f);
      delete(pFont);      
   }

   // Is the bold style available?
   if(pFontFamily[j].IsStyleAvailable(FontStyleBold))
   {
      StringCchCopyW(familyNameAndStyle, LF_FACESIZE, familyName);
      StringCchCatW(familyNameAndStyle, MAX_FACEANDSTYLE_SIZE, L" Bold");

      Font* pFont = new Font(
         familyName, 16, FontStyleBold, UnitPixel, &privateFontCollection);

      graphics.DrawString(familyNameAndStyle, -1, pFont, pointF, &solidBrush);

      pointF.Y += pFont->GetHeight(0.0f);
      delete(pFont);
   }

   // Is the italic style available?
   if(pFontFamily[j].IsStyleAvailable(FontStyleItalic))
   {
      StringCchCopyW(familyNameAndStyle, LF_FACESIZE, familyName);
      StringCchCatW(familyNameAndStyle, MAX_FACEANDSTYLE_SIZE, L" Italic");

      Font* pFont = new Font(
         familyName, 16, FontStyleItalic, UnitPixel, &privateFontCollection);

      graphics.DrawString(familyNameAndStyle, -1, pFont, pointF, &solidBrush);

      pointF.Y += pFont->GetHeight(0.0f);
      delete(pFont);
   }

   // Is the bold italic style available?
   if(pFontFamily[j].IsStyleAvailable(FontStyleBoldItalic))
   {
      StringCchCopyW(familyNameAndStyle, LF_FACESIZE, familyName);
      StringCchCatW(familyNameAndStyle, MAX_FACEANDSTYLE_SIZE, L" BoldItalic");

      Font* pFont = new Font(familyName, 16, 
         FontStyleBoldItalic, UnitPixel, &privateFontCollection);

      graphics.DrawString(familyNameAndStyle, -1, pFont, pointF, &solidBrush);

      pointF.Y += pFont->GetHeight(0.0f);
      delete(pFont);
    }

   // Is the underline style available?
   if(pFontFamily[j].IsStyleAvailable(FontStyleUnderline))
   {
      StringCchCopyW(familyNameAndStyle, LF_FACESIZE, familyName);
      StringCchCatW(familyNameAndStyle, MAX_FACEANDSTYLE_SIZE, L" Underline");

      Font* pFont = new Font(familyName, 16, 
         FontStyleUnderline, UnitPixel, &privateFontCollection);

      graphics.DrawString(familyNameAndStyle, -1, pFont, pointF, &solidBrush);

      pointF.Y += pFont->GetHeight(0.0);
      delete(pFont);
   }
 
   // Is the strikeout style available?
   if(pFontFamily[j].IsStyleAvailable(FontStyleStrikeout))
   {
      StringCchCopyW(familyNameAndStyle, LF_FACESIZE, familyName);
      StringCchCatW(familyNameAndStyle, MAX_FACEANDSTYLE_SIZE, L" Strikeout");

      Font* pFont = new Font(familyName, 16, 
         FontStyleStrikeout, UnitPixel, &privateFontCollection);

      graphics.DrawString(familyNameAndStyle, -1, pFont, pointF, &solidBrush);

      pointF.Y += pFont->GetHeight(0.0f);
      delete(pFont);
   }

   // Separate the families with white space.
   pointF.Y += 10.0f;

} // for

delete pFontFamily;
            
```



<span data-ttu-id="1ae08-127">下圖顯示上述程式碼的輸出。</span><span class="sxs-lookup"><span data-stu-id="1ae08-127">The following illustration shows the output of the preceding code.</span></span>

![視窗的螢幕擷取畫面，其中列出九個字型名稱，每個字型都示範命名字型](images/fontstext7.png)

<span data-ttu-id="1ae08-129">Tff (已新增至上述程式碼範例中的私用字型集合) 是 Arial 標準樣式的字型檔。</span><span class="sxs-lookup"><span data-stu-id="1ae08-129">Arial.tff (which was added to the private font collection in the preceding code example) is the font file for the Arial regular style.</span></span> <span data-ttu-id="1ae08-130">不過請注意，程式輸出會顯示 Arial 字型系列以外的數個可用樣式。</span><span class="sxs-lookup"><span data-stu-id="1ae08-130">Note, however, that the program output shows several available styles other than regular for the Arial font family.</span></span> <span data-ttu-id="1ae08-131">這是因為 Windows GDI + 可以模擬一般樣式的粗體、斜體和粗體斜體樣式。</span><span class="sxs-lookup"><span data-stu-id="1ae08-131">That is because Windows GDI+ can simulate the bold, italic, and bold italic styles from the regular style.</span></span> <span data-ttu-id="1ae08-132">GDI + 也可以從一般樣式產生底線和 strikeouts。</span><span class="sxs-lookup"><span data-stu-id="1ae08-132">GDI+ can also produce underlines and strikeouts from the regular style.</span></span>

<span data-ttu-id="1ae08-133">同樣地，GDI + 也可以從粗體字樣式或斜體樣式來模擬粗體斜體樣式。</span><span class="sxs-lookup"><span data-stu-id="1ae08-133">Similarly, GDI+ can simulate the bold italic style from either the bold style or the italic style.</span></span> <span data-ttu-id="1ae08-134">程式輸出會顯示時間系列的粗體斜體樣式，即使 TimesBd。 tff (次新的羅馬、粗體) 是集合中的唯一時間。</span><span class="sxs-lookup"><span data-stu-id="1ae08-134">The program output shows that the bold italic style is available for the Times family even though TimesBd.tff (Times New Roman, bold) is the only Times file in the collection.</span></span>

<span data-ttu-id="1ae08-135">此資料表指定 GDI + 支援的非系統字型。</span><span class="sxs-lookup"><span data-stu-id="1ae08-135">This table specifies the non-system fonts that GDI+ supports.</span></span>



|                     | <span data-ttu-id="1ae08-136">GDI</span><span class="sxs-lookup"><span data-stu-id="1ae08-136">GDI</span></span> | <span data-ttu-id="1ae08-137">Windows 7 上的 GDI +</span><span class="sxs-lookup"><span data-stu-id="1ae08-137">GDI+ on Windows 7</span></span> | <span data-ttu-id="1ae08-138">Windows 8 上的 GDI +</span><span class="sxs-lookup"><span data-stu-id="1ae08-138">GDI+ on Windows 8</span></span> | <span data-ttu-id="1ae08-139">DirectWrite</span><span class="sxs-lookup"><span data-stu-id="1ae08-139">DirectWrite</span></span> |
|---------------------|-----|-------------------|-------------------|-------------|
| <span data-ttu-id="1ae08-140">.FON</span><span class="sxs-lookup"><span data-stu-id="1ae08-140">.FON</span></span>                | <span data-ttu-id="1ae08-141">是</span><span class="sxs-lookup"><span data-stu-id="1ae08-141">yes</span></span> | <span data-ttu-id="1ae08-142">否</span><span class="sxs-lookup"><span data-stu-id="1ae08-142">no</span></span>                | <span data-ttu-id="1ae08-143">否</span><span class="sxs-lookup"><span data-stu-id="1ae08-143">no</span></span>                | <span data-ttu-id="1ae08-144">不可以</span><span class="sxs-lookup"><span data-stu-id="1ae08-144">no</span></span>          |
| <span data-ttu-id="1ae08-145">.FNT</span><span class="sxs-lookup"><span data-stu-id="1ae08-145">.FNT</span></span>                | <span data-ttu-id="1ae08-146">是</span><span class="sxs-lookup"><span data-stu-id="1ae08-146">yes</span></span> | <span data-ttu-id="1ae08-147">否</span><span class="sxs-lookup"><span data-stu-id="1ae08-147">no</span></span>                | <span data-ttu-id="1ae08-148">否</span><span class="sxs-lookup"><span data-stu-id="1ae08-148">no</span></span>                | <span data-ttu-id="1ae08-149">不可以</span><span class="sxs-lookup"><span data-stu-id="1ae08-149">no</span></span>          |
| <span data-ttu-id="1ae08-150">.TTF</span><span class="sxs-lookup"><span data-stu-id="1ae08-150">.TTF</span></span>                | <span data-ttu-id="1ae08-151">是</span><span class="sxs-lookup"><span data-stu-id="1ae08-151">yes</span></span> | <span data-ttu-id="1ae08-152">是</span><span class="sxs-lookup"><span data-stu-id="1ae08-152">yes</span></span>               | <span data-ttu-id="1ae08-153">是</span><span class="sxs-lookup"><span data-stu-id="1ae08-153">yes</span></span>               | <span data-ttu-id="1ae08-154">是</span><span class="sxs-lookup"><span data-stu-id="1ae08-154">yes</span></span>         |
| <span data-ttu-id="1ae08-155">.使用 TrueType OTF</span><span class="sxs-lookup"><span data-stu-id="1ae08-155">.OTF with TrueType</span></span>  | <span data-ttu-id="1ae08-156">是</span><span class="sxs-lookup"><span data-stu-id="1ae08-156">yes</span></span> | <span data-ttu-id="1ae08-157">是</span><span class="sxs-lookup"><span data-stu-id="1ae08-157">yes</span></span>               | <span data-ttu-id="1ae08-158">是</span><span class="sxs-lookup"><span data-stu-id="1ae08-158">yes</span></span>               | <span data-ttu-id="1ae08-159">是</span><span class="sxs-lookup"><span data-stu-id="1ae08-159">yes</span></span>         |
| <span data-ttu-id="1ae08-160">.Adobe CFF 的 OTF</span><span class="sxs-lookup"><span data-stu-id="1ae08-160">.OTF with Adobe CFF</span></span> | <span data-ttu-id="1ae08-161">是</span><span class="sxs-lookup"><span data-stu-id="1ae08-161">yes</span></span> | <span data-ttu-id="1ae08-162">不可以</span><span class="sxs-lookup"><span data-stu-id="1ae08-162">no</span></span>                | <span data-ttu-id="1ae08-163">是</span><span class="sxs-lookup"><span data-stu-id="1ae08-163">yes</span></span>               | <span data-ttu-id="1ae08-164">是</span><span class="sxs-lookup"><span data-stu-id="1ae08-164">yes</span></span>         |
| <span data-ttu-id="1ae08-165">Adobe 類型1</span><span class="sxs-lookup"><span data-stu-id="1ae08-165">Adobe Type 1</span></span>        | <span data-ttu-id="1ae08-166">是</span><span class="sxs-lookup"><span data-stu-id="1ae08-166">yes</span></span> | <span data-ttu-id="1ae08-167">否</span><span class="sxs-lookup"><span data-stu-id="1ae08-167">no</span></span>                | <span data-ttu-id="1ae08-168">否</span><span class="sxs-lookup"><span data-stu-id="1ae08-168">no</span></span>                | <span data-ttu-id="1ae08-169">不可以</span><span class="sxs-lookup"><span data-stu-id="1ae08-169">no</span></span>          |



 

 

 



