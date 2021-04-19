---
description: 在編碼程式結束時，指定編碼緩衝區的最終層級（以位為單位）。 這個屬性只適用于常數的位元速率 (CBR) 和變數位元速率 (VBR) 編碼模式。
ms.assetid: d5bcdf54-061a-436b-8b1a-61ef7d7c90bf
title: 'AVEncCommonBufferOutLevel 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90d99cdea909a1fd1c3777aac4868a570161c3fc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106972317"
---
# <a name="avenccommonbufferoutlevel-property"></a><span data-ttu-id="177e8-104">AVEncCommonBufferOutLevel 屬性</span><span class="sxs-lookup"><span data-stu-id="177e8-104">AVEncCommonBufferOutLevel property</span></span>

<span data-ttu-id="177e8-105">在編碼程式結束時，指定編碼緩衝區的最終層級（以位為單位）。</span><span class="sxs-lookup"><span data-stu-id="177e8-105">Specifies the final level of the encoding buffer, in bits, at the end of the encoding process.</span></span> <span data-ttu-id="177e8-106">這個屬性只適用于常數的位元速率 (CBR) 和變數位元速率 (VBR) 編碼模式。</span><span class="sxs-lookup"><span data-stu-id="177e8-106">This property applies only to constant bit rate (CBR) and variable bit rate (VBR) encoding modes.</span></span>

<span data-ttu-id="177e8-107">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="177e8-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="177e8-108">資料類型</span><span class="sxs-lookup"><span data-stu-id="177e8-108">Data type</span></span>

<span data-ttu-id="177e8-109">**UINT32** (**VT \_ UI4**) </span><span class="sxs-lookup"><span data-stu-id="177e8-109">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="177e8-110">屬性 GUID</span><span class="sxs-lookup"><span data-stu-id="177e8-110">Property GUID</span></span>

<span data-ttu-id="177e8-111">**CODECAPI \_ AVEncCommonBufferOutLevel**</span><span class="sxs-lookup"><span data-stu-id="177e8-111">**CODECAPI\_AVEncCommonBufferOutLevel**</span></span>

## <a name="property-value"></a><span data-ttu-id="177e8-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="177e8-112">Property value</span></span>

<span data-ttu-id="177e8-113">這個屬性具有線性範圍的值。</span><span class="sxs-lookup"><span data-stu-id="177e8-113">This property has a linear range of values.</span></span> <span data-ttu-id="177e8-114">若要取得支援的範圍，請呼叫 [**ICodecAPI：： GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange)。</span><span class="sxs-lookup"><span data-stu-id="177e8-114">To get the supported range, call [**ICodecAPI::GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span></span>

## <a name="remarks"></a><span data-ttu-id="177e8-115">備註</span><span class="sxs-lookup"><span data-stu-id="177e8-115">Remarks</span></span>

<span data-ttu-id="177e8-116">只有在使用 [**AVEncVideoNoOfFieldsToEncode**](avencvideonooffieldstoencode-property.md) 屬性或 [**AVEncAudioIntervalToEncode**](avencaudiointervaltoencode-property.md) 屬性預先定義編碼期間時，才能使用此屬性。</span><span class="sxs-lookup"><span data-stu-id="177e8-116">The property is available only if the encoding duration is defined in advance, using the [**AVEncVideoNoOfFieldsToEncode**](avencvideonooffieldstoencode-property.md) property or [**AVEncAudioIntervalToEncode**](avencaudiointervaltoencode-property.md) property.</span></span>

<span data-ttu-id="177e8-117">針對 MPEG 影片，這個屬性會定義影片緩衝區驗證器 (VBV 在編碼程式結束時) 飽和度。</span><span class="sxs-lookup"><span data-stu-id="177e8-117">For MPEG video, this property defines the video buffer verifier (VBV) fullness at the end of the encoding process.</span></span> <span data-ttu-id="177e8-118">它支援在編碼期間串連資料流程。</span><span class="sxs-lookup"><span data-stu-id="177e8-118">It supports the concatenation of streams during encoding.</span></span>

## <a name="requirements"></a><span data-ttu-id="177e8-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="177e8-119">Requirements</span></span>



| <span data-ttu-id="177e8-120">需求</span><span class="sxs-lookup"><span data-stu-id="177e8-120">Requirement</span></span> | <span data-ttu-id="177e8-121">值</span><span class="sxs-lookup"><span data-stu-id="177e8-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="177e8-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="177e8-122">Minimum supported client</span></span><br/> | <span data-ttu-id="177e8-123">Windows 2000 專業版傳統型 \[ 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="177e8-123">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="177e8-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="177e8-124">Minimum supported server</span></span><br/> | <span data-ttu-id="177e8-125">Windows 2000 Server \[ desktop 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="177e8-125">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="177e8-126">標頭</span><span class="sxs-lookup"><span data-stu-id="177e8-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="177e8-127"><dt>Codecapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="177e8-127"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="177e8-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="177e8-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="177e8-129">編解碼器 API 屬性</span><span class="sxs-lookup"><span data-stu-id="177e8-129">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="177e8-130">**ICodecAPI 介面**</span><span class="sxs-lookup"><span data-stu-id="177e8-130">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




