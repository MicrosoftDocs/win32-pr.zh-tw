---
title: 如何建立網域著色器
description: 本主題說明如何建立網域著色器。
ms.assetid: 7d02fee4-2d7c-434b-86ab-e5ee615ae93b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f89b7f3d7ec6cf801432a5745520fcbd924d139
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104020973"
---
# <a name="how-to-create-a-domain-shader"></a><span data-ttu-id="8c3de-103">如何：建立網域著色器</span><span class="sxs-lookup"><span data-stu-id="8c3de-103">How To: Create a Domain Shader</span></span>

<span data-ttu-id="8c3de-104">網域著色器是三個階段中的第三個，可共同運作以實行 [鑲嵌](direct3d-11-advanced-stages-tessellation.md)式。</span><span class="sxs-lookup"><span data-stu-id="8c3de-104">A domain shader is the third of three stages that work together to implement [tessellation](direct3d-11-advanced-stages-tessellation.md).</span></span> <span data-ttu-id="8c3de-105">網域著色器階段的輸入來自于輪廓著色器。</span><span class="sxs-lookup"><span data-stu-id="8c3de-105">The inputs for the domain-shader stage come from a hull shader.</span></span> <span data-ttu-id="8c3de-106">本主題說明如何建立網域著色器。</span><span class="sxs-lookup"><span data-stu-id="8c3de-106">This topic shows how to create a domain shader.</span></span>

<span data-ttu-id="8c3de-107">使用輪廓著色器輸出控制點、輪廓著色器輸出 patch-常數資料，以及一組鑲嵌的 uv 座標，網域著色器 (由固定函式的鑲嵌) 階段所建立的介面幾何轉換。</span><span class="sxs-lookup"><span data-stu-id="8c3de-107">A domain shader transforms surface geometry (created by the fixed-function tessellator stage) using hull shader output-control points, hull shader output patch-constant data, and a single set of tessellator uv coordinates.</span></span>

<span data-ttu-id="8c3de-108">**若要建立網域著色器**</span><span class="sxs-lookup"><span data-stu-id="8c3de-108">**To create a domain shader**</span></span>

1.  <span data-ttu-id="8c3de-109">設計網域著色器。</span><span class="sxs-lookup"><span data-stu-id="8c3de-109">Design a domain shader.</span></span> <span data-ttu-id="8c3de-110">請參閱 [如何：設計定義域著色器](direct3d-11-advanced-stages-domain-shader-design.md)。</span><span class="sxs-lookup"><span data-stu-id="8c3de-110">See [How To: Design a Domain Shader](direct3d-11-advanced-stages-domain-shader-design.md).</span></span>
2.  <span data-ttu-id="8c3de-111">編譯著色器程式碼。</span><span class="sxs-lookup"><span data-stu-id="8c3de-111">Compile the shader code.</span></span>
3.  <span data-ttu-id="8c3de-112">使用 [**ID3D11Device：： CreateDomainShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdomainshader)建立網域著色器物件。</span><span class="sxs-lookup"><span data-stu-id="8c3de-112">Create a domain-shader object using [**ID3D11Device::CreateDomainShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdomainshader).</span></span>
    ```
    HRESULT CreateDomainShader(
      const void *pShaderBytecode, // 
      SIZE_T BytecodeLength, // 
      ID3D11ClassLinkage *pClassLinkage, // 
      ID3D11DomainShader **ppDomainShader
    );
    ```

    

4.  <span data-ttu-id="8c3de-113">使用 >id3d11devicecoNtext 初始化管線階段 [**：:D ssetshader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dssetshader)。</span><span class="sxs-lookup"><span data-stu-id="8c3de-113">Initialize the pipeline stage using [**ID3D11DeviceContext::DSSetShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dssetshader).</span></span>
    ```
    void DSSetShader(
      ID3D11DomainShader *pDomainShader, // 
      ID3D11ClassInstance *const *ppClassInstances,
      UINT NumClassInstances
    );
    ```

    

<span data-ttu-id="8c3de-114">如果已系結輪廓著色器，則必須將網域著色器系結至管線。</span><span class="sxs-lookup"><span data-stu-id="8c3de-114">A domain shader must be bound to the pipeline if a hull shader is bound.</span></span> <span data-ttu-id="8c3de-115">尤其是，使用幾何著色器直接串流出輪廓著色器的控制點是不正確。</span><span class="sxs-lookup"><span data-stu-id="8c3de-115">In particular, it is not valid to directly stream out hull shader control points with the geometry shader.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8c3de-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="8c3de-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8c3de-117">如何使用 Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="8c3de-117">How to Use Direct3D 11</span></span>](how-to-use-direct3d-11.md)
</dt> <dt>

[<span data-ttu-id="8c3de-118">鑲嵌式總覽</span><span class="sxs-lookup"><span data-stu-id="8c3de-118">Tessellation Overview</span></span>](direct3d-11-advanced-stages-tessellation.md)
</dt> </dl>

 

 




