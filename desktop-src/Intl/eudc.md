---
description: EUDC 登錄機碼包含一或多個子機碼，其中包含的值定義與使用者定義字元相關聯的字型， (EUDCs) 用於指定的字碼頁。
ms.assetid: d78a1d8f-a239-4388-aa21-c162953fe355
title: EUDC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 781f7c28460c2e56f4bcdb393277f509f88a0383
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106990413"
---
# <a name="eudc"></a><span data-ttu-id="11867-103">EUDC</span><span class="sxs-lookup"><span data-stu-id="11867-103">EUDC</span></span>

<span data-ttu-id="11867-104">EUDC 登錄機碼包含一或多個子機碼，其中包含的值定義與使用者定義字元相關聯的字型， [ (EUDCs) ](end-user-defined-characters.md) 用於指定的字碼頁。</span><span class="sxs-lookup"><span data-stu-id="11867-104">The EUDC registry key contains one or more subkeys containing values defining the fonts associated with [end-user-defined characters (EUDCs)](end-user-defined-characters.md) for a given code page.</span></span> <span data-ttu-id="11867-105">它具有下列登錄位置：</span><span class="sxs-lookup"><span data-stu-id="11867-105">It has the following registry location:</span></span>

<span data-ttu-id="11867-106">HKEY \_ 目前的 \_ 使用者 \\ EUDC</span><span class="sxs-lookup"><span data-stu-id="11867-106">HKEY\_CURRENT\_USER\\EUDC</span></span>

<span data-ttu-id="11867-107">其格式為：</span><span class="sxs-lookup"><span data-stu-id="11867-107">The format is:</span></span>

<span data-ttu-id="11867-108">EUDC SystemDefaultEUDCFont = TrueTypeEUDCFontFileName TrueTypeFontTypeface = TrueTypeEUDCFontFileName</span><span class="sxs-lookup"><span data-stu-id="11867-108">EUDC SystemDefaultEUDCFont=TrueTypeEUDCFontFileName TrueTypeFontTypeface=TrueTypeEUDCFontFileName</span></span>

<span data-ttu-id="11867-109">其中：</span><span class="sxs-lookup"><span data-stu-id="11867-109">where:</span></span>



|                          |                                                                                                                                          |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11867-110">SystemDefaultEUDCFont</span><span class="sxs-lookup"><span data-stu-id="11867-110">SystemDefaultEUDCFont</span></span>    | <span data-ttu-id="11867-111">預先定義的名稱，用來設定系統預設字型。</span><span class="sxs-lookup"><span data-stu-id="11867-111">Predefined name used to set the system default font.</span></span> <span data-ttu-id="11867-112">除非明確指定此專案，否則不會有系統預設的 EUDC 字型。</span><span class="sxs-lookup"><span data-stu-id="11867-112">There is no system default EUDC font unless this entry is explicitly specified.</span></span>     |
| <span data-ttu-id="11867-113">TrueTypeFontTypeface</span><span class="sxs-lookup"><span data-stu-id="11867-113">TrueTypeFontTypeface</span></span>     | <span data-ttu-id="11867-114">與非 EUDC TrueType 字型相關聯的使用者定義名稱。</span><span class="sxs-lookup"><span data-stu-id="11867-114">User-defined name associated with a non-EUDC TrueType font.</span></span>                                                                              |
| <span data-ttu-id="11867-115">TrueTypeEUDCFontFileName</span><span class="sxs-lookup"><span data-stu-id="11867-115">TrueTypeEUDCFontFileName</span></span> | <span data-ttu-id="11867-116">由個別的 EUDC 字型檔案的檔案名所組成的字串。</span><span class="sxs-lookup"><span data-stu-id="11867-116">String consisting of the file name of a separate EUDC font file.</span></span> <span data-ttu-id="11867-117">此檔案會識別要與 TrueTypeFontTypeface 相關聯的字型。</span><span class="sxs-lookup"><span data-stu-id="11867-117">This file identifies a font to be associated with TrueTypeFontTypeface.</span></span> |



 

<span data-ttu-id="11867-118">下列範例會顯示字碼頁932的 EUDC 索引鍵。</span><span class="sxs-lookup"><span data-stu-id="11867-118">The following example shows the EUDC key for code page 932.</span></span>


```C++
HKEY_CURRENT_USER\EUDC\932
SystemDefaultEUDCFont=EUDC.TTF
MS Mincho=MINEUDC.TTF
MS Gothic=GTEUDC.TTF
```



<span data-ttu-id="11867-119">下列範例會將系統預設的 EUDC 字型設定為 ttf，並將個別的 EUDC 字型 Mineudc. ttf 和 Goteudc，分別與字型名稱 MS Ttf 和 MS Mt 產生關聯。</span><span class="sxs-lookup"><span data-stu-id="11867-119">The following example sets the system default EUDC font to be Eudc.ttf and associates the separate EUDC fonts Mineudc.ttf and Goteudc.ttf with the font names MS Mincho and MS Gothic, respectively.</span></span>


```C++
SystemDefaultEUDCFont=EUDC.TTF
MS Mincho=MINEUDC.TTF
MS Gothic=GOTEUDC.TTF
```



<span data-ttu-id="11867-120">當與非 Unicode 程式語言相關聯的 Windows 字碼頁 (system ACP) 符合子機碼時，GDI 子系統會查看子機碼值組，以取得字元的顯示資訊。</span><span class="sxs-lookup"><span data-stu-id="11867-120">When the Windows code page (system ACP) associated with the language for non-Unicode programs matches the subkey, the GDI subsystem looks to the subkey value pairs to obtain display information about the character.</span></span> <span data-ttu-id="11867-121">它會先尋找符合目前字型的名稱。</span><span class="sxs-lookup"><span data-stu-id="11867-121">It first looks for a name matching the current font.</span></span> <span data-ttu-id="11867-122">如果沒有，它會檢查 SystemDefaultEUDCFont 值。</span><span class="sxs-lookup"><span data-stu-id="11867-122">If there is none, it examines the SystemDefaultEUDCFont value.</span></span> <span data-ttu-id="11867-123">如果未定義任何值，GDI 會將字元視為未定義。</span><span class="sxs-lookup"><span data-stu-id="11867-123">If no value is defined, GDI treats the character as undefined.</span></span>

<span data-ttu-id="11867-124">請注意，文字本身不一定要位於 Windows 字碼頁中。</span><span class="sxs-lookup"><span data-stu-id="11867-124">Note that the text itself does not have to be in the Windows code page.</span></span> <span data-ttu-id="11867-125">例如，假設字碼頁的識別碼為1252，也就是英文的預設 Windows 字碼頁。</span><span class="sxs-lookup"><span data-stu-id="11867-125">For example, assume that the code page has the identifier 1252, the default Windows code page for English.</span></span> <span data-ttu-id="11867-126">應用程式會將 Unicode 私用區域中的單一 Unicode 程式碼點 U + E000 傳遞 (PUA) ，以進行 [**DrawText**](/windows/win32/api/winuser/nf-winuser-drawtext)。</span><span class="sxs-lookup"><span data-stu-id="11867-126">An application passes the single Unicode code point U+E000, in the Unicode private use area (PUA), to [**DrawText**](/windows/win32/api/winuser/nf-winuser-drawtext).</span></span> <span data-ttu-id="11867-127">在此情況下，GDI 會查看1252底下的登錄值，以取得字元顯示內容的字型資訊。</span><span class="sxs-lookup"><span data-stu-id="11867-127">In this case, GDI looks at the registry values under 1252 to obtain the font information for the character display properties.</span></span>

## <a name="related-topics"></a><span data-ttu-id="11867-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="11867-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="11867-129">EUDC 登錄專案</span><span class="sxs-lookup"><span data-stu-id="11867-129">EUDC Registry Entries</span></span>](eudc-registry-entries.md)
</dt> <dt>

[<span data-ttu-id="11867-130">EUDCCodeRange</span><span class="sxs-lookup"><span data-stu-id="11867-130">EUDCCodeRange</span></span>](eudccoderange.md)
</dt> </dl>

 

 
