---
description: ModifyStopTime 方法會設定相對於時程表的停止時間。
ms.assetid: 0d9b6cf7-d029-4c35-9045-82cbeff1e3ae
title: 'IAMTimelineSrc：： ModifyStopTime 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.ModifyStopTime
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 5e0f3ac58df4e74926d2163705261ffad4551e69
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996075"
---
# <a name="iamtimelinesrcmodifystoptime-method"></a><span data-ttu-id="d3758-103">IAMTimelineSrc：： ModifyStopTime 方法</span><span class="sxs-lookup"><span data-stu-id="d3758-103">IAMTimelineSrc::ModifyStopTime method</span></span>

> [!Note]  
> <span data-ttu-id="d3758-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="d3758-104">\[Deprecated.</span></span> <span data-ttu-id="d3758-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="d3758-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="d3758-106">`ModifyStopTime`方法會設定相對於時程表的停止時間。</span><span class="sxs-lookup"><span data-stu-id="d3758-106">The `ModifyStopTime` method sets the stop time, relative to the timeline.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3758-107">語法</span><span class="sxs-lookup"><span data-stu-id="d3758-107">Syntax</span></span>


```C++
HRESULT ModifyStopTime(
   REFERENCE_TIME Stop
);
```



## <a name="parameters"></a><span data-ttu-id="d3758-108">參數</span><span class="sxs-lookup"><span data-stu-id="d3758-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3758-109">*停止*</span><span class="sxs-lookup"><span data-stu-id="d3758-109">*Stop*</span></span> 
</dt> <dd>

<span data-ttu-id="d3758-110">新的停止時間，以 100-毫微秒單位表示。</span><span class="sxs-lookup"><span data-stu-id="d3758-110">New stop time, in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d3758-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="d3758-111">Return value</span></span>

<span data-ttu-id="d3758-112">\_如果指定的時間無效，則傳回 S OK 或 E \_ INVALIDARG。</span><span class="sxs-lookup"><span data-stu-id="d3758-112">Returns S\_OK, or E\_INVALIDARG if the specified time is not valid.</span></span>

## <a name="remarks"></a><span data-ttu-id="d3758-113">備註</span><span class="sxs-lookup"><span data-stu-id="d3758-113">Remarks</span></span>

<span data-ttu-id="d3758-114">這個方法相當於呼叫 [**IAMTimelineObj：： SetStartStop**](iamtimelineobj-setstartstop.md) 與原始開始時間和新的停止時間。</span><span class="sxs-lookup"><span data-stu-id="d3758-114">This method is equivalent to calling [**IAMTimelineObj::SetStartStop**](iamtimelineobj-setstartstop.md) with the original start time and a new stop time.</span></span>

> [!Note]  
> <span data-ttu-id="d3758-115">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="d3758-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="d3758-116">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="d3758-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="d3758-117">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="d3758-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d3758-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="d3758-118">Requirements</span></span>



| <span data-ttu-id="d3758-119">需求</span><span class="sxs-lookup"><span data-stu-id="d3758-119">Requirement</span></span> | <span data-ttu-id="d3758-120">值</span><span class="sxs-lookup"><span data-stu-id="d3758-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d3758-121">標頭</span><span class="sxs-lookup"><span data-stu-id="d3758-121">Header</span></span><br/>  | <dl> <span data-ttu-id="d3758-122"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="d3758-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="d3758-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="d3758-123">Library</span></span><br/> | <dl> <span data-ttu-id="d3758-124"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="d3758-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d3758-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d3758-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3758-126">**IAMTimelineSrc 介面**</span><span class="sxs-lookup"><span data-stu-id="d3758-126">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="d3758-127">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="d3758-127">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




