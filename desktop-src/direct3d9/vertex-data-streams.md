---
description: Direct3D 的轉譯介面包含從儲存在一或多個資料緩衝區中的頂點資料轉譯基本的方法。
ms.assetid: e89eae14-f480-470c-b301-f7ff316ad339
title: " (Direct3D 9) 的頂點資料流程"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efd45fc3f645de49060cd201a6a6e9e238712338
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103687728"
---
# <a name="vertex-data-streams-direct3d-9"></a><span data-ttu-id="25ee5-103"> (Direct3D 9) 的頂點資料流程</span><span class="sxs-lookup"><span data-stu-id="25ee5-103">Vertex Data Streams (Direct3D 9)</span></span>

<span data-ttu-id="25ee5-104">Direct3D 的轉譯介面包含從儲存在一或多個資料緩衝區中的頂點資料轉譯基本的方法。</span><span class="sxs-lookup"><span data-stu-id="25ee5-104">The rendering interfaces for Direct3D consist of methods that render primitives from vertex data stored in one or more data buffers.</span></span> <span data-ttu-id="25ee5-105">頂點資料是由結合至表單頂點元件的頂點元素所組成。</span><span class="sxs-lookup"><span data-stu-id="25ee5-105">Vertex data consists of vertex elements combined to form vertex components.</span></span> <span data-ttu-id="25ee5-106">頂點元素是頂點的最小單位，代表位置、標準或色彩等實體。</span><span class="sxs-lookup"><span data-stu-id="25ee5-106">Vertex elements, the smallest unit of a vertex, represent entities such as position, normal, or color.</span></span>

<span data-ttu-id="25ee5-107">頂點元件是一個或多個頂點元素，會連續儲存 (交錯的單一記憶體緩衝區中的每個頂點) 。</span><span class="sxs-lookup"><span data-stu-id="25ee5-107">Vertex components are one or more vertex elements stored contiguously (interleaved per vertex) in a single memory buffer.</span></span> <span data-ttu-id="25ee5-108">完整頂點是由一或多個元件所組成，其中每個元件都在不同的記憶體緩衝區中。</span><span class="sxs-lookup"><span data-stu-id="25ee5-108">A complete vertex consists of one or more components, where each component is in a separate memory buffer.</span></span> <span data-ttu-id="25ee5-109">為了轉譯基本型別，會讀取和組合多個頂點元件，以便讓頂點處理有完整的頂點。</span><span class="sxs-lookup"><span data-stu-id="25ee5-109">To render a primitive, multiple vertex components are read and assembled so that complete vertices are available for vertex processing.</span></span> <span data-ttu-id="25ee5-110">下圖顯示使用頂點元件呈現基本專案的程式。</span><span class="sxs-lookup"><span data-stu-id="25ee5-110">The following diagram shows the process of rendering primitives using vertex components.</span></span>

![使用頂點元件呈現基本專案的程式圖](images/vertexdata.png)

<span data-ttu-id="25ee5-112">轉譯基本專案是由兩個步驟所組成。</span><span class="sxs-lookup"><span data-stu-id="25ee5-112">Rendering primitives consists of two steps.</span></span> <span data-ttu-id="25ee5-113">首先，設定一個或多個頂點元件資料流程;其次，叫用 [**IDirect3DDevice9：:D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) 方法從這些資料流程轉譯。</span><span class="sxs-lookup"><span data-stu-id="25ee5-113">First, set up one or more vertex component streams; second, invoke a [**IDirect3DDevice9::DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) method to render from those streams.</span></span> <span data-ttu-id="25ee5-114">端點著色器會指定這些元件資料流程內頂點元素的識別。</span><span class="sxs-lookup"><span data-stu-id="25ee5-114">Identification of vertex elements within these component streams is specified by the vertex shader.</span></span>

<span data-ttu-id="25ee5-115">[**IDirect3DDevice9：:D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive)方法會指定頂點資料流程中的位移，如此一來，就可以在每個繪製調用中轉譯一組頂點資料內的任意連續子集。</span><span class="sxs-lookup"><span data-stu-id="25ee5-115">The [**IDirect3DDevice9::DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) methods specify an offset in the vertex data streams so that an arbitrary contiguous subset of the primitives within one set of vertex data can be rendered with each draw invocation.</span></span> <span data-ttu-id="25ee5-116">這可讓您在從相同頂點緩衝區轉譯的基本群組之間變更裝置呈現狀態。</span><span class="sxs-lookup"><span data-stu-id="25ee5-116">This enables you to change the device rendering state between groups of primitives that are rendered from the same vertex buffers.</span></span>

<span data-ttu-id="25ee5-117">支援索引和非索引的繪圖方法。</span><span class="sxs-lookup"><span data-stu-id="25ee5-117">Both indexed and nonindexed drawing methods are supported.</span></span> <span data-ttu-id="25ee5-118">如需詳細資訊，請參閱 [從頂點和索引緩衝區轉譯 (Direct3D 9) ](rendering-from-vertex-and-index-buffers.md)。</span><span class="sxs-lookup"><span data-stu-id="25ee5-118">For more information, see [Rendering from Vertex and Index Buffers (Direct3D 9)](rendering-from-vertex-and-index-buffers.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="25ee5-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="25ee5-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="25ee5-120">呈現基本專案</span><span class="sxs-lookup"><span data-stu-id="25ee5-120">Rendering Primitives</span></span>](rendering-primitives.md)
</dt> </dl>

 

 
