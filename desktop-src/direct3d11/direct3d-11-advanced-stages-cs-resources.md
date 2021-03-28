---
title: 新的資源類型
description: 已在 Direct3D 11 中新增數個新的資源類型。
ms.assetid: 597cc12f-dd0e-4603-b670-3f584f25e192
keywords:
- '位元組位址緩衝區 (總覽) '
- '讀取/寫入緩衝區 (總覽) '
- '結構化緩衝區 (總覽) '
- 未排序的存取緩衝區
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4b7a75ec95917a5ee819126e42dce3117994574
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375985"
---
# <a name="new-resource-types"></a><span data-ttu-id="be07a-107">新的資源類型</span><span class="sxs-lookup"><span data-stu-id="be07a-107">New Resource Types</span></span>

<span data-ttu-id="be07a-108">已在 Direct3D 11 中新增數個新的資源類型。</span><span class="sxs-lookup"><span data-stu-id="be07a-108">Several new resource types have been added in Direct3D 11.</span></span>

-   [<span data-ttu-id="be07a-109">讀取/寫入緩衝區和紋理</span><span class="sxs-lookup"><span data-stu-id="be07a-109">Read/Write Buffers and Textures</span></span>](#readwrite-buffers-and-textures)
-   [<span data-ttu-id="be07a-110">結構化緩衝區</span><span class="sxs-lookup"><span data-stu-id="be07a-110">Structured Buffer</span></span>](#structured-buffer)
-   [<span data-ttu-id="be07a-111">位元組位址緩衝區</span><span class="sxs-lookup"><span data-stu-id="be07a-111">Byte Address Buffer</span></span>](#byte-address-buffer)
-   [<span data-ttu-id="be07a-112">未排序的存取緩衝區或紋理</span><span class="sxs-lookup"><span data-stu-id="be07a-112">Unordered Access Buffer or Texture</span></span>](#unordered-access-buffer-or-texture)
    -   [<span data-ttu-id="be07a-113">附加和使用緩衝區</span><span class="sxs-lookup"><span data-stu-id="be07a-113">Append and Consume Buffer</span></span>](#append-and-consume-buffer)
-   [<span data-ttu-id="be07a-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="be07a-114">Related topics</span></span>](#related-topics)

## <a name="readwrite-buffers-and-textures"></a><span data-ttu-id="be07a-115">讀取/寫入緩衝區和紋理</span><span class="sxs-lookup"><span data-stu-id="be07a-115">Read/Write Buffers and Textures</span></span>

<span data-ttu-id="be07a-116">著色器模型4資源是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="be07a-116">Shader model 4 resources are read only.</span></span> <span data-ttu-id="be07a-117">著色器模型5會執行一組新的對應讀取/寫入資源：</span><span class="sxs-lookup"><span data-stu-id="be07a-117">Shader model 5 implements a new corresponding set of read/write resources:</span></span>

-   [<span data-ttu-id="be07a-118">RWBuffer</span><span class="sxs-lookup"><span data-stu-id="be07a-118">RWBuffer</span></span>](/windows/desktop/direct3dhlsl/sm5-object-rwbuffer)
-   <span data-ttu-id="be07a-119">[RWTexture1D](/windows/desktop/direct3dhlsl/sm5-object-rwtexture1d)、 [RWTexture1DArray](/windows/desktop/direct3dhlsl/sm5-object-rwtexture1darray)</span><span class="sxs-lookup"><span data-stu-id="be07a-119">[RWTexture1D](/windows/desktop/direct3dhlsl/sm5-object-rwtexture1d), [RWTexture1DArray](/windows/desktop/direct3dhlsl/sm5-object-rwtexture1darray)</span></span>
-   <span data-ttu-id="be07a-120">[RWTexture2D](/windows/desktop/direct3dhlsl/sm5-object-rwtexture2d)、 [RWTexture2DArray](/windows/desktop/direct3dhlsl/sm5-object-rwtexture2darray)</span><span class="sxs-lookup"><span data-stu-id="be07a-120">[RWTexture2D](/windows/desktop/direct3dhlsl/sm5-object-rwtexture2d), [RWTexture2DArray](/windows/desktop/direct3dhlsl/sm5-object-rwtexture2darray)</span></span>
-   [<span data-ttu-id="be07a-121">RWTexture3D</span><span class="sxs-lookup"><span data-stu-id="be07a-121">RWTexture3D</span></span>](/windows/desktop/direct3dhlsl/sm5-object-rwtexture3d)

<span data-ttu-id="be07a-122">這些資源需要資源變數以透過索引) 存取記憶體 (，因為沒有任何方法可以直接存取記憶體。</span><span class="sxs-lookup"><span data-stu-id="be07a-122">These resources require a resource variable to access memory (through indexing) as there are no methods for accessing memory directly.</span></span> <span data-ttu-id="be07a-123">資源變數可在方程式的左右側邊使用;如果使用於右邊，則範本類型必須是單一元件 (float、int 或 uint) 。</span><span class="sxs-lookup"><span data-stu-id="be07a-123">A resource variable can be used on the left and right sides of an equation; if used on the right side, the template type must be single component (float, int, or uint).</span></span>

## <a name="structured-buffer"></a><span data-ttu-id="be07a-124">結構化緩衝區</span><span class="sxs-lookup"><span data-stu-id="be07a-124">Structured Buffer</span></span>

<span data-ttu-id="be07a-125">結構化緩衝區是包含大小相等之元素的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="be07a-125">A structured buffer is a buffer that contains elements of equal sizes.</span></span> <span data-ttu-id="be07a-126">使用具有一或多個成員類型的結構來定義專案。</span><span class="sxs-lookup"><span data-stu-id="be07a-126">Use a structure with one or more member types to define an element.</span></span> <span data-ttu-id="be07a-127">以下是具有三個成員的結構。</span><span class="sxs-lookup"><span data-stu-id="be07a-127">Here is a structure with three members.</span></span>


```
struct MyStruct
{
    float4 Color;
    float4 Normal;
    bool isAwesome;
};
```



<span data-ttu-id="be07a-128">使用此結構來宣告結構化緩衝區，如下所示：</span><span class="sxs-lookup"><span data-stu-id="be07a-128">Use this structure to declare a structured buffer like this:</span></span>


```
StructuredBuffer<MyStruct> mySB;
```



<span data-ttu-id="be07a-129">除了編制索引之外，結構化緩衝區支援存取單一成員，如下所示：</span><span class="sxs-lookup"><span data-stu-id="be07a-129">In addition to indexing, a structured buffer supports accessing a single member like this:</span></span>


```
float4 myColor = mySb[27].Color;
```



<span data-ttu-id="be07a-130">您可以使用下列物件類型來存取結構化緩衝區：</span><span class="sxs-lookup"><span data-stu-id="be07a-130">Use the following object types to access a structured buffer:</span></span>

-   <span data-ttu-id="be07a-131">[StructuredBuffer](/windows/desktop/direct3dhlsl/sm5-object-structuredbuffer) 是唯讀的結構化緩衝區。</span><span class="sxs-lookup"><span data-stu-id="be07a-131">[StructuredBuffer](/windows/desktop/direct3dhlsl/sm5-object-structuredbuffer) is a read only structured buffer.</span></span>
-   <span data-ttu-id="be07a-132">[RWStructuredBuffer](/windows/desktop/direct3dhlsl/sm5-object-rwstructuredbuffer) 是一個讀寫結構化緩衝區。</span><span class="sxs-lookup"><span data-stu-id="be07a-132">[RWStructuredBuffer](/windows/desktop/direct3dhlsl/sm5-object-rwstructuredbuffer) is a read/write structured buffer.</span></span>

<span data-ttu-id="be07a-133">可以在 **RWStructuredBuffer** 的 int 和 uint 元素上 [執行可執行](direct3d-11-advanced-stages-cs-atomic-functions.md)連鎖作業的不可部分完成函式。</span><span class="sxs-lookup"><span data-stu-id="be07a-133">[Atomic functions](direct3d-11-advanced-stages-cs-atomic-functions.md) which implement interlocked operations are allowed on int and uint elements in an **RWStructuredBuffer**.</span></span>

## <a name="byte-address-buffer"></a><span data-ttu-id="be07a-134">位元組位址緩衝區</span><span class="sxs-lookup"><span data-stu-id="be07a-134">Byte Address Buffer</span></span>

<span data-ttu-id="be07a-135">位元組位址緩衝區是以位元組位移定址其內容的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="be07a-135">A byte address buffer is a buffer whose contents are addressable by a byte offset.</span></span> <span data-ttu-id="be07a-136">一般來說，會使用每個元素的 stride 來為每個專案編制 [緩衝區](overviews-direct3d-11-resources-buffers-intro.md) 的內容， (s) 和元素編號 (N) 所指定的 n \* 。</span><span class="sxs-lookup"><span data-stu-id="be07a-136">Normally, the contents of a [buffer](overviews-direct3d-11-resources-buffers-intro.md) are indexed per element using a stride for each element (S) and the element number (N) as given by S\*N.</span></span> <span data-ttu-id="be07a-137">位元組位址緩衝區也可以稱為原始緩衝區，它會使用緩衝區開頭的位元組值位移來存取資料。</span><span class="sxs-lookup"><span data-stu-id="be07a-137">A byte address buffer, which can also be called a raw buffer, uses a byte value offset from the beginning of the buffer to access data.</span></span> <span data-ttu-id="be07a-138">位元組值必須是四的倍數，如此才會對齊 DWORD。</span><span class="sxs-lookup"><span data-stu-id="be07a-138">The byte value must be a multiple of four so that it is DWORD aligned.</span></span> <span data-ttu-id="be07a-139">如果有提供任何其他值，則行為會是未定義的。</span><span class="sxs-lookup"><span data-stu-id="be07a-139">If any other value is provided, behavior is undefined.</span></span>

<span data-ttu-id="be07a-140">著色器模型5引進了存取 [唯讀位元組位址緩衝區](/windows/desktop/direct3dhlsl/sm5-object-byteaddressbuffer) 以及 [讀寫位元組位址緩衝區](/windows/desktop/direct3dhlsl/sm5-object-rwbyteaddressbuffer)的物件。</span><span class="sxs-lookup"><span data-stu-id="be07a-140">Shader model 5 introduces objects for accessing a [read-only byte address buffer](/windows/desktop/direct3dhlsl/sm5-object-byteaddressbuffer) as well as a [read-write byte address buffer](/windows/desktop/direct3dhlsl/sm5-object-rwbyteaddressbuffer).</span></span> <span data-ttu-id="be07a-141">位元組位址緩衝區的內容是設計成32位不帶正負號的整數;如果緩衝區中的值不是不帶正負號的整數，請使用像是 [**asfloat**](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-asfloat) 的函式來讀取它。</span><span class="sxs-lookup"><span data-stu-id="be07a-141">The contents of a byte address buffer is designed to be a 32-bit unsigned integer; if the value in the buffer is not really an unsigned integer, use a function such as [**asfloat**](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-asfloat) to read it.</span></span>

## <a name="unordered-access-buffer-or-texture"></a><span data-ttu-id="be07a-142">未排序的存取緩衝區或紋理</span><span class="sxs-lookup"><span data-stu-id="be07a-142">Unordered Access Buffer or Texture</span></span>

<span data-ttu-id="be07a-143">未排序的存取資源 (，其中包括緩衝區、紋理和材質陣列，而不含多層式) ，可讓您從多個執行緒暫時未排序的讀取/寫入存取。</span><span class="sxs-lookup"><span data-stu-id="be07a-143">An unordered access resource (which includes buffers, textures, and texture arrays - without multisampling), allows temporally unordered read/write access from multiple threads.</span></span> <span data-ttu-id="be07a-144">這表示此資源類型可以由多個執行緒同時讀取/寫入，而不會透過使用 [不可部分完成的函](direct3d-11-advanced-stages-cs-atomic-functions.md)式來產生記憶體衝突。</span><span class="sxs-lookup"><span data-stu-id="be07a-144">This means that this resource type can be read/written simultaneously by multiple threads without generating memory conflicts through the use of [Atomic Functions](direct3d-11-advanced-stages-cs-atomic-functions.md).</span></span>

<span data-ttu-id="be07a-145">藉由呼叫 [**ID3D11Device：： CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer)或 [**ID3D11Device：： CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d)之類的函式，並從 D3D11 系結 [**\_ \_ 旗**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag)標列舉傳遞 **D3D11 系結 \_ \_ 無排序 \_ 存取** 旗標，來建立未排序的存取緩衝區或紋理。</span><span class="sxs-lookup"><span data-stu-id="be07a-145">Create an unordered access buffer or texture by calling a function such as [**ID3D11Device::CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) or [**ID3D11Device::CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d) and passing in the **D3D11\_BIND\_UNORDERED\_ACCESS** flag from the [**D3D11\_BIND\_FLAG**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag) enumeration.</span></span>

<span data-ttu-id="be07a-146">未排序的存取資源只能系結至圖元著色器和計算著色器。</span><span class="sxs-lookup"><span data-stu-id="be07a-146">Unordered access resources can only be bound to pixel shaders and compute shaders.</span></span> <span data-ttu-id="be07a-147">執行期間，以平行方式執行的圖元著色器或計算著色器會系結相同的未排序存取資源。</span><span class="sxs-lookup"><span data-stu-id="be07a-147">During execution, pixel shaders or compute shaders running in parallel have the same unordered access resources bound.</span></span>

### <a name="append-and-consume-buffer"></a><span data-ttu-id="be07a-148">附加和使用緩衝區</span><span class="sxs-lookup"><span data-stu-id="be07a-148">Append and Consume Buffer</span></span>

<span data-ttu-id="be07a-149">附加和取用緩衝區是一種特殊類型的未排序資源，支援在緩衝區結尾新增和移除值，類似于堆疊的運作方式。</span><span class="sxs-lookup"><span data-stu-id="be07a-149">An append and consume buffer is a special type of an unordered resource that supports adding and removing values from the end of a buffer similar to the way a stack works.</span></span>

<span data-ttu-id="be07a-150">附加和取用緩衝區必須是結構化緩衝區：</span><span class="sxs-lookup"><span data-stu-id="be07a-150">An append and consume buffer must be a structured buffer:</span></span>

-   [<span data-ttu-id="be07a-151">AppendStructuredBuffer</span><span class="sxs-lookup"><span data-stu-id="be07a-151">AppendStructuredBuffer</span></span>](/windows/desktop/direct3dhlsl/sm5-object-appendstructuredbuffer)
-   [<span data-ttu-id="be07a-152">ConsumeStructuredBuffer</span><span class="sxs-lookup"><span data-stu-id="be07a-152">ConsumeStructuredBuffer</span></span>](/windows/desktop/direct3dhlsl/sm5-object-consumestructuredbuffer)

<span data-ttu-id="be07a-153">透過其方法使用這些資源，這些資源就不會使用資源變數。</span><span class="sxs-lookup"><span data-stu-id="be07a-153">Use these resources through their methods, these resources do not use resource variables.</span></span>

## <a name="related-topics"></a><span data-ttu-id="be07a-154">相關主題</span><span class="sxs-lookup"><span data-stu-id="be07a-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="be07a-155">計算著色器總覽</span><span class="sxs-lookup"><span data-stu-id="be07a-155">Compute Shader Overview</span></span>](direct3d-11-advanced-stages-compute-shader.md)
</dt> </dl>

 

 