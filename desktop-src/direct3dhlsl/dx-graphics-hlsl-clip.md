---
title: clip
description: 如果指定的值小於零，則會捨棄目前的圖元。
ms.assetid: c9f84a27-5572-45aa-a12f-4446614b7be5
keywords:
- 剪輯 HLSL
topic_type:
- apiref
api_name:
- clip
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 92a75f2839dbbb605d976e07fffa5c2f9b27fd86
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104971732"
---
# <a name="clip"></a>clip

如果指定的值小於零，則會捨棄目前的圖元。



| 剪輯 (*x*)  |
|-----------|



 

## <a name="parameters"></a>參數



| 項目                                                   | 描述                            |
|--------------------------------------------------------|----------------------------------------|
| <span id="x"></span><span id="X"></span>*X*<br/> | \[在 \] 指定的值中。<br/> |



 

## <a name="return-value"></a>傳回值

無。

## <a name="remarks"></a>備註

如果 *x* 參數的每個元件都代表與平面之間的距離，請使用 **clip** HLSL 內建函式來模擬裁剪平面。

此外，使用 **剪輯** 函式來測試 Alpha 行為，如下列範例所示：


```
clip( Input.Color.A < 0.1f ? -1:1 );
```



## <a name="type-description"></a>類型描述



| Name | [**範本類型**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**元件類型**](dx-graphics-hlsl-intrinsic-functions.md) | 大小 |
|------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| *x*  | 純 [**量、**](dx-graphics-hlsl-intrinsic-functions.md)**向量** 或 **矩陣** | [**浮動**](/windows/desktop/WinProg/windows-data-types)                        | 任意  |



 

## <a name="minimum-shader-model"></a>最小著色器模型

下列著色器模型支援此函數。



| 著色器模型                                              | 支援               |
|-----------------------------------------------------------|-------------------------|
| [著色器模型4](dx-graphics-hlsl-sm4.md)                | 是 (只) 圖元著色器 |
| [著色器模型 3 (DirectX HLSL) ](dx-graphics-hlsl-sm3.md) | 是 (只) 圖元著色器 |
| [著色器模型 2 (DirectX HLSL) ](dx-graphics-hlsl-sm2.md) | 是 (只) 圖元著色器 |
| [著色器模型 1 (DirectX HLSL) ](dx-graphics-hlsl-sm1.md) | 是 (只) 圖元著色器 |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**(DirectX HLSL) 內建函式**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

