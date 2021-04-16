---
description: 調整飽和度。
ms.assetid: bd71f542-36d9-4dfc-b402-35ee8e574731
title: 'MFPKEY_COLOR_SATURATION 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 496b1f017ceff6ab4bd01ce01ccfd5da0759befc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104513117"
---
# <a name="mfpkey_color_saturation-property"></a><span data-ttu-id="1ce3f-103">MFPKEY \_ 色彩 \_ 飽和度屬性</span><span class="sxs-lookup"><span data-stu-id="1ce3f-103">MFPKEY\_COLOR\_SATURATION Property</span></span>

<span data-ttu-id="1ce3f-104">調整飽和度。</span><span class="sxs-lookup"><span data-stu-id="1ce3f-104">Adjusts the saturation.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="1ce3f-105">IPropertyBag 的常數</span><span class="sxs-lookup"><span data-stu-id="1ce3f-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="1ce3f-106">僅可使用 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)。</span><span class="sxs-lookup"><span data-stu-id="1ce3f-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="1ce3f-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="1ce3f-107">Data Type</span></span>

<span data-ttu-id="1ce3f-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="1ce3f-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="1ce3f-109">預設值</span><span class="sxs-lookup"><span data-stu-id="1ce3f-109">Default Value</span></span>

<span data-ttu-id="1ce3f-110">0</span><span class="sxs-lookup"><span data-stu-id="1ce3f-110">0</span></span>

## <a name="applies-to"></a><span data-ttu-id="1ce3f-111">套用至</span><span class="sxs-lookup"><span data-stu-id="1ce3f-111">Applies To</span></span>

-   [<span data-ttu-id="1ce3f-112">色彩控制轉換 DSP</span><span class="sxs-lookup"><span data-stu-id="1ce3f-112">Color Control Transform DSP</span></span>](colorcontroltransform.md)

## <a name="remarks"></a><span data-ttu-id="1ce3f-113">備註</span><span class="sxs-lookup"><span data-stu-id="1ce3f-113">Remarks</span></span>

<span data-ttu-id="1ce3f-114">飽和度調整是藉由將 Cb 和 Cr 值乘以常數來執行。</span><span class="sxs-lookup"><span data-stu-id="1ce3f-114">Saturation adjustment is performed by multiplying the Cb and Cr values by a constant.</span></span>

<span data-ttu-id="1ce3f-115">這個屬性的範圍為-127 到127。</span><span class="sxs-lookup"><span data-stu-id="1ce3f-115">This property has a range of -127 to 127.</span></span> <span data-ttu-id="1ce3f-116">零表示飽和度沒有變更。</span><span class="sxs-lookup"><span data-stu-id="1ce3f-116">Zero indicates no change in saturation.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ce3f-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="1ce3f-117">Requirements</span></span>



| <span data-ttu-id="1ce3f-118">需求</span><span class="sxs-lookup"><span data-stu-id="1ce3f-118">Requirement</span></span> | <span data-ttu-id="1ce3f-119">值</span><span class="sxs-lookup"><span data-stu-id="1ce3f-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1ce3f-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1ce3f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="1ce3f-121">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1ce3f-121">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="1ce3f-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1ce3f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="1ce3f-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1ce3f-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1ce3f-124">標頭</span><span class="sxs-lookup"><span data-stu-id="1ce3f-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="1ce3f-125"><dt>Wmcodecdsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="1ce3f-125"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ce3f-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1ce3f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ce3f-127">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="1ce3f-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
