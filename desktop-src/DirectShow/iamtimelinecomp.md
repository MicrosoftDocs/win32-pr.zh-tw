---
description: IAMTimelineComp 介面會將虛擬追蹤插入或抓取 (DES) 的 DirectShow 編輯服務組合。組合是圖層的集合，可作為單一的複合播放軌。
ms.assetid: b0a47303-9e3c-4b78-ac90-c5d8fce2b727
title: 'IAMTimelineComp 介面 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineComp
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 645abbb9c5f61fcfd04e433c3cfc61b926ed403d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106997752"
---
# <a name="iamtimelinecomp-interface"></a><span data-ttu-id="3f9eb-103">IAMTimelineComp 介面</span><span class="sxs-lookup"><span data-stu-id="3f9eb-103">IAMTimelineComp interface</span></span>

> [!Note]  
> <span data-ttu-id="3f9eb-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="3f9eb-104">\[Deprecated.</span></span> <span data-ttu-id="3f9eb-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="3f9eb-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="3f9eb-106">**IAMTimelineComp** 介面會將虛擬追蹤插入或抓取 (DES) 的 [DirectShow 編輯服務](directshow-editing-services.md)組合。</span><span class="sxs-lookup"><span data-stu-id="3f9eb-106">The **IAMTimelineComp** interface inserts or retrieves virtual tracks on a composition in [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span>

<span data-ttu-id="3f9eb-107">組合是圖層的集合，可作為單一的複合播放 *軌*。例如，包含兩個追蹤的組合，其之間的轉換可作為轉換 precomposited 的單一追蹤。</span><span class="sxs-lookup"><span data-stu-id="3f9eb-107">A composition is a collection of layers that acts as a single, composited *track*. For example, a composition that contains two tracks with a transition between them acts as a single track with the transition precomposited.</span></span> <span data-ttu-id="3f9eb-108">組合應只包含一種類型的媒體 (例如音訊或影片) ，但不會強制執行這項限制。</span><span class="sxs-lookup"><span data-stu-id="3f9eb-108">A composition should contain media of only one type (such as audio or video), but this limitation is not enforced.</span></span> <span data-ttu-id="3f9eb-109">*虛擬追蹤* 是可位於組合中的任何物件，包括追蹤和其他組合。</span><span class="sxs-lookup"><span data-stu-id="3f9eb-109">A *virtual track* is any object that can reside in a composition, including tracks and other compositions.</span></span>

<span data-ttu-id="3f9eb-110">時間軸中的最上層節點是 *群組*。</span><span class="sxs-lookup"><span data-stu-id="3f9eb-110">The topmost nodes in the timeline are *groups*.</span></span> <span data-ttu-id="3f9eb-111">群組會同時執行 `IAMTimelineComp` 介面和 [**IAMTimelineGroup**](iamtimelinegroup.md) 介面。</span><span class="sxs-lookup"><span data-stu-id="3f9eb-111">Groups implement both the `IAMTimelineComp` interface and the [**IAMTimelineGroup**](iamtimelinegroup.md) interface.</span></span>

<span data-ttu-id="3f9eb-112">若要建立組合物件，請呼叫 [**IAMTimeline：： CreateEmptyNode**](iamtimeline-createemptynode.md) ，其值時間軸 \_ 主要 \_ 類型為 \_ 複合。</span><span class="sxs-lookup"><span data-stu-id="3f9eb-112">To create a composition object, call [**IAMTimeline::CreateEmptyNode**](iamtimeline-createemptynode.md) with the value TIMELINE\_MAJOR\_TYPE\_COMPOSITE.</span></span> <span data-ttu-id="3f9eb-113">您可以查詢傳回的介面 [**IAMTimelineObj**](iamtimelineobj.md) 指標 `IAMTimelineComp` 。</span><span class="sxs-lookup"><span data-stu-id="3f9eb-113">You can query the returned [**IAMTimelineObj**](iamtimelineobj.md) pointer for the `IAMTimelineComp` interface.</span></span> <span data-ttu-id="3f9eb-114">如需詳細資訊，請參閱 [時間軸模型](the-timeline-model.md) 和 [建立時間軸](constructing-a-timeline.md)。</span><span class="sxs-lookup"><span data-stu-id="3f9eb-114">For more information, see [The Timeline Model](the-timeline-model.md) and [Constructing a Timeline](constructing-a-timeline.md).</span></span>

## <a name="members"></a><span data-ttu-id="3f9eb-115">成員</span><span class="sxs-lookup"><span data-stu-id="3f9eb-115">Members</span></span>

<span data-ttu-id="3f9eb-116">**IAMTimelineComp** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="3f9eb-116">The **IAMTimelineComp** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="3f9eb-117">**IAMTimelineComp** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="3f9eb-117">**IAMTimelineComp** also has these types of members:</span></span>

-   [<span data-ttu-id="3f9eb-118">方法</span><span class="sxs-lookup"><span data-stu-id="3f9eb-118">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="3f9eb-119">方法</span><span class="sxs-lookup"><span data-stu-id="3f9eb-119">Methods</span></span>

<span data-ttu-id="3f9eb-120">**IAMTimelineComp** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="3f9eb-120">The **IAMTimelineComp** interface has these methods.</span></span>



| <span data-ttu-id="3f9eb-121">方法</span><span class="sxs-lookup"><span data-stu-id="3f9eb-121">Method</span></span>                                                                       | <span data-ttu-id="3f9eb-122">描述</span><span class="sxs-lookup"><span data-stu-id="3f9eb-122">Description</span></span>                                                                                                                                               |
|:-----------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3f9eb-123">**GetCountOfType**</span><span class="sxs-lookup"><span data-stu-id="3f9eb-123">**GetCountOfType**</span></span>](iamtimelinecomp-getcountoftype.md)                     | <span data-ttu-id="3f9eb-124">以遞迴方式抓取此組合中所包含之指定型別的物件數目及其所有虛擬追蹤。</span><span class="sxs-lookup"><span data-stu-id="3f9eb-124">Retrieves the number of objects of a given type contained in this composition and all of its virtual tracks, recursively.</span></span><br/>                      |
| [<span data-ttu-id="3f9eb-125">**GetNextVTrack**</span><span class="sxs-lookup"><span data-stu-id="3f9eb-125">**GetNextVTrack**</span></span>](iamtimelinecomp-getnextvtrack.md)                       | <span data-ttu-id="3f9eb-126">抓取指定虛擬追蹤之後的下一個虛擬追蹤。</span><span class="sxs-lookup"><span data-stu-id="3f9eb-126">Retrieves the next virtual track after a specified virtual track.</span></span><br/>                                                                              |
| [<span data-ttu-id="3f9eb-127">**GetRecursiveLayerOfType**</span><span class="sxs-lookup"><span data-stu-id="3f9eb-127">**GetRecursiveLayerOfType**</span></span>](iamtimelinecomp-getrecursivelayeroftype.md)   | <span data-ttu-id="3f9eb-128">執行此組合中所包含之虛擬追蹤的深度優先順序，並從該順序抓取 *n* 個虛擬追蹤。</span><span class="sxs-lookup"><span data-stu-id="3f9eb-128">Performs a depth-first ordering of the virtual tracks contained in this composition, and retrieves the *n* th virtual track from that ordering.</span></span><br/> |
| [<span data-ttu-id="3f9eb-129">**GetRecursiveLayerOfTypeI**</span><span class="sxs-lookup"><span data-stu-id="3f9eb-129">**GetRecursiveLayerOfTypeI**</span></span>](iamtimelinecomp-getrecursivelayeroftypei.md) | <span data-ttu-id="3f9eb-130">不支援。</span><span class="sxs-lookup"><span data-stu-id="3f9eb-130">Not supported.</span></span><br/>                                                                                                                                 |
| [<span data-ttu-id="3f9eb-131">**GetVTrack**</span><span class="sxs-lookup"><span data-stu-id="3f9eb-131">**GetVTrack**</span></span>](iamtimelinecomp-getvtrack.md)                               | <span data-ttu-id="3f9eb-132">依指定的優先順序抓取虛擬追蹤。</span><span class="sxs-lookup"><span data-stu-id="3f9eb-132">Retrieves the virtual track at the specified priority.</span></span><br/>                                                                                         |
| [<span data-ttu-id="3f9eb-133">**VTrackGetCount**</span><span class="sxs-lookup"><span data-stu-id="3f9eb-133">**VTrackGetCount**</span></span>](iamtimelinecomp-vtrackgetcount.md)                     | <span data-ttu-id="3f9eb-134">抓取組合中包含的虛擬追蹤數目。</span><span class="sxs-lookup"><span data-stu-id="3f9eb-134">Retrieves the number of virtual tracks contained in the composition.</span></span><br/>                                                                           |
| [<span data-ttu-id="3f9eb-135">**VTrackInsBefore**</span><span class="sxs-lookup"><span data-stu-id="3f9eb-135">**VTrackInsBefore**</span></span>](iamtimelinecomp-vtrackinsbefore.md)                   | <span data-ttu-id="3f9eb-136">依指定的優先順序將虛擬追蹤插入組合中。</span><span class="sxs-lookup"><span data-stu-id="3f9eb-136">Inserts a virtual track into the composition at the specified priority.</span></span><br/>                                                                        |
| [<span data-ttu-id="3f9eb-137">**VTrackSwapPriorities**</span><span class="sxs-lookup"><span data-stu-id="3f9eb-137">**VTrackSwapPriorities**</span></span>](iamtimelinecomp-vtrackswappriorities.md)         | <span data-ttu-id="3f9eb-138">切換兩個追蹤的優先權層級。</span><span class="sxs-lookup"><span data-stu-id="3f9eb-138">Switches the priority levels of two tracks.</span></span><br/>                                                                                                    |



 

## <a name="remarks"></a><span data-ttu-id="3f9eb-139">備註</span><span class="sxs-lookup"><span data-stu-id="3f9eb-139">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="3f9eb-140">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="3f9eb-140">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="3f9eb-141">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="3f9eb-141">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="3f9eb-142">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="3f9eb-142">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3f9eb-143">規格需求</span><span class="sxs-lookup"><span data-stu-id="3f9eb-143">Requirements</span></span>



| <span data-ttu-id="3f9eb-144">需求</span><span class="sxs-lookup"><span data-stu-id="3f9eb-144">Requirement</span></span> | <span data-ttu-id="3f9eb-145">值</span><span class="sxs-lookup"><span data-stu-id="3f9eb-145">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3f9eb-146">標頭</span><span class="sxs-lookup"><span data-stu-id="3f9eb-146">Header</span></span><br/>  | <dl> <span data-ttu-id="3f9eb-147"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="3f9eb-147"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="3f9eb-148">程式庫</span><span class="sxs-lookup"><span data-stu-id="3f9eb-148">Library</span></span><br/> | <dl> <span data-ttu-id="3f9eb-149"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="3f9eb-149"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 
