---
description: 指定最小顯示光圈左上角的 x 座標。
ms.assetid: eb9e5330-fd89-4bca-ae8c-62985f9b2373
title: 'MFPKEY_RESIZE_MINAPX 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b3325730bdd77d192abf79ed60e70a22363c398
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192234"
---
# <a name="mfpkey_resize_minapx-property"></a><span data-ttu-id="8fe26-103">MFPKEY \_ RESIZE \_ MINAPX 屬性</span><span class="sxs-lookup"><span data-stu-id="8fe26-103">MFPKEY\_RESIZE\_MINAPX Property</span></span>

<span data-ttu-id="8fe26-104">指定最小顯示光圈左上角的 x 座標。</span><span class="sxs-lookup"><span data-stu-id="8fe26-104">Specifies the x-coordinate of the upper-left corner of the minimum display aperture.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="8fe26-105">IPropertyBag 的常數</span><span class="sxs-lookup"><span data-stu-id="8fe26-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="8fe26-106">僅可使用 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)。</span><span class="sxs-lookup"><span data-stu-id="8fe26-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="8fe26-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="8fe26-107">Data Type</span></span>

<span data-ttu-id="8fe26-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="8fe26-108">VT\_I4</span></span>

## <a name="applies-to"></a><span data-ttu-id="8fe26-109">套用至</span><span class="sxs-lookup"><span data-stu-id="8fe26-109">Applies To</span></span>

-   [<span data-ttu-id="8fe26-110">影片尺寸調整 DSP</span><span class="sxs-lookup"><span data-stu-id="8fe26-110">Video Resizer DSP</span></span>](videoresizer.md)

## <a name="remarks"></a><span data-ttu-id="8fe26-111">備註</span><span class="sxs-lookup"><span data-stu-id="8fe26-111">Remarks</span></span>

<span data-ttu-id="8fe26-112">此值為固定點實數。</span><span class="sxs-lookup"><span data-stu-id="8fe26-112">The value is a fixed-point real number.</span></span> <span data-ttu-id="8fe26-113">數位的整數部分會儲存在較高的2個位元組中，小數部分則會儲存在2個較低的位元組中。</span><span class="sxs-lookup"><span data-stu-id="8fe26-113">The integer portion of the number is stored in the higher 2 bytes and the fractional part is stored in the lower 2 bytes.</span></span>

## <a name="requirements"></a><span data-ttu-id="8fe26-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="8fe26-114">Requirements</span></span>



| <span data-ttu-id="8fe26-115">需求</span><span class="sxs-lookup"><span data-stu-id="8fe26-115">Requirement</span></span> | <span data-ttu-id="8fe26-116">值</span><span class="sxs-lookup"><span data-stu-id="8fe26-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8fe26-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8fe26-117">Minimum supported client</span></span><br/> | <span data-ttu-id="8fe26-118">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8fe26-118">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="8fe26-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8fe26-119">Minimum supported server</span></span><br/> | <span data-ttu-id="8fe26-120">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8fe26-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="8fe26-121">標頭</span><span class="sxs-lookup"><span data-stu-id="8fe26-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="8fe26-122"><dt>Wmcodecdsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="8fe26-122"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8fe26-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8fe26-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8fe26-124">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="8fe26-124">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
