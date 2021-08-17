---
title: 雜訊
description: 使用 Perlin 雜訊演算法產生隨機值。
ms.assetid: 0188a7f3-9955-4e1c-9370-ef1d8aff3765
keywords:
- 雜訊 HLSL
topic_type:
- apiref
api_name:
- noise
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5eb93d32e7730b6840700bba9dc5a629bf3180f83673581f8589a254d467cff8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119120102"
---
# <a name="noise"></a>雜訊

使用 Perlin 雜訊演算法產生隨機值。




| *ret* 雜訊 (*x*)  |
|------------------|



 

## <a name="parameters"></a>參數



| 項目                                                   | 描述                                                                    |
|--------------------------------------------------------|--------------------------------------------------------------------------------|
| <span id="x"></span><span id="X"></span>*X*<br/> | \[在 \] 要產生 Perlin 雜訊的浮點向量中。<br/> |



 

## <a name="return-value"></a>傳回值

介於-1 和1之間範圍內的 Perlin 雜訊值。

## <a name="remarks"></a>備註

Perlin 雜訊值會從某個點順暢地變更為另一個點，以建立自然查看、隨機產生的值。 您可以使用 Perlin 雜訊來產生像是冒煙和火災等效果的程式紋理。

## <a name="type-description"></a>類型描述



| 名稱  | [**範本類型**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**元件類型**](dx-graphics-hlsl-intrinsic-functions.md) | 大小 |
|-------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| *x*   | [**向量**](dx-graphics-hlsl-intrinsic-functions.md) | [**浮動**](/windows/desktop/WinProg/windows-data-types)                        | 任意  |
| *Ret* | [**標量**](dx-graphics-hlsl-intrinsic-functions.md) | [**FLOAT**](/windows/desktop/WinProg/windows-data-types)                        | 1    |



 

## <a name="minimum-shader-model"></a>最小著色器模型

下列著色器模型支援此函數。



| 著色器模型                                                                       | 支援           |
|------------------------------------------------------------------------------------|---------------------|
| [著色器模型 2 (DIRECTX HLSL) ](dx-graphics-hlsl-sm2.md) 和更高的著色器模型 | 否                  |
| [著色器模型 1 (DirectX HLSL) ](dx-graphics-hlsl-sm1.md)                          | 是 (tx \_ 1 \_ 0 僅)  |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**(DirectX HLSL) 內建函式**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

