---
description: 頂點宣告會定義頂點緩衝區版面配置，並針對鑲嵌式引擎進行程式設計。
ms.assetid: 09dae498-3b33-4c33-bc7e-47f2bf784e4c
title: " (Direct3D 9) 的頂點宣告"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c769aa6fb80de1fd83067ebb9f32b591baa8e883
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106970495"
---
# <a name="vertex-declaration-direct3d-9"></a><span data-ttu-id="35cd3-103"> (Direct3D 9) 的頂點宣告</span><span class="sxs-lookup"><span data-stu-id="35cd3-103">Vertex Declaration (Direct3D 9)</span></span>

<span data-ttu-id="35cd3-104">頂點宣告會定義頂點緩衝區版面配置，並針對鑲嵌式引擎進行程式設計。</span><span class="sxs-lookup"><span data-stu-id="35cd3-104">A vertex declaration defines the vertex buffer layout and programs the tessellation engine.</span></span> <span data-ttu-id="35cd3-105">從 Direct3D 9 開始，頂點資料流程會以 [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) 結構的陣列來表示 (而不是使用彈性頂點格式 (FVF) 碼) 。</span><span class="sxs-lookup"><span data-stu-id="35cd3-105">Starting with Direct3D 9, vertex streams are expressed as an array of [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) structures (instead of using flexible vertex format (FVF) codes).</span></span> <span data-ttu-id="35cd3-106">每個陣列元素都會描述每個頂點的資料類型。</span><span class="sxs-lookup"><span data-stu-id="35cd3-106">Each array element describes each per-vertex data type.</span></span> <span data-ttu-id="35cd3-107">下列主題涵蓋將 FVF> 代碼轉換成新格式的程式碼：</span><span class="sxs-lookup"><span data-stu-id="35cd3-107">Converting FVF> codes into the new format is covered in the following topics:</span></span>

-   [<span data-ttu-id="35cd3-108">將 FVF 碼對應至 direct3d 9 宣告 (Direct3D 9) </span><span class="sxs-lookup"><span data-stu-id="35cd3-108">Mapping FVF Codes to a Direct3D 9 Declaration (Direct3D 9)</span></span>](mapping-fvf-codes-to-a-directx-9-declaration.md)
-   [<span data-ttu-id="35cd3-109">修正 (Direct3D 9) 的函式 FVF 碼 </span><span class="sxs-lookup"><span data-stu-id="35cd3-109">Fixed Function FVF Codes (Direct3D 9)</span></span>](fixed-function-fvf-codes.md)
-   [<span data-ttu-id="35cd3-110">Direct3D 宣告與 FVF 碼之間的對應 (Direct3D 9) </span><span class="sxs-lookup"><span data-stu-id="35cd3-110">Mapping between a Direct3D Declaration and FVF Codes (Direct3D 9)</span></span>](mapping-between-a-directx-9-declaration-and-fvf-codes.md)
-   [<span data-ttu-id="35cd3-111">Direct3d 9 宣告與 Direct3D 8 宣告之間的對應 (Direct3D 9) </span><span class="sxs-lookup"><span data-stu-id="35cd3-111">Mapping between a Direct3D 9 Declaration and a Direct3D 8 Declaration (Direct3D 9)</span></span>](mapping-between-a-directx-9-declaration-and-directx-8.md)
-   [<span data-ttu-id="35cd3-112">將一或多個串流程式設計 (Direct3D 9) </span><span class="sxs-lookup"><span data-stu-id="35cd3-112">Programming One or More Streams (Direct3D 9)</span></span>](programming-one-or-more-streams.md)

## <a name="related-topics"></a><span data-ttu-id="35cd3-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="35cd3-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="35cd3-114">頂點緩衝區</span><span class="sxs-lookup"><span data-stu-id="35cd3-114">Vertex Buffers</span></span>](vertex-buffers.md)
</dt> </dl>

 

 



