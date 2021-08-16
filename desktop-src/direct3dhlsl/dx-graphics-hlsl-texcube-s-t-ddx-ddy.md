---
title: texCUBE (HLSL 參考) -選取 mip 層級
description: '使用漸層來選取 mip 層級，以取樣 cube 紋理。 |texCUBE (HLSL 參考) '
ms.assetid: 5615f48b-eb0a-4de7-a441-51ec3cecf6fd
keywords:
- texCUBE HLSL
topic_type:
- apiref
api_name:
- texCUBE
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4e236a17359f94adcb8b54d3af8b67df37b1fcb6aaf7e75e6f4dba298eaae7aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117725656"
---
# <a name="texcube-hlsl-reference---select-the-mip-level"></a>texCUBE (HLSL 參考) -選取 mip 層級

使用漸層來選取 mip 層級，以取樣 cube 紋理。



| ret texCUBE (s、t、ddx、ddy)  |
|-----------------------------|



 

## <a name="parameters"></a>參數



| 項目                                                         | 描述                                                                  |
|--------------------------------------------------------------|------------------------------------------------------------------------------|
| <span id="s"></span><span id="S"></span>*！*<br/>       | \[在 \] 取樣器狀態中。<br/>                                         |
| <span id="t"></span><span id="T"></span>*10gbase-t*<br/>       | \[在 \] 紋理座標中。<br/>                                    |
| <span id="ddx"></span><span id="DDX"></span>*ddx*<br/> | \[以 \] x 方向變更 surface 幾何的速率。<br/> |
| <span id="ddy"></span><span id="DDY"></span>*ddy*<br/> | \[以 \] y 方向變更 surface 幾何的速率。<br/> |



 

## <a name="return-value"></a>傳回值

材質資料的值。

## <a name="type-description"></a>類型描述



| 名稱 | 輸入/輸出 | [**範本類型**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**元件類型**](dx-graphics-hlsl-intrinsic-functions.md) | 大小 |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| s    | in     | [**物件**](dx-graphics-hlsl-intrinsic-functions.md) | [samplerCUBE](dx-graphics-hlsl-sampler.md)                    | 1    |
| t    | in     | [**向量**](dx-graphics-hlsl-intrinsic-functions.md) | [**浮動**](/windows/desktop/WinProg/windows-data-types)                        | 3    |
| ddx  | in     | [**向量**](dx-graphics-hlsl-intrinsic-functions.md) | [**浮動**](/windows/desktop/WinProg/windows-data-types)                        | 3    |
| ddy  | in     | [**向量**](dx-graphics-hlsl-intrinsic-functions.md) | [**浮動**](/windows/desktop/WinProg/windows-data-types)                        | 3    |
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

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**(DirectX HLSL) 內建函式**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

