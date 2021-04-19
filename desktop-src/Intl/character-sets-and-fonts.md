---
description: Windows 允許將雙位元組字元集中非標準字元的本機定義 (Dbcs) 和 Unicode。
ms.assetid: 32d0ddab-4b3f-473e-bf92-3230b3746079
title: 字元集和字型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43dbf3dae2875ec6d714419bb45411f3208bfe5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972025"
---
# <a name="character-sets-and-fonts"></a><span data-ttu-id="af501-103">字元集和字型</span><span class="sxs-lookup"><span data-stu-id="af501-103">Character Sets and Fonts</span></span>

<span data-ttu-id="af501-104">Windows 允許 [將雙位元組字元集](double-byte-character-sets.md) 中非標準字元的本機定義 (dbcs) 和 [Unicode](unicode.md)。</span><span class="sxs-lookup"><span data-stu-id="af501-104">Windows allows for local definition of nonstandard characters in both [double-byte character sets](double-byte-character-sets.md) (DBCSs) and [Unicode](unicode.md).</span></span> <span data-ttu-id="af501-105">若為 DBCS，這些非標準的字元稱為 (EUDC) 的使用者定義字元。</span><span class="sxs-lookup"><span data-stu-id="af501-105">For a DBCS, these nonstandard characters are known as end-user-defined characters (EUDC).</span></span> <span data-ttu-id="af501-106">Unicode 透過其私用區域 (PUA) 提供類似的功能。</span><span class="sxs-lookup"><span data-stu-id="af501-106">Unicode provides a similar capability through its private use area (PUA).</span></span> <span data-ttu-id="af501-107">應用程式會使用關聯的 DBCS 或 Unicode 字元值來識別指定的字元。</span><span class="sxs-lookup"><span data-stu-id="af501-107">Applications identify a specified character by using the associated DBCS or Unicode character value.</span></span>

<span data-ttu-id="af501-108">可以指派的 DBCS 字元值取決於指定的字元集。</span><span class="sxs-lookup"><span data-stu-id="af501-108">The DBCS character values that can be assigned depend on the specified character set.</span></span> <span data-ttu-id="af501-109">每個東亞 Windows [字碼頁](code-pages.md) 都至少有一個保留值範圍可作為 EUDCs 使用。</span><span class="sxs-lookup"><span data-stu-id="af501-109">Each East Asian Windows [code page](code-pages.md) has at least one range of reserved values for use as EUDCs.</span></span> <span data-ttu-id="af501-110">範圍是由 [EUDCCodeRange](eudccoderange.md) 登錄機碼定義。</span><span class="sxs-lookup"><span data-stu-id="af501-110">The ranges are defined by the [EUDCCodeRange](eudccoderange.md) registry key.</span></span> <span data-ttu-id="af501-111">此用途的 unicode 值一律來自 Unicode PUA、值 U + E000 至 U + F8FF、U + F0000 至 U + FFFFD，以及 U + 100000 至 U + 10FFFD。</span><span class="sxs-lookup"><span data-stu-id="af501-111">Unicode values for this purpose always come from the Unicode PUA, values U+E000 to U+F8FF, U+F0000 to U+FFFFD, and U+100000 to U+10FFFD.</span></span>

<span data-ttu-id="af501-112">若要建立 EUDC 或 PUA 字元，使用者可選擇指定範圍內的字元值，並 [將該字元加入至對應](uniscribe-glossary.md) 至該字元值之專案中的字型。</span><span class="sxs-lookup"><span data-stu-id="af501-112">To create an EUDC or PUA character, the user chooses a character value that is within the specified range and adds the [glyph](uniscribe-glossary.md) to the font in the entry that corresponds to that character value.</span></span> <span data-ttu-id="af501-113">使用者會使用 EUDC 編輯器或使用從字型廠商購買的字型套件來建立圖像。</span><span class="sxs-lookup"><span data-stu-id="af501-113">The user creates the glyph using an EUDC editor or using a font package purchased from a font vendor.</span></span> <span data-ttu-id="af501-114">任何 DBCS 字型都可以包含 EUDCs，而且任何 Unicode 字型都可以包含 PUA 字元。</span><span class="sxs-lookup"><span data-stu-id="af501-114">Any DBCS font can contain EUDCs, and any Unicode font can contain PUA characters.</span></span> <span data-ttu-id="af501-115">如果字型只包含 EUDCs，則該字型稱為「個別」的 EUDC/PUA 字型。</span><span class="sxs-lookup"><span data-stu-id="af501-115">The font is called a "separate" EUDC/PUA font if it contains only EUDCs.</span></span> <span data-ttu-id="af501-116">如果字型包含標準字元和 EUDCs，字型就是「整合式」 EUDC/PUA 字型。</span><span class="sxs-lookup"><span data-stu-id="af501-116">The font is an "integrated" EUDC/PUA font if it contains standard characters as well as EUDCs.</span></span>

<span data-ttu-id="af501-117">系統預設的 EUDC/PUA 字型是一種字型，作業系統會自動與所有 DBCS 和 Unicode 字型產生關聯，但具有明確相關聯的 EUDC/PUA 字型字型除外。</span><span class="sxs-lookup"><span data-stu-id="af501-117">The system default EUDC/PUA font is a font that the operating system automatically associates with all DBCS and Unicode fonts, except fonts that have explicitly associated EUDC/PUA fonts.</span></span> <span data-ttu-id="af501-118">應用程式會設定「 [eudc](eudc.md) 」登錄機碼下的 SystemDefaultEUDCFont 名稱值，以設定系統預設的 EUDC/PUA 字型。</span><span class="sxs-lookup"><span data-stu-id="af501-118">Applications set the system default EUDC/PUA font by setting the value of the SystemDefaultEUDCFont name under the [EUDC](eudc.md) registry key.</span></span> <span data-ttu-id="af501-119">同樣地，應用程式可以在 EUDC 索引鍵下指定字型名稱和相關聯的字型檔案，以將個別的 EUDC/PUA 字型與對應的字型產生關聯。</span><span class="sxs-lookup"><span data-stu-id="af501-119">Similarly, applications can associate separate EUDC/PUA fonts with corresponding fonts by specifying a font name and associated font file under the EUDC key.</span></span> <span data-ttu-id="af501-120">作業系統一律會先嘗試尋找目前所選字型中的 EUDC/PUA。</span><span class="sxs-lookup"><span data-stu-id="af501-120">The operating system always first tries to find the EUDC/PUA in the currently selected font.</span></span> <span data-ttu-id="af501-121">如果找不到字型，則作業系統會尋找相關聯的 EUDC/PUA 字型中的字元（如果已定義目前所選字型的字元）。</span><span class="sxs-lookup"><span data-stu-id="af501-121">If the font is not found, the operating system looks for the character in the associated EUDC/PUA font, if one has been defined for the currently selected font.</span></span> <span data-ttu-id="af501-122">如果仍然找不到字元，則作業系統會以系統預設的 EUDC/PUA 字型來尋找它。</span><span class="sxs-lookup"><span data-stu-id="af501-122">If it still fails to find the character, the operating system looks for it in the system default EUDC/PUA font.</span></span>

<span data-ttu-id="af501-123">TrueType 字型可以安裝為 ttf 檔案或 tte 檔案。</span><span class="sxs-lookup"><span data-stu-id="af501-123">TrueType fonts can be installed either as .ttf files or as .tte files.</span></span> <span data-ttu-id="af501-124">由於作業系統會隱藏 tte 檔案，因此應用程式無法使用 GDI API 函式來列舉或檢查已安裝的字型。</span><span class="sxs-lookup"><span data-stu-id="af501-124">Since the operating system hides .tte files, applications cannot enumerate or otherwise examine the installed fonts using GDI API functions.</span></span> <span data-ttu-id="af501-125">在許多作業系統上，系統預設的 EUDC/PUA 字型和個別的 EUDC/PUA 字型會安裝為 tte 檔案。</span><span class="sxs-lookup"><span data-stu-id="af501-125">On many operating systems, the system default EUDC/PUA font and separate EUDC/PUA fonts are installed as .tte files.</span></span> <span data-ttu-id="af501-126">您必須使用登錄專案來新增、修改和刪除這類字型，像是 EUDC 編輯器和主控台的應用程式必須使用登錄專案。</span><span class="sxs-lookup"><span data-stu-id="af501-126">Applications such as EUDC editors and the Control Panel must use registry entries to add, modify, and delete such fonts.</span></span>

<span data-ttu-id="af501-127">使用 EUDC 和 PUA 字元並不會在不同的電腦或字元集之間可靠地保留意義。</span><span class="sxs-lookup"><span data-stu-id="af501-127">Use of EUDC and PUA characters does not reliably preserve meaning across different computers or character sets.</span></span> <span data-ttu-id="af501-128">如需有關使用 EUDC 和 PUA 字元的進一步警告，請參閱 [使用者定義和私用的區域字元](end-user-defined-characters.md) 。</span><span class="sxs-lookup"><span data-stu-id="af501-128">See [End-User-Defined and Private Use Area Characters](end-user-defined-characters.md) for further cautions about the use of EUDC and PUA characters.</span></span>

## <a name="related-topics"></a><span data-ttu-id="af501-129">相關主題</span><span class="sxs-lookup"><span data-stu-id="af501-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="af501-130">終端使用者定義和私用區域字元</span><span class="sxs-lookup"><span data-stu-id="af501-130">End-User-Defined and Private Use Area Characters</span></span>](end-user-defined-characters.md)
</dt> </dl>

 

 



