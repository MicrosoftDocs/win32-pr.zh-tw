---
title: distance
description: 傳回兩個向量之間的距離純量。
ms.assetid: dda8dc39-fd72-4e92-bf9d-e700db0ede9e
keywords:
- 距離 HLSL
topic_type:
- apiref
api_name:
- distance
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c0f3a64778666ac8f7de16b91eed202e36e90ed1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315586"
---
# <a name="distance"></a>distance

傳回兩個向量之間的距離純量。



| *ret* 距離 (*x*， *y*)  |
|--------------------------|



 

## <a name="parameters"></a>參數



| 項目                                                   | 描述                                                    |
|--------------------------------------------------------|----------------------------------------------------------------|
| <span id="x"></span><span id="X"></span>*X*<br/> | \[在 \] 要比較的第一個浮點向量中。<br/>  |
| <span id="y"></span><span id="Y"></span>*Y*<br/> | \[在 \] 要比較的第二個浮點數向量中。<br/> |



 

## <a name="return-value"></a>傳回值

浮點純量值，表示 *x* 參數與 *y* 參數之間的距離。

## <a name="type-description"></a>類型描述



| Name  | [**範本類型**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**元件類型**](dx-graphics-hlsl-intrinsic-functions.md) | 大小                           |
|-------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *x*   | [**向量**](dx-graphics-hlsl-intrinsic-functions.md) | [**浮動**](/windows/desktop/WinProg/windows-data-types)                        | 任意                            |
| *y*   | [**向量**](dx-graphics-hlsl-intrinsic-functions.md) | [**浮動**](/windows/desktop/WinProg/windows-data-types)                        | ) 為輸入 *x* 的相同維度 (s |
| *Ret* | [**純量 (scalar)**](dx-graphics-hlsl-intrinsic-functions.md) | [**FLOAT**](/windows/desktop/WinProg/windows-data-types)                        | 1                              |



 

## <a name="minimum-shader-model"></a>最小著色器模型

下列著色器模型支援此函數。



| 著色器模型                                                                       | 支援 |
|------------------------------------------------------------------------------------|-----------|
| [著色器模型 2 (DIRECTX HLSL) ](dx-graphics-hlsl-sm2.md) 和更高的著色器模型 | 是       |
| [著色器模型 1 (DirectX HLSL) ](dx-graphics-hlsl-sm1.md)                          | vs \_ 1 \_ 1  |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**(DirectX HLSL) 內建函式**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

