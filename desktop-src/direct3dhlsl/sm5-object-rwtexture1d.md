---
title: RWTexture1D
description: 讀取/寫入資源。 |RWTexture1D
ms.assetid: 47866e5a-b26b-4264-9291-c8940882d662
keywords:
- RWTexture1D HLSL
topic_type:
- apiref
api_name:
- RWTexture1D
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 695b73cc14541505ee1b2d4391aac2d145eec8d7
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104973948"
---
# <a name="rwtexture1d"></a><span data-ttu-id="27a13-105">RWTexture1D</span><span class="sxs-lookup"><span data-stu-id="27a13-105">RWTexture1D</span></span>

<span data-ttu-id="27a13-106">讀取/寫入資源。</span><span class="sxs-lookup"><span data-stu-id="27a13-106">A read/write resource.</span></span>



| <span data-ttu-id="27a13-107">方法</span><span class="sxs-lookup"><span data-stu-id="27a13-107">Method</span></span>                                                        | <span data-ttu-id="27a13-108">描述</span><span class="sxs-lookup"><span data-stu-id="27a13-108">Description</span></span>                   |
|---------------------------------------------------------------|-------------------------------|
| [<span data-ttu-id="27a13-109">**GetDimensions**</span><span class="sxs-lookup"><span data-stu-id="27a13-109">**GetDimensions**</span></span>](sm5-object-rwtexture1d-getdimensions.md) | <span data-ttu-id="27a13-110">取得資源維度。</span><span class="sxs-lookup"><span data-stu-id="27a13-110">Gets the resource dimensions.</span></span> |
| [<span data-ttu-id="27a13-111">**載入**</span><span class="sxs-lookup"><span data-stu-id="27a13-111">**Load**</span></span>](rwtexture1d-load.md)                              | <span data-ttu-id="27a13-112">讀取紋理資料。</span><span class="sxs-lookup"><span data-stu-id="27a13-112">Reads texture data.</span></span>           |
| <span data-ttu-id="27a13-113">[**運算子\[\]**](sm5-object-rwtexture1d-operatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="27a13-113">[**Operator\[\]**](sm5-object-rwtexture1d-operatorindex.md)</span></span>  | <span data-ttu-id="27a13-114">取得資源變數。</span><span class="sxs-lookup"><span data-stu-id="27a13-114">Gets a resource variable.</span></span>     |



 

<span data-ttu-id="27a13-115">您可以在 **RWTexture1D** 物件前面加上儲存類別 **globallycoherent**。</span><span class="sxs-lookup"><span data-stu-id="27a13-115">You can prefix **RWTexture1D** objects with the storage class **globallycoherent**.</span></span> <span data-ttu-id="27a13-116">此儲存類別會造成記憶體阻礙和同步處理，以排清整個 GPU 上的資料，讓其他群組可以看到寫入。</span><span class="sxs-lookup"><span data-stu-id="27a13-116">This storage class causes memory barriers and syncs to flush data across the entire GPU such that other groups can see writes.</span></span> <span data-ttu-id="27a13-117">如果沒有這個規範，記憶體屏障或同步將只會在目前群組內排清 UAV。</span><span class="sxs-lookup"><span data-stu-id="27a13-117">Without this specifier, a memory barrier or sync will flush a UAV only within the current group.</span></span>

<span data-ttu-id="27a13-118">**RWTexture1D** 物件需要物件的宣告語句中的元素類型。</span><span class="sxs-lookup"><span data-stu-id="27a13-118">A **RWTexture1D** object requires an element type in a declaration statement for the object.</span></span> <span data-ttu-id="27a13-119">例如，下列宣告是正確的：</span><span class="sxs-lookup"><span data-stu-id="27a13-119">For example, the following declaration is correct:</span></span>


```
RWTexture1D<float> tex;
```



<span data-ttu-id="27a13-120">由於 **RWTexture1D** 物件是 UAV 類型的物件，因此它的屬性與著色器資源檢視不同 (SRV) 型別物件，例如 [**Texture1D**](sm5-object-texture1d.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="27a13-120">Because a **RWTexture1D** object is a UAV-type object, its properties differ from a shader resource view (SRV)-type object, such as a [**Texture1D**](sm5-object-texture1d.md) object.</span></span> <span data-ttu-id="27a13-121">例如，您可以讀取和寫入 **RWTexture1D** 物件，但只能從 **Texture1D** 物件讀取。</span><span class="sxs-lookup"><span data-stu-id="27a13-121">For example, you can read from and write to a **RWTexture1D** object, but you can only read from a **Texture1D** object.</span></span>

<span data-ttu-id="27a13-122">**RWTexture1D** 物件無法使用來自 [**Texture1D**](sm5-object-texture1d.md)物件的方法，例如 [範例](dx-graphics-hlsl-to-sample.md)。</span><span class="sxs-lookup"><span data-stu-id="27a13-122">A **RWTexture1D** object cannot use methods from a [**Texture1D**](sm5-object-texture1d.md) object, such as [Sample](dx-graphics-hlsl-to-sample.md).</span></span> <span data-ttu-id="27a13-123">不過，因為您可以為相同的資源建立多個檢視類型，所以您可以將多個紋理類型宣告為多個著色器中的單一材質。</span><span class="sxs-lookup"><span data-stu-id="27a13-123">However, because you can create multiple view types to the same resource, you can declare multiple texture types as a single texture in multiple shaders.</span></span> <span data-ttu-id="27a13-124">例如，您可以在計算著色器中宣告並使用 **RWTexture1D** 物件做為 *tex* ，然後在圖元著色器中宣告並使用 **Texture1D** 物件做為 *tex* 。</span><span class="sxs-lookup"><span data-stu-id="27a13-124">For example, you can declare and use a **RWTexture1D** object as *tex* in a compute shader and then declare and use a **Texture1D** object as *tex* in a pixel shader.</span></span>

> [!Note]  
> <span data-ttu-id="27a13-125">當您在相同的資源中建立多個檢視類型時，執行時間會強制執行特定的使用模式。</span><span class="sxs-lookup"><span data-stu-id="27a13-125">The runtime enforces certain usage patterns when you create multiple view types to the same resource.</span></span> <span data-ttu-id="27a13-126">例如，執行時間不允許您同時讓相同資源的資源和 SRV 對應的 UAV 對應同時啟用。</span><span class="sxs-lookup"><span data-stu-id="27a13-126">For example, the runtime does not allow you to have both a UAV mapping for a resource and SRV mapping for the same resource active at the same time.</span></span>

 

## <a name="minimum-shader-model"></a><span data-ttu-id="27a13-127">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="27a13-127">Minimum Shader Model</span></span>

<span data-ttu-id="27a13-128">下列著色器模型支援此物件。</span><span class="sxs-lookup"><span data-stu-id="27a13-128">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="27a13-129">著色器模型</span><span class="sxs-lookup"><span data-stu-id="27a13-129">Shader Model</span></span>                                                                | <span data-ttu-id="27a13-130">支援</span><span class="sxs-lookup"><span data-stu-id="27a13-130">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="27a13-131">[著色器模型 5](d3d11-graphics-reference-sm5.md) 和更新版本的著色器模型</span><span class="sxs-lookup"><span data-stu-id="27a13-131">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="27a13-132">是</span><span class="sxs-lookup"><span data-stu-id="27a13-132">yes</span></span>       |



 

<span data-ttu-id="27a13-133">下列著色器類型支援此物件：</span><span class="sxs-lookup"><span data-stu-id="27a13-133">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="27a13-134">頂點</span><span class="sxs-lookup"><span data-stu-id="27a13-134">Vertex</span></span> | <span data-ttu-id="27a13-135">船體</span><span class="sxs-lookup"><span data-stu-id="27a13-135">Hull</span></span> | <span data-ttu-id="27a13-136">網域</span><span class="sxs-lookup"><span data-stu-id="27a13-136">Domain</span></span> | <span data-ttu-id="27a13-137">幾何</span><span class="sxs-lookup"><span data-stu-id="27a13-137">Geometry</span></span> | <span data-ttu-id="27a13-138">像素</span><span class="sxs-lookup"><span data-stu-id="27a13-138">Pixel</span></span> | <span data-ttu-id="27a13-139">計算</span><span class="sxs-lookup"><span data-stu-id="27a13-139">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="27a13-140">x</span><span class="sxs-lookup"><span data-stu-id="27a13-140">x</span></span>     | <span data-ttu-id="27a13-141">x</span><span class="sxs-lookup"><span data-stu-id="27a13-141">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="27a13-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="27a13-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27a13-143">著色器模型5物件</span><span class="sxs-lookup"><span data-stu-id="27a13-143">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 




