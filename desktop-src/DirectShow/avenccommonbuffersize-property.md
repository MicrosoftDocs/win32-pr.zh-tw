---
description: 指定編碼期間使用的緩衝區大小。 這個屬性只適用于常數的位元速率 (CBR) 和變數位元速率 (VBR) 編碼模式。
ms.assetid: 3315785e-306f-44d6-ac39-796025a2da3a
title: 'AVEncCommonBufferSize 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c677c483c320c9dceef391f45c5d8bf163eece0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109668"
---
# <a name="avenccommonbuffersize-property"></a><span data-ttu-id="cfbd5-104">AVEncCommonBufferSize 屬性</span><span class="sxs-lookup"><span data-stu-id="cfbd5-104">AVEncCommonBufferSize property</span></span>

<span data-ttu-id="cfbd5-105">指定編碼期間使用的緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="cfbd5-105">Specifies the size of the buffer used during encoding.</span></span> <span data-ttu-id="cfbd5-106">這個屬性只適用于常數的位元速率 (CBR) 和變數位元速率 (VBR) 編碼模式。</span><span class="sxs-lookup"><span data-stu-id="cfbd5-106">This property applies only to constant bit rate (CBR) and variable bit rate (VBR) encoding modes.</span></span>

<span data-ttu-id="cfbd5-107">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="cfbd5-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="cfbd5-108">資料類型</span><span class="sxs-lookup"><span data-stu-id="cfbd5-108">Data type</span></span>

<span data-ttu-id="cfbd5-109">**UINT32** (**VT \_ UI4**) </span><span class="sxs-lookup"><span data-stu-id="cfbd5-109">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="cfbd5-110">屬性 GUID</span><span class="sxs-lookup"><span data-stu-id="cfbd5-110">Property GUID</span></span>

<span data-ttu-id="cfbd5-111">**CODECAPI \_ AVEncCommonBufferSize**</span><span class="sxs-lookup"><span data-stu-id="cfbd5-111">**CODECAPI\_AVEncCommonBufferSize**</span></span>

## <a name="property-value"></a><span data-ttu-id="cfbd5-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="cfbd5-112">Property value</span></span>

<span data-ttu-id="cfbd5-113">這個屬性具有線性範圍的值。</span><span class="sxs-lookup"><span data-stu-id="cfbd5-113">This property has a linear range of values.</span></span> <span data-ttu-id="cfbd5-114">若要取得支援的範圍，請呼叫 [**ICodecAPI：： GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange)。</span><span class="sxs-lookup"><span data-stu-id="cfbd5-114">To get the supported range, call [**ICodecAPI::GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span></span> <span data-ttu-id="cfbd5-115">UVC 1.5 攝影機編碼器不支援參數範圍。</span><span class="sxs-lookup"><span data-stu-id="cfbd5-115">Parameter ranges are not supported for H.264 UVC 1.5 camera encoders.</span></span>

## <a name="remarks"></a><span data-ttu-id="cfbd5-116">備註</span><span class="sxs-lookup"><span data-stu-id="cfbd5-116">Remarks</span></span>

<span data-ttu-id="cfbd5-117">針對某些影片格式，緩衝區大小是以位指定，其他則以位元組為單位來指定。</span><span class="sxs-lookup"><span data-stu-id="cfbd5-117">For some video formats the buffer size is specified in bits and for others it is specified in bytes.</span></span> <span data-ttu-id="cfbd5-118">請參閱下面的備註，以取得特定資訊。</span><span class="sxs-lookup"><span data-stu-id="cfbd5-118">See the remarks below for specific information.</span></span>

<span data-ttu-id="cfbd5-119">針對 MPEG 影片，這個屬性會定義影片緩衝區驗證器 (VBV) 緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="cfbd5-119">For MPEG video, this property defines the video buffer verifier (VBV) buffer size.</span></span> <span data-ttu-id="cfbd5-120">緩衝區的大小是以位為單位。</span><span class="sxs-lookup"><span data-stu-id="cfbd5-120">The size of the buffer is in bits.</span></span>

<span data-ttu-id="cfbd5-121">針對 h.264 video 和 Windows Media 視訊，屬性會定義假設的參考解碼器 (HRD) 大小。</span><span class="sxs-lookup"><span data-stu-id="cfbd5-121">For H.264 video and Windows Media Video, the property defines the hypothetical reference decoder (HRD) size.</span></span> <span data-ttu-id="cfbd5-122">緩衝區的大小是以位元組為單位。</span><span class="sxs-lookup"><span data-stu-id="cfbd5-122">The size of the buffer is in bytes.</span></span>

<span data-ttu-id="cfbd5-123">針對 UVC 1.5 H264 編碼攝影機，傳送至相機編碼器的 CPB 值必須是16位的對齊方式。</span><span class="sxs-lookup"><span data-stu-id="cfbd5-123">For UVC 1.5 H264 encoding cameras, the CPB value sent to the camera encoder must be 16-bit aligned.</span></span> <span data-ttu-id="cfbd5-124">緩衝區的大小是以位元組為單位。</span><span class="sxs-lookup"><span data-stu-id="cfbd5-124">The size of the buffer is in bytes.</span></span>

<span data-ttu-id="cfbd5-125">這個屬性也會與 h.264 [UVC 1.5 攝影機編碼器](/windows/desktop/medfound/camera-encoder-h264-uvc-1-5)一起使用。</span><span class="sxs-lookup"><span data-stu-id="cfbd5-125">This property is also used with [H.264 UVC 1.5 camera encoders](/windows/desktop/medfound/camera-encoder-h264-uvc-1-5).</span></span>

## <a name="requirements"></a><span data-ttu-id="cfbd5-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="cfbd5-126">Requirements</span></span>



| <span data-ttu-id="cfbd5-127">需求</span><span class="sxs-lookup"><span data-stu-id="cfbd5-127">Requirement</span></span> | <span data-ttu-id="cfbd5-128">值</span><span class="sxs-lookup"><span data-stu-id="cfbd5-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cfbd5-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cfbd5-129">Minimum supported client</span></span><br/> | <span data-ttu-id="cfbd5-130">Windows 2000 專業版傳統型 \[ 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cfbd5-130">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="cfbd5-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cfbd5-131">Minimum supported server</span></span><br/> | <span data-ttu-id="cfbd5-132">Windows 2000 Server \[ desktop 應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cfbd5-132">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="cfbd5-133">標頭</span><span class="sxs-lookup"><span data-stu-id="cfbd5-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="cfbd5-134"><dt>Codecapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="cfbd5-134"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cfbd5-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cfbd5-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cfbd5-136">編解碼器 API 屬性</span><span class="sxs-lookup"><span data-stu-id="cfbd5-136">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="cfbd5-137">**ICodecAPI 介面**</span><span class="sxs-lookup"><span data-stu-id="cfbd5-137">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

