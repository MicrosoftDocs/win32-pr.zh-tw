---
title: 使用不含緩衝區的 Input-Assembler 階段
description: 如果您的著色器不需要緩衝區，則不需要建立和系結緩衝區。 本節包含繪製單一三角形的簡單頂點和圖元著色器範例。
ms.assetid: 84d24494-f2cb-4ca1-84fd-635e20f2c9ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a3aa4c63176d184e1e67349149bd1f4044159e1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104971349"
---
# <a name="using-the-input-assembler-stage-without-buffers"></a>使用不含緩衝區的 Input-Assembler 階段

如果您的著色器不需要緩衝區，則不需要建立和系結緩衝區。 本節包含繪製單一三角形的簡單頂點和圖元著色器範例。

-   [頂點著色器](#vertex-shader)
-   [圖元著色器](#pixel-shader)
-   [技巧](#technique)
-   [應用程式程式碼](#application-code)
-   [相關主題](#related-topics)

## <a name="vertex-shader"></a>頂點著色器

例如，您可以宣告可建立自己頂點的頂點著色器。


```
struct VSIn
{
    uint vertexId : SV_VertexID;
};

struct VSOut
{
    float4 pos : SV_Position;
    float4 color : color;
};

VSOut VSmain(VSIn input)
{
    VSOut output;
    
    if (input.vertexId == 0)
        output.pos = float4(0.0, 0.5, 0.5, 1.0);
    else if (input.vertexId == 2)
        output.pos = float4(0.5, -0.5, 0.5, 1.0);
    else if (input.vertexId == 1)
        output.pos = float4(-0.5, -0.5, 0.5, 1.0);
    
    output.color = clamp(output.pos, 0, 1);
    
    return output;
}
```



## <a name="pixel-shader"></a>像素著色器


```
// NoBuffer.fx
// Copyright (c) 2004 Microsoft Corporation. All rights reserved.
//

struct PSIn
{
    float4 pos : SV_Position;
    linear float4 color : color;
};

struct PSOut
{
    float4 color : SV_Target;
};


PSOut PSmain(PSIn input)
{
    PSOut output;
    
    output.color = input.color;
    
    return output;
}
```



## <a name="technique"></a>技巧

技術是轉譯行程的集合， (至少必須有一個 pass) 。


```
VertexShader vsCompiled = CompileShader( vs_4_0, VSmain() );

technique10 t0
{
    pass p0
    {
        SetVertexShader( vsCompiled );
        SetGeometryShader( NULL );
        SetPixelShader( CompileShader( ps_4_0, PSmain() ));
    }  
}
```



## <a name="application-code"></a>應用程式程式碼


```
m_pD3D11Device->IASetInputLayout( NULL );

m_pD3D11Device->IASetPrimitiveTopology( D3D_PRIMITIVE_TOPOLOGY_TRIANGLELIST );
    
ID3DX11EffectTechnique * pTech = NULL;
pTech = m_pEffect->GetTechniqueByIndex(0);
pTech->GetPassByIndex(iPass)->Apply(0);

m_pD3D11Device->Draw( 3, 0 );
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 Input-Assembler 階段開始使用](d3d10-graphics-programming-guide-input-assembler-stage-getting-started.md)
</dt> </dl>

 

 




