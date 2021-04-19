---
description: RenderOutputPins 方法會建立篩選圖形的預覽部分。
ms.assetid: 66bcb698-cd85-4c22-bfef-2e51973958f1
title: 'IRenderEngine：： RenderOutputPins 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.RenderOutputPins
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e7356df1bb79aa3b1901ee6d3de22510a6df1a9a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994798"
---
# <a name="irenderenginerenderoutputpins-method"></a><span data-ttu-id="e48df-103">IRenderEngine：： RenderOutputPins 方法</span><span class="sxs-lookup"><span data-stu-id="e48df-103">IRenderEngine::RenderOutputPins method</span></span>

> [!Note]  
> <span data-ttu-id="e48df-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="e48df-104">\[Deprecated.</span></span> <span data-ttu-id="e48df-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="e48df-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="e48df-106">`RenderOutputPins`方法會建立篩選圖形的預覽部分。</span><span class="sxs-lookup"><span data-stu-id="e48df-106">The `RenderOutputPins` method creates the previewing portion of the filter graph.</span></span>

## <a name="syntax"></a><span data-ttu-id="e48df-107">語法</span><span class="sxs-lookup"><span data-stu-id="e48df-107">Syntax</span></span>


```C++
HRESULT RenderOutputPins();
```



## <a name="parameters"></a><span data-ttu-id="e48df-108">參數</span><span class="sxs-lookup"><span data-stu-id="e48df-108">Parameters</span></span>

<span data-ttu-id="e48df-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="e48df-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e48df-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="e48df-110">Return value</span></span>

<span data-ttu-id="e48df-111">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="e48df-111">Returns an **HRESULT** values.</span></span> <span data-ttu-id="e48df-112">以下是可能的值：</span><span class="sxs-lookup"><span data-stu-id="e48df-112">The following are possible values:</span></span>



| <span data-ttu-id="e48df-113">傳回碼</span><span class="sxs-lookup"><span data-stu-id="e48df-113">Return code</span></span>                                                                                                  | <span data-ttu-id="e48df-114">Description</span><span class="sxs-lookup"><span data-stu-id="e48df-114">Description</span></span>                                                                |
|--------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e48df-115"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="e48df-115"><dt>**S\_OK**</dt></span></span> </dl>                         | <span data-ttu-id="e48df-116">成功。</span><span class="sxs-lookup"><span data-stu-id="e48df-116">Success.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="e48df-117"><dt>**未轉譯 VFW \_ S \_ 音訊 \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e48df-117"><dt>**VFW\_S\_AUDIO\_NOT\_RENDERED**</dt></span></span> </dl>  | <span data-ttu-id="e48df-118">無法播放音訊串流。</span><span class="sxs-lookup"><span data-stu-id="e48df-118">Cannot play back the audio stream.</span></span><br/>                              |
| <dl> <span data-ttu-id="e48df-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="e48df-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl>                 | <span data-ttu-id="e48df-120">無效引數。</span><span class="sxs-lookup"><span data-stu-id="e48df-120">Invalid argument.</span></span><br/>                                               |
| <dl> <span data-ttu-id="e48df-121"><dt>**E \_ 轉譯 \_ 引擎 \_ 已 \_ 中斷**</dt></span><span class="sxs-lookup"><span data-stu-id="e48df-121"><dt>**E\_RENDER\_ENGINE\_IS\_BROKEN**</dt></span></span> </dl> | <span data-ttu-id="e48df-122">因為未成功轉譯專案，所以操作失敗。</span><span class="sxs-lookup"><span data-stu-id="e48df-122">Operation failed because project was not rendered successfully.</span></span><br/> |
| <dl> <span data-ttu-id="e48df-123"><dt>**E 未 \_ 預期**</dt></span><span class="sxs-lookup"><span data-stu-id="e48df-123"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>                 | <span data-ttu-id="e48df-124">非預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="e48df-124">Unexpected error.</span></span><br/>                                               |



 

## <a name="remarks"></a><span data-ttu-id="e48df-125">備註</span><span class="sxs-lookup"><span data-stu-id="e48df-125">Remarks</span></span>

<span data-ttu-id="e48df-126">在呼叫這個方法之前，請先呼叫 [**IRenderEngine：： ConnectFrontEnd**](irenderengine-connectfrontend.md) 來建立圖形的前端。</span><span class="sxs-lookup"><span data-stu-id="e48df-126">Before calling this method, call [**IRenderEngine::ConnectFrontEnd**](irenderengine-connectfrontend.md) to build the front end of the graph.</span></span> <span data-ttu-id="e48df-127">若要執行預覽以外的作業，請不要呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="e48df-127">To perform an operation other than preview, do not call this method.</span></span> <span data-ttu-id="e48df-128">請改為呼叫 [**IRenderEngine：： GetGroupOutputPin**](irenderengine-getgroupoutputpin.md) 來取得輸出圖釘的指標。</span><span class="sxs-lookup"><span data-stu-id="e48df-128">Instead, call [**IRenderEngine::GetGroupOutputPin**](irenderengine-getgroupoutputpin.md) to obtain pointers to the output pins.</span></span>

<span data-ttu-id="e48df-129">如果使用者的電腦上沒有音效卡，這個方法會傳回未轉譯的 VFW \_ s \_ 音訊 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="e48df-129">If there is no sound card on the user's computer, this method returns VFW\_S\_AUDIO\_NOT\_RENDERED.</span></span> <span data-ttu-id="e48df-130">在此情況下，將不會有音訊預覽，但影片預覽不會受到影響。</span><span class="sxs-lookup"><span data-stu-id="e48df-130">There will not be audio preview in this case, but video preview is unaffected.</span></span>

<span data-ttu-id="e48df-131">如果釘選來自影片群組，這個方法會建立影片視窗。</span><span class="sxs-lookup"><span data-stu-id="e48df-131">If the pin is from a video group, this method creates a video window.</span></span> <span data-ttu-id="e48df-132">呼叫執行緒必須分派訊息（例如，移動視窗），或在視窗的工作區中回應滑鼠點擊。</span><span class="sxs-lookup"><span data-stu-id="e48df-132">The calling thread must dispatch messages—for example, to move the window, or respond to mouse clicks in the window's client area.</span></span>

> [!Note]  
> <span data-ttu-id="e48df-133">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="e48df-133">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="e48df-134">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="e48df-134">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="e48df-135">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="e48df-135">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e48df-136">規格需求</span><span class="sxs-lookup"><span data-stu-id="e48df-136">Requirements</span></span>



| <span data-ttu-id="e48df-137">需求</span><span class="sxs-lookup"><span data-stu-id="e48df-137">Requirement</span></span> | <span data-ttu-id="e48df-138">值</span><span class="sxs-lookup"><span data-stu-id="e48df-138">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e48df-139">標頭</span><span class="sxs-lookup"><span data-stu-id="e48df-139">Header</span></span><br/>  | <dl> <span data-ttu-id="e48df-140"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="e48df-140"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="e48df-141">程式庫</span><span class="sxs-lookup"><span data-stu-id="e48df-141">Library</span></span><br/> | <dl> <span data-ttu-id="e48df-142"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="e48df-142"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e48df-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e48df-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e48df-144">**IRenderEngine 介面**</span><span class="sxs-lookup"><span data-stu-id="e48df-144">**IRenderEngine Interface**</span></span>](irenderengine.md)
</dt> <dt>

[<span data-ttu-id="e48df-145">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="e48df-145">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




