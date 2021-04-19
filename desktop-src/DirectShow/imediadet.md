---
description: IMediaDet 介面會抓取媒體檔案的相關資訊，例如串流的數目，以及每個資料流程的媒體類型、持續時間和畫面播放速率。
ms.assetid: 596fc84e-a88a-4e1b-aa48-b6dc9031db31
title: 'IMediaDet 介面 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ca5c87a1424872491aba5dcf4e01011872e9ff36
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990520"
---
# <a name="imediadet-interface"></a><span data-ttu-id="9be1f-103">IMediaDet 介面</span><span class="sxs-lookup"><span data-stu-id="9be1f-103">IMediaDet interface</span></span>

> [!Note]  
> <span data-ttu-id="9be1f-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="9be1f-104">\[Deprecated.</span></span> <span data-ttu-id="9be1f-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="9be1f-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="9be1f-106">介面會抓取媒體檔案的 `IMediaDet` 相關資訊，例如串流的數目，以及每個資料流程的媒體類型、持續時間和畫面播放速率。</span><span class="sxs-lookup"><span data-stu-id="9be1f-106">The `IMediaDet` interface retrieves information about a media file, such as the number of streams, and the media type, duration, and frame rate of each stream.</span></span> <span data-ttu-id="9be1f-107">它也包含從影片串流中取出個別畫面格的方法。</span><span class="sxs-lookup"><span data-stu-id="9be1f-107">It also contains methods for retrieving individual frames from a video stream.</span></span> <span data-ttu-id="9be1f-108">媒體偵測器 [ (MediaDet) ](media-detector--mediadet.md) 物件會公開這個介面。</span><span class="sxs-lookup"><span data-stu-id="9be1f-108">The [Media Detector (MediaDet)](media-detector--mediadet.md) object exposes this interface.</span></span>

<span data-ttu-id="9be1f-109">若要使用此介面取得檔案的相關資訊，請執行下列步驟：</span><span class="sxs-lookup"><span data-stu-id="9be1f-109">To obtain information about a file using this interface, perform the following steps:</span></span>

1.  <span data-ttu-id="9be1f-110">藉由呼叫 **CoCreateInstance** 來建立 MediaDet 物件的實例。</span><span class="sxs-lookup"><span data-stu-id="9be1f-110">Create an instance of the MediaDet object by calling **CoCreateInstance**.</span></span> <span data-ttu-id="9be1f-111">類別識別碼是 CLSID \_ MediaDet。</span><span class="sxs-lookup"><span data-stu-id="9be1f-111">The class ID is CLSID\_MediaDet.</span></span>
2.  <span data-ttu-id="9be1f-112">呼叫 [**IMediaDet：:p 的 \_**](imediadet-put-filename.md) 檔案名稱，以指定原始程式檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="9be1f-112">Call [**IMediaDet::put\_Filename**](imediadet-put-filename.md) to specify the name of the source file.</span></span>
3.  <span data-ttu-id="9be1f-113">呼叫 [**IMediaDet：： get \_ OutputStreams**](imediadet-get-outputstreams.md) 取得來源中的輸出資料流程數目。</span><span class="sxs-lookup"><span data-stu-id="9be1f-113">Call [**IMediaDet::get\_OutputStreams**](imediadet-get-outputstreams.md) to obtain the number of output streams in the source.</span></span>
4.  <span data-ttu-id="9be1f-114">呼叫 [**IMediaDet：:p 工作 \_ CurrentStream**](imediadet-put-currentstream.md) ]，以指定特定的資料流程。</span><span class="sxs-lookup"><span data-stu-id="9be1f-114">Call [**IMediaDet::put\_CurrentStream**](imediadet-put-currentstream.md) to specify a particular stream.</span></span>
5.  <span data-ttu-id="9be1f-115">呼叫下列任一方法：</span><span class="sxs-lookup"><span data-stu-id="9be1f-115">Call any of the following methods:</span></span>
    -   [<span data-ttu-id="9be1f-116">**IMediaDet：：取得 \_ 幀率**</span><span class="sxs-lookup"><span data-stu-id="9be1f-116">**IMediaDet::get\_FrameRate**</span></span>](imediadet-get-framerate.md)
    -   [<span data-ttu-id="9be1f-117">**IMediaDet：： get \_ StreamLength**</span><span class="sxs-lookup"><span data-stu-id="9be1f-117">**IMediaDet::get\_StreamLength**</span></span>](imediadet-get-streamlength.md)
    -   [<span data-ttu-id="9be1f-118">**IMediaDet：： get \_ StreamMediaType**</span><span class="sxs-lookup"><span data-stu-id="9be1f-118">**IMediaDet::get\_StreamMediaType**</span></span>](imediadet-get-streammediatype.md)
    -   [<span data-ttu-id="9be1f-119">**IMediaDet：： get \_ StreamType**</span><span class="sxs-lookup"><span data-stu-id="9be1f-119">**IMediaDet::get\_StreamType**</span></span>](imediadet-get-streamtype.md)

<span data-ttu-id="9be1f-120">若要取出影片框架，請呼叫 [**IMediaDet：： GetBitmapBits**](imediadet-getbitmapbits.md) 或 [**IMediaDet：： WriteBitmapBits**](imediadet-writebitmapbits.md)。</span><span class="sxs-lookup"><span data-stu-id="9be1f-120">To retrieve a video frame, call [**IMediaDet::GetBitmapBits**](imediadet-getbitmapbits.md) or [**IMediaDet::WriteBitmapBits**](imediadet-writebitmapbits.md).</span></span> <span data-ttu-id="9be1f-121">傳回的框架一律採用24位 RGB 格式。</span><span class="sxs-lookup"><span data-stu-id="9be1f-121">The returned frame is always in 24-bit RGB format.</span></span>

> [!Note]  
> <span data-ttu-id="9be1f-122">請勿使用與多個檔案相同的 MediaDet 物件。</span><span class="sxs-lookup"><span data-stu-id="9be1f-122">Do not use the same MediaDet object with multiple files.</span></span> <span data-ttu-id="9be1f-123">若要從多個檔案取得資訊或影片框架，請使用個別的 MediaDet 實例。</span><span class="sxs-lookup"><span data-stu-id="9be1f-123">To get information or video frames from more than one file, use separate MediaDet instances.</span></span>

 

<span data-ttu-id="9be1f-124">**IMediaDet** 介面不支援 [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2)格式，因此您無法使用此介面來取得交錯式欄位或交錯的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="9be1f-124">The **IMediaDet** interface does not support [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) formats, so you cannot use this interface to get interlaced fields or information about interlacing.</span></span> <span data-ttu-id="9be1f-125">此外，如果上游解碼器只支援 **VIDEOINFOHEADER2**，您就無法使用 `IMediaDet` 。</span><span class="sxs-lookup"><span data-stu-id="9be1f-125">Also, if the upstream decoder supports only **VIDEOINFOHEADER2**, you cannot use `IMediaDet`.</span></span> <span data-ttu-id="9be1f-126">例如，使用 MPEG-2 解碼器時可能會發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="9be1f-126">This might be the case with an MPEG-2 decoder, for example.</span></span> <span data-ttu-id="9be1f-127">此外， `IMediaDet` 介面會忽略檔案中非影片或音訊的任何資料流程。</span><span class="sxs-lookup"><span data-stu-id="9be1f-127">Also, the `IMediaDet` interface ignores any streams in the file that are not video or audio.</span></span> <span data-ttu-id="9be1f-128">例如，如果檔案包含音訊串流、資料流程和影片串流， **get \_ OutputStreams** 方法將只會報告兩個串流 (音訊和影片) 。</span><span class="sxs-lookup"><span data-stu-id="9be1f-128">For example, if the file contains an audio stream, a data stream, and a video stream, the **get\_OutputStreams** method will report only two streams (the audio and video).</span></span>

## <a name="members"></a><span data-ttu-id="9be1f-129">成員</span><span class="sxs-lookup"><span data-stu-id="9be1f-129">Members</span></span>

<span data-ttu-id="9be1f-130">**IMediaDet** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="9be1f-130">The **IMediaDet** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="9be1f-131">**IMediaDet** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="9be1f-131">**IMediaDet** also has these types of members:</span></span>

-   [<span data-ttu-id="9be1f-132">方法</span><span class="sxs-lookup"><span data-stu-id="9be1f-132">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="9be1f-133">方法</span><span class="sxs-lookup"><span data-stu-id="9be1f-133">Methods</span></span>

<span data-ttu-id="9be1f-134">**IMediaDet** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="9be1f-134">The **IMediaDet** interface has these methods.</span></span>



| <span data-ttu-id="9be1f-135">方法</span><span class="sxs-lookup"><span data-stu-id="9be1f-135">Method</span></span>                                                        | <span data-ttu-id="9be1f-136">描述</span><span class="sxs-lookup"><span data-stu-id="9be1f-136">Description</span></span>                                                                                                |
|:--------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9be1f-137">**EnterBitmapGrabMode**</span><span class="sxs-lookup"><span data-stu-id="9be1f-137">**EnterBitmapGrabMode**</span></span>](imediadet-enterbitmapgrabmode.md)  | <span data-ttu-id="9be1f-138">將媒體偵測器切換為點陣圖抓取模式，並搜尋篩選圖形到指定的時間。</span><span class="sxs-lookup"><span data-stu-id="9be1f-138">Switches the media detector to bitmap grab mode and seeks the filter graph to a specified time.</span></span><br/> |
| [<span data-ttu-id="9be1f-139">**取得 \_ CurrentStream**</span><span class="sxs-lookup"><span data-stu-id="9be1f-139">**get\_CurrentStream**</span></span>](imediadet-get-currentstream.md)     | <span data-ttu-id="9be1f-140">抓取媒體偵測器目前使用的資料流程號碼。</span><span class="sxs-lookup"><span data-stu-id="9be1f-140">Retrieves the stream number currently used by the media detector.</span></span><br/>                               |
| [<span data-ttu-id="9be1f-141">**取得 \_ 檔案名**</span><span class="sxs-lookup"><span data-stu-id="9be1f-141">**get\_Filename**</span></span>](imediadet-get-filename.md)               | <span data-ttu-id="9be1f-142">抓取媒體偵測器目前所使用的原始程式檔名稱。</span><span class="sxs-lookup"><span data-stu-id="9be1f-142">Retrieves the name of the source file currently used by the media detector.</span></span><br/>                     |
| [<span data-ttu-id="9be1f-143">**取得 \_ 篩選**</span><span class="sxs-lookup"><span data-stu-id="9be1f-143">**get\_Filter**</span></span>](imediadet-get-filter.md)                   | <span data-ttu-id="9be1f-144">抓取媒體偵測器目前使用的來源篩選指標。</span><span class="sxs-lookup"><span data-stu-id="9be1f-144">Retrieves a pointer to the source filter currently used by the media detector.</span></span><br/>                  |
| [<span data-ttu-id="9be1f-145">**取得 \_ 畫面播放速率**</span><span class="sxs-lookup"><span data-stu-id="9be1f-145">**get\_FrameRate**</span></span>](imediadet-get-framerate.md)             | <span data-ttu-id="9be1f-146">抓取目前資料流程的畫面播放速率。</span><span class="sxs-lookup"><span data-stu-id="9be1f-146">Retrieves the frame rate of the current stream.</span></span><br/>                                                 |
| [<span data-ttu-id="9be1f-147">**取得 \_ OutputStreams**</span><span class="sxs-lookup"><span data-stu-id="9be1f-147">**get\_OutputStreams**</span></span>](imediadet-get-outputstreams.md)     | <span data-ttu-id="9be1f-148">抓取媒體來源中包含的音訊和影片資料流程數目。</span><span class="sxs-lookup"><span data-stu-id="9be1f-148">Retrieves the number of audio and video streams contained in the media source.</span></span><br/>                  |
| [<span data-ttu-id="9be1f-149">**取得 \_ StreamLength**</span><span class="sxs-lookup"><span data-stu-id="9be1f-149">**get\_StreamLength**</span></span>](imediadet-get-streamlength.md)       | <span data-ttu-id="9be1f-150">捕獲目前資料流程的持續時間。</span><span class="sxs-lookup"><span data-stu-id="9be1f-150">Retrieves the duration of the current stream.</span></span><br/>                                                   |
| [<span data-ttu-id="9be1f-151">**取得 \_ StreamMediaType**</span><span class="sxs-lookup"><span data-stu-id="9be1f-151">**get\_StreamMediaType**</span></span>](imediadet-get-streammediatype.md) | <span data-ttu-id="9be1f-152">抓取目前資料流程的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="9be1f-152">Retrieves the media type of the current stream.</span></span><br/>                                                 |
| [<span data-ttu-id="9be1f-153">**取得 \_ StreamType**</span><span class="sxs-lookup"><span data-stu-id="9be1f-153">**get\_StreamType**</span></span>](imediadet-get-streamtype.md)           | <span data-ttu-id="9be1f-154">針對目前資料流程的媒體類型，抓取全域唯一識別碼 (GUID) 。</span><span class="sxs-lookup"><span data-stu-id="9be1f-154">Retrieves the globally unique identifier (GUID) for the media type of the current stream.</span></span><br/>       |
| [<span data-ttu-id="9be1f-155">**取得 \_ StreamTypeB**</span><span class="sxs-lookup"><span data-stu-id="9be1f-155">**get\_StreamTypeB**</span></span>](imediadet-get-streamtypeb.md)         | <span data-ttu-id="9be1f-156">抓取字串，表示目前資料流程之媒體類型的 GUID。</span><span class="sxs-lookup"><span data-stu-id="9be1f-156">Retrieves a string representing the GUID of the media type for the current stream.</span></span><br/>              |
| [<span data-ttu-id="9be1f-157">**GetBitmapBits**</span><span class="sxs-lookup"><span data-stu-id="9be1f-157">**GetBitmapBits**</span></span>](imediadet-getbitmapbits.md)              | <span data-ttu-id="9be1f-158">抓取指定媒體時間的影片畫面。</span><span class="sxs-lookup"><span data-stu-id="9be1f-158">Retrieves a video frame at the specified media time.</span></span><br/>                                            |
| [<span data-ttu-id="9be1f-159">**GetSampleGrabber**</span><span class="sxs-lookup"><span data-stu-id="9be1f-159">**GetSampleGrabber**</span></span>](imediadet-getsamplegrabber.md)        | <span data-ttu-id="9be1f-160">捕獲 [**ISampleGrabber**](isamplegrabber.md) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="9be1f-160">Retrieves a pointer to the [**ISampleGrabber**](isamplegrabber.md) interface.</span></span><br/>                  |
| [<span data-ttu-id="9be1f-161">**put \_ CurrentStream**</span><span class="sxs-lookup"><span data-stu-id="9be1f-161">**put\_CurrentStream**</span></span>](imediadet-put-currentstream.md)     | <span data-ttu-id="9be1f-162">指定要使用之媒體偵測器的串流號碼。</span><span class="sxs-lookup"><span data-stu-id="9be1f-162">Specifies the stream number for the media detector to use.</span></span><br/>                                      |
| [<span data-ttu-id="9be1f-163">**放置 \_ 檔案名**</span><span class="sxs-lookup"><span data-stu-id="9be1f-163">**put\_Filename**</span></span>](imediadet-put-filename.md)               | <span data-ttu-id="9be1f-164">指定媒體偵測器要使用的原始程式檔名稱。</span><span class="sxs-lookup"><span data-stu-id="9be1f-164">Specifies the name of the source file for the media detector to use.</span></span><br/>                            |
| [<span data-ttu-id="9be1f-165">**put \_ 篩選**</span><span class="sxs-lookup"><span data-stu-id="9be1f-165">**put\_Filter**</span></span>](imediadet-put-filter.md)                   | <span data-ttu-id="9be1f-166">指定媒體偵測器要使用的來源篩選器。</span><span class="sxs-lookup"><span data-stu-id="9be1f-166">Specifies a source filter for the media detector to use.</span></span><br/>                                        |
| [<span data-ttu-id="9be1f-167">**WriteBitmapBits**</span><span class="sxs-lookup"><span data-stu-id="9be1f-167">**WriteBitmapBits**</span></span>](imediadet-writebitmapbits.md)          | <span data-ttu-id="9be1f-168">在指定的媒體時間抓取影片畫面格，並將其寫入檔案。</span><span class="sxs-lookup"><span data-stu-id="9be1f-168">Retrieves a video frame at the specified media time and writes it to a file.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="9be1f-169">備註</span><span class="sxs-lookup"><span data-stu-id="9be1f-169">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="9be1f-170">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="9be1f-170">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="9be1f-171">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="9be1f-171">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="9be1f-172">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="9be1f-172">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9be1f-173">規格需求</span><span class="sxs-lookup"><span data-stu-id="9be1f-173">Requirements</span></span>



| <span data-ttu-id="9be1f-174">需求</span><span class="sxs-lookup"><span data-stu-id="9be1f-174">Requirement</span></span> | <span data-ttu-id="9be1f-175">值</span><span class="sxs-lookup"><span data-stu-id="9be1f-175">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9be1f-176">標頭</span><span class="sxs-lookup"><span data-stu-id="9be1f-176">Header</span></span><br/>  | <dl> <span data-ttu-id="9be1f-177"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="9be1f-177"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="9be1f-178">程式庫</span><span class="sxs-lookup"><span data-stu-id="9be1f-178">Library</span></span><br/> | <dl> <span data-ttu-id="9be1f-179"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="9be1f-179"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 
