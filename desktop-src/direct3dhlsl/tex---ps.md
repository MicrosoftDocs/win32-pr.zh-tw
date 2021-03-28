---
title: tex-ps
description: 使用色彩資料載入目的地登錄 (RGBA) 從材質取樣。 材質必須系結至特定的材質階段 (n) 使用 SetTexture。 紋理取樣是由 SetSamplerState 控制。
ms.assetid: vs|directx_sdk|~\tex___ps.htm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a3070883b167d26cf31f7d7f388f6bd3736a4bde
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933394"
---
# <a name="tex---ps"></a><span data-ttu-id="eb4d9-105">tex-ps</span><span class="sxs-lookup"><span data-stu-id="eb4d9-105">tex - ps</span></span>

<span data-ttu-id="eb4d9-106">使用色彩資料載入目的地登錄 (RGBA) 從材質取樣。</span><span class="sxs-lookup"><span data-stu-id="eb4d9-106">Loads the destination register with color data (RGBA) sampled from a texture.</span></span> <span data-ttu-id="eb4d9-107">材質必須系結至特定的材質階段 (n) 使用 [**SetTexture**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture)。</span><span class="sxs-lookup"><span data-stu-id="eb4d9-107">The texture must be bound to a particular texture stage (n) using [**SetTexture**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture).</span></span> <span data-ttu-id="eb4d9-108">紋理取樣是由 [**SetSamplerState**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setsamplerstate)控制。</span><span class="sxs-lookup"><span data-stu-id="eb4d9-108">Texture sampling is controlled by [**SetSamplerState**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setsamplerstate).</span></span>

## <a name="syntax"></a><span data-ttu-id="eb4d9-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="eb4d9-109">Syntax</span></span>



| <span data-ttu-id="eb4d9-110">tex dst</span><span class="sxs-lookup"><span data-stu-id="eb4d9-110">tex dst</span></span> |
|---------|



 

<span data-ttu-id="eb4d9-111">其中</span><span class="sxs-lookup"><span data-stu-id="eb4d9-111">where</span></span>

-   <span data-ttu-id="eb4d9-112">dst 是目的地註冊。</span><span class="sxs-lookup"><span data-stu-id="eb4d9-112">dst is the destination register.</span></span>

## <a name="remarks"></a><span data-ttu-id="eb4d9-113">備註</span><span class="sxs-lookup"><span data-stu-id="eb4d9-113">Remarks</span></span>



| <span data-ttu-id="eb4d9-114">圖元著色器版本</span><span class="sxs-lookup"><span data-stu-id="eb4d9-114">Pixel shader versions</span></span> | <span data-ttu-id="eb4d9-115">1\_1</span><span class="sxs-lookup"><span data-stu-id="eb4d9-115">1\_1</span></span> | <span data-ttu-id="eb4d9-116">1\_2</span><span class="sxs-lookup"><span data-stu-id="eb4d9-116">1\_2</span></span> | <span data-ttu-id="eb4d9-117">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="eb4d9-117">1\_3</span></span> | <span data-ttu-id="eb4d9-118">1\_4</span><span class="sxs-lookup"><span data-stu-id="eb4d9-118">1\_4</span></span> | <span data-ttu-id="eb4d9-119">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="eb4d9-119">2\_0</span></span> | <span data-ttu-id="eb4d9-120">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="eb4d9-120">2\_x</span></span> | <span data-ttu-id="eb4d9-121">2個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="eb4d9-121">2\_sw</span></span> | <span data-ttu-id="eb4d9-122">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="eb4d9-122">3\_0</span></span> | <span data-ttu-id="eb4d9-123">3個 \_ sw</span><span class="sxs-lookup"><span data-stu-id="eb4d9-123">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="eb4d9-124">tex</span><span class="sxs-lookup"><span data-stu-id="eb4d9-124">tex</span></span>                   | <span data-ttu-id="eb4d9-125">x</span><span class="sxs-lookup"><span data-stu-id="eb4d9-125">x</span></span>    | <span data-ttu-id="eb4d9-126">x</span><span class="sxs-lookup"><span data-stu-id="eb4d9-126">x</span></span>    | <span data-ttu-id="eb4d9-127">x</span><span class="sxs-lookup"><span data-stu-id="eb4d9-127">x</span></span>    |      |      |      |       |      |       |



 

<span data-ttu-id="eb4d9-128">目的地暫存器編號會指定紋理階段號碼。</span><span class="sxs-lookup"><span data-stu-id="eb4d9-128">The destination register number specifies the texture stage number.</span></span>

<span data-ttu-id="eb4d9-129">紋理取樣使用材質座標來查閱（或取樣）位於指定之 (u、v、w、q) 座標的色彩值，同時將材質階段狀態屬性納入考慮。</span><span class="sxs-lookup"><span data-stu-id="eb4d9-129">Texture sampling uses texture coordinates to look up, or sample, a color value at the specified (u,v,w,q) coordinates while taking into account the texture stage state attributes.</span></span>

<span data-ttu-id="eb4d9-130">材質座標資料是從頂點材質座標資料中插入，並且與特定的材質階段相關聯。</span><span class="sxs-lookup"><span data-stu-id="eb4d9-130">The texture coordinate data is interpolated from the vertex texture coordinate data and is associated with a specific texture stage.</span></span> <span data-ttu-id="eb4d9-131">預設關聯是紋理階段編號和材質座標宣告順序之間的一對一對應。</span><span class="sxs-lookup"><span data-stu-id="eb4d9-131">The default association is a one-to-one mapping between texture stage number and texture coordinate declaration order.</span></span> <span data-ttu-id="eb4d9-132">這表示，以頂點格式定義的第一組材質座標預設會與材質階段0相關聯。</span><span class="sxs-lookup"><span data-stu-id="eb4d9-132">This means that the first set of texture coordinates defined in the vertex format are by default associated with texture stage 0.</span></span>

<span data-ttu-id="eb4d9-133">材質座標可以與使用兩個技術的任何階段相關聯。</span><span class="sxs-lookup"><span data-stu-id="eb4d9-133">Texture coordinates may be associated with any stage using two techniques.</span></span> <span data-ttu-id="eb4d9-134">使用固定的函式頂點著色器或固定函式管線時，紋理階段狀態旗標 TSS \_ TEXCOORDINDEX 可以在 [**SetTextureStageState**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) 中用來將座標關聯至階段。</span><span class="sxs-lookup"><span data-stu-id="eb4d9-134">When using a fixed function vertex shader or the fixed function pipeline, the texture stage state flag TSS\_TEXCOORDINDEX can be used in [**SetTextureStageState**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) to associate coordinates to a stage.</span></span> <span data-ttu-id="eb4d9-135">否則，當使用可程式化頂點著色器時，頂點著色器 oTn 暫存器會輸出材質座標。</span><span class="sxs-lookup"><span data-stu-id="eb4d9-135">Otherwise, the texture coordinates are output by the vertex shader oTₙ registers when using a programmable vertex shader.</span></span>

## <a name="related-topics"></a><span data-ttu-id="eb4d9-136">相關主題</span><span class="sxs-lookup"><span data-stu-id="eb4d9-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eb4d9-137">圖元著色器指示</span><span class="sxs-lookup"><span data-stu-id="eb4d9-137">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 