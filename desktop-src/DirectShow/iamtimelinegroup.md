---
description: IAMTimelineGroup 介面會設定及抓取 DirectShow 編輯服務 (DES) 中群組的屬性。群組包含一或多個追蹤，而且可能有一或多個組合，而這些組合接著會包含統一類型的來源剪輯，例如影片或音訊。 群組是時間軸中最上層的組合，也會公開 IAMTimelineComp 介面。 時間軸可以包含多個群組。每個群組都有下列屬性。相關聯的媒體類型。群組轉譯的畫面播放速率，以每秒畫面格數 (FPS) 。 所有的編輯都會在四捨五入到最接近的框架界限時進行，如群組 FPS 設定所定義。優先權層級，用於以相同媒體類型的多個資料流程寫入檔案 (例如，兩部影片串流 AVI 檔案) 。若要建立群組物件，請呼叫 IAMTimeline：： CreateEmptyNode 與值時間軸的 \_ 主要 \_ 類型 \_ 群組。 您可以查詢所傳回的 IAMTimelineGroup 介面 IAMTimelineObj 指標。
ms.assetid: c24e5e0a-43a5-4ba7-ac28-6e2ebb341a38
title: 'IAMTimelineGroup 介面 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e82a11db65183e343048f594a7457c0a8febf8bc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991250"
---
# <a name="iamtimelinegroup-interface"></a><span data-ttu-id="c208c-107">IAMTimelineGroup 介面</span><span class="sxs-lookup"><span data-stu-id="c208c-107">IAMTimelineGroup interface</span></span>

> [!Note]  
> <span data-ttu-id="c208c-108">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="c208c-108">\[Deprecated.</span></span> <span data-ttu-id="c208c-109">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="c208c-109">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="c208c-110">`IAMTimelineGroup`介面會設定及抓取[DirectShow 編輯服務](directshow-editing-services.md) (DES) 中群組的屬性。</span><span class="sxs-lookup"><span data-stu-id="c208c-110">The `IAMTimelineGroup` interface sets and retrieves properties on groups in [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span>

<span data-ttu-id="c208c-111">群組包含一或多個追蹤，而且可能有一或多個組合，而這些組合接著會包含統一類型的來源剪輯，例如影片或音訊。</span><span class="sxs-lookup"><span data-stu-id="c208c-111">A group contains one or more tracks, and possibly one or more compositions, which in turn contain source clips of a uniform type, such as video or audio.</span></span> <span data-ttu-id="c208c-112">群組是時間軸中最上層的組合，也會公開 [**IAMTimelineComp**](iamtimelinecomp.md) 介面。</span><span class="sxs-lookup"><span data-stu-id="c208c-112">Groups are the topmost compositions in a timeline, and also expose the [**IAMTimelineComp**](iamtimelinecomp.md) interface.</span></span> <span data-ttu-id="c208c-113">時間軸可以包含多個群組。</span><span class="sxs-lookup"><span data-stu-id="c208c-113">A timeline can contain multiple groups.</span></span>

<span data-ttu-id="c208c-114">每個群組都有下列屬性。</span><span class="sxs-lookup"><span data-stu-id="c208c-114">Each group has the following attributes.</span></span>

-   <span data-ttu-id="c208c-115">相關聯的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="c208c-115">An associated media type.</span></span>
-   <span data-ttu-id="c208c-116">群組轉譯的畫面播放速率，以每秒畫面格數 (FPS) 。</span><span class="sxs-lookup"><span data-stu-id="c208c-116">The frame rate at which the group renders, in frames per second (FPS).</span></span> <span data-ttu-id="c208c-117">所有的編輯都會在四捨五入到最接近的框架界限時進行，如群組 FPS 設定所定義。</span><span class="sxs-lookup"><span data-stu-id="c208c-117">All edits occur at a time rounded to the nearest frame boundary, as defined by the group's FPS setting.</span></span>
-   <span data-ttu-id="c208c-118">優先權層級，用於以相同媒體類型的多個資料流程寫入檔案 (例如，兩部影片串流 AVI 檔案) 。</span><span class="sxs-lookup"><span data-stu-id="c208c-118">A priority level, for writing files with multiple streams of the same media type (for example, a two-video-stream AVI file).</span></span>

<span data-ttu-id="c208c-119">若要建立群組物件，請呼叫 [**IAMTimeline：： CreateEmptyNode**](iamtimeline-createemptynode.md) 與值時間軸的 \_ 主要 \_ 類型 \_ 群組。</span><span class="sxs-lookup"><span data-stu-id="c208c-119">To create a group object, call [**IAMTimeline::CreateEmptyNode**](iamtimeline-createemptynode.md) with the value TIMELINE\_MAJOR\_TYPE\_GROUP.</span></span> <span data-ttu-id="c208c-120">您可以查詢所傳回的 **IAMTimelineGroup** 介面 [**IAMTimelineObj**](iamtimelineobj.md)指標。</span><span class="sxs-lookup"><span data-stu-id="c208c-120">You can query the returned [**IAMTimelineObj**](iamtimelineobj.md) pointer for the **IAMTimelineGroup** interface.</span></span>

## <a name="members"></a><span data-ttu-id="c208c-121">成員</span><span class="sxs-lookup"><span data-stu-id="c208c-121">Members</span></span>

<span data-ttu-id="c208c-122">**IAMTimelineGroup** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="c208c-122">The **IAMTimelineGroup** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="c208c-123">**IAMTimelineGroup** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="c208c-123">**IAMTimelineGroup** also has these types of members:</span></span>

-   [<span data-ttu-id="c208c-124">方法</span><span class="sxs-lookup"><span data-stu-id="c208c-124">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="c208c-125">方法</span><span class="sxs-lookup"><span data-stu-id="c208c-125">Methods</span></span>

<span data-ttu-id="c208c-126">**IAMTimelineGroup** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="c208c-126">The **IAMTimelineGroup** interface has these methods.</span></span>



| <span data-ttu-id="c208c-127">方法</span><span class="sxs-lookup"><span data-stu-id="c208c-127">Method</span></span>                                                                            | <span data-ttu-id="c208c-128">描述</span><span class="sxs-lookup"><span data-stu-id="c208c-128">Description</span></span>                                                                                     |
|:----------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c208c-129">**ClearRecompressFormatDirty**</span><span class="sxs-lookup"><span data-stu-id="c208c-129">**ClearRecompressFormatDirty**</span></span>](iamtimelinegroup-clearrecompressformatdirty.md) | <span data-ttu-id="c208c-130">不支援。</span><span class="sxs-lookup"><span data-stu-id="c208c-130">Not supported.</span></span><br/>                                                                       |
| [<span data-ttu-id="c208c-131">**GetGroupName**</span><span class="sxs-lookup"><span data-stu-id="c208c-131">**GetGroupName**</span></span>](iamtimelinegroup-getgroupname.md)                             | <span data-ttu-id="c208c-132">抓取群組的應用程式定義名稱。</span><span class="sxs-lookup"><span data-stu-id="c208c-132">Retrieves the application-defined name of the group.</span></span><br/>                                 |
| [<span data-ttu-id="c208c-133">**GetMediaType**</span><span class="sxs-lookup"><span data-stu-id="c208c-133">**GetMediaType**</span></span>](iamtimelinegroup-getmediatype.md)                             | <span data-ttu-id="c208c-134">抓取群組的未壓縮媒體類型。</span><span class="sxs-lookup"><span data-stu-id="c208c-134">Retrieves the uncompressed media type for the group.</span></span><br/>                                 |
| [<span data-ttu-id="c208c-135">**GetOutputBuffering**</span><span class="sxs-lookup"><span data-stu-id="c208c-135">**GetOutputBuffering**</span></span>](iamtimelinegroup-getoutputbuffering.md)                 | <span data-ttu-id="c208c-136">抓取預覽期間預先轉譯的畫面格數目。</span><span class="sxs-lookup"><span data-stu-id="c208c-136">Retrieves the number of frames rendered in advance during preview.</span></span><br/>                   |
| [<span data-ttu-id="c208c-137">**GetOutputFPS**</span><span class="sxs-lookup"><span data-stu-id="c208c-137">**GetOutputFPS**</span></span>](iamtimelinegroup-getoutputfps.md)                             | <span data-ttu-id="c208c-138">捕獲此群組的輸出畫面播放速率。</span><span class="sxs-lookup"><span data-stu-id="c208c-138">Retrieves the output frame rate of this group.</span></span><br/>                                       |
| [<span data-ttu-id="c208c-139">**GetPreviewMode**</span><span class="sxs-lookup"><span data-stu-id="c208c-139">**GetPreviewMode**</span></span>](iamtimelinegroup-getpreviewmode.md)                         | <span data-ttu-id="c208c-140">抓取群組的預覽模式。</span><span class="sxs-lookup"><span data-stu-id="c208c-140">Retrieves the preview mode for the group.</span></span><br/>                                            |
| [<span data-ttu-id="c208c-141">**GetPriority**</span><span class="sxs-lookup"><span data-stu-id="c208c-141">**GetPriority**</span></span>](iamtimelinegroup-getpriority.md)                               | <span data-ttu-id="c208c-142">抓取群組的優先順序。</span><span class="sxs-lookup"><span data-stu-id="c208c-142">Retrieves the group's priority.</span></span><br/>                                                      |
| [<span data-ttu-id="c208c-143">**GetSmartRecompressFormat**</span><span class="sxs-lookup"><span data-stu-id="c208c-143">**GetSmartRecompressFormat**</span></span>](iamtimelinegroup-getsmartrecompressformat.md)     | <span data-ttu-id="c208c-144">抓取 smart recompression 目前的壓縮格式。</span><span class="sxs-lookup"><span data-stu-id="c208c-144">Retrieves the current compression format for smart recompression.</span></span><br/>                    |
| [<span data-ttu-id="c208c-145">**GetTimeline**</span><span class="sxs-lookup"><span data-stu-id="c208c-145">**GetTimeline**</span></span>](iamtimelinegroup-gettimeline.md)                               | <span data-ttu-id="c208c-146">抓取此群組所屬的時間軸。</span><span class="sxs-lookup"><span data-stu-id="c208c-146">Retrieves the timeline to which this group belongs.</span></span><br/>                                  |
| [<span data-ttu-id="c208c-147">**IsRecompressFormatDirty**</span><span class="sxs-lookup"><span data-stu-id="c208c-147">**IsRecompressFormatDirty**</span></span>](iamtimelinegroup-isrecompressformatdirty.md)       | <span data-ttu-id="c208c-148">不支援。</span><span class="sxs-lookup"><span data-stu-id="c208c-148">Not supported.</span></span><br/>                                                                       |
| [<span data-ttu-id="c208c-149">**IsSmartRecompressFormatSet**</span><span class="sxs-lookup"><span data-stu-id="c208c-149">**IsSmartRecompressFormatSet**</span></span>](iamtimelinegroup-issmartrecompressformatset.md) | <span data-ttu-id="c208c-150">判斷是否已針對群組設定智慧壓縮格式。</span><span class="sxs-lookup"><span data-stu-id="c208c-150">Determines whether a smart compression format was set for the group.</span></span><br/>                 |
| [<span data-ttu-id="c208c-151">**SetGroupName**</span><span class="sxs-lookup"><span data-stu-id="c208c-151">**SetGroupName**</span></span>](iamtimelinegroup-setgroupname.md)                             | <span data-ttu-id="c208c-152">設定群組的應用程式定義名稱。</span><span class="sxs-lookup"><span data-stu-id="c208c-152">Sets the application-defined name of the group.</span></span><br/>                                      |
| [<span data-ttu-id="c208c-153">**SetMediaType**</span><span class="sxs-lookup"><span data-stu-id="c208c-153">**SetMediaType**</span></span>](iamtimelinegroup-setmediatype.md)                             | <span data-ttu-id="c208c-154">設定群組的未壓縮媒體類型。</span><span class="sxs-lookup"><span data-stu-id="c208c-154">Sets the uncompressed media type for the group.</span></span><br/>                                      |
| [<span data-ttu-id="c208c-155">**SetMediaTypeForVB**</span><span class="sxs-lookup"><span data-stu-id="c208c-155">**SetMediaTypeForVB**</span></span>](iamtimelinegroup-setmediatypeforvb.md)                   | <span data-ttu-id="c208c-156">指定 Automation 用戶端的群組媒體類型。</span><span class="sxs-lookup"><span data-stu-id="c208c-156">Specifies the group media type, for Automation clients.</span></span><br/>                              |
| [<span data-ttu-id="c208c-157">**SetOutputBuffering**</span><span class="sxs-lookup"><span data-stu-id="c208c-157">**SetOutputBuffering**</span></span>](iamtimelinegroup-setoutputbuffering.md)                 | <span data-ttu-id="c208c-158">指定預覽期間預先轉譯的畫面格數目。</span><span class="sxs-lookup"><span data-stu-id="c208c-158">Specifies the number of frames rendered in advance during preview.</span></span><br/>                   |
| [<span data-ttu-id="c208c-159">**SetOutputFPS**</span><span class="sxs-lookup"><span data-stu-id="c208c-159">**SetOutputFPS**</span></span>](iamtimelinegroup-setoutputfps.md)                             | <span data-ttu-id="c208c-160">設定此群組的未壓縮輸出畫面播放速率。</span><span class="sxs-lookup"><span data-stu-id="c208c-160">Sets the uncompressed output frame rate for this group.</span></span><br/>                              |
| [<span data-ttu-id="c208c-161">**SetPreviewMode**</span><span class="sxs-lookup"><span data-stu-id="c208c-161">**SetPreviewMode**</span></span>](iamtimelinegroup-setpreviewmode.md)                         | <span data-ttu-id="c208c-162">設定群組的預覽模式。</span><span class="sxs-lookup"><span data-stu-id="c208c-162">Sets the preview mode for the group.</span></span><br/>                                                 |
| [<span data-ttu-id="c208c-163">**SetRecompFormatFromSource**</span><span class="sxs-lookup"><span data-stu-id="c208c-163">**SetRecompFormatFromSource**</span></span>](iamtimelinegroup-setrecompformatfromsource.md)   | <span data-ttu-id="c208c-164">使用來源檔案中的壓縮格式，設定影片 recompression 格式。</span><span class="sxs-lookup"><span data-stu-id="c208c-164">Sets the video recompression format using the compression format from a source file.</span></span><br/> |
| [<span data-ttu-id="c208c-165">**SetSmartRecompressFormat**</span><span class="sxs-lookup"><span data-stu-id="c208c-165">**SetSmartRecompressFormat**</span></span>](iamtimelinegroup-setsmartrecompressformat.md)     | <span data-ttu-id="c208c-166">指定用於智慧型 recompression 的壓縮格式。</span><span class="sxs-lookup"><span data-stu-id="c208c-166">Specifies a compression format to use for smart recompression.</span></span><br/>                       |
| [<span data-ttu-id="c208c-167">**SetTimeline**</span><span class="sxs-lookup"><span data-stu-id="c208c-167">**SetTimeline**</span></span>](iamtimelinegroup-settimeline.md)                               | <span data-ttu-id="c208c-168">不支援。</span><span class="sxs-lookup"><span data-stu-id="c208c-168">Not supported.</span></span><br/>                                                                       |



 

## <a name="remarks"></a><span data-ttu-id="c208c-169">備註</span><span class="sxs-lookup"><span data-stu-id="c208c-169">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="c208c-170">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="c208c-170">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="c208c-171">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="c208c-171">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="c208c-172">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="c208c-172">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c208c-173">規格需求</span><span class="sxs-lookup"><span data-stu-id="c208c-173">Requirements</span></span>



| <span data-ttu-id="c208c-174">需求</span><span class="sxs-lookup"><span data-stu-id="c208c-174">Requirement</span></span> | <span data-ttu-id="c208c-175">值</span><span class="sxs-lookup"><span data-stu-id="c208c-175">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c208c-176">標頭</span><span class="sxs-lookup"><span data-stu-id="c208c-176">Header</span></span><br/>  | <dl> <span data-ttu-id="c208c-177"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="c208c-177"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="c208c-178">程式庫</span><span class="sxs-lookup"><span data-stu-id="c208c-178">Library</span></span><br/> | <dl> <span data-ttu-id="c208c-179"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="c208c-179"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 
