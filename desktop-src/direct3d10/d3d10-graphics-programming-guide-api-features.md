---
description: Direct3D 10 圖形管線代表基本的架構變更，從硬體和軟體的基礎中重建，以增強下一代的遊戲和3D 多媒體應用程式。
ms.assetid: 2e24de6c-4f73-4844-b87f-3487ef069db6
title: " (Direct3D 10) 的 API 功能"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab12285509441bb429c78d995e68ed1753ceb5bd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104187655"
---
# <a name="api-features-direct3d-10"></a><span data-ttu-id="14a07-103"> (Direct3D 10) 的 API 功能</span><span class="sxs-lookup"><span data-stu-id="14a07-103">API Features (Direct3D 10)</span></span>

<span data-ttu-id="14a07-104">Direct3D 10 圖形管線代表基本的架構變更，從硬體和軟體的基礎中重建，以增強下一代的遊戲和3D 多媒體應用程式。</span><span class="sxs-lookup"><span data-stu-id="14a07-104">The Direct3D 10 graphics pipeline represents a fundamental architecture change, rebuilt from the ground-up in hardware and software to power the next-generation of games and 3D multimedia applications.</span></span> <span data-ttu-id="14a07-105">它使用 Windows 顯示驅動程式模型 (WDDM) ，可啟用效能和行為的增強功能，例如虛擬 GPU 記憶體。</span><span class="sxs-lookup"><span data-stu-id="14a07-105">It uses the Windows Display Driver Model (WDDM), which enables performance and behavioral enhancements such as virtual GPU memory.</span></span>

<span data-ttu-id="14a07-106">熟悉 Direct3D 9 的開發人員將探索 Direct3D 10 中一系列的功能增強功能和效能改進，包括：</span><span class="sxs-lookup"><span data-stu-id="14a07-106">Developers familiar with Direct3D 9 will discover a series of functional enhancements and performance improvements in Direct3D 10, including:</span></span>

-   <span data-ttu-id="14a07-107">在新 [幾何著色器階段](/previous-versions//bb205146(v=vs.85))中處理整個基本專案的能力。</span><span class="sxs-lookup"><span data-stu-id="14a07-107">The ability to process entire primitives in the new [geometry-shader stage](/previous-versions//bb205146(v=vs.85)).</span></span>
-   <span data-ttu-id="14a07-108">使用 [資料流程輸出階段](../direct3d11/d3d10-graphics-programming-guide-output-stream-stage.md)將管線產生的頂點資料輸出至記憶體的能力。</span><span class="sxs-lookup"><span data-stu-id="14a07-108">The ability to output pipeline-generated vertex data to memory using the [stream-output stage](../direct3d11/d3d10-graphics-programming-guide-output-stream-stage.md).</span></span>
-   <span data-ttu-id="14a07-109">將管線狀態組織成5個不可變的 [狀態物件](d3d10-graphics-programming-guide-api-features-state-objects.md)，以便快速設定管線。</span><span class="sxs-lookup"><span data-stu-id="14a07-109">Organization of pipeline state into 5 immutable [state objects](d3d10-graphics-programming-guide-api-features-state-objects.md), enabling fast configuration of the pipeline.</span></span>
-   <span data-ttu-id="14a07-110">將著色器常陣列織成 [常數緩衝區](d3d10-graphics-programming-guide-resources-types.md)，將提供著色器常數資料的頻寬負荷降至最低。</span><span class="sxs-lookup"><span data-stu-id="14a07-110">Organization of shader constants into [constant buffers](d3d10-graphics-programming-guide-resources-types.md), minimizing bandwidth overhead for supplying shader-constant data.</span></span>
-   <span data-ttu-id="14a07-111">使用幾何著色器來執行每個基本材質交換和設定的能力。</span><span class="sxs-lookup"><span data-stu-id="14a07-111">The ability to perform per-primitive material swapping and setup using a geometry shader.</span></span>
-   <span data-ttu-id="14a07-112">新的 [資源類型](d3d10-graphics-programming-guide-resources-types.md) (包括可從著色器) 和資源格式編制索引的材質陣列。</span><span class="sxs-lookup"><span data-stu-id="14a07-112">New [resource types](d3d10-graphics-programming-guide-resources-types.md) (including texture arrays that can be indexed from shaders) and resource formats.</span></span>
-   <span data-ttu-id="14a07-113">使用 [view](d3d10-graphics-programming-guide-resources-access-views.md)提高資源存取的一般化。</span><span class="sxs-lookup"><span data-stu-id="14a07-113">Increased generalization of resource access using a [view](d3d10-graphics-programming-guide-resources-access-views.md).</span></span>
-   <span data-ttu-id="14a07-114">舊版硬體功能位 (caps) 已移除，以提供一組豐富的保證功能，其目標為 Direct3D 10 類別的硬體 (最小) 。</span><span class="sxs-lookup"><span data-stu-id="14a07-114">Legacy hardware capability bits (caps) have been removed in favor of a rich set of guaranteed functionality, which targets Direct3D 10-class hardware (minimum).</span></span>
-   <span data-ttu-id="14a07-115">[分層運行](d3d10-graphics-programming-guide-api-features-layers.md) 時間-DIRECT3D 10 API 是以核心的基本功能來建立，並建立選擇性和開發人員協助工具 (debug 等 ) 在外部層中。</span><span class="sxs-lookup"><span data-stu-id="14a07-115">[Layered Runtime](d3d10-graphics-programming-guide-api-features-layers.md) - The Direct3D 10 API is constructed with layers, starting with the basic functionality at the core and building optional and developer-assist functionality (debug, etc.) in outer layers.</span></span>
-   <span data-ttu-id="14a07-116">完整的 HLSL 整合-所有 Direct3D 10 著色器都會以 HLSL 撰寫，並以 [一般著色器核心](../direct3dhlsl/dx-graphics-hlsl-common-core.md)來執行。</span><span class="sxs-lookup"><span data-stu-id="14a07-116">Full HLSL integration - All Direct3D 10 shaders are written in HLSL and implemented with the [common-shader core](../direct3dhlsl/dx-graphics-hlsl-common-core.md).</span></span>
-   <span data-ttu-id="14a07-117">轉譯目標、紋理和取樣器數目的增加。</span><span class="sxs-lookup"><span data-stu-id="14a07-117">An increase in the number of render targets, textures, and samplers.</span></span> <span data-ttu-id="14a07-118">也沒有任何著色器長度限制。</span><span class="sxs-lookup"><span data-stu-id="14a07-118">There is also no shader length limit.</span></span>
-   <span data-ttu-id="14a07-119">整數和位著色器作業。</span><span class="sxs-lookup"><span data-stu-id="14a07-119">Integer and bitwise shader operations.</span></span>
-   <span data-ttu-id="14a07-120">Readback 深度/樣板表面或多重取樣資源不再系結為轉譯目標。</span><span class="sxs-lookup"><span data-stu-id="14a07-120">Readback of a depth/stencil surface or a multisampled resource, once it is no longer bound as a render target.</span></span>
-   <span data-ttu-id="14a07-121">多重取樣 Alpha 到涵蓋範圍支援。</span><span class="sxs-lookup"><span data-stu-id="14a07-121">Multisampled alpha-to-coverage support.</span></span>

<span data-ttu-id="14a07-122">Direct3D 9 開發人員也應該注意其他的行為差異， (請參閱 [direct3d 9 至 direct3d 10 考慮](d3d10-graphics-programming-guide-d3d9-to-d3d10-considerations.md)) 。</span><span class="sxs-lookup"><span data-stu-id="14a07-122">There are additional behavioral differences that Direct3D 9 developers should also be aware of (see [Direct3D 9 to Direct3D 10 Considerations](d3d10-graphics-programming-guide-d3d9-to-d3d10-considerations.md)).</span></span>

<span data-ttu-id="14a07-123">以下是已不再支援的 Direct3D 9 功能清單，或已在 Direct3D 10 中修改過的 Direct3D 9 功能 (參閱已 [淘汰的功能](d3d10-graphics-programming-guide-api-features-deprecated.md)) 。</span><span class="sxs-lookup"><span data-stu-id="14a07-123">Here is a list of Direct3D 9 features that either are no longer supported, or have been revised in Direct3D 10 (see [Deprecated Features](d3d10-graphics-programming-guide-api-features-deprecated.md)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="14a07-124">相關主題</span><span class="sxs-lookup"><span data-stu-id="14a07-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="14a07-125">Direct3D 10 程式設計手冊</span><span class="sxs-lookup"><span data-stu-id="14a07-125">Programming Guide for Direct3D 10</span></span>](d3d10-graphics-programming-guide.md)
</dt> </dl>

 

 
