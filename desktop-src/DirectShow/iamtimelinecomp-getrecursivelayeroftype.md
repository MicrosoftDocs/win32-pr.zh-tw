---
description: GetRecursiveLayerOfType 方法會針對此組合所包含的虛擬追蹤執行深度優先的排序，並從該順序抓取第 n 個虛擬追蹤。
ms.assetid: 409914fd-3faf-418f-bca1-8adf2948f422
title: 'IAMTimelineComp：： GetRecursiveLayerOfType 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineComp.GetRecursiveLayerOfType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 28dfe8862561108588e57091e92ab2d424c79c26
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106980191"
---
# <a name="iamtimelinecompgetrecursivelayeroftype-method"></a><span data-ttu-id="8dac8-103">IAMTimelineComp：： GetRecursiveLayerOfType 方法</span><span class="sxs-lookup"><span data-stu-id="8dac8-103">IAMTimelineComp::GetRecursiveLayerOfType method</span></span>

> [!Note]  
> <span data-ttu-id="8dac8-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="8dac8-104">\[Deprecated.</span></span> <span data-ttu-id="8dac8-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="8dac8-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="8dac8-106">`GetRecursiveLayerOfType`方法會執行此組合中所包含之虛擬追蹤的深度優先排序，並從該順序抓取 *n* 個虛擬追蹤。</span><span class="sxs-lookup"><span data-stu-id="8dac8-106">The `GetRecursiveLayerOfType` method performs a depth-first ordering of the virtual tracks contained in this composition, and retrieves the *n* th virtual track from that ordering.</span></span>

## <a name="syntax"></a><span data-ttu-id="8dac8-107">語法</span><span class="sxs-lookup"><span data-stu-id="8dac8-107">Syntax</span></span>


```C++
HRESULT GetRecursiveLayerOfType(
  [out] IAMTimelineObj      **ppVirtualTrack,
        long                WhichLayer,
        TIMELINE_MAJOR_TYPE Type
);
```



## <a name="parameters"></a><span data-ttu-id="8dac8-108">參數</span><span class="sxs-lookup"><span data-stu-id="8dac8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8dac8-109">*ppVirtualTrack* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="8dac8-109">*ppVirtualTrack* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8dac8-110">接收虛擬軌 [**IAMTimelineObj**](iamtimelineobj.md) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="8dac8-110">Receives a pointer to the virtual track's [**IAMTimelineObj**](iamtimelineobj.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="8dac8-111">*WhichLayer*</span><span class="sxs-lookup"><span data-stu-id="8dac8-111">*WhichLayer*</span></span> 
</dt> <dd>

<span data-ttu-id="8dac8-112">指定要取出的虛擬追蹤（從零編制索引）。</span><span class="sxs-lookup"><span data-stu-id="8dac8-112">Specifies which virtual track to retrieve, indexed from zero.</span></span>

</dd> <dt>

<span data-ttu-id="8dac8-113">*型別*</span><span class="sxs-lookup"><span data-stu-id="8dac8-113">*Type*</span></span> 
</dt> <dd>

<span data-ttu-id="8dac8-114">[**時間軸 \_ 主要 \_ 類型**](timeline-major-type.md)列舉類型的成員，指定是否要在搜尋中包含曲目。</span><span class="sxs-lookup"><span data-stu-id="8dac8-114">Member of the [**TIMELINE\_MAJOR\_TYPE**](timeline-major-type.md) enumerated type that specifies whether to include tracks in the search.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8dac8-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="8dac8-115">Return value</span></span>

<span data-ttu-id="8dac8-116">傳回下列其中一個 **HRESULT** 值：</span><span class="sxs-lookup"><span data-stu-id="8dac8-116">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="8dac8-117">傳回碼</span><span class="sxs-lookup"><span data-stu-id="8dac8-117">Return code</span></span>                                                                                  | <span data-ttu-id="8dac8-118">Description</span><span class="sxs-lookup"><span data-stu-id="8dac8-118">Description</span></span>                                 |
|----------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <span data-ttu-id="8dac8-119"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="8dac8-119"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="8dac8-120">成功。</span><span class="sxs-lookup"><span data-stu-id="8dac8-120">Success.</span></span><br/>                         |
| <dl> <span data-ttu-id="8dac8-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="8dac8-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="8dac8-122">沒有指定之類型的物件。</span><span class="sxs-lookup"><span data-stu-id="8dac8-122">No object of the specified type.</span></span><br/> |
| <dl> <span data-ttu-id="8dac8-123"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="8dac8-123"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="8dac8-124">**Null** 指標引數。</span><span class="sxs-lookup"><span data-stu-id="8dac8-124">**NULL** pointer argument.</span></span><br/>       |



 

## <a name="remarks"></a><span data-ttu-id="8dac8-125">備註</span><span class="sxs-lookup"><span data-stu-id="8dac8-125">Remarks</span></span>

<span data-ttu-id="8dac8-126">一般來說，應用程式不需要呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="8dac8-126">Typically, an application will not need to call this method.</span></span>

<span data-ttu-id="8dac8-127">如果 *類型* 參數是時間軸 \_ 主要 \_ 類型 \_ 追蹤，深度優先的順序就會包含追蹤。</span><span class="sxs-lookup"><span data-stu-id="8dac8-127">If the *Type* parameter is TIMELINE\_MAJOR\_TYPE\_TRACK, the depth-first ordering includes tracks.</span></span> <span data-ttu-id="8dac8-128">如果沒有，則只包含組合和群組。</span><span class="sxs-lookup"><span data-stu-id="8dac8-128">If not, it includes only compositions and groups.</span></span> <span data-ttu-id="8dac8-129">物件本身會包含在順序中。</span><span class="sxs-lookup"><span data-stu-id="8dac8-129">The object itself is included in the ordering.</span></span>

<span data-ttu-id="8dac8-130">例如，在下列安排中，從組合 A 開始，順序會是 B、C、F、D、E、A。</span><span class="sxs-lookup"><span data-stu-id="8dac8-130">For example, in the following arrangement, starting from Composition A, the ordering would be B, C, F, D, E, A.</span></span>

![getrecursivelayeroftype](images/composition.png)

<span data-ttu-id="8dac8-132">如果方法成功，則傳回的 **IAMTimelineObj** 介面具有未處理的參考計數。</span><span class="sxs-lookup"><span data-stu-id="8dac8-132">If the method succeeds, the **IAMTimelineObj** interface that it returns has an outstanding reference count.</span></span> <span data-ttu-id="8dac8-133">使用完畢後，請務必釋放介面。</span><span class="sxs-lookup"><span data-stu-id="8dac8-133">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="8dac8-134">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="8dac8-134">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="8dac8-135">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="8dac8-135">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="8dac8-136">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="8dac8-136">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8dac8-137">規格需求</span><span class="sxs-lookup"><span data-stu-id="8dac8-137">Requirements</span></span>



| <span data-ttu-id="8dac8-138">需求</span><span class="sxs-lookup"><span data-stu-id="8dac8-138">Requirement</span></span> | <span data-ttu-id="8dac8-139">值</span><span class="sxs-lookup"><span data-stu-id="8dac8-139">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8dac8-140">標頭</span><span class="sxs-lookup"><span data-stu-id="8dac8-140">Header</span></span><br/>  | <dl> <span data-ttu-id="8dac8-141"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="8dac8-141"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="8dac8-142">程式庫</span><span class="sxs-lookup"><span data-stu-id="8dac8-142">Library</span></span><br/> | <dl> <span data-ttu-id="8dac8-143"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="8dac8-143"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8dac8-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8dac8-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8dac8-145">**IAMTimelineComp 介面**</span><span class="sxs-lookup"><span data-stu-id="8dac8-145">**IAMTimelineComp Interface**</span></span>](iamtimelinecomp.md)
</dt> <dt>

[<span data-ttu-id="8dac8-146">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="8dac8-146">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




