---
description: GetSrcAtTime2 方法會根據指定的界限條件，抓取最接近指定時間的來源物件。 這個方法相當於 IAMTimelineTrack：： GetSrcAtTime，但會接受 REFTIME 值。
ms.assetid: 11f6545b-478b-4ffd-8344-2bf8585db2a5
title: 'IAMTimelineTrack：： GetSrcAtTime2 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.GetSrcAtTime2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 7140644f64c66b204d6a50cb8e88cb5beca41dae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106997639"
---
# <a name="iamtimelinetrackgetsrcattime2-method"></a><span data-ttu-id="ee8bf-104">IAMTimelineTrack：： GetSrcAtTime2 方法</span><span class="sxs-lookup"><span data-stu-id="ee8bf-104">IAMTimelineTrack::GetSrcAtTime2 method</span></span>

> [!Note]  
> <span data-ttu-id="ee8bf-105">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="ee8bf-105">\[Deprecated.</span></span> <span data-ttu-id="ee8bf-106">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="ee8bf-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="ee8bf-107">`GetSrcAtTime2`方法會根據指定的界限條件，抓取最接近指定時間的來源物件。</span><span class="sxs-lookup"><span data-stu-id="ee8bf-107">The `GetSrcAtTime2` method retrieves the source object nearest to the specified time, according to the specified boundary conditions.</span></span> <span data-ttu-id="ee8bf-108">這個方法相當於 [**IAMTimelineTrack：： GetSrcAtTime**](iamtimelinetrack-getsrcattime.md)，但會接受 [**REFTIME**](reftime.md) 值。</span><span class="sxs-lookup"><span data-stu-id="ee8bf-108">This method is equivalent to [**IAMTimelineTrack::GetSrcAtTime**](iamtimelinetrack-getsrcattime.md), but takes a [**REFTIME**](reftime.md) value.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee8bf-109">語法</span><span class="sxs-lookup"><span data-stu-id="ee8bf-109">Syntax</span></span>


```C++
HRESULT GetSrcAtTime2(
  [out] IAMTimelineObj **ppSrc,
        REFTIME        Time,
        long           SearchDirection
);
```



## <a name="parameters"></a><span data-ttu-id="ee8bf-110">參數</span><span class="sxs-lookup"><span data-stu-id="ee8bf-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee8bf-111">*ppSrc* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="ee8bf-111">*ppSrc* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ee8bf-112">接收來源物件之 [**IAMTimelineObj**](iamtimelineobj.md) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="ee8bf-112">Receives a pointer to the [**IAMTimelineObj**](iamtimelineobj.md) interface of the source object.</span></span>

</dd> <dt>

<span data-ttu-id="ee8bf-113">*Time*</span><span class="sxs-lookup"><span data-stu-id="ee8bf-113">*Time*</span></span> 
</dt> <dd>

<span data-ttu-id="ee8bf-114">搜尋的開始時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="ee8bf-114">Start time for the search, in seconds.</span></span>

</dd> <dt>

<span data-ttu-id="ee8bf-115">*SearchDirection*</span><span class="sxs-lookup"><span data-stu-id="ee8bf-115">*SearchDirection*</span></span> 
</dt> <dd>

<span data-ttu-id="ee8bf-116">[**DEXTERF \_ TRACK \_ 搜尋 \_ 旗標**](dexterf-track-search-flags.md)列舉類型的成員，可指定搜尋的界限條件。</span><span class="sxs-lookup"><span data-stu-id="ee8bf-116">Member of the [**DEXTERF\_TRACK\_SEARCH\_FLAGS**](dexterf-track-search-flags.md) enumerated type that specifies the boundary conditions for the search.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee8bf-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="ee8bf-117">Return value</span></span>

<span data-ttu-id="ee8bf-118">傳回下列其中一個 **HRESULT** 值：</span><span class="sxs-lookup"><span data-stu-id="ee8bf-118">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="ee8bf-119">傳回碼</span><span class="sxs-lookup"><span data-stu-id="ee8bf-119">Return code</span></span>                                                                                  | <span data-ttu-id="ee8bf-120">Description</span><span class="sxs-lookup"><span data-stu-id="ee8bf-120">Description</span></span>                                |
|----------------------------------------------------------------------------------------------|--------------------------------------------|
| <dl> <span data-ttu-id="ee8bf-121"><dt>**S \_ FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="ee8bf-121"><dt>**S\_FALSE**</dt></span></span> </dl>      | <span data-ttu-id="ee8bf-122">找不到來源物件。</span><span class="sxs-lookup"><span data-stu-id="ee8bf-122">Did not locate a source object.</span></span><br/> |
| <dl> <span data-ttu-id="ee8bf-123"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="ee8bf-123"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="ee8bf-124">找到來源物件。</span><span class="sxs-lookup"><span data-stu-id="ee8bf-124">Located a source object.</span></span><br/>        |
| <dl> <span data-ttu-id="ee8bf-125"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="ee8bf-125"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="ee8bf-126">無效引數。</span><span class="sxs-lookup"><span data-stu-id="ee8bf-126">Invalid argument.</span></span><br/>               |
| <dl> <span data-ttu-id="ee8bf-127"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="ee8bf-127"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="ee8bf-128">**Null** 指標引數。</span><span class="sxs-lookup"><span data-stu-id="ee8bf-128">**NULL** pointer argument.</span></span><br/>      |



 

## <a name="remarks"></a><span data-ttu-id="ee8bf-129">備註</span><span class="sxs-lookup"><span data-stu-id="ee8bf-129">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="ee8bf-130">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="ee8bf-130">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="ee8bf-131">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="ee8bf-131">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="ee8bf-132">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="ee8bf-132">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ee8bf-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="ee8bf-133">Requirements</span></span>



| <span data-ttu-id="ee8bf-134">需求</span><span class="sxs-lookup"><span data-stu-id="ee8bf-134">Requirement</span></span> | <span data-ttu-id="ee8bf-135">值</span><span class="sxs-lookup"><span data-stu-id="ee8bf-135">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ee8bf-136">標頭</span><span class="sxs-lookup"><span data-stu-id="ee8bf-136">Header</span></span><br/>  | <dl> <span data-ttu-id="ee8bf-137"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="ee8bf-137"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="ee8bf-138">程式庫</span><span class="sxs-lookup"><span data-stu-id="ee8bf-138">Library</span></span><br/> | <dl> <span data-ttu-id="ee8bf-139"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="ee8bf-139"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee8bf-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ee8bf-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee8bf-141">**IAMTimelineTrack 介面**</span><span class="sxs-lookup"><span data-stu-id="ee8bf-141">**IAMTimelineTrack Interface**</span></span>](iamtimelinetrack.md)
</dt> <dt>

[<span data-ttu-id="ee8bf-142">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="ee8bf-142">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




