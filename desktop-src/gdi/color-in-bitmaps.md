---
description: 系統會以不同于畫筆、筆刷和文字的色彩，來處理點陣圖中的色彩。
ms.assetid: c315dd6e-87ee-4905-b193-186ea580ac0a
title: 點陣圖中的色彩
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 834744f35ccc8bd0c8714fa5bbb438b59c8b8db3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114701"
---
# <a name="color-in-bitmaps"></a><span data-ttu-id="4238b-103">點陣圖中的色彩</span><span class="sxs-lookup"><span data-stu-id="4238b-103">Color in Bitmaps</span></span>

<span data-ttu-id="4238b-104">系統會以不同于畫筆、筆刷和文字的色彩，來處理點陣圖中的色彩。</span><span class="sxs-lookup"><span data-stu-id="4238b-104">The system handles colors in bitmaps differently than colors in pens, brushes, and text.</span></span> <span data-ttu-id="4238b-105">使用 [**CreateBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmap) 或 [**CreateCompatibleBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatiblebitmap) 函式所建立的相容點陣圖是裝置特定的，而且會以裝置相依的格式保留色彩資訊。</span><span class="sxs-lookup"><span data-stu-id="4238b-105">Compatible bitmaps, created by using the [**CreateBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmap) or [**CreateCompatibleBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatiblebitmap) function, are device specific and retain color information in a device-dependent format.</span></span> <span data-ttu-id="4238b-106">不會使用任何色彩值，而且色彩不會受限於近似值和遞色。</span><span class="sxs-lookup"><span data-stu-id="4238b-106">No color values are used, and the colors are not subject to approximations and dithering.</span></span>

<span data-ttu-id="4238b-107">與裝置無關的點陣圖 (Dib) 將色彩資訊保留為色彩值或調色板索引。</span><span class="sxs-lookup"><span data-stu-id="4238b-107">Device-independent bitmaps (DIBs) retain color information either as color values or color palette indexes.</span></span> <span data-ttu-id="4238b-108">如果使用色彩值，色彩會受限於近似值，但不能遞色。</span><span class="sxs-lookup"><span data-stu-id="4238b-108">If color values are used, the colors are subject to approximation, but not dithering.</span></span> <span data-ttu-id="4238b-109">色階索引只能與支援調色板的裝置搭配使用。</span><span class="sxs-lookup"><span data-stu-id="4238b-109">Color palette indexes can only be used with devices that support color palettes.</span></span> <span data-ttu-id="4238b-110">雖然系統不會計算索引所識別的近似或遞色色彩，但產生的色彩可能會與預期的色彩不同，因為索引只會在建立點陣圖時的最新色彩選擇器內容中產生有效的結果。</span><span class="sxs-lookup"><span data-stu-id="4238b-110">Although the system does not approximate or dither colors identified by indexes, the resulting color may be different than that intended, because the indexes yield valid results only in the context of the color palette that was current at the time the bitmap was created.</span></span> <span data-ttu-id="4238b-111">如果選擇區變更，則點陣圖中的色彩。</span><span class="sxs-lookup"><span data-stu-id="4238b-111">If the palette changes, so do the colors in the bitmap.</span></span> <span data-ttu-id="4238b-112">如需有關調色板索引的詳細資訊，請參閱預設的 [ [調色板](default-palette.md) ] 和 [ [**調色盤索引**](/windows/desktop/api/Wingdi/nf-wingdi-paletteindex)]。</span><span class="sxs-lookup"><span data-stu-id="4238b-112">For more information on palette indexes, see [Default Palette](default-palette.md) and [**PALETTEINDEX**](/windows/desktop/api/Wingdi/nf-wingdi-paletteindex).</span></span>

<span data-ttu-id="4238b-113">除了參考邏輯調色板之外，應用程式也可以參考 DIB 色彩表中的值。</span><span class="sxs-lookup"><span data-stu-id="4238b-113">In addition to referencing the logical palette, an application can also reference a value in a DIB color table.</span></span> <span data-ttu-id="4238b-114">若要選取 DIB 色彩表中的色彩，請呼叫 [**DIBINDEX**](/windows/desktop/api/Mmsystem/nf-mmsystem-dibindex)。</span><span class="sxs-lookup"><span data-stu-id="4238b-114">To select a color in a DIB color table, call [**DIBINDEX**](/windows/desktop/api/Mmsystem/nf-mmsystem-dibindex).</span></span> <span data-ttu-id="4238b-115">請注意，這只適用于已選取 DIB 的裝置內容。</span><span class="sxs-lookup"><span data-stu-id="4238b-115">Note that this is only possible for a device context that has a DIB selected into it.</span></span>

 

 



