---
description: GetCurrentImage 方法會在轉譯器上抓取目前影像的複本。
ms.assetid: fa322bd2-18e4-481d-bde1-92deb0f7de61
title: 'CBaseControlVideo. GetCurrentImage 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.GetCurrentImage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d44e6930d0d7e179162939c13a54f2953c5ab965
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106997804"
---
# <a name="cbasecontrolvideogetcurrentimage-method"></a><span data-ttu-id="a5625-103">CBaseControlVideo. GetCurrentImage 方法</span><span class="sxs-lookup"><span data-stu-id="a5625-103">CBaseControlVideo.GetCurrentImage method</span></span>

<span data-ttu-id="a5625-104">方法會在轉譯器 `GetCurrentImage` 上抓取目前影像的複本。</span><span class="sxs-lookup"><span data-stu-id="a5625-104">The `GetCurrentImage` method retrieves a copy of the current image at the renderer.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5625-105">語法</span><span class="sxs-lookup"><span data-stu-id="a5625-105">Syntax</span></span>


```C++
HRESULT GetCurrentImage(
   long *pBufferSize,
   long *pVideoImage
);
```



## <a name="parameters"></a><span data-ttu-id="a5625-106">參數</span><span class="sxs-lookup"><span data-stu-id="a5625-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5625-107">*pBufferSize*</span><span class="sxs-lookup"><span data-stu-id="a5625-107">*pBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="a5625-108">輸出緩衝區大小的指標。</span><span class="sxs-lookup"><span data-stu-id="a5625-108">Pointer to the size of the output buffer.</span></span>

</dd> <dt>

<span data-ttu-id="a5625-109">*pVideoImage*</span><span class="sxs-lookup"><span data-stu-id="a5625-109">*pVideoImage*</span></span> 
</dt> <dd>

<span data-ttu-id="a5625-110">影像輸出緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="a5625-110">Pointer to the output buffer for the image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a5625-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="a5625-111">Return value</span></span>

<span data-ttu-id="a5625-112">傳回相依于實值的 **HRESULT** 值。可以是下列其中一個值，或其他未列出的值。</span><span class="sxs-lookup"><span data-stu-id="a5625-112">Returns an **HRESULT** value that depends on the implementation; can be one of the following values, or other values not listed.</span></span>



| <span data-ttu-id="a5625-113">傳回碼</span><span class="sxs-lookup"><span data-stu-id="a5625-113">Return code</span></span>                                                                                        | <span data-ttu-id="a5625-114">Description</span><span class="sxs-lookup"><span data-stu-id="a5625-114">Description</span></span>                                                                       |
|----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a5625-115"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="a5625-115"><dt>**E\_FAIL**</dt></span></span> </dl>             | <span data-ttu-id="a5625-116">失敗。</span><span class="sxs-lookup"><span data-stu-id="a5625-116">Failure.</span></span><br/>                                                               |
| <dl> <span data-ttu-id="a5625-117"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="a5625-117"><dt>**E\_INVALIDARG**</dt></span></span> </dl>       | <span data-ttu-id="a5625-118">無效引數。</span><span class="sxs-lookup"><span data-stu-id="a5625-118">Invalid argument.</span></span><br/>                                                      |
| <dl> <span data-ttu-id="a5625-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="a5625-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>      | <span data-ttu-id="a5625-120">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="a5625-120">Out of memory.</span></span> <span data-ttu-id="a5625-121">當 *pVideoInfo* 參數為 **Null** 時傳回。</span><span class="sxs-lookup"><span data-stu-id="a5625-121">Returned when the *pVideoInfo* parameter is **NULL**.</span></span><br/>   |
| <dl> <span data-ttu-id="a5625-122"><dt>**NOERROR**</dt></span><span class="sxs-lookup"><span data-stu-id="a5625-122"><dt>**NOERROR**</dt></span></span> </dl>             | <span data-ttu-id="a5625-123">成功。</span><span class="sxs-lookup"><span data-stu-id="a5625-123">Success.</span></span><br/>                                                               |
| <dl> <span data-ttu-id="a5625-124"><dt>**VFW \_ E \_ 未 \_ 暫停**</dt></span><span class="sxs-lookup"><span data-stu-id="a5625-124"><dt>**VFW\_E\_NOT\_PAUSED**</dt></span></span> </dl> | <span data-ttu-id="a5625-125">無法執行操作，因為篩選未暫停。</span><span class="sxs-lookup"><span data-stu-id="a5625-125">The operation could not be performed because the filter is not paused.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a5625-126">備註</span><span class="sxs-lookup"><span data-stu-id="a5625-126">Remarks</span></span>

<span data-ttu-id="a5625-127">此成員函式會從範例抓取影像，並將它複製到輸出緩衝區。</span><span class="sxs-lookup"><span data-stu-id="a5625-127">This member function retrieves the image from the sample and copies it into the output buffer.</span></span> <span data-ttu-id="a5625-128">複製到輸出緩衝區的影片區段會反映透過 [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) 介面設定的來源矩形。</span><span class="sxs-lookup"><span data-stu-id="a5625-128">The section of video copied into the output buffer reflects the source rectangle set through the [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) interface.</span></span> <span data-ttu-id="a5625-129">它不會反映目的地矩形。</span><span class="sxs-lookup"><span data-stu-id="a5625-129">It does not reflect the destination rectangle.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5625-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="a5625-130">Requirements</span></span>



| <span data-ttu-id="a5625-131">需求</span><span class="sxs-lookup"><span data-stu-id="a5625-131">Requirement</span></span> | <span data-ttu-id="a5625-132">值</span><span class="sxs-lookup"><span data-stu-id="a5625-132">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5625-133">標頭</span><span class="sxs-lookup"><span data-stu-id="a5625-133">Header</span></span><br/>  | <dl> <span data-ttu-id="a5625-134"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="a5625-134"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a5625-135">程式庫</span><span class="sxs-lookup"><span data-stu-id="a5625-135">Library</span></span><br/> | <dl> <span data-ttu-id="a5625-136"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="a5625-136"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a5625-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a5625-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5625-138">**CBaseControlVideo 類別**</span><span class="sxs-lookup"><span data-stu-id="a5625-138">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




