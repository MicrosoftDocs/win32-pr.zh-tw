---
title: 行列 式
description: 傳回指定之浮點數、正方形矩陣的行列式。
ms.assetid: 9062b6f1-8518-4ee4-8d57-5aa9e2176d05
keywords:
- 行列式 HLSL
topic_type:
- apiref
api_name:
- determinant
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 75b17982560d70cf00cfb13832de9605b910f169d1461692f4c6a97274709e52
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119120303"
---
# <a name="determinant"></a>行列 式

傳回指定之浮點數、正方形矩陣的行列式。



| *ret* 行列式 (*m*)  |
|------------------------|



 

## <a name="parameters"></a>參數



| 項目                                                   | 描述                            |
|--------------------------------------------------------|----------------------------------------|
| <span id="m"></span><span id="M"></span>*m*<br/> | \[在 \] 指定的值中。<br/> |



 

## <a name="return-value"></a>傳回值

浮點數的純量值，表示 *m* 參數的行列式。

## <a name="type-description"></a>類型描述



| 名稱  | [**範本類型**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**元件類型**](dx-graphics-hlsl-intrinsic-functions.md) | 大小                                     |
|-------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------------------------------------------|
| *m*   | [**矩陣**](dx-graphics-hlsl-intrinsic-functions.md) | [**浮動**](/windows/desktop/WinProg/windows-data-types)                        | 任何 (的資料列數目 = 資料行數目)  |
| *Ret* | [**標量**](dx-graphics-hlsl-intrinsic-functions.md) | [**FLOAT**](/windows/desktop/WinProg/windows-data-types)                        | 1                                        |



 

## <a name="minimum-shader-model"></a>最小著色器模型

下列著色器模型支援此函數。



| 著色器模型                                                                       | 支援             |
|------------------------------------------------------------------------------------|-----------------------|
| [著色器模型 2 (DIRECTX HLSL) ](dx-graphics-hlsl-sm2.md) 和更高的著色器模型 | 是                   |
| [著色器模型 1 (DirectX HLSL) ](dx-graphics-hlsl-sm1.md)                          | vs \_ 1 \_ 1 和 ps \_ 1 \_ 4 |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**(DirectX HLSL) 內建函式**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

