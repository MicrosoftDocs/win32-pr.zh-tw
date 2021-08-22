---
description: 定義常數，以描述支援的陰影模式。
ms.assetid: ba4e0c62-b496-427b-a324-2fb560d153ba
title: 'D3DSHADEMODE 列舉 (D3d9types) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DSHADEMODE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 6a8c937000912eb203986bed4889785b9484afec7682418aed43fcc58c438e58
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119241558"
---
# <a name="d3dshademode-enumeration"></a>D3DSHADEMODE 列舉

定義常數，以描述支援的陰影模式。

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DSHADEMODE { 
  D3DSHADE_FLAT         = 1,
  D3DSHADE_GOURAUD      = 2,
  D3DSHADE_PHONG        = 3,
  D3DSHADE_FORCE_DWORD  = 0x7fffffff
} D3DSHADEMODE, *LPD3DSHADEMODE;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="D3DSHADE_FLAT"></span><span id="d3dshade_flat"></span>**D3DSHADE \_ 平面**
</dt> <dd>

平面陰影模式。 三角形中第一個頂點的色彩和反射元件是用來判斷臉部的色彩和反射元件。 這些色彩在三角形中保持不變;也就是說，它們不是插補。 反射 Alpha 是插補。 請參閱＜備註＞。

</dd> <dt>

<span id="D3DSHADE_GOURAUD"></span><span id="d3dshade_gouraud"></span>**D3DSHADE \_ GOURAUD**
</dt> <dd>

Gouraud 網底模式。 臉部的色彩和反射元件是由三角形的所有頂點之間的線性插補所決定。

</dd> <dt>

<span id="D3DSHADE_PHONG"></span><span id="d3dshade_phong"></span>**D3DSHADE \_ PHONG**
</dt> <dd>

不支援。

</dd> <dt>

<span id="D3DSHADE_FORCE_DWORD"></span><span id="d3dshade_force_dword"></span>**D3DSHADE \_ 強制 \_ DWORD**
</dt> <dd>

強制此列舉的大小編譯為32位。 如果沒有這個值，某些編譯器會允許此列舉編譯成32位以外的大小。 不使用這個值。

</dd> </dl>

## <a name="remarks"></a>備註

一般陰影模式之三角形的第一個頂點會以下列方式定義。

-   若為三角形清單，則為三角形的第一個頂點 i \* 3。
-   若為三角形帶，則三角形的第一個頂點是頂點 i。
-   若為三角形風扇，則三角形的第一個頂點是頂點 i + 1。

此列舉類型的成員會定義 D3DRS SHADEMODE 轉譯狀態的數值 \_ 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3d9types。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Direct3D 列舉](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**D3DRENDERSTATETYPE**](./d3drenderstatetype.md)
</dt> </dl>

 

 
