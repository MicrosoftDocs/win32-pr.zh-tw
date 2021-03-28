---
title: 'D3DX11_CHANNEL_FLAG 列舉 (D3DX11tex .h) '
description: 請注意，D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。 這些旗標會由函式使用，這些函式會在材質中的一或多個通道上運作。
ms.assetid: 058a0a1e-3c1b-4397-a41a-2e47d878cd92
keywords:
- D3DX11_CHANNEL_FLAG 列舉 Direct3D 11
- LPD3DX11_CHANNEL_FLAG 列舉指標 Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_CHANNEL_FLAG
api_location:
- D3DX11tex.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2e3097552637ce96663671dda443684ebda2b65
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104386522"
---
# <a name="d3dx11_channel_flag-enumeration"></a>D3DX11 \_ 通道 \_ 旗標列舉

> [!Note]  
> D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。

 

這些旗標會由函式使用，這些函式會在材質中的一或多個通道上運作。

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DX11_CHANNEL_FLAG { 
  D3DX11_CHANNEL_RED        = (1 << 0),
  D3DX11_CHANNEL_BLUE       = (1 << 1),
  D3DX11_CHANNEL_GREEN      = (1 << 2),
  D3DX11_CHANNEL_ALPHA      = (1 << 3),
  D3DX11_CHANNEL_LUMINANCE  = (1 << 4)
} D3DX11_CHANNEL_FLAG, *LPD3DX11_CHANNEL_FLAG;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="D3DX11_CHANNEL_RED"></span><span id="d3dx11_channel_red"></span>**D3DX11 \_ 頻道 \_ 紅色**
</dt> <dd>

表示應該使用紅色通道。

</dd> <dt>

<span id="D3DX11_CHANNEL_BLUE"></span><span id="d3dx11_channel_blue"></span>**D3DX11 \_ CHANNEL \_ BLUE**
</dt> <dd>

表示應該使用藍色通道。

</dd> <dt>

<span id="D3DX11_CHANNEL_GREEN"></span><span id="d3dx11_channel_green"></span>**D3DX11 \_ CHANNEL \_ 綠**
</dt> <dd>

表示應該使用綠色通道。

</dd> <dt>

<span id="D3DX11_CHANNEL_ALPHA"></span><span id="d3dx11_channel_alpha"></span>**D3DX11 \_ 頻道 \_ ALPHA**
</dt> <dd>

表示應該使用 Alpha 色板。

</dd> <dt>

<span id="D3DX11_CHANNEL_LUMINANCE"></span><span id="d3dx11_channel_luminance"></span>**D3DX11 \_ 通道 \_ 亮度**
</dt> <dd>

指出應該使用紅色、綠色和藍色通道的 luminaces。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3DX11tex。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 列舉](d3d11-graphics-reference-d3dx11-enums.md)
</dt> </dl>

 

 





