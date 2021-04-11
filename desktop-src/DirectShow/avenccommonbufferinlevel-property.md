---
description: 指定編碼緩衝區的初始層級（以位為單位）。 這個屬性只適用于常數的位元速率 (CBR) 和變數位元速率 (VBR) 編碼模式。
ms.assetid: 92ec9483-443e-4723-8795-9bf847c36131
title: 'AVEncCommonBufferInLevel 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8219ab951fb68cd5dfc04e0b5415d77fe674e763
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109669"
---
# <a name="avenccommonbufferinlevel-property"></a><span data-ttu-id="3a4fb-104">AVEncCommonBufferInLevel 屬性</span><span class="sxs-lookup"><span data-stu-id="3a4fb-104">AVEncCommonBufferInLevel property</span></span>

<span data-ttu-id="3a4fb-105">指定編碼緩衝區的初始層級（以位為單位）。</span><span class="sxs-lookup"><span data-stu-id="3a4fb-105">Specifies the initial level of the encoding buffer, in bits.</span></span> <span data-ttu-id="3a4fb-106">這個屬性只適用于常數的位元速率 (CBR) 和變數位元速率 (VBR) 編碼模式。</span><span class="sxs-lookup"><span data-stu-id="3a4fb-106">This property applies only to constant bit rate (CBR) and variable bit rate (VBR) encoding modes.</span></span>

<span data-ttu-id="3a4fb-107">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="3a4fb-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="3a4fb-108">資料類型</span><span class="sxs-lookup"><span data-stu-id="3a4fb-108">Data type</span></span>

<span data-ttu-id="3a4fb-109">**UINT32** (**VT \_ UI4**) </span><span class="sxs-lookup"><span data-stu-id="3a4fb-109">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="3a4fb-110">屬性 GUID</span><span class="sxs-lookup"><span data-stu-id="3a4fb-110">Property GUID</span></span>

<span data-ttu-id="3a4fb-111">**CODECAPI \_ AVEncCommonBufferInLevel**</span><span class="sxs-lookup"><span data-stu-id="3a4fb-111">**CODECAPI\_AVEncCommonBufferInLevel**</span></span>

## <a name="property-value"></a><span data-ttu-id="3a4fb-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="3a4fb-112">Property value</span></span>

<span data-ttu-id="3a4fb-113">這個屬性具有線性範圍的值。</span><span class="sxs-lookup"><span data-stu-id="3a4fb-113">This property has a linear range of values.</span></span> <span data-ttu-id="3a4fb-114">若要取得支援的範圍，請呼叫 [**ICodecAPI：： GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange)。</span><span class="sxs-lookup"><span data-stu-id="3a4fb-114">To get the supported range, call [**ICodecAPI::GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span></span>

## <a name="remarks"></a><span data-ttu-id="3a4fb-115">備註</span><span class="sxs-lookup"><span data-stu-id="3a4fb-115">Remarks</span></span>

<span data-ttu-id="3a4fb-116">針對 MPEG 影片，這個屬性會定義初始的影片緩衝區驗證器 (VBV) 飽和度。</span><span class="sxs-lookup"><span data-stu-id="3a4fb-116">For MPEG video, this property defines the initial video buffer verifier (VBV) fullness.</span></span> <span data-ttu-id="3a4fb-117">它支援在編碼期間串連資料流程。</span><span class="sxs-lookup"><span data-stu-id="3a4fb-117">It supports the concatenation of streams during encoding.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a4fb-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="3a4fb-118">Requirements</span></span>



| <span data-ttu-id="3a4fb-119">需求</span><span class="sxs-lookup"><span data-stu-id="3a4fb-119">Requirement</span></span> | <span data-ttu-id="3a4fb-120">值</span><span class="sxs-lookup"><span data-stu-id="3a4fb-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3a4fb-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3a4fb-121">Minimum supported client</span></span><br/> | <span data-ttu-id="3a4fb-122">Windows 2000 專業版傳統型 \[ 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3a4fb-122">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="3a4fb-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3a4fb-123">Minimum supported server</span></span><br/> | <span data-ttu-id="3a4fb-124">Windows 2000 Server \[ desktop 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3a4fb-124">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="3a4fb-125">標頭</span><span class="sxs-lookup"><span data-stu-id="3a4fb-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="3a4fb-126"><dt>Codecapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="3a4fb-126"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a4fb-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3a4fb-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a4fb-128">編解碼器 API 屬性</span><span class="sxs-lookup"><span data-stu-id="3a4fb-128">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="3a4fb-129">**ICodecAPI 介面**</span><span class="sxs-lookup"><span data-stu-id="3a4fb-129">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




