---
description: 設定編碼器將「影片」欄位視為多餘的閾值。
ms.assetid: db6c2f0e-f451-4d2d-984f-b507083e8358
title: 'AVEncVideoInverseTelecineThreshold 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3427a8ff1491277c2e36640560acf728c0ef7208
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103687507"
---
# <a name="avencvideoinversetelecinethreshold-property"></a><span data-ttu-id="ac87d-103">AVEncVideoInverseTelecineThreshold 屬性</span><span class="sxs-lookup"><span data-stu-id="ac87d-103">AVEncVideoInverseTelecineThreshold property</span></span>

<span data-ttu-id="ac87d-104">設定編碼器將「影片」欄位視為多餘的閾值。</span><span class="sxs-lookup"><span data-stu-id="ac87d-104">Sets the threshold at which the encoder considers a video field redundant.</span></span>

<span data-ttu-id="ac87d-105">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="ac87d-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="ac87d-106">資料類型</span><span class="sxs-lookup"><span data-stu-id="ac87d-106">Data type</span></span>

<span data-ttu-id="ac87d-107">**UINT32** (**VT \_ UI4**) </span><span class="sxs-lookup"><span data-stu-id="ac87d-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="ac87d-108">屬性 GUID</span><span class="sxs-lookup"><span data-stu-id="ac87d-108">Property GUID</span></span>

<span data-ttu-id="ac87d-109">**CODECAPI \_ AVEncVideoInverseTelecineThreshold**</span><span class="sxs-lookup"><span data-stu-id="ac87d-109">**CODECAPI\_AVEncVideoInverseTelecineThreshold**</span></span>

## <a name="property-value"></a><span data-ttu-id="ac87d-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="ac87d-110">Property value</span></span>

<span data-ttu-id="ac87d-111">這個屬性的值具有下列範圍。</span><span class="sxs-lookup"><span data-stu-id="ac87d-111">The value of this property has the following range.</span></span>



| <span data-ttu-id="ac87d-112">值</span><span class="sxs-lookup"><span data-stu-id="ac87d-112">Value</span></span> | <span data-ttu-id="ac87d-113">描述</span><span class="sxs-lookup"><span data-stu-id="ac87d-113">Description</span></span>                                                    |
|-------|----------------------------------------------------------------|
| <span data-ttu-id="ac87d-114">0</span><span class="sxs-lookup"><span data-stu-id="ac87d-114">0</span></span>     | <span data-ttu-id="ac87d-115">編碼器較不可能將影片欄位視為多餘。</span><span class="sxs-lookup"><span data-stu-id="ac87d-115">The encoder is less likely to consider video fields redundant.</span></span> |
| <span data-ttu-id="ac87d-116">100</span><span class="sxs-lookup"><span data-stu-id="ac87d-116">100</span></span>   | <span data-ttu-id="ac87d-117">編碼器更可能將影片欄位視為多餘的。</span><span class="sxs-lookup"><span data-stu-id="ac87d-117">The encoder is more likely to consider video fields redundant.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="ac87d-118">備註</span><span class="sxs-lookup"><span data-stu-id="ac87d-118">Remarks</span></span>

<span data-ttu-id="ac87d-119">如果編碼器正在使用類比影片來源執行反向電視電影，請設定此屬性。</span><span class="sxs-lookup"><span data-stu-id="ac87d-119">Set this property if the encoder is performing inverse telecine with an analog video source.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac87d-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="ac87d-120">Requirements</span></span>



| <span data-ttu-id="ac87d-121">需求</span><span class="sxs-lookup"><span data-stu-id="ac87d-121">Requirement</span></span> | <span data-ttu-id="ac87d-122">值</span><span class="sxs-lookup"><span data-stu-id="ac87d-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ac87d-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ac87d-123">Minimum supported client</span></span><br/> | <span data-ttu-id="ac87d-124">Windows 2000 專業版傳統型 \[ 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ac87d-124">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="ac87d-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ac87d-125">Minimum supported server</span></span><br/> | <span data-ttu-id="ac87d-126">Windows 2000 Server \[ desktop 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ac87d-126">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="ac87d-127">標頭</span><span class="sxs-lookup"><span data-stu-id="ac87d-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="ac87d-128"><dt>Codecapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="ac87d-128"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac87d-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ac87d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac87d-130">編解碼器 API 屬性</span><span class="sxs-lookup"><span data-stu-id="ac87d-130">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="ac87d-131">**ICodecAPI 介面**</span><span class="sxs-lookup"><span data-stu-id="ac87d-131">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




