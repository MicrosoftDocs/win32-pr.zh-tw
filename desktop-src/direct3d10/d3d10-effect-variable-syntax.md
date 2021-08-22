---
description: 效果變數是使用下列語法來宣告。
ms.assetid: 53939c65-3725-44cc-bec6-775c3b921770
title: " (Direct3D 10) 的效果變數語法"
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2422ba2cebf18c72a14d621ef13a98700aefd2858169c6e96566b455ec21d2ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119497708"
---
# <a name="effect-variable-syntax-direct3d-10"></a> (Direct3D 10) 的效果變數語法

效果變數是使用下列語法來宣告。

## <a name="syntax"></a>Syntax

*DataType* *VariableName* \[ ： *SemanticName* \]  <  *注釋*>;



| 名稱         | 描述                                                                                                                                                                                 |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DataType     | 任何 [基本](../direct3dhlsl/dx-graphics-hlsl-variable-syntax.md) 或 [紋理](../direct3dhlsl/dx-graphics-hlsl-to-type.md) 類型。                                                                        |
| VariableName | 可唯一識別效果變數名稱的 ASCII 字串。                                                                                                                   |
| SemanticName | 表示應該如何使用變數之其他資訊的 ASCII 字串。 語義是 ASCII 字串，可以是預先定義的系統值或自訂使用者字串。 |
| 註解  |  (中繼資料) 的一或多個使用者提供的資訊，會被效果系統忽略。 如需語法，請參閱 [ (Direct3D 10) 的批註語法 ](d3d10-effect-annotation-syntax.md)。     |



 

在所有函式之外宣告的效果變數都會被視為範圍中的全域。在函式中宣告的變數是該函式的本機變數。

## <a name="example"></a>範例

[BasicHLSL10 範例](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx)會使用全域變數，而不使用材質色彩、淺色屬性和轉換矩陣的語法。

此範例說明全域效果變數。


```
float4 g_MaterialAmbientColor;      // Material's ambient color
float4 g_MaterialDiffuseColor;      // Material's diffuse color
float3 g_LightDir[3];               // Light's direction in world space
float4x4 g_mWorld;                  // World matrix for object
```



此範例說明著色器函式本機的效果變數。


```
VS_OUTPUT RenderSceneVS( ... )
{
    float3 vNormalWorldSpace;
    float4 vAnimatedPos;

    // shader body
}
```



此範例說明具有語義的函數參數。


```
VS_OUTPUT RenderSceneVS( float4 vPos : SV_POSITION,
                         float3 vNormal : NORMAL,
                         float2 vTexCoord0 : TEXCOORD0,
                         uniform int nNumLights,
                         uniform bool bTexture,
                         uniform bool bAnimate )
{
  ...
}
```



此範例說明如何宣告材質變數。


```
Texture2D g_MeshTexture;            // Color texture for mesh
```



使用紋理取樣器來取樣紋理。 若要設定效果中的取樣器，請參閱 [取樣器類型](../direct3dhlsl/dx-graphics-hlsl-sampler.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[效果格式](d3d10-effect-format.md)
</dt> </dl>

 

 
