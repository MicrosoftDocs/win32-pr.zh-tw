---
description: IRenderEngine 介面會將 DirectShow 編輯服務 (DES) 專案中，藉由從時間軸建立篩選圖形來呈現。DES 提供兩個可執行此介面的元件：基本轉譯引擎會建立未壓縮的輸出。
ms.assetid: e2a91b34-ee4d-405e-81bf-29d15ea6342a
title: 'IRenderEngine 介面 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: d8c57e976fac877a02c3f3993fb3fe4d27f9033b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106980207"
---
# <a name="irenderengine-interface"></a><span data-ttu-id="b5c67-103">IRenderEngine 介面</span><span class="sxs-lookup"><span data-stu-id="b5c67-103">IRenderEngine interface</span></span>

> [!Note]  
> <span data-ttu-id="b5c67-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="b5c67-104">\[Deprecated.</span></span> <span data-ttu-id="b5c67-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="b5c67-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="b5c67-106">介面會藉 `IRenderEngine` 由從時間軸建立篩選圖形， (DES) 專案呈現 [DirectShow 編輯服務](directshow-editing-services.md) 。</span><span class="sxs-lookup"><span data-stu-id="b5c67-106">The `IRenderEngine` interface renders a [DirectShow Editing Services](directshow-editing-services.md) (DES) project by constructing a filter graph from a timeline.</span></span>

<span data-ttu-id="b5c67-107">DES 提供兩個可執行此介面的元件：</span><span class="sxs-lookup"><span data-stu-id="b5c67-107">DES provides two components that implement this interface:</span></span>

-   <span data-ttu-id="b5c67-108">*基本轉譯引擎* 會建立未壓縮的輸出。</span><span class="sxs-lookup"><span data-stu-id="b5c67-108">The *basic render engine* creates uncompressed output.</span></span> <span data-ttu-id="b5c67-109">您可以使用預覽的輸出，或透過壓縮篩選將其傳送至檔案，並將其寫入檔案。</span><span class="sxs-lookup"><span data-stu-id="b5c67-109">You can use the output for preview, or route it through compression filters and write it to a file.</span></span>
-   <span data-ttu-id="b5c67-110">*智慧型轉譯引擎* 會使用 *智慧型 recompression* 來建立壓縮的輸出。</span><span class="sxs-lookup"><span data-stu-id="b5c67-110">The *smart render engine* creates compressed output, using *smart recompression*.</span></span> <span data-ttu-id="b5c67-111">使用智慧型 recompression 時，只有當原始程式檔的格式與輸出格式不同時，才會 recompressed 原始程式檔。</span><span class="sxs-lookup"><span data-stu-id="b5c67-111">With smart recompression, a source file is recompressed only if its format differs from the output format.</span></span> <span data-ttu-id="b5c67-112">具有相符格式的來源會直接寫入輸出檔。</span><span class="sxs-lookup"><span data-stu-id="b5c67-112">A source with a matching format is written directly to the output file.</span></span> <span data-ttu-id="b5c67-113">根據案例而定，智慧型 recompression 可以大幅改善轉譯時間。</span><span class="sxs-lookup"><span data-stu-id="b5c67-113">Depending on the scenario, smart recompression can greatly improve rendering time.</span></span>

<span data-ttu-id="b5c67-114">智慧型轉譯引擎也支援 [**ISmartRenderEngine**](ismartrenderengine.md) 介面。</span><span class="sxs-lookup"><span data-stu-id="b5c67-114">The smart render engine also supports the [**ISmartRenderEngine**](ismartrenderengine.md) interface.</span></span>

<span data-ttu-id="b5c67-115">雖然應用程式可以建立篩選圖形並將它傳遞至轉譯引擎，但一般案例是讓轉譯引擎建立篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="b5c67-115">Although an application can create a filter graph and pass it to a render engine, the typical scenario is for the render engine to create the filter graph.</span></span> <span data-ttu-id="b5c67-116">建立圖形是兩階段的流程。</span><span class="sxs-lookup"><span data-stu-id="b5c67-116">Building the graph is a two-stage process.</span></span> <span data-ttu-id="b5c67-117">首先，藉由呼叫 [**IRenderEngine：： ConnectFrontEnd**](irenderengine-connectfrontend.md) 方法來建立前端。</span><span class="sxs-lookup"><span data-stu-id="b5c67-117">First, build the front end by calling the [**IRenderEngine::ConnectFrontEnd**](irenderengine-connectfrontend.md) method.</span></span> <span data-ttu-id="b5c67-118">然後將前端的輸出接點連接到所需的轉譯篩選準則：</span><span class="sxs-lookup"><span data-stu-id="b5c67-118">Then connect the output pins on the front end to the desired rendering filters:</span></span>

-   <span data-ttu-id="b5c67-119">適用于預覽的影片和音訊轉譯器，或</span><span class="sxs-lookup"><span data-stu-id="b5c67-119">Video and audio renderers for preview, or</span></span>
-   <span data-ttu-id="b5c67-120">壓縮機、multiplexers 和 file 寫入器，以產生最終輸出。</span><span class="sxs-lookup"><span data-stu-id="b5c67-120">Compressors, multiplexers, and file writers to generate the final output.</span></span>

## <a name="members"></a><span data-ttu-id="b5c67-121">成員</span><span class="sxs-lookup"><span data-stu-id="b5c67-121">Members</span></span>

<span data-ttu-id="b5c67-122">**IRenderEngine** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="b5c67-122">The **IRenderEngine** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="b5c67-123">**IRenderEngine** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="b5c67-123">**IRenderEngine** also has these types of members:</span></span>

-   [<span data-ttu-id="b5c67-124">方法</span><span class="sxs-lookup"><span data-stu-id="b5c67-124">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="b5c67-125">方法</span><span class="sxs-lookup"><span data-stu-id="b5c67-125">Methods</span></span>

<span data-ttu-id="b5c67-126">**IRenderEngine** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="b5c67-126">The **IRenderEngine** interface has these methods.</span></span>



| <span data-ttu-id="b5c67-127">方法</span><span class="sxs-lookup"><span data-stu-id="b5c67-127">Method</span></span>                                                                             | <span data-ttu-id="b5c67-128">描述</span><span class="sxs-lookup"><span data-stu-id="b5c67-128">Description</span></span>                                                                           |
|:-----------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------|
| [<span data-ttu-id="b5c67-129">**提交**</span><span class="sxs-lookup"><span data-stu-id="b5c67-129">**Commit**</span></span>](irenderengine-commit.md)                                             | <span data-ttu-id="b5c67-130">未實作。</span><span class="sxs-lookup"><span data-stu-id="b5c67-130">Not implemented.</span></span><br/>                                                           |
| [<span data-ttu-id="b5c67-131">**ConnectFrontEnd**</span><span class="sxs-lookup"><span data-stu-id="b5c67-131">**ConnectFrontEnd**</span></span>](irenderengine-connectfrontend.md)                           | <span data-ttu-id="b5c67-132">從目前的時間軸建立篩選圖形的前端。</span><span class="sxs-lookup"><span data-stu-id="b5c67-132">Builds the front end of the filter graph from the current timeline.</span></span><br/>        |
| [<span data-ttu-id="b5c67-133">**取消認可**</span><span class="sxs-lookup"><span data-stu-id="b5c67-133">**Decommit**</span></span>](irenderengine-decommit.md)                                         | <span data-ttu-id="b5c67-134">未實作。</span><span class="sxs-lookup"><span data-stu-id="b5c67-134">Not implemented.</span></span><br/>                                                           |
| [<span data-ttu-id="b5c67-135">**DoSmartRecompression**</span><span class="sxs-lookup"><span data-stu-id="b5c67-135">**DoSmartRecompression**</span></span>](irenderengine-dosmartrecompression.md)                 | <span data-ttu-id="b5c67-136">不支援。</span><span class="sxs-lookup"><span data-stu-id="b5c67-136">Not supported.</span></span><br/>                                                             |
| [<span data-ttu-id="b5c67-137">**GetCaps**</span><span class="sxs-lookup"><span data-stu-id="b5c67-137">**GetCaps**</span></span>](irenderengine-getcaps.md)                                           | <span data-ttu-id="b5c67-138">未實作。</span><span class="sxs-lookup"><span data-stu-id="b5c67-138">Not implemented.</span></span><br/>                                                           |
| [<span data-ttu-id="b5c67-139">**GetFilterGraph**</span><span class="sxs-lookup"><span data-stu-id="b5c67-139">**GetFilterGraph**</span></span>](irenderengine-getfiltergraph.md)                             | <span data-ttu-id="b5c67-140">抓取轉譯引擎已建立的篩選圖形（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="b5c67-140">Retrieves the filter graph that the render engine has constructed, if any.</span></span><br/> |
| [<span data-ttu-id="b5c67-141">**GetGroupOutputPin**</span><span class="sxs-lookup"><span data-stu-id="b5c67-141">**GetGroupOutputPin**</span></span>](irenderengine-getgroupoutputpin.md)                       | <span data-ttu-id="b5c67-142">抓取指定群組的輸出圖釘。</span><span class="sxs-lookup"><span data-stu-id="b5c67-142">Retrieves the output pin for the specified group.</span></span><br/>                          |
| [<span data-ttu-id="b5c67-143">**GetTimelineObject**</span><span class="sxs-lookup"><span data-stu-id="b5c67-143">**GetTimelineObject**</span></span>](irenderengine-gettimelineobject.md)                       | <span data-ttu-id="b5c67-144">抓取轉譯引擎目前使用的時間軸。</span><span class="sxs-lookup"><span data-stu-id="b5c67-144">Retrieves the timeline that the render engine is currently using.</span></span><br/>          |
| [<span data-ttu-id="b5c67-145">**GetVendorString**</span><span class="sxs-lookup"><span data-stu-id="b5c67-145">**GetVendorString**</span></span>](irenderengine-getvendorstring.md)                           | <span data-ttu-id="b5c67-146">捕獲廠商字串。</span><span class="sxs-lookup"><span data-stu-id="b5c67-146">Retrieves the vendor string.</span></span><br/>                                               |
| [<span data-ttu-id="b5c67-147">**RenderOutputPins**</span><span class="sxs-lookup"><span data-stu-id="b5c67-147">**RenderOutputPins**</span></span>](irenderengine-renderoutputpins.md)                         | <span data-ttu-id="b5c67-148">建立篩選圖形的預覽部分。</span><span class="sxs-lookup"><span data-stu-id="b5c67-148">Creates the previewing portion of the filter graph.</span></span><br/>                        |
| [<span data-ttu-id="b5c67-149">**ScrapIt**</span><span class="sxs-lookup"><span data-stu-id="b5c67-149">**ScrapIt**</span></span>](irenderengine-scrapit.md)                                           | <span data-ttu-id="b5c67-150">捨棄轉譯引擎的篩選圖形以及所有相關聯的物件。</span><span class="sxs-lookup"><span data-stu-id="b5c67-150">Discards the render engine's filter graph and all associated objects.</span></span><br/>      |
| [<span data-ttu-id="b5c67-151">**SetDynamicReconnectLevel**</span><span class="sxs-lookup"><span data-stu-id="b5c67-151">**SetDynamicReconnectLevel**</span></span>](irenderengine-setdynamicreconnectlevel.md)         | <span data-ttu-id="b5c67-152">設定轉譯期間的動態重新連接層級。</span><span class="sxs-lookup"><span data-stu-id="b5c67-152">Sets the level of dynamic reconnection during rendering.</span></span><br/>                   |
| [<span data-ttu-id="b5c67-153">**SetFilterGraph**</span><span class="sxs-lookup"><span data-stu-id="b5c67-153">**SetFilterGraph**</span></span>](irenderengine-setfiltergraph.md)                             | <span data-ttu-id="b5c67-154">指定要用於轉譯引擎的篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="b5c67-154">Specifies a filter graph for the render engine to use.</span></span><br/>                     |
| [<span data-ttu-id="b5c67-155">**SetInterestRange**</span><span class="sxs-lookup"><span data-stu-id="b5c67-155">**SetInterestRange**</span></span>](irenderengine-setinterestrange.md)                         | <span data-ttu-id="b5c67-156">不支援。</span><span class="sxs-lookup"><span data-stu-id="b5c67-156">Not supported.</span></span><br/>                                                             |
| [<span data-ttu-id="b5c67-157">**SetInterestRange2**</span><span class="sxs-lookup"><span data-stu-id="b5c67-157">**SetInterestRange2**</span></span>](irenderengine-setinterestrange2.md)                       | <span data-ttu-id="b5c67-158">不支援。</span><span class="sxs-lookup"><span data-stu-id="b5c67-158">Not supported.</span></span><br/>                                                             |
| [<span data-ttu-id="b5c67-159">**SetRenderRange**</span><span class="sxs-lookup"><span data-stu-id="b5c67-159">**SetRenderRange**</span></span>](irenderengine-setrenderrange.md)                             | <span data-ttu-id="b5c67-160">設定要轉譯的時間範圍。</span><span class="sxs-lookup"><span data-stu-id="b5c67-160">Sets the range of time to be rendered.</span></span><br/>                                     |
| [<span data-ttu-id="b5c67-161">**SetRenderRange2**</span><span class="sxs-lookup"><span data-stu-id="b5c67-161">**SetRenderRange2**</span></span>](irenderengine-setrenderrange2.md)                           | <span data-ttu-id="b5c67-162">設定要轉譯的時間範圍，以 **雙精度浮點數**。</span><span class="sxs-lookup"><span data-stu-id="b5c67-162">Sets the range of time to be rendered, as a **double**.</span></span><br/>                    |
| [<span data-ttu-id="b5c67-163">**SetSourceConnectCallback**</span><span class="sxs-lookup"><span data-stu-id="b5c67-163">**SetSourceConnectCallback**</span></span>](irenderengine-setsourceconnectcallback.md)         | <span data-ttu-id="b5c67-164">不支援。</span><span class="sxs-lookup"><span data-stu-id="b5c67-164">Not supported.</span></span><br/>                                                             |
| [<span data-ttu-id="b5c67-165">**SetSourceNameValidation**</span><span class="sxs-lookup"><span data-stu-id="b5c67-165">**SetSourceNameValidation**</span></span>](irenderengine-setsourcenamevalidation.md)           | <span data-ttu-id="b5c67-166">指定轉譯引擎如何驗證檔案名。</span><span class="sxs-lookup"><span data-stu-id="b5c67-166">Specifies how the render engine validates file names.</span></span><br/>                      |
| [<span data-ttu-id="b5c67-167">**SetTimelineObject**</span><span class="sxs-lookup"><span data-stu-id="b5c67-167">**SetTimelineObject**</span></span>](irenderengine-settimelineobject.md)                       | <span data-ttu-id="b5c67-168">設定要使用之轉譯引擎的時間軸。</span><span class="sxs-lookup"><span data-stu-id="b5c67-168">Sets the timeline for the render engine to use.</span></span><br/>                            |
| [<span data-ttu-id="b5c67-169">**UseInSmartRecompressionGraph**</span><span class="sxs-lookup"><span data-stu-id="b5c67-169">**UseInSmartRecompressionGraph**</span></span>](irenderengine-useinsmartrecompressiongraph.md) | <span data-ttu-id="b5c67-170">不支援。</span><span class="sxs-lookup"><span data-stu-id="b5c67-170">Not supported.</span></span><br/>                                                             |



 

## <a name="remarks"></a><span data-ttu-id="b5c67-171">備註</span><span class="sxs-lookup"><span data-stu-id="b5c67-171">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="b5c67-172">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="b5c67-172">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="b5c67-173">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="b5c67-173">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="b5c67-174">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="b5c67-174">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b5c67-175">規格需求</span><span class="sxs-lookup"><span data-stu-id="b5c67-175">Requirements</span></span>



| <span data-ttu-id="b5c67-176">需求</span><span class="sxs-lookup"><span data-stu-id="b5c67-176">Requirement</span></span> | <span data-ttu-id="b5c67-177">值</span><span class="sxs-lookup"><span data-stu-id="b5c67-177">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b5c67-178">標頭</span><span class="sxs-lookup"><span data-stu-id="b5c67-178">Header</span></span><br/>  | <dl> <span data-ttu-id="b5c67-179"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="b5c67-179"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="b5c67-180">程式庫</span><span class="sxs-lookup"><span data-stu-id="b5c67-180">Library</span></span><br/> | <dl> <span data-ttu-id="b5c67-181"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="b5c67-181"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5c67-182">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b5c67-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5c67-183">轉譯專案</span><span class="sxs-lookup"><span data-stu-id="b5c67-183">Rendering a Project</span></span>](rendering-a-project.md)
</dt> </dl>

 

 
