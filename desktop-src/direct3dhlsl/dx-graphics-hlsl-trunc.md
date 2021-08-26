---
title: 'trunc (Corecrt \_ math .h) '
description: 將浮點值截斷為整陣列件。
ms.assetid: a0978fa2-71f8-4257-8c90-96224c2ec953
keywords:
- trunc HLSL
topic_type:
- apiref
api_name:
- trunc
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0845e619e8674d729735da1b639802df256d9c210615d71578a4e1effd777e39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119845768"
---
# <a name="trunc"></a>trunc

將浮點值截斷為整陣列件。



| ret trunc (*x*)  |
|----------------|



 

## <a name="parameters"></a>參數



| 項目                                                   | 描述                            |
|--------------------------------------------------------|----------------------------------------|
| <span id="x"></span><span id="X"></span>*X*<br/> | \[在 \] 指定的輸入中。<br/> |



 

## <a name="return-value"></a>傳回值

輸入值已截斷為整陣列件。

## <a name="remarks"></a>備註

此函式會將浮點值截斷為整陣列件。 假設浮點值為1.6，trunc 函式會傳回1.0，其中的 [**round (DIRECTX HLSL)**](dx-graphics-hlsl-round.md) 函數會傳回2.0。

## <a name="type-description"></a>類型描述



| 名稱 | [**範本類型**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**元件類型**](dx-graphics-hlsl-intrinsic-functions.md) | 大小                         |
|------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|------------------------------|
| *x*  | 純 [**量、**](dx-graphics-hlsl-intrinsic-functions.md)**向量** 或 **矩陣** | [**浮動**](/windows/desktop/WinProg/windows-data-types)                        | 任意                          |
| Ret  | 與輸入 x 相同的類型                                                                                           | [**浮動**](/windows/desktop/WinProg/windows-data-types)                        | ) 為輸入 x 的相同維度 (s |



 

## <a name="minimum-shader-model"></a>最小著色器模型

下列著色器模型支援此函數。



| 著色器模型                                                                       | 支援 |
|------------------------------------------------------------------------------------|-----------|
| [著色器模型 1 (DIRECTX HLSL) ](dx-graphics-hlsl-sm1.md) 和更高的著色器模型 | 是       |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|--------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Corecrt \_ math。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**(DirectX HLSL) 內建函式**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

