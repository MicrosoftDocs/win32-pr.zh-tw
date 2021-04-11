---
description: 調整亮度。
ms.assetid: 1b3f56eb-3f22-4120-ba6c-331eccd5d303
title: 'MFPKEY_COLOR_BRIGHTNESS 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 685ab934a91f1843183fcfa88bb94c83e602db27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849119"
---
# <a name="mfpkey_color_brightness-property"></a><span data-ttu-id="175c2-103">MFPKEY \_ 色彩 \_ 亮度屬性</span><span class="sxs-lookup"><span data-stu-id="175c2-103">MFPKEY\_COLOR\_BRIGHTNESS Property</span></span>

<span data-ttu-id="175c2-104">調整亮度。</span><span class="sxs-lookup"><span data-stu-id="175c2-104">Adjusts the brightness.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="175c2-105">IPropertyBag 的常數</span><span class="sxs-lookup"><span data-stu-id="175c2-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="175c2-106">僅可使用 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)。</span><span class="sxs-lookup"><span data-stu-id="175c2-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="175c2-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="175c2-107">Data Type</span></span>

<span data-ttu-id="175c2-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="175c2-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="175c2-109">預設值</span><span class="sxs-lookup"><span data-stu-id="175c2-109">Default Value</span></span>

<span data-ttu-id="175c2-110">0</span><span class="sxs-lookup"><span data-stu-id="175c2-110">0</span></span>

## <a name="applies-to"></a><span data-ttu-id="175c2-111">套用至</span><span class="sxs-lookup"><span data-stu-id="175c2-111">Applies To</span></span>

-   [<span data-ttu-id="175c2-112">色彩控制轉換 DSP</span><span class="sxs-lookup"><span data-stu-id="175c2-112">Color Control Transform DSP</span></span>](colorcontroltransform.md)

## <a name="remarks"></a><span data-ttu-id="175c2-113">備註</span><span class="sxs-lookup"><span data-stu-id="175c2-113">Remarks</span></span>

<span data-ttu-id="175c2-114">亮度調整是藉由將值新增至 luma 通道來執行。</span><span class="sxs-lookup"><span data-stu-id="175c2-114">Brightness adjustment is performed by adding a value to the luma channel.</span></span>

<span data-ttu-id="175c2-115">這個屬性的範圍為-127 到127。</span><span class="sxs-lookup"><span data-stu-id="175c2-115">This property has a range of -127 to 127.</span></span> <span data-ttu-id="175c2-116">零表示亮度沒有變更。</span><span class="sxs-lookup"><span data-stu-id="175c2-116">Zero indicates no change in brightness.</span></span>

## <a name="requirements"></a><span data-ttu-id="175c2-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="175c2-117">Requirements</span></span>



| <span data-ttu-id="175c2-118">需求</span><span class="sxs-lookup"><span data-stu-id="175c2-118">Requirement</span></span> | <span data-ttu-id="175c2-119">值</span><span class="sxs-lookup"><span data-stu-id="175c2-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="175c2-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="175c2-120">Minimum supported client</span></span><br/> | <span data-ttu-id="175c2-121">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="175c2-121">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="175c2-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="175c2-122">Minimum supported server</span></span><br/> | <span data-ttu-id="175c2-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="175c2-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="175c2-124">標頭</span><span class="sxs-lookup"><span data-stu-id="175c2-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="175c2-125"><dt>Wmcodecdsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="175c2-125"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="175c2-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="175c2-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="175c2-127">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="175c2-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
