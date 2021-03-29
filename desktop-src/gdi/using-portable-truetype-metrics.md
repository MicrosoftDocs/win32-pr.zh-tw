---
description: 使用 TrueType 文字度量的應用程式可達到高程度的印表機和檔可攜性;即使它們必須維持與舊版 Windows 的相容性，也可以使用 TrueType 計量。
ms.assetid: 29b54315-7c4e-4b8c-ad79-0b85c7386860
title: 使用可移植的 TrueType 計量
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83360b620bde11e20726b0ee4124d35bf6cf00b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991506"
---
# <a name="using-portable-truetype-metrics"></a><span data-ttu-id="3d67b-103">使用可移植的 TrueType 計量</span><span class="sxs-lookup"><span data-stu-id="3d67b-103">Using Portable TrueType Metrics</span></span>

<span data-ttu-id="3d67b-104">使用 TrueType 文字度量的應用程式可達到高程度的印表機和檔可攜性;即使它們必須維持與舊版 Windows 的相容性，也可以使用 TrueType 計量。</span><span class="sxs-lookup"><span data-stu-id="3d67b-104">Applications that use the TrueType text metrics can achieve a high degree of printer and document portability; they can use TrueType metrics even if they must maintain compatibility with early 16-bit versions of Windows.</span></span>

<span data-ttu-id="3d67b-105">設計寬度會克服實體裝置所引進之裝置相關文字的大部分問題。</span><span class="sxs-lookup"><span data-stu-id="3d67b-105">Design widths overcome most of the problems of device-dependent text introduced by physical devices.</span></span> <span data-ttu-id="3d67b-106">設計寬度是一種邏輯寬度。</span><span class="sxs-lookup"><span data-stu-id="3d67b-106">Design widths are a kind of logical width.</span></span> <span data-ttu-id="3d67b-107">與任何柵格化問題或縮放轉換無關，每個字元都有邏輯寬度和高度。</span><span class="sxs-lookup"><span data-stu-id="3d67b-107">Independent of any rasterization problems or scaling transformations, each glyph has a logical width and height.</span></span> <span data-ttu-id="3d67b-108">組成邏輯頁面時，字串中的每個字元都有一個與實體裝置寬度無關的位置。</span><span class="sxs-lookup"><span data-stu-id="3d67b-108">Composed to a logical page, each character in a string has a place that is independent of the physical device widths.</span></span> <span data-ttu-id="3d67b-109">雖然邏輯寬度表示寬度可在所有點大小以線性方式調整，但 nonportable 或大部分的 TrueType 字型都不一定如此。</span><span class="sxs-lookup"><span data-stu-id="3d67b-109">Although a logical width implies that widths can be scaled linearly at all point sizes, this is not necessarily true for either nonportable or most TrueType fonts.</span></span> <span data-ttu-id="3d67b-110">在較小的點大小，某些字元的高度會相對於其高度，以提供更好的可讀性。</span><span class="sxs-lookup"><span data-stu-id="3d67b-110">At smaller point sizes, some glyphs are made wider relative to their height for better readability.</span></span>

<span data-ttu-id="3d67b-111">TrueType 核心字型中的字元是針對 2048 by 2048 方格所設計。</span><span class="sxs-lookup"><span data-stu-id="3d67b-111">The characters in TrueType core fonts are designed against a 2048 by 2048 grid.</span></span> <span data-ttu-id="3d67b-112">設計寬度是以這些格線單位表示的字元寬度。</span><span class="sxs-lookup"><span data-stu-id="3d67b-112">The design width is the width of a character in these grid units.</span></span> <span data-ttu-id="3d67b-113"> (TrueType 支援的任何整數格線大小上限為16384（16384）;以2倍的整數乘冪的格線大小比其他格線大小更快。 ) </span><span class="sxs-lookup"><span data-stu-id="3d67b-113">(TrueType supports any integer grid size up to 16,384 by 16,384; grid sizes that are integer powers of 2 scale faster than other grid sizes.)</span></span>

<span data-ttu-id="3d67b-114">字型大綱是以名義單位來設計的。</span><span class="sxs-lookup"><span data-stu-id="3d67b-114">The font outline is designed in notional units.</span></span> <span data-ttu-id="3d67b-115">Em 正方形是用於調整字型外框的名義方格。</span><span class="sxs-lookup"><span data-stu-id="3d67b-115">The em square is the notional grid against which the font outline is fitted.</span></span> <span data-ttu-id="3d67b-116"> (您可以使用 [OUTLINETEXTMETRIC](/windows/desktop/api/Wingdi/ns-wingdi-outlinetextmetrica)的 **OtmEMSquare** 成員和 [NEWTEXTMETRIC](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica)的 **ntmSizeEM** 成員，以名義單位來取得 em 平方的大小。 ) 當字型建立時，如果裝置單位中有 (的點大小) 等於其 em 正方形的大小，則此字型的 ABC 寬度就是所需的設計寬度。</span><span class="sxs-lookup"><span data-stu-id="3d67b-116">(You can use the **otmEMSquare** member of [OUTLINETEXTMETRIC](/windows/desktop/api/Wingdi/ns-wingdi-outlinetextmetrica) and the **ntmSizeEM** member of [NEWTEXTMETRIC](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica) to retrieve the size of the em square in notional units.) When a font is created that has a point size (in device units) equal to the size of its em square, the ABC widths for this font are the desired design widths.</span></span> <span data-ttu-id="3d67b-117">例如，假設 em 正方形的大小為1000，而字型中字元的 ABC 寬度為150、400和150。</span><span class="sxs-lookup"><span data-stu-id="3d67b-117">For example, assume the size of an em square is 1000 and the ABC widths of a character in the font are 150, 400, and 150.</span></span> <span data-ttu-id="3d67b-118">這個字型中為10個裝置單位高的字元，會分別有1.5、4和1.5 的 ABC 寬度。</span><span class="sxs-lookup"><span data-stu-id="3d67b-118">A character in this font that is 10 device units high would have ABC widths of 1.5, 4, and 1.5, respectively.</span></span> <span data-ttu-id="3d67b-119">由於 MM \_ 文字對應模式最常用於字型 (而 mm \_ 文字相當於裝置單位) ，這是簡單的計算。</span><span class="sxs-lookup"><span data-stu-id="3d67b-119">Since the MM\_TEXT mapping mode is most commonly used with fonts (and MM\_TEXT is equivalent to device units), this is a simple calculation.</span></span>

<span data-ttu-id="3d67b-120">由於 TrueType 設計寬度的高解析度，因此使用它們的應用程式必須考慮可以建立的大型數值。</span><span class="sxs-lookup"><span data-stu-id="3d67b-120">Because of the high resolution of TrueType design widths, applications that use them must take into account the large numeric values that can be created.</span></span> <span data-ttu-id="3d67b-121">如需詳細資訊，請參閱下列主題：</span><span class="sxs-lookup"><span data-stu-id="3d67b-121">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="3d67b-122">裝置與設計單位</span><span class="sxs-lookup"><span data-stu-id="3d67b-122">Device vs. Design Units</span></span>](device-vs--design-units.md)
-   [<span data-ttu-id="3d67b-123">便攜檔的計量</span><span class="sxs-lookup"><span data-stu-id="3d67b-123">Metrics for Portable Documents</span></span>](metrics-for-portable-documents.md)

 

 



