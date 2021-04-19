---
description: 定義4位元組陣列，其中包含 4 8 位的空格、a-z 或 a-z 的 ASCII 值，以識別 OpenType 腳本、語言和字型功能標記。
ms.assetid: 188ad9a1-e0eb-411f-b6df-8c394d122d6f
title: 'OPENTYPE_TAG (Usp10) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf973c03f26bdb8f8b3799e1780fed5075d315cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106992432"
---
# <a name="opentype_tag"></a><span data-ttu-id="646bd-103">OPENTYPE \_ 標記</span><span class="sxs-lookup"><span data-stu-id="646bd-103">OPENTYPE\_TAG</span></span>

<span data-ttu-id="646bd-104">定義4位元組陣列，其中包含 4 8 位的空格、a-z 或 a-z 的 ASCII 值，以識別 OpenType 腳本、語言和字型功能標記。</span><span class="sxs-lookup"><span data-stu-id="646bd-104">Defines a 4-byte array that contains four 8-bit ASCII values of space, A-Z, or a-z to identify OpenType script, language, and font feature tags.</span></span>


```C++
typedef ULONG OPENTYPE_TAG;
```



## <a name="remarks"></a><span data-ttu-id="646bd-105">備註</span><span class="sxs-lookup"><span data-stu-id="646bd-105">Remarks</span></span>

<span data-ttu-id="646bd-106">下列範例會定義 OpenType 功能標記的標記法。</span><span class="sxs-lookup"><span data-stu-id="646bd-106">The following examples define representations of OpenType feature tags.</span></span>

-   <span data-ttu-id="646bd-107">連字功能的功能標記為 "liga"。</span><span class="sxs-lookup"><span data-stu-id="646bd-107">The feature tag for the ligature feature is "liga".</span></span>
-   <span data-ttu-id="646bd-108">適用于羅馬尼亞文、烏爾即文和波斯文的語言標記分別為「ROM」、「URD」和「遠」。</span><span class="sxs-lookup"><span data-stu-id="646bd-108">The language tags for Romanian, Urdu, and Persian are "ROM ", "URD ", and "FAR ", respectively.</span></span> <span data-ttu-id="646bd-109">請注意，每個標記的結尾都是空格。</span><span class="sxs-lookup"><span data-stu-id="646bd-109">Note that each of these tags ends with a space.</span></span>
-   <span data-ttu-id="646bd-110">拉丁和阿拉伯文腳本的腳本標記分別為 "latn" 和 "阿拉伯"。</span><span class="sxs-lookup"><span data-stu-id="646bd-110">The script tags for Latin and Arabic scripts are "latn" and "arab", respectively.</span></span>

<span data-ttu-id="646bd-111">如需 OpenType 功能標記和 OpenType 規格的詳細資訊，請參閱 <https://www.microsoft.com/typography/otspec/featuretags.htm> 。</span><span class="sxs-lookup"><span data-stu-id="646bd-111">For more information on OpenType feature tags and the OpenType specification, see <https://www.microsoft.com/typography/otspec/featuretags.htm>.</span></span>

## <a name="requirements"></a><span data-ttu-id="646bd-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="646bd-112">Requirements</span></span>



| <span data-ttu-id="646bd-113">需求</span><span class="sxs-lookup"><span data-stu-id="646bd-113">Requirement</span></span> | <span data-ttu-id="646bd-114">值</span><span class="sxs-lookup"><span data-stu-id="646bd-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="646bd-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="646bd-115">Minimum supported client</span></span><br/> | <span data-ttu-id="646bd-116">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="646bd-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="646bd-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="646bd-117">Minimum supported server</span></span><br/> | <span data-ttu-id="646bd-118">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="646bd-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="646bd-119">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="646bd-119">Redistributable</span></span><br/>          | <span data-ttu-id="646bd-120">Usp10.dll 1.600 版或更高版本的于 windows 展開 x) </span><span class="sxs-lookup"><span data-stu-id="646bd-120">Usp10.dll version 1.600 or greater onWindows XPand later</span></span><br/>                |
| <span data-ttu-id="646bd-121">標頭</span><span class="sxs-lookup"><span data-stu-id="646bd-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="646bd-122"><dt>Usp10。h</dt></span><span class="sxs-lookup"><span data-stu-id="646bd-122"><dt>Usp10.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="646bd-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="646bd-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="646bd-124">Uniscribe</span><span class="sxs-lookup"><span data-stu-id="646bd-124">Uniscribe</span></span>](uniscribe.md)
</dt> <dt>

[<span data-ttu-id="646bd-125">Uniscribe 結構</span><span class="sxs-lookup"><span data-stu-id="646bd-125">Uniscribe Structures</span></span>](uniscribe-structures.md)
</dt> <dt>

[<span data-ttu-id="646bd-126">**ScriptGetFontAlternateGlyphs**</span><span class="sxs-lookup"><span data-stu-id="646bd-126">**ScriptGetFontAlternateGlyphs**</span></span>](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontalternateglyphs)
</dt> <dt>

[<span data-ttu-id="646bd-127">**ScriptGetFontFeatureTags**</span><span class="sxs-lookup"><span data-stu-id="646bd-127">**ScriptGetFontFeatureTags**</span></span>](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontfeaturetags)
</dt> <dt>

[<span data-ttu-id="646bd-128">**ScriptGetFontLanguageTags**</span><span class="sxs-lookup"><span data-stu-id="646bd-128">**ScriptGetFontLanguageTags**</span></span>](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontlanguagetags)
</dt> <dt>

[<span data-ttu-id="646bd-129">**ScriptGetFontScriptTags**</span><span class="sxs-lookup"><span data-stu-id="646bd-129">**ScriptGetFontScriptTags**</span></span>](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontscripttags)
</dt> <dt>

[<span data-ttu-id="646bd-130">**ScriptItemizeOpenType**</span><span class="sxs-lookup"><span data-stu-id="646bd-130">**ScriptItemizeOpenType**</span></span>](/windows/desktop/api/usp10/nf-usp10-scriptitemizeopentype)
</dt> <dt>

[<span data-ttu-id="646bd-131">**ScriptPlaceOpenType**</span><span class="sxs-lookup"><span data-stu-id="646bd-131">**ScriptPlaceOpenType**</span></span>](/windows/desktop/api/Usp10/nf-usp10-scriptplaceopentype)
</dt> <dt>

[<span data-ttu-id="646bd-132">**ScriptPositionSingleGlyph**</span><span class="sxs-lookup"><span data-stu-id="646bd-132">**ScriptPositionSingleGlyph**</span></span>](/windows/desktop/api/Usp10/nf-usp10-scriptpositionsingleglyph)
</dt> <dt>

[<span data-ttu-id="646bd-133">**ScriptShapeOpenType**</span><span class="sxs-lookup"><span data-stu-id="646bd-133">**ScriptShapeOpenType**</span></span>](/windows/desktop/api/Usp10/nf-usp10-scriptshapeopentype)
</dt> <dt>

[<span data-ttu-id="646bd-134">**ScriptSubstituteSingleGlyph**</span><span class="sxs-lookup"><span data-stu-id="646bd-134">**ScriptSubstituteSingleGlyph**</span></span>](/windows/desktop/api/Usp10/nf-usp10-scriptsubstitutesingleglyph)
</dt> </dl>

 

 




