---
description: 本節包含下列著色器結構的相關資訊：
ms.assetid: b36309e0-1c44-42d9-adcf-33acd753438c
title: 著色器結構 (Direct3D 10 圖形)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e0d84096e743b15e0d5f85635dab4caf72c7e93
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104187786"
---
# <a name="shader-structures-direct3d-10-graphics"></a><span data-ttu-id="1dc3b-103">著色器結構 (Direct3D 10 圖形)</span><span class="sxs-lookup"><span data-stu-id="1dc3b-103">Shader Structures (Direct3D 10 Graphics)</span></span>

<span data-ttu-id="1dc3b-104">本節包含下列著色器結構的相關資訊：</span><span class="sxs-lookup"><span data-stu-id="1dc3b-104">This section contains information about the following shader structures:</span></span>



| <span data-ttu-id="1dc3b-105">結構</span><span class="sxs-lookup"><span data-stu-id="1dc3b-105">Structures</span></span>                                                                         | <span data-ttu-id="1dc3b-106">Description</span><span class="sxs-lookup"><span data-stu-id="1dc3b-106">Description</span></span>                                                                           |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [<span data-ttu-id="1dc3b-107">**D3D10 \_ 著色器 \_ 緩衝區 \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="1dc3b-107">**D3D10\_SHADER\_BUFFER\_DESC**</span></span>](/windows/win32/api/D3D10Shader/ns-d3d10shader-d3d10_shader_buffer_desc)                    | <span data-ttu-id="1dc3b-108">描述著色器常數緩衝區或著色器材質緩衝區。</span><span class="sxs-lookup"><span data-stu-id="1dc3b-108">Describes a shader-constant buffer or a shader-texture buffer.</span></span>                        |
| [<span data-ttu-id="1dc3b-109">**D3D10 \_ 著色器 \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="1dc3b-109">**D3D10\_SHADER\_DESC**</span></span>](/windows/win32/api/D3D10Shader/ns-d3d10shader-d3d10_shader_desc)                                   | <span data-ttu-id="1dc3b-110">描述著色器。</span><span class="sxs-lookup"><span data-stu-id="1dc3b-110">Describes a shader.</span></span>                                                                   |
| [<span data-ttu-id="1dc3b-111">**D3D10 \_ 著色器 \_ 調試檔 \_ \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="1dc3b-111">**D3D10\_SHADER\_DEBUG\_FILE\_INFO**</span></span>](/windows/win32/api/d3d10_1shader/ns-d3d10_1shader-d3d10_shader_debug_file_info)           | <span data-ttu-id="1dc3b-112">描述著色器所包含的檔案。</span><span class="sxs-lookup"><span data-stu-id="1dc3b-112">Describes files included by a shader.</span></span>                                                 |
| [<span data-ttu-id="1dc3b-113">**D3D10 \_ 著色器 \_ 調試 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="1dc3b-113">**D3D10\_SHADER\_DEBUG\_INFO**</span></span>](/windows/win32/api/d3d10_1shader/ns-d3d10_1shader-d3d10_shader_debug_info)                      | <span data-ttu-id="1dc3b-114">描述 D3D10GetShaderDebugInfo 所傳回之 ID3D10Blob 介面的格式。</span><span class="sxs-lookup"><span data-stu-id="1dc3b-114">Describes the format of the ID3D10Blob Interface returned by D3D10GetShaderDebugInfo.</span></span> |
| [<span data-ttu-id="1dc3b-115">**D3D10 \_ 著色器 \_ 調試的 \_ 輸入 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="1dc3b-115">**D3D10\_SHADER\_DEBUG\_INPUT\_INFO**</span></span>](/windows/win32/api/d3d10_1shader/ns-d3d10_1shader-d3d10_shader_debug_input_info)         | <span data-ttu-id="1dc3b-116">描述著色器輸入。</span><span class="sxs-lookup"><span data-stu-id="1dc3b-116">Describes a shader input.</span></span>                                                             |
| [<span data-ttu-id="1dc3b-117">**D3D10 \_ 著色器 \_ 調試 \_ INST \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="1dc3b-117">**D3D10\_SHADER\_DEBUG\_INST\_INFO**</span></span>](/windows/win32/api/d3d10_1shader/ns-d3d10_1shader-d3d10_shader_debug_inst_info)           | <span data-ttu-id="1dc3b-118">包含指令資料。</span><span class="sxs-lookup"><span data-stu-id="1dc3b-118">Contains instruction data.</span></span>                                                            |
| [<span data-ttu-id="1dc3b-119">**D3D10 \_ 著色器 \_ 調試 \_ OUTPUTREG \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="1dc3b-119">**D3D10\_SHADER\_DEBUG\_OUTPUTREG\_INFO**</span></span>](/windows/win32/api/d3d10_1shader/ns-d3d10_1shader-d3d10_shader_debug_outputreg_info) | <span data-ttu-id="1dc3b-120">描述著色器輸出暫存器。</span><span class="sxs-lookup"><span data-stu-id="1dc3b-120">Describes a shader output register.</span></span>                                                   |
| [<span data-ttu-id="1dc3b-121">**D3D10 \_ 著色器 \_ 調試 \_ OUTPUTVAR**</span><span class="sxs-lookup"><span data-stu-id="1dc3b-121">**D3D10\_SHADER\_DEBUG\_OUTPUTVAR**</span></span>](/windows/win32/api/d3d10_1shader/ns-d3d10_1shader-d3d10_shader_debug_outputvar)            | <span data-ttu-id="1dc3b-122">描述著色器輸出變數。</span><span class="sxs-lookup"><span data-stu-id="1dc3b-122">Describes a shader output variable.</span></span>                                                   |
| [<span data-ttu-id="1dc3b-123">**D3D10 \_ 著色器 \_ 調試 \_ 範圍 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="1dc3b-123">**D3D10\_SHADER\_DEBUG\_SCOPE\_INFO**</span></span>](/windows/win32/api/d3d10_1shader/ns-d3d10_1shader-d3d10_shader_debug_scope_info)         | <span data-ttu-id="1dc3b-124">包含將變數名稱對應至 debug 變數的範圍資料。</span><span class="sxs-lookup"><span data-stu-id="1dc3b-124">Contains scope data that maps variable names to debug variables.</span></span>                      |
| [<span data-ttu-id="1dc3b-125">**D3D10 \_ 著色器 \_ 調試 \_ SCOPEVAR \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="1dc3b-125">**D3D10\_SHADER\_DEBUG\_SCOPEVAR\_INFO**</span></span>](/windows/win32/api/d3d10_1shader/ns-d3d10_1shader-d3d10_shader_debug_scopevar_info)   | <span data-ttu-id="1dc3b-126">描述範圍變數。</span><span class="sxs-lookup"><span data-stu-id="1dc3b-126">Describes a scope variable.</span></span>                                                           |
| [<span data-ttu-id="1dc3b-127">**D3D10 \_ 著色器 \_ 調試 \_ TOKEN \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="1dc3b-127">**D3D10\_SHADER\_DEBUG\_TOKEN\_INFO**</span></span>](/windows/win32/api/d3d10_1shader/ns-d3d10_1shader-d3d10_shader_debug_token_info)         | <span data-ttu-id="1dc3b-128">提供著色器元素的來源位置。</span><span class="sxs-lookup"><span data-stu-id="1dc3b-128">Gives the source location for a shader element.</span></span>                                       |
| [<span data-ttu-id="1dc3b-129">**D3D10 \_ 著色器的 \_ DEBUG \_ VARTYPE**</span><span class="sxs-lookup"><span data-stu-id="1dc3b-129">**D3D10\_SHADER\_DEBUG\_VARTYPE**</span></span>](/windows/win32/api/d3d10_1shader/ne-d3d10_1shader-d3d10_shader_debug_vartype)                | <span data-ttu-id="1dc3b-130">區分變數與範圍中的函式。</span><span class="sxs-lookup"><span data-stu-id="1dc3b-130">Distinguishes variables from functions in a scope.</span></span>                                    |
| [<span data-ttu-id="1dc3b-131">**D3D10 \_ 著色器 \_ 調試的 \_ VAR \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="1dc3b-131">**D3D10\_SHADER\_DEBUG\_VAR\_INFO**</span></span>](/windows/win32/api/d3d10_1shader/ns-d3d10_1shader-d3d10_shader_debug_var_info)             | <span data-ttu-id="1dc3b-132">包含變數的資訊。</span><span class="sxs-lookup"><span data-stu-id="1dc3b-132">Contains information on a variable.</span></span>                                                   |
| [<span data-ttu-id="1dc3b-133">**D3D10 \_ 著色器輸入系結 \_ \_ \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="1dc3b-133">**D3D10\_SHADER\_INPUT\_BIND\_DESC**</span></span>](/windows/win32/api/D3D10Shader/ns-d3d10shader-d3d10_shader_input_bind_desc)           | <span data-ttu-id="1dc3b-134">描述著色器資源系結至著色器輸入的方式。</span><span class="sxs-lookup"><span data-stu-id="1dc3b-134">Describes how a shader resource is bound to a shader input.</span></span>                           |
| [<span data-ttu-id="1dc3b-135">**D3D \_ 著色器 \_ 宏**</span><span class="sxs-lookup"><span data-stu-id="1dc3b-135">**D3D\_SHADER\_MACRO**</span></span>](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro)                                 | <span data-ttu-id="1dc3b-136">定義著色器宏。</span><span class="sxs-lookup"><span data-stu-id="1dc3b-136">Defines a shader macro.</span></span>                                                               |
| [<span data-ttu-id="1dc3b-137">**D3D10 \_ 著色器 \_ 類型 \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="1dc3b-137">**D3D10\_SHADER\_TYPE\_DESC**</span></span>](/windows/win32/api/D3D10Shader/ns-d3d10shader-d3d10_shader_type_desc)                        | <span data-ttu-id="1dc3b-138">描述著色器變數型別。</span><span class="sxs-lookup"><span data-stu-id="1dc3b-138">Describes a shader-variable type.</span></span>                                                     |
| [<span data-ttu-id="1dc3b-139">**D3D10 \_ 著色器 \_ 變數 \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="1dc3b-139">**D3D10\_SHADER\_VARIABLE\_DESC**</span></span>](/windows/win32/api/D3D10Shader/ns-d3d10shader-d3d10_shader_variable_desc)                | <span data-ttu-id="1dc3b-140">描述著色器變數。</span><span class="sxs-lookup"><span data-stu-id="1dc3b-140">Describes a shader variable.</span></span>                                                          |
| [<span data-ttu-id="1dc3b-141">**D3D10 \_ 簽名 \_ 參數 \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="1dc3b-141">**D3D10\_SIGNATURE\_PARAMETER\_DESC**</span></span>](/windows/win32/api/D3D10Shader/ns-d3d10shader-d3d10_signature_parameter_desc)        | <span data-ttu-id="1dc3b-142">描述著色器簽章。</span><span class="sxs-lookup"><span data-stu-id="1dc3b-142">Describes a shader signature.</span></span>                                                         |



 

## <a name="related-topics"></a><span data-ttu-id="1dc3b-143">相關主題</span><span class="sxs-lookup"><span data-stu-id="1dc3b-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1dc3b-144">著色器參考</span><span class="sxs-lookup"><span data-stu-id="1dc3b-144">Shader Reference</span></span>](d3d10-graphics-reference-d3d10-shader.md)
</dt> </dl>

 

 



