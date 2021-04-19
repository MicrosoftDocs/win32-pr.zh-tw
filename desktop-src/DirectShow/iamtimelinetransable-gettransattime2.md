---
description: GetTransAtTime2 方法會根據指定的界限條件，抓取最接近指定時間的轉換。 這個方法相當於 IAMTimelineTransable：： GetTransAtTime，但會接受 REFTIME 參數。
ms.assetid: b51b53ec-4b56-4900-98b5-427d752354b0
title: 'IAMTimelineTransable：： GetTransAtTime2 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTransable.GetTransAtTime2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 6b3de498791a634ea651da46ba9c95557ca12b87
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998641"
---
# <a name="iamtimelinetransablegettransattime2-method"></a><span data-ttu-id="1a6bc-104">IAMTimelineTransable：： GetTransAtTime2 方法</span><span class="sxs-lookup"><span data-stu-id="1a6bc-104">IAMTimelineTransable::GetTransAtTime2 method</span></span>

> [!Note]  
> <span data-ttu-id="1a6bc-105">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="1a6bc-105">\[Deprecated.</span></span> <span data-ttu-id="1a6bc-106">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="1a6bc-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="1a6bc-107">`GetTransAtTime2`方法會根據指定的界限條件，抓取最接近指定時間的轉換。</span><span class="sxs-lookup"><span data-stu-id="1a6bc-107">The `GetTransAtTime2` method retrieves the transition nearest to the specified time, according to the specified boundary conditions.</span></span> <span data-ttu-id="1a6bc-108">這個方法相當於 [**IAMTimelineTransable：： GetTransAtTime**](iamtimelinetransable-gettransattime.md)，但會接受 [**REFTIME**](reftime.md) 參數。</span><span class="sxs-lookup"><span data-stu-id="1a6bc-108">This method is equivalent to [**IAMTimelineTransable::GetTransAtTime**](iamtimelinetransable-gettransattime.md), but takes a [**REFTIME**](reftime.md) parameter.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a6bc-109">語法</span><span class="sxs-lookup"><span data-stu-id="1a6bc-109">Syntax</span></span>


```C++
HRESULT GetTransAtTime2(
  [out] IAMTimelineObj **ppObj,
        REFTIME        Time,
        long           SearchDirection
);
```



## <a name="parameters"></a><span data-ttu-id="1a6bc-110">參數</span><span class="sxs-lookup"><span data-stu-id="1a6bc-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a6bc-111">*ppObj* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="1a6bc-111">*ppObj* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1a6bc-112">接收轉換 [**IAMTimelineObj**](iamtimelineobj.md) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="1a6bc-112">Receives a pointer to the transition's [**IAMTimelineObj**](iamtimelineobj.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="1a6bc-113">*Time*</span><span class="sxs-lookup"><span data-stu-id="1a6bc-113">*Time*</span></span> 
</dt> <dd>

<span data-ttu-id="1a6bc-114">開始搜尋的時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="1a6bc-114">Time from which to begin the search, in seconds.</span></span>

</dd> <dt>

<span data-ttu-id="1a6bc-115">*SearchDirection*</span><span class="sxs-lookup"><span data-stu-id="1a6bc-115">*SearchDirection*</span></span> 
</dt> <dd>

<span data-ttu-id="1a6bc-116">[**DEXTERF \_ TRACK \_ 搜尋 \_ 旗標**](dexterf-track-search-flags.md)列舉類型的成員，可指定搜尋的界限條件。</span><span class="sxs-lookup"><span data-stu-id="1a6bc-116">Member of the [**DEXTERF\_TRACK\_SEARCH\_FLAGS**](dexterf-track-search-flags.md) enumerated type that specifies the boundary conditions for the search.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a6bc-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="1a6bc-117">Return value</span></span>

<span data-ttu-id="1a6bc-118">傳回下列其中一個 **HRESULT** 值：</span><span class="sxs-lookup"><span data-stu-id="1a6bc-118">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="1a6bc-119">傳回碼</span><span class="sxs-lookup"><span data-stu-id="1a6bc-119">Return code</span></span>                                                                                  | <span data-ttu-id="1a6bc-120">Description</span><span class="sxs-lookup"><span data-stu-id="1a6bc-120">Description</span></span>                           |
|----------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="1a6bc-121"><dt>**S \_ FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="1a6bc-121"><dt>**S\_FALSE**</dt></span></span> </dl>      | <span data-ttu-id="1a6bc-122">找不到轉換。</span><span class="sxs-lookup"><span data-stu-id="1a6bc-122">No transition was found.</span></span><br/>   |
| <dl> <span data-ttu-id="1a6bc-123"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="1a6bc-123"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="1a6bc-124">找到轉換。</span><span class="sxs-lookup"><span data-stu-id="1a6bc-124">Transition was found.</span></span><br/>      |
| <dl> <span data-ttu-id="1a6bc-125"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="1a6bc-125"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="1a6bc-126">無效引數。</span><span class="sxs-lookup"><span data-stu-id="1a6bc-126">Invalid argument.</span></span><br/>          |
| <dl> <span data-ttu-id="1a6bc-127"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="1a6bc-127"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="1a6bc-128">**Null** 指標引數。</span><span class="sxs-lookup"><span data-stu-id="1a6bc-128">**NULL** pointer argument.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="1a6bc-129">備註</span><span class="sxs-lookup"><span data-stu-id="1a6bc-129">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="1a6bc-130">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="1a6bc-130">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="1a6bc-131">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="1a6bc-131">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="1a6bc-132">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="1a6bc-132">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="1a6bc-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="1a6bc-133">Requirements</span></span>



| <span data-ttu-id="1a6bc-134">需求</span><span class="sxs-lookup"><span data-stu-id="1a6bc-134">Requirement</span></span> | <span data-ttu-id="1a6bc-135">值</span><span class="sxs-lookup"><span data-stu-id="1a6bc-135">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1a6bc-136">標頭</span><span class="sxs-lookup"><span data-stu-id="1a6bc-136">Header</span></span><br/>  | <dl> <span data-ttu-id="1a6bc-137"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="1a6bc-137"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="1a6bc-138">程式庫</span><span class="sxs-lookup"><span data-stu-id="1a6bc-138">Library</span></span><br/> | <dl> <span data-ttu-id="1a6bc-139"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="1a6bc-139"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a6bc-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1a6bc-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a6bc-141">**IAMTimelineTransable 介面**</span><span class="sxs-lookup"><span data-stu-id="1a6bc-141">**IAMTimelineTransable Interface**</span></span>](iamtimelinetransable.md)
</dt> <dt>

[<span data-ttu-id="1a6bc-142">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="1a6bc-142">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




