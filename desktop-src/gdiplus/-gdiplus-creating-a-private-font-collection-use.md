---
description: PrivateFontCollection 類別繼承自 FontCollection 抽象基類。 您可以使用 PrivateFontCollection 物件來為您的應用程式維護一組字型。
ms.assetid: ae12afcf-12cc-4c84-9aba-de56fc39437b
title: 建立私人字型集合
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df673273611ed329e933c84e6540ed984088202590dc1d1c644ccdedca2c80c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118977588"
---
# <a name="creating-a-private-font-collection"></a>建立私人字型集合

[**PrivateFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection)類別繼承自 [**FontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontcollection)抽象基類。 您可以使用 **PrivateFontCollection** 物件來為您的應用程式維護一組字型。

私用字型集合可以包含已安裝的系統字型，以及尚未安裝在電腦上的字型。 若要將字型檔案加入至私用字型集合，請呼叫 [**PrivateFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection)物件的 [**PrivateFontCollection：： AddFontFile**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-privatefontcollection-addfontfile)方法。

> [!Note]  
> 當您使用 GDI+ API 時，您絕不能讓應用程式從不受信任的來源下載任意字型。 作業系統需要較高的許可權，以確保所有已安裝的字型都受到信任。

 

[**PrivateFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection)物件的 [**FontCollection：： GetFamilies**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilies)方法會傳回 [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily)物件的陣列。 在呼叫 **FontCollection：： GetFamilies** 之前，您必須配置夠大的緩衝區來保存該陣列。 若要判斷所需的緩衝區大小，請呼叫 [**FontCollection：： GetFamilyCount**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilycount) 方法，並將傳回值乘以 **sizeof** (**FontFamily**) 。

私用字型集合中的字型系列數目不一定與已新增至集合的字型檔案數目相同。 例如，假設您將 ArialBd. tff、tff 和 TimesBd 等檔案新增至集合。 有三個檔案，但集合中只有兩個系列，因為 tff 和 TimesBd 都屬於相同的系列。

下列範例會將下列三個字型檔案新增至 [**PrivateFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection) 物件：

-   C： \\ WINNT \\ 字型 \\ Arial. tff (Arial、regular) 
-   C： \\ WINNT \\ 字型 \\ CourBI. tff (新的粗體斜體) 
-   C： \\ WINNT \\ 字型 \\ TimesBd. Tff (次 New 羅馬，bold) 

程式碼會呼叫 [**PrivateFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection)物件的 [**FontCollection：： GetFamilyCount**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilycount)方法，以判斷私用集合中的系列數目，然後呼叫 [**FontCollection：： GetFamilies**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilies)來取出 [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily)物件的陣列。

針對集合中的每個 [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) 物件，程式碼會呼叫 [**FontFamily：： IsStyleAvailable**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontfamily-isstyleavailable) 方法，以判斷是否可以使用各種樣式 (一般、粗體、斜體、粗體斜體、底線和刪除線) 。 傳遞給 **FontFamily：： IsStyleAvailable** 方法的引數是 [**FontStyle**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-fontstyle) 列舉的成員，其宣告于 Gdiplusenums .h 中。

如果有特定的系列/樣式組合可用，則會使用該家族和樣式來構成 [**字型**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font) 物件。 傳遞至 **字型** 函式的第一個引數是字型系列名稱 (不是 [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) 物件，就像 **字型** 的其他變化) 的情況一樣，最後一個引數是 [**PrivateFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection) 物件的位址。 在建立 **字型** 物件之後，會將其位址傳遞至 [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics)類別的 [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush))方法，以顯示該系列名稱以及樣式的名稱。


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



下圖顯示上述程式碼的輸出。

![視窗的螢幕擷取畫面，其中列出九個字型名稱，每個字型都示範命名字型](images/fontstext7.png)

Tff (已新增至上述程式碼範例中的私用字型集合) 是 Arial 標準樣式的字型檔。 不過請注意，程式輸出會顯示 Arial 字型系列以外的數個可用樣式。 這是因為 Windows GDI+ 可以從一般樣式中模擬粗體、斜體和粗體斜體樣式。 GDI+ 也可以從一般樣式產生底線和 strikeouts。

同樣地，GDI+ 可以從粗體字樣式或斜體樣式來模擬粗體斜體樣式。 程式輸出會顯示時間系列的粗體斜體樣式，即使 TimesBd。 tff (次新的羅馬、粗體) 是集合中的唯一時間。

下表指定 GDI+ 支援的非系統字型。



|                     | GDI | Windows 7 上的 GDI+ | Windows 8 上的 GDI+ | DirectWrite |
|---------------------|-----|-------------------|-------------------|-------------|
| .FON                | 是 | 否                | 否                | 否          |
| .FNT                | 是 | 否                | 否                | 否          |
| .TTF                | 是 | 是               | 是               | 是         |
| .使用 TrueType OTF  | 是 | 是               | 是               | 是         |
| .Adobe CFF 的 OTF | 是 | 否                | 是               | 是         |
| Adobe 類型1        | 是 | 否                | 否                | 否          |



 

 

 



