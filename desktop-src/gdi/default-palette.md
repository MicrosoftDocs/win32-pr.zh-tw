---
description: 預設調色板是色彩值的陣列，可識別預設可搭配裝置內容使用的色彩。
ms.assetid: 7972d5da-2b73-4cd7-a2ee-fca3a571f611
title: 預設調色板
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c100eeb144ab4f6483281b33739578642880a91f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848566"
---
# <a name="default-palette"></a><span data-ttu-id="44c34-103">預設調色板</span><span class="sxs-lookup"><span data-stu-id="44c34-103">Default Palette</span></span>

<span data-ttu-id="44c34-104">*預設調色板* 是色彩值的陣列，可識別預設可搭配裝置內容使用的色彩。</span><span class="sxs-lookup"><span data-stu-id="44c34-104">The *default palette* is an array of color values identifying the colors that can be used with a device context by default.</span></span> <span data-ttu-id="44c34-105">當應用程式為支援調色板的裝置建立內容時，系統會將預設的調色板與內容產生關聯。</span><span class="sxs-lookup"><span data-stu-id="44c34-105">the system associates the default palette with a context whenever an application creates a context for a device that supports color palettes.</span></span> <span data-ttu-id="44c34-106">預設的調色板可確保應用程式可使用色彩，而不需要採取任何進一步的動作。</span><span class="sxs-lookup"><span data-stu-id="44c34-106">The default palette ensures that colors are available for use by an application without any further action.</span></span>

<span data-ttu-id="44c34-107">預設的調色板通常會有20個專案 (色彩) ，但實際的專案數目可能會因裝置而異。</span><span class="sxs-lookup"><span data-stu-id="44c34-107">The default palette typically has 20 entries (colors), but the exact number of entries may vary from device to device.</span></span> <span data-ttu-id="44c34-108">這個數位等於 [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) 函數所傳回的 NUMCOLORS 值。</span><span class="sxs-lookup"><span data-stu-id="44c34-108">This number is equal to the NUMCOLORS value returned by the [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) function.</span></span> <span data-ttu-id="44c34-109">應用程式可以藉由列舉單色筆刷來取得預設調色板中色彩的色彩值，這是用來探索 nonpalette 裝置上可用色彩的相同技術。</span><span class="sxs-lookup"><span data-stu-id="44c34-109">An application can retrieve the color values for colors in the default palette by enumerating solid pens, the same technique used to discover the colors available on nonpalette devices.</span></span> <span data-ttu-id="44c34-110">預設調色板中的色彩取決於裝置。</span><span class="sxs-lookup"><span data-stu-id="44c34-110">The colors in the default palette depend on the device.</span></span> <span data-ttu-id="44c34-111">例如，顯示裝置通常會使用 VGA 顯示器的16種標準色彩，以及 Windows 所定義的4種其他色彩。</span><span class="sxs-lookup"><span data-stu-id="44c34-111">Display devices, for example, often use the 16 standard colors of the VGA display and 4 other colors defined by Windows.</span></span> <span data-ttu-id="44c34-112">列印裝置可能會使用其他預設色彩。</span><span class="sxs-lookup"><span data-stu-id="44c34-112">Print devices may use other default colors.</span></span>

<span data-ttu-id="44c34-113">使用預設的調色板時，應用程式會使用色彩值來指定畫筆和文字色彩。</span><span class="sxs-lookup"><span data-stu-id="44c34-113">When using the default palette, applications use color values to specify pen and text colors.</span></span> <span data-ttu-id="44c34-114">如果要求的色彩不在調色板中，系統會使用調色板中最接近的色彩來接近色彩。</span><span class="sxs-lookup"><span data-stu-id="44c34-114">If the requested color is not in the palette, The system approximates the color by using the closest color in the palette.</span></span> <span data-ttu-id="44c34-115">如果應用程式要求的是不在調色板中的純色筆刷色彩，系統就會使用調色板中的色彩來進行遞色來模擬色彩。</span><span class="sxs-lookup"><span data-stu-id="44c34-115">If an application requests a solid brush color that is not in the palette, the system simulates the color by dithering with colors that are in the palette.</span></span>

<span data-ttu-id="44c34-116">為了避免近似值和遞色，應用程式也可以使用色板索引（而非色彩值）來指定畫筆、筆刷和文字色彩。</span><span class="sxs-lookup"><span data-stu-id="44c34-116">To avoid approximations and dithering, applications can also specify pen, brush, and text colors by using color palette indexes rather than color values.</span></span> <span data-ttu-id="44c34-117">色調色板索引是識別特定調色板專案的整數值。</span><span class="sxs-lookup"><span data-stu-id="44c34-117">A color palette index is an integer value that identifies a specific palette entry.</span></span> <span data-ttu-id="44c34-118">應用程式可以使用調色板索引來取代色彩值，但必須使用 [**調色盤索引**](/windows/desktop/api/Wingdi/nf-wingdi-paletteindex) 宏來建立索引。</span><span class="sxs-lookup"><span data-stu-id="44c34-118">Applications can use color palette indexes in place of color values but must use the [**PALETTEINDEX**](/windows/desktop/api/Wingdi/nf-wingdi-paletteindex) macro to create the indexes.</span></span>

<span data-ttu-id="44c34-119">色彩選擇區索引僅適用于支援調色板的裝置。</span><span class="sxs-lookup"><span data-stu-id="44c34-119">Color palette indexes are only useful for devices that support color palettes.</span></span> <span data-ttu-id="44c34-120">為了避免這種裝置的相依性，使用相同程式碼的應用程式同時繪製至調色板和 nonpalette 裝置，應該使用調色板相關的色彩值來指定畫筆、筆刷和文字色彩。</span><span class="sxs-lookup"><span data-stu-id="44c34-120">To avoid this device dependence, applications that use the same code to draw to both palette and nonpalette devices should use palette-relative color values to specify pen, brush, and text colors.</span></span> <span data-ttu-id="44c34-121">這些值與色彩值相同，不同之處在于建立純色筆刷。</span><span class="sxs-lookup"><span data-stu-id="44c34-121">These values are identical to color values except when creating solid brushes.</span></span> <span data-ttu-id="44c34-122"> (在調色板裝置上，由調色板相關色彩值所指定的純色筆刷色彩，會受限於色彩近似值而非遞色。 ) 應用程式必須使用 [**PALETTERGB**](/windows/desktop/api/Wingdi/nf-wingdi-palettergb) 宏來建立調色板相關的色彩值。</span><span class="sxs-lookup"><span data-stu-id="44c34-122">(On palette devices, a solid brush color specified by a palette-relative color value is subject to color approximation instead of dithering.) Applications must use the [**PALETTERGB**](/windows/desktop/api/Wingdi/nf-wingdi-palettergb) macro to create palette-relative color values.</span></span>

<span data-ttu-id="44c34-123">系統不允許應用程式變更預設調色板中的專案。</span><span class="sxs-lookup"><span data-stu-id="44c34-123">The system does not allow an application to change the entries in the default palette.</span></span> <span data-ttu-id="44c34-124">若要使用預設調色板中以外的色彩，應用程式必須建立自己的邏輯調色板，並在裝置內容中選取 [選擇區]。</span><span class="sxs-lookup"><span data-stu-id="44c34-124">To use colors other than those in the default palette, an application must create its own logical palette and select the palette into the device context.</span></span>

 

 



