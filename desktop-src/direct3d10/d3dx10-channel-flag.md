---
description: 這些旗標會由函式使用，這些函式會在材質中的一或多個通道上運作。
ms.assetid: 54ecb39a-a36e-43bb-bb51-78b7375716d8
title: 'D3DX10_CHANNEL_FLAG 列舉 (D3DX10Tex .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_CHANNEL_FLAG
api_type:
- HeaderDef
api_location:
- D3DX10Tex.h
ms.openlocfilehash: 4b29cbb958b2aa8af02000fc62d4d3a848c2efba585bd927674c9ceca9d65d9e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119634958"
---
# <a name="d3dx10_channel_flag-enumeration"></a>D3DX10 \_ 通道 \_ 旗標列舉

這些旗標會由函式使用，這些函式會在材質中的一或多個通道上運作。

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DX10_CHANNEL_FLAG { 
  D3DX10_CHANNEL_RED        = (1 << 0),
  D3DX10_CHANNEL_BLUE       = (1 << 1),
  D3DX10_CHANNEL_GREEN      = (1 << 2),
  D3DX10_CHANNEL_ALPHA      = (1 << 3),
  D3DX10_CHANNEL_LUMINANCE  = (1 << 4)
} D3DX10_CHANNEL_FLAG, *LPD3DX10_CHANNEL_FLAG;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="D3DX10_CHANNEL_RED"></span><span id="d3dx10_channel_red"></span>**D3DX10 \_ 頻道 \_ 紅色**
</dt> <dd>

表示應該使用紅色通道。

</dd> <dt>

<span id="D3DX10_CHANNEL_BLUE"></span><span id="d3dx10_channel_blue"></span>**D3DX10 \_ CHANNEL \_ BLUE**
</dt> <dd>

表示應該使用藍色通道。

</dd> <dt>

<span id="D3DX10_CHANNEL_GREEN"></span><span id="d3dx10_channel_green"></span>**D3DX10 \_ CHANNEL \_ 綠**
</dt> <dd>

表示應該使用綠色通道。

</dd> <dt>

<span id="D3DX10_CHANNEL_ALPHA"></span><span id="d3dx10_channel_alpha"></span>**D3DX10 \_ 頻道 \_ ALPHA**
</dt> <dd>

表示應該使用 Alpha 色板。

</dd> <dt>

<span id="D3DX10_CHANNEL_LUMINANCE"></span><span id="d3dx10_channel_luminance"></span>**D3DX10 \_ 通道 \_ 亮度**
</dt> <dd>

指出應該使用紅色、綠色和藍色通道的 luminaces。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3DX10Tex。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 列舉](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 




