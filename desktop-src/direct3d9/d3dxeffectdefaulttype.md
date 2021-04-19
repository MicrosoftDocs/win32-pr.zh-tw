---
description: 效果資料類型。 資料會包含在 D3DXEFFECTDEFAULT 的 pValue 成員中。
ms.assetid: d698ad6e-2ce2-48d6-90be-49bc08f172a9
title: 'D3DXEFFECTDEFAULTTYPE 列舉 (D3dx9mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXEFFECTDEFAULTTYPE
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: ffd31167d712a8270011c061cd6328aa9214352e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106992717"
---
# <a name="d3dxeffectdefaulttype-enumeration"></a>D3DXEFFECTDEFAULTTYPE 列舉

效果資料類型。 資料會包含在 [**D3DXEFFECTDEFAULT**](d3dxeffectdefault.md)的 pValue 成員中。

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DXEFFECTDEFAULTTYPE { 
  D3DXEDT_STRING      = 1,
  D3DXEDT_FLOATS      = 2,
  D3DXEDT_DWORD       = 3,
  D3DXEDT_FORCEDWORD  = 0x7fffffff
} D3DXEFFECTDEFAULTTYPE, *LPD3DXEFFECTDEFAULTTYPE;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="D3DXEDT_STRING"></span><span id="d3dxedt_string"></span>**D3DXEDT \_ 字串**
</dt> <dd>

資料型別是以 Null 結束的 ASCII 文字字串。

</dd> <dt>

<span id="D3DXEDT_FLOATS"></span><span id="d3dxedt_floats"></span>**D3DXEDT \_ 浮動**
</dt> <dd>

資料類型是 float 類型的陣列。 陣列中的 float 類型數目是由 [**D3DXEFFECTDEFAULT**](d3dxeffectdefault.md)中的 NumBytes 指定。

</dd> <dt>

<span id="D3DXEDT_DWORD"></span><span id="d3dxedt_dword"></span>**D3DXEDT \_ DWORD**
</dt> <dd>

資料類型是 DWORD。

</dd> <dt>

<span id="D3DXEDT_FORCEDWORD"></span><span id="d3dxedt_forcedword"></span>**D3DXEDT \_ FORCEDWORD**
</dt> <dd>

強制此列舉的大小編譯為32位。 如果沒有這個值，某些編譯器會允許此列舉編譯成32位以外的大小。 不使用這個值。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3dx9mesh。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 列舉](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




