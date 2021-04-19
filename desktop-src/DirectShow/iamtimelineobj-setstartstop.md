---
description: SetStartStop 方法會設定物件的開始和停止時間，相對於物件的父系。
ms.assetid: 6275a36b-f963-4916-bf60-ea68008ad153
title: 'IAMTimelineObj：： SetStartStop 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetStartStop
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e7839417a0406fc2702fb0fbd593edc92fa80437
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987826"
---
# <a name="iamtimelineobjsetstartstop-method"></a><span data-ttu-id="d42d6-103">IAMTimelineObj：： SetStartStop 方法</span><span class="sxs-lookup"><span data-stu-id="d42d6-103">IAMTimelineObj::SetStartStop method</span></span>

> [!Note]  
> <span data-ttu-id="d42d6-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="d42d6-104">\[Deprecated.</span></span> <span data-ttu-id="d42d6-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="d42d6-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="d42d6-106">`SetStartStop`方法會設定物件的開始和停止時間，相對於物件的父系。</span><span class="sxs-lookup"><span data-stu-id="d42d6-106">The `SetStartStop` method sets the object's start and stop times, relative to the object's parent.</span></span>

## <a name="syntax"></a><span data-ttu-id="d42d6-107">語法</span><span class="sxs-lookup"><span data-stu-id="d42d6-107">Syntax</span></span>


```C++
HRESULT SetStartStop(
   REFERENCE_TIME Start,
   REFERENCE_TIME Stop
);
```



## <a name="parameters"></a><span data-ttu-id="d42d6-108">參數</span><span class="sxs-lookup"><span data-stu-id="d42d6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d42d6-109">*開始*</span><span class="sxs-lookup"><span data-stu-id="d42d6-109">*Start*</span></span> 
</dt> <dd>

<span data-ttu-id="d42d6-110">新的開始時間（以 100-毫微秒單位），或-1 會保留現有的開始時間。</span><span class="sxs-lookup"><span data-stu-id="d42d6-110">New start time, in 100-nanosecond units, or –1 to keep the existing start time.</span></span>

</dd> <dt>

<span data-ttu-id="d42d6-111">*停止*</span><span class="sxs-lookup"><span data-stu-id="d42d6-111">*Stop*</span></span> 
</dt> <dd>

<span data-ttu-id="d42d6-112">新的停止時間（100-毫微秒單位）或-1，以保留現有的停止時間。</span><span class="sxs-lookup"><span data-stu-id="d42d6-112">New stop time, in 100-nanosecond units, or –1 to keep the existing stop time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d42d6-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="d42d6-113">Return value</span></span>

<span data-ttu-id="d42d6-114">傳回下列其中一個 **HRESULT** 值：</span><span class="sxs-lookup"><span data-stu-id="d42d6-114">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="d42d6-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="d42d6-115">Return code</span></span>                                                                                  | <span data-ttu-id="d42d6-116">Description</span><span class="sxs-lookup"><span data-stu-id="d42d6-116">Description</span></span>                  |
|----------------------------------------------------------------------------------------------|------------------------------|
| <dl> <span data-ttu-id="d42d6-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="d42d6-117"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="d42d6-118">成功。</span><span class="sxs-lookup"><span data-stu-id="d42d6-118">Success.</span></span><br/>          |
| <dl> <span data-ttu-id="d42d6-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="d42d6-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="d42d6-120">無效引數。</span><span class="sxs-lookup"><span data-stu-id="d42d6-120">Invalid argument.</span></span><br/> |
| <dl> <span data-ttu-id="d42d6-121"><dt>**E \_ >NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="d42d6-121"><dt>**E\_NOTIMPL**</dt></span></span> </dl>    | <span data-ttu-id="d42d6-122">未實作。</span><span class="sxs-lookup"><span data-stu-id="d42d6-122">Not implemented.</span></span><br/>  |



 

## <a name="remarks"></a><span data-ttu-id="d42d6-123">備註</span><span class="sxs-lookup"><span data-stu-id="d42d6-123">Remarks</span></span>

<span data-ttu-id="d42d6-124">追蹤、組合和群組都不會執行此方法。</span><span class="sxs-lookup"><span data-stu-id="d42d6-124">Tracks, compositions, and groups do not implement this method.</span></span> <span data-ttu-id="d42d6-125">針對這些物件，開始時間一律為零，而停止時間是其所包含物件的最大停止時間。</span><span class="sxs-lookup"><span data-stu-id="d42d6-125">For these objects, the start time is always zero, and the stop time is the maximum stop time of the objects they contain.</span></span>

<span data-ttu-id="d42d6-126">請勿在相同的播放軌內的來源物件上設定重迭的時間。這樣做可能會導致未定義的行為。</span><span class="sxs-lookup"><span data-stu-id="d42d6-126">Do not set overlapping times on source objects within the same track. Doing so can cause undefined behaviors.</span></span>

<span data-ttu-id="d42d6-127">針對來源物件，開始和停止時間與媒體開始和媒體停止時間無關。</span><span class="sxs-lookup"><span data-stu-id="d42d6-127">For source objects, the start and stop times are independent of the media start and media stop times.</span></span> <span data-ttu-id="d42d6-128">變更一對值並不會變更另一個值。</span><span class="sxs-lookup"><span data-stu-id="d42d6-128">Changing one pair of values does not change the other.</span></span> <span data-ttu-id="d42d6-129">若要設定媒體的開始和停止時間，請呼叫 [**IAMTimelineSrc：： SetMediaTimes**](iamtimelinesrc-setmediatimes.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="d42d6-129">To set the media start and stop times, call the [**IAMTimelineSrc::SetMediaTimes**](iamtimelinesrc-setmediatimes.md) method.</span></span> <span data-ttu-id="d42d6-130">如需詳細資訊，請參閱 [DirectShow 編輯服務中的時間](time-in-directshow-editing-services.md)。</span><span class="sxs-lookup"><span data-stu-id="d42d6-130">For more information, see [Time in DirectShow Editing Services](time-in-directshow-editing-services.md).</span></span>

<span data-ttu-id="d42d6-131">若要取得幀精確的剪下和轉換，請將 *Start* 和 *Stop* 參數設定為框架界限。</span><span class="sxs-lookup"><span data-stu-id="d42d6-131">To get frame-accurate cuts and transitions, set the *Start* and *Stop* parameters to frame boundaries.</span></span> <span data-ttu-id="d42d6-132">您可以使用 [**IAMTimelineObj：： FixTimes**](iamtimelineobj-fixtimes.md) 方法，將時間值轉換為最接近的框架界限，或使用下列函式，從畫面格編號轉換為參考時間：</span><span class="sxs-lookup"><span data-stu-id="d42d6-132">You can use the [**IAMTimelineObj::FixTimes**](iamtimelineobj-fixtimes.md) method to convert a time value into the nearest frame boundary, or use the following function to convert from frame number to reference time:</span></span>


```C++
REFERENCE_TIME inline FrameNumToTime(LONGLONG frame, double fps)
{
    double dt = (frame * 10000000 / fps);
    if (frame >= 0) 
    {
        dt += 0.5;    }
    else
    {
        dt -= 0.5;
    }
    return (REFERENCE_TIME)dt;
}
```



> [!Note]  
> <span data-ttu-id="d42d6-133">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="d42d6-133">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="d42d6-134">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="d42d6-134">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="d42d6-135">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="d42d6-135">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d42d6-136">規格需求</span><span class="sxs-lookup"><span data-stu-id="d42d6-136">Requirements</span></span>



| <span data-ttu-id="d42d6-137">需求</span><span class="sxs-lookup"><span data-stu-id="d42d6-137">Requirement</span></span> | <span data-ttu-id="d42d6-138">值</span><span class="sxs-lookup"><span data-stu-id="d42d6-138">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d42d6-139">標頭</span><span class="sxs-lookup"><span data-stu-id="d42d6-139">Header</span></span><br/>  | <dl> <span data-ttu-id="d42d6-140"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="d42d6-140"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="d42d6-141">程式庫</span><span class="sxs-lookup"><span data-stu-id="d42d6-141">Library</span></span><br/> | <dl> <span data-ttu-id="d42d6-142"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="d42d6-142"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d42d6-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d42d6-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d42d6-144">**IAMTimelineObj 介面**</span><span class="sxs-lookup"><span data-stu-id="d42d6-144">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="d42d6-145">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="d42d6-145">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




