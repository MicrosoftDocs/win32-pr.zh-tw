---
description: 效果狀態是運算式形式的成對名稱/值。
ms.assetid: 4612c6bd-bc1f-42ad-8465-c0d4b577d1db
title: '效果狀態群組 (Direct3D 10) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c132db3a5258cbe3573ddc5103df8b3cbcf2085d
ms.sourcegitcommit: 628fda3e63fd1d513ce9a5f55be8bbc4af4b2a4b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "104321672"
---
# <a name="effect-state-groups-direct3d-10"></a><span data-ttu-id="d3e12-103">效果狀態群組 (Direct3D 10) </span><span class="sxs-lookup"><span data-stu-id="d3e12-103">Effect state groups (Direct3D 10)</span></span>

<span data-ttu-id="d3e12-104">效果狀態是運算式形式的成對名稱/值。</span><span class="sxs-lookup"><span data-stu-id="d3e12-104">Effect states are name-value pairs in the form of an expression.</span></span>

## <a name="blend-state"></a><span data-ttu-id="d3e12-105">Blend 狀態</span><span class="sxs-lookup"><span data-stu-id="d3e12-105">Blend state</span></span>

| | |
|-|-|
| <span data-ttu-id="d3e12-106">**ALPHATOCOVERAGEENABLE**、 **BLENDENABLE**、 **SRCBLEND**、 **DESTBLEND**、 **BLENDOP**、 **SRCBLENDALPHA**、 **DESTBLENDALPHA**、 **BLENDOPALPHA**、 **RENDERTARGETWRITEMASK**</span><span class="sxs-lookup"><span data-stu-id="d3e12-106">**ALPHATOCOVERAGEENABLE**, **BLENDENABLE**, **SRCBLEND**, **DESTBLEND**, **BLENDOP**, **SRCBLENDALPHA**, **DESTBLENDALPHA**, **BLENDOPALPHA**, **RENDERTARGETWRITEMASK**</span></span> | <span data-ttu-id="d3e12-107">[ **D3D10 \_ BLEND \_ DESC** 的成員](/windows/desktop/api/D3D10/ns-d3d10-d3d10_blend_desc)</span><span class="sxs-lookup"><span data-stu-id="d3e12-107">Members of [**D3D10\_BLEND\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_blend_desc)</span></span> |

## <a name="depth-and-stencil-state"></a><span data-ttu-id="d3e12-108">深度和樣板狀態</span><span class="sxs-lookup"><span data-stu-id="d3e12-108">Depth and stencil state</span></span>

| | |
|-|-|
| <span data-ttu-id="d3e12-109">**DEPTHENABLE**、 **DEPTHWRITEMASK**、 **DEPTHFUNC**、 **STENCILENABLE**、 **STENCILREADMASK**、 **STENCILWRITEMASK**</span><span class="sxs-lookup"><span data-stu-id="d3e12-109">**DEPTHENABLE**, **DEPTHWRITEMASK**, **DEPTHFUNC**, **STENCILENABLE**, **STENCILREADMASK**, **STENCILWRITEMASK**</span></span> | <span data-ttu-id="d3e12-110">[ **D3D10 深度樣板 \_ \_ \_ DESC** 的成員](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencil_desc)</span><span class="sxs-lookup"><span data-stu-id="d3e12-110">Members of [**D3D10\_DEPTH\_STENCIL\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencil_desc)</span></span> |
| <span data-ttu-id="d3e12-111">FRONTFACESTENCILFAIL \* \*、 **FRONTFACESTENCILZFAIL**、 **FRONTFACESTENCILPASS**、 **FRONTFACESTENCILFUNC**、 **BACKFACESTENCILFAIL**、 **BACKFACESTENCILZFAIL**、 **BACKFACESTENCILPASS**、 **BACKFACESTENCILFUNC**</span><span class="sxs-lookup"><span data-stu-id="d3e12-111">FRONTFACESTENCILFAIL\*\*, **FRONTFACESTENCILZFAIL**, **FRONTFACESTENCILPASS**, **FRONTFACESTENCILFUNC**, **BACKFACESTENCILFAIL**, **BACKFACESTENCILZFAIL**, **BACKFACESTENCILPASS**, **BACKFACESTENCILFUNC**</span></span> | <span data-ttu-id="d3e12-112">[ **D3D10 \_ 深度 \_ STENCILOP \_ DESC** 的成員](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencilop_desc)</span><span class="sxs-lookup"><span data-stu-id="d3e12-112">Member of [**D3D10\_DEPTH\_STENCILOP\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencilop_desc)</span></span> |

## <a name="rasterizer-state"></a><span data-ttu-id="d3e12-113">轉譯器狀態</span><span class="sxs-lookup"><span data-stu-id="d3e12-113">Rasterizer state</span></span>

| | |
|-|-|
| <span data-ttu-id="d3e12-114">FILLMODE</span><span class="sxs-lookup"><span data-stu-id="d3e12-114">FILLMODE</span></span> | [<span data-ttu-id="d3e12-115">**D3D10 \_ 填滿 \_ 模式**</span><span class="sxs-lookup"><span data-stu-id="d3e12-115">**D3D10\_FILL\_MODE**</span></span>](/windows/desktop/api/D3D10/ne-d3d10-d3d10_fill_mode) |
| <span data-ttu-id="d3e12-116">CULLMODE</span><span class="sxs-lookup"><span data-stu-id="d3e12-116">CULLMODE</span></span> | [<span data-ttu-id="d3e12-117">**D3D10 的 \_ 挑選 \_ 模式**</span><span class="sxs-lookup"><span data-stu-id="d3e12-117">**D3D10\_CULL\_MODE**</span></span>](/windows/desktop/api/D3D10/ne-d3d10-d3d10_cull_mode) |
| <span data-ttu-id="d3e12-118">**FRONTCOUNTERCLOCKWISE**、 **DEPTHBIAS**、 **DEPTHBIASCLAMP**、 **SLOPESCALEDDEPTHBIAS**、 **ZCLIPENABLE**、 **SCISSORENABLE**、 **MULTISAMPLEENABLE**、 **ANTIALIASEDLINEENABLE**</span><span class="sxs-lookup"><span data-stu-id="d3e12-118">**FRONTCOUNTERCLOCKWISE**, **DEPTHBIAS**, **DEPTHBIASCLAMP**, **SLOPESCALEDDEPTHBIAS**, **ZCLIPENABLE**, **SCISSORENABLE**, **MULTISAMPLEENABLE**, **ANTIALIASEDLINEENABLE**</span></span> | <span data-ttu-id="d3e12-119">D3D10 轉譯器 [ **\_ \_ DESC** 的成員](/windows/desktop/api/D3D10/ns-d3d10-d3d10_rasterizer_desc)</span><span class="sxs-lookup"><span data-stu-id="d3e12-119">Members of [**D3D10\_RASTERIZER\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_rasterizer_desc)</span></span> |

## <a name="sampler-state"></a><span data-ttu-id="d3e12-120">取樣器狀態</span><span class="sxs-lookup"><span data-stu-id="d3e12-120">Sampler state</span></span>

| | |
|-|-|
| <span data-ttu-id="d3e12-121">**Filter**、 **AddressU**、 **AddressV**、 **AddressW**、 **MipLODBias**、 **MaxAnisotropy**、 **ComparisonFunc**、 **邊框**、 **MinLOD**、 **MaxLOD**</span><span class="sxs-lookup"><span data-stu-id="d3e12-121">**Filter**, **AddressU**, **AddressV**, **AddressW**, **MipLODBias**, **MaxAnisotropy**, **ComparisonFunc**, **BorderColor**, **MinLOD**, **MaxLOD**</span></span> | <span data-ttu-id="d3e12-122">[ **D3D10 取樣器 \_ \_ DESC** 的成員](/windows/desktop/api/D3D10/ns-d3d10-d3d10_sampler_desc)</span><span class="sxs-lookup"><span data-stu-id="d3e12-122">Members of [**D3D10\_SAMPLER\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_sampler_desc)</span></span> |

<span data-ttu-id="d3e12-123">如需範例，請參閱 [ (DIRECTX HLSL) 的取樣器類型 ](../direct3dhlsl/dx-graphics-hlsl-sampler.md) 。</span><span class="sxs-lookup"><span data-stu-id="d3e12-123">See [Sampler type (DirectX HLSL)](../direct3dhlsl/dx-graphics-hlsl-sampler.md) for examples.</span></span>

## <a name="effect-object-state"></a><span data-ttu-id="d3e12-124">效果物件狀態</span><span class="sxs-lookup"><span data-stu-id="d3e12-124">Effect object state</span></span>

| <span data-ttu-id="d3e12-125">此效果物件</span><span class="sxs-lookup"><span data-stu-id="d3e12-125">This effect object</span></span> | <span data-ttu-id="d3e12-126">對應至</span><span class="sxs-lookup"><span data-stu-id="d3e12-126">Maps to</span></span> |
|-|-|
| <span data-ttu-id="d3e12-127">RASTERIZERSTATE</span><span class="sxs-lookup"><span data-stu-id="d3e12-127">RASTERIZERSTATE</span></span> | <span data-ttu-id="d3e12-128">轉譯器 [狀態](#rasterizer-state) 狀態物件。</span><span class="sxs-lookup"><span data-stu-id="d3e12-128">A [Rasterizer State](#rasterizer-state) state object.</span></span> |
| <span data-ttu-id="d3e12-129">DEPTHSTENCILSTATE</span><span class="sxs-lookup"><span data-stu-id="d3e12-129">DEPTHSTENCILSTATE</span></span> | <span data-ttu-id="d3e12-130">[深度和樣板狀態](#depth-and-stencil-state)狀態物件。</span><span class="sxs-lookup"><span data-stu-id="d3e12-130">A [Depth and Stencil State](#depth-and-stencil-state) state object.</span></span> |
| <span data-ttu-id="d3e12-131">BLENDSTATE</span><span class="sxs-lookup"><span data-stu-id="d3e12-131">BLENDSTATE</span></span> | <span data-ttu-id="d3e12-132">[Blend 狀態](#blend-state)狀態物件。</span><span class="sxs-lookup"><span data-stu-id="d3e12-132">A [Blend State](#blend-state) state object.</span></span> |
| <span data-ttu-id="d3e12-133">VERTEXSHADER</span><span class="sxs-lookup"><span data-stu-id="d3e12-133">VERTEXSHADER</span></span> | <span data-ttu-id="d3e12-134">已編譯的頂點著色器物件。</span><span class="sxs-lookup"><span data-stu-id="d3e12-134">A compiled vertex shader object.</span></span> |
| <span data-ttu-id="d3e12-135">無效</span><span class="sxs-lookup"><span data-stu-id="d3e12-135">PIXELSHADER</span></span> | <span data-ttu-id="d3e12-136">編譯的圖元著色器物件。</span><span class="sxs-lookup"><span data-stu-id="d3e12-136">A compiled pixel shader object.</span></span> |
| <span data-ttu-id="d3e12-137">GEOMETRYSHADER</span><span class="sxs-lookup"><span data-stu-id="d3e12-137">GEOMETRYSHADER</span></span> | <span data-ttu-id="d3e12-138">已編譯的幾何著色器物件。</span><span class="sxs-lookup"><span data-stu-id="d3e12-138">A compiled geometry shader object.</span></span> |
| <span data-ttu-id="d3e12-139">DS \_ STENCILREF AB \_ BLENDFACTOR AB \_ SAMPLEMASK</span><span class="sxs-lookup"><span data-stu-id="d3e12-139">DS\_STENCILREF AB\_BLENDFACTOR AB\_SAMPLEMASK</span></span> | <span data-ttu-id="d3e12-140">[**D3D10 \_ PASS \_ DESC**](/windows/desktop/api/d3d10effect/ns-d3d10effect-d3d10_pass_desc)的成員。</span><span class="sxs-lookup"><span data-stu-id="d3e12-140">Members of [**D3D10\_PASS\_DESC**](/windows/desktop/api/d3d10effect/ns-d3d10effect-d3d10_pass_desc).</span></span> |

## <a name="defining-and-using-state-objects"></a><span data-ttu-id="d3e12-141">定義和使用狀態物件</span><span class="sxs-lookup"><span data-stu-id="d3e12-141">Defining and using state objects</span></span>

<span data-ttu-id="d3e12-142">系統會以下列格式在 FX 檔案中宣告狀態物件。</span><span class="sxs-lookup"><span data-stu-id="d3e12-142">State objects are declared in FX files in the following format.</span></span> <span data-ttu-id="d3e12-143">*StateObjectType* 是上面所列的其中一個狀態， *而成員* 名稱是將擁有非預設值之任何成員的名稱。</span><span class="sxs-lookup"><span data-stu-id="d3e12-143">*StateObjectType* is one of the states listed above, and *MemberName* is the name of any member that will have a non-default value.</span></span>

```
StateObjectType ObjectName {
 MemberName = value;
 ...
 MemberName = value;
};
```

<span data-ttu-id="d3e12-144">例如，若要設定 AlphaToCoverageEnable，並將 BlendEnable \[ 0 設為 FALSE 的 blend 狀態物件 \] ，則會使用下列程式碼。 </span><span class="sxs-lookup"><span data-stu-id="d3e12-144">For example, to set up a blend state object with AlphaToCoverageEnable and BlendEnable\[0\] set to **FALSE**, the following code would be used.</span></span>

```
BlendState NoBlend {
 AlphaToCoverageEnable = FALSE;
 BlendEnable[0] = FALSE;
};
```

<span data-ttu-id="d3e12-145">使用 [ (Direct3D 10) 的效果技巧語法 ](d3d10-effect-technique-syntax.md)中所述的其中一種 SetStateGroup 函式，將狀態物件套用至技術傳遞。</span><span class="sxs-lookup"><span data-stu-id="d3e12-145">The state object is applied to a technique pass using one of the SetStateGroup functions described in [Effect Technique Syntax (Direct3D 10)](d3d10-effect-technique-syntax.md).</span></span> <span data-ttu-id="d3e12-146">例如，若要套用上面所述的 BlendState 物件，則會使用下列程式碼。</span><span class="sxs-lookup"><span data-stu-id="d3e12-146">For example, to apply the BlendState object described above the following code would be used.</span></span>

```
SetBlendState( NoBlend, float4( 0.0f, 0.0f, 0.0f, 0.0f ), 0xFFFFFFFF );
```

<span data-ttu-id="d3e12-147">如需說明使用狀態的教學課程，請參閱 [狀態管理](https://msdn.microsoft.com/library/Ee416550(v=VS.85).aspx)。</span><span class="sxs-lookup"><span data-stu-id="d3e12-147">For a tutorial describing the use of states see [State management](https://msdn.microsoft.com/library/Ee416550(v=VS.85).aspx).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d3e12-148">相關主題</span><span class="sxs-lookup"><span data-stu-id="d3e12-148">Related topics</span></span>

* [<span data-ttu-id="d3e12-149">效果技巧語法</span><span class="sxs-lookup"><span data-stu-id="d3e12-149">Effect Technique Syntax</span></span>](d3d10-effect-technique-syntax.md)
* [<span data-ttu-id="d3e12-150"> (Direct3D 10) 的效果格式 </span><span class="sxs-lookup"><span data-stu-id="d3e12-150">Effect Format (Direct3D 10)</span></span>](d3d10-effect-format.md)
