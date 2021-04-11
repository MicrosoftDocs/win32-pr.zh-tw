---
description: D3DXSHADER \_ CONSTANTINFO 結構
ms.assetid: 0c42cea7-559e-4475-b66a-e932a9cb42de
title: 'D3DXSHADER_CONSTANTINFO 結構 (D3dx9shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHADER_CONSTANTINFO
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: e90c0085035e78b9bc3ce1c48642157d8badc924
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196240"
---
# <a name="d3dxshader_constantinfo-structure"></a>D3DXSHADER \_ CONSTANTINFO 結構

## <a name="syntax"></a>語法


```C++
typedef struct D3DXSHADER_CONSTANTINFO {
  DWORD Name;
  WORD  RegisterSet;
  WORD  RegisterIndex;
  WORD  RegisterCount;
  WORD  Reserved;
  DWORD TypeInfo;
  DWORD DefaultValue;
} D3DXSHADER_CONSTANTINFO, *LPD3DXSHADER_CONSTANTINFO;
```



## <a name="members"></a>成員

<dl> <dt>

**名稱**
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

從這個結構開頭算起的位移（以位元組為單位），指向包含常數資訊的字串。

</dd> <dt>

**RegisterSet**
</dt> <dd>

類型： **[ **WORD**](../winprog/windows-data-types.md)**

</dd> <dd>

註冊集。 請參閱 [**D3DXREGISTER \_ SET**](./d3dxregister-set.md)。

</dd> <dt>

**RegisterIndex**
</dt> <dd>

類型： **[ **WORD**](../winprog/windows-data-types.md)**

</dd> <dd>

註冊索引。

</dd> <dt>

**RegisterCount**
</dt> <dd>

類型： **[ **WORD**](../winprog/windows-data-types.md)**

</dd> <dd>

註冊數目。

</dd> <dt>

**已保留**
</dt> <dd>

類型： **[ **WORD**](../winprog/windows-data-types.md)**

</dd> <dd>

保留的。

</dd> <dt>

**TypeInfo**
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

從這個結構開頭算起的位移（以位元組為單位），指向包含 [**D3DXSHADER \_ TYPEINFO**](d3dxshader-typeinfo.md) 資訊的字串。

</dd> <dt>

**DefaultValue**
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

從這個結構開頭算起的位移（以位元組為單位），指向包含預設值的字串。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3dx9shader。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 結構](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
