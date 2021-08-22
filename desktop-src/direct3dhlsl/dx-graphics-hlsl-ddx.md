---
title: ddx
description: 傳回指定值的部分導數（相對於螢幕空間 x 座標）。
ms.assetid: a21c2d2a-7c62-4dc6-8521-273690be1104
keywords:
- ddx HLSL
topic_type:
- apiref
api_name:
- ddx
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a60f2376af13e291ff0c59966bd50261cf2fd29ceb10d8ea26f621e257956ce0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119043816"
---
# <a name="ddx"></a>ddx

傳回指定值的部分導數（相對於螢幕空間 x 座標）。



| *ret* ddx (*x*)  |
|----------------|



 

此函數會計算相對於螢幕空間 x 座標的部分衍生。 若要計算與螢幕空間 y 座標相關的部分衍生，請使用 [**ddy**](dx-graphics-hlsl-ddy.md) 函數。

只有圖元著色器支援此函式。

## <a name="parameters"></a>參數



| 項目                                                   | 描述                            |
|--------------------------------------------------------|----------------------------------------|
| <span id="x"></span><span id="X"></span>*X*<br/> | \[在 \] 指定的值中。<br/> |



 

## <a name="return-value"></a>傳回值

*X* 參數的部分衍生。

## <a name="type-description"></a>類型描述



| 名稱  | [**範本類型**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**元件類型**](dx-graphics-hlsl-intrinsic-functions.md) | 大小                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *x*   | 純 [**量、**](dx-graphics-hlsl-intrinsic-functions.md)**向量** 或 **矩陣** | [**浮動**](/windows/desktop/WinProg/windows-data-types)                        | 任意                            |
| *Ret* | 與輸入 *x* 相同                                                                                              | [**浮動**](/windows/desktop/WinProg/windows-data-types)                        | ) 為輸入 *x* 的相同維度 (s |



 

## <a name="minimum-shader-model"></a>最小著色器模型

下列著色器模型支援此函數。



| 著色器模型                                                                | 支援                                 |
|-----------------------------------------------------------------------------|-------------------------------------------|
| [著色器模型 5](d3d11-graphics-reference-sm5.md) 和更新版本的著色器模型 | 是                                       |
| [著色器模型4](dx-graphics-hlsl-sm4.md)                                  | 是                                       |
| [著色器模型 3 (DirectX HLSL) ](dx-graphics-hlsl-sm3.md)                   | 是                                       |
| [著色器模型 2 (DirectX HLSL) ](dx-graphics-hlsl-sm2.md)                   | 是在 ps \_ 2 \_ x 中，不支援在 ps \_ 2 \_ 0 中。 |
| [著色器模型 1 (DirectX HLSL) ](dx-graphics-hlsl-sm1.md)                   | 否                                        |



 

下列著色器類型支援此函數：



| 頂點 | 船體 | 網域 | 幾何形狀 | 像素 | 計算 |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     |         |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**(DirectX HLSL) 內建函式**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

