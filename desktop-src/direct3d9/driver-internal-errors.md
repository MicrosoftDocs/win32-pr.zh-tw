---
description: 在 Direct3D 9 中，Direct3D 可讓驅動程式傳回錯誤碼（例如 E \_ OUTOFMEMORY、D3DERR \_ OUTOFVIDEOMEMORY 和 D3DERR UNSUPPORTEDCOLORARG）， \_ 讓應用程式能夠回應這些錯誤碼。
ms.assetid: 483fdb03-e453-4a1b-bd8e-294e9e9a20c2
title: " (Direct3D 9) 的驅動程式內部錯誤"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c81b0ee8ba50edb3c14fbd9a22c9fa9dc93aab8f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109341"
---
# <a name="driver-internal-errors-direct3d-9"></a><span data-ttu-id="96183-103"> (Direct3D 9) 的驅動程式內部錯誤</span><span class="sxs-lookup"><span data-stu-id="96183-103">Driver Internal Errors (Direct3D 9)</span></span>

<span data-ttu-id="96183-104">在 Direct3D 9 中，Direct3D 可讓驅動程式傳回錯誤碼（例如 E \_ OUTOFMEMORY、D3DERR \_ OUTOFVIDEOMEMORY 和 D3DERR UNSUPPORTEDCOLORARG）， \_ 讓應用程式能夠回應這些錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="96183-104">In Direct3D 9, Direct3D will allow the driver to return error codes such as E\_OUTOFMEMORY, D3DERR\_OUTOFVIDEOMEMORY, and D3DERR\_UNSUPPORTEDCOLORARG so that an application would be able to respond to them.</span></span> <span data-ttu-id="96183-105">不過，有時產生這些傳回型別的 API 呼叫會載入至命令緩衝區，並進行批次處理以傳送至 GPU (請參閱 [控制執行時間和驅動程式優化](accurately-profiling-direct3d-api-calls.md)) 。</span><span class="sxs-lookup"><span data-stu-id="96183-105">However, sometimes the API calls that generated these return types get loaded into a command buffer and are batched up to be sent to the GPU (see [Controlling Runtime and Driver Optimizations](accurately-profiling-direct3d-api-calls.md)).</span></span> <span data-ttu-id="96183-106">在此情況下，當需要採取動作時，錯誤無法轉送至應用程式，因此執行時間會取用錯誤碼，並在發生這種情況時對裝置物件發出附注。</span><span class="sxs-lookup"><span data-stu-id="96183-106">In this case, the errors cannot be relayed to the application when action needs to be taken, so the error code is consumed by the runtime and a note is made on the device object that this happened.</span></span> <span data-ttu-id="96183-107">稍後當應用程式叫用 [**IDirect3DDevice9：:P**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present)重新傳送時， **IDirect3DDevice9：:P** 重新傳送將會傳回 D3DERR \_ DRIVERINTERNALERROR。</span><span class="sxs-lookup"><span data-stu-id="96183-107">Later when the application invokes [**IDirect3DDevice9::Present**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present), **IDirect3DDevice9::Present** will return D3DERR\_DRIVERINTERNALERROR.</span></span> <span data-ttu-id="96183-108">這就是為什麼當應用程式收到來自 IDirect3DDevice9 的 D3DERR DRIVERINTERNALERROR 時，應用程式的最佳方法 \_ **：:P** 重新傳送是終結並重新建立裝置。</span><span class="sxs-lookup"><span data-stu-id="96183-108">This is why the best approach for an application to take when receiving a D3DERR\_DRIVERINTERNALERROR from **IDirect3DDevice9::Present** is to destroy and recreate the device.</span></span>

<span data-ttu-id="96183-109">如果您想要進一步進行偵錯工具，以下有幾個建議您嘗試找出產生錯誤的 API 呼叫：</span><span class="sxs-lookup"><span data-stu-id="96183-109">If you want to try to debug further, here are a couple of suggestions for trying to figure out which API call is generating the error:</span></span>

-   <span data-ttu-id="96183-110">因為可能傳回值的清單不完整，所以您可以嘗試找出每個 API 呼叫的周圍失敗的呼叫，如下所示：</span><span class="sxs-lookup"><span data-stu-id="96183-110">Because the list of possible return values is not complete, you can try to find which call is failing by surrounding each API call like this:</span></span>

    ```
    TRACE ( "Calling DrawPrimitive" );
    d3ddev->DrawPrim(...);
    TRACE ( "done\n" );
    ```

    

    <span data-ttu-id="96183-111">輸出的 debug 資料流程應該會顯示造成此問題的呼叫。</span><span class="sxs-lookup"><span data-stu-id="96183-111">The output debug stream should then show the call that is causing the problem.</span></span>

-   <span data-ttu-id="96183-112">此外，基於偵錯工具的目的，請嘗試在每個 IDirect3DDevice9 之前立即呼叫 [**IDirect3DDevice9：： ValidateDevice**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-validatedevice) [**：:D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) 以查看設備磁碟機是否有額外的問題 (不支援的作業、材質格式的組合等) 。</span><span class="sxs-lookup"><span data-stu-id="96183-112">Additionally, for debugging purposes, try calling [**IDirect3DDevice9::ValidateDevice**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-validatedevice) immediately before each [**IDirect3DDevice9::DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) to see if there is an additional problem with the device driver (unsupported operation, unusable combination of texture formats, etc).</span></span>

    > [!Note]  
    > <span data-ttu-id="96183-113">[**IDirect3DDevice9：： ValidateDevice**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-validatedevice) 應該謹慎地使用，因為驅動程式必須執行的驗證工作量，才能傳回答案。</span><span class="sxs-lookup"><span data-stu-id="96183-113">[**IDirect3DDevice9::ValidateDevice**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-validatedevice) should be used carefully and sparingly because of the amount of validation work the driver needs to perform to return an answer.</span></span>

     

## <a name="related-topics"></a><span data-ttu-id="96183-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="96183-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="96183-115">程式設計秘訣</span><span class="sxs-lookup"><span data-stu-id="96183-115">Programming Tips</span></span>](programming-tips.md)
</dt> </dl>

 

 
