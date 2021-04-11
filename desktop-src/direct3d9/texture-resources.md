---
description: 材質資源會在 IDirect3DTexture9 介面中執行。 若要取得紋理介面的指標，請呼叫 IDirect3DDevice9：： CreateTexture 方法或下列任何 D3DX 函數。
ms.assetid: vs|directx_sdk|~\texture_resources.htm
title: " (Direct3D 9) 的材質資源"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14134ca53b7735426e3f01340308282858da5516
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104187544"
---
# <a name="texture-resources-direct3d-9"></a><span data-ttu-id="d8a02-104"> (Direct3D 9) 的材質資源</span><span class="sxs-lookup"><span data-stu-id="d8a02-104">Texture Resources (Direct3D 9)</span></span>

<span data-ttu-id="d8a02-105">材質資源會在 [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) 介面中執行。</span><span class="sxs-lookup"><span data-stu-id="d8a02-105">Texture resources are implemented in the [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface.</span></span> <span data-ttu-id="d8a02-106">若要取得紋理介面的指標，請呼叫 [**IDirect3DDevice9：： CreateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture) 方法或下列任何 D3DX 函數。</span><span class="sxs-lookup"><span data-stu-id="d8a02-106">To obtain a pointer to a texture interface, call the [**IDirect3DDevice9::CreateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture) method or any of the following D3DX functions.</span></span>

-   [<span data-ttu-id="d8a02-107">**D3DXCreateTexture**</span><span class="sxs-lookup"><span data-stu-id="d8a02-107">**D3DXCreateTexture**</span></span>](d3dxcreatetexture.md)
-   [<span data-ttu-id="d8a02-108">**D3DXCreateTextureFromFile**</span><span class="sxs-lookup"><span data-stu-id="d8a02-108">**D3DXCreateTextureFromFile**</span></span>](d3dxcreatetexturefromfile.md)
-   [<span data-ttu-id="d8a02-109">**D3DXCreateTextureFromFileEx**</span><span class="sxs-lookup"><span data-stu-id="d8a02-109">**D3DXCreateTextureFromFileEx**</span></span>](d3dxcreatetexturefromfileex.md)
-   [<span data-ttu-id="d8a02-110">**D3DXCreateTextureFromFileInMemory**</span><span class="sxs-lookup"><span data-stu-id="d8a02-110">**D3DXCreateTextureFromFileInMemory**</span></span>](d3dxcreatetexturefromfileinmemory.md)
-   [<span data-ttu-id="d8a02-111">**D3DXCreateTextureFromFileInMemoryEx**</span><span class="sxs-lookup"><span data-stu-id="d8a02-111">**D3DXCreateTextureFromFileInMemoryEx**</span></span>](d3dxcreatetexturefromfileinmemoryex.md)
-   [<span data-ttu-id="d8a02-112">**D3DXCreateTextureFromResource**</span><span class="sxs-lookup"><span data-stu-id="d8a02-112">**D3DXCreateTextureFromResource**</span></span>](d3dxcreatetexturefromresource.md)
-   [<span data-ttu-id="d8a02-113">**D3DXCreateTextureFromResourceEx**</span><span class="sxs-lookup"><span data-stu-id="d8a02-113">**D3DXCreateTextureFromResourceEx**</span></span>](d3dxcreatetexturefromresourceex.md)

<span data-ttu-id="d8a02-114">下列程式碼範例會使用 [**D3DXCreateTextureFromFile**](d3dxcreatetexturefromfile.md) 從 Tiger.bmp 載入材質。</span><span class="sxs-lookup"><span data-stu-id="d8a02-114">The following code example uses [**D3DXCreateTextureFromFile**](d3dxcreatetexturefromfile.md) to load a texture from Tiger.bmp.</span></span>


```
// The following code example assumes that D3dDevice
// is a valid pointer to an IDirect3DDevice9 interface.

LPDIRECT3DTEXTURE9 pTexture;

D3DXCreateTextureFromFile( d3dDevice, "tiger.bmp", &pTexture);
```



<span data-ttu-id="d8a02-115">[**D3DXCreateTextureFromFile**](d3dxcreatetexturefromfile.md)所接受的第一個參數是 [**IDirect3DDevice9**](/windows/desktop/api)介面的指標。</span><span class="sxs-lookup"><span data-stu-id="d8a02-115">The first parameter that [**D3DXCreateTextureFromFile**](d3dxcreatetexturefromfile.md) accepts is a pointer to an [**IDirect3DDevice9**](/windows/desktop/api) interface.</span></span> <span data-ttu-id="d8a02-116">第二個參數會告訴 Direct3D 要從中載入材質的檔案名。</span><span class="sxs-lookup"><span data-stu-id="d8a02-116">The second parameter tells Direct3D the name of the file from which to load the texture.</span></span> <span data-ttu-id="d8a02-117">第三個參數會接受 [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) 介面指標的位址，表示所建立的材質物件。</span><span class="sxs-lookup"><span data-stu-id="d8a02-117">The third parameter takes the address of a pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) interface, representing the created texture object.</span></span>

## <a name="rendering-with-texture-resources"></a><span data-ttu-id="d8a02-118">以材質資源呈現</span><span class="sxs-lookup"><span data-stu-id="d8a02-118">Rendering with Texture Resources</span></span>

<span data-ttu-id="d8a02-119">Direct3D 透過紋理階段的概念支援多重紋理混合。</span><span class="sxs-lookup"><span data-stu-id="d8a02-119">Direct3D supports multiple texture blending through the concept of texture stages.</span></span> <span data-ttu-id="d8a02-120">每個紋理階段都包含了一個紋理及可以執行於該紋理之上的運算。</span><span class="sxs-lookup"><span data-stu-id="d8a02-120">Each texture stage contains a texture and operations that can be performed on the texture.</span></span> <span data-ttu-id="d8a02-121">紋理階段中的紋理構成了現有紋理的組合。</span><span class="sxs-lookup"><span data-stu-id="d8a02-121">The textures in the texture stages form the set of current textures.</span></span> <span data-ttu-id="d8a02-122">如需詳細資訊，請參閱 [ (Direct3D 9) 的材質混色 ](texture-blending.md)。</span><span class="sxs-lookup"><span data-stu-id="d8a02-122">For more information, see [Texture Blending (Direct3D 9)](texture-blending.md).</span></span> <span data-ttu-id="d8a02-123">每個紋理的狀態都封裝於其紋理階段中。</span><span class="sxs-lookup"><span data-stu-id="d8a02-123">The state of each texture is encapsulated in its texture stage.</span></span>

<span data-ttu-id="d8a02-124">在 c + + 應用程式中，每個材質的狀態都必須使用 [**IDirect3DDevice9：： SetTextureStageState**](/windows/desktop/api) 方法來設定。</span><span class="sxs-lookup"><span data-stu-id="d8a02-124">In a C++ application, the state of each texture must be set with the [**IDirect3DDevice9::SetTextureStageState**](/windows/desktop/api) method.</span></span> <span data-ttu-id="d8a02-125">將階段號碼 (0-7) 傳遞為第一個參數的值。</span><span class="sxs-lookup"><span data-stu-id="d8a02-125">Pass the stage number (0-7) as the value of the first parameter.</span></span> <span data-ttu-id="d8a02-126">將第二個參數的值設定為 [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md) 列舉型別的成員。</span><span class="sxs-lookup"><span data-stu-id="d8a02-126">Set the value of the second parameter to a member of the [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md) enumerated type.</span></span> <span data-ttu-id="d8a02-127">最後一個參數是特定材質狀態的狀態值。</span><span class="sxs-lookup"><span data-stu-id="d8a02-127">The final parameter is the state value for the particular texture state.</span></span>

<span data-ttu-id="d8a02-128">使用紋理介面指標時，您的應用程式可以轉譯最多8個材質的 blend。</span><span class="sxs-lookup"><span data-stu-id="d8a02-128">Using texture interface pointers, your application can render a blend of up to eight textures.</span></span> <span data-ttu-id="d8a02-129">藉由叫用 [**IDirect3DDevice9：： SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) 方法來設定目前的材質。</span><span class="sxs-lookup"><span data-stu-id="d8a02-129">Set the current textures by invoking the [**IDirect3DDevice9::SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) method.</span></span> <span data-ttu-id="d8a02-130">Direct3D 會將所有目前的材質混合到它所呈現的基本專案。</span><span class="sxs-lookup"><span data-stu-id="d8a02-130">Direct3D blends all current textures onto the primitives that it renders.</span></span>

> [!Note]  
> <span data-ttu-id="d8a02-131">[**IDirect3DDevice9：： SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture)方法會遞增所指派之材質介面的參考計數。</span><span class="sxs-lookup"><span data-stu-id="d8a02-131">The [**IDirect3DDevice9::SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) method increments the reference count of the texture surface being assigned.</span></span> <span data-ttu-id="d8a02-132">當不再需要材質時，您應該將適當階段的材質設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="d8a02-132">When the texture is no longer needed, you should set the texture at the appropriate stage to **NULL**.</span></span> <span data-ttu-id="d8a02-133">如果您無法這樣做，將不會釋放介面，導致記憶體流失。</span><span class="sxs-lookup"><span data-stu-id="d8a02-133">If you fail to do this, the surface will not be released, resulting in a memory leak.</span></span>

 

<span data-ttu-id="d8a02-134">您的應用程式可以藉由呼叫 [**IDirect3DDevice9：： graphicsdevice**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) 方法，來設定目前材質的材質換行狀態。</span><span class="sxs-lookup"><span data-stu-id="d8a02-134">Your application can set the texture wrapping state for the current textures by calling the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method.</span></span> <span data-ttu-id="d8a02-135">從 D3DRS \_ WRAP0 到 D3DRS WRAP7 傳遞值 \_ 做為第一個參數的值，並使用 D3DWRAPCOORD \_ 0、D3DWRAPCOORD \_ 1、D3DWRAPCOORD \_ 2 和 D3DWRAPCOORD 3 旗標的組合， \_ 以啟用 u、v 或 w 方向的換行。</span><span class="sxs-lookup"><span data-stu-id="d8a02-135">Pass a value from D3DRS\_WRAP0 through D3DRS\_WRAP7 as the value of the first parameter, and use a combination of the D3DWRAPCOORD\_0, D3DWRAPCOORD\_1, D3DWRAPCOORD\_2, and D3DWRAPCOORD\_3 flags to enable wrapping in the u, v, or w directions.</span></span>

<span data-ttu-id="d8a02-136">您的應用程式也可以設定紋理透視及紋理篩選狀態。</span><span class="sxs-lookup"><span data-stu-id="d8a02-136">Your application can also set the texture perspective and texture filtering states.</span></span> <span data-ttu-id="d8a02-137">請參閱 [ (Direct3D 9) 的材質篩選 ](texture-filtering.md)。</span><span class="sxs-lookup"><span data-stu-id="d8a02-137">See [Texture Filtering (Direct3D 9)](texture-filtering.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d8a02-138">相關主題</span><span class="sxs-lookup"><span data-stu-id="d8a02-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d8a02-139">Direct3D 紋理</span><span class="sxs-lookup"><span data-stu-id="d8a02-139">Direct3D Textures</span></span>](direct3d-textures.md)
</dt> </dl>

 

 
