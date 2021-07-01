---
description: EUDC 登錄機碼包含一或多個子機碼，其中包含的值定義與使用者定義字元相關聯的字型， (EUDCs) 用於指定的字碼頁。
ms.assetid: d78a1d8f-a239-4388-aa21-c162953fe355
title: EUDC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27b583c7a0bfaa67684901e8d0a4a95ac5e45658
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120703"
---
# <a name="eudc"></a><span data-ttu-id="a689a-103">EUDC</span><span class="sxs-lookup"><span data-stu-id="a689a-103">EUDC</span></span>

<span data-ttu-id="a689a-104">EUDC 登錄機碼包含一或多個子機碼，其中包含的值定義與使用者定義字元相關聯的字型， [ (EUDCs) ](end-user-defined-characters.md) 用於指定的字碼頁。</span><span class="sxs-lookup"><span data-stu-id="a689a-104">The EUDC registry key contains one or more subkeys containing values defining the fonts associated with [end-user-defined characters (EUDCs)](end-user-defined-characters.md) for a given code page.</span></span> <span data-ttu-id="a689a-105">它具有下列登錄位置：</span><span class="sxs-lookup"><span data-stu-id="a689a-105">It has the following registry location:</span></span>

<span data-ttu-id="a689a-106">HKEY \_ 目前的 \_ 使用者 \\ EUDC</span><span class="sxs-lookup"><span data-stu-id="a689a-106">HKEY\_CURRENT\_USER\\EUDC</span></span>

<span data-ttu-id="a689a-107">其格式為：</span><span class="sxs-lookup"><span data-stu-id="a689a-107">The format is:</span></span>

<span data-ttu-id="a689a-108">EUDC SystemDefaultEUDCFont = TrueTypeEUDCFontFileName TrueTypeFontTypeface = TrueTypeEUDCFontFileName</span><span class="sxs-lookup"><span data-stu-id="a689a-108">EUDC SystemDefaultEUDCFont=TrueTypeEUDCFontFileName TrueTypeFontTypeface=TrueTypeEUDCFontFileName</span></span>

<span data-ttu-id="a689a-109">其中：</span><span class="sxs-lookup"><span data-stu-id="a689a-109">where:</span></span>



| <span data-ttu-id="a689a-110">值</span><span class="sxs-lookup"><span data-stu-id="a689a-110">Value</span></span>                         | <span data-ttu-id="a689a-111">描述</span><span class="sxs-lookup"><span data-stu-id="a689a-111">Description</span></span>                                                                                                                                         |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a689a-112">SystemDefaultEUDCFont</span><span class="sxs-lookup"><span data-stu-id="a689a-112">SystemDefaultEUDCFont</span></span>    | <span data-ttu-id="a689a-113">預先定義的名稱，用來設定系統預設字型。</span><span class="sxs-lookup"><span data-stu-id="a689a-113">Predefined name used to set the system default font.</span></span> <span data-ttu-id="a689a-114">除非明確指定此專案，否則不會有系統預設的 EUDC 字型。</span><span class="sxs-lookup"><span data-stu-id="a689a-114">There is no system default EUDC font unless this entry is explicitly specified.</span></span>     |
| <span data-ttu-id="a689a-115">TrueTypeFontTypeface</span><span class="sxs-lookup"><span data-stu-id="a689a-115">TrueTypeFontTypeface</span></span>     | <span data-ttu-id="a689a-116">與非 EUDC TrueType 字型相關聯的使用者定義名稱。</span><span class="sxs-lookup"><span data-stu-id="a689a-116">User-defined name associated with a non-EUDC TrueType font.</span></span>                                                                              |
| <span data-ttu-id="a689a-117">TrueTypeEUDCFontFileName</span><span class="sxs-lookup"><span data-stu-id="a689a-117">TrueTypeEUDCFontFileName</span></span> | <span data-ttu-id="a689a-118">由個別的 EUDC 字型檔案的檔案名所組成的字串。</span><span class="sxs-lookup"><span data-stu-id="a689a-118">String consisting of the file name of a separate EUDC font file.</span></span> <span data-ttu-id="a689a-119">此檔案會識別要與 TrueTypeFontTypeface 相關聯的字型。</span><span class="sxs-lookup"><span data-stu-id="a689a-119">This file identifies a font to be associated with TrueTypeFontTypeface.</span></span> |



 

<span data-ttu-id="a689a-120">下列範例會顯示字碼頁932的 EUDC 索引鍵。</span><span class="sxs-lookup"><span data-stu-id="a689a-120">The following example shows the EUDC key for code page 932.</span></span>


```C++
HKEY_CURRENT_USER\EUDC\932
SystemDefaultEUDCFont=EUDC.TTF
MS Mincho=MINEUDC.TTF
MS Gothic=GTEUDC.TTF
```



<span data-ttu-id="a689a-121">下列範例會將系統預設的 EUDC 字型設定為 ttf，並將個別的 EUDC 字型 Mineudc. ttf 和 Goteudc，分別與字型名稱 MS Ttf 和 MS Mt 產生關聯。</span><span class="sxs-lookup"><span data-stu-id="a689a-121">The following example sets the system default EUDC font to be Eudc.ttf and associates the separate EUDC fonts Mineudc.ttf and Goteudc.ttf with the font names MS Mincho and MS Gothic, respectively.</span></span>


```C++
SystemDefaultEUDCFont=EUDC.TTF
MS Mincho=MINEUDC.TTF
MS Gothic=GOTEUDC.TTF
```



<span data-ttu-id="a689a-122">當與非 Unicode 程式語言相關聯的 Windows 字碼頁 (system ACP) 符合子機碼時，GDI 子系統會查看子機碼值組，以取得字元的顯示資訊。</span><span class="sxs-lookup"><span data-stu-id="a689a-122">When the Windows code page (system ACP) associated with the language for non-Unicode programs matches the subkey, the GDI subsystem looks to the subkey value pairs to obtain display information about the character.</span></span> <span data-ttu-id="a689a-123">它會先尋找符合目前字型的名稱。</span><span class="sxs-lookup"><span data-stu-id="a689a-123">It first looks for a name matching the current font.</span></span> <span data-ttu-id="a689a-124">如果沒有，它會檢查 SystemDefaultEUDCFont 值。</span><span class="sxs-lookup"><span data-stu-id="a689a-124">If there is none, it examines the SystemDefaultEUDCFont value.</span></span> <span data-ttu-id="a689a-125">如果未定義任何值，GDI 會將字元視為未定義。</span><span class="sxs-lookup"><span data-stu-id="a689a-125">If no value is defined, GDI treats the character as undefined.</span></span>

<span data-ttu-id="a689a-126">請注意，文字本身不一定要位於 Windows 字碼頁中。</span><span class="sxs-lookup"><span data-stu-id="a689a-126">Note that the text itself does not have to be in the Windows code page.</span></span> <span data-ttu-id="a689a-127">例如，假設字碼頁的識別碼為1252，也就是英文的預設 Windows 字碼頁。</span><span class="sxs-lookup"><span data-stu-id="a689a-127">For example, assume that the code page has the identifier 1252, the default Windows code page for English.</span></span> <span data-ttu-id="a689a-128">應用程式會將 Unicode 私用區域中的單一 Unicode 程式碼點 U + E000 傳遞 (PUA) ，以進行 [**DrawText**](/windows/win32/api/winuser/nf-winuser-drawtext)。</span><span class="sxs-lookup"><span data-stu-id="a689a-128">An application passes the single Unicode code point U+E000, in the Unicode private use area (PUA), to [**DrawText**](/windows/win32/api/winuser/nf-winuser-drawtext).</span></span> <span data-ttu-id="a689a-129">在此情況下，GDI 會查看1252底下的登錄值，以取得字元顯示內容的字型資訊。</span><span class="sxs-lookup"><span data-stu-id="a689a-129">In this case, GDI looks at the registry values under 1252 to obtain the font information for the character display properties.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a689a-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="a689a-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a689a-131">EUDC 登錄專案</span><span class="sxs-lookup"><span data-stu-id="a689a-131">EUDC Registry Entries</span></span>](eudc-registry-entries.md)
</dt> <dt>

[<span data-ttu-id="a689a-132">EUDCCodeRange</span><span class="sxs-lookup"><span data-stu-id="a689a-132">EUDCCodeRange</span></span>](eudccoderange.md)
</dt> </dl>

 

 
