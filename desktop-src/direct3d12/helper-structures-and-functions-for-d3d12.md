---
title: D3D12 的 Helper 結構和函式
description: 這些 helper 結構和 helper 函式是在 d3dx12 中宣告。
ms.assetid: 095958A9-345B-45AE-8363-B353534044B2
keywords:
- Helper 函式
- Helper 結構
- d3dx12。h
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4d612d97610a749f32a6a23010b632c17d34461
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106966807"
---
# <a name="helper-structures-and-functions-for-d3d12"></a><span data-ttu-id="7dc94-106">D3D12 的 Helper 結構和函式</span><span class="sxs-lookup"><span data-stu-id="7dc94-106">Helper Structures and Functions for D3D12</span></span>

<span data-ttu-id="7dc94-107">這些 helper 結構和 helper 函式是在 **d3dx12** 中宣告。</span><span class="sxs-lookup"><span data-stu-id="7dc94-107">These helper structures and helper functions are declared in **d3dx12.h**.</span></span>

<span data-ttu-id="7dc94-108">您可以使用這些 helper 結構來建立和初始化 Direct3D 結構。</span><span class="sxs-lookup"><span data-stu-id="7dc94-108">You can use these helper structures to create and initialize Direct3D structures.</span></span> <span data-ttu-id="7dc94-109">這些 helper 結構的行為就像 c + + 類別一樣。</span><span class="sxs-lookup"><span data-stu-id="7dc94-109">These helper structures behave like C++ classes.</span></span> <span data-ttu-id="7dc94-110">每個 helper 結構通常都有一個預設的函式、一個明確的函式、一個函式，以及相關聯 D3D12 結構的 cast 運算子。</span><span class="sxs-lookup"><span data-stu-id="7dc94-110">Each helper structure typically has a default constructor, an explicit constructor, a destructor, and a cast operator for the associated D3D12 structure.</span></span> <span data-ttu-id="7dc94-111">每個協助程式結構都有 ' C ' 前置詞，而且與缺少 ' C ' 前置詞的 D3D12 結構相關聯。</span><span class="sxs-lookup"><span data-stu-id="7dc94-111">Each helper structure has a 'C' prefix and is associated with a D3D12 structure which lacks the 'C' prefix.</span></span> <span data-ttu-id="7dc94-112">大部分的協助程式結構都包含初始化成員方法，有些則包含比較函數。</span><span class="sxs-lookup"><span data-stu-id="7dc94-112">Most helper structures contain initialization member methods, some contain comparison functions.</span></span>

<span data-ttu-id="7dc94-113">**d3dx12** 與 Direct3D 12 標頭分開提供。</span><span class="sxs-lookup"><span data-stu-id="7dc94-113">**d3dx12.h** is available separately from the Direct3D 12 headers.</span></span> <span data-ttu-id="7dc94-114">您可以從 [D3D12 Helper 程式庫](https://github.com/Microsoft/DirectX-Graphics-Samples/tree/master/Libraries/D3DX12)下載 **d3dx12. h** 。</span><span class="sxs-lookup"><span data-stu-id="7dc94-114">You can download **d3dx12.h** from [The D3D12 Helper Library](https://github.com/Microsoft/DirectX-Graphics-Samples/tree/master/Libraries/D3DX12).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="7dc94-115">本節內容</span><span class="sxs-lookup"><span data-stu-id="7dc94-115">In this section</span></span>



| <span data-ttu-id="7dc94-116">主題</span><span class="sxs-lookup"><span data-stu-id="7dc94-116">Topic</span></span>                                                                     | <span data-ttu-id="7dc94-117">描述</span><span class="sxs-lookup"><span data-stu-id="7dc94-117">Description</span></span>                                                                                                              |
|---------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7dc94-118">D3D12 的 Helper 介面</span><span class="sxs-lookup"><span data-stu-id="7dc94-118">Helper Interfaces for D3D12</span></span>](helper-interfaces-for-d3d12.md)<br/> | <span data-ttu-id="7dc94-119">這些協助程式介面特別有助於處理子資源，而且會在 **d3dx12** 中宣告。</span><span class="sxs-lookup"><span data-stu-id="7dc94-119">These helper interfaces help particularly in handling subresources, and are declared in **d3dx12.h**.</span></span> <br/>        |
| [<span data-ttu-id="7dc94-120">D3D12 的 Helper 結構</span><span class="sxs-lookup"><span data-stu-id="7dc94-120">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)<br/> | <span data-ttu-id="7dc94-121">這些 helper 結構有助於初始化許多 Direct3D 12 結構，並在 **d3dx12** 中宣告。</span><span class="sxs-lookup"><span data-stu-id="7dc94-121">These helper structures help initialize many of the Direct3D 12 structures, and are declared in **d3dx12.h**.</span></span><br/> |
| [<span data-ttu-id="7dc94-122">D3D12 的 Helper 函式</span><span class="sxs-lookup"><span data-stu-id="7dc94-122">Helper Functions for D3D12</span></span>](helper-functions-for-d3d12.md)<br/>   | <span data-ttu-id="7dc94-123">這些 helper 函式特別有助於處理子資源，而且會在 **d3dx12** 中宣告。</span><span class="sxs-lookup"><span data-stu-id="7dc94-123">These helper functions help particularly in handling subresources, and are declared in **d3dx12.h**.</span></span> <br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="7dc94-124">相關主題</span><span class="sxs-lookup"><span data-stu-id="7dc94-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7dc94-125">Direct3D 12 參考</span><span class="sxs-lookup"><span data-stu-id="7dc94-125">Direct3D 12 Reference</span></span>](direct3d-12-reference.md)
</dt> </dl>

 

 





