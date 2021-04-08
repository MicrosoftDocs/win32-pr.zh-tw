---
description: 表示使用 Alpha 的色彩值，用於透明度。
ms.assetid: 5F9DDDC1-644E-4DA2-8E3D-F157789809E7
title: 'DXGI_RGBA 結構 (DXGItype .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DXGI_RGBA
api_type:
- HeaderDef
api_location:
- DXGItype.h
ms.openlocfilehash: 77b526e916d43868304c6c01a7dbbe8ebbb5692b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103688060"
---
# <a name="dxgi_rgba-structure"></a>DXGI \_ RGBA 結構

表示使用 Alpha 的色彩值，用於透明度。

## <a name="syntax"></a>語法


```C++
typedef struct _DXGI_RGBA {
  float r;
  float g;
  float b;
  float a;
} DXGI_RGBA;
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

DXGItype 標頭類型-將 **DXGI \_ RGBA** 定義為 [**D3DCOLORVALUE**](d3dcolorvalue.md)的別名，如下所示：


```
typedef D3DCOLORVALUE DXGI_RGBA;
```



您可以使用 **dxgi \_ RGBA** 搭配 [**IDXGISwapChain1：： SetBackgroundColor**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-setbackgroundcolor)、 [**IDXGISwapChain1：： GetBackgroundColor**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-getbackgroundcolor)和 [**dxgi \_ ALPHA \_ 模式**](/windows/desktop/api/DXGI1_2/ne-dxgi1_2-dxgi_alpha_mode)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 適用于 Windows 7 \[ desktop app \| UWP 應用程式的 Windows 8 和平臺更新\]<br/>                        |
| 最低支援的伺服器<br/> | Windows server 2012 和 Windows Server 2008 R2 \[ desktop apps \| UWP 應用程式的平臺更新\]<br/> |
| 標頭<br/>                   | <dl> <dt>DXGItype。h</dt> </dl>                      |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[DXGI 結構](d3d10-graphics-reference-dxgi-structures.md)
</dt> <dt>

[**D3DCOLORVALUE**](d3dcolorvalue.md)
</dt> <dt>

[**Direct3D 9 中的 D3DCOLORVALUE ()**](../direct3d9/d3dcolorvalue.md)
</dt> </dl>

 

 
