---
description: SetTimelineObject 方法會設定轉譯引擎要使用的時間軸。
ms.assetid: 9b60b148-9768-43ba-a986-a96838c4d2bb
title: 'IRenderEngine：： SetTimelineObject 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.SetTimelineObject
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 954fab15e92e6111439abb66d53d53525a5afdb5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995011"
---
# <a name="irenderenginesettimelineobject-method"></a><span data-ttu-id="95ce4-103">IRenderEngine：： SetTimelineObject 方法</span><span class="sxs-lookup"><span data-stu-id="95ce4-103">IRenderEngine::SetTimelineObject method</span></span>

> [!Note]  
> <span data-ttu-id="95ce4-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="95ce4-104">\[Deprecated.</span></span> <span data-ttu-id="95ce4-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="95ce4-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="95ce4-106">`SetTimelineObject`方法會設定轉譯引擎要使用的時間軸。</span><span class="sxs-lookup"><span data-stu-id="95ce4-106">The `SetTimelineObject` method sets the timeline for the render engine to use.</span></span>

## <a name="syntax"></a><span data-ttu-id="95ce4-107">語法</span><span class="sxs-lookup"><span data-stu-id="95ce4-107">Syntax</span></span>


```C++
HRESULT SetTimelineObject(
   IAMTimeline *pTimeline
);
```



## <a name="parameters"></a><span data-ttu-id="95ce4-108">參數</span><span class="sxs-lookup"><span data-stu-id="95ce4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95ce4-109">*pTimeline*</span><span class="sxs-lookup"><span data-stu-id="95ce4-109">*pTimeline*</span></span> 
</dt> <dd>

<span data-ttu-id="95ce4-110">時間軸物件之 [**IAMTimeline**](iamtimeline.md) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="95ce4-110">Pointer to the timeline object's [**IAMTimeline**](iamtimeline.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95ce4-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="95ce4-111">Return value</span></span>

<span data-ttu-id="95ce4-112">傳回下列其中一個 **HRESULT** 值：</span><span class="sxs-lookup"><span data-stu-id="95ce4-112">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="95ce4-113">傳回碼</span><span class="sxs-lookup"><span data-stu-id="95ce4-113">Return code</span></span>                                                                                            | <span data-ttu-id="95ce4-114">Description</span><span class="sxs-lookup"><span data-stu-id="95ce4-114">Description</span></span>                                    |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="95ce4-115"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="95ce4-115"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="95ce4-116">成功。</span><span class="sxs-lookup"><span data-stu-id="95ce4-116">Success.</span></span><br/>                            |
| <dl> <span data-ttu-id="95ce4-117"><dt>**E \_ 必須 \_ INIT 轉譯器 \_**</dt></span><span class="sxs-lookup"><span data-stu-id="95ce4-117"><dt>**E\_MUST\_INIT\_RENDERER**</dt></span></span> </dl> | <span data-ttu-id="95ce4-118">轉譯引擎無法初始化。</span><span class="sxs-lookup"><span data-stu-id="95ce4-118">Render engine failed to initialize.</span></span><br/> |
| <dl> <span data-ttu-id="95ce4-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="95ce4-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>          | <span data-ttu-id="95ce4-120">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="95ce4-120">Insufficient memory.</span></span><br/>                |
| <dl> <span data-ttu-id="95ce4-121"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="95ce4-121"><dt>**E\_POINTER**</dt></span></span> </dl>              | <span data-ttu-id="95ce4-122">指標無效。</span><span class="sxs-lookup"><span data-stu-id="95ce4-122">Invalid pointer.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="95ce4-123">備註</span><span class="sxs-lookup"><span data-stu-id="95ce4-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="95ce4-124">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="95ce4-124">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="95ce4-125">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="95ce4-125">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="95ce4-126">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="95ce4-126">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="95ce4-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="95ce4-127">Requirements</span></span>



| <span data-ttu-id="95ce4-128">需求</span><span class="sxs-lookup"><span data-stu-id="95ce4-128">Requirement</span></span> | <span data-ttu-id="95ce4-129">值</span><span class="sxs-lookup"><span data-stu-id="95ce4-129">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="95ce4-130">標頭</span><span class="sxs-lookup"><span data-stu-id="95ce4-130">Header</span></span><br/>  | <dl> <span data-ttu-id="95ce4-131"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="95ce4-131"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="95ce4-132">程式庫</span><span class="sxs-lookup"><span data-stu-id="95ce4-132">Library</span></span><br/> | <dl> <span data-ttu-id="95ce4-133"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="95ce4-133"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95ce4-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="95ce4-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95ce4-135">**IRenderEngine 介面**</span><span class="sxs-lookup"><span data-stu-id="95ce4-135">**IRenderEngine Interface**</span></span>](irenderengine.md)
</dt> <dt>

[<span data-ttu-id="95ce4-136">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="95ce4-136">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




