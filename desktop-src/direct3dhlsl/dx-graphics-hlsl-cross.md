---
title: 交叉
description: 傳回兩個浮點數3D 向量的交叉乘積。
ms.assetid: 5f1832af-6bc5-49a7-956a-fd762f674f5f
keywords:
- 跨 HLSL
topic_type:
- apiref
api_name:
- cross
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 91959bf415c3e56edf370942de268523bf998743
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104991014"
---
# <a name="cross"></a>交叉

傳回兩個浮點數3D 向量的交叉乘積。



| *ret* cross (*x*， *y*)  |
|-----------------------|



 

## <a name="parameters"></a>參數



| 項目                                                   | 描述                                             |
|--------------------------------------------------------|---------------------------------------------------------|
| <span id="x"></span><span id="X"></span>*X*<br/> | \[在 \] 第一個浮點的3d 向量中。<br/>  |
| <span id="y"></span><span id="Y"></span>*Y*<br/> | \[在 \] 第二個浮點數的立體向量中。<br/> |



 

## <a name="return-value"></a>傳回值

*X* 參數和 *y* 參數的交叉乘積。

## <a name="type-description"></a>類型描述



| Name  | [**範本類型**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**元件類型**](dx-graphics-hlsl-intrinsic-functions.md) | 大小 |
|-------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| *x*   | [**向量**](dx-graphics-hlsl-intrinsic-functions.md) | [**浮動**](/windows/desktop/WinProg/windows-data-types)                        | 3    |
| *y*   | [**向量**](dx-graphics-hlsl-intrinsic-functions.md) | [**浮動**](/windows/desktop/WinProg/windows-data-types)                        | 3    |
| *Ret* | [**向量**](dx-graphics-hlsl-intrinsic-functions.md) | [**浮動**](/windows/desktop/WinProg/windows-data-types)                        | 3    |



 

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

 

