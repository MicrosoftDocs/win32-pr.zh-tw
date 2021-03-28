---
title: 緩衝區
description: 緩衝區包含的資料用於描述幾何、編制幾何資訊的索引，以及著色器常數。 本節說明 Direct3D 11 中使用的緩衝區，以及一般案例的工作式檔連結。
ms.assetid: 4ab4c9e5-9155-4bfd-b69b-40b3e8cdd4ba
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c544f00515f25c9c311f6c75fda109d3e88294b4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301272"
---
# <a name="buffers"></a><span data-ttu-id="c5930-104">緩衝區</span><span class="sxs-lookup"><span data-stu-id="c5930-104">Buffers</span></span>

<span data-ttu-id="c5930-105">緩衝區包含的資料用於描述幾何、編制幾何資訊的索引，以及著色器常數。</span><span class="sxs-lookup"><span data-stu-id="c5930-105">Buffers contain data that is used for describing geometry, indexing geometry information, and shader constants.</span></span> <span data-ttu-id="c5930-106">本節說明 Direct3D 11 中使用的緩衝區，以及一般案例的工作式檔連結。</span><span class="sxs-lookup"><span data-stu-id="c5930-106">This section describes buffers that are used in Direct3D 11 and links to task-based documentation for common scenarios.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="c5930-107">本節內容</span><span class="sxs-lookup"><span data-stu-id="c5930-107">In this section</span></span>



| <span data-ttu-id="c5930-108">主題</span><span class="sxs-lookup"><span data-stu-id="c5930-108">Topic</span></span>                                                                                                  | <span data-ttu-id="c5930-109">描述</span><span class="sxs-lookup"><span data-stu-id="c5930-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c5930-110">Direct3D 11 中的緩衝區簡介</span><span class="sxs-lookup"><span data-stu-id="c5930-110">Introduction to Buffers in Direct3D 11</span></span>](overviews-direct3d-11-resources-buffers-intro.md)<br/> | <span data-ttu-id="c5930-111">緩衝區資源是一個完整輸入的資料集合，由元素所組成。</span><span class="sxs-lookup"><span data-stu-id="c5930-111">A buffer resource is a collection of fully typed data grouped into elements.</span></span> <span data-ttu-id="c5930-112">您可以使用緩衝區存放各式各樣的資料，包含位置向量、法向向量、頂點緩衝區中的紋理座標、索引緩衝區中的索引、或裝置狀態。</span><span class="sxs-lookup"><span data-stu-id="c5930-112">You can use buffers to store a wide variety of data, including position vectors, normal vectors, texture coordinates in a vertex buffer, indexes in an index buffer, or device state.</span></span> <span data-ttu-id="c5930-113">緩衝元素由 1 到 4 個元件組成。</span><span class="sxs-lookup"><span data-stu-id="c5930-113">A buffer element is made up of 1 to 4 components.</span></span> <span data-ttu-id="c5930-114">緩衝元素可以包含封裝資料值 (像是 R8G8B8A8 面值)、單一 8 位整數，或四個 32 位元浮點數值。</span><span class="sxs-lookup"><span data-stu-id="c5930-114">Buffer elements can include packed data values (like R8G8B8A8 surface values), single 8-bit integers, or four 32-bit floating point values.</span></span> <br/> |



 

## <a name="related-topics"></a><span data-ttu-id="c5930-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="c5930-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c5930-116">如何：建立常數緩衝區</span><span class="sxs-lookup"><span data-stu-id="c5930-116">How to: Create a Constant Buffer</span></span>](overviews-direct3d-11-resources-buffers-constant-how-to.md)
</dt> <dt>

[<span data-ttu-id="c5930-117">如何：建立索引緩衝區</span><span class="sxs-lookup"><span data-stu-id="c5930-117">How to: Create an Index Buffer</span></span>](overviews-direct3d-11-resources-buffers-index-how-to.md)
</dt> <dt>

[<span data-ttu-id="c5930-118">如何：建立頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="c5930-118">How to: Create a Vertex Buffer</span></span>](overviews-direct3d-11-resources-buffers-vertex-how-to.md)
</dt> <dt>

[<span data-ttu-id="c5930-119">資源</span><span class="sxs-lookup"><span data-stu-id="c5930-119">Resources</span></span>](overviews-direct3d-11-resources.md)
</dt> </dl>

 

 





