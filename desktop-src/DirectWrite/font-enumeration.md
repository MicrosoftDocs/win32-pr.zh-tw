---
title: 如何列舉字型
description: 本總覽將示範如何依系列名稱列舉系統字型集合中的字型。
ms.assetid: c1ec7721-2a30-4de3-b986-932f098228a6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9db05deb6b367f1392151ac8c12f2792d6e34f0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375889"
---
# <a name="how-to-enumerate-fonts"></a>如何列舉字型

本總覽將示範如何依系列名稱列舉系統字型集合中的字型。

此總覽包含下列部分：

-   [步驟1：取得系統字型集合。](#step-1-get-the-system-font-collection)
-   [步驟2：取得字型家族計數。](#step-2-get-the-font-family-count)
-   [建立 For 迴圈。](#make-a-for-loop)
    -   [步驟3：取得字型家族。](#step-3-get-the-font-family)
    -   [步驟4：取得系列名稱。](#step-4-get-the-family-names)
    -   [步驟5：尋找地區設定名稱。](#step-5-find-the-locale-name)
    -   [步驟6：取得系列名稱字串長度和字串的長度。](#step-6-get-the-length-of-the-family-name-string-length-and-the-string)
-   [結論](#conclusion)
-   [範例程式碼](#example-code)

## <a name="step-1-get-the-system-font-collection"></a>步驟1：取得系統字型集合。

使用 DirectWrite Factory 提供的 [**GetSystemFontCollection**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-getsystemfontcollection) 方法來傳回 [**IDWriteFontCollection**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection) ，其中包含其中的所有系統字型。


```C++
IDWriteFontCollection* pFontCollection = NULL;

// Get the system font collection.
if (SUCCEEDED(hr))
{
    hr = pDWriteFactory->GetSystemFontCollection(&pFontCollection);
}
```



## <a name="step-2-get-the-font-family-count"></a>步驟2：取得字型家族計數。

接下來，使用 [**IDWriteFontCollection：： GetFontFamilyCount**](/windows/win32/api/dwrite/nf-dwrite-idwritefontcollection-getfontfamilycount)從字型集合取得字型家族計數。 我們將使用這項功能，對集合中的每個字型系列執行迴圈。


```C++
UINT32 familyCount = 0;

// Get the number of font families in the collection.
if (SUCCEEDED(hr))
{
    familyCount = pFontCollection->GetFontFamilyCount();
}
```



## <a name="make-a-for-loop"></a>建立 For 迴圈。


```C++
for (UINT32 i = 0; i < familyCount; ++i)
```



現在您已有字型集合和字型計數，其餘的步驟會對每個字型系列進行迴圈，以抓取 [**IDWriteFontFamily**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfamily) 物件並進行查詢。

### <a name="step-3-get-the-font-family"></a>步驟3：取得字型家族。

使用 [**IDWriteFontCollection：： GetFontFamily**](/windows/win32/api/dwrite/nf-dwrite-idwritefontcollection-getfontfamily)取得 [**IDWriteFontFamily**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfamily)物件，並將它傳遞至目前的索引（ *i*）。


```C++
IDWriteFontFamily* pFontFamily = NULL;

// Get the font family.
if (SUCCEEDED(hr))
{
    hr = pFontCollection->GetFontFamily(i, &pFontFamily);
}
```



### <a name="step-4-get-the-family-names"></a>步驟4：取得系列名稱。

使用 [**IDWriteFontFamily：： GetFamilyNames**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfamily-getfamilynames)取得字型家族名稱。 這是 [**IDWriteLocalizedStrings**](/windows/win32/api/dwrite/nn-dwrite-idwritelocalizedstrings) 物件。 它可以有多個當地語系化版本的字型家族的系列名稱。


```C++
IDWriteLocalizedStrings* pFamilyNames = NULL;

// Get a list of localized strings for the family name.
if (SUCCEEDED(hr))
{
    hr = pFontFamily->GetFamilyNames(&pFamilyNames);
}
```



### <a name="step-5-find-the-locale-name"></a>步驟5：尋找地區設定名稱。

使用 [**IDWriteLocalizedStrings：： FindLocaleName**](/windows/win32/api/dwrite/nf-dwrite-idwritelocalizedstrings-findlocalename) 方法，取得您想要的地區設定中的字型 famliy 名稱。 在此情況下，會先抓取和要求預設地區設定。 如果沒有作用，則會要求 "en-us" 地區設定。 如果找不到其中一個指定的地區設定，則此範例只會切換回索引0，也就是第一個可用的地區設定。


```C++
UINT32 index = 0;
BOOL exists = false;

wchar_t localeName[LOCALE_NAME_MAX_LENGTH];

if (SUCCEEDED(hr))
{
    // Get the default locale for this user.
    int defaultLocaleSuccess = GetUserDefaultLocaleName(localeName, LOCALE_NAME_MAX_LENGTH);

    // If the default locale is returned, find that locale name, otherwise use "en-us".
    if (defaultLocaleSuccess)
    {
        hr = pFamilyNames->FindLocaleName(localeName, &index, &exists);
    }
    if (SUCCEEDED(hr) && !exists) // if the above find did not find a match, retry with US English
    {
        hr = pFamilyNames->FindLocaleName(L"en-us", &index, &exists);
    }
}

// If the specified locale doesn't exist, select the first on the list.
if (!exists)
    index = 0;
```



### <a name="step-6-get-the-length-of-the-family-name-string-length-and-the-string"></a>步驟6：取得系列名稱字串長度和字串的長度。

最後，使用 [**IDWriteLocalizedStrings：： GetStringLength**](/windows/win32/api/dwrite/nf-dwrite-idwritelocalizedstrings-getstringlength)來取得系列名稱字串的長度。 使用此長度來配置夠大的字串以容納名稱，然後使用 [**IDWriteLocalizedStrings：： GetString**](/windows/win32/api/dwrite/nf-dwrite-idwritelocalizedstrings-getstring)來取得字型家族名稱。


```C++
UINT32 length = 0;

// Get the string length.
if (SUCCEEDED(hr))
{
    hr = pFamilyNames->GetStringLength(index, &length);
}

// Allocate a string big enough to hold the name.
wchar_t* name = new (std::nothrow) wchar_t[length+1];
if (name == NULL)
{
    hr = E_OUTOFMEMORY;
}

// Get the family name.
if (SUCCEEDED(hr))
{
    hr = pFamilyNames->GetString(index, name, length+1);
}
```



## <a name="conclusion"></a>結論

當您在地區設定中有系列名稱或名稱之後，您可以將其列出供使用者選擇，或將其傳遞至 CreateTextFormat 以開始使用指定的字型系列來格式化文字，依此類推。

## <a name="example-code"></a>範例程式碼

若要查看此範例的完整原始碼，請參閱 [字型列舉範例](/samples/browse/?redirectedfrom=MSDN-samples)。

 

 