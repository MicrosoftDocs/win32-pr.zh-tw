---
title: CD3D11 Helper 結構
description: Direct3D 11 定義了數個協助程式結構，可讓您用來建立 Direct3D 結構。 這些 helper 結構的行為就像 c + + 類別一樣。
ms.assetid: E44951D9-7830-4825-B7FA-CF98CC0D024C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 578e8fb398ef5348146f9623f98f0b6d01414a50
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "104463953"
---
# <a name="cd3d11-helper-structures"></a><span data-ttu-id="6f88b-104">CD3D11 Helper 結構</span><span class="sxs-lookup"><span data-stu-id="6f88b-104">CD3D11 Helper Structures</span></span>

<span data-ttu-id="6f88b-105">Direct3D 11 定義了數個協助程式結構，可讓您用來建立 Direct3D 結構。</span><span class="sxs-lookup"><span data-stu-id="6f88b-105">Direct3D 11 defines several helper structures that you can use to create Direct3D structures.</span></span> <span data-ttu-id="6f88b-106">這些 helper 結構的行為就像 c + + 類別一樣。</span><span class="sxs-lookup"><span data-stu-id="6f88b-106">These helper structures behave like C++ classes.</span></span>


## <a name="in-this-section"></a><span data-ttu-id="6f88b-107">本節內容</span><span class="sxs-lookup"><span data-stu-id="6f88b-107">In this section</span></span>



| <span data-ttu-id="6f88b-108">主題</span><span class="sxs-lookup"><span data-stu-id="6f88b-108">Topic</span></span>                                                                                         | <span data-ttu-id="6f88b-109">描述</span><span class="sxs-lookup"><span data-stu-id="6f88b-109">Description</span></span>                                                                                                                         |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6f88b-110">**CD3D11 \_ RECT**</span><span class="sxs-lookup"><span data-stu-id="6f88b-110">**CD3D11\_RECT**</span></span>](/windows/win32/api/d3d11/ns-d3d11-cd3d11_rect)<br/>                                                | <span data-ttu-id="6f88b-111">表示矩形，並提供便利的方法來建立矩形。</span><span class="sxs-lookup"><span data-stu-id="6f88b-111">Represents a rectangle and provides convenience methods for creating rectangles.</span></span><br/>                                         |
| [<span data-ttu-id="6f88b-112">**CD3D11 \_ BOX**</span><span class="sxs-lookup"><span data-stu-id="6f88b-112">**CD3D11\_BOX**</span></span>](/windows/win32/api/d3d11/ns-d3d11-cd3d11_box)<br/>                                                  | <span data-ttu-id="6f88b-113">表示方塊，並提供建立方塊的便利方法。</span><span class="sxs-lookup"><span data-stu-id="6f88b-113">Represents a box and provides convenience methods for creating boxes.</span></span><br/>                                                    |
| [<span data-ttu-id="6f88b-114">**CD3D11 \_ 深度 \_ 樣板 \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="6f88b-114">**CD3D11\_DEPTH\_STENCIL\_DESC**</span></span>](/windows/win32/api/d3d11/ns-d3d11-cd3d11_depth_stencil_desc)<br/>                  | <span data-ttu-id="6f88b-115">表示深度樣板狀態結構，並提供建立深度樣板狀態結構的便利方法。</span><span class="sxs-lookup"><span data-stu-id="6f88b-115">Represents a depth-stencil-state structure and provides convenience methods for creating depth-stencil-state structures.</span></span><br/> |
| [<span data-ttu-id="6f88b-116">**CD3D11 \_ BLEND \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="6f88b-116">**CD3D11\_BLEND\_DESC**</span></span>](/windows/desktop/api/D3D11/ns-d3d11-cd3d11_blend_desc)<br/>                                   | <span data-ttu-id="6f88b-117">表示 blend 結構，並提供建立 blend 狀態結構的便利方法。</span><span class="sxs-lookup"><span data-stu-id="6f88b-117">Represents a blend-state structure and provides convenience methods for creating blend-state structures.</span></span><br/>                 |
| [<span data-ttu-id="6f88b-118">**CD3D11 轉譯器 \_ \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="6f88b-118">**CD3D11\_RASTERIZER\_DESC**</span></span>](/windows/win32/api/d3d11/ns-d3d11-cd3d11_rasterizer_desc)<br/>                         | <span data-ttu-id="6f88b-119">表示轉譯器狀態結構，並提供建立轉譯器狀態結構的便利方法。</span><span class="sxs-lookup"><span data-stu-id="6f88b-119">Represents a rasterizer-state structure and provides convenience methods for creating rasterizer-state structures.</span></span><br/>       |
| [<span data-ttu-id="6f88b-120">**CD3D11 \_ 緩衝區 \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="6f88b-120">**CD3D11\_BUFFER\_DESC**</span></span>](/windows/desktop/api/D3D11/ns-d3d11-cd3d11_buffer_desc)<br/>                                 | <span data-ttu-id="6f88b-121">代表緩衝區，並提供建立緩衝區的便利方法。</span><span class="sxs-lookup"><span data-stu-id="6f88b-121">Represents a buffer and provides convenience methods for creating buffers.</span></span><br/>                                               |
| [<span data-ttu-id="6f88b-122">**CD3D11 \_ TEXTURE1D \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="6f88b-122">**CD3D11\_TEXTURE1D\_DESC**</span></span>](/windows/win32/api/d3d11/ns-d3d11-cd3d11_texture1d_desc)<br/>                           | <span data-ttu-id="6f88b-123">代表1D 材質，並提供建立1D 紋理的便利方法。</span><span class="sxs-lookup"><span data-stu-id="6f88b-123">Represents a 1D texture and provides convenience methods for creating 1D textures.</span></span><br/>                                       |
| [<span data-ttu-id="6f88b-124">**CD3D11 \_ TEXTURE2D \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="6f88b-124">**CD3D11\_TEXTURE2D\_DESC**</span></span>](/windows/win32/api/d3d11/ns-d3d11-cd3d11_texture2d_desc)<br/>                           | <span data-ttu-id="6f88b-125">代表2D 材質，並提供建立2D 材質的便利方法。</span><span class="sxs-lookup"><span data-stu-id="6f88b-125">Represents a 2D texture and provides convenience methods for creating 2D textures.</span></span><br/>                                       |
| [<span data-ttu-id="6f88b-126">**CD3D11 \_ TEXTURE3D \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="6f88b-126">**CD3D11\_TEXTURE3D\_DESC**</span></span>](/windows/win32/api/d3d11/ns-d3d11-cd3d11_texture3d_desc)<br/>                           | <span data-ttu-id="6f88b-127">表示3D 材質，並提供建立3D 紋理的便利方法。</span><span class="sxs-lookup"><span data-stu-id="6f88b-127">Represents a 3D texture and provides convenience methods for creating 3D textures.</span></span><br/>                                       |
| [<span data-ttu-id="6f88b-128">**CD3D11 \_ 著色器 \_ 資源 \_ 視圖 \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="6f88b-128">**CD3D11\_SHADER\_RESOURCE\_VIEW\_DESC**</span></span>](/windows/win32/api/d3d11/ns-d3d11-cd3d11_shader_resource_view_desc)<br/>   | <span data-ttu-id="6f88b-129">表示著色器資源檢視，並提供建立著色器資源檢視的便利方法。</span><span class="sxs-lookup"><span data-stu-id="6f88b-129">Represents a shader-resource view and provides convenience methods for creating shader-resource views.</span></span><br/>                   |
| [<span data-ttu-id="6f88b-130">**CD3D11 \_ 轉譯 \_ 目標 \_ 視圖 \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="6f88b-130">**CD3D11\_RENDER\_TARGET\_VIEW\_DESC**</span></span>](/windows/win32/api/d3d11/ns-d3d11-cd3d11_render_target_view_desc)<br/>       | <span data-ttu-id="6f88b-131">表示轉譯目標視圖，並提供建立呈現目標視圖的便利方法。</span><span class="sxs-lookup"><span data-stu-id="6f88b-131">Represents a render-target view and provides convenience methods for creating render-target views.</span></span><br/>                       |
| [<span data-ttu-id="6f88b-132">**CD3D11 \_ 區**</span><span class="sxs-lookup"><span data-stu-id="6f88b-132">**CD3D11\_VIEWPORT**</span></span>](/windows/win32/api/d3d11/ns-d3d11-cd3d11_viewport)<br/>                                        | <span data-ttu-id="6f88b-133">代表一個區，並提供便利的方法來建立查看區。</span><span class="sxs-lookup"><span data-stu-id="6f88b-133">Represents a viewport and provides convenience methods for creating viewports.</span></span><br/>                                           |
| [<span data-ttu-id="6f88b-134">**CD3D11 \_ 深度 \_ 樣板 \_ 視圖 \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="6f88b-134">**CD3D11\_DEPTH\_STENCIL\_VIEW\_DESC**</span></span>](/windows/win32/api/d3d11/ns-d3d11-cd3d11_depth_stencil_view_desc)<br/>       | <span data-ttu-id="6f88b-135">代表深度樣板視圖，並提供建立深度樣板視圖的便利方法。</span><span class="sxs-lookup"><span data-stu-id="6f88b-135">Represents a depth-stencil view and provides convenience methods for creating depth-stencil views.</span></span><br/>                       |
| [<span data-ttu-id="6f88b-136">**CD3D11 未 \_ 排序的 \_ 存取權 \_ 視圖 \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="6f88b-136">**CD3D11\_UNORDERED\_ACCESS\_VIEW\_DESC**</span></span>](/windows/win32/api/d3d11/ns-d3d11-cd3d11_unordered_access_view_desc)<br/> | <span data-ttu-id="6f88b-137">代表未排序的存取視圖，並提供建立未排序存取視圖的便利方法。</span><span class="sxs-lookup"><span data-stu-id="6f88b-137">Represents a unordered-access view and provides convenience methods for creating unordered-access views.</span></span><br/>                 |
| [<span data-ttu-id="6f88b-138">**CD3D11 \_ 取樣器 \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="6f88b-138">**CD3D11\_SAMPLER\_DESC**</span></span>](/windows/win32/api/d3d11/ns-d3d11-cd3d11_sampler_desc)<br/>                               | <span data-ttu-id="6f88b-139">表示取樣器狀態，並提供建立取樣器狀態的便利方法。</span><span class="sxs-lookup"><span data-stu-id="6f88b-139">Represents a sampler state and provides convenience methods for creating sampler states.</span></span><br/>                                 |
| [<span data-ttu-id="6f88b-140">**CD3D11 \_ 查詢 \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="6f88b-140">**CD3D11\_QUERY\_DESC**</span></span>](/windows/win32/api/d3d11/ns-d3d11-cd3d11_query_desc)<br/>                                   | <span data-ttu-id="6f88b-141">表示查詢，並提供建立查詢的便利方法。</span><span class="sxs-lookup"><span data-stu-id="6f88b-141">Represents a query and provides convenience methods for creating queries.</span></span><br/>                                                |
| [<span data-ttu-id="6f88b-142">**CD3D11 \_ 計數器 \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="6f88b-142">**CD3D11\_COUNTER\_DESC**</span></span>](/windows/win32/api/d3d11/ns-d3d11-cd3d11_counter_desc)<br/>                               | <span data-ttu-id="6f88b-143">代表計數器，並提供建立計數器的便利方法。</span><span class="sxs-lookup"><span data-stu-id="6f88b-143">Represents a counter and provides convenience methods for creating counters.</span></span><br/>                                             |



 

## <a name="related-topics"></a><span data-ttu-id="6f88b-144">相關主題</span><span class="sxs-lookup"><span data-stu-id="6f88b-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6f88b-145">Direct3D 11 參考</span><span class="sxs-lookup"><span data-stu-id="6f88b-145">Direct3D 11 Reference</span></span>](d3d11-graphics-reference.md)
</dt> </dl>

 

