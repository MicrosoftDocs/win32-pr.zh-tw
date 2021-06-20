---
description: 深入瞭解 D3DX 中的材質支援。 D3DX 是提供 helper 服務的公用程式庫。 它是 Direct3D 元件之上的一層。
ms.assetid: 84815851-ca96-47ab-9f84-56ecaeb4a6d9
title: 'D3DX 中的材質支援 (Direct3D 9) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f31a597ddcab317477d31e0d833c9da96f71ed4
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404601"
---
# <a name="texture-support-in-d3dx-direct3d-9"></a><span data-ttu-id="8e749-105">D3DX 中的材質支援 (Direct3D 9) </span><span class="sxs-lookup"><span data-stu-id="8e749-105">Texture Support in D3DX (Direct3D 9)</span></span>

<span data-ttu-id="8e749-106">D3DX 是提供 helper 服務的公用程式庫。</span><span class="sxs-lookup"><span data-stu-id="8e749-106">D3DX is a utility library that provides helper services.</span></span> <span data-ttu-id="8e749-107">它是 Direct3D 元件之上的一層。</span><span class="sxs-lookup"><span data-stu-id="8e749-107">It is a layer above the Direct3D component.</span></span>

## <a name="textures"></a><span data-ttu-id="8e749-108">紋理</span><span class="sxs-lookup"><span data-stu-id="8e749-108">Textures</span></span>

<span data-ttu-id="8e749-109">下列主題支援許多不同的材質。</span><span class="sxs-lookup"><span data-stu-id="8e749-109">Many different textures are supported in the following topics.</span></span>

-   <span data-ttu-id="8e749-110">標準 mipmapped 材質支援。</span><span class="sxs-lookup"><span data-stu-id="8e749-110">Standard mipmapped texture support.</span></span> <span data-ttu-id="8e749-111">請參閱 [自動產生 mipmap (Direct3D 9) ](automatic-generation-of-mipmaps.md)。</span><span class="sxs-lookup"><span data-stu-id="8e749-111">See [Automatic Generation of Mipmaps (Direct3D 9)](automatic-generation-of-mipmaps.md).</span></span>
-   <span data-ttu-id="8e749-112">Cube 地圖支援。</span><span class="sxs-lookup"><span data-stu-id="8e749-112">Cube map support.</span></span> <span data-ttu-id="8e749-113">請參閱 [ (Direct3D 9) 的三次環境對應 ](cubic-environment-mapping.md)。</span><span class="sxs-lookup"><span data-stu-id="8e749-113">See [Cubic Environment Mapping (Direct3D 9)](cubic-environment-mapping.md).</span></span>
-   <span data-ttu-id="8e749-114">磁片區材質支援。</span><span class="sxs-lookup"><span data-stu-id="8e749-114">Volume texture support.</span></span> <span data-ttu-id="8e749-115">請參閱 [ (Direct3D 9) 的音量材質資源 ](volume-texture-resources.md)。</span><span class="sxs-lookup"><span data-stu-id="8e749-115">See [Volume Texture Resources (Direct3D 9)](volume-texture-resources.md).</span></span>
-   <span data-ttu-id="8e749-116">環境對應支援。</span><span class="sxs-lookup"><span data-stu-id="8e749-116">Environment mapping support.</span></span> <span data-ttu-id="8e749-117">請參閱 [ (Direct3D 9) 的環境對應 ](environment-mapping.md)。</span><span class="sxs-lookup"><span data-stu-id="8e749-117">See [Environment Mapping (Direct3D 9)](environment-mapping.md).</span></span>
-   <span data-ttu-id="8e749-118">凹凸對應支援。</span><span class="sxs-lookup"><span data-stu-id="8e749-118">Bump mapping support.</span></span> <span data-ttu-id="8e749-119">請參閱 [ (Direct3D 9) 的 [凹凸對應 ](bump-mapping.md)]。</span><span class="sxs-lookup"><span data-stu-id="8e749-119">See [Bump Mapping (Direct3D 9)](bump-mapping.md).</span></span>

### <a name="texture-color-conversion"></a><span data-ttu-id="8e749-120">材質色彩轉換</span><span class="sxs-lookup"><span data-stu-id="8e749-120">Texture Color Conversion</span></span>

<span data-ttu-id="8e749-121">使用任何 D3DXLoadSurfacexxx、D3DXLoadVolumexxx、D3DXCreateTexturexxx、D3DXCreateCubeTexturexxx 或 D3DXCreateVolumeTexturexxx 函數時，可能需要執行色彩轉換。</span><span class="sxs-lookup"><span data-stu-id="8e749-121">When using any of the D3DXLoadSurfacexxx, D3DXLoadVolumexxx, D3DXCreateTexturexxx, D3DXCreateCubeTexturexxx, or D3DXCreateVolumeTexturexxx functions, color conversion might need to be performed.</span></span> <span data-ttu-id="8e749-122">例如，一個介面可能是 RGBA 類型，另一個則可能是 UVWQ。</span><span class="sxs-lookup"><span data-stu-id="8e749-122">For example, one surface might be type RGBA and the other might be UVWQ.</span></span> <span data-ttu-id="8e749-123">針對不同格式的案例，轉換順序如下所示：</span><span class="sxs-lookup"><span data-stu-id="8e749-123">For cases of dissimilar formats, the conversion sequence is as follows:</span></span>

### <a name="mapping-rgba-to-uvwq"></a><span data-ttu-id="8e749-124">將 RGBA 對應至 UVWQ</span><span class="sxs-lookup"><span data-stu-id="8e749-124">Mapping RGBA to UVWQ</span></span>

-   <span data-ttu-id="8e749-125">R <-> U，R 通道會對應至 U 通道，反之亦然。</span><span class="sxs-lookup"><span data-stu-id="8e749-125">R <-> U, R channel is mapped to the U channel, or vice versa.</span></span>
-   <span data-ttu-id="8e749-126">G <-> V、G 通道會對應至 V 通道，反之亦然。</span><span class="sxs-lookup"><span data-stu-id="8e749-126">G <-> V, G channel is mapped to the V channel, or vice versa.</span></span>
-   <span data-ttu-id="8e749-127">B <-> W，B 通道會對應至 W 通道，反之亦然。</span><span class="sxs-lookup"><span data-stu-id="8e749-127">B <-> W, B channel is mapped to the W channel, or vice versa.</span></span>
-   <span data-ttu-id="8e749-128">< > Q/L，通道會對應至 Q 或 L 通道 (，視目的地格式的可用版本) ，反之亦然。</span><span class="sxs-lookup"><span data-stu-id="8e749-128">A <-> Q/L, A channel is mapped to either the Q or the L channel (depending on which one is available in the destination format), or vice versa.</span></span>


```
R->U
G->V
B->W
A->Q or A->L
```



### <a name="mapping-uv-to-rgba"></a><span data-ttu-id="8e749-129">將 UV 對應到 RGBA</span><span class="sxs-lookup"><span data-stu-id="8e749-129">Mapping UV to RGBA</span></span>

-   <span data-ttu-id="8e749-130">U <-> R、U 通道會對應至 R 通道，反之亦然。</span><span class="sxs-lookup"><span data-stu-id="8e749-130">U <-> R, U channel is mapped to the R channel, or vice versa.</span></span>
-   <span data-ttu-id="8e749-131">V <-> G，V 通道會對應至 G 通道，反之亦然。</span><span class="sxs-lookup"><span data-stu-id="8e749-131">V <-> G, V channel is mapped to the G channel, or vice versa.</span></span>
-   <span data-ttu-id="8e749-132">1 <-> B，1對應至 B 通道，反之亦然。</span><span class="sxs-lookup"><span data-stu-id="8e749-132">1 <-> B, 1 is mapped to the B channel, or vice versa.</span></span>
-   <span data-ttu-id="8e749-133">1 <-> A、1對應至通道，反之亦然。</span><span class="sxs-lookup"><span data-stu-id="8e749-133">1 <-> A, 1 is mapped to the A channel, or vice versa.</span></span>

<span data-ttu-id="8e749-134">如果來源中沒有一個通道，則會假設為 1 (但 A8 除外，其中 R、G、B 假設為 0) 。</span><span class="sxs-lookup"><span data-stu-id="8e749-134">If a channel does not exist in the source, it is assumed to be 1 (with the exception of A8, where R,G,B are assumed to be 0).</span></span> <span data-ttu-id="8e749-135">例如：</span><span class="sxs-lookup"><span data-stu-id="8e749-135">For example:</span></span>


```
U -> R
V -> G
1 -> B
1 -> A
```



## <a name="related-topics"></a><span data-ttu-id="8e749-136">相關主題</span><span class="sxs-lookup"><span data-stu-id="8e749-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8e749-137">D3DX</span><span class="sxs-lookup"><span data-stu-id="8e749-137">D3DX</span></span>](d3dx.md)
</dt> </dl>

 

 



