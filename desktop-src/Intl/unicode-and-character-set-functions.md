---
description: 下列函式會與字元集一起使用。
ms.assetid: 1799f5da-1391-4b6e-ac13-718017a77557
title: Unicode 和字元集函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6996139d8a9bb426c21a460ac2bcb1358e6c8e7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027291"
---
# <a name="unicode-and-character-set-functions"></a><span data-ttu-id="46bef-103">Unicode 和字元集函數</span><span class="sxs-lookup"><span data-stu-id="46bef-103">Unicode and Character Set Functions</span></span>

<span data-ttu-id="46bef-104">下列函式會與字元集一起使用。</span><span class="sxs-lookup"><span data-stu-id="46bef-104">The following functions are used with character sets.</span></span>



| <span data-ttu-id="46bef-105">函式</span><span class="sxs-lookup"><span data-stu-id="46bef-105">Function</span></span>                                                       | <span data-ttu-id="46bef-106">描述</span><span class="sxs-lookup"><span data-stu-id="46bef-106">Description</span></span>                                                                                                           |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="46bef-107">**GetTextCharset**</span><span class="sxs-lookup"><span data-stu-id="46bef-107">**GetTextCharset**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-gettextcharset)                       | <span data-ttu-id="46bef-108">針對目前在指定的裝置內容中選取的字型抓取字元集識別碼。</span><span class="sxs-lookup"><span data-stu-id="46bef-108">Retrieves a character set identifier for the font that is currently selected into a specified device context.</span></span>         |
| [<span data-ttu-id="46bef-109">**GetTextCharsetInfo**</span><span class="sxs-lookup"><span data-stu-id="46bef-109">**GetTextCharsetInfo**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-gettextcharsetinfo)               | <span data-ttu-id="46bef-110">抓取目前在指定的裝置內容中，所選字型字元集的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="46bef-110">Retrieves information about the character set of the font that is currently selected into a specified device context.</span></span> |
| [<span data-ttu-id="46bef-111">**IsDBCSLeadByte**</span><span class="sxs-lookup"><span data-stu-id="46bef-111">**IsDBCSLeadByte**</span></span>](/windows/desktop/api/Winnls/nf-winnls-isdbcsleadbyte)                       | <span data-ttu-id="46bef-112">判斷指定的字元是否為系統預設 Windows ANSI 字碼頁的前導位元組 (CP \_ ACP) 。</span><span class="sxs-lookup"><span data-stu-id="46bef-112">Determines if a specified character is a lead byte for the system default Windows ANSI code page (CP\_ACP).</span></span>           |
| [<span data-ttu-id="46bef-113">**IsDBCSLeadByteEx**</span><span class="sxs-lookup"><span data-stu-id="46bef-113">**IsDBCSLeadByteEx**</span></span>](/windows/desktop/api/Winnls/nf-winnls-isdbcsleadbyteex)                   | <span data-ttu-id="46bef-114">判斷指定的字元是否可能是前導位元組。</span><span class="sxs-lookup"><span data-stu-id="46bef-114">Determines if a specified character is potentially a lead byte.</span></span>                                                       |
| [<span data-ttu-id="46bef-115">**IsTextUnicode**</span><span class="sxs-lookup"><span data-stu-id="46bef-115">**IsTextUnicode**</span></span>](/windows/desktop/api/Winbase/nf-winbase-istextunicode)                         | <span data-ttu-id="46bef-116">判斷緩衝區是否可能包含 Unicode 文字的格式。</span><span class="sxs-lookup"><span data-stu-id="46bef-116">Determines if a buffer is likely to contain a form of Unicode text.</span></span>                                                   |
| [<span data-ttu-id="46bef-117">**MultiByteToWideChar**</span><span class="sxs-lookup"><span data-stu-id="46bef-117">**MultiByteToWideChar**</span></span>](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar)             | <span data-ttu-id="46bef-118">將字元字串對應至 UTF-16 (寬字元) 字串。</span><span class="sxs-lookup"><span data-stu-id="46bef-118">Maps a character string to a UTF-16 (wide character) string.</span></span>                                                          |
| [<span data-ttu-id="46bef-119">**TranslateCharsetInfo**</span><span class="sxs-lookup"><span data-stu-id="46bef-119">**TranslateCharsetInfo**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-translatecharsetinfo)           | <span data-ttu-id="46bef-120">轉譯字元集資訊，並將目的結構的所有成員設定為適當的值。</span><span class="sxs-lookup"><span data-stu-id="46bef-120">Translates character set information and sets all members of a destination structure to appropriate values.</span></span>           |
| [<span data-ttu-id="46bef-121">**WideCharToMultiByte**</span><span class="sxs-lookup"><span data-stu-id="46bef-121">**WideCharToMultiByte**</span></span>](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte)             | <span data-ttu-id="46bef-122">將 UTF-16 (寬字元) 字串對應至新的字元字串。</span><span class="sxs-lookup"><span data-stu-id="46bef-122">Maps a UTF-16 (wide character) string to a new character string.</span></span>                                                      |
| <span data-ttu-id="46bef-123">[**BytesToUnicode**](/previous-versions/dd317724(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="46bef-123">[**BytesToUnicode**](/previous-versions/dd317724(v=vs.85))</span></span>                       | <span data-ttu-id="46bef-124">請勿使用。</span><span class="sxs-lookup"><span data-stu-id="46bef-124">Do not use.</span></span>                                                                                                           |
| [<span data-ttu-id="46bef-125">**NlsDllCodePageTranslation**</span><span class="sxs-lookup"><span data-stu-id="46bef-125">**NlsDllCodePageTranslation**</span></span>](/windows/desktop/api/Gb18030/nf-gb18030-nlsdllcodepagetranslation) | <span data-ttu-id="46bef-126">請勿使用。</span><span class="sxs-lookup"><span data-stu-id="46bef-126">Do not use.</span></span>                                                                                                           |
| <span data-ttu-id="46bef-127">[**UnicodeToBytes**](/previous-versions/windows/desktop/legacy/dd374082(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="46bef-127">[**UnicodeToBytes**](/previous-versions/windows/desktop/legacy/dd374082(v=vs.85))</span></span>                       | <span data-ttu-id="46bef-128">請勿使用。</span><span class="sxs-lookup"><span data-stu-id="46bef-128">Do not use.</span></span>                                                                                                           |



 

 

 
