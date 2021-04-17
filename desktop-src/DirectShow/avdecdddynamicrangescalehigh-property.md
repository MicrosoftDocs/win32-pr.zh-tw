---
description: 指定當解碼器在杜比 AC-3 音訊串流上執行動態範圍控制時的高階剪下。
ms.assetid: 8771a5f9-878b-43fd-8eaa-0bfc276194aa
title: 'AVDecDDDynamicRangeScaleHigh 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 521cd631d92db73f23c7018adeda9bd321d23c1a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104467831"
---
# <a name="avdecdddynamicrangescalehigh-property"></a><span data-ttu-id="1bdf2-103">AVDecDDDynamicRangeScaleHigh 屬性</span><span class="sxs-lookup"><span data-stu-id="1bdf2-103">AVDecDDDynamicRangeScaleHigh property</span></span>

<span data-ttu-id="1bdf2-104">指定當解碼器在杜比 AC-3 音訊串流上執行動態範圍控制時的高階剪下。</span><span class="sxs-lookup"><span data-stu-id="1bdf2-104">Specifies the high-level cut when the decoder performs dynamic range control on a Dolby AC-3 audio stream.</span></span>

<span data-ttu-id="1bdf2-105">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="1bdf2-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="1bdf2-106">資料類型</span><span class="sxs-lookup"><span data-stu-id="1bdf2-106">Data type</span></span>

<span data-ttu-id="1bdf2-107">**UINT32** (**VT \_ UI4**) </span><span class="sxs-lookup"><span data-stu-id="1bdf2-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="1bdf2-108">屬性 GUID</span><span class="sxs-lookup"><span data-stu-id="1bdf2-108">Property GUID</span></span>

<span data-ttu-id="1bdf2-109">**CODECAPI \_ AVDecDDDynamicRangeScaleHigh**</span><span class="sxs-lookup"><span data-stu-id="1bdf2-109">**CODECAPI\_AVDecDDDynamicRangeScaleHigh**</span></span>

## <a name="property-value"></a><span data-ttu-id="1bdf2-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="1bdf2-110">Property value</span></span>

<span data-ttu-id="1bdf2-111">這個屬性的值具有下列範圍。</span><span class="sxs-lookup"><span data-stu-id="1bdf2-111">The value of this property has the following range.</span></span>



| <span data-ttu-id="1bdf2-112">值</span><span class="sxs-lookup"><span data-stu-id="1bdf2-112">Value</span></span> | <span data-ttu-id="1bdf2-113">描述</span><span class="sxs-lookup"><span data-stu-id="1bdf2-113">Description</span></span>                                                    |
|-------|----------------------------------------------------------------|
| <span data-ttu-id="1bdf2-114">0</span><span class="sxs-lookup"><span data-stu-id="1bdf2-114">0</span></span>     | <span data-ttu-id="1bdf2-115">沒有動態範圍壓縮。</span><span class="sxs-lookup"><span data-stu-id="1bdf2-115">No dynamic range compression.</span></span> <span data-ttu-id="1bdf2-116">保留完整的動態範圍。</span><span class="sxs-lookup"><span data-stu-id="1bdf2-116">Preserve the full dynamic range.</span></span> |
| <span data-ttu-id="1bdf2-117">100</span><span class="sxs-lookup"><span data-stu-id="1bdf2-117">100</span></span>   | <span data-ttu-id="1bdf2-118">套用完整的動態範圍壓縮。</span><span class="sxs-lookup"><span data-stu-id="1bdf2-118">Apply full dynamic range compression.</span></span>                          |



 

## <a name="remarks"></a><span data-ttu-id="1bdf2-119">備註</span><span class="sxs-lookup"><span data-stu-id="1bdf2-119">Remarks</span></span>

<span data-ttu-id="1bdf2-120">只有當 [**AVDecDDOperationalMode**](avdecddoperationalmode-property.md) 屬性的值是 eAVDecDDOperationalMode 行時，才會套用此屬性 \_ 。</span><span class="sxs-lookup"><span data-stu-id="1bdf2-120">This property applies only when the value of the [**AVDecDDOperationalMode**](avdecddoperationalmode-property.md) property is eAVDecDDOperationalMode\_LINE.</span></span>

## <a name="requirements"></a><span data-ttu-id="1bdf2-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="1bdf2-121">Requirements</span></span>



| <span data-ttu-id="1bdf2-122">需求</span><span class="sxs-lookup"><span data-stu-id="1bdf2-122">Requirement</span></span> | <span data-ttu-id="1bdf2-123">值</span><span class="sxs-lookup"><span data-stu-id="1bdf2-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1bdf2-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1bdf2-124">Minimum supported client</span></span><br/> | <span data-ttu-id="1bdf2-125">Windows 2000 專業版傳統型 \[ 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1bdf2-125">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="1bdf2-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1bdf2-126">Minimum supported server</span></span><br/> | <span data-ttu-id="1bdf2-127">Windows 2000 Server \[ desktop 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1bdf2-127">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="1bdf2-128">標頭</span><span class="sxs-lookup"><span data-stu-id="1bdf2-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="1bdf2-129"><dt>Codecapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="1bdf2-129"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1bdf2-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1bdf2-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1bdf2-131">編解碼器 API 屬性</span><span class="sxs-lookup"><span data-stu-id="1bdf2-131">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="1bdf2-132">**ICodecAPI 介面**</span><span class="sxs-lookup"><span data-stu-id="1bdf2-132">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




