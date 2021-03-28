---
title: sin
description: 傳回指定之值的正弦。
ms.assetid: e1c3ead8-73dd-4798-8553-1a42dbaefe8e
keywords:
- sin HLSL
topic_type:
- apiref
api_name:
- sin
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d48332d35052a893dcb348a70e4d464a6bbfe0c9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382553"
---
# <a name="sin"></a>sin

傳回指定之值的正弦。



| *ret* sin (*x*)  |
|----------------|



 

## <a name="parameters"></a>參數



| 項目                                                   | 描述                                        |
|--------------------------------------------------------|----------------------------------------------------|
| <span id="x"></span><span id="X"></span>*X*<br/> | \[在 \] 指定的值中，以弧度為單位。<br/> |



 

## <a name="return-value"></a>傳回值

*X* 參數的正弦。

## <a name="type-description"></a>類型描述



| Name  | [**範本類型**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**元件類型**](dx-graphics-hlsl-intrinsic-functions.md) | 大小                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *x*   | 純 [**量、**](dx-graphics-hlsl-intrinsic-functions.md)**向量** 或 **矩陣** | [**浮動**](/windows/desktop/WinProg/windows-data-types)                        | 任意                            |
| *Ret* | 與輸入 *x* 相同                                                                                              | [**浮動**](/windows/desktop/WinProg/windows-data-types)                        | ) 為輸入 *x* 的相同維度 (s |



 

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

 

