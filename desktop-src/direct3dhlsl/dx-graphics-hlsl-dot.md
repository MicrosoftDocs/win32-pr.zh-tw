---
title: dot
description: 傳回兩個向量的內積。
ms.assetid: ad24c06c-0b40-4dc5-a2b9-1d5438635ed8
keywords:
- 點 HLSL
topic_type:
- apiref
api_name:
- dot
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d6d05abf0d67628d1d77b362b028107e07b83457
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933495"
---
# <a name="dot"></a>dot

傳回兩個向量的內積。



| *ret* 點 (*x*， *y*)  |
|---------------------|



 

## <a name="parameters"></a>參數



| 項目                                                   | 描述                          |
|--------------------------------------------------------|--------------------------------------|
| <span id="x"></span><span id="X"></span>*X*<br/> | \[在 \] 第一個向量中。<br/>  |
| <span id="y"></span><span id="Y"></span>*Y*<br/> | \[在 \] 第二個向量中。<br/> |



 

## <a name="return-value"></a>傳回值

*X* 參數和 *y* 參數的點乘積。

## <a name="type-description"></a>類型描述



| Name  | [**範本類型**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**元件類型**](dx-graphics-hlsl-intrinsic-functions.md)                 | 大小                            |
|-------|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|---------------------------------|
| *x*   | [**向量**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)、 [ **int**](/windows/desktop/WinProg/windows-data-types) | 任意                             |
| *y*   | [**向量**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)、 [ **int**](/windows/desktop/WinProg/windows-data-types) |  (s 的相同維度) 為輸入 *x* |
| *Ret* | [**純量 (scalar)**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)、 [ **int**](/windows/desktop/WinProg/windows-data-types) | 1                               |



 

## <a name="minimum-shader-model"></a>最小著色器模型

下列著色器模型支援此函數。



| 著色器模型                                                                       | 支援 |
|------------------------------------------------------------------------------------|-----------|
| [著色器模型 2 (DIRECTX HLSL) ](dx-graphics-hlsl-sm2.md) 和更高的著色器模型 | 是       |
| [著色器模型 1 (DirectX HLSL) ](dx-graphics-hlsl-sm1.md)                          | 是       |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**(DirectX HLSL) 內建函式**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

