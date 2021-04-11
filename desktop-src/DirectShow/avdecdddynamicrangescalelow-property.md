---
description: 指定當解碼器在杜比 AC-3 音訊串流上執行動態範圍控制時的低層級提升。
ms.assetid: d723c825-f2f1-4ba0-a667-8285009764fd
title: 'AVDecDDDynamicRangeScaleLow 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8b68b1d4376d9ba15859be943ded23458fe16d6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104025778"
---
# <a name="avdecdddynamicrangescalelow-property"></a><span data-ttu-id="38912-103">AVDecDDDynamicRangeScaleLow 屬性</span><span class="sxs-lookup"><span data-stu-id="38912-103">AVDecDDDynamicRangeScaleLow property</span></span>

<span data-ttu-id="38912-104">指定當解碼器在杜比 AC-3 音訊串流上執行動態範圍控制時的低層級提升。</span><span class="sxs-lookup"><span data-stu-id="38912-104">Specifies the low-level boost when the decoder performs dynamic range control on a Dolby AC-3 audio stream.</span></span>

<span data-ttu-id="38912-105">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="38912-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="38912-106">資料類型</span><span class="sxs-lookup"><span data-stu-id="38912-106">Data type</span></span>

<span data-ttu-id="38912-107">**UINT32** (**VT \_ UI4**) </span><span class="sxs-lookup"><span data-stu-id="38912-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="38912-108">屬性 GUID</span><span class="sxs-lookup"><span data-stu-id="38912-108">Property GUID</span></span>

<span data-ttu-id="38912-109">**CODECAPI \_ AVDecDDDynamicRangeScaleLow**</span><span class="sxs-lookup"><span data-stu-id="38912-109">**CODECAPI\_AVDecDDDynamicRangeScaleLow**</span></span>

## <a name="property-value"></a><span data-ttu-id="38912-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="38912-110">Property value</span></span>

<span data-ttu-id="38912-111">這個屬性的值具有下列範圍。</span><span class="sxs-lookup"><span data-stu-id="38912-111">The value of this property has the following range.</span></span>



| <span data-ttu-id="38912-112">值</span><span class="sxs-lookup"><span data-stu-id="38912-112">Value</span></span> | <span data-ttu-id="38912-113">描述</span><span class="sxs-lookup"><span data-stu-id="38912-113">Description</span></span>                                                    |
|-------|----------------------------------------------------------------|
| <span data-ttu-id="38912-114">0</span><span class="sxs-lookup"><span data-stu-id="38912-114">0</span></span>     | <span data-ttu-id="38912-115">沒有動態範圍壓縮。</span><span class="sxs-lookup"><span data-stu-id="38912-115">No dynamic range compression.</span></span> <span data-ttu-id="38912-116">保留完整的動態範圍。</span><span class="sxs-lookup"><span data-stu-id="38912-116">Preserve the full dynamic range.</span></span> |
| <span data-ttu-id="38912-117">100</span><span class="sxs-lookup"><span data-stu-id="38912-117">100</span></span>   | <span data-ttu-id="38912-118">套用完整的動態範圍壓縮。</span><span class="sxs-lookup"><span data-stu-id="38912-118">Apply full dynamic range compression.</span></span>                          |



 

## <a name="remarks"></a><span data-ttu-id="38912-119">備註</span><span class="sxs-lookup"><span data-stu-id="38912-119">Remarks</span></span>

<span data-ttu-id="38912-120">只有當 [**AVDecDDOperationalMode**](avdecddoperationalmode-property.md) 屬性的值是 eAVDecDDOperationalMode 行時，才會套用此屬性 \_ 。</span><span class="sxs-lookup"><span data-stu-id="38912-120">This property applies only when the value of the [**AVDecDDOperationalMode**](avdecddoperationalmode-property.md) property is eAVDecDDOperationalMode\_LINE.</span></span>

## <a name="requirements"></a><span data-ttu-id="38912-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="38912-121">Requirements</span></span>



| <span data-ttu-id="38912-122">需求</span><span class="sxs-lookup"><span data-stu-id="38912-122">Requirement</span></span> | <span data-ttu-id="38912-123">值</span><span class="sxs-lookup"><span data-stu-id="38912-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="38912-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="38912-124">Minimum supported client</span></span><br/> | <span data-ttu-id="38912-125">Windows 2000 專業版傳統型 \[ 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="38912-125">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="38912-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="38912-126">Minimum supported server</span></span><br/> | <span data-ttu-id="38912-127">Windows 2000 Server \[ desktop 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="38912-127">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="38912-128">標頭</span><span class="sxs-lookup"><span data-stu-id="38912-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="38912-129"><dt>Codecapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="38912-129"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="38912-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="38912-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38912-131">編解碼器 API 屬性</span><span class="sxs-lookup"><span data-stu-id="38912-131">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="38912-132">**ICodecAPI 介面**</span><span class="sxs-lookup"><span data-stu-id="38912-132">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




