---
title: 折射
description: 使用輸入光線、表面標準和折射索引，傳回折射向量。
ms.assetid: 9f9467d7-dd9b-472a-bbdc-752394d382c6
keywords:
- refract HLSL
topic_type:
- apiref
api_name:
- refract
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9e499d078a020ade1ff9ff2566c3fd15b2a820d2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104991007"
---
# <a name="refract"></a>折射

使用輸入光線、表面標準和折射索引，傳回折射向量。



| *ret* refract (*i*， *n*，？ )  |
|----------------------------|



 

## <a name="parameters"></a>參數



| 項目                                                   | 描述                                                  |
|--------------------------------------------------------|--------------------------------------------------------------|
| <span id="i"></span><span id="I"></span>*我*<br/> | \[在 \] 浮點的光線方向向量中。<br/>    |
| <span id="n"></span><span id="N"></span>*n-1*<br/> | \[在 \] 浮點的表面標準向量中。<br/>   |
| *?*<br/>                                         | \[\]浮點數中的折射索引純量。<br/> |



 

## <a name="return-value"></a>傳回值

浮點數折射向量。 如果輸入光線 i 和表面標準 n 之間的角度太適合指定的折射索引，則傳回值會是 (0，0，0) 。

## <a name="type-description"></a>類型描述



| Name              | [**範本類型**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**元件類型**](dx-graphics-hlsl-intrinsic-functions.md) | 大小                           |
|-------------------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *i*               | [**向量**](dx-graphics-hlsl-intrinsic-functions.md) | [**浮動**](/windows/desktop/WinProg/windows-data-types)                        | 任意                            |
| *n*               | [**向量**](dx-graphics-hlsl-intrinsic-functions.md) | [**浮動**](/windows/desktop/WinProg/windows-data-types)                        | 相同維度 (s) 為輸入 *i* |
| ?                 | [**純量 (scalar)**](dx-graphics-hlsl-intrinsic-functions.md) | [**FLOAT**](/windows/desktop/WinProg/windows-data-types)                        | 1                              |
| 折射向量 | [**向量**](dx-graphics-hlsl-intrinsic-functions.md) | [**浮動**](/windows/desktop/WinProg/windows-data-types)                        | 相同維度 (s) 為輸入 *i* |



 

## <a name="minimum-shader-model"></a>最小著色器模型

下列著色器模型支援此函數。



| 著色器模型                                                                       | 支援           |
|------------------------------------------------------------------------------------|---------------------|
| [著色器模型 2 (DIRECTX HLSL) ](dx-graphics-hlsl-sm2.md) 和更高的著色器模型 | 是                 |
| [著色器模型 1 (DirectX HLSL) ](dx-graphics-hlsl-sm1.md)                          | 是 (\_ \_ 只有) 的 vs 1 |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**(DirectX HLSL) 內建函式**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

