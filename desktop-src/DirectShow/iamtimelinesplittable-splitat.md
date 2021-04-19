---
description: SplitAt 方法會在指定的時間分割物件。
ms.assetid: 37870c6f-a35e-4c08-8188-1c4c7b25ff88
title: 'IAMTimelineSplittable：： SplitAt 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSplittable.SplitAt
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a44aabf3386a4e906bd4f3e149c416642ba6c4fc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994132"
---
# <a name="iamtimelinesplittablesplitat-method"></a><span data-ttu-id="3f726-103">IAMTimelineSplittable：： SplitAt 方法</span><span class="sxs-lookup"><span data-stu-id="3f726-103">IAMTimelineSplittable::SplitAt method</span></span>

> [!Note]  
> <span data-ttu-id="3f726-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="3f726-104">\[Deprecated.</span></span> <span data-ttu-id="3f726-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="3f726-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="3f726-106">`SplitAt`方法會在指定的時間分割物件。</span><span class="sxs-lookup"><span data-stu-id="3f726-106">The `SplitAt` method splits the object at the specified time.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f726-107">語法</span><span class="sxs-lookup"><span data-stu-id="3f726-107">Syntax</span></span>


```C++
HRESULT SplitAt(
   REFERENCE_TIME Time
);
```



## <a name="parameters"></a><span data-ttu-id="3f726-108">參數</span><span class="sxs-lookup"><span data-stu-id="3f726-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f726-109">*Time*</span><span class="sxs-lookup"><span data-stu-id="3f726-109">*Time*</span></span> 
</dt> <dd>

<span data-ttu-id="3f726-110">分割物件的時間（相對於時間軸的開始時間，以 100-毫微秒單位表示）。</span><span class="sxs-lookup"><span data-stu-id="3f726-110">Time at which to split the object, relative to the start of the timeline, in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3f726-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="3f726-111">Return value</span></span>

<span data-ttu-id="3f726-112">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="3f726-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="3f726-113">可能的值如下：</span><span class="sxs-lookup"><span data-stu-id="3f726-113">Possible values include the following:</span></span>



| <span data-ttu-id="3f726-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="3f726-114">Return code</span></span>                                                                                   | <span data-ttu-id="3f726-115">Description</span><span class="sxs-lookup"><span data-stu-id="3f726-115">Description</span></span>                                        |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <span data-ttu-id="3f726-116"><dt>**S \_ FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="3f726-116"><dt>**S\_FALSE**</dt></span></span> </dl>       | <span data-ttu-id="3f726-117">沒有要分割的專案。</span><span class="sxs-lookup"><span data-stu-id="3f726-117">Nothing to split.</span></span><br/>                       |
| <dl> <span data-ttu-id="3f726-118"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="3f726-118"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="3f726-119">成功。</span><span class="sxs-lookup"><span data-stu-id="3f726-119">Success.</span></span><br/>                                |
| <dl> <span data-ttu-id="3f726-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="3f726-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="3f726-121">此物件目前不存在。</span><span class="sxs-lookup"><span data-stu-id="3f726-121">The object does not exist at this time.</span></span><br/> |
| <dl> <span data-ttu-id="3f726-122"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="3f726-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="3f726-123">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="3f726-123">Insufficient memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="3f726-124">備註</span><span class="sxs-lookup"><span data-stu-id="3f726-124">Remarks</span></span>

<span data-ttu-id="3f726-125">如果您分割來源、效果或轉換，這個方法會建立相同型別的第二個物件。</span><span class="sxs-lookup"><span data-stu-id="3f726-125">If you split a source, effect, or transition, this method creates a second object of the same type.</span></span> <span data-ttu-id="3f726-126">原始物件會在指定的分割時間被截斷，而新的物件會取代截斷的部分。</span><span class="sxs-lookup"><span data-stu-id="3f726-126">The original object is truncated at the specified split time, and the new object replaces the truncated portion.</span></span> <span data-ttu-id="3f726-127">新的物件會繼承所有相同的屬性。</span><span class="sxs-lookup"><span data-stu-id="3f726-127">The new object inherits all of the same properties.</span></span> <span data-ttu-id="3f726-128">在來源物件中，此方法也會分割落在分割時間的任何效果。</span><span class="sxs-lookup"><span data-stu-id="3f726-128">In a source object, the method also splits any effects that fall on the split time.</span></span>

<span data-ttu-id="3f726-129">在追蹤上呼叫這個方法，會將追蹤中包含的所有來源、效果和轉換分割為指定的分割時間。</span><span class="sxs-lookup"><span data-stu-id="3f726-129">Calling this method on a track splits all the sources, effects, and transitions that are contained in the track at the specified split time.</span></span> <span data-ttu-id="3f726-130">它不會建立第二個曲目。 (一段時間從零開始，並延伸到無限大。 ) </span><span class="sxs-lookup"><span data-stu-id="3f726-130">It does not create a second track. (A track begins at time zero and extends to infinity.)</span></span>

<span data-ttu-id="3f726-131">針對追蹤，如果分割時間晚于追蹤中的所有專案，則此方法會傳回 \_ FALSE。</span><span class="sxs-lookup"><span data-stu-id="3f726-131">For a track, if the split time is later than everything in the track, the method returns S\_FALSE.</span></span> <span data-ttu-id="3f726-132">針對任何其他物件，如果分割時間不是落在物件內的任何位置，則方法會傳回 E \_ INVALIDARG。</span><span class="sxs-lookup"><span data-stu-id="3f726-132">For any other object, if the split time does not fall anywhere within the object, the method returns E\_INVALIDARG.</span></span>

> [!Note]  
> <span data-ttu-id="3f726-133">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="3f726-133">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="3f726-134">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="3f726-134">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="3f726-135">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="3f726-135">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3f726-136">規格需求</span><span class="sxs-lookup"><span data-stu-id="3f726-136">Requirements</span></span>



| <span data-ttu-id="3f726-137">需求</span><span class="sxs-lookup"><span data-stu-id="3f726-137">Requirement</span></span> | <span data-ttu-id="3f726-138">值</span><span class="sxs-lookup"><span data-stu-id="3f726-138">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3f726-139">標頭</span><span class="sxs-lookup"><span data-stu-id="3f726-139">Header</span></span><br/>  | <dl> <span data-ttu-id="3f726-140"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="3f726-140"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="3f726-141">程式庫</span><span class="sxs-lookup"><span data-stu-id="3f726-141">Library</span></span><br/> | <dl> <span data-ttu-id="3f726-142"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="3f726-142"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3f726-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3f726-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f726-144">**IAMTimelineSplittable 介面**</span><span class="sxs-lookup"><span data-stu-id="3f726-144">**IAMTimelineSplittable Interface**</span></span>](iamtimelinesplittable.md)
</dt> <dt>

[<span data-ttu-id="3f726-145">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="3f726-145">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




