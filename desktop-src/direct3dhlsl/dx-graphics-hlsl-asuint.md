---
title: asuint
description: 以不帶正負號的整數來解讀 x 的位模式。
ms.assetid: 8401001d-f9ee-43da-9756-f311e9f2bb20
keywords:
- asuint HLSL
topic_type:
- apiref
api_name:
- asuint
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1a2d351eb36c6910790e2dceb94e3a97951ad850
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104971772"
---
# <a name="asuint"></a>asuint

以不帶正負號的整數來解讀 *x* 的位模式。



| ret asuint (*x*)  |
|-----------------|



 

## <a name="parameters"></a>參數



| 項目                                                   | 描述                        |
|--------------------------------------------------------|------------------------------------|
| <span id="x"></span><span id="X"></span>*X*<br/> | \[在 \] 輸入值中。<br/> |



 

## <a name="return-value"></a>傳回值

轉譯為不帶正負號整數的輸入。

## <a name="type-description"></a>類型描述



| Name  | [**範本類型**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**元件類型**](dx-graphics-hlsl-intrinsic-functions.md)                 | 大小                           |
|-------|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|--------------------------------|
| *x*   | 純 [**量、**](dx-graphics-hlsl-intrinsic-functions.md)**向量** 或 **矩陣** | [**float**](/windows/desktop/WinProg/windows-data-types)、 [ **int**](/windows/desktop/WinProg/windows-data-types) | 任意                            |
| *Ret* | 與輸入 *x* 相同                                                                                              | [**uint**](/windows/desktop/WinProg/windows-data-types)                                         | ) 為輸入 *x* 的相同維度 (s |



 

## <a name="minimum-shader-model"></a>最小著色器模型

下列著色器模型支援此函數。



| 著色器模型                                                        | 支援 |
|---------------------------------------------------------------------|-----------|
| [著色器模型 4](dx-graphics-hlsl-sm4.md) 和更高的著色器模型 | 是       |
| [著色器模型 3 (DirectX HLSL) ](dx-graphics-hlsl-sm3.md)           | 不可以        |
| [著色器模型 2 (DirectX HLSL) ](dx-graphics-hlsl-sm2.md)           | 不可以        |
| [著色器模型 1 (DirectX HLSL) ](dx-graphics-hlsl-sm1.md)           | 不可以        |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**(DirectX HLSL) 內建函式**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

