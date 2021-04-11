---
description: 在 Direct3D 10 中，材質資源是使用 view 來存取，這是在記憶體中資源的硬體轉譯機制。
ms.assetid: ccfe6273-0dcf-4b42-9d74-665a0b4cd14a
title: " (Direct3D 10) 的材質視圖"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f06cd98a00782b826713e68304ad7cc132e4e0fe
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936370"
---
# <a name="texture-views-direct3d-10"></a><span data-ttu-id="b9047-103"> (Direct3D 10) 的材質視圖</span><span class="sxs-lookup"><span data-stu-id="b9047-103">Texture Views (Direct3D 10)</span></span>

<span data-ttu-id="b9047-104">在 Direct3D 10 中，材質資源是使用 view 來存取，這是在記憶體中資源的硬體轉譯機制。</span><span class="sxs-lookup"><span data-stu-id="b9047-104">In Direct3D 10, texture resources are accessed with a view, which is a mechanism for hardware interpretation of a resource in memory.</span></span> <span data-ttu-id="b9047-105">檢視允許特定的管線階段，在應用程式所要的表示中，只能存取其所需的[子資源](d3d10-graphics-programming-guide-resources-types.md)。</span><span class="sxs-lookup"><span data-stu-id="b9047-105">A view allows a particular pipeline stage to access only the [subresources](d3d10-graphics-programming-guide-resources-types.md) it needs, in the representation desired by the application.</span></span>

<span data-ttu-id="b9047-106">視圖支援無類型資源的概念。</span><span class="sxs-lookup"><span data-stu-id="b9047-106">A view supports the notion of a type-less resource.</span></span> <span data-ttu-id="b9047-107">不具類型的資源是以特定大小建立的資源，但不是特定資料類型。</span><span class="sxs-lookup"><span data-stu-id="b9047-107">A type-less resource is a resource created with a specific size but not a specific data type.</span></span> <span data-ttu-id="b9047-108">資料在與管線繫結之後會進行動態解譯。</span><span class="sxs-lookup"><span data-stu-id="b9047-108">The data is interpreted dynamically when it is bound to the pipeline.</span></span>

<span data-ttu-id="b9047-109">下列圖例呈現了透過建立著色器資源檢視，以將 2D 紋理陣列與 6 個紋理繫結，作為著色器資源使用的範例。</span><span class="sxs-lookup"><span data-stu-id="b9047-109">The following illustration shows an example of binding a 2D texture array with 6 textures as a shader resource by creating a shader resource view for it.</span></span> <span data-ttu-id="b9047-110">資源接著便會作為紋理陣列進行定址。</span><span class="sxs-lookup"><span data-stu-id="b9047-110">The resource is then addressed as an array of textures.</span></span> <span data-ttu-id="b9047-111">(注意︰子資源無法同時作為輸入及輸出繫結。)</span><span class="sxs-lookup"><span data-stu-id="b9047-111">(Note: a subresource cannot be bound as both input and output to the pipeline simultaneously.)</span></span>

![六個紋理的紋理陣列圖例](images/d3d10-cube-texture-faces.png)

<span data-ttu-id="b9047-113">當使用 2D 紋理陣列作為轉譯目標時，資源可以作為具備 Mipmap 層級 (在此範例中為 3) 的 2D 紋理陣列 (在此範例中為 6 個紋理) 檢視。</span><span class="sxs-lookup"><span data-stu-id="b9047-113">When using a 2D texture array as a render target, the resource can be viewed as an array of 2D textures (6 in this example) with mipmap levels (3 in this example).</span></span>

<span data-ttu-id="b9047-114">透過呼叫 CreateRenderTargetView 以建立轉譯目標的檢視物件。</span><span class="sxs-lookup"><span data-stu-id="b9047-114">Create a view object for a render target by calling CreateRenderTargetView.</span></span> <span data-ttu-id="b9047-115">接著呼叫 OMSetRenderTargets 為管線設定轉譯目標檢視。</span><span class="sxs-lookup"><span data-stu-id="b9047-115">Then call OMSetRenderTargets to set the render target view to the pipeline.</span></span> <span data-ttu-id="b9047-116">藉由呼叫 Draw 及使用 RenderTargetArrayIndex，索引至陣列中適當的紋理，並且轉譯進轉譯目標之中。</span><span class="sxs-lookup"><span data-stu-id="b9047-116">Render into the render targets by calling Draw and using the RenderTargetArrayIndex to index into the proper texture in the array.</span></span> <span data-ttu-id="b9047-117">您可使用子資源 (一個 Mipmap 層級與陣列索引的組合) 繫結至任何子資源的陣列。</span><span class="sxs-lookup"><span data-stu-id="b9047-117">You can use a subresource (a mipmap level, array index combination) to bind to any array of subresources.</span></span> <span data-ttu-id="b9047-118">如此一來，您就可以繫結至第二個 Mipmap 層級，並且在您需要的時候只更新此一特定 Mipmap 層級，如下圖例所示。</span><span class="sxs-lookup"><span data-stu-id="b9047-118">So you could bind to the second mipmap level and only update this particular mipmap level if you wanted, as in the following illustration.</span></span>

![僅繫結至紋理陣列的第二個 Mipmap 層級之圖例](images/d3d10-cube-texture-faces-subresource.png)



|                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b9047-120">Direct3D 9 與 Direct3D 10 之間的差異：在 Direct3D 10 中，您不再將資源直接系結至管線、建立資源的視圖，然後將視圖設定為管線。</span><span class="sxs-lookup"><span data-stu-id="b9047-120">Differences between Direct3D 9 and Direct3D 10: In Direct3D 10, you no longer bind a resource directly to the pipeline, you create a view of a resource, and then set the view to the pipeline.</span></span> <span data-ttu-id="b9047-121">這可讓執行時間和驅動程式中的驗證和對應發生于建立時，並在系結時將類型檢查降至最低。</span><span class="sxs-lookup"><span data-stu-id="b9047-121">This allows validation and mapping in the runtime and driver to occur at view creation, minimizing type checking at bind-time.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="b9047-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="b9047-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b9047-123"> (Direct3D 10) 的資源 </span><span class="sxs-lookup"><span data-stu-id="b9047-123">Resources (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 




