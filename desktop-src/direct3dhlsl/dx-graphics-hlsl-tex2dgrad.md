---
title: tex2Dgrad
description: 使用漸層來選取 mip 層級，以取樣2D 材質。 |tex2Dgrad
ms.assetid: a9ab7972-3480-4b37-aa10-c5cf811bdd0e
keywords:
- tex2Dgrad HLSL
topic_type:
- apiref
api_name:
- tex2Dgrad
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 358690291cbb8cffbf6d60ef034b42d075902b923a3899824845e42bad999a21
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119912"
---
# <a name="tex2dgrad"></a>tex2Dgrad

使用漸層來選取 mip 層級，以取樣2D 材質。



| ret tex2Dgrad (s、t、ddx、ddy)  |
|-------------------------------|



 

## <a name="parameters"></a>參數



| 項目                                                         | 描述                                                                  |
|--------------------------------------------------------------|------------------------------------------------------------------------------|
| <span id="s"></span><span id="S"></span>*！*<br/>       | \[在 \] 取樣器狀態中。<br/>                                         |
| <span id="t"></span><span id="T"></span>*10gbase-t*<br/>       | \[在 \] 紋理座標中。<br/>                                   |
| <span id="ddx"></span><span id="DDX"></span>*ddx*<br/> | \[以 \] x 方向變更 surface 幾何的速率。<br/> |
| <span id="ddy"></span><span id="DDY"></span>*ddy*<br/> | \[以 \] y 方向變更 surface 幾何的速率。<br/> |



 

## <a name="return-value"></a>傳回值

材質資料的值。

## <a name="type-description"></a>類型描述



| 名稱 | 輸入/輸出 | [**範本類型**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**元件類型**](dx-graphics-hlsl-intrinsic-functions.md) | 大小 |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| s    | in     | [**物件**](dx-graphics-hlsl-intrinsic-functions.md) | [sampler2D](dx-graphics-hlsl-sampler.md)                      | 1    |
| t    | in     | [**向量**](dx-graphics-hlsl-intrinsic-functions.md) | [**浮動**](/windows/desktop/WinProg/windows-data-types)                        | 2    |
| ddx  | in     | [**向量**](dx-graphics-hlsl-intrinsic-functions.md) | [**浮動**](/windows/desktop/WinProg/windows-data-types)                        | 2    |
| ddy  | in     | [**向量**](dx-graphics-hlsl-intrinsic-functions.md) | [**浮動**](/windows/desktop/WinProg/windows-data-types)                        | 2    |
| Ret  | out    | [**向量**](dx-graphics-hlsl-intrinsic-functions.md) | [**浮動**](/windows/desktop/WinProg/windows-data-types)                        | 4    |



 

## <a name="minimum-shader-model"></a>最小著色器模型

下列著色器模型支援此函數。



| 著色器模型                                              | 支援                |
|-----------------------------------------------------------|--------------------------|
| [著色器模型4](dx-graphics-hlsl-sm4.md)                | 是 (只) 圖元著色器  |
| [著色器模型 3 (DirectX HLSL) ](dx-graphics-hlsl-sm3.md) | 是 (只) 圖元著色器 |
| [著色器模型 2 (DirectX HLSL) ](dx-graphics-hlsl-sm2.md) | 是 (只) 圖元著色器 |
| [著色器模型 1 (DirectX HLSL) ](dx-graphics-hlsl-sm1.md) | 否                       |



 

1.  大量的程式碼重新排列是為了將漸層計算移至流程式控制制之外。
2.  如果 D3DPSHADERCAPS2 \_ 0 cap 設定了 D3DD3DPSHADERCAPS2 \_ 0 \_ GRADIENTINSTRUCTIONS，則編譯器會將此函式對應至 texldd。

## <a name="remarks"></a>備註

當流程式控制件存在於著色器中時，在指定分支路徑內要求的漸層計算結果，在連續的圖元可能會中斷個別的流程式控制制路徑時則不明確。 因此，使用任何圖元著色器作業時，可能會要求漸層計算發生在流程式控制制結構內的位置，而該位置可能會因圖元而異，而對指定的基本類型進行了點陣化。 如果 **if** 語句的任一端與 branch 屬性使用漸層函式，可能會產生編譯器錯誤。 請參閱 [ (DIRECTX HLSL) 的 If 語句 ](dx-graphics-hlsl-if.md)。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**(DirectX HLSL) 內建函式**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

