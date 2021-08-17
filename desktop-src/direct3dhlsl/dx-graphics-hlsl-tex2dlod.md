---
title: tex2Dlod
description: 使用 mipmap 取樣2D 材質。 Mipmap」 LOD 是在 t.w. 中指定的
ms.assetid: 689eff39-f6ac-4c25-8b92-ca68707ae8ad
keywords:
- tex2Dlod HLSL
topic_type:
- apiref
api_name:
- tex2Dlod
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f9581418eb2a3d8736fcd0e125eaafec11494e6b6d5471cef33f9592475d5ec0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117725676"
---
# <a name="tex2dlod"></a>tex2Dlod

使用 mipmap 取樣2D 材質。 Mipmap」 LOD 是在 t.w. 中指定的



| ret tex2Dlod (s，t)  |
|--------------------|



 

## <a name="parameters"></a>參數



| 項目                                                   | 描述                               |
|--------------------------------------------------------|-------------------------------------------|
| <span id="s"></span><span id="S"></span>*！*<br/> | \[在 \] 取樣器狀態中。<br/>      |
| <span id="t"></span><span id="T"></span>*10gbase-t*<br/> | \[在 \] 紋理座標中。<br/> |



 

## <a name="return-value"></a>傳回值

材質資料的值。

## <a name="type-description"></a>類型描述



| 名稱 | 輸入/輸出 | [**範本類型**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**元件類型**](dx-graphics-hlsl-intrinsic-functions.md) | 大小 |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| s    | in     | [**物件**](dx-graphics-hlsl-intrinsic-functions.md) | [sampler2D](dx-graphics-hlsl-sampler.md)                      | 1    |
| t    | in     | [**向量**](dx-graphics-hlsl-intrinsic-functions.md) | [**浮動**](/windows/desktop/WinProg/windows-data-types)                        | 4    |
| Ret  | out    | [**向量**](dx-graphics-hlsl-intrinsic-functions.md) | [**浮動**](/windows/desktop/WinProg/windows-data-types)                        | 4    |



 

## <a name="minimum-shader-model"></a>最小著色器模型

下列著色器模型支援此函數。



| 著色器模型                                                                       | 支援 |
|------------------------------------------------------------------------------------|-----------|
| [著色器模型 3 (DIRECTX HLSL) ](dx-graphics-hlsl-sm3.md) 和更高的著色器模型 | 是       |
| [著色器模型 2 (DirectX HLSL) ](dx-graphics-hlsl-sm2.md)                          | 否        |
| [著色器模型 1 (DirectX HLSL) ](dx-graphics-hlsl-sm1.md)                          | 否        |



 

## <a name="remarks"></a>備註

從 Direct3D 10 開始，您可以使用新的 HLSL 語法來存取材質和其他資源。 您可以使用更多物件導向的樣式來取代內建樣式的紋理查閱函數（例如 **tex2Dlod**）。 在此物件導向的樣式中，紋理會與取樣器分離，並具有載入和取樣的方法。

若要取樣2D 材質，請不要使用 **tex2Dlod** ，如下列程式碼所示：


```
sampler S;
...
color = tex2Dlod(S, Location);
```



使用 [**紋理物件**](dx-graphics-hlsl-to-type.md)的 [SampleLevel](dx-graphics-hlsl-to-samplelevel.md)方法，如下列程式碼所示：


```
Texture2D MyTexture;
SamplerState MySampler;
...
color = MyTexture.SampleLevel(MySampler, Location, LOD);
```



若要使用內建樣式的材質查閱函數（例如 **tex2Dlod**），並搭配 [著色器模型 4](dx-graphics-hlsl-sm4.md) 和更高版本，請使用 [**D3DCOMPILE \_ 讓回溯 \_ \_ 相容性**](d3dcompile-constants.md) 進行編譯。 但是，如果您想要以著色器模型4和更高版本為目標 (甚至是[ \* \_ 4 \_ 0 \_ 層級 \_ 9 \_ \* ](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro)) 具有較新的物件導向樣式程式碼，請遷移至較新的 HLSL 語法。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**(DirectX HLSL) 內建函式**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

