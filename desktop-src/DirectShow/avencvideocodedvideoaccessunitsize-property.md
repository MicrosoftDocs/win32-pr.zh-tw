---
description: 指定影片存取單位的大小（以位元組為單位）。 這個屬性只適用于變數的位元速率 (VBR) 控制項模式。
ms.assetid: bb46b171-d70a-4e01-88c4-321a210a0220
title: 'AVEncVideoCodedVideoAccessUnitSize 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be3a6e499749d862fdcc63f28b1a9a02f476d1c7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103935640"
---
# <a name="avencvideocodedvideoaccessunitsize-property"></a><span data-ttu-id="fbc71-104">AVEncVideoCodedVideoAccessUnitSize 屬性</span><span class="sxs-lookup"><span data-stu-id="fbc71-104">AVEncVideoCodedVideoAccessUnitSize property</span></span>

<span data-ttu-id="fbc71-105">指定影片存取單位的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="fbc71-105">Specifies the size of the video access units, in bytes.</span></span> <span data-ttu-id="fbc71-106">這個屬性只適用于變數的位元速率 (VBR) 控制項模式。</span><span class="sxs-lookup"><span data-stu-id="fbc71-106">This property applies only to variable bit rate (VBR) control modes.</span></span>

<span data-ttu-id="fbc71-107">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="fbc71-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="fbc71-108">資料類型</span><span class="sxs-lookup"><span data-stu-id="fbc71-108">Data type</span></span>

<span data-ttu-id="fbc71-109">**UINT32** (**VT \_ UI4**) </span><span class="sxs-lookup"><span data-stu-id="fbc71-109">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="fbc71-110">屬性 GUID</span><span class="sxs-lookup"><span data-stu-id="fbc71-110">Property GUID</span></span>

<span data-ttu-id="fbc71-111">**CODECAPI \_ AVEncVideoCodedVideoAccessUnitSize**</span><span class="sxs-lookup"><span data-stu-id="fbc71-111">**CODECAPI\_AVEncVideoCodedVideoAccessUnitSize**</span></span>

## <a name="property-value"></a><span data-ttu-id="fbc71-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="fbc71-112">Property value</span></span>

<span data-ttu-id="fbc71-113">這個屬性會以值範圍的形式傳回。</span><span class="sxs-lookup"><span data-stu-id="fbc71-113">This property is returned as a range of values.</span></span> <span data-ttu-id="fbc71-114">若要取得支援的範圍，請呼叫 [**ICodecAPI：： GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange)。</span><span class="sxs-lookup"><span data-stu-id="fbc71-114">To get the supported range, call [**ICodecAPI::GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span></span>

## <a name="requirements"></a><span data-ttu-id="fbc71-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="fbc71-115">Requirements</span></span>



| <span data-ttu-id="fbc71-116">需求</span><span class="sxs-lookup"><span data-stu-id="fbc71-116">Requirement</span></span> | <span data-ttu-id="fbc71-117">值</span><span class="sxs-lookup"><span data-stu-id="fbc71-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fbc71-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fbc71-118">Minimum supported client</span></span><br/> | <span data-ttu-id="fbc71-119">Windows 2000 專業版傳統型 \[ 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fbc71-119">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="fbc71-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fbc71-120">Minimum supported server</span></span><br/> | <span data-ttu-id="fbc71-121">Windows 2000 Server \[ desktop 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fbc71-121">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="fbc71-122">標頭</span><span class="sxs-lookup"><span data-stu-id="fbc71-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="fbc71-123"><dt>Codecapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="fbc71-123"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fbc71-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fbc71-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fbc71-125">編解碼器 API 屬性</span><span class="sxs-lookup"><span data-stu-id="fbc71-125">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="fbc71-126">**ICodecAPI 介面**</span><span class="sxs-lookup"><span data-stu-id="fbc71-126">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




