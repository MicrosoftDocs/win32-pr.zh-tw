---
description: 只有在將字型選取至裝置內容之後，應用程式才能取得實體字型的字型度量。
ms.assetid: 3eaabc8b-e244-4b65-918b-a20043afa535
title: 裝置與設計單位
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fb52a671727a2fa84d5514b469be5bd320f3318
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848562"
---
# <a name="device-vs-design-units"></a><span data-ttu-id="0b7d0-103">裝置與設計單位</span><span class="sxs-lookup"><span data-stu-id="0b7d0-103">Device vs. Design Units</span></span>

<span data-ttu-id="0b7d0-104">只有在將字型選取至裝置內容之後，應用程式才能取得實體字型的字型度量。</span><span class="sxs-lookup"><span data-stu-id="0b7d0-104">An application can retrieve font metrics for a physical font only after the font has been selected into a device context.</span></span> <span data-ttu-id="0b7d0-105">在裝置內容中選取字型時，會針對裝置進行縮放。</span><span class="sxs-lookup"><span data-stu-id="0b7d0-105">When a font is selected into a device context, it is scaled for the device.</span></span> <span data-ttu-id="0b7d0-106">裝置特定的字型計量稱為裝置單位。</span><span class="sxs-lookup"><span data-stu-id="0b7d0-106">The font metrics specific to the device are known as device units.</span></span>

<span data-ttu-id="0b7d0-107">字型中的可攜計量稱為「設計單位」。</span><span class="sxs-lookup"><span data-stu-id="0b7d0-107">Portable metrics in fonts are known as design units.</span></span> <span data-ttu-id="0b7d0-108">若要套用至指定的裝置，設計單位必須轉換成裝置單位。</span><span class="sxs-lookup"><span data-stu-id="0b7d0-108">To apply to a specified device, design units must be converted to device units.</span></span> <span data-ttu-id="0b7d0-109">使用下列公式將設計單位轉換成裝置單位。</span><span class="sxs-lookup"><span data-stu-id="0b7d0-109">Use the following formula to convert design units to device units.</span></span>

<span data-ttu-id="0b7d0-110">*DeviceUnits* = (*DesignUnits* / *unitsPerEm*) \* (*dialog*/72) \* *DeviceResolution*</span><span class="sxs-lookup"><span data-stu-id="0b7d0-110">*DeviceUnits* = (*DesignUnits*/*unitsPerEm*) \* (*PointSize*/72) \* *DeviceResolution*</span></span>

<span data-ttu-id="0b7d0-111">此公式中的變數具有下列意義。</span><span class="sxs-lookup"><span data-stu-id="0b7d0-111">The variables in this formula have the following meanings.</span></span>



| <span data-ttu-id="0b7d0-112">變數</span><span class="sxs-lookup"><span data-stu-id="0b7d0-112">Variable</span></span>           | <span data-ttu-id="0b7d0-113">描述</span><span class="sxs-lookup"><span data-stu-id="0b7d0-113">Description</span></span>                                                                                                                                                                |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b7d0-114">*DeviceUnits*</span><span class="sxs-lookup"><span data-stu-id="0b7d0-114">*DeviceUnits*</span></span>      | <span data-ttu-id="0b7d0-115">指定轉換成裝置單位的 *DesignUnits* 字型度量。</span><span class="sxs-lookup"><span data-stu-id="0b7d0-115">Specifies the *DesignUnits* font metric converted to device units.</span></span> <span data-ttu-id="0b7d0-116">此值的單位與針對 *DeviceResolution* 指定的值相同。</span><span class="sxs-lookup"><span data-stu-id="0b7d0-116">This value is in the same units as the value specified for *DeviceResolution*.</span></span>                          |
| <span data-ttu-id="0b7d0-117">*DesignUnits*</span><span class="sxs-lookup"><span data-stu-id="0b7d0-117">*DesignUnits*</span></span>      | <span data-ttu-id="0b7d0-118">指定要轉換成裝置單位的字型度量。</span><span class="sxs-lookup"><span data-stu-id="0b7d0-118">Specifies the font metric to be converted to device units.</span></span> <span data-ttu-id="0b7d0-119">這個值可以是任何字型指標，包括字元寬度或整個字型的 ascender 值。</span><span class="sxs-lookup"><span data-stu-id="0b7d0-119">This value can be any font metric, including the width of a character or the ascender value for an entire font.</span></span> |
| <span data-ttu-id="0b7d0-120">*unitsPerEm*</span><span class="sxs-lookup"><span data-stu-id="0b7d0-120">*unitsPerEm*</span></span>       | <span data-ttu-id="0b7d0-121">指定字型的 em 正方形大小。</span><span class="sxs-lookup"><span data-stu-id="0b7d0-121">Specifies the em square size for the font.</span></span>                                                                                                                                 |
| <span data-ttu-id="0b7d0-122">*Dialog*</span><span class="sxs-lookup"><span data-stu-id="0b7d0-122">*PointSize*</span></span>        | <span data-ttu-id="0b7d0-123">指定字型的大小（以點為單位）。</span><span class="sxs-lookup"><span data-stu-id="0b7d0-123">Specifies size of the font, in points.</span></span> <span data-ttu-id="0b7d0-124"> (一點等於1/72 英寸。 ) </span><span class="sxs-lookup"><span data-stu-id="0b7d0-124">(One point equals 1/72 of an inch.)</span></span>                                                                                                 |
| <span data-ttu-id="0b7d0-125">*DeviceResolution*</span><span class="sxs-lookup"><span data-stu-id="0b7d0-125">*DeviceResolution*</span></span> | <span data-ttu-id="0b7d0-126">指定每英寸 (圖元) 的裝置單位數目。</span><span class="sxs-lookup"><span data-stu-id="0b7d0-126">Specifies number of device units (pixels) per inch.</span></span> <span data-ttu-id="0b7d0-127">雷射印表機的一般值可能是300，而針對 VGA 螢幕則是96。</span><span class="sxs-lookup"><span data-stu-id="0b7d0-127">Typical values might be 300 for a laser printer or 96 for a VGA screen.</span></span>                                                |



 

<span data-ttu-id="0b7d0-128">此公式不能用來將裝置單位轉換回設計單位。</span><span class="sxs-lookup"><span data-stu-id="0b7d0-128">This formula should not be used to convert device units back to design units.</span></span> <span data-ttu-id="0b7d0-129">裝置單位一律會四捨五入至最接近的圖元。</span><span class="sxs-lookup"><span data-stu-id="0b7d0-129">Device units are always rounded to the nearest pixel.</span></span> <span data-ttu-id="0b7d0-130">傳播的舍入錯誤可能會變得非常大，特別是當應用程式使用螢幕大小時。</span><span class="sxs-lookup"><span data-stu-id="0b7d0-130">The propagated round-off error can become very large, especially when an application is working with screen sizes.</span></span>

<span data-ttu-id="0b7d0-131">若要要求設計單位，請建立其高度指定為 *unitsPerEm* 的邏輯字型。</span><span class="sxs-lookup"><span data-stu-id="0b7d0-131">To request design units, create a logical font whose height is specified as *unitsPerEm*.</span></span> <span data-ttu-id="0b7d0-132">應用程式可以藉由呼叫 [**>enumfontfamilies**](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesa)函式並檢查 [**NEWTEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica)結構的 **NtmSizeEM** 成員，來取得 *unitsPerEm* 的值。</span><span class="sxs-lookup"><span data-stu-id="0b7d0-132">Applications can retrieve the value for *unitsPerEm* by calling the [**EnumFontFamilies**](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesa) function and checking the **ntmSizeEM** member of the [**NEWTEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica) structure.</span></span>

 

 



