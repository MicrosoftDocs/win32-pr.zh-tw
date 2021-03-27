---
title: 任意
description: 判斷指定值的任何元件是否為非零。
ms.assetid: 69a30478-662a-47de-babc-3cc67f89809c
keywords:
- 任何 HLSL
topic_type:
- apiref
api_name:
- any
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6bc5a908336f011973690bd3ca3d598583b0d32d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104971796"
---
# <a name="any"></a>任意

判斷指定值的任何元件是否為非零。



| *ret* 任何 (*x*)  |
|----------------|



 

## <a name="parameters"></a>參數



| 項目                                                   | 描述                            |
|--------------------------------------------------------|----------------------------------------|
| <span id="x"></span><span id="X"></span>*X*<br/> | \[在 \] 指定的值中。<br/> |



 

## <a name="return-value"></a>傳回值

如果 *x* 參數的任何元件為非零，則 **為 True** ;否則 **為 false**。

## <a name="remarks"></a>備註

此函數類似于 [**all**](dx-graphics-hlsl-all.md) HLSL 內建函式。 **Any** 函式會判斷指定值的任何元件是否為非零，而 **all** 函數會判斷指定值的所有元件是否為非零。

## <a name="type-description"></a>類型描述



| Name  | [**範本類型**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**元件類型**](dx-graphics-hlsl-intrinsic-functions.md)                                                         | 大小 |
|-------|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|------|
| *x*   | 純 [**量、**](dx-graphics-hlsl-intrinsic-functions.md)**向量** 或 **矩陣** | [**float**](/windows/desktop/WinProg/windows-data-types)、 [**int**](/windows/desktop/WinProg/windows-data-types)、 [**bool**](/windows/desktop/WinProg/windows-data-types) | 任意  |
| *Ret* | [**純量 (scalar)**](dx-graphics-hlsl-intrinsic-functions.md)                            | [**bool**](/windows/desktop/WinProg/windows-data-types)                                                                                 | 1    |



 

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

 

