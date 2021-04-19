---
description: SetCallback 方法會指定要對傳入範例呼叫的回呼方法。
ms.assetid: b84d3f52-b986-492a-a8b9-1d98618dcdd3
title: 'ISampleGrabber：： SetCallback 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabber.SetCallback
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 46e0565c314bab86967ee0d5dabee6ba449a87dd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993524"
---
# <a name="isamplegrabbersetcallback-method"></a><span data-ttu-id="aff25-103">ISampleGrabber：： SetCallback 方法</span><span class="sxs-lookup"><span data-stu-id="aff25-103">ISampleGrabber::SetCallback method</span></span>

> [!Note]  
> <span data-ttu-id="aff25-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="aff25-104">\[Deprecated.</span></span> <span data-ttu-id="aff25-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="aff25-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="aff25-106">**SetCallback** 方法會指定要對傳入範例呼叫的回呼方法。</span><span class="sxs-lookup"><span data-stu-id="aff25-106">The **SetCallback** method specifies a callback method to call on incoming samples.</span></span>

## <a name="syntax"></a><span data-ttu-id="aff25-107">語法</span><span class="sxs-lookup"><span data-stu-id="aff25-107">Syntax</span></span>


```C++
HRESULT SetCallback(
   ISampleGrabberCB *pCallback,
   long             WhichMethodToCallback
);
```



## <a name="parameters"></a><span data-ttu-id="aff25-108">參數</span><span class="sxs-lookup"><span data-stu-id="aff25-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aff25-109">*pCallback*</span><span class="sxs-lookup"><span data-stu-id="aff25-109">*pCallback*</span></span> 
</dt> <dd>

<span data-ttu-id="aff25-110">包含回呼方法之 [**ISampleGrabberCB**](isamplegrabbercb.md) 介面的指標，或為 **Null** 以取消回呼。</span><span class="sxs-lookup"><span data-stu-id="aff25-110">Pointer to an [**ISampleGrabberCB**](isamplegrabbercb.md) interface containing the callback method, or **NULL** to cancel the callback.</span></span>

</dd> <dt>

<span data-ttu-id="aff25-111">*WhichMethodToCallback*</span><span class="sxs-lookup"><span data-stu-id="aff25-111">*WhichMethodToCallback*</span></span> 
</dt> <dd>

<span data-ttu-id="aff25-112">指定回呼方法的索引。</span><span class="sxs-lookup"><span data-stu-id="aff25-112">Index specifying the callback method.</span></span> <span data-ttu-id="aff25-113">必須是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="aff25-113">Must be one of the following values.</span></span>



| <span data-ttu-id="aff25-114">值</span><span class="sxs-lookup"><span data-stu-id="aff25-114">Value</span></span> | <span data-ttu-id="aff25-115">描述</span><span class="sxs-lookup"><span data-stu-id="aff25-115">Description</span></span>                                                                                                                                                                                     |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aff25-116">0</span><span class="sxs-lookup"><span data-stu-id="aff25-116">0</span></span>     | <span data-ttu-id="aff25-117">範例捕獲篩選準則會呼叫 [**ISampleGrabberCB：： SampleCB**](isamplegrabbercb-samplecb.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="aff25-117">The Sample Grabber filter calls the [**ISampleGrabberCB::SampleCB**](isamplegrabbercb-samplecb.md) method.</span></span> <span data-ttu-id="aff25-118">這個方法會接收 [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) 指標。</span><span class="sxs-lookup"><span data-stu-id="aff25-118">This method receives an [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) pointer.</span></span>               |
| <span data-ttu-id="aff25-119">1</span><span class="sxs-lookup"><span data-stu-id="aff25-119">1</span></span>     | <span data-ttu-id="aff25-120">範例捕獲篩選準則會呼叫 [**ISampleGrabberCB：： BufferCB**](isamplegrabbercb-buffercb.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="aff25-120">The Sample Grabber filter calls the [**ISampleGrabberCB::BufferCB**](isamplegrabbercb-buffercb.md) method.</span></span> <span data-ttu-id="aff25-121">這個方法會接收包含在媒體範例中的緩衝區指標。</span><span class="sxs-lookup"><span data-stu-id="aff25-121">This method receives a pointer to the buffer that is contained in the media sample.</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aff25-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="aff25-122">Return value</span></span>

<span data-ttu-id="aff25-123">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="aff25-123">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="aff25-124">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="aff25-124">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="aff25-125">備註</span><span class="sxs-lookup"><span data-stu-id="aff25-125">Remarks</span></span>

<span data-ttu-id="aff25-126">資料處理執行緒會封鎖，直到回呼方法傳回為止。</span><span class="sxs-lookup"><span data-stu-id="aff25-126">The data processing thread blocks until the callback method returns.</span></span> <span data-ttu-id="aff25-127">如果回呼不會快速傳回，它可能會干擾播放。</span><span class="sxs-lookup"><span data-stu-id="aff25-127">If the callback does not return quickly, it can interfere with playback.</span></span>

<span data-ttu-id="aff25-128">此篩選不會叫用預算範例的回呼函式，或針對 [**am \_ sample2.xml \_ 屬性**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties)結構的 **dwStreamId** 成員是串流媒體以外的任何範例 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="aff25-128">The filter does not invoke the callback function for preroll samples, or for samples in which the **dwStreamId** member of the [**AM\_SAMPLE2\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) structure is anything other than AM\_STREAM\_MEDIA.</span></span>

> [!Note]  
> <span data-ttu-id="aff25-129">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="aff25-129">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="aff25-130">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="aff25-130">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="aff25-131">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="aff25-131">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="aff25-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="aff25-132">Requirements</span></span>



| <span data-ttu-id="aff25-133">需求</span><span class="sxs-lookup"><span data-stu-id="aff25-133">Requirement</span></span> | <span data-ttu-id="aff25-134">值</span><span class="sxs-lookup"><span data-stu-id="aff25-134">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="aff25-135">標頭</span><span class="sxs-lookup"><span data-stu-id="aff25-135">Header</span></span><br/>  | <dl> <span data-ttu-id="aff25-136"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="aff25-136"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="aff25-137">程式庫</span><span class="sxs-lookup"><span data-stu-id="aff25-137">Library</span></span><br/> | <dl> <span data-ttu-id="aff25-138"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="aff25-138"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aff25-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="aff25-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aff25-140">使用範例捕獲</span><span class="sxs-lookup"><span data-stu-id="aff25-140">Using the Sample Grabber</span></span>](using-the-sample-grabber.md)
</dt> <dt>

[<span data-ttu-id="aff25-141">**ISampleGrabber 介面**</span><span class="sxs-lookup"><span data-stu-id="aff25-141">**ISampleGrabber Interface**</span></span>](isamplegrabber.md)
</dt> </dl>

 

 




