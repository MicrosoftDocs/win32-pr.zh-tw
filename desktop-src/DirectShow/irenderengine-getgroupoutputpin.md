---
description: GetGroupOutputPin 方法會抓取指定群組的輸出圖釘。
ms.assetid: be4e17b6-15bf-43b1-8d93-d52d08c8bce6
title: 'IRenderEngine：： GetGroupOutputPin 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.GetGroupOutputPin
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 21e603e15f598c6d493e179a147391cb941a6c7c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990721"
---
# <a name="irenderenginegetgroupoutputpin-method"></a><span data-ttu-id="4a2e0-103">IRenderEngine：： GetGroupOutputPin 方法</span><span class="sxs-lookup"><span data-stu-id="4a2e0-103">IRenderEngine::GetGroupOutputPin method</span></span>

> [!Note]  
> <span data-ttu-id="4a2e0-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="4a2e0-104">\[Deprecated.</span></span> <span data-ttu-id="4a2e0-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="4a2e0-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="4a2e0-106">方法會抓取 `GetGroupOutputPin` 指定群組的輸出圖釘。</span><span class="sxs-lookup"><span data-stu-id="4a2e0-106">The `GetGroupOutputPin` method retrieves the output pin for the specified group.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a2e0-107">語法</span><span class="sxs-lookup"><span data-stu-id="4a2e0-107">Syntax</span></span>


```C++
HRESULT GetGroupOutputPin(
        long Group,
  [out] IPin **ppRenderPin
);
```



## <a name="parameters"></a><span data-ttu-id="4a2e0-108">參數</span><span class="sxs-lookup"><span data-stu-id="4a2e0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a2e0-109">*群組*</span><span class="sxs-lookup"><span data-stu-id="4a2e0-109">*Group*</span></span> 
</dt> <dd>

<span data-ttu-id="4a2e0-110">以零為基底的索引，可指定群組。</span><span class="sxs-lookup"><span data-stu-id="4a2e0-110">Zero-based index that specifies the group.</span></span>

</dd> <dt>

<span data-ttu-id="4a2e0-111">*ppRenderPin* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="4a2e0-111">*ppRenderPin* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4a2e0-112">接收輸出釘選 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="4a2e0-112">Receives a pointer to the output pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a2e0-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="4a2e0-113">Return value</span></span>

<span data-ttu-id="4a2e0-114">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="4a2e0-114">Returns an **HRESULT** value.</span></span> <span data-ttu-id="4a2e0-115">可能的值如下：</span><span class="sxs-lookup"><span data-stu-id="4a2e0-115">Possible values include the following:</span></span>



| <span data-ttu-id="4a2e0-116">傳回碼</span><span class="sxs-lookup"><span data-stu-id="4a2e0-116">Return code</span></span>                                                                                                  | <span data-ttu-id="4a2e0-117">Description</span><span class="sxs-lookup"><span data-stu-id="4a2e0-117">Description</span></span>                                                                |
|--------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4a2e0-118"><dt>**S \_ FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="4a2e0-118"><dt>**S\_FALSE**</dt></span></span> </dl>                      | <span data-ttu-id="4a2e0-119">群組沒有輸出圖釘。</span><span class="sxs-lookup"><span data-stu-id="4a2e0-119">Group does not have an output pin.</span></span><br/>                              |
| <dl> <span data-ttu-id="4a2e0-120"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="4a2e0-120"><dt>**S\_OK**</dt></span></span> </dl>                         | <span data-ttu-id="4a2e0-121">成功。</span><span class="sxs-lookup"><span data-stu-id="4a2e0-121">Success.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="4a2e0-122"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="4a2e0-122"><dt>**E\_INVALIDARG**</dt></span></span> </dl>                 | <span data-ttu-id="4a2e0-123">無效引數。</span><span class="sxs-lookup"><span data-stu-id="4a2e0-123">Invalid argument.</span></span><br/>                                               |
| <dl> <span data-ttu-id="4a2e0-124"><dt>**E \_ 必須 \_ INIT 轉譯器 \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4a2e0-124"><dt>**E\_MUST\_INIT\_RENDERER**</dt></span></span> </dl>       | <span data-ttu-id="4a2e0-125">轉譯引擎無法初始化。</span><span class="sxs-lookup"><span data-stu-id="4a2e0-125">Render engine failed to initialize.</span></span><br/>                             |
| <dl> <span data-ttu-id="4a2e0-126"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="4a2e0-126"><dt>**E\_POINTER**</dt></span></span> </dl>                    | <span data-ttu-id="4a2e0-127">指標無效。</span><span class="sxs-lookup"><span data-stu-id="4a2e0-127">Invalid pointer.</span></span><br/>                                                |
| <dl> <span data-ttu-id="4a2e0-128"><dt>**E \_ 轉譯 \_ 引擎 \_ 已 \_ 中斷**</dt></span><span class="sxs-lookup"><span data-stu-id="4a2e0-128"><dt>**E\_RENDER\_ENGINE\_IS\_BROKEN**</dt></span></span> </dl> | <span data-ttu-id="4a2e0-129">因為未成功轉譯專案，所以操作失敗。</span><span class="sxs-lookup"><span data-stu-id="4a2e0-129">Operation failed because project was not rendered successfully.</span></span><br/> |
| <dl> <span data-ttu-id="4a2e0-130"><dt>**E 未 \_ 預期**</dt></span><span class="sxs-lookup"><span data-stu-id="4a2e0-130"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>                 | <span data-ttu-id="4a2e0-131">非預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="4a2e0-131">Unexpected error.</span></span><br/>                                               |



 

## <a name="remarks"></a><span data-ttu-id="4a2e0-132">備註</span><span class="sxs-lookup"><span data-stu-id="4a2e0-132">Remarks</span></span>

<span data-ttu-id="4a2e0-133">在呼叫這個方法之前，請先呼叫 [**IRenderEngine：： ConnectFrontEnd**](irenderengine-connectfrontend.md) 來建立圖形的前端。</span><span class="sxs-lookup"><span data-stu-id="4a2e0-133">Before calling this method, call [**IRenderEngine::ConnectFrontEnd**](irenderengine-connectfrontend.md) to build the front end of the graph.</span></span> <span data-ttu-id="4a2e0-134">每個群組都代表一個媒體資料流程，而前端則有對應的輸出圖釘。</span><span class="sxs-lookup"><span data-stu-id="4a2e0-134">Each group represents a single media stream, and the front end has a corresponding output pin.</span></span>

<span data-ttu-id="4a2e0-135">您可以使用這個方法來建立檔案寫入圖形的轉譯部分。</span><span class="sxs-lookup"><span data-stu-id="4a2e0-135">You can use this method to create the rendering portion of a file-writing graph.</span></span> <span data-ttu-id="4a2e0-136">將輸出圖釘連接到多工器篩選器和檔案寫入器篩選器。</span><span class="sxs-lookup"><span data-stu-id="4a2e0-136">Connect the output pins to multiplexer filters and file writer filters.</span></span> <span data-ttu-id="4a2e0-137">如需詳細資訊，請參閱 [呈現專案](rendering-a-project.md)。</span><span class="sxs-lookup"><span data-stu-id="4a2e0-137">For more information, see [Rendering a Project](rendering-a-project.md).</span></span>

<span data-ttu-id="4a2e0-138">若為預覽版本，您不需要呼叫此方法。</span><span class="sxs-lookup"><span data-stu-id="4a2e0-138">For preview, you don't need to call this method.</span></span> <span data-ttu-id="4a2e0-139">只要呼叫 **ConnectFrontEnd** ，然後再呼叫 [**IRenderEngine：： RenderOutputPins**](irenderengine-renderoutputpins.md)。</span><span class="sxs-lookup"><span data-stu-id="4a2e0-139">Just call **ConnectFrontEnd** followed by [**IRenderEngine::RenderOutputPins**](irenderengine-renderoutputpins.md).</span></span>

<span data-ttu-id="4a2e0-140">如果方法傳回 S \_ OK，則傳回的 **IPin** 介面具有未處理的參考計數。</span><span class="sxs-lookup"><span data-stu-id="4a2e0-140">If the method returns S\_OK, the **IPin** interface that it returns has an outstanding reference count.</span></span> <span data-ttu-id="4a2e0-141">使用完畢後，請務必釋放介面。</span><span class="sxs-lookup"><span data-stu-id="4a2e0-141">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="4a2e0-142">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="4a2e0-142">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="4a2e0-143">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="4a2e0-143">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="4a2e0-144">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="4a2e0-144">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4a2e0-145">規格需求</span><span class="sxs-lookup"><span data-stu-id="4a2e0-145">Requirements</span></span>



| <span data-ttu-id="4a2e0-146">需求</span><span class="sxs-lookup"><span data-stu-id="4a2e0-146">Requirement</span></span> | <span data-ttu-id="4a2e0-147">值</span><span class="sxs-lookup"><span data-stu-id="4a2e0-147">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4a2e0-148">標頭</span><span class="sxs-lookup"><span data-stu-id="4a2e0-148">Header</span></span><br/>  | <dl> <span data-ttu-id="4a2e0-149"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="4a2e0-149"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="4a2e0-150">程式庫</span><span class="sxs-lookup"><span data-stu-id="4a2e0-150">Library</span></span><br/> | <dl> <span data-ttu-id="4a2e0-151"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="4a2e0-151"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a2e0-152">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4a2e0-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a2e0-153">**IRenderEngine 介面**</span><span class="sxs-lookup"><span data-stu-id="4a2e0-153">**IRenderEngine Interface**</span></span>](irenderengine.md)
</dt> <dt>

[<span data-ttu-id="4a2e0-154">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="4a2e0-154">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




