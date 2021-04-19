---
description: GetTransAtTime 方法會根據指定的界限條件，抓取最接近指定時間的轉換。
ms.assetid: 33b3686b-5a9d-4eb2-bd40-4d6f569e7d89
title: 'IAMTimelineTransable：： GetTransAtTime 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTransable.GetTransAtTime
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 77ca7b1c9a5517d849b38ba1ba22216583d7af87
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001202"
---
# <a name="iamtimelinetransablegettransattime-method"></a><span data-ttu-id="1e0d5-103">IAMTimelineTransable：： GetTransAtTime 方法</span><span class="sxs-lookup"><span data-stu-id="1e0d5-103">IAMTimelineTransable::GetTransAtTime method</span></span>

> [!Note]  
> <span data-ttu-id="1e0d5-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="1e0d5-104">\[Deprecated.</span></span> <span data-ttu-id="1e0d5-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="1e0d5-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="1e0d5-106">`GetTransAtTime`方法會根據指定的界限條件，抓取最接近指定時間的轉換。</span><span class="sxs-lookup"><span data-stu-id="1e0d5-106">The `GetTransAtTime` method retrieves the transition nearest to the specified time, according to the specified boundary conditions.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e0d5-107">語法</span><span class="sxs-lookup"><span data-stu-id="1e0d5-107">Syntax</span></span>


```C++
HRESULT GetTransAtTime(
  [out] IAMTimelineObj **ppObj,
        REFERENCE_TIME Time,
        long           SearchDirection
);
```



## <a name="parameters"></a><span data-ttu-id="1e0d5-108">參數</span><span class="sxs-lookup"><span data-stu-id="1e0d5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e0d5-109">*ppObj* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="1e0d5-109">*ppObj* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1e0d5-110">接收轉換 [**IAMTimelineObj**](iamtimelineobj.md) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="1e0d5-110">Receives a pointer to the transition's [**IAMTimelineObj**](iamtimelineobj.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="1e0d5-111">*Time*</span><span class="sxs-lookup"><span data-stu-id="1e0d5-111">*Time*</span></span> 
</dt> <dd>

<span data-ttu-id="1e0d5-112">開始搜尋的時間，以 100-毫微秒單位表示。</span><span class="sxs-lookup"><span data-stu-id="1e0d5-112">Time from which to begin the search, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="1e0d5-113">*SearchDirection*</span><span class="sxs-lookup"><span data-stu-id="1e0d5-113">*SearchDirection*</span></span> 
</dt> <dd>

<span data-ttu-id="1e0d5-114">[**DEXTERF \_ TRACK \_ 搜尋 \_ 旗標**](dexterf-track-search-flags.md)列舉類型的成員，可指定搜尋的界限條件。</span><span class="sxs-lookup"><span data-stu-id="1e0d5-114">Member of the [**DEXTERF\_TRACK\_SEARCH\_FLAGS**](dexterf-track-search-flags.md) enumerated type that specifies the boundary conditions for the search.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e0d5-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="1e0d5-115">Return value</span></span>

<span data-ttu-id="1e0d5-116">傳回下列其中一個 **HRESULT** 值：</span><span class="sxs-lookup"><span data-stu-id="1e0d5-116">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="1e0d5-117">傳回碼</span><span class="sxs-lookup"><span data-stu-id="1e0d5-117">Return code</span></span>                                                                                  | <span data-ttu-id="1e0d5-118">Description</span><span class="sxs-lookup"><span data-stu-id="1e0d5-118">Description</span></span>                           |
|----------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="1e0d5-119"><dt>**S \_ FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="1e0d5-119"><dt>**S\_FALSE**</dt></span></span> </dl>      | <span data-ttu-id="1e0d5-120">找不到轉換。</span><span class="sxs-lookup"><span data-stu-id="1e0d5-120">No transition was found.</span></span><br/>   |
| <dl> <span data-ttu-id="1e0d5-121"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="1e0d5-121"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="1e0d5-122">找到轉換。</span><span class="sxs-lookup"><span data-stu-id="1e0d5-122">Transition was found.</span></span><br/>      |
| <dl> <span data-ttu-id="1e0d5-123"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="1e0d5-123"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="1e0d5-124">無效引數。</span><span class="sxs-lookup"><span data-stu-id="1e0d5-124">Invalid argument.</span></span><br/>          |
| <dl> <span data-ttu-id="1e0d5-125"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="1e0d5-125"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="1e0d5-126">**Null** 指標引數。</span><span class="sxs-lookup"><span data-stu-id="1e0d5-126">**NULL** pointer argument.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="1e0d5-127">備註</span><span class="sxs-lookup"><span data-stu-id="1e0d5-127">Remarks</span></span>

<span data-ttu-id="1e0d5-128">如果方法傳回 S \_ OK，則傳回的 **IAMTimelineObj** 介面具有未處理的參考計數。</span><span class="sxs-lookup"><span data-stu-id="1e0d5-128">If the method returns S\_OK, the **IAMTimelineObj** interface that it returns has an outstanding reference count.</span></span> <span data-ttu-id="1e0d5-129">使用完畢後，請務必釋放介面。</span><span class="sxs-lookup"><span data-stu-id="1e0d5-129">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="1e0d5-130">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="1e0d5-130">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="1e0d5-131">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="1e0d5-131">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="1e0d5-132">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="1e0d5-132">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="1e0d5-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="1e0d5-133">Requirements</span></span>



| <span data-ttu-id="1e0d5-134">需求</span><span class="sxs-lookup"><span data-stu-id="1e0d5-134">Requirement</span></span> | <span data-ttu-id="1e0d5-135">值</span><span class="sxs-lookup"><span data-stu-id="1e0d5-135">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1e0d5-136">標頭</span><span class="sxs-lookup"><span data-stu-id="1e0d5-136">Header</span></span><br/>  | <dl> <span data-ttu-id="1e0d5-137"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="1e0d5-137"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="1e0d5-138">程式庫</span><span class="sxs-lookup"><span data-stu-id="1e0d5-138">Library</span></span><br/> | <dl> <span data-ttu-id="1e0d5-139"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="1e0d5-139"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e0d5-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1e0d5-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e0d5-141">**IAMTimelineTransable 介面**</span><span class="sxs-lookup"><span data-stu-id="1e0d5-141">**IAMTimelineTransable Interface**</span></span>](iamtimelinetransable.md)
</dt> <dt>

[<span data-ttu-id="1e0d5-142">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="1e0d5-142">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




