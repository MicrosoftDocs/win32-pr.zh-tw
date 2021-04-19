---
title: " (Direct3D 12 圖形) 的著色器結構"
description: d3d12shader 會宣告下列結構，這些結構是用來建立和使用著色器。
ms.assetid: b8ece5c3-5065-4711-b12c-6cf7ea0e1ba0
keywords:
- 結構，Direct3D 12 著色器
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 400d50c48b8b94fc9a59d8e48179aae43e14a4f5
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "106967511"
---
# <a name="shader-structures-direct3d-12-graphics"></a><span data-ttu-id="9ae05-104"> (Direct3D 12 圖形) 的著色器結構</span><span class="sxs-lookup"><span data-stu-id="9ae05-104">Shader Structures (Direct3D 12 Graphics)</span></span>

<span data-ttu-id="9ae05-105">d3d12shader 會宣告下列結構，這些結構是用來建立和使用著色器。</span><span class="sxs-lookup"><span data-stu-id="9ae05-105">d3d12shader.h declares the following structures, which are used to create and use shaders.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="9ae05-106">本節內容</span><span class="sxs-lookup"><span data-stu-id="9ae05-106">In this section</span></span>



| <span data-ttu-id="9ae05-107">主題</span><span class="sxs-lookup"><span data-stu-id="9ae05-107">Topic</span></span>                                                                                  | <span data-ttu-id="9ae05-108">描述</span><span class="sxs-lookup"><span data-stu-id="9ae05-108">Description</span></span>                                                             |
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [<span data-ttu-id="9ae05-109">**D3D12 \_ 函數 \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="9ae05-109">**D3D12\_FUNCTION\_DESC**</span></span>](/windows/desktop/api/d3d12shader/ns-d3d12shader-d3d12_function_desc)<br/>                        | <span data-ttu-id="9ae05-110">描述函數。</span><span class="sxs-lookup"><span data-stu-id="9ae05-110">Describes a function.</span></span> <br/>                                       |
| [<span data-ttu-id="9ae05-111">**D3D12 連結 \_ 庫 \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="9ae05-111">**D3D12\_LIBRARY\_DESC**</span></span>](/windows/desktop/api/d3d12shader/ns-d3d12shader-d3d12_library_desc)<br/>                          | <span data-ttu-id="9ae05-112">描述程式庫。</span><span class="sxs-lookup"><span data-stu-id="9ae05-112">Describes a library.</span></span> <br/>                                        |
| [<span data-ttu-id="9ae05-113">**D3D12 \_ 參數 \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="9ae05-113">**D3D12\_PARAMETER\_DESC**</span></span>](/windows/desktop/api/d3d12shader/ns-d3d12shader-d3d12_parameter_desc)<br/>                      | <span data-ttu-id="9ae05-114">描述函數參數。</span><span class="sxs-lookup"><span data-stu-id="9ae05-114">Describes a function parameter.</span></span> <br/>                             |
| [<span data-ttu-id="9ae05-115">**D3D12 \_ 著色器 \_ 緩衝區 \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="9ae05-115">**D3D12\_SHADER\_BUFFER\_DESC**</span></span>](/windows/desktop/api/d3d12shader/ns-d3d12shader-d3d12_shader_buffer_desc)<br/>             | <span data-ttu-id="9ae05-116">描述著色器常數緩衝區。</span><span class="sxs-lookup"><span data-stu-id="9ae05-116">Describes a shader constant-buffer.</span></span> <br/>                         |
| [<span data-ttu-id="9ae05-117">**D3D12 \_ 著色器 \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="9ae05-117">**D3D12\_SHADER\_DESC**</span></span>](/windows/desktop/api/d3d12shader/ns-d3d12shader-d3d12_shader_desc)<br/>                            | <span data-ttu-id="9ae05-118">描述著色器。</span><span class="sxs-lookup"><span data-stu-id="9ae05-118">Describes a shader.</span></span> <br/>                                         |
| [<span data-ttu-id="9ae05-119">**D3D12 \_ 著色器輸入系結 \_ \_ \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="9ae05-119">**D3D12\_SHADER\_INPUT\_BIND\_DESC**</span></span>](/windows/desktop/api/d3d12shader/ns-d3d12shader-d3d12_shader_input_bind_desc)<br/>    | <span data-ttu-id="9ae05-120">描述著色器資源系結至著色器輸入的方式。</span><span class="sxs-lookup"><span data-stu-id="9ae05-120">Describes how a shader resource is bound to a shader input.</span></span> <br/> |
| [<span data-ttu-id="9ae05-121">**D3D12 \_ 著色器 \_ 類型 \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="9ae05-121">**D3D12\_SHADER\_TYPE\_DESC**</span></span>](/windows/desktop/api/d3d12shader/ns-d3d12shader-d3d12_shader_type_desc)<br/>                 | <span data-ttu-id="9ae05-122">描述著色器變數型別。</span><span class="sxs-lookup"><span data-stu-id="9ae05-122">Describes a shader-variable type.</span></span> <br/>                           |
| [<span data-ttu-id="9ae05-123">**D3D12 \_ 著色器 \_ 變數 \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="9ae05-123">**D3D12\_SHADER\_VARIABLE\_DESC**</span></span>](/windows/desktop/api/d3d12shader/ns-d3d12shader-d3d12_shader_variable_desc)<br/>         | <span data-ttu-id="9ae05-124">描述著色器變數。</span><span class="sxs-lookup"><span data-stu-id="9ae05-124">Describes a shader variable.</span></span> <br/>                                |
| [<span data-ttu-id="9ae05-125">**D3D12 \_ 簽名 \_ 參數 \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="9ae05-125">**D3D12\_SIGNATURE\_PARAMETER\_DESC**</span></span>](/windows/desktop/api/d3d12shader/ns-d3d12shader-d3d12_signature_parameter_desc)<br/> | <span data-ttu-id="9ae05-126">描述著色器簽章。</span><span class="sxs-lookup"><span data-stu-id="9ae05-126">Describes a shader signature.</span></span> <br/>                               |



 

## <a name="related-topics"></a><span data-ttu-id="9ae05-127">相關主題</span><span class="sxs-lookup"><span data-stu-id="9ae05-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9ae05-128">Direct3D 12 參考</span><span class="sxs-lookup"><span data-stu-id="9ae05-128">Direct3D 12 Reference</span></span>](direct3d-12-reference.md)
</dt> <dt>

[<span data-ttu-id="9ae05-129">著色器參考</span><span class="sxs-lookup"><span data-stu-id="9ae05-129">Shader Reference</span></span>](d3d12-graphics-reference-shader-reference.md)
</dt> </dl>

 

 





