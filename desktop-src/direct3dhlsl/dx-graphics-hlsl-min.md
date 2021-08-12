---
title: 分鐘
description: 選取 x 和 y 的較小者。
ms.assetid: 4e10cfc2-d680-4d7f-81b2-fa52024f902d
keywords:
- 最小 HLSL
topic_type:
- apiref
api_name:
- min
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8ba9474383af448c36c6bb1130470aa6706fd8bd06c2d21bef66eb1c4bbcda0b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118513819"
---
# <a name="min"></a>分鐘

選取 x 和 y 的較小者。



| ret min (x，y)  |
|---------------|



 

## <a name="parameters"></a>參數



| Item                                                   | 描述                          |
|--------------------------------------------------------|--------------------------------------|
| <span id="x"></span><span id="X"></span>*X*<br/> | \[在 \] [x 輸入值] 中。<br/> |
| <span id="y"></span><span id="Y"></span>*Y*<br/> | \[（在 \] y 輸入值中）。<br/> |



 

## <a name="return-value"></a>傳回值

*X* 或 *y* 參數，以最小值為准。


## <a name="remarks"></a>備註

Denormals 的處理方式如下：

| src0 src1-> | -inf | F             | +inf | NAN  |
|-------------|------|---------------|------|------|
| -inf        | -inf | -inf          | -inf | -inf |
| F           | -inf | src0 或 src1  | src0 | src0 |
| +inf        | -inf | src1          | +inf | +inf |
| NaN         | -inf | src1          | +inf | NaN  |

F 表示有限實數。


## <a name="type-description"></a>類型描述

| 名稱 | 輸入/輸出      | [**範本類型**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**元件類型**](dx-graphics-hlsl-intrinsic-functions.md)                 | 大小                         |
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

[**DirectX 功能規格**](https://microsoft.github.io/DirectX-Specs/d3d/archive/D3D11_3_FunctionalSpec.htm#inst_MIN)