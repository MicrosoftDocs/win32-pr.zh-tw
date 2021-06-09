---
title: " (Direct3D 9 HLSL) 的片段宣告語法"
description: 您可以透過新增片段宣告，將每個 Microsoft 高階著色器語言 (HLSL) 函數轉換成著色器片段。
ms.assetid: 34ceef8c-8fb9-4c73-86cc-014b7a2ee4d7
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 60ac1153ff3491bc904f4f759f6653cb4243adff
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/09/2021
ms.locfileid: "111825725"
---
# <a name="fragment-declaration-syntax-direct3d-9-hlsl"></a> (Direct3D 9 HLSL) 的片段宣告語法

您可以透過新增片段宣告，將每個 Microsoft 高階著色器語言 (HLSL) 函數轉換成著色器片段。

## <a name="syntax"></a>Syntax


```
fragmentKeyword FragmentName = compile_fragment shaderProfile FunctionName();
```



其中：



| 值                  | 描述                                                                                                                                                                                                                                                      |
|-------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| fragmentKeyword   | 必要關鍵字。 可能是 pixelfragment 或 vertexfragment。                                                                                                                                                                                             |
| FragmentName      | 指定已編譯片段名稱的 ASCII 文字字串。                                                                                                                                                                                       |
| 編譯 \_ 片段 | 必要關鍵字。                                                                                                                                                                                                                                     |
| shaderProfile     | 要針對編譯的著色器模型。 任何有效的頂點著色器設定檔 (查看 [**D3DXGetVertexShaderProfile**](/windows/desktop/direct3d9/d3dxgetvertexshaderprofile)) 或圖元著色器設定檔 (參閱 [**D3DXGetPixelShaderProfile**](/windows/desktop/direct3d9/d3dxgetpixelshaderprofile)) 。 |
| FunctionName ()     | 著色器函式名稱，後面接著括弧。                                                                                                                                                                                                    |



 

共用片段參數會藉由將 ' r \_ ' 前置詞新增至其語義來標記。


```
void AmbientDiffuse( float3 vPosWorld: r_PosWorld,
                     float3 vNormalWorld: r_NormalWorld,
                     out float4 vColor: COLOR0 )
{  
    // Compute the light vector
    float3 vLight = normalize( g_vLightPosition - vPosWorld );
    
    // Compute the ambient and diffuse components of illumination
    vColor = g_vLightColor * g_vMaterialAmbient;
    vColor += g_vLightColor * g_vMaterialDiffuse * saturate( dot( vLight, vNormalWorld ) );
}
vertexfragment AmbientDiffuseFragment = compile_fragment vs_1_1 AmbientDiffuse();
```



在此範例中，r \_ PosWorld 和 r \_ NormalWorld 語義會識別這兩個參數是其他片段之間的共用參數。

> [!Note]  
> 片段連結器是 D3DX 9 中的 Microsoft Direct3D 9 技術。 片段連結器是一種工具 (Flink.exe) 、D3DX 9 API，以及 HLSL 增強功能。 從2009年8月的 DirectX SDK 版本中卸載了片段連結器。 片段連結器從未套用到 Microsoft Direct3D 10、Microsoft Direct3D 10.1 或 Microsoft Direct3D 11。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[著色器模型 3 (DirectX HLSL) ](dx-graphics-hlsl-sm3.md)
</dt> </dl>

 

 
