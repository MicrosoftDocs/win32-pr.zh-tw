---
description: 指定移動與靜止影像之間的取捨。 這個屬性只適用于常數的位元速率 (CBR) 控制模式。
ms.assetid: e657e971-4624-4c87-ad51-6bf0cd1f9246
title: 'AVEncVideoCBRMotionTradeoff 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b746559f48858f995cbd87184a2f13ada33db7c4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103935941"
---
# <a name="avencvideocbrmotiontradeoff-property"></a><span data-ttu-id="41295-104">AVEncVideoCBRMotionTradeoff 屬性</span><span class="sxs-lookup"><span data-stu-id="41295-104">AVEncVideoCBRMotionTradeoff property</span></span>

<span data-ttu-id="41295-105">指定移動與靜止影像之間的取捨。</span><span class="sxs-lookup"><span data-stu-id="41295-105">Specifies the tradeoff between motion and still images.</span></span> <span data-ttu-id="41295-106">這個屬性只適用于常數的位元速率 (CBR) 控制模式。</span><span class="sxs-lookup"><span data-stu-id="41295-106">This property applies only to constant bit rate (CBR) control mode.</span></span>

<span data-ttu-id="41295-107">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="41295-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="41295-108">資料類型</span><span class="sxs-lookup"><span data-stu-id="41295-108">Data type</span></span>

<span data-ttu-id="41295-109">**UINT32** (**VT \_ UI4**) </span><span class="sxs-lookup"><span data-stu-id="41295-109">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="41295-110">屬性 GUID</span><span class="sxs-lookup"><span data-stu-id="41295-110">Property GUID</span></span>

<span data-ttu-id="41295-111">**CODECAPI \_ AVEncVideoCBRMotionTradeoff**</span><span class="sxs-lookup"><span data-stu-id="41295-111">**CODECAPI\_AVEncVideoCBRMotionTradeoff**</span></span>

## <a name="property-value"></a><span data-ttu-id="41295-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="41295-112">Property value</span></span>

<span data-ttu-id="41295-113">這個屬性的值具有下列範圍。</span><span class="sxs-lookup"><span data-stu-id="41295-113">The value of this property has the following range.</span></span>



| <span data-ttu-id="41295-114">值</span><span class="sxs-lookup"><span data-stu-id="41295-114">Value</span></span> | <span data-ttu-id="41295-115">描述</span><span class="sxs-lookup"><span data-stu-id="41295-115">Description</span></span>               |
|-------|---------------------------|
| <span data-ttu-id="41295-116">0</span><span class="sxs-lookup"><span data-stu-id="41295-116">0</span></span>     | <span data-ttu-id="41295-117">針對靜止影像優化</span><span class="sxs-lookup"><span data-stu-id="41295-117">Optimize for still images</span></span> |
| <span data-ttu-id="41295-118">100</span><span class="sxs-lookup"><span data-stu-id="41295-118">100</span></span>   | <span data-ttu-id="41295-119">優化動作。</span><span class="sxs-lookup"><span data-stu-id="41295-119">Optimize for motion.</span></span>      |



 

## <a name="requirements"></a><span data-ttu-id="41295-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="41295-120">Requirements</span></span>



| <span data-ttu-id="41295-121">需求</span><span class="sxs-lookup"><span data-stu-id="41295-121">Requirement</span></span> | <span data-ttu-id="41295-122">值</span><span class="sxs-lookup"><span data-stu-id="41295-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="41295-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="41295-123">Minimum supported client</span></span><br/> | <span data-ttu-id="41295-124">Windows 2000 專業版傳統型 \[ 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="41295-124">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="41295-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="41295-125">Minimum supported server</span></span><br/> | <span data-ttu-id="41295-126">Windows 2000 Server \[ desktop 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="41295-126">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="41295-127">標頭</span><span class="sxs-lookup"><span data-stu-id="41295-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="41295-128"><dt>Codecapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="41295-128"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41295-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="41295-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41295-130">編解碼器 API 屬性</span><span class="sxs-lookup"><span data-stu-id="41295-130">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="41295-131">**ICodecAPI 介面**</span><span class="sxs-lookup"><span data-stu-id="41295-131">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




