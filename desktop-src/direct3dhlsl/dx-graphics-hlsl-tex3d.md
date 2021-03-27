---
title: 'tex3D (HLSL 參考) '
description: 範例3D 紋理。
ms.assetid: 713eec24-bdf5-456e-98da-30e2c9d7e808
keywords:
- tex3D HLSL
topic_type:
- apiref
api_name:
- tex3D
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e3a071d00dedabdff02bae302c71aa8ecece4ba2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682912"
---
# <a name="tex3d-hlsl-reference"></a>tex3D (HLSL 參考) 

範例3D 紋理。



| ret tex3D (s，t)  |
|-----------------|



 

## <a name="parameters"></a>參數



| 項目                                                   | 描述                               |
|--------------------------------------------------------|-------------------------------------------|
| <span id="s"></span><span id="S"></span>*！*<br/> | \[在 \] 取樣器狀態中。<br/>      |
| <span id="t"></span><span id="T"></span>*10gbase-t*<br/> | \[在 \] 紋理座標中。<br/> |



 

## <a name="return-value"></a>傳回值

材質資料的值。

## <a name="type-description"></a>類型描述



| Name | 輸入/輸出 | [**範本類型**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**元件類型**](dx-graphics-hlsl-intrinsic-functions.md) | 大小 |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| s    | in     | [**物件**](dx-graphics-hlsl-intrinsic-functions.md) | [sampler3D](dx-graphics-hlsl-sampler.md)                      | 1    |
| t    | in     | [**向量**](dx-graphics-hlsl-intrinsic-functions.md) | [**浮動**](/windows/desktop/WinProg/windows-data-types)                        | 3    |
| Ret  | out    | [**向量**](dx-graphics-hlsl-intrinsic-functions.md) | [**浮動**](/windows/desktop/WinProg/windows-data-types)                        | 4    |



 

## <a name="minimum-shader-model"></a>最小著色器模型

下列著色器模型支援此函數。



| 著色器模型                                              | 支援                                                                                                                         |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [著色器模型4](dx-graphics-hlsl-sm4.md)                | 是 (只) 圖元著色器，但在編譯時，您必須使用 [舊版編譯選項](/windows/desktop/direct3dtools/dx-graphics-tools-fxc-syntax) 。 |
| [著色器模型 3 (DirectX HLSL) ](dx-graphics-hlsl-sm3.md) | 是 (只) 圖元著色器                                                                                                           |
| [著色器模型 2 (DirectX HLSL) ](dx-graphics-hlsl-sm2.md) | 是 (只) 圖元著色器                                                                                                           |
| [著色器模型 1 (DirectX HLSL) ](dx-graphics-hlsl-sm1.md) | 是 (只) 圖元著色器                                                                                                           |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**(DirectX HLSL) 內建函式**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

