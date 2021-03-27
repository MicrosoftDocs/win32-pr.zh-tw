---
title: " (Direct3D 11 圖形) 的著色器結構"
description: 結構是用來建立和使用著色器。
ms.assetid: 3b8ece5c-5065-4711-b12c-06cf7ea0e1ba
keywords:
- 結構，Direct3D 11 著色器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14739e3db38c075e19e58a90b12bbf7d06b48a4e
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "103685430"
---
# <a name="shader-structures-direct3d-11-graphics"></a><span data-ttu-id="a9710-104"> (Direct3D 11 圖形) 的著色器結構</span><span class="sxs-lookup"><span data-stu-id="a9710-104">Shader Structures (Direct3D 11 Graphics)</span></span>

<span data-ttu-id="a9710-105">結構是用來建立和使用著色器。</span><span class="sxs-lookup"><span data-stu-id="a9710-105">Structures are used to create and use shaders.</span></span>


## <a name="in-this-section"></a><span data-ttu-id="a9710-106">本節內容</span><span class="sxs-lookup"><span data-stu-id="a9710-106">In this section</span></span>



| <span data-ttu-id="a9710-107">主題</span><span class="sxs-lookup"><span data-stu-id="a9710-107">Topic</span></span>                                                                                       | <span data-ttu-id="a9710-108">描述</span><span class="sxs-lookup"><span data-stu-id="a9710-108">Description</span></span>                                                            |
|---------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="a9710-109">**D3D11 \_ 類別 \_ 實例 \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="a9710-109">**D3D11\_CLASS\_INSTANCE\_DESC**</span></span>](/windows/desktop/api/D3D11/ns-d3d11-d3d11_class_instance_desc)<br/>                | <span data-ttu-id="a9710-110">描述 HLSL 類別實例。</span><span class="sxs-lookup"><span data-stu-id="a9710-110">Describes an HLSL class instance.</span></span><br/>                           |
| [<span data-ttu-id="a9710-111">**D3D11 \_ 計算 \_ 著色器 \_ 追蹤 \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="a9710-111">**D3D11\_COMPUTE\_SHADER\_TRACE\_DESC**</span></span>](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_compute_shader_trace_desc)<br/>   | <span data-ttu-id="a9710-112">描述要追蹤的計算著色器實例。</span><span class="sxs-lookup"><span data-stu-id="a9710-112">Describes an instance of a compute shader to trace.</span></span><br/>         |
| [<span data-ttu-id="a9710-113">**D3D11 \_ 網域 \_ 著色器 \_ 追蹤 \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="a9710-113">**D3D11\_DOMAIN\_SHADER\_TRACE\_DESC**</span></span>](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_domain_shader_trace_desc)<br/>     | <span data-ttu-id="a9710-114">描述要追蹤之網域著色器的實例。</span><span class="sxs-lookup"><span data-stu-id="a9710-114">Describes an instance of a domain shader to trace.</span></span><br/>          |
| [<span data-ttu-id="a9710-115">**D3D11 \_ 函數 \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="a9710-115">**D3D11\_FUNCTION\_DESC**</span></span>](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_function_desc)<br/>                             | <span data-ttu-id="a9710-116">描述函數。</span><span class="sxs-lookup"><span data-stu-id="a9710-116">Describes a function.</span></span><br/>                                       |
| [<span data-ttu-id="a9710-117">**D3D11 \_ 幾何 \_ 著色器 \_ 追蹤 \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="a9710-117">**D3D11\_GEOMETRY\_SHADER\_TRACE\_DESC**</span></span>](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_geometry_shader_trace_desc)<br/> | <span data-ttu-id="a9710-118">描述要追蹤之幾何著色器的實例。</span><span class="sxs-lookup"><span data-stu-id="a9710-118">Describes an instance of a geometry shader to trace.</span></span><br/>        |
| [<span data-ttu-id="a9710-119">**D3D11 \_ 輪廓 \_ 著色器 \_ 追蹤 \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="a9710-119">**D3D11\_HULL\_SHADER\_TRACE\_DESC**</span></span>](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_hull_shader_trace_desc)<br/>         | <span data-ttu-id="a9710-120">描述要追蹤的輪廓著色器實例。</span><span class="sxs-lookup"><span data-stu-id="a9710-120">Describes an instance of a hull shader to trace.</span></span><br/>            |
| [<span data-ttu-id="a9710-121">**D3D11 連結 \_ 庫 \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="a9710-121">**D3D11\_LIBRARY\_DESC**</span></span>](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_library_desc)<br/>                               | <span data-ttu-id="a9710-122">描述程式庫。</span><span class="sxs-lookup"><span data-stu-id="a9710-122">Describes a library.</span></span><br/>                                        |
| [<span data-ttu-id="a9710-123">**D3D11 \_ 參數 \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="a9710-123">**D3D11\_PARAMETER\_DESC**</span></span>](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_parameter_desc)<br/>                           | <span data-ttu-id="a9710-124">描述函數參數。</span><span class="sxs-lookup"><span data-stu-id="a9710-124">Describes a function parameter.</span></span> <br/>                            |
| [<span data-ttu-id="a9710-125">**D3D11 \_ 圖元 \_ 著色器 \_ 追蹤 \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="a9710-125">**D3D11\_PIXEL\_SHADER\_TRACE\_DESC**</span></span>](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_pixel_shader_trace_desc)<br/>       | <span data-ttu-id="a9710-126">描述要追蹤之圖元著色器的實例。</span><span class="sxs-lookup"><span data-stu-id="a9710-126">Describes an instance of a pixel shader to trace.</span></span><br/>           |
| [<span data-ttu-id="a9710-127">**D3D11 \_ 著色器 \_ 緩衝區 \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="a9710-127">**D3D11\_SHADER\_BUFFER\_DESC**</span></span>](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_shader_buffer_desc)<br/>                  | <span data-ttu-id="a9710-128">描述著色器常數緩衝區。</span><span class="sxs-lookup"><span data-stu-id="a9710-128">Describes a shader constant-buffer.</span></span><br/>                         |
| [<span data-ttu-id="a9710-129">**D3D11 \_ 著色器 \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="a9710-129">**D3D11\_SHADER\_DESC**</span></span>](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_shader_desc)<br/>                                 | <span data-ttu-id="a9710-130">描述著色器。</span><span class="sxs-lookup"><span data-stu-id="a9710-130">Describes a shader.</span></span><br/>                                         |
| [<span data-ttu-id="a9710-131">**D3D11 \_ 著色器輸入系結 \_ \_ \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="a9710-131">**D3D11\_SHADER\_INPUT\_BIND\_DESC**</span></span>](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_shader_input_bind_desc)<br/>         | <span data-ttu-id="a9710-132">描述著色器資源系結至著色器輸入的方式。</span><span class="sxs-lookup"><span data-stu-id="a9710-132">Describes how a shader resource is bound to a shader input.</span></span><br/> |
| [<span data-ttu-id="a9710-133">**D3D11 \_ 著色器 \_ 追蹤 \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="a9710-133">**D3D11\_SHADER\_TRACE\_DESC**</span></span>](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_shader_trace_desc)<br/>                    | <span data-ttu-id="a9710-134">描述著色器追蹤物件。</span><span class="sxs-lookup"><span data-stu-id="a9710-134">Describes a shader-trace object.</span></span><br/>                            |
| [<span data-ttu-id="a9710-135">**D3D11 \_ 著色器 \_ 類型 \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="a9710-135">**D3D11\_SHADER\_TYPE\_DESC**</span></span>](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_shader_type_desc)<br/>                      | <span data-ttu-id="a9710-136">描述著色器變數型別。</span><span class="sxs-lookup"><span data-stu-id="a9710-136">Describes a shader-variable type.</span></span><br/>                           |
| [<span data-ttu-id="a9710-137">**D3D11 \_ 著色器 \_ 變數 \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="a9710-137">**D3D11\_SHADER\_VARIABLE\_DESC**</span></span>](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_shader_variable_desc)<br/>              | <span data-ttu-id="a9710-138">描述著色器變數。</span><span class="sxs-lookup"><span data-stu-id="a9710-138">Describes a shader variable.</span></span><br/>                                |
| [<span data-ttu-id="a9710-139">**D3D11 \_ 簽名 \_ 參數 \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="a9710-139">**D3D11\_SIGNATURE\_PARAMETER\_DESC**</span></span>](/windows/desktop/api/D3D11Shader/ns-d3d11shader-d3d11_signature_parameter_desc)<br/>      | <span data-ttu-id="a9710-140">描述著色器簽章。</span><span class="sxs-lookup"><span data-stu-id="a9710-140">Describes a shader signature.</span></span><br/>                               |
| [<span data-ttu-id="a9710-141">**D3D11 \_ 追蹤 \_ 註冊**</span><span class="sxs-lookup"><span data-stu-id="a9710-141">**D3D11\_TRACE\_REGISTER**</span></span>](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_trace_register)<br/>                           | <span data-ttu-id="a9710-142">描述追蹤註冊。</span><span class="sxs-lookup"><span data-stu-id="a9710-142">Describes a trace register.</span></span><br/>                                 |
| [<span data-ttu-id="a9710-143">**D3D11 \_ 追蹤 \_ 統計資料**</span><span class="sxs-lookup"><span data-stu-id="a9710-143">**D3D11\_TRACE\_STATS**</span></span>](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_trace_stats)<br/>                                 | <span data-ttu-id="a9710-144">指定追蹤的相關統計資料。</span><span class="sxs-lookup"><span data-stu-id="a9710-144">Specifies statistics about a trace.</span></span><br/>                         |
| [<span data-ttu-id="a9710-145">**D3D11 \_ 追蹤 \_ 步驟**</span><span class="sxs-lookup"><span data-stu-id="a9710-145">**D3D11\_TRACE\_STEP**</span></span>](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_trace_step)<br/>                                   | <span data-ttu-id="a9710-146">描述追蹤步驟，這是一個指令。</span><span class="sxs-lookup"><span data-stu-id="a9710-146">Describes a trace step, which is an instruction.</span></span><br/>            |
| [<span data-ttu-id="a9710-147">**D3D11 \_ 追蹤 \_ 值**</span><span class="sxs-lookup"><span data-stu-id="a9710-147">**D3D11\_TRACE\_VALUE**</span></span>](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_trace_value)<br/>                                 | <span data-ttu-id="a9710-148">描述追蹤值。</span><span class="sxs-lookup"><span data-stu-id="a9710-148">Describes a trace value.</span></span><br/>                                    |
| [<span data-ttu-id="a9710-149">**D3D11 \_ 頂點 \_ 著色器 \_ 追蹤 \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="a9710-149">**D3D11\_VERTEX\_SHADER\_TRACE\_DESC**</span></span>](/windows/desktop/api/D3D11ShaderTracing/ns-d3d11shadertracing-d3d11_vertex_shader_trace_desc)<br/>     | <span data-ttu-id="a9710-150">描述要追蹤之頂點著色器的實例。</span><span class="sxs-lookup"><span data-stu-id="a9710-150">Describes an instance of a vertex shader to trace.</span></span><br/>          |



 

## <a name="related-topics"></a><span data-ttu-id="a9710-151">相關主題</span><span class="sxs-lookup"><span data-stu-id="a9710-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a9710-152">著色器參考</span><span class="sxs-lookup"><span data-stu-id="a9710-152">Shader Reference</span></span>](d3d11-graphics-reference-d3d11-shader.md)
</dt> </dl>

 

 





