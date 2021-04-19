---
description: IAMTimelineTrack 介面提供在 DirectShow 編輯服務 (DES) 中操作追蹤物件的方法。追蹤包含在最終輸出中所呈現的來源清單。
ms.assetid: 42ac88f2-1361-413a-a9b0-95f5c32a7c3c
title: 'IAMTimelineTrack 介面 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 71003694d33b33980fb262f06f6b2e7aa55a70d1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994894"
---
# <a name="iamtimelinetrack-interface"></a><span data-ttu-id="1923e-103">IAMTimelineTrack 介面</span><span class="sxs-lookup"><span data-stu-id="1923e-103">IAMTimelineTrack interface</span></span>

> [!Note]  
> <span data-ttu-id="1923e-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="1923e-104">\[Deprecated.</span></span> <span data-ttu-id="1923e-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="1923e-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="1923e-106">`IAMTimelineTrack`介面提供在 [DirectShow 編輯服務](directshow-editing-services.md) (DES) 中操作 *追蹤* 物件的方法。</span><span class="sxs-lookup"><span data-stu-id="1923e-106">The `IAMTimelineTrack` interface provides methods for manipulating *track* objects in [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span>

<span data-ttu-id="1923e-107">追蹤包含在最終輸出中所呈現的來源清單。</span><span class="sxs-lookup"><span data-stu-id="1923e-107">A track contains a list of sources that are rendered in the final output.</span></span> <span data-ttu-id="1923e-108">相同播放軌內的來源可能不會重迭。</span><span class="sxs-lookup"><span data-stu-id="1923e-108">Sources within the same track may not overlap.</span></span> <span data-ttu-id="1923e-109">影片播放軌可以有效果和轉換。</span><span class="sxs-lookup"><span data-stu-id="1923e-109">Video tracks can have both effects and transitions.</span></span> <span data-ttu-id="1923e-110">轉譯引擎會在套用轉換之前套用效果。</span><span class="sxs-lookup"><span data-stu-id="1923e-110">The render engine applies effects before it applies transitions.</span></span> <span data-ttu-id="1923e-111">音訊播放軌可以有效果，但不能有轉換。</span><span class="sxs-lookup"><span data-stu-id="1923e-111">Audio tracks can have effects, but not transitions.</span></span> <span data-ttu-id="1923e-112">如需詳細資訊，請參閱 [時間軸模型](the-timeline-model.md)。</span><span class="sxs-lookup"><span data-stu-id="1923e-112">For more information, see [The Timeline Model](the-timeline-model.md).</span></span>

<span data-ttu-id="1923e-113">若要建立 track 物件，請呼叫 [**IAMTimeline：： CreateEmptyNode**](iamtimeline-createemptynode.md) ，並提供值時間軸的 \_ 主要 \_ 類型 \_ 追蹤。</span><span class="sxs-lookup"><span data-stu-id="1923e-113">To create a track object, call [**IAMTimeline::CreateEmptyNode**](iamtimeline-createemptynode.md) with the value TIMELINE\_MAJOR\_TYPE\_TRACK.</span></span> <span data-ttu-id="1923e-114">您可以查詢傳回的介面 **IAMTimelineObj** 指標 `IAMTimelineTrack` 。</span><span class="sxs-lookup"><span data-stu-id="1923e-114">You can query the returned **IAMTimelineObj** pointer for the `IAMTimelineTrack` interface.</span></span>

## <a name="members"></a><span data-ttu-id="1923e-115">成員</span><span class="sxs-lookup"><span data-stu-id="1923e-115">Members</span></span>

<span data-ttu-id="1923e-116">**IAMTimelineTrack** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="1923e-116">The **IAMTimelineTrack** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="1923e-117">**IAMTimelineTrack** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="1923e-117">**IAMTimelineTrack** also has these types of members:</span></span>

-   [<span data-ttu-id="1923e-118">方法</span><span class="sxs-lookup"><span data-stu-id="1923e-118">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="1923e-119">方法</span><span class="sxs-lookup"><span data-stu-id="1923e-119">Methods</span></span>

<span data-ttu-id="1923e-120">**IAMTimelineTrack** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="1923e-120">The **IAMTimelineTrack** interface has these methods.</span></span>



| <span data-ttu-id="1923e-121">方法</span><span class="sxs-lookup"><span data-stu-id="1923e-121">Method</span></span>                                                          | <span data-ttu-id="1923e-122">描述</span><span class="sxs-lookup"><span data-stu-id="1923e-122">Description</span></span>                                                                                                                                          |
|:----------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1923e-123">**AreYouBlank**</span><span class="sxs-lookup"><span data-stu-id="1923e-123">**AreYouBlank**</span></span>](iamtimelinetrack-areyoublank.md)             | <span data-ttu-id="1923e-124">判斷此曲目是否為空白 (不包含任何來源物件) 。</span><span class="sxs-lookup"><span data-stu-id="1923e-124">Determines whether the track is blank (contains no source objects).</span></span><br/>                                                                       |
| [<span data-ttu-id="1923e-125">**GetNextSrc**</span><span class="sxs-lookup"><span data-stu-id="1923e-125">**GetNextSrc**</span></span>](iamtimelinetrack-getnextsrc.md)               | <span data-ttu-id="1923e-126">搜尋播放程式在指定時間或之後出現的下一個來源的軌跡。</span><span class="sxs-lookup"><span data-stu-id="1923e-126">Searches the track for the next source that appears at the specified time or later.</span></span><br/>                                                       |
| [<span data-ttu-id="1923e-127">**GetNextSrc2**</span><span class="sxs-lookup"><span data-stu-id="1923e-127">**GetNextSrc2**</span></span>](iamtimelinetrack-getnextsrc2.md)             | <span data-ttu-id="1923e-128">使用指定的做為 [**REFTIME**](reftime.md) 值，在曲目中搜尋在指定時間或之後出現的下一個來源。</span><span class="sxs-lookup"><span data-stu-id="1923e-128">Searches the track for the next source that appears at the specified time or later, with the given as a [**REFTIME**](reftime.md) value.</span></span><br/> |
| [<span data-ttu-id="1923e-129">**GetNextSrcEx**</span><span class="sxs-lookup"><span data-stu-id="1923e-129">**GetNextSrcEx**</span></span>](iamtimelinetrack-getnextsrcex.md)           | <span data-ttu-id="1923e-130">抓取指定來源之後的下一個來源。</span><span class="sxs-lookup"><span data-stu-id="1923e-130">Retrieves the next source after the specified source.</span></span><br/>                                                                                     |
| [<span data-ttu-id="1923e-131">**GetSourcesCount**</span><span class="sxs-lookup"><span data-stu-id="1923e-131">**GetSourcesCount**</span></span>](iamtimelinetrack-getsourcescount.md)     | <span data-ttu-id="1923e-132">抓取曲目中的來源數目。</span><span class="sxs-lookup"><span data-stu-id="1923e-132">Retrieves the number of sources in the track.</span></span><br/>                                                                                             |
| [<span data-ttu-id="1923e-133">**GetSrcAtTime**</span><span class="sxs-lookup"><span data-stu-id="1923e-133">**GetSrcAtTime**</span></span>](iamtimelinetrack-getsrcattime.md)           | <span data-ttu-id="1923e-134">根據指定的界限條件，抓取最接近指定時間的來源物件。</span><span class="sxs-lookup"><span data-stu-id="1923e-134">Retrieves the source object nearest to the specified time, according to the specified boundary conditions.</span></span><br/>                                |
| [<span data-ttu-id="1923e-135">**GetSrcAtTime2**</span><span class="sxs-lookup"><span data-stu-id="1923e-135">**GetSrcAtTime2**</span></span>](iamtimelinetrack-getsrcattime2.md)         | <span data-ttu-id="1923e-136">取得最接近指定時間的來源物件，指定為 [**REFTIME**](reftime.md) 值。</span><span class="sxs-lookup"><span data-stu-id="1923e-136">Retrieves the source object nearest to the specified time, given as a [**REFTIME**](reftime.md) value.</span></span><br/>                                   |
| [<span data-ttu-id="1923e-137">**InsertSpace**</span><span class="sxs-lookup"><span data-stu-id="1923e-137">**InsertSpace**</span></span>](iamtimelinetrack-insertspace.md)             | <span data-ttu-id="1923e-138">分割存在於指定時間的任何物件，並在兩者之間插入空格。</span><span class="sxs-lookup"><span data-stu-id="1923e-138">Splits any objects that exist at the specified time and inserts space between them.</span></span><br/>                                                       |
| [<span data-ttu-id="1923e-139">**InsertSpace2**</span><span class="sxs-lookup"><span data-stu-id="1923e-139">**InsertSpace2**</span></span>](iamtimelinetrack-insertspace2.md)           | <span data-ttu-id="1923e-140">使用 [**REFTIME**](reftime.md) 值，分割存在於指定時間的任何物件，並在兩者之間插入空格。</span><span class="sxs-lookup"><span data-stu-id="1923e-140">Splits any objects that exist at the specified time and inserts space between them, using [**REFTIME**](reftime.md) values.</span></span><br/>              |
| [<span data-ttu-id="1923e-141">**MoveEverythingBy**</span><span class="sxs-lookup"><span data-stu-id="1923e-141">**MoveEverythingBy**</span></span>](iamtimelinetrack-moveeverythingby.md)   | <span data-ttu-id="1923e-142">不支援。</span><span class="sxs-lookup"><span data-stu-id="1923e-142">Not supported.</span></span><br/>                                                                                                                            |
| [<span data-ttu-id="1923e-143">**MoveEverythingBy2**</span><span class="sxs-lookup"><span data-stu-id="1923e-143">**MoveEverythingBy2**</span></span>](iamtimelinetrack-moveeverythingby2.md) | <span data-ttu-id="1923e-144">不支援。</span><span class="sxs-lookup"><span data-stu-id="1923e-144">Not supported.</span></span><br/>                                                                                                                            |
| [<span data-ttu-id="1923e-145">**SrcAdd**</span><span class="sxs-lookup"><span data-stu-id="1923e-145">**SrcAdd**</span></span>](iamtimelinetrack-srcadd.md)                       | <span data-ttu-id="1923e-146">將來源新增至曲目。</span><span class="sxs-lookup"><span data-stu-id="1923e-146">Adds a source to the track.</span></span><br/>                                                                                                               |
| [<span data-ttu-id="1923e-147">**ZeroBetween**</span><span class="sxs-lookup"><span data-stu-id="1923e-147">**ZeroBetween**</span></span>](iamtimelinetrack-zerobetween.md)             | <span data-ttu-id="1923e-148">從指定時間之間的曲目中移除所有專案。</span><span class="sxs-lookup"><span data-stu-id="1923e-148">Removes everything from the track between the specified times.</span></span><br/>                                                                            |
| [<span data-ttu-id="1923e-149">**ZeroBetween2**</span><span class="sxs-lookup"><span data-stu-id="1923e-149">**ZeroBetween2**</span></span>](iamtimelinetrack-zerobetween2.md)           | <span data-ttu-id="1923e-150">從指定時間（指定為 [**REFTIME**](reftime.md) 值）之間的追蹤中移除所有專案。</span><span class="sxs-lookup"><span data-stu-id="1923e-150">Removes everything from the track between the specified times, given as [**REFTIME**](reftime.md) values.</span></span><br/>                                |



 

## <a name="remarks"></a><span data-ttu-id="1923e-151">備註</span><span class="sxs-lookup"><span data-stu-id="1923e-151">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="1923e-152">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="1923e-152">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="1923e-153">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="1923e-153">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="1923e-154">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="1923e-154">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="1923e-155">規格需求</span><span class="sxs-lookup"><span data-stu-id="1923e-155">Requirements</span></span>



| <span data-ttu-id="1923e-156">需求</span><span class="sxs-lookup"><span data-stu-id="1923e-156">Requirement</span></span> | <span data-ttu-id="1923e-157">值</span><span class="sxs-lookup"><span data-stu-id="1923e-157">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1923e-158">標頭</span><span class="sxs-lookup"><span data-stu-id="1923e-158">Header</span></span><br/>  | <dl> <span data-ttu-id="1923e-159"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="1923e-159"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="1923e-160">程式庫</span><span class="sxs-lookup"><span data-stu-id="1923e-160">Library</span></span><br/> | <dl> <span data-ttu-id="1923e-161"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="1923e-161"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 
