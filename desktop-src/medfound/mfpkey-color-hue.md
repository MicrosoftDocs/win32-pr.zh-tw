---
description: 調整色調。
ms.assetid: 8dc3c888-5ab8-40a1-8768-bec58b62eaf0
title: 'MFPKEY_COLOR_HUE 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b3ddf0109090bfb56102560dc06a853c970e7ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115136"
---
# <a name="mfpkey_color_hue-property"></a><span data-ttu-id="a3acc-103">MFPKEY \_ 色彩 \_ 色調屬性</span><span class="sxs-lookup"><span data-stu-id="a3acc-103">MFPKEY\_COLOR\_HUE Property</span></span>

<span data-ttu-id="a3acc-104">調整色調。</span><span class="sxs-lookup"><span data-stu-id="a3acc-104">Adjusts the hue.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="a3acc-105">IPropertyBag 的常數</span><span class="sxs-lookup"><span data-stu-id="a3acc-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="a3acc-106">僅可使用 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)。</span><span class="sxs-lookup"><span data-stu-id="a3acc-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="a3acc-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="a3acc-107">Data Type</span></span>

<span data-ttu-id="a3acc-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="a3acc-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="a3acc-109">預設值</span><span class="sxs-lookup"><span data-stu-id="a3acc-109">Default Value</span></span>

<span data-ttu-id="a3acc-110">0</span><span class="sxs-lookup"><span data-stu-id="a3acc-110">0</span></span>

## <a name="applies-to"></a><span data-ttu-id="a3acc-111">套用至</span><span class="sxs-lookup"><span data-stu-id="a3acc-111">Applies To</span></span>

-   [<span data-ttu-id="a3acc-112">色彩控制轉換 DSP</span><span class="sxs-lookup"><span data-stu-id="a3acc-112">Color Control Transform DSP</span></span>](colorcontroltransform.md)

## <a name="remarks"></a><span data-ttu-id="a3acc-113">備註</span><span class="sxs-lookup"><span data-stu-id="a3acc-113">Remarks</span></span>

<span data-ttu-id="a3acc-114">色調調整是藉由混用 Cb 和 Cr 值來執行。</span><span class="sxs-lookup"><span data-stu-id="a3acc-114">Hue adjustment is performed by mixing the Cb and Cr values.</span></span> <span data-ttu-id="a3acc-115"> (如果 Cb 和 Cr 繪製在二維空間中，則色調調整是藉由在原點周圍旋轉來執行。 ) </span><span class="sxs-lookup"><span data-stu-id="a3acc-115">(If Cb and Cr are plotted in a 2-dimensional space, hue adjustment is performed by rotating around the origin.)</span></span>

<span data-ttu-id="a3acc-116">這個屬性的範圍為-127 到127。</span><span class="sxs-lookup"><span data-stu-id="a3acc-116">This property has a range of -127 to 127.</span></span> <span data-ttu-id="a3acc-117">零表示色調沒有變更。</span><span class="sxs-lookup"><span data-stu-id="a3acc-117">Zero indicates no change in hue.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3acc-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="a3acc-118">Requirements</span></span>



| <span data-ttu-id="a3acc-119">需求</span><span class="sxs-lookup"><span data-stu-id="a3acc-119">Requirement</span></span> | <span data-ttu-id="a3acc-120">值</span><span class="sxs-lookup"><span data-stu-id="a3acc-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a3acc-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a3acc-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a3acc-122">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a3acc-122">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="a3acc-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a3acc-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a3acc-124">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a3acc-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a3acc-125">標頭</span><span class="sxs-lookup"><span data-stu-id="a3acc-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="a3acc-126"><dt>Wmcodecdsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="a3acc-126"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a3acc-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a3acc-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3acc-128">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="a3acc-128">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
