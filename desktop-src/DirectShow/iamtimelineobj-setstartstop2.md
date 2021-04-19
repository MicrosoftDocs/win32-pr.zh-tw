---
description: SetStartStop2 方法會設定物件的開始和停止時間，相對於物件的父系。 這個方法相當於 IAMTimelineObj：： SetStartStop，但會接受 REFTIME 的值。
ms.assetid: 0fc79c82-d8e1-4b87-9e59-6d9e6ca614f3
title: 'IAMTimelineObj：： SetStartStop2 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetStartStop2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 190e47d2ccee00d202dc16e20704b545447d844f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001125"
---
# <a name="iamtimelineobjsetstartstop2-method"></a><span data-ttu-id="0a7f6-104">IAMTimelineObj：： SetStartStop2 方法</span><span class="sxs-lookup"><span data-stu-id="0a7f6-104">IAMTimelineObj::SetStartStop2 method</span></span>

> [!Note]  
> <span data-ttu-id="0a7f6-105">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="0a7f6-105">\[Deprecated.</span></span> <span data-ttu-id="0a7f6-106">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="0a7f6-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="0a7f6-107">`SetStartStop2`方法會設定物件的開始和停止時間，相對於物件的父系。</span><span class="sxs-lookup"><span data-stu-id="0a7f6-107">The `SetStartStop2` method sets the object's start and stop times, relative to the object's parent.</span></span> <span data-ttu-id="0a7f6-108">這個方法相當於 [**IAMTimelineObj：： SetStartStop**](iamtimelineobj-setstartstop.md)，但會接受 [**REFTIME**](reftime.md) 的值。</span><span class="sxs-lookup"><span data-stu-id="0a7f6-108">This method is equivalent to [**IAMTimelineObj::SetStartStop**](iamtimelineobj-setstartstop.md), but takes [**REFTIME**](reftime.md) values.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a7f6-109">語法</span><span class="sxs-lookup"><span data-stu-id="0a7f6-109">Syntax</span></span>


```C++
HRESULT SetStartStop2(
   REFTIME Start,
   REFTIME Stop
);
```



## <a name="parameters"></a><span data-ttu-id="0a7f6-110">參數</span><span class="sxs-lookup"><span data-stu-id="0a7f6-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a7f6-111">*開始*</span><span class="sxs-lookup"><span data-stu-id="0a7f6-111">*Start*</span></span> 
</dt> <dd>

<span data-ttu-id="0a7f6-112">新的開始時間（以秒為單位），或-1 會保留現有的開始時間。</span><span class="sxs-lookup"><span data-stu-id="0a7f6-112">New start time, in seconds, or –1 to keep the existing start time.</span></span>

</dd> <dt>

<span data-ttu-id="0a7f6-113">*停止*</span><span class="sxs-lookup"><span data-stu-id="0a7f6-113">*Stop*</span></span> 
</dt> <dd>

<span data-ttu-id="0a7f6-114">新的停止時間（以秒為單位），或-1 會保留現有的停止時間。</span><span class="sxs-lookup"><span data-stu-id="0a7f6-114">New stop time, in seconds, or –1 to keep the existing stop time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a7f6-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="0a7f6-115">Return value</span></span>

<span data-ttu-id="0a7f6-116">傳回下列其中一個 **HRESULT** 值：</span><span class="sxs-lookup"><span data-stu-id="0a7f6-116">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="0a7f6-117">傳回碼</span><span class="sxs-lookup"><span data-stu-id="0a7f6-117">Return code</span></span>                                                                                  | <span data-ttu-id="0a7f6-118">Description</span><span class="sxs-lookup"><span data-stu-id="0a7f6-118">Description</span></span>                  |
|----------------------------------------------------------------------------------------------|------------------------------|
| <dl> <span data-ttu-id="0a7f6-119"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="0a7f6-119"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="0a7f6-120">成功。</span><span class="sxs-lookup"><span data-stu-id="0a7f6-120">Success.</span></span><br/>          |
| <dl> <span data-ttu-id="0a7f6-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="0a7f6-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="0a7f6-122">無效引數。</span><span class="sxs-lookup"><span data-stu-id="0a7f6-122">Invalid argument.</span></span><br/> |
| <dl> <span data-ttu-id="0a7f6-123"><dt>**E \_ >NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="0a7f6-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>    | <span data-ttu-id="0a7f6-124">未實作。</span><span class="sxs-lookup"><span data-stu-id="0a7f6-124">Not implemented.</span></span><br/>  |



 

## <a name="remarks"></a><span data-ttu-id="0a7f6-125">備註</span><span class="sxs-lookup"><span data-stu-id="0a7f6-125">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="0a7f6-126">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="0a7f6-126">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="0a7f6-127">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="0a7f6-127">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="0a7f6-128">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="0a7f6-128">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="0a7f6-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="0a7f6-129">Requirements</span></span>



| <span data-ttu-id="0a7f6-130">需求</span><span class="sxs-lookup"><span data-stu-id="0a7f6-130">Requirement</span></span> | <span data-ttu-id="0a7f6-131">值</span><span class="sxs-lookup"><span data-stu-id="0a7f6-131">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0a7f6-132">標頭</span><span class="sxs-lookup"><span data-stu-id="0a7f6-132">Header</span></span><br/>  | <dl> <span data-ttu-id="0a7f6-133"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="0a7f6-133"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="0a7f6-134">程式庫</span><span class="sxs-lookup"><span data-stu-id="0a7f6-134">Library</span></span><br/> | <dl> <span data-ttu-id="0a7f6-135"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="0a7f6-135"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a7f6-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0a7f6-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a7f6-137">**IAMTimelineObj 介面**</span><span class="sxs-lookup"><span data-stu-id="0a7f6-137">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="0a7f6-138">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="0a7f6-138">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




