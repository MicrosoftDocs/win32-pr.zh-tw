---
description: GetFilterGraph 方法會抓取轉譯引擎所建立的篩選圖形（如果有的話）。
ms.assetid: 509b2c9c-c21b-4855-880f-f09ad342e758
title: 'IRenderEngine：： GetFilterGraph 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.GetFilterGraph
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4c4750e6127c0d57758e46b2309f4d91afc110e0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983953"
---
# <a name="irenderenginegetfiltergraph-method"></a><span data-ttu-id="839d8-103">IRenderEngine：： GetFilterGraph 方法</span><span class="sxs-lookup"><span data-stu-id="839d8-103">IRenderEngine::GetFilterGraph method</span></span>

> [!Note]  
> <span data-ttu-id="839d8-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="839d8-104">\[Deprecated.</span></span> <span data-ttu-id="839d8-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="839d8-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="839d8-106">方法會抓取轉譯引擎所建立的 `GetFilterGraph` 篩選圖形（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="839d8-106">The `GetFilterGraph` method retrieves the filter graph that the render engine has constructed, if any.</span></span>

## <a name="syntax"></a><span data-ttu-id="839d8-107">語法</span><span class="sxs-lookup"><span data-stu-id="839d8-107">Syntax</span></span>


```C++
HRESULT GetFilterGraph(
  [out] IGraphBuilder **ppFG
);
```



## <a name="parameters"></a><span data-ttu-id="839d8-108">參數</span><span class="sxs-lookup"><span data-stu-id="839d8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="839d8-109">*ppFG* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="839d8-109">*ppFG* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="839d8-110">接收篩選圖形的 [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) 介面指標。</span><span class="sxs-lookup"><span data-stu-id="839d8-110">Receives a pointer to the filter graph's [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) interface.</span></span> <span data-ttu-id="839d8-111">如果沒有篩選圖形，則會接收 **Null** 值。</span><span class="sxs-lookup"><span data-stu-id="839d8-111">It receives the value **NULL** if there is no filter graph.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="839d8-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="839d8-112">Return value</span></span>

<span data-ttu-id="839d8-113">傳回下列其中一個 **HRESULT** 值：</span><span class="sxs-lookup"><span data-stu-id="839d8-113">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="839d8-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="839d8-114">Return code</span></span>                                                                                            | <span data-ttu-id="839d8-115">Description</span><span class="sxs-lookup"><span data-stu-id="839d8-115">Description</span></span>                                    |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="839d8-116"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="839d8-116"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="839d8-117">成功。</span><span class="sxs-lookup"><span data-stu-id="839d8-117">Success.</span></span><br/>                            |
| <dl> <span data-ttu-id="839d8-118"><dt>**E \_ 必須 \_ INIT 轉譯器 \_**</dt></span><span class="sxs-lookup"><span data-stu-id="839d8-118"><dt>**E\_MUST\_INIT\_RENDERER**</dt></span></span> </dl> | <span data-ttu-id="839d8-119">轉譯引擎無法初始化。</span><span class="sxs-lookup"><span data-stu-id="839d8-119">Render engine failed to initialize.</span></span><br/> |
| <dl> <span data-ttu-id="839d8-120"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="839d8-120"><dt>**E\_POINTER**</dt></span></span> </dl>              | <span data-ttu-id="839d8-121">指標無效。</span><span class="sxs-lookup"><span data-stu-id="839d8-121">Invalid pointer.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="839d8-122">備註</span><span class="sxs-lookup"><span data-stu-id="839d8-122">Remarks</span></span>

<span data-ttu-id="839d8-123">使用 [**IRenderEngine：： ConnectFrontEnd**](irenderengine-connectfrontend.md) 方法來建立篩選圖形的前端。</span><span class="sxs-lookup"><span data-stu-id="839d8-123">Use the [**IRenderEngine::ConnectFrontEnd**](irenderengine-connectfrontend.md) method to build the front end of the filter graph.</span></span> <span data-ttu-id="839d8-124">若為預覽版本，請使用 [**IRenderEngine：： RenderOutputPins**](irenderengine-renderoutputpins.md) 來完成圖形。</span><span class="sxs-lookup"><span data-stu-id="839d8-124">For preview, use the [**IRenderEngine::RenderOutputPins**](irenderengine-renderoutputpins.md) to complete the graph.</span></span> <span data-ttu-id="839d8-125">針對檔案輸出，將前端連接至 mux/檔案寫入器組合。</span><span class="sxs-lookup"><span data-stu-id="839d8-125">For file output, connect the front end to a mux/file writer combination.</span></span> <span data-ttu-id="839d8-126">如需詳細資訊，請參閱 [呈現專案](rendering-a-project.md)。</span><span class="sxs-lookup"><span data-stu-id="839d8-126">For more information, see [Rendering a Project](rendering-a-project.md).</span></span>

<span data-ttu-id="839d8-127">產生的圖形可以執行、暫停、停止和 seeked;不過，播放速率無法變更。</span><span class="sxs-lookup"><span data-stu-id="839d8-127">The resulting graph can be run, paused, stopped, and seeked; the playback rate cannot be changed, however.</span></span>

<span data-ttu-id="839d8-128">傳回時，如果 *\* ppFG* 的值為非 **Null**，則 **IGraphBuilder** 介面具有未處理的參考計數。</span><span class="sxs-lookup"><span data-stu-id="839d8-128">On return, if the value of *\*ppFG* is non-**NULL**, the **IGraphBuilder** interface has an outstanding reference count.</span></span> <span data-ttu-id="839d8-129">使用完畢後，請務必釋放介面。</span><span class="sxs-lookup"><span data-stu-id="839d8-129">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="839d8-130">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="839d8-130">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="839d8-131">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="839d8-131">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="839d8-132">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="839d8-132">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="839d8-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="839d8-133">Requirements</span></span>



| <span data-ttu-id="839d8-134">需求</span><span class="sxs-lookup"><span data-stu-id="839d8-134">Requirement</span></span> | <span data-ttu-id="839d8-135">值</span><span class="sxs-lookup"><span data-stu-id="839d8-135">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="839d8-136">標頭</span><span class="sxs-lookup"><span data-stu-id="839d8-136">Header</span></span><br/>  | <dl> <span data-ttu-id="839d8-137"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="839d8-137"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="839d8-138">程式庫</span><span class="sxs-lookup"><span data-stu-id="839d8-138">Library</span></span><br/> | <dl> <span data-ttu-id="839d8-139"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="839d8-139"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="839d8-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="839d8-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="839d8-141">**IRenderEngine 介面**</span><span class="sxs-lookup"><span data-stu-id="839d8-141">**IRenderEngine Interface**</span></span>](irenderengine.md)
</dt> <dt>

[<span data-ttu-id="839d8-142">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="839d8-142">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




