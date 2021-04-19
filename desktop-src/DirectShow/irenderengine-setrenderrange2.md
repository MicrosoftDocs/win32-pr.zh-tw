---
description: SetRenderRange2 方法會設定時間軸上要轉譯的時間範圍。 這個方法相當於 IRenderEngine：： SetRenderRange，但會採用 double 類型的值。
ms.assetid: 07df97a8-aa83-405d-91a0-45cd99185588
title: 'IRenderEngine：： SetRenderRange2 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.SetRenderRange2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 555533b11c96073763af0d2b52823af44e3797be
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001121"
---
# <a name="irenderenginesetrenderrange2-method"></a><span data-ttu-id="cfe01-104">IRenderEngine：： SetRenderRange2 方法</span><span class="sxs-lookup"><span data-stu-id="cfe01-104">IRenderEngine::SetRenderRange2 method</span></span>

> [!Note]  
> <span data-ttu-id="cfe01-105">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="cfe01-105">\[Deprecated.</span></span> <span data-ttu-id="cfe01-106">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="cfe01-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="cfe01-107">`SetRenderRange2`方法會設定要轉譯的時間軸上的時間範圍。</span><span class="sxs-lookup"><span data-stu-id="cfe01-107">The `SetRenderRange2` method sets the range of time on the timeline to be rendered.</span></span> <span data-ttu-id="cfe01-108">這個方法相當於 [**IRenderEngine：： SetRenderRange**](irenderengine-setrenderrange.md)，但會採用 **double** 類型的值。</span><span class="sxs-lookup"><span data-stu-id="cfe01-108">This method is equivalent to [**IRenderEngine::SetRenderRange**](irenderengine-setrenderrange.md), but takes values of type **double**.</span></span>

## <a name="syntax"></a><span data-ttu-id="cfe01-109">語法</span><span class="sxs-lookup"><span data-stu-id="cfe01-109">Syntax</span></span>


```C++
HRESULT SetRenderRange2(
   double Start,
   double Stop
);
```



## <a name="parameters"></a><span data-ttu-id="cfe01-110">參數</span><span class="sxs-lookup"><span data-stu-id="cfe01-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cfe01-111">*開始*</span><span class="sxs-lookup"><span data-stu-id="cfe01-111">*Start*</span></span> 
</dt> <dd>

<span data-ttu-id="cfe01-112">開始時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="cfe01-112">Start time, in seconds.</span></span>

</dd> <dt>

<span data-ttu-id="cfe01-113">*停止*</span><span class="sxs-lookup"><span data-stu-id="cfe01-113">*Stop*</span></span> 
</dt> <dd>

<span data-ttu-id="cfe01-114">停止時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="cfe01-114">Stop time, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cfe01-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="cfe01-115">Return value</span></span>

<span data-ttu-id="cfe01-116">傳回下列其中一個 **HRESULT** 值：</span><span class="sxs-lookup"><span data-stu-id="cfe01-116">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="cfe01-117">傳回碼</span><span class="sxs-lookup"><span data-stu-id="cfe01-117">Return code</span></span>                                                                                            | <span data-ttu-id="cfe01-118">Description</span><span class="sxs-lookup"><span data-stu-id="cfe01-118">Description</span></span>                                    |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="cfe01-119"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="cfe01-119"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="cfe01-120">成功。</span><span class="sxs-lookup"><span data-stu-id="cfe01-120">Success.</span></span><br/>                            |
| <dl> <span data-ttu-id="cfe01-121"><dt>**E \_ 必須 \_ INIT 轉譯器 \_**</dt></span><span class="sxs-lookup"><span data-stu-id="cfe01-121"><dt>**E\_MUST\_INIT\_RENDERER**</dt></span></span> </dl> | <span data-ttu-id="cfe01-122">轉譯引擎無法初始化。</span><span class="sxs-lookup"><span data-stu-id="cfe01-122">Render engine failed to initialize.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="cfe01-123">備註</span><span class="sxs-lookup"><span data-stu-id="cfe01-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="cfe01-124">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="cfe01-124">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="cfe01-125">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="cfe01-125">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="cfe01-126">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="cfe01-126">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="cfe01-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="cfe01-127">Requirements</span></span>



| <span data-ttu-id="cfe01-128">需求</span><span class="sxs-lookup"><span data-stu-id="cfe01-128">Requirement</span></span> | <span data-ttu-id="cfe01-129">值</span><span class="sxs-lookup"><span data-stu-id="cfe01-129">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cfe01-130">標頭</span><span class="sxs-lookup"><span data-stu-id="cfe01-130">Header</span></span><br/>  | <dl> <span data-ttu-id="cfe01-131"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="cfe01-131"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="cfe01-132">程式庫</span><span class="sxs-lookup"><span data-stu-id="cfe01-132">Library</span></span><br/> | <dl> <span data-ttu-id="cfe01-133"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="cfe01-133"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cfe01-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cfe01-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cfe01-135">**IRenderEngine 介面**</span><span class="sxs-lookup"><span data-stu-id="cfe01-135">**IRenderEngine Interface**</span></span>](irenderengine.md)
</dt> <dt>

[<span data-ttu-id="cfe01-136">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="cfe01-136">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




