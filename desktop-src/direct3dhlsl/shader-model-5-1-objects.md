---
title: 著色器模型5.1 物件
description: 下列物件已新增至著色器模型5.1。
ms.assetid: 2958618D-54C6-4860-9910-B45AAB73CCFD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c56fbe035f63bd8f25a8b34377c333c2ce9946c
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/26/2021
ms.locfileid: "107993855"
---
# <a name="shader-model-51-objects"></a><span data-ttu-id="ae70b-103">著色器模型5.1 物件</span><span class="sxs-lookup"><span data-stu-id="ae70b-103">Shader Model 5.1 Objects</span></span>

<span data-ttu-id="ae70b-104">下列物件已新增至著色器模型5.1。</span><span class="sxs-lookup"><span data-stu-id="ae70b-104">The following objects have been added to shader model 5.1.</span></span>

<span data-ttu-id="ae70b-105">針對 (D3D 11.3 和 D3D12) 提供的轉譯器 [順序視圖](/windows/desktop/direct3d11/rasterizer-order-views) ，下列物件是新的，而且只能在圖元著色器中使用。</span><span class="sxs-lookup"><span data-stu-id="ae70b-105">For the [Rasterizer Order Views](/windows/desktop/direct3d11/rasterizer-order-views) (available in D3D11.3 and D3D12), the following objects are new, and are only allowed in the pixel shader.</span></span> <span data-ttu-id="ae70b-106">請注意，其支援的方法與對應的 UAV 物件相同。</span><span class="sxs-lookup"><span data-stu-id="ae70b-106">Note that the methods they support are identical to the corresponding UAV objects.</span></span>



|                                    |                                                               |
|------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="ae70b-107">轉譯器物件</span><span class="sxs-lookup"><span data-stu-id="ae70b-107">Rasterizer Object</span></span>                  | <span data-ttu-id="ae70b-108">UAV 物件</span><span class="sxs-lookup"><span data-stu-id="ae70b-108">UAV Object</span></span>                                                    |
| <span data-ttu-id="ae70b-109">RasterizerOrderedBuffer</span><span class="sxs-lookup"><span data-stu-id="ae70b-109">RasterizerOrderedBuffer</span></span>            | [<span data-ttu-id="ae70b-110">**RWBuffer**</span><span class="sxs-lookup"><span data-stu-id="ae70b-110">**RWBuffer**</span></span>](sm5-object-rwbuffer.md)                       |
| <span data-ttu-id="ae70b-111">RasterizerOrderedByteAddressBuffer</span><span class="sxs-lookup"><span data-stu-id="ae70b-111">RasterizerOrderedByteAddressBuffer</span></span> | [<span data-ttu-id="ae70b-112">**RWByteAddressBuffer**</span><span class="sxs-lookup"><span data-stu-id="ae70b-112">**RWByteAddressBuffer**</span></span>](sm5-object-rwbyteaddressbuffer.md) |
| <span data-ttu-id="ae70b-113">RasterizerOrderedStructuredBuffer</span><span class="sxs-lookup"><span data-stu-id="ae70b-113">RasterizerOrderedStructuredBuffer</span></span>  | [<span data-ttu-id="ae70b-114">**RWStructuredBuffer**</span><span class="sxs-lookup"><span data-stu-id="ae70b-114">**RWStructuredBuffer**</span></span>](sm5-object-rwstructuredbuffer.md)   |
| <span data-ttu-id="ae70b-115">RasterizerOrderedTexture1D</span><span class="sxs-lookup"><span data-stu-id="ae70b-115">RasterizerOrderedTexture1D</span></span>         | [<span data-ttu-id="ae70b-116">**RWTexture1D**</span><span class="sxs-lookup"><span data-stu-id="ae70b-116">**RWTexture1D**</span></span>](sm5-object-rwtexture1d.md)                 |
| <span data-ttu-id="ae70b-117">RasterizerOrderedTexture1DArray</span><span class="sxs-lookup"><span data-stu-id="ae70b-117">RasterizerOrderedTexture1DArray</span></span>    | [<span data-ttu-id="ae70b-118">**RWTexture1DArray**</span><span class="sxs-lookup"><span data-stu-id="ae70b-118">**RWTexture1DArray**</span></span>](sm5-object-rwtexture1darray.md)       |
| <span data-ttu-id="ae70b-119">RasterizerOrderedTexture2D</span><span class="sxs-lookup"><span data-stu-id="ae70b-119">RasterizerOrderedTexture2D</span></span>         | [<span data-ttu-id="ae70b-120">**RWTexture2D**</span><span class="sxs-lookup"><span data-stu-id="ae70b-120">**RWTexture2D**</span></span>](sm5-object-rwtexture2d.md)                 |
| <span data-ttu-id="ae70b-121">RasterizerOrderedTexture2DArray</span><span class="sxs-lookup"><span data-stu-id="ae70b-121">RasterizerOrderedTexture2DArray</span></span>    | [<span data-ttu-id="ae70b-122">**RWTexture2DArray**</span><span class="sxs-lookup"><span data-stu-id="ae70b-122">**RWTexture2DArray**</span></span>](sm5-object-rwtexture2darray.md)       |
| <span data-ttu-id="ae70b-123">RasterizerOrderedTexture3D</span><span class="sxs-lookup"><span data-stu-id="ae70b-123">RasterizerOrderedTexture3D</span></span>         | [<span data-ttu-id="ae70b-124">**RWTexture3D**</span><span class="sxs-lookup"><span data-stu-id="ae70b-124">**RWTexture3D**</span></span>](sm5-object-rwtexture3d.md)                 |



 

## <a name="related-topics"></a><span data-ttu-id="ae70b-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="ae70b-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ae70b-126">著色器模型5。1</span><span class="sxs-lookup"><span data-stu-id="ae70b-126">Shader Model 5.1</span></span>](shader-model-5-1.md)
</dt> <dt>

[<span data-ttu-id="ae70b-127">適用于 Direct3D 12 的 HLSL 著色器模型5.1 功能</span><span class="sxs-lookup"><span data-stu-id="ae70b-127">HLSL Shader Model 5.1 Features for Direct3D 12</span></span>](hlsl-shader-model-5-1-features-for-direct3d-12.md)
</dt> </dl>

 

 
