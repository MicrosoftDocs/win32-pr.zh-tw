---
title: asfloat
description: 以浮點數的形式來解讀 x 的位模式。
ms.assetid: 48e1e0cb-8578-4e6d-8c46-2b8b201906c1
keywords:
- asfloat HLSL
topic_type:
- apiref
api_name:
- asfloat
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9a5701d959fb59519318dd7f2e91b6790f4c0b6e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104990990"
---
# <a name="asfloat"></a>asfloat

以浮點數的形式來解讀 *x* 的位模式。



| ret asfloat (*x*)  |
|------------------|



 

## <a name="parameters"></a>參數



| 項目                                                   | 描述                        |
|--------------------------------------------------------|------------------------------------|
| <span id="x"></span><span id="X"></span>*X*<br/> | \[在 \] 輸入值中。<br/> |



 

## <a name="return-value"></a>傳回值

解釋為浮點數的輸入。

## <a name="type-description"></a>類型描述



| Name  | [**範本類型**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**元件類型**](dx-graphics-hlsl-intrinsic-functions.md)                                                         | 大小                           |
|-------|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| *x*   | 純 [**量、**](dx-graphics-hlsl-intrinsic-functions.md)**向量** 或 **矩陣** | [**float**](/windows/desktop/WinProg/windows-data-types)、 [**int**](/windows/desktop/WinProg/windows-data-types)、 [**uint**](/windows/desktop/WinProg/windows-data-types) | 任意                            |
| *Ret* | 與輸入 *x* 相同                                                                                              | [**浮動**](/windows/desktop/WinProg/windows-data-types)                                                                                | ) 為輸入 *x* 的相同維度 (s |



 

## <a name="function-overloads"></a>函數多載

<dl> ' float <x> asfloat (float <x> 值) ; `  
`float <x> asfloat (int <x> 值) ; `  
`float <x> asfloat (uint <x> 值) ; '
</dl>

## <a name="minimum-shader-model"></a>最小著色器模型

下列著色器模型支援此函數。



| 著色器模型                                                        | 支援 |
|---------------------------------------------------------------------|-----------|
| [著色器模型 4](dx-graphics-hlsl-sm4.md) 和更高的著色器模型 | 是       |
| [著色器模型 3 (DirectX HLSL) ](dx-graphics-hlsl-sm3.md)           | 不可以        |
| [著色器模型 2 (DirectX HLSL) ](dx-graphics-hlsl-sm2.md)           | 不可以        |
| [著色器模型 1 (DirectX HLSL) ](dx-graphics-hlsl-sm1.md)           | 不可以        |



 

## <a name="remarks"></a>備註

舊版編譯器不正確地允許 `asfloat(bool)` ，但請注意，不支援 bool 輸入。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**(DirectX HLSL) 內建函式**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

