---
description: " (Direct3D 10) 的效能考慮"
ms.assetid: 9f029be5-4ce0-46ca-909b-adaa980398e7
title: " (Direct3D 10) 的效能考慮"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ba2dbe00475efebdb6ff5d772b3eccd6cd4263a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104025867"
---
# <a name="performance-considerations-direct3d-10"></a><span data-ttu-id="d222b-103"> (Direct3D 10) 的效能考慮</span><span class="sxs-lookup"><span data-stu-id="d222b-103">Performance Considerations (Direct3D 10)</span></span>

## <a name="using-effect-pools"></a><span data-ttu-id="d222b-104">使用效果集區</span><span class="sxs-lookup"><span data-stu-id="d222b-104">Using Effect Pools</span></span>

<span data-ttu-id="d222b-105">轉譯管線通常會使用許多著色器來呈現不同的物件類型和特殊效果。</span><span class="sxs-lookup"><span data-stu-id="d222b-105">It is common for rendering pipelines to use many shaders to render different object types and special effects.</span></span> <span data-ttu-id="d222b-106">著色器是所有著色器（例如世界矩陣或光線位置）中常見的狀態，以及每個著色器（例如物件的擴散色彩或反射反白顯示計算）特定的狀態。</span><span class="sxs-lookup"><span data-stu-id="d222b-106">The shader are a mixture of states that a common among all the shaders such as a world matrix or a light position, and other state that is specific to each shader such as an object's diffuse color, or specular highlight calculation.</span></span> <span data-ttu-id="d222b-107">效果集區是記憶體中的位置，用於儲存許多著色器所使用的狀態，以及一般裝置物件（例如著色器、轉譯狀態物件和常數緩衝區）。</span><span class="sxs-lookup"><span data-stu-id="d222b-107">An effect pool is a place in memory to store state that is used across many shaders, as well as common device objects such as shaders, render state objects and constant buffers.</span></span> <span data-ttu-id="d222b-108">效能改進的結果是針對所有需要該狀態的著色器，更新常見狀態一次。</span><span class="sxs-lookup"><span data-stu-id="d222b-108">The performance improvement results from updating the common state once for all the shaders that need that state.</span></span>

<span data-ttu-id="d222b-109">效果集區是作用中狀態的共用記憶體位置。</span><span class="sxs-lookup"><span data-stu-id="d222b-109">An effect pool is a shared memory location for effect state.</span></span> <span data-ttu-id="d222b-110">建立集區的方式類似于效果;您可以從記憶體 (或檔案或資源) 來建立它。</span><span class="sxs-lookup"><span data-stu-id="d222b-110">A pool is created similarly to an effect; it can be created from memory (or a file or a resource).</span></span> <span data-ttu-id="d222b-111">這會導致兩種不同類型的效果：不依賴其他效果中狀態的全域效果，以及相依于其他效果中狀態的子效果。</span><span class="sxs-lookup"><span data-stu-id="d222b-111">This leads to two different types of effects: a global effect that does not depend on state in other effect versus a child effect which depends on state in another effect.</span></span>

<span data-ttu-id="d222b-112">您可以在建立效果時，藉由提供 [D3D10 \_ 效果 \_ 編譯 \_ 子 \_ 效果](d3d10-effect.md) 旗標) ，指定效果是否為全域效果 (預設案例) 或子效果 (。</span><span class="sxs-lookup"><span data-stu-id="d222b-112">You specify whether an effect is a global effect (the default case) or a child effect (by supplying the [D3D10\_EFFECT\_COMPILE\_CHILD\_EFFECT](d3d10-effect.md) flag) when the effect is created.</span></span> <span data-ttu-id="d222b-113">全域效果可以作為效果集區;子效果不能是效果集區。</span><span class="sxs-lookup"><span data-stu-id="d222b-113">A global effect can serve as an effect pool; a child effect cannot be an effect pool.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d222b-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="d222b-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d222b-115">呈現效果</span><span class="sxs-lookup"><span data-stu-id="d222b-115">Rendering an Effect</span></span>](d3d10-graphics-programming-guide-effects-render.md)
</dt> <dt>

[<span data-ttu-id="d222b-116"> (Direct3D 10) 的效果 </span><span class="sxs-lookup"><span data-stu-id="d222b-116">Effects (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-effects.md)
</dt> </dl>

 

 



