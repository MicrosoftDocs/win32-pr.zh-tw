---
description: 若要建立 Direct3D 裝置，請先建立 Direct3D 物件 (參閱 Direct3DCreate9) 。
ms.assetid: 06810f31-fa6c-416e-bd7b-65cfb3e6d7f2
title: " (Direct3D 9) 建立裝置"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a9c033ed25262f0a3bcdee9db73509ddf5cb53b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970711"
---
# <a name="creating-a-device-direct3d-9"></a><span data-ttu-id="1d28e-103"> (Direct3D 9) 建立裝置</span><span class="sxs-lookup"><span data-stu-id="1d28e-103">Creating a Device (Direct3D 9)</span></span>

<span data-ttu-id="1d28e-104">若要建立 Direct3D 裝置，請先建立 Direct3D 物件 (參閱 [**Direct3DCreate9**](/windows/win32/api/d3d9/nf-d3d9-direct3dcreate9)) 。</span><span class="sxs-lookup"><span data-stu-id="1d28e-104">To create a Direct3D device, first create a Direct3D object (see [**Direct3DCreate9**](/windows/win32/api/d3d9/nf-d3d9-direct3dcreate9)).</span></span> <span data-ttu-id="1d28e-105">Direct3D 物件所建立的所有轉譯裝置都會共用相同的實體資源。</span><span class="sxs-lookup"><span data-stu-id="1d28e-105">All rendering devices created by a Direct3D object share the same physical resources.</span></span> <span data-ttu-id="1d28e-106">如果您從單一 Direct3D 物件建立多個轉譯裝置，將會因為它們共用相同的硬體而產生極端的效能負面影響。</span><span class="sxs-lookup"><span data-stu-id="1d28e-106">If you create multiple rendering devices from a single Direct3D object, extreme performance penalties will be incurred because they share the same hardware.</span></span>

<span data-ttu-id="1d28e-107">首先，將用來建立 Direct3D 裝置的 [**D3DPRESENT \_ 參數**](d3dpresent-parameters.md) 結構的值初始化。</span><span class="sxs-lookup"><span data-stu-id="1d28e-107">First, initialize values for the [**D3DPRESENT\_PARAMETERS**](d3dpresent-parameters.md) structure that is used to create the Direct3D device.</span></span> <span data-ttu-id="1d28e-108">下列程式碼範例會指定視窗化的應用程式，其中的背景緩衝區只會在垂直同步作業期間複製到前端緩衝區。</span><span class="sxs-lookup"><span data-stu-id="1d28e-108">The following code example specifies a windowed application where the back buffer is copied to the front buffer during a vertical sync operation only.</span></span>


```
LPDIRECT3DDEVICE9 pDevice = NULL;

D3DPRESENT_PARAMETERS d3dpp; 

ZeroMemory( &d3dpp, sizeof(d3dpp) );
d3dpp.Windowed   = TRUE;
d3dpp.SwapEffect = D3DSWAPEFFECT_COPY;
```



<span data-ttu-id="1d28e-109">接著，建立 Direct3D 裝置。</span><span class="sxs-lookup"><span data-stu-id="1d28e-109">Next, create the Direct3D device.</span></span> <span data-ttu-id="1d28e-110">下列 [**IDirect3D9：： CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) 呼叫會指定預設的介面卡、硬體抽象層 (HAL) 裝置和軟體頂點處理。</span><span class="sxs-lookup"><span data-stu-id="1d28e-110">The following [**IDirect3D9::CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) call specifies the default adapter, a hardware abstraction layer (HAL) device, and software vertex processing.</span></span>


```
if( FAILED( g_pD3D->CreateDevice( D3DADAPTER_DEFAULT, D3DDEVTYPE_HAL, hWnd,
                                    D3DCREATE_SOFTWARE_VERTEXPROCESSING,
                                    &d3dpp, &d3dDevice ) ) )
    return E_FAIL;
```



<span data-ttu-id="1d28e-111">請注意，只有在與焦點視窗的視窗程式相同的執行緒上，才會執行建立、釋放或重設裝置的呼叫。</span><span class="sxs-lookup"><span data-stu-id="1d28e-111">Note that a call to create, release, or reset the device should happen only on the same thread as the window procedure of the focus window.</span></span>

<span data-ttu-id="1d28e-112">建立裝置之後，請設定其狀態。</span><span class="sxs-lookup"><span data-stu-id="1d28e-112">After creating the device, set its state.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1d28e-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="1d28e-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1d28e-114">Direct3D 裝置</span><span class="sxs-lookup"><span data-stu-id="1d28e-114">Direct3D Devices</span></span>](direct3d-devices.md)
</dt> </dl>

 

 
