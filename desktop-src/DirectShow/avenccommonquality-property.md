---
description: 指定編碼的品質等級。
ms.assetid: 2c7f3836-2392-47c6-9a56-d5a9b52560ff
title: 'AVEncCommonQuality 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a0e69d797f2e26e830158c969c8fcf4ec0b242a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104467889"
---
# <a name="avenccommonquality-property"></a><span data-ttu-id="566f6-103">AVEncCommonQuality 屬性</span><span class="sxs-lookup"><span data-stu-id="566f6-103">AVEncCommonQuality property</span></span>

<span data-ttu-id="566f6-104">指定編碼的品質等級。</span><span class="sxs-lookup"><span data-stu-id="566f6-104">Specifies the quality level for encoding.</span></span>

<span data-ttu-id="566f6-105">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="566f6-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="566f6-106">資料類型</span><span class="sxs-lookup"><span data-stu-id="566f6-106">Data type</span></span>

<span data-ttu-id="566f6-107">**UINT32** (**VT \_ UI4**) </span><span class="sxs-lookup"><span data-stu-id="566f6-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="566f6-108">屬性 GUID</span><span class="sxs-lookup"><span data-stu-id="566f6-108">Property GUID</span></span>

<span data-ttu-id="566f6-109">**CODECAPI \_ AVEncCommonQuality**</span><span class="sxs-lookup"><span data-stu-id="566f6-109">**CODECAPI\_AVEncCommonQuality**</span></span>

## <a name="property-value"></a><span data-ttu-id="566f6-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="566f6-110">Property value</span></span>

<span data-ttu-id="566f6-111">這個屬性的值具有下列範圍。</span><span class="sxs-lookup"><span data-stu-id="566f6-111">The value of this property has the following range.</span></span>



| <span data-ttu-id="566f6-112">值</span><span class="sxs-lookup"><span data-stu-id="566f6-112">Value</span></span> | <span data-ttu-id="566f6-113">描述</span><span class="sxs-lookup"><span data-stu-id="566f6-113">Description</span></span>                           |
|-------|---------------------------------------|
| <span data-ttu-id="566f6-114">0</span><span class="sxs-lookup"><span data-stu-id="566f6-114">0</span></span>     | <span data-ttu-id="566f6-115">最小品質、較小的輸出大小。</span><span class="sxs-lookup"><span data-stu-id="566f6-115">Minimum quality, smaller output size.</span></span> |
| <span data-ttu-id="566f6-116">100</span><span class="sxs-lookup"><span data-stu-id="566f6-116">100</span></span>   | <span data-ttu-id="566f6-117">品質上限，較大的輸出大小。</span><span class="sxs-lookup"><span data-stu-id="566f6-117">Maximum quality, larger output size.</span></span>  |



 

## <a name="remarks"></a><span data-ttu-id="566f6-118">備註</span><span class="sxs-lookup"><span data-stu-id="566f6-118">Remarks</span></span>

<span data-ttu-id="566f6-119">當編碼器未使用限制的位元速率時，此屬性會控制品質層級。</span><span class="sxs-lookup"><span data-stu-id="566f6-119">This property controls the quality level when the encoder is not using a constrained bit rate.</span></span> <span data-ttu-id="566f6-120">[**AVEncCommonRateControlMode**](avenccommonratecontrolmode-property.md)屬性可判斷位元速率是否受限制。</span><span class="sxs-lookup"><span data-stu-id="566f6-120">The [**AVEncCommonRateControlMode**](avenccommonratecontrolmode-property.md) property determines whether the bit rate is constrained.</span></span>

## <a name="requirements"></a><span data-ttu-id="566f6-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="566f6-121">Requirements</span></span>



| <span data-ttu-id="566f6-122">需求</span><span class="sxs-lookup"><span data-stu-id="566f6-122">Requirement</span></span> | <span data-ttu-id="566f6-123">值</span><span class="sxs-lookup"><span data-stu-id="566f6-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="566f6-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="566f6-124">Minimum supported client</span></span><br/> | <span data-ttu-id="566f6-125">Windows 2000 專業版傳統型 \[ 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="566f6-125">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="566f6-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="566f6-126">Minimum supported server</span></span><br/> | <span data-ttu-id="566f6-127">Windows 2000 Server \[ desktop 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="566f6-127">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="566f6-128">標頭</span><span class="sxs-lookup"><span data-stu-id="566f6-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="566f6-129"><dt>Codecapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="566f6-129"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="566f6-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="566f6-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="566f6-131">編解碼器 API 屬性</span><span class="sxs-lookup"><span data-stu-id="566f6-131">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="566f6-132">**ICodecAPI 介面**</span><span class="sxs-lookup"><span data-stu-id="566f6-132">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




