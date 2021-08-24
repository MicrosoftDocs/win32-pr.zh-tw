---
title: D3DCOLORtoUBYTE4
description: 將 D3DCOLOR 所設定的浮點數、4D 向量轉換成 UBYTE4。
ms.assetid: 20a7be00-1e36-41c3-bc98-933b3faa8f35
keywords:
- D3DCOLORtoUBYTE4 HLSL
topic_type:
- apiref
api_name:
- D3DCOLORtoUBYTE4
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cea438b8c305c7ff76b6f9795c9f2c869a0f262f70e670d2e34c5b882de7c9c5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119789798"
---
# <a name="d3dcolortoubyte4"></a>D3DCOLORtoUBYTE4

將 D3DCOLOR 所設定的浮點數、4D 向量轉換成 UBYTE4。



| *ret* D3DCOLORtoUBYTE4 (*x*)  |
|-----------------------------|



 

此函式會 swizzles 和調整 *x* 參數的元件。 您可以使用此函式來彌補一些硬體中是否缺少 UBYTE4 支援。

## <a name="parameters"></a>參數



| 項目                                                   | 描述                                              |
|--------------------------------------------------------|----------------------------------------------------------|
| <span id="x"></span><span id="X"></span>*X*<br/> | \[\]要轉換的浮點數 vector4。<br/> |



 

## <a name="return-value"></a>傳回值

*X* 參數的 UBYTE4 標記法。

## <a name="type-description"></a>類型描述



| 名稱  | [**範本類型**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**元件類型**](dx-graphics-hlsl-intrinsic-functions.md) | 大小 |
|-------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| *x*   | [**向量**](dx-graphics-hlsl-intrinsic-functions.md) | [**浮動**](/windows/desktop/WinProg/windows-data-types)                        | 4    |
| *Ret* | [**向量**](dx-graphics-hlsl-intrinsic-functions.md) | [**整數**](/windows/desktop/WinProg/windows-data-types)                      | 4    |



 

## <a name="minimum-shader-model"></a>最小著色器模型

下列著色器模型支援此函數。



| 著色器模型                                                                       | 支援 |
|------------------------------------------------------------------------------------|-----------|
| [著色器模型 2 (DIRECTX HLSL) ](dx-graphics-hlsl-sm2.md) 和更高的著色器模型 | 是       |
| [著色器模型 1 (DirectX HLSL) ](dx-graphics-hlsl-sm1.md)                          | vs \_ 1 \_ 1  |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**(DirectX HLSL) 內建函式**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

