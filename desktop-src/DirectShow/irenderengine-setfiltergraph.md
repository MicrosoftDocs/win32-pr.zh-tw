---
description: SetFilterGraph 方法會指定轉譯引擎要使用的篩選圖形。
ms.assetid: 6a245864-7d22-4608-995b-b28662a6ab90
title: 'IRenderEngine：： SetFilterGraph 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.SetFilterGraph
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 72c93ef6610fd301c497589858a8941e2b8f71b3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981411"
---
# <a name="irenderenginesetfiltergraph-method"></a><span data-ttu-id="bfd7e-103">IRenderEngine：： SetFilterGraph 方法</span><span class="sxs-lookup"><span data-stu-id="bfd7e-103">IRenderEngine::SetFilterGraph method</span></span>

> [!Note]  
> <span data-ttu-id="bfd7e-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="bfd7e-104">\[Deprecated.</span></span> <span data-ttu-id="bfd7e-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="bfd7e-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="bfd7e-106">`SetFilterGraph`方法會指定要用於轉譯引擎的篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="bfd7e-106">The `SetFilterGraph` method specifies a filter graph for the render engine to use.</span></span>

## <a name="syntax"></a><span data-ttu-id="bfd7e-107">語法</span><span class="sxs-lookup"><span data-stu-id="bfd7e-107">Syntax</span></span>


```C++
HRESULT SetFilterGraph(
   IGraphBuilder *pFG
);
```



## <a name="parameters"></a><span data-ttu-id="bfd7e-108">參數</span><span class="sxs-lookup"><span data-stu-id="bfd7e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bfd7e-109">*pFG*</span><span class="sxs-lookup"><span data-stu-id="bfd7e-109">*pFG*</span></span> 
</dt> <dd>

<span data-ttu-id="bfd7e-110">篩選圖形的 [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) 介面指標。</span><span class="sxs-lookup"><span data-stu-id="bfd7e-110">Pointer to the [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) interface of the filter graph.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bfd7e-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="bfd7e-111">Return value</span></span>

<span data-ttu-id="bfd7e-112">傳回下列其中一個 **HRESULT** 值：</span><span class="sxs-lookup"><span data-stu-id="bfd7e-112">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="bfd7e-113">傳回碼</span><span class="sxs-lookup"><span data-stu-id="bfd7e-113">Return code</span></span>                                                                                            | <span data-ttu-id="bfd7e-114">Description</span><span class="sxs-lookup"><span data-stu-id="bfd7e-114">Description</span></span>                                    |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="bfd7e-115"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="bfd7e-115"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="bfd7e-116">成功。</span><span class="sxs-lookup"><span data-stu-id="bfd7e-116">Success.</span></span><br/>                            |
| <dl> <span data-ttu-id="bfd7e-117"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="bfd7e-117"><dt>**E\_INVALIDARG**</dt></span></span> </dl>           | <span data-ttu-id="bfd7e-118">無效引數。</span><span class="sxs-lookup"><span data-stu-id="bfd7e-118">Invalid argument.</span></span><br/>                   |
| <dl> <span data-ttu-id="bfd7e-119"><dt>**E \_ 必須 \_ INIT 轉譯器 \_**</dt></span><span class="sxs-lookup"><span data-stu-id="bfd7e-119"><dt>**E\_MUST\_INIT\_RENDERER**</dt></span></span> </dl> | <span data-ttu-id="bfd7e-120">轉譯引擎無法初始化。</span><span class="sxs-lookup"><span data-stu-id="bfd7e-120">Render engine failed to initialize.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="bfd7e-121">備註</span><span class="sxs-lookup"><span data-stu-id="bfd7e-121">Remarks</span></span>

<span data-ttu-id="bfd7e-122">大部分的應用程式都不需要呼叫此方法。</span><span class="sxs-lookup"><span data-stu-id="bfd7e-122">Most applications do not need to call this method.</span></span> <span data-ttu-id="bfd7e-123">藉由呼叫 [**IRenderEngine：： ConnectFrontEnd**](irenderengine-connectfrontend.md) 方法，讓轉譯引擎為您建立圖形更為常見。</span><span class="sxs-lookup"><span data-stu-id="bfd7e-123">It is more typical to let the render engine build the graph for you, by calling the [**IRenderEngine::ConnectFrontEnd**](irenderengine-connectfrontend.md) method.</span></span>

<span data-ttu-id="bfd7e-124">如果轉譯引擎已經有篩選圖形，則這個方法會失敗。</span><span class="sxs-lookup"><span data-stu-id="bfd7e-124">This method fails if the render engine already has a filter graph.</span></span>

<span data-ttu-id="bfd7e-125">絕對不要取出某個轉譯引擎所建立之篩選圖形的指標，然後在另一個轉譯引擎上使用它做為此方法的參數。</span><span class="sxs-lookup"><span data-stu-id="bfd7e-125">Never retrieve a pointer to a filter graph created by one render engine and then use it as the parameter to this method on another render engine.</span></span> <span data-ttu-id="bfd7e-126">這麼做會導致無法預期的結果。</span><span class="sxs-lookup"><span data-stu-id="bfd7e-126">Doing so will cause unpredictable results.</span></span>

<span data-ttu-id="bfd7e-127">**ConnectFrontEnd** 方法會眼淚任何現有的篩選圖形，但會保留相同的篩選圖形管理員實例。</span><span class="sxs-lookup"><span data-stu-id="bfd7e-127">The **ConnectFrontEnd** method tears down any existing filter graph, but keeps the same Filter Graph Manager instance.</span></span>

> [!Note]  
> <span data-ttu-id="bfd7e-128">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="bfd7e-128">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="bfd7e-129">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="bfd7e-129">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="bfd7e-130">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="bfd7e-130">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="bfd7e-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="bfd7e-131">Requirements</span></span>



| <span data-ttu-id="bfd7e-132">需求</span><span class="sxs-lookup"><span data-stu-id="bfd7e-132">Requirement</span></span> | <span data-ttu-id="bfd7e-133">值</span><span class="sxs-lookup"><span data-stu-id="bfd7e-133">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bfd7e-134">標頭</span><span class="sxs-lookup"><span data-stu-id="bfd7e-134">Header</span></span><br/>  | <dl> <span data-ttu-id="bfd7e-135"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="bfd7e-135"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="bfd7e-136">程式庫</span><span class="sxs-lookup"><span data-stu-id="bfd7e-136">Library</span></span><br/> | <dl> <span data-ttu-id="bfd7e-137"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="bfd7e-137"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bfd7e-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bfd7e-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bfd7e-139">**IRenderEngine 介面**</span><span class="sxs-lookup"><span data-stu-id="bfd7e-139">**IRenderEngine Interface**</span></span>](irenderengine.md)
</dt> <dt>

[<span data-ttu-id="bfd7e-140">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="bfd7e-140">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




