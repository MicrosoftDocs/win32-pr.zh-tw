---
title: 'isfinite (Corecrt \_ math .h) '
description: 判斷指定的浮點值是否為有限。
ms.assetid: 8be10499-2d06-4520-9697-dab2f461bd0d
keywords:
- isfinite HLSL
topic_type:
- apiref
api_name:
- isfinite
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f63c943dadccad9f485668948f366698f3bce5e6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104992190"
---
# <a name="isfinite"></a>isfinite

判斷指定的浮點值是否為有限。



| *ret* isfinite (*x*)  |
|---------------------|



 

## <a name="parameters"></a>參數



| 項目                                                   | 描述                            |
|--------------------------------------------------------|----------------------------------------|
| <span id="x"></span><span id="X"></span>*X*<br/> | \[在 \] 指定的值中。<br/> |



 

## <a name="return-value"></a>傳回值

傳回與輸入相同大小的值，如果 *x* 參數是有限的，則值設定為 **True** 。否則 **為 False**。

## <a name="type-description"></a>類型描述



| Name  | [**範本類型**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**元件類型**](dx-graphics-hlsl-intrinsic-functions.md) | 大小     |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|----------|
| *x*   | 純 [**量、**](dx-graphics-hlsl-intrinsic-functions.md)**向量** 或 **矩陣** | [**浮動**](/windows/desktop/WinProg/windows-data-types)                        | 任意      |
| *Ret* | 純 [**量、**](dx-graphics-hlsl-intrinsic-functions.md)**向量** 或 **矩陣** | [**bool**](/windows/desktop/WinProg/windows-data-types)                         | 作為輸入 |



 

## <a name="minimum-shader-model"></a>最小著色器模型

下列著色器模型支援此函數。



| 著色器模型                                                                       | 支援           |
|------------------------------------------------------------------------------------|---------------------|
| [著色器模型 2 (DIRECTX HLSL) ](dx-graphics-hlsl-sm2.md) 和更高的著色器模型 | 是                 |
| [著色器模型 1 (DirectX HLSL) ](dx-graphics-hlsl-sm1.md)                          | 是 (\_ \_ 只有) 的 vs 1 |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|--------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Corecrt \_ math。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**(DirectX HLSL) 內建函式**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

