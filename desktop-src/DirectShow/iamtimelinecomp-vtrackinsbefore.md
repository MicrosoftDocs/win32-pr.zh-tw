---
description: VTrackInsBefore 方法會依指定的優先順序，將虛擬追蹤插入組合中。
ms.assetid: 82ae0867-13b6-41ae-adb9-a55ac78e21cb
title: 'IAMTimelineComp：： VTrackInsBefore 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineComp.VTrackInsBefore
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ff5356591db6ccd20de720efd898387240075f19
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996455"
---
# <a name="iamtimelinecompvtrackinsbefore-method"></a><span data-ttu-id="dcdd1-103">IAMTimelineComp：： VTrackInsBefore 方法</span><span class="sxs-lookup"><span data-stu-id="dcdd1-103">IAMTimelineComp::VTrackInsBefore method</span></span>

> [!Note]  
> <span data-ttu-id="dcdd1-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="dcdd1-104">\[Deprecated.</span></span> <span data-ttu-id="dcdd1-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="dcdd1-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="dcdd1-106">方法會依 `VTrackInsBefore` 指定的優先順序，將虛擬追蹤插入組合中。</span><span class="sxs-lookup"><span data-stu-id="dcdd1-106">The `VTrackInsBefore` method inserts a virtual track into the composition at the specified priority.</span></span>

## <a name="syntax"></a><span data-ttu-id="dcdd1-107">語法</span><span class="sxs-lookup"><span data-stu-id="dcdd1-107">Syntax</span></span>


```C++
HRESULT VTrackInsBefore(
   IAMTimelineObj *pVirtualTrack,
   long           Priority
);
```



## <a name="parameters"></a><span data-ttu-id="dcdd1-108">參數</span><span class="sxs-lookup"><span data-stu-id="dcdd1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dcdd1-109">*pVirtualTrack*</span><span class="sxs-lookup"><span data-stu-id="dcdd1-109">*pVirtualTrack*</span></span> 
</dt> <dd>

<span data-ttu-id="dcdd1-110">虛擬追蹤的 [**IAMTimelineObj**](iamtimelineobj.md) 介面指標。</span><span class="sxs-lookup"><span data-stu-id="dcdd1-110">Pointer to the [**IAMTimelineObj**](iamtimelineobj.md) interface of the virtual track.</span></span>

</dd> <dt>

<span data-ttu-id="dcdd1-111">*優先順序*</span><span class="sxs-lookup"><span data-stu-id="dcdd1-111">*Priority*</span></span> 
</dt> <dd>

<span data-ttu-id="dcdd1-112">要插入虛擬追蹤的優先順序，或-1 則會在優先順序清單的結尾插入虛擬記錄。</span><span class="sxs-lookup"><span data-stu-id="dcdd1-112">Priority at which to insert the virtual track, or –1 to insert the virtual track at the end of the priority list.</span></span> <span data-ttu-id="dcdd1-113">優先權清單決定哪些剪輯是可見的。</span><span class="sxs-lookup"><span data-stu-id="dcdd1-113">The priority list determines which clips are visible.</span></span> <span data-ttu-id="dcdd1-114">如需詳細資訊，請參閱「備註」。</span><span class="sxs-lookup"><span data-stu-id="dcdd1-114">See Remarks for more information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dcdd1-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="dcdd1-115">Return value</span></span>

<span data-ttu-id="dcdd1-116">傳回下列其中一個 **HRESULT** 值：</span><span class="sxs-lookup"><span data-stu-id="dcdd1-116">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="dcdd1-117">傳回碼</span><span class="sxs-lookup"><span data-stu-id="dcdd1-117">Return code</span></span>                                                                                   | <span data-ttu-id="dcdd1-118">Description</span><span class="sxs-lookup"><span data-stu-id="dcdd1-118">Description</span></span>                               |
|-----------------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="dcdd1-119"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="dcdd1-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="dcdd1-120">成功。</span><span class="sxs-lookup"><span data-stu-id="dcdd1-120">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="dcdd1-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="dcdd1-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="dcdd1-122">無效引數。</span><span class="sxs-lookup"><span data-stu-id="dcdd1-122">Invalid argument.</span></span><br/>              |
| <dl> <span data-ttu-id="dcdd1-123"><dt>**E \_ NOINTERFACE**</dt></span><span class="sxs-lookup"><span data-stu-id="dcdd1-123"><dt>**E\_NOINTERFACE**</dt></span></span> </dl> | <span data-ttu-id="dcdd1-124">物件不是虛擬追蹤。</span><span class="sxs-lookup"><span data-stu-id="dcdd1-124">Object is not a virtual track.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="dcdd1-125">備註</span><span class="sxs-lookup"><span data-stu-id="dcdd1-125">Remarks</span></span>

<span data-ttu-id="dcdd1-126">組合中的每個虛擬追蹤都有唯一的優先權層級。</span><span class="sxs-lookup"><span data-stu-id="dcdd1-126">Each virtual track in composition has a unique priority level.</span></span> <span data-ttu-id="dcdd1-127">優先權層級的範圍是從0到 *n* -1，其中 *n* 是組合中的虛擬追蹤數目。</span><span class="sxs-lookup"><span data-stu-id="dcdd1-127">Priority levels range from 0 to *n* - 1, where *n* is the number of virtual tracks in the composition.</span></span> <span data-ttu-id="dcdd1-128">若為影片群組，虛擬追蹤會以較低的優先權層級隱藏任何虛擬追蹤，但追蹤是空的或包含轉換的位置除外。</span><span class="sxs-lookup"><span data-stu-id="dcdd1-128">For video groups, a virtual track hides any virtual tracks with a lower priority level, except in places where the track is empty or contains a transition.</span></span> <span data-ttu-id="dcdd1-129">您可以將虛擬追蹤視為最終組合中的圖層。</span><span class="sxs-lookup"><span data-stu-id="dcdd1-129">You can think of virtual tracks as being layers in the final composition.</span></span> <span data-ttu-id="dcdd1-130">Track 1 會分層置於曲目0的上方，而 track 2 則會分層顯示在曲目1的上方，依此類推。</span><span class="sxs-lookup"><span data-stu-id="dcdd1-130">Track 1 is layered on top of track 0, track 2 is layered on top of track 1, and so forth.</span></span>

<span data-ttu-id="dcdd1-131">如果您為 *Priority* 參數指定-1，則會在清單結尾插入虛擬追蹤，而且優先順序值會高於現有的追蹤。</span><span class="sxs-lookup"><span data-stu-id="dcdd1-131">If you specify -1 for the *Priority* parameter, the virtual track is inserted at the end of the list, with a higher priority value than the existing tracks.</span></span> <span data-ttu-id="dcdd1-132">如果您指定的優先順序值已存在於組合中，則每個具有相等或更高優先順序的追蹤都會向上移動一個優先權層級。</span><span class="sxs-lookup"><span data-stu-id="dcdd1-132">If you specify a priority value that already exists in the composition, every track with an equal or greater priority moves up one priority level.</span></span>

<span data-ttu-id="dcdd1-133">**範例**：追蹤 A 具有優先權0，而追蹤 B 的優先順序為1。</span><span class="sxs-lookup"><span data-stu-id="dcdd1-133">**Example**: Track A has priority 0, and track B has priority 1.</span></span> <span data-ttu-id="dcdd1-134">如果在優先順序0插入追蹤 C，請追蹤移至優先順序1，並將追蹤 B 移至優先順序2。</span><span class="sxs-lookup"><span data-stu-id="dcdd1-134">If track C is inserted at priority 0, track A moves to priority 1, and track B moves to priority 2.</span></span>

<span data-ttu-id="dcdd1-135">如果指定的優先順序大於組合中目前的曲目數，則方法會失敗。</span><span class="sxs-lookup"><span data-stu-id="dcdd1-135">If the specified priority is greater than the current number of tracks in the composition, the method fails.</span></span>

> [!Note]  
> <span data-ttu-id="dcdd1-136">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="dcdd1-136">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="dcdd1-137">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="dcdd1-137">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="dcdd1-138">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="dcdd1-138">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="dcdd1-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="dcdd1-139">Requirements</span></span>



| <span data-ttu-id="dcdd1-140">需求</span><span class="sxs-lookup"><span data-stu-id="dcdd1-140">Requirement</span></span> | <span data-ttu-id="dcdd1-141">值</span><span class="sxs-lookup"><span data-stu-id="dcdd1-141">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dcdd1-142">標頭</span><span class="sxs-lookup"><span data-stu-id="dcdd1-142">Header</span></span><br/>  | <dl> <span data-ttu-id="dcdd1-143"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="dcdd1-143"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="dcdd1-144">程式庫</span><span class="sxs-lookup"><span data-stu-id="dcdd1-144">Library</span></span><br/> | <dl> <span data-ttu-id="dcdd1-145"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="dcdd1-145"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dcdd1-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dcdd1-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dcdd1-147">**IAMTimelineComp 介面**</span><span class="sxs-lookup"><span data-stu-id="dcdd1-147">**IAMTimelineComp Interface**</span></span>](iamtimelinecomp.md)
</dt> <dt>

[<span data-ttu-id="dcdd1-148">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="dcdd1-148">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




