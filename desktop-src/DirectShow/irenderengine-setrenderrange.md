---
description: SetRenderRange 方法會設定時間軸上要轉譯的時間範圍。 不會轉譯位於指定範圍外的物件，也不會配置資源給它們。
ms.assetid: 2dcdca6b-2bae-4a27-bfbc-19a9b2ea633a
title: 'IRenderEngine：： SetRenderRange 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.SetRenderRange
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e715c2c0077a890948cfd5f5026afe98633325ef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984786"
---
# <a name="irenderenginesetrenderrange-method"></a><span data-ttu-id="2fa00-104">IRenderEngine：： SetRenderRange 方法</span><span class="sxs-lookup"><span data-stu-id="2fa00-104">IRenderEngine::SetRenderRange method</span></span>

> [!Note]  
> <span data-ttu-id="2fa00-105">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="2fa00-105">\[Deprecated.</span></span> <span data-ttu-id="2fa00-106">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="2fa00-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="2fa00-107">`SetRenderRange`方法會設定要轉譯的時間軸上的時間範圍。</span><span class="sxs-lookup"><span data-stu-id="2fa00-107">The `SetRenderRange` method sets the range of time on the timeline to be rendered.</span></span> <span data-ttu-id="2fa00-108">不會轉譯位於指定範圍外的物件，也不會配置資源給它們。</span><span class="sxs-lookup"><span data-stu-id="2fa00-108">Objects that lie outside the specified range are not rendered, and resources are not allocated for them.</span></span>

## <a name="syntax"></a><span data-ttu-id="2fa00-109">語法</span><span class="sxs-lookup"><span data-stu-id="2fa00-109">Syntax</span></span>


```C++
HRESULT SetRenderRange(
   REFERENCE_TIME Start,
   REFERENCE_TIME Stop
);
```



## <a name="parameters"></a><span data-ttu-id="2fa00-110">參數</span><span class="sxs-lookup"><span data-stu-id="2fa00-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2fa00-111">*開始*</span><span class="sxs-lookup"><span data-stu-id="2fa00-111">*Start*</span></span> 
</dt> <dd>

<span data-ttu-id="2fa00-112">開始時間，以 100-毫微秒單位表示。</span><span class="sxs-lookup"><span data-stu-id="2fa00-112">Start time, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="2fa00-113">*停止*</span><span class="sxs-lookup"><span data-stu-id="2fa00-113">*Stop*</span></span> 
</dt> <dd>

<span data-ttu-id="2fa00-114">停止時間，以 100-毫微秒單位表示。</span><span class="sxs-lookup"><span data-stu-id="2fa00-114">Stop time, in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2fa00-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="2fa00-115">Return value</span></span>

<span data-ttu-id="2fa00-116">傳回下列其中一個 **HRESULT** 值：</span><span class="sxs-lookup"><span data-stu-id="2fa00-116">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="2fa00-117">傳回碼</span><span class="sxs-lookup"><span data-stu-id="2fa00-117">Return code</span></span>                                                                                            | <span data-ttu-id="2fa00-118">Description</span><span class="sxs-lookup"><span data-stu-id="2fa00-118">Description</span></span>                                    |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="2fa00-119"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="2fa00-119"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="2fa00-120">成功。</span><span class="sxs-lookup"><span data-stu-id="2fa00-120">Success.</span></span><br/>                            |
| <dl> <span data-ttu-id="2fa00-121"><dt>**E \_ 必須 \_ INIT 轉譯器 \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2fa00-121"><dt>**E\_MUST\_INIT\_RENDERER**</dt></span></span> </dl> | <span data-ttu-id="2fa00-122">轉譯引擎無法初始化。</span><span class="sxs-lookup"><span data-stu-id="2fa00-122">Render engine failed to initialize.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="2fa00-123">備註</span><span class="sxs-lookup"><span data-stu-id="2fa00-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="2fa00-124">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="2fa00-124">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="2fa00-125">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="2fa00-125">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="2fa00-126">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="2fa00-126">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="2fa00-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="2fa00-127">Requirements</span></span>



| <span data-ttu-id="2fa00-128">需求</span><span class="sxs-lookup"><span data-stu-id="2fa00-128">Requirement</span></span> | <span data-ttu-id="2fa00-129">值</span><span class="sxs-lookup"><span data-stu-id="2fa00-129">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2fa00-130">標頭</span><span class="sxs-lookup"><span data-stu-id="2fa00-130">Header</span></span><br/>  | <dl> <span data-ttu-id="2fa00-131"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="2fa00-131"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="2fa00-132">程式庫</span><span class="sxs-lookup"><span data-stu-id="2fa00-132">Library</span></span><br/> | <dl> <span data-ttu-id="2fa00-133"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="2fa00-133"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2fa00-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2fa00-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2fa00-135">**IRenderEngine 介面**</span><span class="sxs-lookup"><span data-stu-id="2fa00-135">**IRenderEngine Interface**</span></span>](irenderengine.md)
</dt> <dt>

[<span data-ttu-id="2fa00-136">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="2fa00-136">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




