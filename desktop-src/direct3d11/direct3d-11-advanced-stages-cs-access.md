---
title: 存取資源
description: 有數種方式可存取資源。
ms.assetid: 83950c4d-5df2-4ed1-9d8f-222a62791c18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e69ab7bffd22b2271c4d648c3a95ec8d98656973
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104990971"
---
# <a name="accessing-resources"></a><span data-ttu-id="4bc38-103">存取資源</span><span class="sxs-lookup"><span data-stu-id="4bc38-103">Accessing Resources</span></span>

<span data-ttu-id="4bc38-104">有數種方式可存取 [資源](overviews-direct3d-11-resources-types.md)。</span><span class="sxs-lookup"><span data-stu-id="4bc38-104">There are several ways to access [resources](overviews-direct3d-11-resources-types.md).</span></span> <span data-ttu-id="4bc38-105">無論如何，Direct3D 保證會針對任何超出範圍存取的資源傳回零。</span><span class="sxs-lookup"><span data-stu-id="4bc38-105">Regardless, Direct3D guarantees to return zero for any resource that is accessed out of bounds.</span></span>

-   [<span data-ttu-id="4bc38-106">以位元組位移存取</span><span class="sxs-lookup"><span data-stu-id="4bc38-106">Access By Byte Offset</span></span>](#access-by-byte-offset)
-   [<span data-ttu-id="4bc38-107">依索引存取</span><span class="sxs-lookup"><span data-stu-id="4bc38-107">Access By Index</span></span>](#access-by-index)
-   [<span data-ttu-id="4bc38-108">由 Mips 方法存取</span><span class="sxs-lookup"><span data-stu-id="4bc38-108">Access By Mips Method</span></span>](#access-by-mips-method)
-   [<span data-ttu-id="4bc38-109">相關主題</span><span class="sxs-lookup"><span data-stu-id="4bc38-109">Related topics</span></span>](#related-topics)

## <a name="access-by-byte-offset"></a><span data-ttu-id="4bc38-110">以位元組位移存取</span><span class="sxs-lookup"><span data-stu-id="4bc38-110">Access By Byte Offset</span></span>

<span data-ttu-id="4bc38-111">您可以使用位元組位移來存取兩個新的緩衝區類型：</span><span class="sxs-lookup"><span data-stu-id="4bc38-111">Two new buffer types can be accessed using a byte offset:</span></span>

-   <span data-ttu-id="4bc38-112">[**ByteAddressBuffer**](/windows/desktop/direct3dhlsl/sm5-object-byteaddressbuffer) 是唯讀緩衝區。</span><span class="sxs-lookup"><span data-stu-id="4bc38-112">[**ByteAddressBuffer**](/windows/desktop/direct3dhlsl/sm5-object-byteaddressbuffer) is a read-only buffer.</span></span>
-   <span data-ttu-id="4bc38-113">[**RWByteAddressBuffer**](/windows/desktop/direct3dhlsl/sm5-object-rwbyteaddressbuffer) 是讀取或寫入緩衝區。</span><span class="sxs-lookup"><span data-stu-id="4bc38-113">[**RWByteAddressBuffer**](/windows/desktop/direct3dhlsl/sm5-object-rwbyteaddressbuffer) is a read or write buffer.</span></span>

## <a name="access-by-index"></a><span data-ttu-id="4bc38-114">依索引存取</span><span class="sxs-lookup"><span data-stu-id="4bc38-114">Access By Index</span></span>

<span data-ttu-id="4bc38-115">資源類型可以使用索引來參考資源中的特定位置。</span><span class="sxs-lookup"><span data-stu-id="4bc38-115">Resource types can use an index to reference a specific location in the resource.</span></span> <span data-ttu-id="4bc38-116">請考慮此範例：</span><span class="sxs-lookup"><span data-stu-id="4bc38-116">Consider this example:</span></span>


```
uint2 pos;
Texture2D<float4> myTexture;
float4 myVar = myTexture[pos];
```



<span data-ttu-id="4bc38-117">此範例會將位於 *myTexture* 2d 材質資源中 *pos* 位置的材質所儲存的4個 float 值，指派給 *myVar* 變數。</span><span class="sxs-lookup"><span data-stu-id="4bc38-117">This example assigns the 4 float values that are stored at the texel located at the *pos* position in the *myTexture* 2D texture resource to the *myVar* variable.</span></span>

> [!Note]  
> <span data-ttu-id="4bc38-118">以這種方式存取材質的預設值是 mipmap 層級零 () 最詳細的層級。</span><span class="sxs-lookup"><span data-stu-id="4bc38-118">The default for accessing a texture in this way is mipmap level zero (the most detailed level).</span></span>

 

> [!Note]  
> <span data-ttu-id="4bc38-119">"Float4 myVar = myTexture \[ pos \] ;" 行相當於 "float4 MyVar = MyTexture. Load (uint3 (pos，0) ) ;"。</span><span class="sxs-lookup"><span data-stu-id="4bc38-119">The "float4 myVar = myTexture\[pos\];" line is equivalent to "float4 myVar = myTexture.Load(uint3(pos,0));".</span></span> <span data-ttu-id="4bc38-120">依索引存取是新的 HLSL 語法增強功能。</span><span class="sxs-lookup"><span data-stu-id="4bc38-120">Access by index is a new HLSL syntax enhancement.</span></span>

 

> [!Note]  
> <span data-ttu-id="4bc38-121">在2010年6月版的 DirectX SDK 和更新版本中，編譯器可讓您編制除了 [位元組位址緩衝區](direct3d-11-advanced-stages-cs-resources.md)以外的所有資源類型。</span><span class="sxs-lookup"><span data-stu-id="4bc38-121">The compiler in the June 2010 version of the DirectX SDK and later lets you index all resource types except for [byte address buffers](direct3d-11-advanced-stages-cs-resources.md).</span></span>

 

> [!Note]  
> <span data-ttu-id="4bc38-122">2010年6月編譯器和更新版本可讓您宣告本機資源變數。</span><span class="sxs-lookup"><span data-stu-id="4bc38-122">The June 2010 compiler and later lets you declare local resource variables.</span></span> <span data-ttu-id="4bc38-123">您可以將全域定義的資源指派 (例如，將) *myTexture* 至這些變數，並使用與全域對應專案相同的方式來使用它們。</span><span class="sxs-lookup"><span data-stu-id="4bc38-123">You can assign globally defined resources (like *myTexture*) to these variables and use them the same way as their global counterparts.</span></span>

 

## <a name="access-by-mips-method"></a><span data-ttu-id="4bc38-124">由 Mips 方法存取</span><span class="sxs-lookup"><span data-stu-id="4bc38-124">Access By Mips Method</span></span>

<span data-ttu-id="4bc38-125">材質物件有 **mips** 方法 (例如， [**Texture2D**](/previous-versions/windows/desktop/legacy/ff471560(v=vs.85))) ，您可以用它來指定 mipmap 層級。</span><span class="sxs-lookup"><span data-stu-id="4bc38-125">Texture objects have a **mips** method (for example, [**Texture2D.mips**](/previous-versions/windows/desktop/legacy/ff471560(v=vs.85))), which you can use to specify the mipmap level.</span></span> <span data-ttu-id="4bc38-126">此範例會讀取2D 材質中 mipmap 層級 2 (7、16) 所儲存的色彩：</span><span class="sxs-lookup"><span data-stu-id="4bc38-126">This example reads the color stored at (7,16) on mipmap level 2 in a 2D texture:</span></span>


```
uint x = 7;
uint y = 16;
float4 myColor = myTexture.mips[2][uint2(x,y)];
```



<span data-ttu-id="4bc38-127">這是2010年6月編譯器和更新版本的增強功能。</span><span class="sxs-lookup"><span data-stu-id="4bc38-127">This is an enhancement from the June 2010 compiler and later.</span></span> <span data-ttu-id="4bc38-128">"MyTexture mips \[ 2 \] \[ uint2 (x，y) \] " 運算式相當於 "myTexture. Load (uint3 (x，y，2) ) "。</span><span class="sxs-lookup"><span data-stu-id="4bc38-128">The "myTexture.mips\[2\]\[uint2(x,y)\]" expression is equivalent to "myTexture.Load(uint3(x,y,2))".</span></span>

## <a name="related-topics"></a><span data-ttu-id="4bc38-129">相關主題</span><span class="sxs-lookup"><span data-stu-id="4bc38-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4bc38-130">計算著色器總覽</span><span class="sxs-lookup"><span data-stu-id="4bc38-130">Compute Shader Overview</span></span>](direct3d-11-advanced-stages-compute-shader.md)
</dt> </dl>

 

 