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
# <a name="how-to-create-a-domain-shader"></a>如何：建立網域著色器

網域著色器是三個階段中的第三個，可共同運作以實行 [鑲嵌](direct3d-11-advanced-stages-tessellation.md)式。 網域著色器階段的輸入來自于輪廓著色器。 本主題說明如何建立網域著色器。

使用輪廓著色器輸出控制點、輪廓著色器輸出 patch-常數資料，以及一組鑲嵌的 uv 座標，網域著色器 (由固定函式的鑲嵌) 階段所建立的介面幾何轉換。

**若要建立網域著色器**

1.  設計網域著色器。 請參閱 [如何：設計定義域著色器](direct3d-11-advanced-stages-domain-shader-design.md)。
2.  編譯著色器程式碼。
3.  使用 [**ID3D11Device：： CreateDomainShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdomainshader)建立網域著色器物件。
    ```
    HRESULT CreateDomainShader(
      const void *pShaderBytecode, // 
      SIZE_T BytecodeLength, // 
      ID3D11ClassLinkage *pClassLinkage, // 
      ID3D11DomainShader **ppDomainShader
    );
    ```

    

4.  使用 >id3d11devicecoNtext 初始化管線階段 [**：:D ssetshader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dssetshader)。
    ```
    void DSSetShader(
      ID3D11DomainShader *pDomainShader, // 
      ID3D11ClassInstance *const *ppClassInstances,
      UINT NumClassInstances
    );
    ```

    

如果已系結輪廓著色器，則必須將網域著色器系結至管線。 尤其是，使用幾何著色器直接串流出輪廓著色器的控制點是不正確。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[如何使用 Direct3D 11](how-to-use-direct3d-11.md)
</dt> <dt>

[鑲嵌式總覽](direct3d-11-advanced-stages-tessellation.md)
</dt> </dl>

 

 




