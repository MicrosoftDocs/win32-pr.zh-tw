---
description: 效果狀態是運算式形式的成對名稱/值。
ms.assetid: 4612c6bd-bc1f-42ad-8465-c0d4b577d1db
title: '效果狀態群組 (Direct3D 10) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4617f786b984c96b271600e05b3ea8da9b5701fd
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335565"
---
# <a name="effect-state-groups-direct3d-10"></a><span data-ttu-id="def38-103">效果狀態群組 (Direct3D 10) </span><span class="sxs-lookup"><span data-stu-id="def38-103">Effect state groups (Direct3D 10)</span></span>

<span data-ttu-id="def38-104">效果狀態是運算式形式的成對名稱/值。</span><span class="sxs-lookup"><span data-stu-id="def38-104">Effect states are name-value pairs in the form of an expression.</span></span>

## <a name="blend-state"></a><span data-ttu-id="def38-105">Blend 狀態</span><span class="sxs-lookup"><span data-stu-id="def38-105">Blend state</span></span>

| <span data-ttu-id="def38-106">效果狀態</span><span class="sxs-lookup"><span data-stu-id="def38-106">Effect state</span></span> | <span data-ttu-id="def38-107">Group</span><span class="sxs-lookup"><span data-stu-id="def38-107">Group</span></span> |
|-|-|
| <span data-ttu-id="def38-108">**ALPHATOCOVERAGEENABLE**、 **BLENDENABLE**、 **SRCBLEND**、 **DESTBLEND**、 **BLENDOP**、 **SRCBLENDALPHA**、 **DESTBLENDALPHA**、 **BLENDOPALPHA**、 **RENDERTARGETWRITEMASK**</span><span class="sxs-lookup"><span data-stu-id="def38-108">**ALPHATOCOVERAGEENABLE**, **BLENDENABLE**, **SRCBLEND**, **DESTBLEND**, **BLENDOP**, **SRCBLENDALPHA**, **DESTBLENDALPHA**, **BLENDOPALPHA**, **RENDERTARGETWRITEMASK**</span></span> | <span data-ttu-id="def38-109">[ **D3D10 \_ BLEND \_ DESC** 的成員](/windows/desktop/api/D3D10/ns-d3d10-d3d10_blend_desc)</span><span class="sxs-lookup"><span data-stu-id="def38-109">Members of [**D3D10\_BLEND\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_blend_desc)</span></span> |

## <a name="depth-and-stencil-state"></a><span data-ttu-id="def38-110">深度和樣板狀態</span><span class="sxs-lookup"><span data-stu-id="def38-110">Depth and stencil state</span></span>

| <span data-ttu-id="def38-111">效果狀態</span><span class="sxs-lookup"><span data-stu-id="def38-111">Effect state</span></span>| <span data-ttu-id="def38-112">Group</span><span class="sxs-lookup"><span data-stu-id="def38-112">Group</span></span> |
|-|-|
| <span data-ttu-id="def38-113">**DEPTHENABLE**、 **DEPTHWRITEMASK**、 **DEPTHFUNC**、 **STENCILENABLE**、 **STENCILREADMASK**、 **STENCILWRITEMASK**</span><span class="sxs-lookup"><span data-stu-id="def38-113">**DEPTHENABLE**, **DEPTHWRITEMASK**, **DEPTHFUNC**, **STENCILENABLE**, **STENCILREADMASK**, **STENCILWRITEMASK**</span></span> | <span data-ttu-id="def38-114">[ **D3D10 深度樣板 \_ \_ \_ DESC** 的成員](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencil_desc)</span><span class="sxs-lookup"><span data-stu-id="def38-114">Members of [**D3D10\_DEPTH\_STENCIL\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencil_desc)</span></span> |
| <span data-ttu-id="def38-115">**FRONTFACESTENCILFAIL**、 **FRONTFACESTENCILZFAIL**、 **FRONTFACESTENCILPASS**、 **FRONTFACESTENCILFUNC**、 **BACKFACESTENCILFAIL**、 **BACKFACESTENCILZFAIL**、 **BACKFACESTENCILPASS**、 **BACKFACESTENCILFUNC**</span><span class="sxs-lookup"><span data-stu-id="def38-115">**FRONTFACESTENCILFAIL**, **FRONTFACESTENCILZFAIL**, **FRONTFACESTENCILPASS**, **FRONTFACESTENCILFUNC**, **BACKFACESTENCILFAIL**, **BACKFACESTENCILZFAIL**, **BACKFACESTENCILPASS**, **BACKFACESTENCILFUNC**</span></span> | <span data-ttu-id="def38-116">[ **D3D10 \_ 深度 \_ STENCILOP \_ DESC** 的成員](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencilop_desc)</span><span class="sxs-lookup"><span data-stu-id="def38-116">Member of [**D3D10\_DEPTH\_STENCILOP\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencilop_desc)</span></span> |

## <a name="rasterizer-state"></a><span data-ttu-id="def38-117">轉譯器狀態</span><span class="sxs-lookup"><span data-stu-id="def38-117">Rasterizer state</span></span>

| <span data-ttu-id="def38-118">效果狀態</span><span class="sxs-lookup"><span data-stu-id="def38-118">Effect state</span></span>| <span data-ttu-id="def38-119">Group</span><span class="sxs-lookup"><span data-stu-id="def38-119">Group</span></span> |
|-|-|
| <span data-ttu-id="def38-120">FILLMODE</span><span class="sxs-lookup"><span data-stu-id="def38-120">FILLMODE</span></span> | [<span data-ttu-id="def38-121">**D3D10 \_ 填滿 \_ 模式**</span><span class="sxs-lookup"><span data-stu-id="def38-121">**D3D10\_FILL\_MODE**</span></span>](/windows/desktop/api/D3D10/ne-d3d10-d3d10_fill_mode) |
| <span data-ttu-id="def38-122">CULLMODE</span><span class="sxs-lookup"><span data-stu-id="def38-122">CULLMODE</span></span> | [<span data-ttu-id="def38-123">**D3D10 的 \_ 挑選 \_ 模式**</span><span class="sxs-lookup"><span data-stu-id="def38-123">**D3D10\_CULL\_MODE**</span></span>](/windows/desktop/api/D3D10/ne-d3d10-d3d10_cull_mode) |
| <span data-ttu-id="def38-124">**FRONTCOUNTERCLOCKWISE**、 **DEPTHBIAS**、 **DEPTHBIASCLAMP**、 **SLOPESCALEDDEPTHBIAS**、 **ZCLIPENABLE**、 **SCISSORENABLE**、 **MULTISAMPLEENABLE**、 **ANTIALIASEDLINEENABLE**</span><span class="sxs-lookup"><span data-stu-id="def38-124">**FRONTCOUNTERCLOCKWISE**, **DEPTHBIAS**, **DEPTHBIASCLAMP**, **SLOPESCALEDDEPTHBIAS**, **ZCLIPENABLE**, **SCISSORENABLE**, **MULTISAMPLEENABLE**, **ANTIALIASEDLINEENABLE**</span></span> | <span data-ttu-id="def38-125">D3D10 轉譯器 [ **\_ \_ DESC** 的成員](/windows/desktop/api/D3D10/ns-d3d10-d3d10_rasterizer_desc)</span><span class="sxs-lookup"><span data-stu-id="def38-125">Members of [**D3D10\_RASTERIZER\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_rasterizer_desc)</span></span> |

## <a name="sampler-state"></a><span data-ttu-id="def38-126">取樣器狀態</span><span class="sxs-lookup"><span data-stu-id="def38-126">Sampler state</span></span>

| <span data-ttu-id="def38-127">效果狀態</span><span class="sxs-lookup"><span data-stu-id="def38-127">Effect state</span></span> | <span data-ttu-id="def38-128">Group</span><span class="sxs-lookup"><span data-stu-id="def38-128">Group</span></span> |
|-|-|
| <span data-ttu-id="def38-129">**Filter**、 **AddressU**、 **AddressV**、 **AddressW**、 **MipLODBias**、 **MaxAnisotropy**、 **ComparisonFunc**、 **邊框**、 **MinLOD**、 **MaxLOD**</span><span class="sxs-lookup"><span data-stu-id="def38-129">**Filter**, **AddressU**, **AddressV**, **AddressW**, **MipLODBias**, **MaxAnisotropy**, **ComparisonFunc**, **BorderColor**, **MinLOD**, **MaxLOD**</span></span> | <span data-ttu-id="def38-130">[ **D3D10 取樣器 \_ \_ DESC** 的成員](/windows/desktop/api/D3D10/ns-d3d10-d3d10_sampler_desc)</span><span class="sxs-lookup"><span data-stu-id="def38-130">Members of [**D3D10\_SAMPLER\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_sampler_desc)</span></span> |

<span data-ttu-id="def38-131">如需範例，請參閱 [ (DIRECTX HLSL) 的取樣器類型 ](../direct3dhlsl/dx-graphics-hlsl-sampler.md) 。</span><span class="sxs-lookup"><span data-stu-id="def38-131">See [Sampler type (DirectX HLSL)](../direct3dhlsl/dx-graphics-hlsl-sampler.md) for examples.</span></span>

## <a name="effect-object-state"></a><span data-ttu-id="def38-132">效果物件狀態</span><span class="sxs-lookup"><span data-stu-id="def38-132">Effect object state</span></span>

| <span data-ttu-id="def38-133">此效果物件</span><span class="sxs-lookup"><span data-stu-id="def38-133">This effect object</span></span> | <span data-ttu-id="def38-134">對應至</span><span class="sxs-lookup"><span data-stu-id="def38-134">Maps to</span></span> |
|-|-|
| <span data-ttu-id="def38-135">RASTERIZERSTATE</span><span class="sxs-lookup"><span data-stu-id="def38-135">RASTERIZERSTATE</span></span> | <span data-ttu-id="def38-136">轉譯器 [狀態](#rasterizer-state) 狀態物件。</span><span class="sxs-lookup"><span data-stu-id="def38-136">A [Rasterizer State](#rasterizer-state) state object.</span></span> |
| <span data-ttu-id="def38-137">DEPTHSTENCILSTATE</span><span class="sxs-lookup"><span data-stu-id="def38-137">DEPTHSTENCILSTATE</span></span> | <span data-ttu-id="def38-138">[深度和樣板狀態](#depth-and-stencil-state)狀態物件。</span><span class="sxs-lookup"><span data-stu-id="def38-138">A [Depth and Stencil State](#depth-and-stencil-state) state object.</span></span> |
| <span data-ttu-id="def38-139">BLENDSTATE</span><span class="sxs-lookup"><span data-stu-id="def38-139">BLENDSTATE</span></span> | <span data-ttu-id="def38-140">[Blend 狀態](#blend-state)狀態物件。</span><span class="sxs-lookup"><span data-stu-id="def38-140">A [Blend State](#blend-state) state object.</span></span> |
| <span data-ttu-id="def38-141">VERTEXSHADER</span><span class="sxs-lookup"><span data-stu-id="def38-141">VERTEXSHADER</span></span> | <span data-ttu-id="def38-142">已編譯的頂點著色器物件。</span><span class="sxs-lookup"><span data-stu-id="def38-142">A compiled vertex shader object.</span></span> |
| <span data-ttu-id="def38-143">無效</span><span class="sxs-lookup"><span data-stu-id="def38-143">PIXELSHADER</span></span> | <span data-ttu-id="def38-144">編譯的圖元著色器物件。</span><span class="sxs-lookup"><span data-stu-id="def38-144">A compiled pixel shader object.</span></span> |
| <span data-ttu-id="def38-145">GEOMETRYSHADER</span><span class="sxs-lookup"><span data-stu-id="def38-145">GEOMETRYSHADER</span></span> | <span data-ttu-id="def38-146">已編譯的幾何著色器物件。</span><span class="sxs-lookup"><span data-stu-id="def38-146">A compiled geometry shader object.</span></span> |
| <span data-ttu-id="def38-147">DS \_ STENCILREF AB \_ BLENDFACTOR AB \_ SAMPLEMASK</span><span class="sxs-lookup"><span data-stu-id="def38-147">DS\_STENCILREF AB\_BLENDFACTOR AB\_SAMPLEMASK</span></span> | <span data-ttu-id="def38-148">[**D3D10 \_ PASS \_ DESC**](/windows/desktop/api/d3d10effect/ns-d3d10effect-d3d10_pass_desc)的成員。</span><span class="sxs-lookup"><span data-stu-id="def38-148">Members of [**D3D10\_PASS\_DESC**](/windows/desktop/api/d3d10effect/ns-d3d10effect-d3d10_pass_desc).</span></span> |

## <a name="defining-and-using-state-objects"></a><span data-ttu-id="def38-149">定義和使用狀態物件</span><span class="sxs-lookup"><span data-stu-id="def38-149">Defining and using state objects</span></span>

<span data-ttu-id="def38-150">系統會以下列格式在 FX 檔案中宣告狀態物件。</span><span class="sxs-lookup"><span data-stu-id="def38-150">State objects are declared in FX files in the following format.</span></span> <span data-ttu-id="def38-151">*StateObjectType* 是上面所列的其中一個狀態， *而成員* 名稱是將擁有非預設值之任何成員的名稱。</span><span class="sxs-lookup"><span data-stu-id="def38-151">*StateObjectType* is one of the states listed above, and *MemberName* is the name of any member that will have a non-default value.</span></span>

```
StateObjectType ObjectName {
 MemberName = value;
 ...
 MemberName = value;
};
```

<span data-ttu-id="def38-152">例如，若要設定 AlphaToCoverageEnable，並將 BlendEnable \[ 0 設為 FALSE 的 blend 狀態物件 \] ，則會使用下列程式碼。 </span><span class="sxs-lookup"><span data-stu-id="def38-152">For example, to set up a blend state object with AlphaToCoverageEnable and BlendEnable\[0\] set to **FALSE**, the following code would be used.</span></span>

```
BlendState NoBlend {
 AlphaToCoverageEnable = FALSE;
 BlendEnable[0] = FALSE;
};
```

<span data-ttu-id="def38-153">使用 [ (Direct3D 10) 的效果技巧語法 ](d3d10-effect-technique-syntax.md)中所述的其中一種 SetStateGroup 函式，將狀態物件套用至技術傳遞。</span><span class="sxs-lookup"><span data-stu-id="def38-153">The state object is applied to a technique pass using one of the SetStateGroup functions described in [Effect Technique Syntax (Direct3D 10)](d3d10-effect-technique-syntax.md).</span></span> <span data-ttu-id="def38-154">例如，若要套用上面所述的 BlendState 物件，則會使用下列程式碼。</span><span class="sxs-lookup"><span data-stu-id="def38-154">For example, to apply the BlendState object described above the following code would be used.</span></span>

```
SetBlendState( NoBlend, float4( 0.0f, 0.0f, 0.0f, 0.0f ), 0xFFFFFFFF );
```

<span data-ttu-id="def38-155">如需說明使用狀態的教學課程，請參閱 [狀態管理](https://msdn.microsoft.com/library/Ee416550(v=VS.85).aspx)。</span><span class="sxs-lookup"><span data-stu-id="def38-155">For a tutorial describing the use of states see [State management](https://msdn.microsoft.com/library/Ee416550(v=VS.85).aspx).</span></span>

## <a name="related-topics"></a><span data-ttu-id="def38-156">相關主題</span><span class="sxs-lookup"><span data-stu-id="def38-156">Related topics</span></span>

* [<span data-ttu-id="def38-157">效果技巧語法</span><span class="sxs-lookup"><span data-stu-id="def38-157">Effect Technique Syntax</span></span>](d3d10-effect-technique-syntax.md)
* [<span data-ttu-id="def38-158"> (Direct3D 10) 的效果格式 </span><span class="sxs-lookup"><span data-stu-id="def38-158">Effect Format (Direct3D 10)</span></span>](d3d10-effect-format.md)
