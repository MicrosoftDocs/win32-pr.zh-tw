---
description: 定義必須針對光源計算存取色彩或色彩元件的位置。
ms.assetid: 76061d47-a31c-4008-aa8d-a0464dd3423f
title: 'D3DMATERIALCOLORSOURCE 列舉 (D3D9Types) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DMATERIALCOLORSOURCE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 8877eece8e33c6508768b22c989e992cf8178823
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106991477"
---
# <a name="d3dmaterialcolorsource-enumeration"></a>D3DMATERIALCOLORSOURCE 列舉

定義必須針對光源計算存取色彩或色彩元件的位置。

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DMATERIALCOLORSOURCE { 
  D3DMCS_MATERIAL     = 0,
  D3DMCS_COLOR1       = 1,
  D3DMCS_COLOR2       = 2,
  D3DMCS_FORCE_DWORD  = 0x7fffffff
} D3DMATERIALCOLORSOURCE, *LPD3DMATERIALCOLORSOURCE;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="D3DMCS_MATERIAL"></span><span id="d3dmcs_material"></span>**D3DMCS \_ 材質**
</dt> <dd>

使用目前材質的色彩。

</dd> <dt>

<span id="D3DMCS_COLOR1"></span><span id="d3dmcs_color1"></span>**D3DMCS \_ COLOR1**
</dt> <dd>

使用擴散頂點色彩。

</dd> <dt>

<span id="D3DMCS_COLOR2"></span><span id="d3dmcs_color2"></span>**D3DMCS \_ COLOR2**
</dt> <dd>

使用反射頂點色彩。

</dd> <dt>

<span id="D3DMCS_FORCE_DWORD"></span><span id="d3dmcs_force_dword"></span>**D3DMCS \_ 強制 \_ DWORD**
</dt> <dd>

強制此列舉的大小編譯為32位。 如果沒有這個值，某些編譯器會允許此列舉編譯成32位以外的大小。 不使用這個值。

</dd> </dl>

## <a name="remarks"></a>備註

這些旗標是用來設定 [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md) 列舉類型中下列轉譯狀態的值。

-   D3DRS \_ AMBIENTMATERIALSOURCE
-   D3DRS \_ DIFFUSEMATERIALSOURCE
-   D3DRS \_ EMISSIVEMATERIALSOURCE
-   D3DRS \_ SPECULARMATERIALSOURCE

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3D9Types。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Direct3D 列舉](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**D3DRENDERSTATETYPE**](./d3drenderstatetype.md)
</dt> </dl>

 

 
