---
description: GetCutPoint 方法會抓取剪下點。
ms.assetid: f54ef17e-3407-4164-911d-3dc7fad656ed
title: 'IAMTimelineTrans：： GetCutPoint 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrans.GetCutPoint
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e89cc2e7bc6d18842212a58bc5c00b6424947b66
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983225"
---
# <a name="iamtimelinetransgetcutpoint-method"></a><span data-ttu-id="5de85-103">IAMTimelineTrans：： GetCutPoint 方法</span><span class="sxs-lookup"><span data-stu-id="5de85-103">IAMTimelineTrans::GetCutPoint method</span></span>

> [!Note]  
> <span data-ttu-id="5de85-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="5de85-104">\[Deprecated.</span></span> <span data-ttu-id="5de85-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="5de85-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="5de85-106">方法會抓取 `GetCutPoint` 剪下點。</span><span class="sxs-lookup"><span data-stu-id="5de85-106">The `GetCutPoint` method retrieves the cut point.</span></span> <span data-ttu-id="5de85-107">如果您將轉換轉譯為剪下，剪下點就是轉換從某個來源剪下到下一個來源的時間。</span><span class="sxs-lookup"><span data-stu-id="5de85-107">If you render a transition as a cut, the cut point is the time when the transition cuts from one source to the next.</span></span> <span data-ttu-id="5de85-108">根據預設，這個值是轉換的中間。</span><span class="sxs-lookup"><span data-stu-id="5de85-108">By default, this value is the middle of the transition.</span></span> <span data-ttu-id="5de85-109">例如，在橫跨1秒的轉換中，預設的剪下點在轉換中是0.5 秒。</span><span class="sxs-lookup"><span data-stu-id="5de85-109">For example, in a transition that spans one second, the default cut point is 0.5 seconds into the transition.</span></span>

## <a name="syntax"></a><span data-ttu-id="5de85-110">語法</span><span class="sxs-lookup"><span data-stu-id="5de85-110">Syntax</span></span>


```C++
HRESULT GetCutPoint(
   REFERENCE_TIME *pTLTime
);
```



## <a name="parameters"></a><span data-ttu-id="5de85-111">參數</span><span class="sxs-lookup"><span data-stu-id="5de85-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5de85-112">*pTLTime*</span><span class="sxs-lookup"><span data-stu-id="5de85-112">*pTLTime*</span></span> 
</dt> <dd>

<span data-ttu-id="5de85-113">接收相對於轉換開始時間的剪點（以 100-毫微秒單位表示）。</span><span class="sxs-lookup"><span data-stu-id="5de85-113">Receives the cut point, relative to the start time of the transition, in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5de85-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="5de85-114">Return value</span></span>

<span data-ttu-id="5de85-115">傳回下列其中一個 **HRESULT** 值：</span><span class="sxs-lookup"><span data-stu-id="5de85-115">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="5de85-116">傳回碼</span><span class="sxs-lookup"><span data-stu-id="5de85-116">Return code</span></span>                                                                               | <span data-ttu-id="5de85-117">Description</span><span class="sxs-lookup"><span data-stu-id="5de85-117">Description</span></span>                                                                    |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5de85-118"><dt>**S \_ FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="5de85-118"><dt>**S\_FALSE**</dt></span></span> </dl>   | <span data-ttu-id="5de85-119">未設定剪下點。</span><span class="sxs-lookup"><span data-stu-id="5de85-119">The cut point was not set.</span></span> <span data-ttu-id="5de85-120">傳回的值是預設值。</span><span class="sxs-lookup"><span data-stu-id="5de85-120">The value returned is the default value.</span></span><br/> |
| <dl> <span data-ttu-id="5de85-121"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="5de85-121"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="5de85-122">剪下點已設定為預設值以外的值。</span><span class="sxs-lookup"><span data-stu-id="5de85-122">The cut point was set to a value other than the default.</span></span><br/>            |
| <dl> <span data-ttu-id="5de85-123"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="5de85-123"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="5de85-124">**Null** 指標引數。</span><span class="sxs-lookup"><span data-stu-id="5de85-124">**NULL** pointer argument.</span></span><br/>                                          |



 

## <a name="remarks"></a><span data-ttu-id="5de85-125">備註</span><span class="sxs-lookup"><span data-stu-id="5de85-125">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="5de85-126">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="5de85-126">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="5de85-127">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="5de85-127">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="5de85-128">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="5de85-128">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5de85-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="5de85-129">Requirements</span></span>



| <span data-ttu-id="5de85-130">需求</span><span class="sxs-lookup"><span data-stu-id="5de85-130">Requirement</span></span> | <span data-ttu-id="5de85-131">值</span><span class="sxs-lookup"><span data-stu-id="5de85-131">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5de85-132">標頭</span><span class="sxs-lookup"><span data-stu-id="5de85-132">Header</span></span><br/>  | <dl> <span data-ttu-id="5de85-133"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="5de85-133"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="5de85-134">程式庫</span><span class="sxs-lookup"><span data-stu-id="5de85-134">Library</span></span><br/> | <dl> <span data-ttu-id="5de85-135"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="5de85-135"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5de85-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5de85-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5de85-137">**IAMTimelineTrans 介面**</span><span class="sxs-lookup"><span data-stu-id="5de85-137">**IAMTimelineTrans Interface**</span></span>](iamtimelinetrans.md)
</dt> <dt>

[<span data-ttu-id="5de85-138">**IAMTimelineTrans::SetCutPoint**</span><span class="sxs-lookup"><span data-stu-id="5de85-138">**IAMTimelineTrans::SetCutPoint**</span></span>](iamtimelinetrans-setcutpoint.md)
</dt> <dt>

[<span data-ttu-id="5de85-139">**IAMTimelineTrans::GetCutsOnly**</span><span class="sxs-lookup"><span data-stu-id="5de85-139">**IAMTimelineTrans::GetCutsOnly**</span></span>](iamtimelinetrans-getcutsonly.md)
</dt> <dt>

[<span data-ttu-id="5de85-140">**IAMTimeline::TransitionsEnabled**</span><span class="sxs-lookup"><span data-stu-id="5de85-140">**IAMTimeline::TransitionsEnabled**</span></span>](iamtimeline-transitionsenabled.md)
</dt> <dt>

[<span data-ttu-id="5de85-141">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="5de85-141">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




