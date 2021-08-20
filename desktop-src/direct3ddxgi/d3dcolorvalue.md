---
description: D3DCOLORVALUE 結構 (Dxgitype) -表示使用 Alpha 的色彩值，用於透明度。
ms.assetid: 27A86A10-FC0E-421E-BEA7-2DEB539849BB
title: 'D3DCOLORVALUE 結構 (Dxgitype .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOLORVALUE
api_type:
- HeaderDef
api_location:
- dxgitype.h
ms.openlocfilehash: ba2e4731e1fd308c3b87cb5d1856020e5471f5fe0eac8f8cc99de3e3f32ded5e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117910034"
---
# <a name="d3dcolorvalue-structure-dxgitypeh"></a>D3DCOLORVALUE 結構 (Dxgitype .h) 

表示使用 Alpha 的色彩值，用於透明度。

## <a name="syntax"></a>語法


```C++
typedef struct _D3DCOLORVALUE {
  float r;
  float g;
  float b;
  float a;
} D3DCOLORVALUE;
```



## <a name="members"></a>成員

<dl> <dt>

**r**
</dt> <dd>

指定色彩之紅色元件的浮點值。 此值通常在0.0 到1.0 的範圍內。 值為0.0 表示完全沒有紅色的元件，而值1.0 則表示完全有紅色。

</dd> <dt>

**G**
</dt> <dd>

指定色彩之綠色元件的浮點值。 此值通常在0.0 到1.0 的範圍內。 值為0.0 表示完全沒有綠色的元件，而值1.0 表示綠色已完全存在。

</dd> <dt>

**b**
</dt> <dd>

指定色彩之藍色元件的浮點值。 此值通常在0.0 到1.0 的範圍內。 值為0.0 表示完全沒有藍色的元件，而值1.0 則表示藍色已完全存在。

</dd> <dt>

**的**
</dt> <dd>

指定色彩之 Alpha 元件的浮點值。 此值通常在0.0 到1.0 的範圍內。 值為0.0 表示完全透明，而值1.0 則表示完全不透明。

</dd> </dl>

## <a name="remarks"></a>備註

您可以將此結構的成員設定為0到1範圍以外的值，以實行一些不尋常的效果。 大於1的值會產生傾向于將場景沖蝕的強大燈。 負數值會產生深亮燈，以實際從場景中移除光線。

DXGItype 標頭類型-將 [**DXGI \_ RGBA**](dxgi-rgba.md) 定義為 **D3DCOLORVALUE** 的別名，如下所示：


```
typedef D3DCOLORVALUE DXGI_RGBA;
```



您可以使用 D3DCOLORVALUE 或 [**dxgi \_ RGBA**](dxgi-rgba.md) 搭配 [**IDXGISwapChain1：： SetBackgroundColor**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-setbackgroundcolor)、 [**IDXGISwapChain1：： GetBackgroundColor**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-getbackgroundcolor)和 [**DXGI \_ ALPHA \_ 模式**](/windows/desktop/api/DXGI1_2/ne-dxgi1_2-dxgi_alpha_mode)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Dxgitype。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[DXGI 結構](d3d10-graphics-reference-dxgi-structures.md)
</dt> <dt>

[**DXGI \_ RGBA**](dxgi-rgba.md)
</dt> </dl>

 

 




