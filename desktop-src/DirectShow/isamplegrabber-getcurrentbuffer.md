---
description: GetCurrentBuffer 方法會抓取與最新樣本相關聯的緩衝區複本。
ms.assetid: 08550c82-4711-4725-9cd0-19b43cf4c92e
title: 'ISampleGrabber：： GetCurrentBuffer 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabber.GetCurrentBuffer
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: d4df4c825761b42533590f10432bf62e5e4e0298
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996214"
---
# <a name="isamplegrabbergetcurrentbuffer-method"></a><span data-ttu-id="05bbf-103">ISampleGrabber：： GetCurrentBuffer 方法</span><span class="sxs-lookup"><span data-stu-id="05bbf-103">ISampleGrabber::GetCurrentBuffer method</span></span>

> [!Note]  
> <span data-ttu-id="05bbf-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="05bbf-104">\[Deprecated.</span></span> <span data-ttu-id="05bbf-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="05bbf-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="05bbf-106">**GetCurrentBuffer** 方法會抓取與最新樣本相關聯的緩衝區複本。</span><span class="sxs-lookup"><span data-stu-id="05bbf-106">The **GetCurrentBuffer** method retrieves a copy of the buffer associated with the most recent sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="05bbf-107">語法</span><span class="sxs-lookup"><span data-stu-id="05bbf-107">Syntax</span></span>


```C++
HRESULT GetCurrentBuffer(
  [in, out] long *pBufferSize,
  [out]     long *pBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="05bbf-108">參數</span><span class="sxs-lookup"><span data-stu-id="05bbf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05bbf-109">*pBufferSize* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="05bbf-109">*pBufferSize* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="05bbf-110">緩衝區大小的指標。</span><span class="sxs-lookup"><span data-stu-id="05bbf-110">Pointer to the size of the buffer.</span></span> <span data-ttu-id="05bbf-111">如果 *pBuffer* 為 **Null**，則此參數會收到所需的緩衝區大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="05bbf-111">If *pBuffer* is **NULL**, this parameter receives the required buffer size, in bytes.</span></span> <span data-ttu-id="05bbf-112">如果 *pBuffer* 不是 **Null**，請將此參數設定為等於緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="05bbf-112">If *pBuffer* is not **NULL**, set this parameter equal to the size of the buffer, in bytes.</span></span> <span data-ttu-id="05bbf-113">在輸出上，參數會接收復制到緩衝區的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="05bbf-113">On output, the parameter receives the number of bytes that were copied into the buffer.</span></span> <span data-ttu-id="05bbf-114">這個值可能小於緩衝區的大小。</span><span class="sxs-lookup"><span data-stu-id="05bbf-114">This value might be smaller than the size of the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="05bbf-115">*pBuffer* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="05bbf-115">*pBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="05bbf-116">*PBufferSize* 大小位元組陣列的指標，或 **為 Null**。</span><span class="sxs-lookup"><span data-stu-id="05bbf-116">Pointer to an array of bytes of size *pBufferSize*, or **NULL**.</span></span> <span data-ttu-id="05bbf-117">如果這個參數不是 **Null**，則會將目前的緩衝區複製到陣列中。</span><span class="sxs-lookup"><span data-stu-id="05bbf-117">If this parameter is not **NULL**, the current buffer is copied into the array.</span></span> <span data-ttu-id="05bbf-118">如果此參數為 **Null**，則 *pBufferSize* 參數會收到所需的緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="05bbf-118">If this parameter is **NULL**, the *pBufferSize* parameter receives the required buffer size.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="05bbf-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="05bbf-119">Return value</span></span>

<span data-ttu-id="05bbf-120">傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="05bbf-120">Returns one of the following values.</span></span>



| <span data-ttu-id="05bbf-121">傳回碼</span><span class="sxs-lookup"><span data-stu-id="05bbf-121">Return code</span></span>                                                                                           | <span data-ttu-id="05bbf-122">Description</span><span class="sxs-lookup"><span data-stu-id="05bbf-122">Description</span></span>                                                                                                                  |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="05bbf-123"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="05bbf-123"><dt>**E\_INVALIDARG**</dt></span></span> </dl>          | <span data-ttu-id="05bbf-124">未緩衝處理範例。</span><span class="sxs-lookup"><span data-stu-id="05bbf-124">Samples are not being buffered.</span></span> <span data-ttu-id="05bbf-125">呼叫 [**ISampleGrabber：： SetBufferSamples**](isamplegrabber-setbuffersamples.md)。</span><span class="sxs-lookup"><span data-stu-id="05bbf-125">Call [**ISampleGrabber::SetBufferSamples**](isamplegrabber-setbuffersamples.md).</span></span><br/> |
| <dl> <span data-ttu-id="05bbf-126"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="05bbf-126"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>         | <span data-ttu-id="05bbf-127">指定的緩衝區不夠大。</span><span class="sxs-lookup"><span data-stu-id="05bbf-127">The specified buffer is not large enough.</span></span><br/>                                                                         |
| <dl> <span data-ttu-id="05bbf-128"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="05bbf-128"><dt>**E\_POINTER**</dt></span></span> </dl>             | <span data-ttu-id="05bbf-129">**Null** 指標引數。</span><span class="sxs-lookup"><span data-stu-id="05bbf-129">**NULL** pointer argument.</span></span><br/>                                                                                        |
| <dl> <span data-ttu-id="05bbf-130"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="05bbf-130"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="05bbf-131">成功。</span><span class="sxs-lookup"><span data-stu-id="05bbf-131">Success.</span></span><br/>                                                                                                          |
| <dl> <span data-ttu-id="05bbf-132"><dt>**VFW \_ E \_ 未 \_ 連線**</dt></span><span class="sxs-lookup"><span data-stu-id="05bbf-132"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="05bbf-133">篩選未連接。</span><span class="sxs-lookup"><span data-stu-id="05bbf-133">The filter is not connected.</span></span><br/>                                                                                      |
| <dl> <span data-ttu-id="05bbf-134"><dt>**VFW \_ E \_ 錯誤的 \_ 狀態**</dt></span><span class="sxs-lookup"><span data-stu-id="05bbf-134"><dt>**VFW\_E\_WRONG\_STATE**</dt></span></span> </dl>   | <span data-ttu-id="05bbf-135">篩選尚未收到任何範例。</span><span class="sxs-lookup"><span data-stu-id="05bbf-135">The filter has not received any samples yet.</span></span> <span data-ttu-id="05bbf-136">若要傳遞範例，請執行或暫停圖形。</span><span class="sxs-lookup"><span data-stu-id="05bbf-136">To deliver a sample, run or pause the graph.</span></span><br/>                         |



 

## <a name="remarks"></a><span data-ttu-id="05bbf-137">備註</span><span class="sxs-lookup"><span data-stu-id="05bbf-137">Remarks</span></span>

<span data-ttu-id="05bbf-138">若要啟用緩衝處理，請呼叫 [**ISampleGrabber：： SetBufferSamples**](isamplegrabber-setbuffersamples.md) ，並將值 **設為 TRUE**。</span><span class="sxs-lookup"><span data-stu-id="05bbf-138">To activate buffering, call [**ISampleGrabber::SetBufferSamples**](isamplegrabber-setbuffersamples.md) with a value of **TRUE**.</span></span>

<span data-ttu-id="05bbf-139">呼叫這個方法兩次。</span><span class="sxs-lookup"><span data-stu-id="05bbf-139">Call this method twice.</span></span> <span data-ttu-id="05bbf-140">在第一次呼叫時，將 *pBuffer* 設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="05bbf-140">On the first call, set *pBuffer* to **NULL**.</span></span> <span data-ttu-id="05bbf-141">緩衝區的大小會在 *pBufferSize* 中傳回。</span><span class="sxs-lookup"><span data-stu-id="05bbf-141">The size of the buffer is returned in *pBufferSize*.</span></span> <span data-ttu-id="05bbf-142">然後配置陣列，並再次呼叫方法。</span><span class="sxs-lookup"><span data-stu-id="05bbf-142">Then allocate an array and call the method again.</span></span> <span data-ttu-id="05bbf-143">在第二個呼叫中，傳遞 *pBufferSize* 中的陣列大小，然後在 *pBuffer* 中傳遞陣列的位址。</span><span class="sxs-lookup"><span data-stu-id="05bbf-143">On the second call, pass the size of the array in *pBufferSize*, and pass the address of the array in *pBuffer*.</span></span> <span data-ttu-id="05bbf-144">如果陣列不夠大，則方法會傳回 E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="05bbf-144">If the array is not large enough, the method returns E\_OUTOFMEMORY.</span></span>

<span data-ttu-id="05bbf-145">*PBuffer* 參數的類型為 **long** 指標，但緩衝區的內容會根據資料的格式而定。</span><span class="sxs-lookup"><span data-stu-id="05bbf-145">The *pBuffer* parameter is typed as a **long** pointer, but the contents of the buffer depend on the format of the data.</span></span> <span data-ttu-id="05bbf-146">呼叫 [**ISampleGrabber：： GetConnectedMediaType**](isamplegrabber-getconnectedmediatype.md) 來取得格式的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="05bbf-146">Call [**ISampleGrabber::GetConnectedMediaType**](isamplegrabber-getconnectedmediatype.md) to get the media type of the format.</span></span>

<span data-ttu-id="05bbf-147">當篩選圖形正在執行時，請勿呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="05bbf-147">Do not call this method while the filter graph is running.</span></span> <span data-ttu-id="05bbf-148">當篩選圖形正在執行時，範例捕獲篩選器會在每次收到新的範例時覆寫緩衝區的內容。</span><span class="sxs-lookup"><span data-stu-id="05bbf-148">While the filter graph is running, the Sample Grabber filter overwrites the contents of the buffer whenever it receives a new sample.</span></span> <span data-ttu-id="05bbf-149">使用這個方法的最佳方式是使用「一次模式」，這會在收到第一個樣本之後停止圖形。</span><span class="sxs-lookup"><span data-stu-id="05bbf-149">The best way to use this method is to use "one-shot mode," which stops the graph after receiving the first sample.</span></span> <span data-ttu-id="05bbf-150">若要設定一次模式，請呼叫 [**ISampleGrabber：： SetOneShot**](isamplegrabber-setoneshot.md)。</span><span class="sxs-lookup"><span data-stu-id="05bbf-150">To set one-shot mode, call [**ISampleGrabber::SetOneShot**](isamplegrabber-setoneshot.md).</span></span>

<span data-ttu-id="05bbf-151">篩選不會緩衝預先執行的範例，或者 [**am \_ sample2.xml \_ 屬性**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties)結構的 **dwStreamId** 成員是串流媒體以外的任何其他範例 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="05bbf-151">The filter does not buffer preroll samples, or samples in which the **dwStreamId** member of the [**AM\_SAMPLE2\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) structure is anything other than AM\_STREAM\_MEDIA.</span></span>

> [!Note]  
> <span data-ttu-id="05bbf-152">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="05bbf-152">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="05bbf-153">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="05bbf-153">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="05bbf-154">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="05bbf-154">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="05bbf-155">規格需求</span><span class="sxs-lookup"><span data-stu-id="05bbf-155">Requirements</span></span>



| <span data-ttu-id="05bbf-156">需求</span><span class="sxs-lookup"><span data-stu-id="05bbf-156">Requirement</span></span> | <span data-ttu-id="05bbf-157">值</span><span class="sxs-lookup"><span data-stu-id="05bbf-157">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="05bbf-158">標頭</span><span class="sxs-lookup"><span data-stu-id="05bbf-158">Header</span></span><br/>  | <dl> <span data-ttu-id="05bbf-159"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="05bbf-159"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="05bbf-160">程式庫</span><span class="sxs-lookup"><span data-stu-id="05bbf-160">Library</span></span><br/> | <dl> <span data-ttu-id="05bbf-161"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="05bbf-161"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05bbf-162">另請參閱</span><span class="sxs-lookup"><span data-stu-id="05bbf-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05bbf-163">使用範例捕獲</span><span class="sxs-lookup"><span data-stu-id="05bbf-163">Using the Sample Grabber</span></span>](using-the-sample-grabber.md)
</dt> <dt>

[<span data-ttu-id="05bbf-164">**ISampleGrabber 介面**</span><span class="sxs-lookup"><span data-stu-id="05bbf-164">**ISampleGrabber Interface**</span></span>](isamplegrabber.md)
</dt> </dl>

 

 




