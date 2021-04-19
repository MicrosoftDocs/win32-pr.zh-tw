---
description: GetImageSize 方法會捕獲影片影像大小資訊。
ms.assetid: a6d7f949-c6a9-49e9-b10a-f6f5bd73dc00
title: 'CBaseControlVideo. GetImageSize 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.GetImageSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ed7795e3998bc101e907bce87c9981e86f51fcb6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978526"
---
# <a name="cbasecontrolvideogetimagesize-method"></a><span data-ttu-id="57ae7-103">CBaseControlVideo. GetImageSize 方法</span><span class="sxs-lookup"><span data-stu-id="57ae7-103">CBaseControlVideo.GetImageSize method</span></span>

<span data-ttu-id="57ae7-104">`GetImageSize`方法會捕獲影片影像大小資訊。</span><span class="sxs-lookup"><span data-stu-id="57ae7-104">The `GetImageSize` method retrieves video image size information.</span></span>

## <a name="syntax"></a><span data-ttu-id="57ae7-105">語法</span><span class="sxs-lookup"><span data-stu-id="57ae7-105">Syntax</span></span>


```C++
HRESULT GetImageSize(
   VIDEOINFOHEADER *pVideoInfo,
   long            *pBufferSize,
   RECT            *pSourceRect
);
```



## <a name="parameters"></a><span data-ttu-id="57ae7-106">參數</span><span class="sxs-lookup"><span data-stu-id="57ae7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57ae7-107">*pVideoInfo*</span><span class="sxs-lookup"><span data-stu-id="57ae7-107">*pVideoInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="57ae7-108">要填入之 [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="57ae7-108">Pointer to a [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure to be filled in.</span></span>

</dd> <dt>

<span data-ttu-id="57ae7-109">*pBufferSize*</span><span class="sxs-lookup"><span data-stu-id="57ae7-109">*pBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="57ae7-110">影片緩衝區大小的指標。</span><span class="sxs-lookup"><span data-stu-id="57ae7-110">Pointer to the size of the video buffer.</span></span>

</dd> <dt>

<span data-ttu-id="57ae7-111">*pSourceRect*</span><span class="sxs-lookup"><span data-stu-id="57ae7-111">*pSourceRect*</span></span> 
</dt> <dd>

<span data-ttu-id="57ae7-112">來源影片的矩形維度指標。</span><span class="sxs-lookup"><span data-stu-id="57ae7-112">Pointer to the rectangle dimensions of the source video.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57ae7-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="57ae7-113">Return value</span></span>

<span data-ttu-id="57ae7-114">傳回相依于實值的 **HRESULT** 值。可以是下列其中一個值，或其他未列出的值。</span><span class="sxs-lookup"><span data-stu-id="57ae7-114">Returns an **HRESULT** value that depends on the implementation; can be one of the following values, or other values not listed.</span></span>



| <span data-ttu-id="57ae7-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="57ae7-115">Return code</span></span>                                                                                  | <span data-ttu-id="57ae7-116">Description</span><span class="sxs-lookup"><span data-stu-id="57ae7-116">Description</span></span>                                                               |
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <span data-ttu-id="57ae7-117"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="57ae7-117"><dt>**E\_FAIL**</dt></span></span> </dl>       | <span data-ttu-id="57ae7-118">失敗。</span><span class="sxs-lookup"><span data-stu-id="57ae7-118">Failure.</span></span><br/>                                                       |
| <dl> <span data-ttu-id="57ae7-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="57ae7-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="57ae7-120">無效引數。</span><span class="sxs-lookup"><span data-stu-id="57ae7-120">Invalid argument.</span></span> <span data-ttu-id="57ae7-121">資料格式不相容。</span><span class="sxs-lookup"><span data-stu-id="57ae7-121">The data format is not compatible.</span></span><br/>           |
| <dl> <span data-ttu-id="57ae7-122"><dt>**E 未 \_ 預期**</dt></span><span class="sxs-lookup"><span data-stu-id="57ae7-122"><dt>**E\_UNEXPECTED**</dt></span></span> </dl> | <span data-ttu-id="57ae7-123">發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="57ae7-123">Unexpected error occurred.</span></span> <span data-ttu-id="57ae7-124">一或多個引數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="57ae7-124">One or more arguments are **NULL**.</span></span><br/> |
| <dl> <span data-ttu-id="57ae7-125"><dt>**NOERROR**</dt></span><span class="sxs-lookup"><span data-stu-id="57ae7-125"><dt>**NOERROR**</dt></span></span> </dl>       | <span data-ttu-id="57ae7-126">成功。</span><span class="sxs-lookup"><span data-stu-id="57ae7-126">Success.</span></span><br/>                                                       |



 

## <a name="remarks"></a><span data-ttu-id="57ae7-127">備註</span><span class="sxs-lookup"><span data-stu-id="57ae7-127">Remarks</span></span>

<span data-ttu-id="57ae7-128">此成員函式是用來建立 DIB 映射之記憶體影像轉譯的 helper 函式。</span><span class="sxs-lookup"><span data-stu-id="57ae7-128">This member function is a helper function used for creating memory image renderings of DIB images.</span></span> <span data-ttu-id="57ae7-129">當 **Null**_pVideoImage_ 參數傳遞至該成員函式時，它會從 [**CBaseControlVideo：： GetCurrentImage**](cbasecontrolvideo-getcurrentimage.md)的基類實作為呼叫。</span><span class="sxs-lookup"><span data-stu-id="57ae7-129">It is called from the base class implementation of [**CBaseControlVideo::GetCurrentImage**](cbasecontrolvideo-getcurrentimage.md) when a **NULL**_pVideoImage_ parameter is passed to that member function.</span></span> <span data-ttu-id="57ae7-130">如此一來，這個成員函式會使用 *pBufferSize* 和 *pSourceRect* 中的資訊來建立並傳回 [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader)結構。</span><span class="sxs-lookup"><span data-stu-id="57ae7-130">As a result, this member function constructs and returns a [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure, using the information in *pBufferSize* and *pSourceRect*.</span></span>

## <a name="requirements"></a><span data-ttu-id="57ae7-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="57ae7-131">Requirements</span></span>



| <span data-ttu-id="57ae7-132">需求</span><span class="sxs-lookup"><span data-stu-id="57ae7-132">Requirement</span></span> | <span data-ttu-id="57ae7-133">值</span><span class="sxs-lookup"><span data-stu-id="57ae7-133">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="57ae7-134">標頭</span><span class="sxs-lookup"><span data-stu-id="57ae7-134">Header</span></span><br/>  | <dl> <span data-ttu-id="57ae7-135"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="57ae7-135"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="57ae7-136">程式庫</span><span class="sxs-lookup"><span data-stu-id="57ae7-136">Library</span></span><br/> | <dl> <span data-ttu-id="57ae7-137"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="57ae7-137"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="57ae7-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="57ae7-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57ae7-139">**CBaseControlVideo 類別**</span><span class="sxs-lookup"><span data-stu-id="57ae7-139">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




