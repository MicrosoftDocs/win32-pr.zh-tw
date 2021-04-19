---
description: GetBitmapBits 方法會在指定的媒體時間取出影片畫面。 傳回的框架一律採用24位 RGB 格式。
ms.assetid: b51df9d1-9c54-41bd-b0f8-ec290525deca
title: 'IMediaDet：： GetBitmapBits 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.GetBitmapBits
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 95aea5281f77b32868e0f0856bc63063e4f08639
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000436"
---
# <a name="imediadetgetbitmapbits-method"></a><span data-ttu-id="798e4-104">IMediaDet：： GetBitmapBits 方法</span><span class="sxs-lookup"><span data-stu-id="798e4-104">IMediaDet::GetBitmapBits method</span></span>

> [!Note]  
> <span data-ttu-id="798e4-105">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="798e4-105">\[Deprecated.</span></span> <span data-ttu-id="798e4-106">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="798e4-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="798e4-107">`GetBitmapBits`方法會在指定的媒體時間取出影片畫面。</span><span class="sxs-lookup"><span data-stu-id="798e4-107">The `GetBitmapBits` method retrieves a video frame at the specified media time.</span></span> <span data-ttu-id="798e4-108">傳回的框架一律採用24位 RGB 格式。</span><span class="sxs-lookup"><span data-stu-id="798e4-108">The returned frame is always in 24-bit RGB format.</span></span>

## <a name="syntax"></a><span data-ttu-id="798e4-109">語法</span><span class="sxs-lookup"><span data-stu-id="798e4-109">Syntax</span></span>


```C++
HRESULT GetBitmapBits(
   double StreamTime,
   long   *pBufferSize,
   char   *pBuffer,
   long   Width,
   long   Height
);
```



## <a name="parameters"></a><span data-ttu-id="798e4-110">參數</span><span class="sxs-lookup"><span data-stu-id="798e4-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="798e4-111">*StreamTime*</span><span class="sxs-lookup"><span data-stu-id="798e4-111">*StreamTime*</span></span> 
</dt> <dd>

<span data-ttu-id="798e4-112">取出影片畫面的時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="798e4-112">Time at which to retrieve the video frame, in seconds.</span></span>

</dd> <dt>

<span data-ttu-id="798e4-113">*pBufferSize*</span><span class="sxs-lookup"><span data-stu-id="798e4-113">*pBufferSize*</span></span> 
</dt> <dd>

<span data-ttu-id="798e4-114">接收所需的緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="798e4-114">Receives the required buffer size.</span></span> <span data-ttu-id="798e4-115">如果 *pBuffer* 為 **Null**，則變數會收到取出框架所需的緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="798e4-115">If *pBuffer* is **NULL**, the variable receives the size of the buffer needed to retrieve the frame.</span></span> <span data-ttu-id="798e4-116">如果 *pBuffer* 不是 **Null**，則會忽略此參數。</span><span class="sxs-lookup"><span data-stu-id="798e4-116">If *pBuffer* is not **NULL**, this parameter is ignored.</span></span>

</dd> <dt>

<span data-ttu-id="798e4-117">*pBuffer*</span><span class="sxs-lookup"><span data-stu-id="798e4-117">*pBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="798e4-118">緩衝區的指標，此緩衝區會接收 [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) 結構，後面接著 DIB 位。</span><span class="sxs-lookup"><span data-stu-id="798e4-118">Pointer to a buffer that receives a [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure followed by the DIB bits.</span></span>

</dd> <dt>

<span data-ttu-id="798e4-119">*寬度*</span><span class="sxs-lookup"><span data-stu-id="798e4-119">*Width*</span></span> 
</dt> <dd>

<span data-ttu-id="798e4-120">影片影像的寬度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="798e4-120">Width of the video image, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="798e4-121">*高度*</span><span class="sxs-lookup"><span data-stu-id="798e4-121">*Height*</span></span> 
</dt> <dd>

<span data-ttu-id="798e4-122">影片影像的高度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="798e4-122">Height of the video image, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="798e4-123">傳回值</span><span class="sxs-lookup"><span data-stu-id="798e4-123">Return value</span></span>

<span data-ttu-id="798e4-124">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="798e4-124">Returns an **HRESULT** value.</span></span> <span data-ttu-id="798e4-125">可能的值如下：</span><span class="sxs-lookup"><span data-stu-id="798e4-125">Possible values include the following:</span></span>



| <span data-ttu-id="798e4-126">傳回碼</span><span class="sxs-lookup"><span data-stu-id="798e4-126">Return code</span></span>                                                                                             | <span data-ttu-id="798e4-127">Description</span><span class="sxs-lookup"><span data-stu-id="798e4-127">Description</span></span>                                                                                       |
|---------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="798e4-128"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="798e4-128"><dt>**S\_OK**</dt></span></span> </dl>                    | <span data-ttu-id="798e4-129">成功。</span><span class="sxs-lookup"><span data-stu-id="798e4-129">Success.</span></span><br/>                                                                               |
| <dl> <span data-ttu-id="798e4-130"><dt>**E \_ NOINTERFACE**</dt></span><span class="sxs-lookup"><span data-stu-id="798e4-130"><dt>**E\_NOINTERFACE**</dt></span></span> </dl>           | <span data-ttu-id="798e4-131">無法將 [**範例捕獲**](sample-grabber-filter.md) 篩選新增至圖形。</span><span class="sxs-lookup"><span data-stu-id="798e4-131">Could not add the [**Sample Grabber**](sample-grabber-filter.md) filter to the graph.</span></span><br/> |
| <dl> <span data-ttu-id="798e4-132"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="798e4-132"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>           | <span data-ttu-id="798e4-133">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="798e4-133">Insufficient memory.</span></span><br/>                                                                   |
| <dl> <span data-ttu-id="798e4-134"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="798e4-134"><dt>**E\_POINTER**</dt></span></span> </dl>               | <span data-ttu-id="798e4-135">**Null** 指標錯誤。</span><span class="sxs-lookup"><span data-stu-id="798e4-135">**NULL** pointer error.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="798e4-136"><dt>**E 未 \_ 預期**</dt></span><span class="sxs-lookup"><span data-stu-id="798e4-136"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>            | <span data-ttu-id="798e4-137">非預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="798e4-137">Unexpected error.</span></span><br/>                                                                      |
| <dl> <span data-ttu-id="798e4-138"><dt>**VFW \_ E \_ INVALIDMEDIATYPE**</dt></span><span class="sxs-lookup"><span data-stu-id="798e4-138"><dt>**VFW\_E\_INVALIDMEDIATYPE**</dt></span></span> </dl> | <span data-ttu-id="798e4-139">媒體類型無效。</span><span class="sxs-lookup"><span data-stu-id="798e4-139">Invalid media type.</span></span><br/>                                                                    |



 

## <a name="remarks"></a><span data-ttu-id="798e4-140">備註</span><span class="sxs-lookup"><span data-stu-id="798e4-140">Remarks</span></span>

<span data-ttu-id="798e4-141">在呼叫這個方法之前，請先呼叫 [**IMediaDet：:p \_**](imediadet-put-filename.md)的檔案名稱和串流，方法是呼叫： [**:p 的 IMediaDet： \_**](imediadet-put-currentstream.md)</span><span class="sxs-lookup"><span data-stu-id="798e4-141">Before calling this method, set the file name and stream by calling [**IMediaDet::put\_Filename**](imediadet-put-filename.md) and [**IMediaDet::put\_CurrentStream**](imediadet-put-currentstream.md).</span></span>

<span data-ttu-id="798e4-142">若要判斷所需的緩衝區大小，請使用等於 **Null** 的 *pBuffer* 呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="798e4-142">To determine the size of the buffer that is required, call this method with *pBuffer* equal to **NULL**.</span></span> <span data-ttu-id="798e4-143">大小會在 *pBufferSize* 所指向的變數中傳回。</span><span class="sxs-lookup"><span data-stu-id="798e4-143">The size is returned in the variable pointed to by *pBufferSize*.</span></span> <span data-ttu-id="798e4-144">然後建立緩衝區，並再次呼叫方法，其 *pBuffer* 等於緩衝區的位址。</span><span class="sxs-lookup"><span data-stu-id="798e4-144">Then create the buffer and call the method again, with *pBuffer* equal to the address of the buffer.</span></span> <span data-ttu-id="798e4-145">當方法傳回時，緩衝區會包含 **BITMAPINFOHEADER** 結構，後面接著點陣圖。</span><span class="sxs-lookup"><span data-stu-id="798e4-145">When the method returns, the buffer contains a **BITMAPINFOHEADER** structure followed by the bitmap.</span></span> <span data-ttu-id="798e4-146">點陣圖會調整為 [ *寬度* ] 和 [ *高度* ] 參數中所指定的維度。</span><span class="sxs-lookup"><span data-stu-id="798e4-146">The bitmap is scaled to the dimensions specified in the *Width* and *Height* parameters.</span></span>

<span data-ttu-id="798e4-147">這個方法會將媒體偵測器放入點陣圖抓取模式。</span><span class="sxs-lookup"><span data-stu-id="798e4-147">This method puts the media detector into bitmap grab mode.</span></span> <span data-ttu-id="798e4-148">一旦呼叫這個方法，除非您建立新的媒體偵測器實例，否則 **IMediaDet** 中的各種資料流程資訊方法將無法運作。</span><span class="sxs-lookup"><span data-stu-id="798e4-148">Once this method has been called, the various stream information methods in **IMediaDet** do not work, unless you create a new instance of the media detector.</span></span>

> [!Note]  
> <span data-ttu-id="798e4-149">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="798e4-149">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="798e4-150">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="798e4-150">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="798e4-151">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="798e4-151">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="examples"></a><span data-ttu-id="798e4-152">範例</span><span class="sxs-lookup"><span data-stu-id="798e4-152">Examples</span></span>

<span data-ttu-id="798e4-153">下列程式碼會使用 `GetBitmapBits` 方法來建立與裝置無關的點陣圖。</span><span class="sxs-lookup"><span data-stu-id="798e4-153">The following code uses the `GetBitmapBits` method to create a device-independent bitmap.</span></span>


```C++
long size;
hr = pDet->GetBitmapBits(0, &size, 0, width, height);
if (SUCCEEDED(hr)) 
{
    char *pBuffer = new char[size];
    if (!pBuffer)
        return E_OUTOFMEMORY;
    try {
        hr = pDet->GetBitmapBits(0, 0, pBuffer, width, height);
    }
    catch (...) {
        delete [] pBuffer;
        throw;
    }
    if (SUCCEEDED(hr))
    {
        BITMAPINFOHEADER *bmih = (BITMAPINFOHEADER*)pBuffer;
        HDC hdcDest = GetDC(0);
        
        // Find the address of the start of the image data.
        void *pData = pBuffer + sizeof(BITMAPINFOHEADER);
        
        // Note: In general a BITMAPINFOHEADER can include extra color
        // information at the end, so calculating the offset to the image
        // data is not generally correct. However, the IMediaDet interface
        // always returns an RGB-24 image with no extra color information.
        
        BITMAPINFO bmi;
        ZeroMemory(&bmi, sizeof(BITMAPINFO));
        CopyMemory(&(bmi.bmiHeader), bmih, sizeof(BITMAPINFOHEADER));
        HBITMAP hBitmap = CreateDIBitmap(hdcDest, bmih, CBM_INIT, 
            pData, &bmi, DIB_RGB_COLORS);
    }
    delete[] pBuffer;
}
```



## <a name="requirements"></a><span data-ttu-id="798e4-154">規格需求</span><span class="sxs-lookup"><span data-stu-id="798e4-154">Requirements</span></span>



| <span data-ttu-id="798e4-155">需求</span><span class="sxs-lookup"><span data-stu-id="798e4-155">Requirement</span></span> | <span data-ttu-id="798e4-156">值</span><span class="sxs-lookup"><span data-stu-id="798e4-156">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="798e4-157">標頭</span><span class="sxs-lookup"><span data-stu-id="798e4-157">Header</span></span><br/>  | <dl> <span data-ttu-id="798e4-158"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="798e4-158"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="798e4-159">程式庫</span><span class="sxs-lookup"><span data-stu-id="798e4-159">Library</span></span><br/> | <dl> <span data-ttu-id="798e4-160"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="798e4-160"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="798e4-161">另請參閱</span><span class="sxs-lookup"><span data-stu-id="798e4-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="798e4-162">**IMediaDet 介面**</span><span class="sxs-lookup"><span data-stu-id="798e4-162">**IMediaDet Interface**</span></span>](imediadet.md)
</dt> <dt>

[<span data-ttu-id="798e4-163">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="798e4-163">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




