---
title: max
description: 選取 x 和 y 的較大。
ms.assetid: 08e17a0c-6d44-49ea-b613-bd262534522c
keywords:
- 最大 HLSL
topic_type:
- apiref
api_name:
- max
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9a40ccb32bb2c2fcd7ca7342b9d7d4d143688102
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104376193"
---
# <a name="max"></a>max

選取 x 和 y 的較大。



| ret max (x，y)  |
|---------------|



 

## <a name="parameters"></a>參數



| 項目                                                   | 描述                          |
|--------------------------------------------------------|--------------------------------------|
| <span id="x"></span><span id="X"></span>*X*<br/> | \[在 \] [x 輸入值] 中。<br/> |
| <span id="y"></span><span id="Y"></span>*Y*<br/> | \[（在 \] y 輸入值中）。<br/> |



 

## <a name="return-value"></a>傳回值

*X* 或 *y* 參數，以最大值為准。


## <a name="remarks"></a>備註

Denormals 的處理方式如下：

| src0 src1-> | -inf | F             | +inf | NAN  |
|-------------|------|---------------|------|------|
| -inf        | -inf | src1          | +inf | -inf |
| F           | src0 | src0 或 src1  | +inf | src0 |
| +inf        | +inf | +inf          | +inf | +inf |
| NaN         | -inf | src1          | +inf | NaN  |

F 表示有限實數。


## <a name="type-description"></a>類型描述

| Name | 輸入/輸出      | [**範本類型**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**元件類型**](dx-graphics-hlsl-intrinsic-functions.md)                 | 大小                         |
|------|-------------|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|------------------------------|
| x    | in          | 純 [**量、**](dx-graphics-hlsl-intrinsic-functions.md)**向量** 或 **矩陣** | [**float**](/windows/desktop/WinProg/windows-data-types)、 [ **int**](/windows/desktop/WinProg/windows-data-types) | 任意                          |
| y    | in          | 與輸入 x 相同                                                                                                | [**float**](/windows/desktop/WinProg/windows-data-types)、 [ **int**](/windows/desktop/WinProg/windows-data-types) | ) 為輸入 x 的相同維度 (s |
| Ret  | 傳回類型 | 與輸入 x 相同                                                                                                | [**float**](/windows/desktop/WinProg/windows-data-types)、 [ **int**](/windows/desktop/WinProg/windows-data-types) | ) 為輸入 x 的相同維度 (s |



 

## <a name="minimum-shader-model"></a>最小著色器模型

下列著色器模型支援此函數。



| 著色器模型                                                                       | 支援                   |
|------------------------------------------------------------------------------------|-----------------------------|
| [著色器模型 2 (DIRECTX HLSL) ](dx-graphics-hlsl-sm2.md) 和更高的著色器模型 | 是                         |
| [著色器模型 1 (DirectX HLSL) ](dx-graphics-hlsl-sm1.md)                          | 是 (vs \_ 1 \_ 1 和 ps \_ 1 \_ 4)  |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**(DirectX HLSL) 內建函式**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

[**DirectX 功能規格**](https://microsoft.github.io/DirectX-Specs/d3d/archive/D3D11_3_FunctionalSpec.htm#inst_MAX) 
</dt> </dl>
 
