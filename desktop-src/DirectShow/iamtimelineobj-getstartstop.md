---
description: GetStartStop 方法會抓取物件的開始和停止時間（相對於物件的父系）。
ms.assetid: de77e332-85ba-48bf-ae37-f198ce7c3a73
title: 'IAMTimelineObj：： GetStartStop 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetStartStop
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: aa4204f2bd41d72a6d3ef67f633f8b64a58051b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992882"
---
# <a name="iamtimelineobjgetstartstop-method"></a><span data-ttu-id="2d4fc-103">IAMTimelineObj：： GetStartStop 方法</span><span class="sxs-lookup"><span data-stu-id="2d4fc-103">IAMTimelineObj::GetStartStop method</span></span>

> [!Note]  
> <span data-ttu-id="2d4fc-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="2d4fc-104">\[Deprecated.</span></span> <span data-ttu-id="2d4fc-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="2d4fc-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="2d4fc-106">方法會抓取 `GetStartStop` 物件的開始和停止時間（相對於物件的父系）。</span><span class="sxs-lookup"><span data-stu-id="2d4fc-106">The `GetStartStop` method retrieves the object's start and stop times, relative to the object's parent.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d4fc-107">語法</span><span class="sxs-lookup"><span data-stu-id="2d4fc-107">Syntax</span></span>


```C++
HRESULT GetStartStop(
   REFERENCE_TIME *pStart,
   REFERENCE_TIME *pStop
);
```



## <a name="parameters"></a><span data-ttu-id="2d4fc-108">參數</span><span class="sxs-lookup"><span data-stu-id="2d4fc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d4fc-109">*pStart*</span><span class="sxs-lookup"><span data-stu-id="2d4fc-109">*pStart*</span></span> 
</dt> <dd>

<span data-ttu-id="2d4fc-110">接收開始時間，以 100-毫微秒單位表示。</span><span class="sxs-lookup"><span data-stu-id="2d4fc-110">Receives the start time, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="2d4fc-111">*pStop*</span><span class="sxs-lookup"><span data-stu-id="2d4fc-111">*pStop*</span></span> 
</dt> <dd>

<span data-ttu-id="2d4fc-112">接收停止時間，以 100-毫微秒單位表示。</span><span class="sxs-lookup"><span data-stu-id="2d4fc-112">Receives the stop time, in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2d4fc-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="2d4fc-113">Return value</span></span>

<span data-ttu-id="2d4fc-114">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="2d4fc-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="2d4fc-115">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="2d4fc-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="2d4fc-116">備註</span><span class="sxs-lookup"><span data-stu-id="2d4fc-116">Remarks</span></span>

<span data-ttu-id="2d4fc-117">組合、群組和曲目的開始時間一律為0。</span><span class="sxs-lookup"><span data-stu-id="2d4fc-117">Compositions, groups, and tracks always have a start time of 0.</span></span>

<span data-ttu-id="2d4fc-118">在轉譯期間，DES 會將物件的開始和停止時間四捨五入至最接近的框架界限。</span><span class="sxs-lookup"><span data-stu-id="2d4fc-118">During rendering, DES rounds an object's start and stop times to the nearest frame boundary.</span></span> <span data-ttu-id="2d4fc-119">不過，DES 不會覆寫物件的時間。</span><span class="sxs-lookup"><span data-stu-id="2d4fc-119">However, DES does not overwrite the object's times.</span></span> <span data-ttu-id="2d4fc-120">如果您變更群組畫面播放速率，則永遠會從原始時間計算舍入的時間。</span><span class="sxs-lookup"><span data-stu-id="2d4fc-120">If you change the group frame rate, the rounded times are always calculated from the original times.</span></span> <span data-ttu-id="2d4fc-121">如需詳細資訊，請查看 [DirectShow 編輯服務的時間](time-in-directshow-editing-services.md)。</span><span class="sxs-lookup"><span data-stu-id="2d4fc-121">For more information, [Time in DirectShow Editing Services](time-in-directshow-editing-services.md).</span></span>

<span data-ttu-id="2d4fc-122">若要判斷轉譯專案中的開始和停止時間，請將傳回的值傳遞 `GetStartStop` 給 [**IAMTimelineObj：： FixTimes**](iamtimelineobj-fixtimes.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="2d4fc-122">To determine the start and stop times in the rendered project, pass the values returned by `GetStartStop` to the [**IAMTimelineObj::FixTimes**](iamtimelineobj-fixtimes.md) method.</span></span>

> [!Note]  
> <span data-ttu-id="2d4fc-123">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="2d4fc-123">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="2d4fc-124">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="2d4fc-124">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="2d4fc-125">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="2d4fc-125">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="2d4fc-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="2d4fc-126">Requirements</span></span>



| <span data-ttu-id="2d4fc-127">需求</span><span class="sxs-lookup"><span data-stu-id="2d4fc-127">Requirement</span></span> | <span data-ttu-id="2d4fc-128">值</span><span class="sxs-lookup"><span data-stu-id="2d4fc-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2d4fc-129">標頭</span><span class="sxs-lookup"><span data-stu-id="2d4fc-129">Header</span></span><br/>  | <dl> <span data-ttu-id="2d4fc-130"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="2d4fc-130"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="2d4fc-131">程式庫</span><span class="sxs-lookup"><span data-stu-id="2d4fc-131">Library</span></span><br/> | <dl> <span data-ttu-id="2d4fc-132"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="2d4fc-132"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2d4fc-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2d4fc-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d4fc-134">**IAMTimelineObj 介面**</span><span class="sxs-lookup"><span data-stu-id="2d4fc-134">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="2d4fc-135">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="2d4fc-135">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




