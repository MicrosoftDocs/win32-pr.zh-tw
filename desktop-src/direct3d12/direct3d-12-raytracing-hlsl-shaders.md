---
title: Direct3D 12 Raytracing HLSL 著色器
description: 查看描述高階著色器語言 (HLSL) 著色器（支援 Direct3D 12 raytracing 管線）之文章的連結。
ms.assetid: ''
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ca19081b1ea963851e82d18912153434c3e38d1
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112394833"
---
# <a name="direct3d-12-raytracing-hlsl-shaders"></a><span data-ttu-id="ef2c9-103">Direct3D 12 Raytracing HLSL 著色器</span><span class="sxs-lookup"><span data-stu-id="ef2c9-103">Direct3D 12 Raytracing HLSL Shaders</span></span>

<span data-ttu-id="ef2c9-104">下列 HLSL 著色器支援 Direct3D 12 raytracing 管線。</span><span class="sxs-lookup"><span data-stu-id="ef2c9-104">The following HLSL shaders support the Direct3D 12 raytracing pipeline.</span></span> <span data-ttu-id="ef2c9-105">這些著色器是編譯成程式庫的函式，其中包含目標模型 lib_6_3，並由著色器函式上的屬性 *[著色器 ( "shadertype" ) ]* 識別。</span><span class="sxs-lookup"><span data-stu-id="ef2c9-105">These shaders are functions compiled into a library, with target model lib_6_3, and identified by an attribute *[shader("shadertype")]* on the shader function.</span></span> <span data-ttu-id="ef2c9-106">請參閱 **內建函式** 和 **系統值** ，以查看每個著色器類型所允許的內容。</span><span class="sxs-lookup"><span data-stu-id="ef2c9-106">See **Intrinsics** and **System Values** to see what is allowed for each shader type.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="ef2c9-107">本節內容</span><span class="sxs-lookup"><span data-stu-id="ef2c9-107">In this section</span></span>



| <span data-ttu-id="ef2c9-108">主題</span><span class="sxs-lookup"><span data-stu-id="ef2c9-108">Topic</span></span>                                                                                                       | <span data-ttu-id="ef2c9-109">描述</span><span class="sxs-lookup"><span data-stu-id="ef2c9-109">Description</span></span>                                                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ef2c9-110">**任何命中著色器**</span><span class="sxs-lookup"><span data-stu-id="ef2c9-110">**Any Hit Shader**</span></span>](any-hit-shader.md)<br/>                              | <span data-ttu-id="ef2c9-111">當光線交集不透明時，所叫用的著色器。</span><span class="sxs-lookup"><span data-stu-id="ef2c9-111">A shader that is invoked when ray intersections are not opaque.</span></span><br/>                                                                                                                                                                                                                                              |
| [<span data-ttu-id="ef2c9-112">**可呼叫著色器**</span><span class="sxs-lookup"><span data-stu-id="ef2c9-112">**Callable Shader**</span></span>](callable-shader.md)<br/>                              | <span data-ttu-id="ef2c9-113">從具有 **CallShader** 內建的另一個著色器叫用的著色器。</span><span class="sxs-lookup"><span data-stu-id="ef2c9-113">A shader that is invoked from another shader with the **CallShader** intrinsic.</span></span><br/>                                                                                                                                                                                                                                              |
| [<span data-ttu-id="ef2c9-114">**最接近的點擊著色器**</span><span class="sxs-lookup"><span data-stu-id="ef2c9-114">**Closest Hit Shader**</span></span>](closest-hit-shader.md)<br/>                              | <span data-ttu-id="ef2c9-115">當它已啟用，且已判定最接近的點擊，或光線交集搜尋結束時，即會叫用著色器。</span><span class="sxs-lookup"><span data-stu-id="ef2c9-115">A shader that is invoked when it is enabled and the closest hit has been determined or ray intersection search ended.</span></span><br/>                                                                                                                                                                                                                                              |
| [<span data-ttu-id="ef2c9-116">**交集著色器**</span><span class="sxs-lookup"><span data-stu-id="ef2c9-116">**Intersection Shader**</span></span>](intersection-shader.md)<br/>                              | <span data-ttu-id="ef2c9-117">著色器，用來針對與關聯的周框方塊 (周框方塊) 相交的光線，執行自訂交集基本專案。</span><span class="sxs-lookup"><span data-stu-id="ef2c9-117">A shader that is used to implement custom intersection primitives for rays intersecting an associated bounding volume (bounding box).</span></span><br/>                                                                                                                                                                                                                                              |
| [<span data-ttu-id="ef2c9-118">**遺漏著色器**</span><span class="sxs-lookup"><span data-stu-id="ef2c9-118">**Miss Shader**</span></span>](miss-shader.md)<br/>                              | <span data-ttu-id="ef2c9-119">找不到或不接受光線交集時，所叫用的著色器。</span><span class="sxs-lookup"><span data-stu-id="ef2c9-119">A shader that is invoked when no ray intersections are found or accepted.</span></span><br/>                                                                                                                                                                                                                                              |
| [<span data-ttu-id="ef2c9-120">**光線產生著色器**</span><span class="sxs-lookup"><span data-stu-id="ef2c9-120">**Ray Generation Shader**</span></span>](ray-generation-shader.md)<br/>                              | <span data-ttu-id="ef2c9-121">呼叫 [**TraceRay**](traceray-function.md) 以產生光線的著色器。</span><span class="sxs-lookup"><span data-stu-id="ef2c9-121">A shader that calls [**TraceRay**](traceray-function.md) to generate rays.</span></span><br/>                                                                                                                                                                                                                                              |

## <a name="related-topics"></a><span data-ttu-id="ef2c9-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="ef2c9-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ef2c9-123">核心參考</span><span class="sxs-lookup"><span data-stu-id="ef2c9-123">Core Reference</span></span>](direct3d-12-core-reference.md)
</dt> <dt>

[<span data-ttu-id="ef2c9-124">Direct3D 12 參考</span><span class="sxs-lookup"><span data-stu-id="ef2c9-124">Direct3D 12 Reference</span></span>](direct3d-12-reference.md)
</dt> </dl>

 

 





