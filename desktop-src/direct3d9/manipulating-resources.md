---
description: 您的應用程式會操控資源以轉譯場景。
ms.assetid: 4f0eea7d-b1e4-4d53-a136-f40df7a0fbb1
title: " (Direct3D 9) 操作資源"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 886dfee3af024d103dab8666687f1b053a5fb46a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104385493"
---
# <a name="manipulating-resources-direct3d-9"></a><span data-ttu-id="370df-103"> (Direct3D 9) 操作資源</span><span class="sxs-lookup"><span data-stu-id="370df-103">Manipulating Resources (Direct3D 9)</span></span>

<span data-ttu-id="370df-104">您的應用程式會操控資源以轉譯場景。</span><span class="sxs-lookup"><span data-stu-id="370df-104">Your application manipulates resources in order to render a scene.</span></span> <span data-ttu-id="370df-105">首先，應用程式必須使用下列其中一種方法來建立材質資源：</span><span class="sxs-lookup"><span data-stu-id="370df-105">First, an application needs to create a texture resource with one of the following methods:</span></span>

-   [<span data-ttu-id="370df-106">**IDirect3DDevice9::CreateCubeTexture**</span><span class="sxs-lookup"><span data-stu-id="370df-106">**IDirect3DDevice9::CreateCubeTexture**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createcubetexture)
-   [<span data-ttu-id="370df-107">**IDirect3DDevice9::CreateTexture**</span><span class="sxs-lookup"><span data-stu-id="370df-107">**IDirect3DDevice9::CreateTexture**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture)
-   [<span data-ttu-id="370df-108">**IDirect3DDevice9::CreateVolumeTexture**</span><span class="sxs-lookup"><span data-stu-id="370df-108">**IDirect3DDevice9::CreateVolumeTexture**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvolumetexture)

<span data-ttu-id="370df-109">您可以使用其中一個 D3DXCreatexxx 紋理函式來建立材質資源。</span><span class="sxs-lookup"><span data-stu-id="370df-109">A texture resource can instead be created with one of the D3DXCreatexxx texturing functions.</span></span>

<span data-ttu-id="370df-110">材質建立方法所傳回的材質物件是表面或磁片區的容器;這些容器一般稱為緩衝區。</span><span class="sxs-lookup"><span data-stu-id="370df-110">The texture objects returned by the texture creation methods are containers for surfaces or volumes; these containers are generically known as buffers.</span></span> <span data-ttu-id="370df-111">資源所擁有的緩衝區會繼承資源的使用方式、格式和集區，但會有自己的類型。</span><span class="sxs-lookup"><span data-stu-id="370df-111">The buffers owned by the resource inherit the usages, format, and pool of the resource but have their own type.</span></span> <span data-ttu-id="370df-112">如需詳細資訊，請參閱 [ (Direct3D 9) 的資源屬性 ](resource-properties.md)。</span><span class="sxs-lookup"><span data-stu-id="370df-112">For more information, see [Resource Properties (Direct3D 9)](resource-properties.md).</span></span>

<span data-ttu-id="370df-113">應用程式會藉由呼叫下列方法，取得所包含表面的存取權，以載入插圖。</span><span class="sxs-lookup"><span data-stu-id="370df-113">The application gains access to the contained surfaces, for the purpose of loading artwork, by calling the following methods.</span></span> <span data-ttu-id="370df-114">如需詳細資訊，請參閱 [ (Direct3D 9) 的鎖定資源 ](locking-resources.md)。</span><span class="sxs-lookup"><span data-stu-id="370df-114">For details, see [Locking Resources (Direct3D 9)](locking-resources.md).</span></span>

-   [<span data-ttu-id="370df-115">**IDirect3DCubeTexture9::LockRect**</span><span class="sxs-lookup"><span data-stu-id="370df-115">**IDirect3DCubeTexture9::LockRect**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-lockrect)
-   [<span data-ttu-id="370df-116">**IDirect3DTexture9::LockRect**</span><span class="sxs-lookup"><span data-stu-id="370df-116">**IDirect3DTexture9::LockRect**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-lockrect)
-   [<span data-ttu-id="370df-117">**IDirect3DVolumeTexture9：：加密箱**</span><span class="sxs-lookup"><span data-stu-id="370df-117">**IDirect3DVolumeTexture9::LockBox**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-lockbox)

<span data-ttu-id="370df-118">鎖定方法會使用引數來表示內含的介面（例如，mipmap 的子層級或立方體的材質面），並將指標傳回至圖元。</span><span class="sxs-lookup"><span data-stu-id="370df-118">The lock methods take arguments denoting the contained surface - for example, the mipmap sub-level or cube face of the texture - and return pointers to the pixels.</span></span> <span data-ttu-id="370df-119">一般的應用程式永遠不會直接使用介面物件。</span><span class="sxs-lookup"><span data-stu-id="370df-119">The typical application never uses a surface object directly.</span></span>

<span data-ttu-id="370df-120">藉由呼叫 [**IDirect3DDevice9：： CreateIndexBuffer**](/windows/desktop/api) 或 [**IDirect3DDevice9：： CreateVertexBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvertexbuffer)來建立幾何導向的資源。</span><span class="sxs-lookup"><span data-stu-id="370df-120">Create geometry-oriented resources by calling [**IDirect3DDevice9::CreateIndexBuffer**](/windows/desktop/api) or [**IDirect3DDevice9::CreateVertexBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvertexbuffer).</span></span>

<span data-ttu-id="370df-121">藉由呼叫 [**IDirect3DIndexBuffer9：： lock**](/windows/desktop/api) 或 [**IDirect3DVertexBuffer9：： lock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvertexbuffer9-lock)來鎖定和填滿緩衝區資源，視資源而定。</span><span class="sxs-lookup"><span data-stu-id="370df-121">Lock and fill the buffer resources by calling either [**IDirect3DIndexBuffer9::Lock**](/windows/desktop/api) or [**IDirect3DVertexBuffer9::Lock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvertexbuffer9-lock), depending upon the resource.</span></span>

<span data-ttu-id="370df-122">針對 managed 材質資源，資源建立程式會在此結束。</span><span class="sxs-lookup"><span data-stu-id="370df-122">For managed texture resources, the resource creation process ends here.</span></span> <span data-ttu-id="370df-123">針對非受控材質資源，應用程式會藉由呼叫 [**IDirect3DDevice9：： UpdateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatetexture)，將系統記憶體資源升級為可存取裝置的資源 (硬體加速) 。</span><span class="sxs-lookup"><span data-stu-id="370df-123">For non-managed texture resources, an application promotes system memory resources to device-accessible resources (for hardware acceleration) by calling [**IDirect3DDevice9::UpdateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatetexture).</span></span>

<span data-ttu-id="370df-124">若要呈現從資源轉譯的影像，應用程式也需要色彩和深度樣板的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="370df-124">To present images rendered from resources, the application also needs color and depth-stencil buffers.</span></span> <span data-ttu-id="370df-125">針對一般的應用程式，顏色緩衝區是由裝置的交換鏈所擁有，也就是後置緩衝區介面的集合，且會使用裝置隱含建立。</span><span class="sxs-lookup"><span data-stu-id="370df-125">For typical applications, the color buffer is owned by the device's swap chain, which is a collection of back-buffer surfaces, and is implicitly created with the device.</span></span> <span data-ttu-id="370df-126">您可以使用 [**IDirect3DDevice9：： CreateDepthStencilSurface**](/windows/desktop/api) 方法，以隱含方式建立或明確建立深度樣板表面。</span><span class="sxs-lookup"><span data-stu-id="370df-126">Depth-stencil surfaces can be implicitly created, or explicitly created by using the [**IDirect3DDevice9::CreateDepthStencilSurface**](/windows/desktop/api) method.</span></span> <span data-ttu-id="370df-127">應用程式會透過呼叫 [**IDirect3DDevice9：： SetRenderTarget**](/windows/desktop/api) 或 [**IDirect3DDevice9：： SetDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setdepthstencilsurface)，將裝置及其深度和色彩緩衝區相關聯。</span><span class="sxs-lookup"><span data-stu-id="370df-127">The application associates a device and its depth and color buffer with a call to [**IDirect3DDevice9::SetRenderTarget**](/windows/desktop/api) or [**IDirect3DDevice9::SetDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setdepthstencilsurface).</span></span>

<span data-ttu-id="370df-128">如需呈現最終影像的詳細資訊，請參閱 [ (Direct3D 9 呈現場景) ](presenting-a-scene.md)。</span><span class="sxs-lookup"><span data-stu-id="370df-128">For details on presenting the final image, see [Presenting a Scene (Direct3D 9)](presenting-a-scene.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="370df-129">相關主題</span><span class="sxs-lookup"><span data-stu-id="370df-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="370df-130">Direct3D 資源</span><span class="sxs-lookup"><span data-stu-id="370df-130">Direct3D Resources</span></span>](direct3d-resources.md)
</dt> </dl>

 

 
