---
description: ZeroBetween 方法會從指定時間之間的曲目中移除所有專案。 這個方法會分割橫跨指定時間範圍的任何物件，並移除落在範圍內的片段。
ms.assetid: df173a3c-147b-4f2d-9bcb-a8c2873f5420
title: 'IAMTimelineTrack：： ZeroBetween 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.ZeroBetween
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: bef669bae5e5e5c4c31a49b545fcfc7f58285f97
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981331"
---
# <a name="iamtimelinetrackzerobetween-method"></a><span data-ttu-id="5db4d-104">IAMTimelineTrack：： ZeroBetween 方法</span><span class="sxs-lookup"><span data-stu-id="5db4d-104">IAMTimelineTrack::ZeroBetween method</span></span>

> [!Note]  
> <span data-ttu-id="5db4d-105">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="5db4d-105">\[Deprecated.</span></span> <span data-ttu-id="5db4d-106">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="5db4d-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="5db4d-107">`ZeroBetween`方法會從指定時間之間的曲目中移除所有專案。</span><span class="sxs-lookup"><span data-stu-id="5db4d-107">The `ZeroBetween` method removes everything from the track between the specified times.</span></span> <span data-ttu-id="5db4d-108">這個方法會分割橫跨指定時間範圍的任何物件，並移除落在範圍內的片段。</span><span class="sxs-lookup"><span data-stu-id="5db4d-108">This method splits any objects that span the specified time range and removes the pieces that fall within the range.</span></span>

## <a name="syntax"></a><span data-ttu-id="5db4d-109">語法</span><span class="sxs-lookup"><span data-stu-id="5db4d-109">Syntax</span></span>


```C++
HRESULT ZeroBetween(
   REFERENCE_TIME rtStart,
   REFERENCE_TIME rtEnd
);
```



## <a name="parameters"></a><span data-ttu-id="5db4d-110">參數</span><span class="sxs-lookup"><span data-stu-id="5db4d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5db4d-111">*rtStart*</span><span class="sxs-lookup"><span data-stu-id="5db4d-111">*rtStart*</span></span> 
</dt> <dd>

<span data-ttu-id="5db4d-112">要清除之範圍的開頭，以 100-毫微秒單位表示。</span><span class="sxs-lookup"><span data-stu-id="5db4d-112">Beginning of the range to clear, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="5db4d-113">*rtEnd*</span><span class="sxs-lookup"><span data-stu-id="5db4d-113">*rtEnd*</span></span> 
</dt> <dd>

<span data-ttu-id="5db4d-114">要清除之範圍的結尾，以 100-毫微秒單位表示。</span><span class="sxs-lookup"><span data-stu-id="5db4d-114">End of the range to clear, in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5db4d-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="5db4d-115">Return value</span></span>

<span data-ttu-id="5db4d-116">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="5db4d-116">Returns an **HRESULT** value.</span></span> <span data-ttu-id="5db4d-117">可能的值如下。</span><span class="sxs-lookup"><span data-stu-id="5db4d-117">Possible values include the following.</span></span>



| <span data-ttu-id="5db4d-118">傳回碼</span><span class="sxs-lookup"><span data-stu-id="5db4d-118">Return code</span></span>                                                                             | <span data-ttu-id="5db4d-119">Description</span><span class="sxs-lookup"><span data-stu-id="5db4d-119">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="5db4d-120"><dt>**S \_ FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="5db4d-120"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="5db4d-121">時間範圍超出曲目中的所有專案。</span><span class="sxs-lookup"><span data-stu-id="5db4d-121">The time range falls beyond everything in the track.</span></span><br/> |
| <dl> <span data-ttu-id="5db4d-122"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="5db4d-122"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="5db4d-123">成功。</span><span class="sxs-lookup"><span data-stu-id="5db4d-123">Success.</span></span><br/>                                             |



 

## <a name="remarks"></a><span data-ttu-id="5db4d-124">備註</span><span class="sxs-lookup"><span data-stu-id="5db4d-124">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="5db4d-125">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="5db4d-125">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="5db4d-126">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="5db4d-126">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="5db4d-127">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="5db4d-127">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5db4d-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="5db4d-128">Requirements</span></span>



| <span data-ttu-id="5db4d-129">需求</span><span class="sxs-lookup"><span data-stu-id="5db4d-129">Requirement</span></span> | <span data-ttu-id="5db4d-130">值</span><span class="sxs-lookup"><span data-stu-id="5db4d-130">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5db4d-131">標頭</span><span class="sxs-lookup"><span data-stu-id="5db4d-131">Header</span></span><br/>  | <dl> <span data-ttu-id="5db4d-132"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="5db4d-132"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="5db4d-133">程式庫</span><span class="sxs-lookup"><span data-stu-id="5db4d-133">Library</span></span><br/> | <dl> <span data-ttu-id="5db4d-134"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="5db4d-134"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5db4d-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5db4d-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5db4d-136">**IAMTimelineTrack 介面**</span><span class="sxs-lookup"><span data-stu-id="5db4d-136">**IAMTimelineTrack Interface**</span></span>](iamtimelinetrack.md)
</dt> <dt>

[<span data-ttu-id="5db4d-137">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="5db4d-137">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




