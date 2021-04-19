---
description: ZeroBetween2 方法會從指定時間之間的曲目中移除所有專案。 這個方法相當於 IAMTimelineTrack：： ZeroBetween，但會接受 REFTIME 的值。
ms.assetid: 56b9be30-cc3f-4843-bf35-910498242d71
title: 'IAMTimelineTrack：： ZeroBetween2 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.ZeroBetween2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 27e3ab5cc2a631cb54c926824c2f3410413cd981
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982944"
---
# <a name="iamtimelinetrackzerobetween2-method"></a><span data-ttu-id="76d24-104">IAMTimelineTrack：： ZeroBetween2 方法</span><span class="sxs-lookup"><span data-stu-id="76d24-104">IAMTimelineTrack::ZeroBetween2 method</span></span>

> [!Note]  
> <span data-ttu-id="76d24-105">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="76d24-105">\[Deprecated.</span></span> <span data-ttu-id="76d24-106">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="76d24-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="76d24-107">`ZeroBetween2`方法會從指定時間之間的曲目中移除所有專案。</span><span class="sxs-lookup"><span data-stu-id="76d24-107">The `ZeroBetween2` method removes everything from the track between the specified times.</span></span> <span data-ttu-id="76d24-108">這個方法相當於 [**IAMTimelineTrack：： ZeroBetween**](iamtimelinetrack-zerobetween.md)，但會接受 [**REFTIME**](reftime.md) 的值。</span><span class="sxs-lookup"><span data-stu-id="76d24-108">This method is equivalent to [**IAMTimelineTrack::ZeroBetween**](iamtimelinetrack-zerobetween.md), but takes [**REFTIME**](reftime.md) values.</span></span>

## <a name="syntax"></a><span data-ttu-id="76d24-109">語法</span><span class="sxs-lookup"><span data-stu-id="76d24-109">Syntax</span></span>


```C++
HRESULT ZeroBetween2(
   REFTIME rtStart,
   REFTIME rtEnd
);
```



## <a name="parameters"></a><span data-ttu-id="76d24-110">參數</span><span class="sxs-lookup"><span data-stu-id="76d24-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="76d24-111">*rtStart*</span><span class="sxs-lookup"><span data-stu-id="76d24-111">*rtStart*</span></span> 
</dt> <dd>

<span data-ttu-id="76d24-112">要清除的範圍開頭（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="76d24-112">Beginning of the range to clear, in seconds.</span></span>

</dd> <dt>

<span data-ttu-id="76d24-113">*rtEnd*</span><span class="sxs-lookup"><span data-stu-id="76d24-113">*rtEnd*</span></span> 
</dt> <dd>

<span data-ttu-id="76d24-114">要清除的範圍結尾（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="76d24-114">End of the range to clear, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="76d24-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="76d24-115">Return value</span></span>

<span data-ttu-id="76d24-116">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="76d24-116">Returns an **HRESULT** value.</span></span> <span data-ttu-id="76d24-117">可能的值如下。</span><span class="sxs-lookup"><span data-stu-id="76d24-117">Possible values include the following.</span></span>



| <span data-ttu-id="76d24-118">傳回碼</span><span class="sxs-lookup"><span data-stu-id="76d24-118">Return code</span></span>                                                                             | <span data-ttu-id="76d24-119">Description</span><span class="sxs-lookup"><span data-stu-id="76d24-119">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="76d24-120"><dt>**S \_ FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="76d24-120"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="76d24-121">時間範圍超出曲目中的所有專案。</span><span class="sxs-lookup"><span data-stu-id="76d24-121">The time range falls beyond everything in the track.</span></span><br/> |
| <dl> <span data-ttu-id="76d24-122"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="76d24-122"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="76d24-123">成功。</span><span class="sxs-lookup"><span data-stu-id="76d24-123">Success.</span></span><br/>                                             |



 

## <a name="remarks"></a><span data-ttu-id="76d24-124">備註</span><span class="sxs-lookup"><span data-stu-id="76d24-124">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="76d24-125">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="76d24-125">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="76d24-126">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="76d24-126">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="76d24-127">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="76d24-127">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="76d24-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="76d24-128">Requirements</span></span>



| <span data-ttu-id="76d24-129">需求</span><span class="sxs-lookup"><span data-stu-id="76d24-129">Requirement</span></span> | <span data-ttu-id="76d24-130">值</span><span class="sxs-lookup"><span data-stu-id="76d24-130">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="76d24-131">標頭</span><span class="sxs-lookup"><span data-stu-id="76d24-131">Header</span></span><br/>  | <dl> <span data-ttu-id="76d24-132"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="76d24-132"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="76d24-133">程式庫</span><span class="sxs-lookup"><span data-stu-id="76d24-133">Library</span></span><br/> | <dl> <span data-ttu-id="76d24-134"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="76d24-134"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="76d24-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="76d24-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76d24-136">**IAMTimelineTrack 介面**</span><span class="sxs-lookup"><span data-stu-id="76d24-136">**IAMTimelineTrack Interface**</span></span>](iamtimelinetrack.md)
</dt> <dt>

[<span data-ttu-id="76d24-137">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="76d24-137">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




