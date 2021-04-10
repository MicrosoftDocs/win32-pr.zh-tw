---
description: 深度緩衝區是裝置的屬性。 若要建立由 Direct3D 管理的深度緩衝區，請設定 D3DPRESENT 參數結構的適當成員， \_ 如下列程式碼範例所示。
ms.assetid: 2b442cf7-2146-4dea-809a-ebb8bcfbec08
title: " (Direct3D 9) 建立深度緩衝區"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa30ccba6c44d3582201ea96017a16cc903fecce
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110273"
---
# <a name="creating-a-depth-buffer-direct3d-9"></a><span data-ttu-id="03733-104"> (Direct3D 9) 建立深度緩衝區</span><span class="sxs-lookup"><span data-stu-id="03733-104">Creating a Depth Buffer (Direct3D 9)</span></span>

<span data-ttu-id="03733-105">深度緩衝區是裝置的屬性。</span><span class="sxs-lookup"><span data-stu-id="03733-105">A depth buffer is a property of the device.</span></span> <span data-ttu-id="03733-106">若要建立由 Direct3D 管理的深度緩衝區，請設定 [**D3DPRESENT \_ 參數**](d3dpresent-parameters.md) 結構的適當成員，如下列程式碼範例所示。</span><span class="sxs-lookup"><span data-stu-id="03733-106">To create a depth buffer that is managed by Direct3D, set the appropriate members of the [**D3DPRESENT\_PARAMETERS**](d3dpresent-parameters.md) structure as shown in the following code example.</span></span>


```
D3DPRESENT_PARAMETERS d3dpp; 
ZeroMemory( &d3dpp, sizeof(d3dpp) );
d3dpp.Windowed               = TRUE;
d3dpp.SwapEffect             = D3DSWAPEFFECT_COPY;
d3dpp.EnableAutoDepthStencil = TRUE;
d3dpp.AutoDepthStencilFormat = D3DFMT_D16;
```



<span data-ttu-id="03733-107">藉由將 EnableAutoDepthStencil 成員設定為 **TRUE**，您可以指示 Direct3D 來管理應用程式的深度緩衝區。</span><span class="sxs-lookup"><span data-stu-id="03733-107">By setting the EnableAutoDepthStencil member to **TRUE**, you instruct Direct3D to manage depth buffers for the application.</span></span> <span data-ttu-id="03733-108">請注意，AutoDepthStencilFormat 必須設定為有效的深度緩衝區格式。</span><span class="sxs-lookup"><span data-stu-id="03733-108">Note that AutoDepthStencilFormat must be set to a valid depth buffer format.</span></span> <span data-ttu-id="03733-109">D3DFMT \_ D16 旗標會指定16位的深度緩衝區（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="03733-109">The D3DFMT\_D16 flag specifies a 16-bit depth buffer, if one is available.</span></span>

<span data-ttu-id="03733-110">下列 [**IDirect3D9：： CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) 方法呼叫會建立接著建立深度緩衝區的裝置。</span><span class="sxs-lookup"><span data-stu-id="03733-110">The following call to the [**IDirect3D9::CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) method creates a device that then creates a depth buffer.</span></span>


```
if( FAILED( g_pD3D->CreateDevice( D3DADAPTER_DEFAULT, D3DDEVTYPE_HAL, hWnd,
                                D3DCREATE_SOFTWARE_VERTEXPROCESSING,
                                &d3dpp, &d3dDevice ) ) )
return E_FAIL;
```



<span data-ttu-id="03733-111">深度緩衝區會自動設定為裝置的呈現目標。</span><span class="sxs-lookup"><span data-stu-id="03733-111">The depth buffer is automatically set as the render target of the device.</span></span> <span data-ttu-id="03733-112">當裝置重設時，會自動終結深度緩衝區，並重新建立新的大小。</span><span class="sxs-lookup"><span data-stu-id="03733-112">When the device is reset, the depth buffer is automatically destroyed and re-created in the new size.</span></span>

<span data-ttu-id="03733-113">若要建立新的深度緩衝區介面，請使用 [**IDirect3DDevice9：： CreateDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createdepthstencilsurface) 方法。</span><span class="sxs-lookup"><span data-stu-id="03733-113">To create a new depth buffer surface, use the [**IDirect3DDevice9::CreateDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createdepthstencilsurface) method.</span></span>

<span data-ttu-id="03733-114">若要為裝置設定新的深度緩衝區介面，請使用 [**IDirect3DDevice9：： SetDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setdepthstencilsurface) 方法。</span><span class="sxs-lookup"><span data-stu-id="03733-114">To set a new depth-buffer surface for the device, use the [**IDirect3DDevice9::SetDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setdepthstencilsurface) method.</span></span>

<span data-ttu-id="03733-115">若要在您的應用程式中使用深度緩衝區，您必須啟用深度緩衝區。</span><span class="sxs-lookup"><span data-stu-id="03733-115">To use the depth buffer in your application, you need to enable the depth buffer.</span></span> <span data-ttu-id="03733-116">如需詳細資訊，請參閱 [啟用 (Direct3D 9) 的深度緩衝 ](enabling-depth-buffering.md)。</span><span class="sxs-lookup"><span data-stu-id="03733-116">For details, see [Enabling Depth Buffering (Direct3D 9)](enabling-depth-buffering.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="03733-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="03733-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="03733-118">深度緩衝區</span><span class="sxs-lookup"><span data-stu-id="03733-118">Depth Buffers</span></span>](depth-buffers.md)
</dt> </dl>

 

 
