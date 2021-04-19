---
description: 指定編解碼器用來判斷要使用哪一個巨大區塊模式的成本方法。
ms.assetid: 2ba9b943-0daa-40c1-87ea-2fa647fb7095
title: 'MFPKEY_MACROBLOCKMODECOSTMETHOD 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 289219300a79c67565891c48cec848851c17bd7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974633"
---
# <a name="mfpkey_macroblockmodecostmethod-property"></a><span data-ttu-id="671fe-103">MFPKEY \_ MACROBLOCKMODECOSTMETHOD 屬性</span><span class="sxs-lookup"><span data-stu-id="671fe-103">MFPKEY\_MACROBLOCKMODECOSTMETHOD Property</span></span>

<span data-ttu-id="671fe-104">指定編解碼器用來判斷要使用哪一個巨大區塊模式的成本方法。</span><span class="sxs-lookup"><span data-stu-id="671fe-104">Specifies the cost method used by the codec to determine which macroblock mode to use.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="671fe-105">IPropertyBag 的常數</span><span class="sxs-lookup"><span data-stu-id="671fe-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="671fe-106">g \_ wszWMVCMacroblockModeCostMethod</span><span class="sxs-lookup"><span data-stu-id="671fe-106">g\_wszWMVCMacroblockModeCostMethod</span></span>

## <a name="data-type"></a><span data-ttu-id="671fe-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="671fe-107">Data Type</span></span>

<span data-ttu-id="671fe-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="671fe-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="671fe-109">預設值</span><span class="sxs-lookup"><span data-stu-id="671fe-109">Default Value</span></span>

<span data-ttu-id="671fe-110">0</span><span class="sxs-lookup"><span data-stu-id="671fe-110">0</span></span>

## <a name="remarks"></a><span data-ttu-id="671fe-111">備註</span><span class="sxs-lookup"><span data-stu-id="671fe-111">Remarks</span></span>

<span data-ttu-id="671fe-112">這個屬性可以設定為下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="671fe-112">This property may be set to one of the following values.</span></span>



| <span data-ttu-id="671fe-113">值</span><span class="sxs-lookup"><span data-stu-id="671fe-113">Value</span></span> | <span data-ttu-id="671fe-114">使用的方法</span><span class="sxs-lookup"><span data-stu-id="671fe-114">Method used</span></span>                                                                                            |
|-------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="671fe-115">0</span><span class="sxs-lookup"><span data-stu-id="671fe-115">0</span></span>     | <span data-ttu-id="671fe-116">悲傷/Hadamard。</span><span class="sxs-lookup"><span data-stu-id="671fe-116">SAD/Hadamard.</span></span> <span data-ttu-id="671fe-117">此選項會將編解碼器設定為僅在計算成本時使用失真。</span><span class="sxs-lookup"><span data-stu-id="671fe-117">This option configures the codec to use only distortion when computing cost.</span></span>             |
| <span data-ttu-id="671fe-118">1</span><span class="sxs-lookup"><span data-stu-id="671fe-118">1</span></span>     | <span data-ttu-id="671fe-119">RD 成本。</span><span class="sxs-lookup"><span data-stu-id="671fe-119">RD cost.</span></span> <span data-ttu-id="671fe-120">此選項會設定編解碼器，以在計算成本時同時考慮速率和失真。</span><span class="sxs-lookup"><span data-stu-id="671fe-120">This option configures the codec to account for both rate and distortion when computing cost.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="671fe-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="671fe-121">Requirements</span></span>



| <span data-ttu-id="671fe-122">需求</span><span class="sxs-lookup"><span data-stu-id="671fe-122">Requirement</span></span> | <span data-ttu-id="671fe-123">值</span><span class="sxs-lookup"><span data-stu-id="671fe-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="671fe-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="671fe-124">Minimum supported client</span></span><br/> | <span data-ttu-id="671fe-125">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="671fe-125">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="671fe-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="671fe-126">Minimum supported server</span></span><br/> | <span data-ttu-id="671fe-127">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="671fe-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="671fe-128">標頭</span><span class="sxs-lookup"><span data-stu-id="671fe-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="671fe-129"><dt>Wmcodecdsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="671fe-129"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="671fe-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="671fe-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="671fe-131">MFPKEY \_ MOTIONMATCHMETHOD</span><span class="sxs-lookup"><span data-stu-id="671fe-131">MFPKEY\_MOTIONMATCHMETHOD</span></span>](mfpkey-motionmatchmethodproperty.md)
</dt> <dt>

[<span data-ttu-id="671fe-132">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="671fe-132">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




