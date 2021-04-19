---
description: ConnectFrontEnd 方法會從目前的時間軸建立篩選圖形的前端。
ms.assetid: ac484fd6-b88d-4c3a-bc4d-f118083d706d
title: 'IRenderEngine：： ConnectFrontEnd 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.ConnectFrontEnd
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 58ebd8e162f376b6ef942397e601139c46d8e4cf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987864"
---
# <a name="irenderengineconnectfrontend-method"></a><span data-ttu-id="4c43d-103">IRenderEngine：： ConnectFrontEnd 方法</span><span class="sxs-lookup"><span data-stu-id="4c43d-103">IRenderEngine::ConnectFrontEnd method</span></span>

> [!Note]  
> <span data-ttu-id="4c43d-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="4c43d-104">\[Deprecated.</span></span> <span data-ttu-id="4c43d-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="4c43d-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="4c43d-106">`ConnectFrontEnd`方法會從目前的時間軸建立篩選圖形的前端。</span><span class="sxs-lookup"><span data-stu-id="4c43d-106">The `ConnectFrontEnd` method builds the front end of the filter graph from the current timeline.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c43d-107">語法</span><span class="sxs-lookup"><span data-stu-id="4c43d-107">Syntax</span></span>


```C++
HRESULT ConnectFrontEnd();
```



## <a name="parameters"></a><span data-ttu-id="4c43d-108">參數</span><span class="sxs-lookup"><span data-stu-id="4c43d-108">Parameters</span></span>

<span data-ttu-id="4c43d-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="4c43d-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4c43d-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="4c43d-110">Return value</span></span>

<span data-ttu-id="4c43d-111">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="4c43d-111">Returns an **HRESULT** value.</span></span> <span data-ttu-id="4c43d-112">可能的傳回值包括下列各項：</span><span class="sxs-lookup"><span data-stu-id="4c43d-112">Possible return values include the following:</span></span>



| <span data-ttu-id="4c43d-113">傳回碼</span><span class="sxs-lookup"><span data-stu-id="4c43d-113">Return code</span></span>                                                                                                  | <span data-ttu-id="4c43d-114">Description</span><span class="sxs-lookup"><span data-stu-id="4c43d-114">Description</span></span>                                                                    |
|--------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4c43d-115"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="4c43d-115"><dt>**S\_OK**</dt></span></span> </dl>                         | <span data-ttu-id="4c43d-116">成功。</span><span class="sxs-lookup"><span data-stu-id="4c43d-116">Success.</span></span><br/>                                                            |
| <dl> <span data-ttu-id="4c43d-117"><dt>**S \_ 警告 \_ OUTPUTRESET**</dt></span><span class="sxs-lookup"><span data-stu-id="4c43d-117"><dt>**S\_WARN\_OUTPUTRESET**</dt></span></span> </dl>          | <span data-ttu-id="4c43d-118">已刪除圖形的轉譯部分。</span><span class="sxs-lookup"><span data-stu-id="4c43d-118">Rendering portion of the graph was deleted.</span></span><br/>                         |
| <dl> <span data-ttu-id="4c43d-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="4c43d-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl>                 | <span data-ttu-id="4c43d-120">未設定此轉譯引擎的時間軸。</span><span class="sxs-lookup"><span data-stu-id="4c43d-120">No timeline set for this render engine.</span></span><br/>                             |
| <dl> <span data-ttu-id="4c43d-121"><dt>**E \_ 必須 \_ INIT 轉譯器 \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4c43d-121"><dt>**E\_MUST\_INIT\_RENDERER**</dt></span></span> </dl>       | <span data-ttu-id="4c43d-122">轉譯引擎無法初始化。</span><span class="sxs-lookup"><span data-stu-id="4c43d-122">Render engine failed to initialize.</span></span><br/>                                 |
| <dl> <span data-ttu-id="4c43d-123"><dt>**E \_ 轉譯 \_ 引擎 \_ 已 \_ 中斷**</dt></span><span class="sxs-lookup"><span data-stu-id="4c43d-123"><dt>**E\_RENDER\_ENGINE\_IS\_BROKEN**</dt></span></span> </dl> | <span data-ttu-id="4c43d-124">因為未成功轉譯專案，所以作業失敗。</span><span class="sxs-lookup"><span data-stu-id="4c43d-124">Operation failed because the project was not rendered successfully.</span></span><br/> |
| <dl> <span data-ttu-id="4c43d-125"><dt>**E 未 \_ 預期**</dt></span><span class="sxs-lookup"><span data-stu-id="4c43d-125"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>                 | <span data-ttu-id="4c43d-126">非預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="4c43d-126">Unexpected error.</span></span><br/>                                                   |
| <dl> <span data-ttu-id="4c43d-127"><dt>**VFW \_ E \_ INVALIDMEDIATYPE**</dt></span><span class="sxs-lookup"><span data-stu-id="4c43d-127"><dt>**VFW\_E\_INVALIDMEDIATYPE**</dt></span></span> </dl>      | <span data-ttu-id="4c43d-128">媒體類型無效。</span><span class="sxs-lookup"><span data-stu-id="4c43d-128">Invalid media type.</span></span><br/>                                                 |



 

## <a name="remarks"></a><span data-ttu-id="4c43d-129">備註</span><span class="sxs-lookup"><span data-stu-id="4c43d-129">Remarks</span></span>

<span data-ttu-id="4c43d-130">這個方法不會建立篩選圖形的呈現部分。</span><span class="sxs-lookup"><span data-stu-id="4c43d-130">This method does not build the rendering portion of the filter graph.</span></span> <span data-ttu-id="4c43d-131">應用程式必須將前端的輸出圖釘連接到所需的轉譯篩選器：</span><span class="sxs-lookup"><span data-stu-id="4c43d-131">The application must connect the output pins on the front end to the desired rendering filters:</span></span>

-   <span data-ttu-id="4c43d-132">若要預覽，請呼叫 [**IRenderEngine：： RenderOutputPins**](irenderengine-renderoutputpins.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="4c43d-132">To preview, call the [**IRenderEngine::RenderOutputPins**](irenderengine-renderoutputpins.md) method.</span></span>
-   <span data-ttu-id="4c43d-133">若要輸出檔案，請呼叫 [**IRenderEngine：： GetGroupOutputPin**](irenderengine-getgroupoutputpin.md) 來取得每個群組的輸出針腳，然後將這些釘選到多工器篩選器。</span><span class="sxs-lookup"><span data-stu-id="4c43d-133">To output a file, call [**IRenderEngine::GetGroupOutputPin**](irenderengine-getgroupoutputpin.md) to retrieve the output pin for each group, then connect the pins to a multiplexer filter.</span></span>

<span data-ttu-id="4c43d-134">如果您使用的是基本轉譯引擎，前端的輸出圖釘會產生未壓縮的資料。</span><span class="sxs-lookup"><span data-stu-id="4c43d-134">If you are using the basic render engine, the output pins on the front end produce uncompressed data.</span></span> <span data-ttu-id="4c43d-135">如果您使用智慧型轉譯引擎，輸出圖釘會產生壓縮的資料。</span><span class="sxs-lookup"><span data-stu-id="4c43d-135">If you are using the smart render engine, the output pins produce compressed data.</span></span>

<span data-ttu-id="4c43d-136">如果您在建立篩選圖形之後變更時間軸，則必須再次呼叫 `ConnectFrontEnd` 以重建前端。</span><span class="sxs-lookup"><span data-stu-id="4c43d-136">If you change the timeline after you build the filter graph, you must call `ConnectFrontEnd` again to rebuild the front end.</span></span> <span data-ttu-id="4c43d-137">方法會盡可能保留圖形的呈現部分。</span><span class="sxs-lookup"><span data-stu-id="4c43d-137">The method preserves the rendering portion of the graph whenever possible.</span></span> <span data-ttu-id="4c43d-138">但是，如果您新增或刪除群組，或是變更群組的順序，就 `ConnectFrontEnd` 會刪除轉譯部分，而您的應用程式必須重建。</span><span class="sxs-lookup"><span data-stu-id="4c43d-138">However, if you add or delete a group, or change the order of the groups, `ConnectFrontEnd` deletes the rendering portion and your application must rebuild it.</span></span> <span data-ttu-id="4c43d-139">如果方法刪除了轉譯部分，則會傳回 S \_ 警告 \_ OUTPUTRESET。</span><span class="sxs-lookup"><span data-stu-id="4c43d-139">If the method deletes the rendering portion, it returns S\_WARN\_OUTPUTRESET.</span></span>

> [!Note]  
> <span data-ttu-id="4c43d-140">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="4c43d-140">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="4c43d-141">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="4c43d-141">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="4c43d-142">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="4c43d-142">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4c43d-143">規格需求</span><span class="sxs-lookup"><span data-stu-id="4c43d-143">Requirements</span></span>



| <span data-ttu-id="4c43d-144">需求</span><span class="sxs-lookup"><span data-stu-id="4c43d-144">Requirement</span></span> | <span data-ttu-id="4c43d-145">值</span><span class="sxs-lookup"><span data-stu-id="4c43d-145">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4c43d-146">標頭</span><span class="sxs-lookup"><span data-stu-id="4c43d-146">Header</span></span><br/>  | <dl> <span data-ttu-id="4c43d-147"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="4c43d-147"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="4c43d-148">程式庫</span><span class="sxs-lookup"><span data-stu-id="4c43d-148">Library</span></span><br/> | <dl> <span data-ttu-id="4c43d-149"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="4c43d-149"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c43d-150">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4c43d-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c43d-151">**IRenderEngine 介面**</span><span class="sxs-lookup"><span data-stu-id="4c43d-151">**IRenderEngine Interface**</span></span>](irenderengine.md)
</dt> <dt>

[<span data-ttu-id="4c43d-152">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="4c43d-152">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




