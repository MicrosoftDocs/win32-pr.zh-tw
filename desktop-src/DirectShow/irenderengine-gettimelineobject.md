---
description: GetTimelineObject 方法會抓取轉譯引擎目前使用的時間軸。
ms.assetid: 74398f85-07b2-42fa-bb4f-a1e7e1669e3f
title: 'IRenderEngine：： GetTimelineObject 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.GetTimelineObject
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: aab8e9a5f77affc464763b1c5a5045eaa4fc042a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995395"
---
# <a name="irenderenginegettimelineobject-method"></a><span data-ttu-id="496d3-103">IRenderEngine：： GetTimelineObject 方法</span><span class="sxs-lookup"><span data-stu-id="496d3-103">IRenderEngine::GetTimelineObject method</span></span>

> [!Note]  
> <span data-ttu-id="496d3-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="496d3-104">\[Deprecated.</span></span> <span data-ttu-id="496d3-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="496d3-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="496d3-106">`GetTimelineObject`方法會抓取轉譯引擎目前使用的時間軸。</span><span class="sxs-lookup"><span data-stu-id="496d3-106">The `GetTimelineObject` method retrieves the timeline that the render engine is currently using.</span></span>

## <a name="syntax"></a><span data-ttu-id="496d3-107">語法</span><span class="sxs-lookup"><span data-stu-id="496d3-107">Syntax</span></span>


```C++
HRESULT GetTimelineObject(
  [out] IAMTimeline **ppTimeline
);
```



## <a name="parameters"></a><span data-ttu-id="496d3-108">參數</span><span class="sxs-lookup"><span data-stu-id="496d3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="496d3-109">*ppTimeline* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="496d3-109">*ppTimeline* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="496d3-110">接收時間軸 [**IAMTimeline**](iamtimeline.md) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="496d3-110">Receives a pointer to the timeline's [**IAMTimeline**](iamtimeline.md) interface.</span></span> <span data-ttu-id="496d3-111">如果沒有時間軸，則會接收 **Null** 值。</span><span class="sxs-lookup"><span data-stu-id="496d3-111">It receives the value **NULL** if there is no timeline.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="496d3-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="496d3-112">Return value</span></span>

<span data-ttu-id="496d3-113">傳回下列其中一個 **HRESULT** 值：</span><span class="sxs-lookup"><span data-stu-id="496d3-113">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="496d3-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="496d3-114">Return code</span></span>                                                                                            | <span data-ttu-id="496d3-115">Description</span><span class="sxs-lookup"><span data-stu-id="496d3-115">Description</span></span>                                    |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="496d3-116"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="496d3-116"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="496d3-117">成功。</span><span class="sxs-lookup"><span data-stu-id="496d3-117">Success.</span></span><br/>                            |
| <dl> <span data-ttu-id="496d3-118"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="496d3-118"><dt>**E\_POINTER**</dt></span></span> </dl>              | <span data-ttu-id="496d3-119">指標無效。</span><span class="sxs-lookup"><span data-stu-id="496d3-119">Invalid pointer.</span></span><br/>                    |
| <dl> <span data-ttu-id="496d3-120"><dt>**E \_ 必須 \_ INIT 轉譯器 \_**</dt></span><span class="sxs-lookup"><span data-stu-id="496d3-120"><dt>**E\_MUST\_INIT\_RENDERER**</dt></span></span> </dl> | <span data-ttu-id="496d3-121">轉譯引擎無法初始化。</span><span class="sxs-lookup"><span data-stu-id="496d3-121">Render engine failed to initialize.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="496d3-122">備註</span><span class="sxs-lookup"><span data-stu-id="496d3-122">Remarks</span></span>

<span data-ttu-id="496d3-123">傳回時，如果 *\* ppTimeline* 的值為非 **Null**，則 **IAMTimeline** 介面具有未處理的參考計數。</span><span class="sxs-lookup"><span data-stu-id="496d3-123">On return, if the value of *\*ppTimeline* is non-**NULL**, the **IAMTimeline** interface has an outstanding reference count.</span></span> <span data-ttu-id="496d3-124">使用完畢後，請務必釋放介面。</span><span class="sxs-lookup"><span data-stu-id="496d3-124">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="496d3-125">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="496d3-125">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="496d3-126">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="496d3-126">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="496d3-127">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="496d3-127">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="496d3-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="496d3-128">Requirements</span></span>



| <span data-ttu-id="496d3-129">需求</span><span class="sxs-lookup"><span data-stu-id="496d3-129">Requirement</span></span> | <span data-ttu-id="496d3-130">值</span><span class="sxs-lookup"><span data-stu-id="496d3-130">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="496d3-131">標頭</span><span class="sxs-lookup"><span data-stu-id="496d3-131">Header</span></span><br/>  | <dl> <span data-ttu-id="496d3-132"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="496d3-132"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="496d3-133">程式庫</span><span class="sxs-lookup"><span data-stu-id="496d3-133">Library</span></span><br/> | <dl> <span data-ttu-id="496d3-134"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="496d3-134"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="496d3-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="496d3-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="496d3-136">**IRenderEngine 介面**</span><span class="sxs-lookup"><span data-stu-id="496d3-136">**IRenderEngine Interface**</span></span>](irenderengine.md)
</dt> <dt>

[<span data-ttu-id="496d3-137">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="496d3-137">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




