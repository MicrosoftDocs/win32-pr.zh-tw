---
description: SetOneShot 方法會指定範例抓取篩選器是否會在篩選器收到範例後停止。
ms.assetid: 7e3a3e8c-1834-425b-9657-279ab4451a2b
title: 'ISampleGrabber：： SetOneShot 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabber.SetOneShot
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 72a6e0e1798bcb8e19807619e982f487b0f04e6b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982595"
---
# <a name="isamplegrabbersetoneshot-method"></a><span data-ttu-id="7cf37-103">ISampleGrabber：： SetOneShot 方法</span><span class="sxs-lookup"><span data-stu-id="7cf37-103">ISampleGrabber::SetOneShot method</span></span>

> [!Note]  
> <span data-ttu-id="7cf37-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="7cf37-104">\[Deprecated.</span></span> <span data-ttu-id="7cf37-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="7cf37-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="7cf37-106">**SetOneShot** 方法會指定 [**範例**](sample-grabber-filter.md)抓取篩選器是否會在篩選器收到範例後停止。</span><span class="sxs-lookup"><span data-stu-id="7cf37-106">The **SetOneShot** method specifies whether the [**Sample Grabber**](sample-grabber-filter.md) filter halts after the filter receives a sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="7cf37-107">語法</span><span class="sxs-lookup"><span data-stu-id="7cf37-107">Syntax</span></span>


```C++
HRESULT SetOneShot(
   BOOL OneShot
);
```



## <a name="parameters"></a><span data-ttu-id="7cf37-108">參數</span><span class="sxs-lookup"><span data-stu-id="7cf37-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7cf37-109">*OneShot*</span><span class="sxs-lookup"><span data-stu-id="7cf37-109">*OneShot*</span></span> 
</dt> <dd>

<span data-ttu-id="7cf37-110">布林值，這個值會指定在接收到範例之後，範例抓取篩選器是否會中止。</span><span class="sxs-lookup"><span data-stu-id="7cf37-110">A Boolean value that specifies whether the Sample Grabber filter halts after receiving a sample.</span></span>



| <span data-ttu-id="7cf37-111">值</span><span class="sxs-lookup"><span data-stu-id="7cf37-111">Value</span></span>                                                                                                                                    | <span data-ttu-id="7cf37-112">意義</span><span class="sxs-lookup"><span data-stu-id="7cf37-112">Meaning</span></span>                                                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span id="TRUE"></span><span id="true"></span><dl> <span data-ttu-id="7cf37-113"><dt>TRUE \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="7cf37-113"><dt>\*\*\*\*TRUE\*\*\*\*</dt></span></span> </dl>    | <span data-ttu-id="7cf37-114">範例捕獲會在第一個範例之後停止。</span><span class="sxs-lookup"><span data-stu-id="7cf37-114">The Sample Grabber halts after the first sample.</span></span> <br/>                                                      |
| <span id="FALSE"></span><span id="false"></span><dl> <span data-ttu-id="7cf37-115"><dt>FALSE \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="7cf37-115"><dt>\*\*\*\*FALSE\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="7cf37-116">在第一個範例之後，範例抓取程式會繼續處理範例。</span><span class="sxs-lookup"><span data-stu-id="7cf37-116">After the first sample, the Sample Grabber continues to process samples.</span></span> <span data-ttu-id="7cf37-117">這是預設行為。</span><span class="sxs-lookup"><span data-stu-id="7cf37-117">This is the default behavior.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7cf37-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="7cf37-118">Return value</span></span>

<span data-ttu-id="7cf37-119">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="7cf37-119">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="7cf37-120">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="7cf37-120">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="7cf37-121">備註</span><span class="sxs-lookup"><span data-stu-id="7cf37-121">Remarks</span></span>

<span data-ttu-id="7cf37-122">使用這個方法可從資料流程取得單一範例，如下所示：</span><span class="sxs-lookup"><span data-stu-id="7cf37-122">Use this method to get a single sample from the stream, as follows:</span></span>

1.  <span data-ttu-id="7cf37-123">使用值 **TRUE** 來呼叫 **SetOneShot** 。</span><span class="sxs-lookup"><span data-stu-id="7cf37-123">Call **SetOneShot** with the value **TRUE**.</span></span>
2.  <span data-ttu-id="7cf37-124">（選擇性）使用 [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) 介面搜尋資料流程中的位置。</span><span class="sxs-lookup"><span data-stu-id="7cf37-124">Optionally, use the [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) interface to seek to a position in the stream.</span></span>
3.  <span data-ttu-id="7cf37-125">呼叫 [**IMediaControl：： run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) 以執行篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="7cf37-125">Call [**IMediaControl::Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) to run the filter graph.</span></span>
4.  <span data-ttu-id="7cf37-126">呼叫 [**IMediaEvent：： WaitForCompletion**](/windows/desktop/api/Control/nf-control-imediaevent-waitforcompletion) 以等候圖形停止。</span><span class="sxs-lookup"><span data-stu-id="7cf37-126">Call [**IMediaEvent::WaitForCompletion**](/windows/desktop/api/Control/nf-control-imediaevent-waitforcompletion) to wait for the graph to halt.</span></span> <span data-ttu-id="7cf37-127">或者，您也可以呼叫 [**IMediaEvent：： GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) 來取得圖形事件，直到您收到 [**EC \_ 完成**](ec-complete.md) 事件為止。</span><span class="sxs-lookup"><span data-stu-id="7cf37-127">Alternatively, call [**IMediaEvent::GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) to get graph events, until you receive the [**EC\_COMPLETE**](ec-complete.md) event.</span></span>

<span data-ttu-id="7cf37-128">在範例捕獲程式停止之後，篩選圖形仍處於執行中狀態。</span><span class="sxs-lookup"><span data-stu-id="7cf37-128">After the Sample Grabber halts, the filter graph is still in a running state.</span></span> <span data-ttu-id="7cf37-129">您可以搜尋或暫停圖形來取得另一個範例。</span><span class="sxs-lookup"><span data-stu-id="7cf37-129">You can seek or pause the graph to get another sample.</span></span>

> [!Note]  
> <span data-ttu-id="7cf37-130">舊版檔指出篩選圖形會在收到範例後停止。</span><span class="sxs-lookup"><span data-stu-id="7cf37-130">An earlier version of the documentation stated that the filter graph stops after the sample is received.</span></span> <span data-ttu-id="7cf37-131">這是不正確的。</span><span class="sxs-lookup"><span data-stu-id="7cf37-131">That is not accurate.</span></span> <span data-ttu-id="7cf37-132">資料流程結束，但圖形仍處於執行中狀態。</span><span class="sxs-lookup"><span data-stu-id="7cf37-132">The stream ends, but the graph remains in the running state.</span></span>

 

<span data-ttu-id="7cf37-133">此範例會藉由呼叫下游篩選器上的 [**IPin：： EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) ，並 \_ 從它的 [**IMemInputPin：： Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) 方法傳回 FALSE，來執行一次模式。</span><span class="sxs-lookup"><span data-stu-id="7cf37-133">The Sample Grabber implements one-shot mode by calling [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) on the downstream filter and returning S\_FALSE from the [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) method of it.</span></span>

> [!Note]  
> <span data-ttu-id="7cf37-134">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="7cf37-134">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="7cf37-135">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="7cf37-135">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="7cf37-136">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="7cf37-136">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="7cf37-137">規格需求</span><span class="sxs-lookup"><span data-stu-id="7cf37-137">Requirements</span></span>



| <span data-ttu-id="7cf37-138">需求</span><span class="sxs-lookup"><span data-stu-id="7cf37-138">Requirement</span></span> | <span data-ttu-id="7cf37-139">值</span><span class="sxs-lookup"><span data-stu-id="7cf37-139">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7cf37-140">標頭</span><span class="sxs-lookup"><span data-stu-id="7cf37-140">Header</span></span><br/>  | <dl> <span data-ttu-id="7cf37-141"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="7cf37-141"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="7cf37-142">程式庫</span><span class="sxs-lookup"><span data-stu-id="7cf37-142">Library</span></span><br/> | <dl> <span data-ttu-id="7cf37-143"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="7cf37-143"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7cf37-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7cf37-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7cf37-145">使用範例捕獲</span><span class="sxs-lookup"><span data-stu-id="7cf37-145">Using the Sample Grabber</span></span>](using-the-sample-grabber.md)
</dt> <dt>

[<span data-ttu-id="7cf37-146">**ISampleGrabber 介面**</span><span class="sxs-lookup"><span data-stu-id="7cf37-146">**ISampleGrabber Interface**</span></span>](isamplegrabber.md)
</dt> </dl>

 

 




