---
title: 如何建立輪廓著色器
description: 本主題說明如何建立輪廓著色器。
ms.assetid: 221cb578-fcfc-411a-8515-7880a96e32ce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1a1eea7d2e6e70377028976f9576790ce3b64ab
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671655"
---
# <a name="how-to-create-a-hull-shader"></a><span data-ttu-id="823e1-103">如何：建立輪廓著色器</span><span class="sxs-lookup"><span data-stu-id="823e1-103">How To: Create a Hull Shader</span></span>

<span data-ttu-id="823e1-104">輪廓著色器是三個階段中的第一個，可共同運作以實行 [鑲嵌](direct3d-11-advanced-stages-tessellation.md)式。</span><span class="sxs-lookup"><span data-stu-id="823e1-104">A hull shader is the first of three stages that work together to implement [tessellation](direct3d-11-advanced-stages-tessellation.md).</span></span> <span data-ttu-id="823e1-105">輪廓著色器輸出會驅動鑲嵌階段以及網域著色器階段。</span><span class="sxs-lookup"><span data-stu-id="823e1-105">The hull-shader outputs drive the tessellator stage, as well as the domain-shader stage.</span></span> <span data-ttu-id="823e1-106">本主題說明如何建立輪廓著色器。</span><span class="sxs-lookup"><span data-stu-id="823e1-106">This topic shows how to create a hull shader.</span></span>

<span data-ttu-id="823e1-107">輪廓著色器會將一組輸入控制點 (從頂點著色器) 轉換為一組輸出控制點。</span><span class="sxs-lookup"><span data-stu-id="823e1-107">A hull shader transforms a set of input control points (from a vertex shader) into a set of output control points.</span></span> <span data-ttu-id="823e1-108">輸入和輸出點的數目可能會隨著轉換而有所不同， (一般轉換會是基礎轉換) 。</span><span class="sxs-lookup"><span data-stu-id="823e1-108">The number of input and output points can vary in contents and number depending on the transform (a typical transformation would be a basis transformation).</span></span>

<span data-ttu-id="823e1-109">輪廓著色器也會輸出網域著色器和鑲嵌的 patch 常數資訊，例如鑲嵌式因素。</span><span class="sxs-lookup"><span data-stu-id="823e1-109">A hull shader also outputs patch constant information, such as tessellation factors, for a domain shader and the tessellator.</span></span> <span data-ttu-id="823e1-110">固定函式鑲嵌階段會使用鑲嵌式因素以及在輪廓著色器中宣告的其他狀態，來決定要 tessellate 多少。</span><span class="sxs-lookup"><span data-stu-id="823e1-110">The fixed-function tessellator stage uses the tessellation factors as well as other state declared in a hull shader to determine how much to tessellate.</span></span>

<span data-ttu-id="823e1-111">**若要建立輪廓著色器**</span><span class="sxs-lookup"><span data-stu-id="823e1-111">**To create a hull shader**</span></span>

1.  <span data-ttu-id="823e1-112">設計輪廓著色器。</span><span class="sxs-lookup"><span data-stu-id="823e1-112">Design a hull shader.</span></span> <span data-ttu-id="823e1-113">請參閱 [如何：設計輪廓著色器](direct3d-11-advanced-stages-hull-shader-design.md)。</span><span class="sxs-lookup"><span data-stu-id="823e1-113">See [How To: Design a Hull Shader](direct3d-11-advanced-stages-hull-shader-design.md).</span></span>
2.  <span data-ttu-id="823e1-114">編譯著色器程式碼</span><span class="sxs-lookup"><span data-stu-id="823e1-114">Compile the shader code</span></span>
3.  <span data-ttu-id="823e1-115">使用 [**ID3D11Device：： CreateHullShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createhullshader)建立輪廓著色器物件。</span><span class="sxs-lookup"><span data-stu-id="823e1-115">Create a hull-shader object using [**ID3D11Device::CreateHullShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createhullshader).</span></span>
    ```
    HRESULT CreateHullShader(
      const void *pShaderBytecode,  
      SIZE_T BytecodeLength,  
      ID3D11ClassLinkage *pClassLinkage,  
      ID3D11HullShader **ppHullShader
    );
    ```

    

4.  <span data-ttu-id="823e1-116">使用 [**>id3d11devicecoNtext：： HSSetShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hssetshader)初始化管線階段。</span><span class="sxs-lookup"><span data-stu-id="823e1-116">Initialize the pipeline stage using [**ID3D11DeviceContext::HSSetShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hssetshader).</span></span>
    ```
    void HSSetShader(
      ID3D11HullShader *pHullShader,  
      ID3D11ClassInstance *const *ppClassInstances,
      UINT NumClassInstances
    );
    ```

    

<span data-ttu-id="823e1-117">如果已系結輪廓著色器，則必須將網域著色器系結至管線。</span><span class="sxs-lookup"><span data-stu-id="823e1-117">A domain shader must be bound to the pipeline if a hull shader is bound.</span></span> <span data-ttu-id="823e1-118">尤其是，使用幾何著色器直接串流出輪廓著色器的控制點是不正確。</span><span class="sxs-lookup"><span data-stu-id="823e1-118">In particular, it is not valid to directly stream out hull shader control points with the geometry shader.</span></span>

## <a name="related-topics"></a><span data-ttu-id="823e1-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="823e1-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="823e1-120">如何使用 Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="823e1-120">How to Use Direct3D 11</span></span>](how-to-use-direct3d-11.md)
</dt> <dt>

[<span data-ttu-id="823e1-121">鑲嵌式總覽</span><span class="sxs-lookup"><span data-stu-id="823e1-121">Tessellation Overview</span></span>](direct3d-11-advanced-stages-tessellation.md)
</dt> </dl>

 

 




