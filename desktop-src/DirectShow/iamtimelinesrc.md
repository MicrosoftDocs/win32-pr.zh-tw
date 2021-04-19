---
description: IAMTimelineSrc 介面會提供方法，在 (DES) 的 DirectShow 編輯服務中操作和設定來源物件上的屬性。
ms.assetid: 39a64718-1fac-4d90-8340-b712d3bad2ec
title: 'IAMTimelineSrc 介面 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 25733b1353bc0cbd92c40335a8d342473b03a806
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978611"
---
# <a name="iamtimelinesrc-interface"></a><span data-ttu-id="ccf00-103">IAMTimelineSrc 介面</span><span class="sxs-lookup"><span data-stu-id="ccf00-103">IAMTimelineSrc interface</span></span>

> [!Note]  
> <span data-ttu-id="ccf00-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="ccf00-104">\[Deprecated.</span></span> <span data-ttu-id="ccf00-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="ccf00-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="ccf00-106">`IAMTimelineSrc`介面會提供方法，在 (DES) 的[DirectShow 編輯服務](directshow-editing-services.md)中操作和設定來源物件上的屬性。</span><span class="sxs-lookup"><span data-stu-id="ccf00-106">The `IAMTimelineSrc` interface provides methods for manipulating and setting properties on source objects in [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span> <span data-ttu-id="ccf00-107">來源物件代表來自媒體來源的一個資料流程。</span><span class="sxs-lookup"><span data-stu-id="ccf00-107">A source object represents one stream from a media source.</span></span>

<span data-ttu-id="ccf00-108">您可以設定媒體開始和媒體停止時間，以在原始程式檔中使用部分資料。</span><span class="sxs-lookup"><span data-stu-id="ccf00-108">You can use a portion of the data within a source file by setting the media start and media stop times.</span></span> <span data-ttu-id="ccf00-109">這些值會指定來源物件的開頭和結尾，相對於原始媒體來源。</span><span class="sxs-lookup"><span data-stu-id="ccf00-109">These values specify the beginning and end of the source object, relative to the original media source.</span></span> <span data-ttu-id="ccf00-110">媒體時間可能與物件在時間軸上的開始和停止時間不同，可進行快速或緩慢的播放動作。</span><span class="sxs-lookup"><span data-stu-id="ccf00-110">The media times can differ from the object's start and stop times on the timeline, allowing for fast- or slow-motion playback.</span></span> <span data-ttu-id="ccf00-111">使用音訊來源 (時，會發生音調變化。 ) </span><span class="sxs-lookup"><span data-stu-id="ccf00-111">(With audio sources, pitch shifting occurs.)</span></span>

<span data-ttu-id="ccf00-112">若要建立來源物件，請呼叫 [**IAMTimeline：： CreateEmptyNode**](iamtimeline-createemptynode.md) 與值時間軸的 \_ 主要 \_ 類型 \_ 來源。</span><span class="sxs-lookup"><span data-stu-id="ccf00-112">To create a source object, call [**IAMTimeline::CreateEmptyNode**](iamtimeline-createemptynode.md) with the value TIMELINE\_MAJOR\_TYPE\_SOURCE.</span></span> <span data-ttu-id="ccf00-113">您可以查詢所傳回的 **IAMTimelineSrc** 介面 [**IAMTimelineObj**](iamtimelineobj.md)指標。</span><span class="sxs-lookup"><span data-stu-id="ccf00-113">You can query the returned [**IAMTimelineObj**](iamtimelineobj.md) pointer for the **IAMTimelineSrc** interface.</span></span> <span data-ttu-id="ccf00-114">如需詳細資訊，請參閱 [建立時間軸](constructing-a-timeline.md) 和 [使用來源](working-with-sources.md)。</span><span class="sxs-lookup"><span data-stu-id="ccf00-114">For more information, see [Constructing a Timeline](constructing-a-timeline.md) and [Working with Sources](working-with-sources.md).</span></span>

## <a name="members"></a><span data-ttu-id="ccf00-115">成員</span><span class="sxs-lookup"><span data-stu-id="ccf00-115">Members</span></span>

<span data-ttu-id="ccf00-116">**IAMTimelineSrc** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="ccf00-116">The **IAMTimelineSrc** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="ccf00-117">**IAMTimelineSrc** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="ccf00-117">**IAMTimelineSrc** also has these types of members:</span></span>

-   [<span data-ttu-id="ccf00-118">方法</span><span class="sxs-lookup"><span data-stu-id="ccf00-118">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="ccf00-119">方法</span><span class="sxs-lookup"><span data-stu-id="ccf00-119">Methods</span></span>

<span data-ttu-id="ccf00-120">**IAMTimelineSrc** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="ccf00-120">The **IAMTimelineSrc** interface has these methods.</span></span>



| <span data-ttu-id="ccf00-121">方法</span><span class="sxs-lookup"><span data-stu-id="ccf00-121">Method</span></span>                                                    | <span data-ttu-id="ccf00-122">描述</span><span class="sxs-lookup"><span data-stu-id="ccf00-122">Description</span></span>                                                                                              |
|:----------------------------------------------------------|:---------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ccf00-123">**FixMediaTimes**</span><span class="sxs-lookup"><span data-stu-id="ccf00-123">**FixMediaTimes**</span></span>](iamtimelinesrc-fixmediatimes.md)     | <span data-ttu-id="ccf00-124">將指定的時間值四捨五入到最接近的框架界限。</span><span class="sxs-lookup"><span data-stu-id="ccf00-124">Rounds the specified time values to the nearest frame boundary.</span></span><br/>                               |
| [<span data-ttu-id="ccf00-125">**FixMediaTimes2**</span><span class="sxs-lookup"><span data-stu-id="ccf00-125">**FixMediaTimes2**</span></span>](iamtimelinesrc-fixmediatimes2.md)   | <span data-ttu-id="ccf00-126">將指定的時間值（指定為 **REFTIME** 值）四捨五入至最接近的框架界限。</span><span class="sxs-lookup"><span data-stu-id="ccf00-126">Rounds the specified time values, given as **REFTIME** values, to the nearest frame boundary.</span></span><br/> |
| [<span data-ttu-id="ccf00-127">**GetDefaultFPS**</span><span class="sxs-lookup"><span data-stu-id="ccf00-127">**GetDefaultFPS**</span></span>](iamtimelinesrc-getdefaultfps.md)     | <span data-ttu-id="ccf00-128">抓取來源物件的預設畫面播放速率。</span><span class="sxs-lookup"><span data-stu-id="ccf00-128">Retrieves the source object's default frame rate.</span></span><br/>                                             |
| [<span data-ttu-id="ccf00-129">**GetMediaLength**</span><span class="sxs-lookup"><span data-stu-id="ccf00-129">**GetMediaLength**</span></span>](iamtimelinesrc-getmedialength.md)   | <span data-ttu-id="ccf00-130">抓取此來源物件的媒體長度。</span><span class="sxs-lookup"><span data-stu-id="ccf00-130">Retrieves the media length of this source object.</span></span><br/>                                             |
| [<span data-ttu-id="ccf00-131">**GetMediaLength2**</span><span class="sxs-lookup"><span data-stu-id="ccf00-131">**GetMediaLength2**</span></span>](iamtimelinesrc-getmedialength2.md) | <span data-ttu-id="ccf00-132">以 **REFTIME** 值形式抓取此來源物件的媒體長度。</span><span class="sxs-lookup"><span data-stu-id="ccf00-132">Retrieves the media length of this source object, as a **REFTIME** value.</span></span><br/>                     |
| [<span data-ttu-id="ccf00-133">**GetMediaName**</span><span class="sxs-lookup"><span data-stu-id="ccf00-133">**GetMediaName**</span></span>](iamtimelinesrc-getmedianame.md)       | <span data-ttu-id="ccf00-134">抓取此來源物件所表示之原始程式檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="ccf00-134">Retrieves the name of the source file represented by this source object.</span></span><br/>                      |
| [<span data-ttu-id="ccf00-135">**GetMediaTimes**</span><span class="sxs-lookup"><span data-stu-id="ccf00-135">**GetMediaTimes**</span></span>](iamtimelinesrc-getmediatimes.md)     | <span data-ttu-id="ccf00-136">抓取媒體的開始和停止時間。</span><span class="sxs-lookup"><span data-stu-id="ccf00-136">Retrieves the media start and stop times.</span></span><br/>                                                     |
| [<span data-ttu-id="ccf00-137">**GetMediaTimes2**</span><span class="sxs-lookup"><span data-stu-id="ccf00-137">**GetMediaTimes2**</span></span>](iamtimelinesrc-getmediatimes2.md)   | <span data-ttu-id="ccf00-138">以 **REFTIME** 值形式抓取媒體開始和停止時間。</span><span class="sxs-lookup"><span data-stu-id="ccf00-138">Retrieves the media start and stop times, as **REFTIME** values.</span></span><br/>                              |
| [<span data-ttu-id="ccf00-139">**GetStreamNumber**</span><span class="sxs-lookup"><span data-stu-id="ccf00-139">**GetStreamNumber**</span></span>](iamtimelinesrc-getstreamnumber.md) | <span data-ttu-id="ccf00-140">抓取來源物件目前的資料流程數目。</span><span class="sxs-lookup"><span data-stu-id="ccf00-140">Retrieves the current stream number for the source object.</span></span><br/>                                    |
| [<span data-ttu-id="ccf00-141">**GetStretchMode**</span><span class="sxs-lookup"><span data-stu-id="ccf00-141">**GetStretchMode**</span></span>](iamtimelinesrc-getstretchmode.md)   | <span data-ttu-id="ccf00-142">捕獲影片來源的延展模式。</span><span class="sxs-lookup"><span data-stu-id="ccf00-142">Retrieves the stretch mode of a video source.</span></span><br/>                                                 |
| [<span data-ttu-id="ccf00-143">**IsNormalRate**</span><span class="sxs-lookup"><span data-stu-id="ccf00-143">**IsNormalRate**</span></span>](iamtimelinesrc-isnormalrate.md)       | <span data-ttu-id="ccf00-144">指出是否會以正常播放速率播放剪輯。</span><span class="sxs-lookup"><span data-stu-id="ccf00-144">Indicates whether the clip will play at the normal playback rate.</span></span><br/>                             |
| [<span data-ttu-id="ccf00-145">**ModifyStopTime**</span><span class="sxs-lookup"><span data-stu-id="ccf00-145">**ModifyStopTime**</span></span>](iamtimelinesrc-modifystoptime.md)   | <span data-ttu-id="ccf00-146">設定相對於時程表的停止時間。</span><span class="sxs-lookup"><span data-stu-id="ccf00-146">Sets the stop time, relative to the timeline.</span></span><br/>                                                 |
| [<span data-ttu-id="ccf00-147">**ModifyStopTime2**</span><span class="sxs-lookup"><span data-stu-id="ccf00-147">**ModifyStopTime2**</span></span>](iamtimelinesrc-modifystoptime2.md) | <span data-ttu-id="ccf00-148">將停止時間設定為 **REFTIME** 值。</span><span class="sxs-lookup"><span data-stu-id="ccf00-148">Sets the stop time, as a **REFTIME** value.</span></span><br/>                                                   |
| [<span data-ttu-id="ccf00-149">**SetDefaultFPS**</span><span class="sxs-lookup"><span data-stu-id="ccf00-149">**SetDefaultFPS**</span></span>](iamtimelinesrc-setdefaultfps.md)     | <span data-ttu-id="ccf00-150">設定來源物件的預設畫面播放速率。</span><span class="sxs-lookup"><span data-stu-id="ccf00-150">Sets the source object's default frame rate.</span></span><br/>                                                  |
| [<span data-ttu-id="ccf00-151">**SetMediaLength**</span><span class="sxs-lookup"><span data-stu-id="ccf00-151">**SetMediaLength**</span></span>](iamtimelinesrc-setmedialength.md)   | <span data-ttu-id="ccf00-152">指定原始程式檔的持續時間。</span><span class="sxs-lookup"><span data-stu-id="ccf00-152">Specifies the duration of the source file.</span></span><br/>                                                    |
| [<span data-ttu-id="ccf00-153">**SetMediaLength2**</span><span class="sxs-lookup"><span data-stu-id="ccf00-153">**SetMediaLength2**</span></span>](iamtimelinesrc-setmedialength2.md) | <span data-ttu-id="ccf00-154">指定原始程式檔的持續時間，做為 **REFTIME** 值。</span><span class="sxs-lookup"><span data-stu-id="ccf00-154">Specifies the duration of the source file, as a **REFTIME** value.</span></span><br/>                            |
| [<span data-ttu-id="ccf00-155">**SetMediaName**</span><span class="sxs-lookup"><span data-stu-id="ccf00-155">**SetMediaName**</span></span>](iamtimelinesrc-setmedianame.md)       | <span data-ttu-id="ccf00-156">指定此來源物件所表示之原始程式檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="ccf00-156">Specifies the name of the source file represented by this source object.</span></span><br/>                      |
| [<span data-ttu-id="ccf00-157">**SetMediaTimes**</span><span class="sxs-lookup"><span data-stu-id="ccf00-157">**SetMediaTimes**</span></span>](iamtimelinesrc-setmediatimes.md)     | <span data-ttu-id="ccf00-158">設定媒體停止和開始時間。</span><span class="sxs-lookup"><span data-stu-id="ccf00-158">Sets the media stop and start times.</span></span><br/>                                                          |
| [<span data-ttu-id="ccf00-159">**SetMediaTimes2**</span><span class="sxs-lookup"><span data-stu-id="ccf00-159">**SetMediaTimes2**</span></span>](iamtimelinesrc-setmediatimes2.md)   | <span data-ttu-id="ccf00-160">將媒體停止和開始時間設定為 **REFTIME** 值。</span><span class="sxs-lookup"><span data-stu-id="ccf00-160">Sets the media stop and start times, as **REFTIME** values.</span></span><br/>                                   |
| [<span data-ttu-id="ccf00-161">**SetStreamNumber**</span><span class="sxs-lookup"><span data-stu-id="ccf00-161">**SetStreamNumber**</span></span>](iamtimelinesrc-setstreamnumber.md) | <span data-ttu-id="ccf00-162">指定要從與此來源物件相關聯之來源檔案讀取的資料流程。</span><span class="sxs-lookup"><span data-stu-id="ccf00-162">Specifies which stream to read from the source file associated with this source object.</span></span><br/>       |
| [<span data-ttu-id="ccf00-163">**SetStretchMode**</span><span class="sxs-lookup"><span data-stu-id="ccf00-163">**SetStretchMode**</span></span>](iamtimelinesrc-setstretchmode.md)   | <span data-ttu-id="ccf00-164">設定影片來源的延展模式。</span><span class="sxs-lookup"><span data-stu-id="ccf00-164">Sets the stretch mode of a video source.</span></span><br/>                                                      |
| [<span data-ttu-id="ccf00-165">**SpliceWithNext**</span><span class="sxs-lookup"><span data-stu-id="ccf00-165">**SpliceWithNext**</span></span>](iamtimelinesrc-splicewithnext.md)   | <span data-ttu-id="ccf00-166">將此來源物件聯結至另一個來源物件。</span><span class="sxs-lookup"><span data-stu-id="ccf00-166">Joins this source object to another source object.</span></span><br/>                                            |



 

## <a name="remarks"></a><span data-ttu-id="ccf00-167">備註</span><span class="sxs-lookup"><span data-stu-id="ccf00-167">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="ccf00-168">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="ccf00-168">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="ccf00-169">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="ccf00-169">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="ccf00-170">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="ccf00-170">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ccf00-171">規格需求</span><span class="sxs-lookup"><span data-stu-id="ccf00-171">Requirements</span></span>



| <span data-ttu-id="ccf00-172">需求</span><span class="sxs-lookup"><span data-stu-id="ccf00-172">Requirement</span></span> | <span data-ttu-id="ccf00-173">值</span><span class="sxs-lookup"><span data-stu-id="ccf00-173">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ccf00-174">標頭</span><span class="sxs-lookup"><span data-stu-id="ccf00-174">Header</span></span><br/>  | <dl> <span data-ttu-id="ccf00-175"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="ccf00-175"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="ccf00-176">程式庫</span><span class="sxs-lookup"><span data-stu-id="ccf00-176">Library</span></span><br/> | <dl> <span data-ttu-id="ccf00-177"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="ccf00-177"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 
