---
description: 以 Unicode 為基礎的 OpenType 字型格式可延伸 TrueType 字型檔案格式。
ms.assetid: 0d67481a-79ff-448c-b77c-a55bf935a22a
title: OpenType 字型格式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a907f0a0480c92a35b299540e3bed240ebc3b6b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988457"
---
# <a name="opentype-font-format"></a><span data-ttu-id="c1fef-103">OpenType 字型格式</span><span class="sxs-lookup"><span data-stu-id="c1fef-103">OpenType Font Format</span></span>

<span data-ttu-id="c1fef-104">以 Unicode 為基礎的 OpenType 字型格式可延伸 TrueType 字型檔案格式。</span><span class="sxs-lookup"><span data-stu-id="c1fef-104">The Unicode-based OpenType font format extends the TrueType font file format.</span></span> <span data-ttu-id="c1fef-105">OpenType [字型](uniscribe-glossary.md)允許在字元和字元之間進行對應，以支援連字號、位置形式、替代項和其他替代。</span><span class="sxs-lookup"><span data-stu-id="c1fef-105">OpenType fonts allow mapping between characters and [glyphs](uniscribe-glossary.md), enabling support for ligatures, positional forms, alternates, and other substitutions.</span></span> <span data-ttu-id="c1fef-106">OpenType 字型也可以包含支援二維圖像定位和圖像附件的資訊，而且可以包含 TrueType 或 PostScript 大綱。</span><span class="sxs-lookup"><span data-stu-id="c1fef-106">OpenType fonts can also include information that supports two-dimensional glyph positioning and glyph attachment, and can contain either TrueType or PostScript outlines.</span></span>

<span data-ttu-id="c1fef-107">OpenType 字型內的版面配置功能是依腳本和語言來組織，允許單一字型支援多個書寫系統，即使在同一個腳本內也一樣。</span><span class="sxs-lookup"><span data-stu-id="c1fef-107">Layout features within OpenType fonts are organized by scripts and languages, allowing a single font to support multiple writing systems, even within the same script.</span></span> <span data-ttu-id="c1fef-108">為了確保文字版面配置作業的一致性，並避免字型檔案或應用程式中不必要的額外負荷，Uniscribe 中包含許多文字配置和語言語義演算法。</span><span class="sxs-lookup"><span data-stu-id="c1fef-108">To ensure consistency in text layout operations and to avoid unnecessary overhead in font files or applications, many of the text layout and language semantic algorithms are included in Uniscribe.</span></span> <span data-ttu-id="c1fef-109">如此一來，字型開發人員就不需要在字型內定義一般化腳本規則。</span><span class="sxs-lookup"><span data-stu-id="c1fef-109">This relieves the font developer from having to define generalized script rules within a font.</span></span>

<span data-ttu-id="c1fef-110">應用程式可能會引入有關腳本配置的特定知識或喜好設定。</span><span class="sxs-lookup"><span data-stu-id="c1fef-110">Applications can introduce specific knowledge or preferences regarding script layout.</span></span> <span data-ttu-id="c1fef-111">OpenType 版面配置字型甚至可能包含複製或取代作業系統服務所套用的配置規則。</span><span class="sxs-lookup"><span data-stu-id="c1fef-111">OpenType layout fonts might even contain layout rules that duplicate or supersede those applied by operating system services.</span></span> <span data-ttu-id="c1fef-112">支援文字配置之作業系統服務的分層結構，可讓應用程式選擇要使用的配置資訊，然後選取要套用的版面配置資訊。</span><span class="sxs-lookup"><span data-stu-id="c1fef-112">The layered structure of operating system services supporting text layout allows an application to choose the layout information to use, and select how to apply it.</span></span> <span data-ttu-id="c1fef-113">如需詳細資訊，請參閱 [Microsoft 印刷樣式規格總覽](https://www.microsoft.com/typography/SpecificationsOverview.mspx) 或 [OpenType 規格](https://www.microsoft.com/typography/otspec/)。</span><span class="sxs-lookup"><span data-stu-id="c1fef-113">For additional information, see the [Microsoft Typography Specifications overview](https://www.microsoft.com/typography/SpecificationsOverview.mspx) or the [OpenType Specification](https://www.microsoft.com/typography/otspec/).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c1fef-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="c1fef-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c1fef-115">關於 Uniscribe</span><span class="sxs-lookup"><span data-stu-id="c1fef-115">About Uniscribe</span></span>](about-uniscribe.md)
</dt> </dl>

 

 



