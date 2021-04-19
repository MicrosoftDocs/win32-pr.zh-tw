---
description: SetDynamicReconnectLevel 方法會在轉譯期間設定動態重新連接的層級。
ms.assetid: 092f3464-84a2-48b0-9647-66fe27e9706d
title: 'IRenderEngine：： SetDynamicReconnectLevel 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.SetDynamicReconnectLevel
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ae02fb6158b58cd5785aa7df539651acfbea5db8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001843"
---
# <a name="irenderenginesetdynamicreconnectlevel-method"></a><span data-ttu-id="2c8c2-103">IRenderEngine：： SetDynamicReconnectLevel 方法</span><span class="sxs-lookup"><span data-stu-id="2c8c2-103">IRenderEngine::SetDynamicReconnectLevel method</span></span>

> [!Note]  
> <span data-ttu-id="2c8c2-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="2c8c2-104">\[Deprecated.</span></span> <span data-ttu-id="2c8c2-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="2c8c2-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="2c8c2-106">方法會在轉譯 `SetDynamicReconnectLevel` 期間設定動態重新連接的層級。</span><span class="sxs-lookup"><span data-stu-id="2c8c2-106">The `SetDynamicReconnectLevel` method sets the level of dynamic reconnection during rendering.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c8c2-107">語法</span><span class="sxs-lookup"><span data-stu-id="2c8c2-107">Syntax</span></span>


```C++
HRESULT SetDynamicReconnectLevel(
   DWORD Level
);
```



## <a name="parameters"></a><span data-ttu-id="2c8c2-108">參數</span><span class="sxs-lookup"><span data-stu-id="2c8c2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c8c2-109">*Level*</span><span class="sxs-lookup"><span data-stu-id="2c8c2-109">*Level*</span></span> 
</dt> <dd>

<span data-ttu-id="2c8c2-110">動態重新 [**連接旗標**](dynamic-reconnection-flags.md)的組合，指定動態重新連接的層級。</span><span class="sxs-lookup"><span data-stu-id="2c8c2-110">Combination of [**Dynamic Reconnection Flags**](dynamic-reconnection-flags.md), specifying the level of dynamic reconnection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c8c2-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="2c8c2-111">Return value</span></span>

<span data-ttu-id="2c8c2-112">傳回下列其中一個 **HRESULT** 值：</span><span class="sxs-lookup"><span data-stu-id="2c8c2-112">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="2c8c2-113">傳回碼</span><span class="sxs-lookup"><span data-stu-id="2c8c2-113">Return code</span></span>                                                                               | <span data-ttu-id="2c8c2-114">Description</span><span class="sxs-lookup"><span data-stu-id="2c8c2-114">Description</span></span>                 |
|-------------------------------------------------------------------------------------------|-----------------------------|
| <dl> <span data-ttu-id="2c8c2-115"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="2c8c2-115"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="2c8c2-116">成功。</span><span class="sxs-lookup"><span data-stu-id="2c8c2-116">Success.</span></span><br/>         |
| <dl> <span data-ttu-id="2c8c2-117"><dt>**E \_ >NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="2c8c2-117"><dt>**E\_NOTIMPL**</dt></span></span> </dl> | <span data-ttu-id="2c8c2-118">未實作。</span><span class="sxs-lookup"><span data-stu-id="2c8c2-118">Not implemented.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="2c8c2-119">備註</span><span class="sxs-lookup"><span data-stu-id="2c8c2-119">Remarks</span></span>

<span data-ttu-id="2c8c2-120">根據預設，基本轉譯引擎會在轉譯專案之前載入每個來源。</span><span class="sxs-lookup"><span data-stu-id="2c8c2-120">By default, the basic render engine loads every source before rendering a project.</span></span> <span data-ttu-id="2c8c2-121">這可能會導致很長的啟動時間。</span><span class="sxs-lookup"><span data-stu-id="2c8c2-121">This can result in a long start-up time.</span></span> <span data-ttu-id="2c8c2-122">使用動態重新連接時，只有在需要時才會載入來源。</span><span class="sxs-lookup"><span data-stu-id="2c8c2-122">With dynamic reconnection, sources are loaded only when needed.</span></span> <span data-ttu-id="2c8c2-123">這可以縮短啟動時間，但可能會干擾順暢的播放。</span><span class="sxs-lookup"><span data-stu-id="2c8c2-123">This can shorten the start-up time, but possibly interfere with smooth playback.</span></span> <span data-ttu-id="2c8c2-124">通常，專案所使用的來源剪輯越多，您可能會受益于動態重新連接。</span><span class="sxs-lookup"><span data-stu-id="2c8c2-124">Generally, the more source clips that a project uses, the more you might benefit from dynamic reconnection.</span></span>

<span data-ttu-id="2c8c2-125">智慧型轉譯引擎不會執行此方法。</span><span class="sxs-lookup"><span data-stu-id="2c8c2-125">The smart render engine does not implement this method.</span></span>

> [!Note]  
> <span data-ttu-id="2c8c2-126">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="2c8c2-126">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="2c8c2-127">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="2c8c2-127">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="2c8c2-128">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="2c8c2-128">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="2c8c2-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="2c8c2-129">Requirements</span></span>



| <span data-ttu-id="2c8c2-130">需求</span><span class="sxs-lookup"><span data-stu-id="2c8c2-130">Requirement</span></span> | <span data-ttu-id="2c8c2-131">值</span><span class="sxs-lookup"><span data-stu-id="2c8c2-131">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2c8c2-132">標頭</span><span class="sxs-lookup"><span data-stu-id="2c8c2-132">Header</span></span><br/>  | <dl> <span data-ttu-id="2c8c2-133"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="2c8c2-133"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="2c8c2-134">程式庫</span><span class="sxs-lookup"><span data-stu-id="2c8c2-134">Library</span></span><br/> | <dl> <span data-ttu-id="2c8c2-135"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="2c8c2-135"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c8c2-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2c8c2-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c8c2-137">**IRenderEngine 介面**</span><span class="sxs-lookup"><span data-stu-id="2c8c2-137">**IRenderEngine Interface**</span></span>](irenderengine.md)
</dt> <dt>

[<span data-ttu-id="2c8c2-138">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="2c8c2-138">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




