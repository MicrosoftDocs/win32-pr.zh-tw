---
title: RWTexture2D
description: 讀取/寫入資源。 |RWTexture2D
ms.assetid: 19b383f1-c787-4c20-b77a-60ef9f212b9f
keywords:
- RWTexture2D HLSL
topic_type:
- apiref
api_name:
- RWTexture2D
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ccdeae4dd47d3ad4bf5d756c2ca362033eae6814
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104322164"
---
# <a name="rwtexture2d"></a><span data-ttu-id="22024-105">RWTexture2D</span><span class="sxs-lookup"><span data-stu-id="22024-105">RWTexture2D</span></span>

<span data-ttu-id="22024-106">讀取/寫入資源。</span><span class="sxs-lookup"><span data-stu-id="22024-106">A read/write resource.</span></span>



| <span data-ttu-id="22024-107">方法</span><span class="sxs-lookup"><span data-stu-id="22024-107">Method</span></span>                                                        | <span data-ttu-id="22024-108">描述</span><span class="sxs-lookup"><span data-stu-id="22024-108">Description</span></span>                   |
|---------------------------------------------------------------|-------------------------------|
| [<span data-ttu-id="22024-109">**GetDimensions**</span><span class="sxs-lookup"><span data-stu-id="22024-109">**GetDimensions**</span></span>](sm5-object-rwtexture2d-getdimensions.md) | <span data-ttu-id="22024-110">取得資源維度。</span><span class="sxs-lookup"><span data-stu-id="22024-110">Gets the resource dimensions.</span></span> |
| [<span data-ttu-id="22024-111">**載入**</span><span class="sxs-lookup"><span data-stu-id="22024-111">**Load**</span></span>](rwtexture2d-load.md)                              | <span data-ttu-id="22024-112">讀取紋理資料。</span><span class="sxs-lookup"><span data-stu-id="22024-112">Reads texture data.</span></span>           |
| <span data-ttu-id="22024-113">[**運算子\[\]**](sm5-object-rwtexture2d-operatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="22024-113">[**Operator\[\]**](sm5-object-rwtexture2d-operatorindex.md)</span></span>  | <span data-ttu-id="22024-114">取得資源變數。</span><span class="sxs-lookup"><span data-stu-id="22024-114">Gets a resource variable.</span></span>     |



 

<span data-ttu-id="22024-115">您可以在 RWTexture2D 物件前面加上儲存類別 **globallycoherent**。</span><span class="sxs-lookup"><span data-stu-id="22024-115">You can prefix RWTexture2D objects with the storage class **globallycoherent**.</span></span> <span data-ttu-id="22024-116">此儲存類別會造成記憶體阻礙和同步處理，以排清整個 GPU 上的資料，讓其他群組可以看到寫入。</span><span class="sxs-lookup"><span data-stu-id="22024-116">This storage class causes memory barriers and syncs to flush data across the entire GPU such that other groups can see writes.</span></span> <span data-ttu-id="22024-117">如果沒有這個規範，記憶體屏障或同步將只會清除未排序的存取視圖， (UAV) 在目前群組中。</span><span class="sxs-lookup"><span data-stu-id="22024-117">Without this specifier, a memory barrier or sync will flush only an unordered access view (UAV) within the current group.</span></span>

<span data-ttu-id="22024-118">RWTexture2D 物件需要物件的宣告語句中的元素類型。</span><span class="sxs-lookup"><span data-stu-id="22024-118">A RWTexture2D object requires an element type in a declaration statement for the object.</span></span> <span data-ttu-id="22024-119">例如，下列宣告不正確：</span><span class="sxs-lookup"><span data-stu-id="22024-119">For example, the following declaration is not correct:</span></span>


```
// The following declaration is incorrectly coded.
RWTexture2D myTexture;
```



<span data-ttu-id="22024-120">下列宣告是正確的：</span><span class="sxs-lookup"><span data-stu-id="22024-120">The following declaration is correct:</span></span>


```
// The following declaration is correctly coded.
RWTexture2D<float> tex;
```



<span data-ttu-id="22024-121">由於 RWTexture2D 物件是 UAV 類型的物件，因此它的屬性與著色器資源檢視不同 (SRV) 型別物件，例如 [Texture2D](sm5-object-texture2d.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="22024-121">Because a RWTexture2D object is a UAV-type object, its properties differ from a shader resource view (SRV)-type object, such as a [Texture2D](sm5-object-texture2d.md) object.</span></span> <span data-ttu-id="22024-122">例如，您可以讀取和寫入 RWTexture2D 物件，但只能從 Texture2D 物件讀取。</span><span class="sxs-lookup"><span data-stu-id="22024-122">For example, you can read from and write to a RWTexture2D object, but you can only read from a Texture2D object.</span></span>

<span data-ttu-id="22024-123">RWTexture2D 物件無法使用來自 [Texture2D](sm5-object-texture2d.md) 物件的方法，例如 [範例](dx-graphics-hlsl-to-sample.md)。</span><span class="sxs-lookup"><span data-stu-id="22024-123">A RWTexture2D object cannot use methods from a [Texture2D](sm5-object-texture2d.md) object, such as [Sample](dx-graphics-hlsl-to-sample.md).</span></span> <span data-ttu-id="22024-124">不過，因為您可以為相同的資源建立多個檢視類型，所以您可以將多個紋理類型宣告為多個著色器中的單一材質。</span><span class="sxs-lookup"><span data-stu-id="22024-124">However, because you can create multiple view types to the same resource, you can declare multiple texture types as a single texture in multiple shaders.</span></span> <span data-ttu-id="22024-125">例如，下列程式碼片段會示範如何在計算著色器中宣告和使用 RWTexture2D 物件做為 *tex* ，然後在圖元著色器中宣告並使用 Texture2D 物件做為 *tex* 。</span><span class="sxs-lookup"><span data-stu-id="22024-125">For example, the following code snippets show how you can declare and use a RWTexture2D object as *tex* in a compute shader and then declare and use a Texture2D object as *tex* in a pixel shader.</span></span>

> [!Note]  
> <span data-ttu-id="22024-126">當您在相同的資源中建立多個檢視類型時，執行時間會強制執行特定的使用模式。</span><span class="sxs-lookup"><span data-stu-id="22024-126">The runtime enforces certain usage patterns when you create multiple view types to the same resource.</span></span> <span data-ttu-id="22024-127">例如，執行時間不允許您同時讓相同資源的資源和 SRV 對應的 UAV 對應同時啟用。</span><span class="sxs-lookup"><span data-stu-id="22024-127">For example, the runtime does not allow you to have both a UAV mapping for a resource and SRV mapping for the same resource active at the same time.</span></span>

 

<span data-ttu-id="22024-128">下列程式碼適用于計算著色器：</span><span class="sxs-lookup"><span data-stu-id="22024-128">The following code is for the compute shader:</span></span>


```
RWTexture2D<float> tex;
[numthreads(groupDim_x, groupDim_y, 1)]
void main(
    uint3 groupId : SV_GroupID,
    uint3 groupThreadId : SV_GroupThreadID,
    uint3 dispatchThreadId : SV_DispatchThreadID,
    uint groupIndex : SV_GroupIndex)
{
    tex [dispatchThreadId.xy] = <something>;
}
```



<span data-ttu-id="22024-129">下列程式碼適用于圖元著色器：</span><span class="sxs-lookup"><span data-stu-id="22024-129">The following code is for the pixel shader:</span></span>


```
struct PixelShaderInput
{
    float4 pos : SV_POSITION;
    float2 tex : TEXTURE;
};

Texture2D<float> tex;
float4 main(PixelShaderInput input) : SV_TARGET
{
    return tex.Sample(TextureSampler, input.tex);
}
```



## <a name="minimum-shader-model"></a><span data-ttu-id="22024-130">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="22024-130">Minimum Shader Model</span></span>

<span data-ttu-id="22024-131">下列著色器模型支援此物件。</span><span class="sxs-lookup"><span data-stu-id="22024-131">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="22024-132">著色器模型</span><span class="sxs-lookup"><span data-stu-id="22024-132">Shader Model</span></span>                                                                | <span data-ttu-id="22024-133">支援</span><span class="sxs-lookup"><span data-stu-id="22024-133">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="22024-134">[著色器模型 5](d3d11-graphics-reference-sm5.md) 和更新版本的著色器模型</span><span class="sxs-lookup"><span data-stu-id="22024-134">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="22024-135">是</span><span class="sxs-lookup"><span data-stu-id="22024-135">yes</span></span>       |



 

<span data-ttu-id="22024-136">下列著色器類型支援此物件：</span><span class="sxs-lookup"><span data-stu-id="22024-136">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="22024-137">頂點</span><span class="sxs-lookup"><span data-stu-id="22024-137">Vertex</span></span> | <span data-ttu-id="22024-138">船體</span><span class="sxs-lookup"><span data-stu-id="22024-138">Hull</span></span> | <span data-ttu-id="22024-139">網域</span><span class="sxs-lookup"><span data-stu-id="22024-139">Domain</span></span> | <span data-ttu-id="22024-140">幾何</span><span class="sxs-lookup"><span data-stu-id="22024-140">Geometry</span></span> | <span data-ttu-id="22024-141">像素</span><span class="sxs-lookup"><span data-stu-id="22024-141">Pixel</span></span> | <span data-ttu-id="22024-142">計算</span><span class="sxs-lookup"><span data-stu-id="22024-142">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="22024-143">x</span><span class="sxs-lookup"><span data-stu-id="22024-143">x</span></span>     | <span data-ttu-id="22024-144">x</span><span class="sxs-lookup"><span data-stu-id="22024-144">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="22024-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="22024-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22024-146">著色器模型5物件</span><span class="sxs-lookup"><span data-stu-id="22024-146">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 




