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
# <a name="how-to-enumerate-fonts"></a><span data-ttu-id="e808f-103">如何列舉字型</span><span class="sxs-lookup"><span data-stu-id="e808f-103">How to Enumerate Fonts</span></span>

<span data-ttu-id="e808f-104">本總覽將示範如何依系列名稱列舉系統字型集合中的字型。</span><span class="sxs-lookup"><span data-stu-id="e808f-104">This overview will show how to enumerate the fonts in the system font collection, by family name.</span></span>

<span data-ttu-id="e808f-105">此總覽包含下列部分：</span><span class="sxs-lookup"><span data-stu-id="e808f-105">This overview consists of the following parts:</span></span>

-   [<span data-ttu-id="e808f-106">步驟1：取得系統字型集合。</span><span class="sxs-lookup"><span data-stu-id="e808f-106">Step 1: Get the System Font Collection.</span></span>](#step-1-get-the-system-font-collection)
-   [<span data-ttu-id="e808f-107">步驟2：取得字型家族計數。</span><span class="sxs-lookup"><span data-stu-id="e808f-107">Step 2: Get the Font Family Count.</span></span>](#step-2-get-the-font-family-count)
-   [<span data-ttu-id="e808f-108">建立 For 迴圈。</span><span class="sxs-lookup"><span data-stu-id="e808f-108">Make a For Loop.</span></span>](#make-a-for-loop)
    -   [<span data-ttu-id="e808f-109">步驟3：取得字型家族。</span><span class="sxs-lookup"><span data-stu-id="e808f-109">Step 3: Get the Font Family.</span></span>](#step-3-get-the-font-family)
    -   [<span data-ttu-id="e808f-110">步驟4：取得系列名稱。</span><span class="sxs-lookup"><span data-stu-id="e808f-110">Step 4: Get the Family Names.</span></span>](#step-4-get-the-family-names)
    -   [<span data-ttu-id="e808f-111">步驟5：尋找地區設定名稱。</span><span class="sxs-lookup"><span data-stu-id="e808f-111">Step 5: Find the Locale Name.</span></span>](#step-5-find-the-locale-name)
    -   [<span data-ttu-id="e808f-112">步驟6：取得系列名稱字串長度和字串的長度。</span><span class="sxs-lookup"><span data-stu-id="e808f-112">Step 6: Get the Length of the Family Name String Length and the String.</span></span>](#step-6-get-the-length-of-the-family-name-string-length-and-the-string)
-   [<span data-ttu-id="e808f-113">結論</span><span class="sxs-lookup"><span data-stu-id="e808f-113">Conclusion</span></span>](#conclusion)
-   [<span data-ttu-id="e808f-114">範例程式碼</span><span class="sxs-lookup"><span data-stu-id="e808f-114">Example Code</span></span>](#example-code)

## <a name="step-1-get-the-system-font-collection"></a><span data-ttu-id="e808f-115">步驟1：取得系統字型集合。</span><span class="sxs-lookup"><span data-stu-id="e808f-115">Step 1: Get the System Font Collection.</span></span>

<span data-ttu-id="e808f-116">使用 DirectWrite Factory 提供的 [**GetSystemFontCollection**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-getsystemfontcollection) 方法來傳回 [**IDWriteFontCollection**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection) ，其中包含其中的所有系統字型。</span><span class="sxs-lookup"><span data-stu-id="e808f-116">Use the [**GetSystemFontCollection**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-getsystemfontcollection) method provided by the DirectWrite Factory to return an [**IDWriteFontCollection**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection) with all of the system fonts in it.</span></span>


```C++
IDWriteFontCollection* pFontCollection = NULL;

// Get the system font collection.
if (SUCCEEDED(hr))
{
    hr = pDWriteFactory->GetSystemFontCollection(&pFontCollection);
}
```



## <a name="step-2-get-the-font-family-count"></a><span data-ttu-id="e808f-117">步驟2：取得字型家族計數。</span><span class="sxs-lookup"><span data-stu-id="e808f-117">Step 2: Get the Font Family Count.</span></span>

<span data-ttu-id="e808f-118">接下來，使用 [**IDWriteFontCollection：： GetFontFamilyCount**](/windows/win32/api/dwrite/nf-dwrite-idwritefontcollection-getfontfamilycount)從字型集合取得字型家族計數。</span><span class="sxs-lookup"><span data-stu-id="e808f-118">Next, get the font family count from the font collection by using [**IDWriteFontCollection::GetFontFamilyCount**](/windows/win32/api/dwrite/nf-dwrite-idwritefontcollection-getfontfamilycount).</span></span> <span data-ttu-id="e808f-119">我們將使用這項功能，對集合中的每個字型系列執行迴圈。</span><span class="sxs-lookup"><span data-stu-id="e808f-119">We'll use this to loop over each font family in the collection.</span></span>


```C++
UINT32 familyCount = 0;

// Get the number of font families in the collection.
if (SUCCEEDED(hr))
{
    familyCount = pFontCollection->GetFontFamilyCount();
}
```



## <a name="make-a-for-loop"></a><span data-ttu-id="e808f-120">建立 For 迴圈。</span><span class="sxs-lookup"><span data-stu-id="e808f-120">Make a For Loop.</span></span>


```C++
for (UINT32 i = 0; i < familyCount; ++i)
```



<span data-ttu-id="e808f-121">現在您已有字型集合和字型計數，其餘的步驟會對每個字型系列進行迴圈，以抓取 [**IDWriteFontFamily**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfamily) 物件並進行查詢。</span><span class="sxs-lookup"><span data-stu-id="e808f-121">Now that you have the font collection and the font count, the remaining steps loop over each font family, retrieving the [**IDWriteFontFamily**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfamily) object and querying it.</span></span>

### <a name="step-3-get-the-font-family"></a><span data-ttu-id="e808f-122">步驟3：取得字型家族。</span><span class="sxs-lookup"><span data-stu-id="e808f-122">Step 3: Get the Font Family.</span></span>

<span data-ttu-id="e808f-123">使用 [**IDWriteFontCollection：： GetFontFamily**](/windows/win32/api/dwrite/nf-dwrite-idwritefontcollection-getfontfamily)取得 [**IDWriteFontFamily**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfamily)物件，並將它傳遞至目前的索引（ *i*）。</span><span class="sxs-lookup"><span data-stu-id="e808f-123">Get a [**IDWriteFontFamily**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfamily) object by using [**IDWriteFontCollection::GetFontFamily**](/windows/win32/api/dwrite/nf-dwrite-idwritefontcollection-getfontfamily) and passing it the current index, *i*.</span></span>


```C++
IDWriteFontFamily* pFontFamily = NULL;

// Get the font family.
if (SUCCEEDED(hr))
{
    hr = pFontCollection->GetFontFamily(i, &pFontFamily);
}
```



### <a name="step-4-get-the-family-names"></a><span data-ttu-id="e808f-124">步驟4：取得系列名稱。</span><span class="sxs-lookup"><span data-stu-id="e808f-124">Step 4: Get the Family Names.</span></span>

<span data-ttu-id="e808f-125">使用 [**IDWriteFontFamily：： GetFamilyNames**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfamily-getfamilynames)取得字型家族名稱。</span><span class="sxs-lookup"><span data-stu-id="e808f-125">Get the font family names by using the [**IDWriteFontFamily::GetFamilyNames**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfamily-getfamilynames).</span></span> <span data-ttu-id="e808f-126">這是 [**IDWriteLocalizedStrings**](/windows/win32/api/dwrite/nn-dwrite-idwritelocalizedstrings) 物件。</span><span class="sxs-lookup"><span data-stu-id="e808f-126">This is an [**IDWriteLocalizedStrings**](/windows/win32/api/dwrite/nn-dwrite-idwritelocalizedstrings) object.</span></span> <span data-ttu-id="e808f-127">它可以有多個當地語系化版本的字型家族的系列名稱。</span><span class="sxs-lookup"><span data-stu-id="e808f-127">It can have multiple localized versions of the family name for the font family.</span></span>


```C++
IDWriteLocalizedStrings* pFamilyNames = NULL;

// Get a list of localized strings for the family name.
if (SUCCEEDED(hr))
{
    hr = pFontFamily->GetFamilyNames(&pFamilyNames);
}
```



### <a name="step-5-find-the-locale-name"></a><span data-ttu-id="e808f-128">步驟5：尋找地區設定名稱。</span><span class="sxs-lookup"><span data-stu-id="e808f-128">Step 5: Find the Locale Name.</span></span>

<span data-ttu-id="e808f-129">使用 [**IDWriteLocalizedStrings：： FindLocaleName**](/windows/win32/api/dwrite/nf-dwrite-idwritelocalizedstrings-findlocalename) 方法，取得您想要的地區設定中的字型 famliy 名稱。</span><span class="sxs-lookup"><span data-stu-id="e808f-129">Get the font famliy name in the locale you want by using the [**IDWriteLocalizedStrings::FindLocaleName**](/windows/win32/api/dwrite/nf-dwrite-idwritelocalizedstrings-findlocalename) method.</span></span> <span data-ttu-id="e808f-130">在此情況下，會先抓取和要求預設地區設定。</span><span class="sxs-lookup"><span data-stu-id="e808f-130">In this case, first the default locale is retrieved and requested.</span></span> <span data-ttu-id="e808f-131">如果沒有作用，則會要求 "en-us" 地區設定。</span><span class="sxs-lookup"><span data-stu-id="e808f-131">If that does not work, the "en-us" locale is requested.</span></span> <span data-ttu-id="e808f-132">如果找不到其中一個指定的地區設定，則此範例只會切換回索引0，也就是第一個可用的地區設定。</span><span class="sxs-lookup"><span data-stu-id="e808f-132">If either of the specified locales are not found, this example simply falls back to index 0, the first available locale.</span></span>


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



### <a name="step-6-get-the-length-of-the-family-name-string-length-and-the-string"></a><span data-ttu-id="e808f-133">步驟6：取得系列名稱字串長度和字串的長度。</span><span class="sxs-lookup"><span data-stu-id="e808f-133">Step 6: Get the Length of the Family Name String Length and the String.</span></span>

<span data-ttu-id="e808f-134">最後，使用 [**IDWriteLocalizedStrings：： GetStringLength**](/windows/win32/api/dwrite/nf-dwrite-idwritelocalizedstrings-getstringlength)來取得系列名稱字串的長度。</span><span class="sxs-lookup"><span data-stu-id="e808f-134">Finally, get the length of the family name string by using [**IDWriteLocalizedStrings::GetStringLength**](/windows/win32/api/dwrite/nf-dwrite-idwritelocalizedstrings-getstringlength).</span></span> <span data-ttu-id="e808f-135">使用此長度來配置夠大的字串以容納名稱，然後使用 [**IDWriteLocalizedStrings：： GetString**](/windows/win32/api/dwrite/nf-dwrite-idwritelocalizedstrings-getstring)來取得字型家族名稱。</span><span class="sxs-lookup"><span data-stu-id="e808f-135">Use this length to allocate a string large enough to hold the name and then get the font family name by using [**IDWriteLocalizedStrings::GetString**](/windows/win32/api/dwrite/nf-dwrite-idwritelocalizedstrings-getstring).</span></span>


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



## <a name="conclusion"></a><span data-ttu-id="e808f-136">結論</span><span class="sxs-lookup"><span data-stu-id="e808f-136">Conclusion</span></span>

<span data-ttu-id="e808f-137">當您在地區設定中有系列名稱或名稱之後，您可以將其列出供使用者選擇，或將其傳遞至 CreateTextFormat 以開始使用指定的字型系列來格式化文字，依此類推。</span><span class="sxs-lookup"><span data-stu-id="e808f-137">Once you have the family name or names in the locale, you can list them for the user to choose from, or pass it to CreateTextFormat to begin formatting text with the specified font family, and so on.</span></span>

## <a name="example-code"></a><span data-ttu-id="e808f-138">範例程式碼</span><span class="sxs-lookup"><span data-stu-id="e808f-138">Example Code</span></span>

<span data-ttu-id="e808f-139">若要查看此範例的完整原始碼，請參閱 [字型列舉範例](/samples/browse/?redirectedfrom=MSDN-samples)。</span><span class="sxs-lookup"><span data-stu-id="e808f-139">To see the full source code for this example see the [Font Enumeration Sample](/samples/browse/?redirectedfrom=MSDN-samples).</span></span>

 

 