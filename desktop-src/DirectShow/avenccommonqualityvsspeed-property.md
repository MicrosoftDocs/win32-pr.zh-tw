---
description: 指定編碼品質與速度之間的取捨。 此屬性在所有速率控制模式中都是有效的。
ms.assetid: d721a50d-dec9-4e2d-bda5-25913f225d68
title: 'AVEncCommonQualityVsSpeed 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d8af65f816bc9be6642e2a23ee4dc05e2e4fa40
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109664"
---
# <a name="avenccommonqualityvsspeed-property"></a><span data-ttu-id="c6433-104">AVEncCommonQualityVsSpeed 屬性</span><span class="sxs-lookup"><span data-stu-id="c6433-104">AVEncCommonQualityVsSpeed property</span></span>

<span data-ttu-id="c6433-105">指定編碼品質與速度之間的取捨。</span><span class="sxs-lookup"><span data-stu-id="c6433-105">Specifies the tradeoff between encoding quality and speed.</span></span> <span data-ttu-id="c6433-106">此屬性在所有速率控制模式中都是有效的。</span><span class="sxs-lookup"><span data-stu-id="c6433-106">This property is valid in all rate control modes.</span></span>

<span data-ttu-id="c6433-107">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="c6433-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="c6433-108">資料類型</span><span class="sxs-lookup"><span data-stu-id="c6433-108">Data type</span></span>

<span data-ttu-id="c6433-109">**UINT32** (**VT \_ UI4**) </span><span class="sxs-lookup"><span data-stu-id="c6433-109">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="c6433-110">屬性 GUID</span><span class="sxs-lookup"><span data-stu-id="c6433-110">Property GUID</span></span>

<span data-ttu-id="c6433-111">**CODECAPI \_ AVEncCommonQualityVsSpeed**</span><span class="sxs-lookup"><span data-stu-id="c6433-111">**CODECAPI\_AVEncCommonQualityVsSpeed**</span></span>

## <a name="property-value"></a><span data-ttu-id="c6433-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="c6433-112">Property value</span></span>

<span data-ttu-id="c6433-113">這個屬性的值具有下列範圍。</span><span class="sxs-lookup"><span data-stu-id="c6433-113">The value of this property has the following range.</span></span>



| <span data-ttu-id="c6433-114">值</span><span class="sxs-lookup"><span data-stu-id="c6433-114">Value</span></span> | <span data-ttu-id="c6433-115">描述</span><span class="sxs-lookup"><span data-stu-id="c6433-115">Description</span></span>                      |
|-------|----------------------------------|
| <span data-ttu-id="c6433-116">0</span><span class="sxs-lookup"><span data-stu-id="c6433-116">0</span></span>     | <span data-ttu-id="c6433-117">較低的品質、更快速的編碼方式。</span><span class="sxs-lookup"><span data-stu-id="c6433-117">Lower quality, faster encoding.</span></span>  |
| <span data-ttu-id="c6433-118">100</span><span class="sxs-lookup"><span data-stu-id="c6433-118">100</span></span>   | <span data-ttu-id="c6433-119">品質較高、速度較慢的編碼。</span><span class="sxs-lookup"><span data-stu-id="c6433-119">Higher quality, slower encoding.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="c6433-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="c6433-120">Requirements</span></span>



| <span data-ttu-id="c6433-121">需求</span><span class="sxs-lookup"><span data-stu-id="c6433-121">Requirement</span></span> | <span data-ttu-id="c6433-122">值</span><span class="sxs-lookup"><span data-stu-id="c6433-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c6433-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c6433-123">Minimum supported client</span></span><br/> | <span data-ttu-id="c6433-124">Windows 2000 專業版傳統型 \[ 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c6433-124">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="c6433-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c6433-125">Minimum supported server</span></span><br/> | <span data-ttu-id="c6433-126">Windows 2000 Server \[ desktop 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c6433-126">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="c6433-127">標頭</span><span class="sxs-lookup"><span data-stu-id="c6433-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="c6433-128"><dt>Codecapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="c6433-128"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6433-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c6433-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6433-130">編解碼器 API 屬性</span><span class="sxs-lookup"><span data-stu-id="c6433-130">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="c6433-131">**ICodecAPI 介面**</span><span class="sxs-lookup"><span data-stu-id="c6433-131">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




