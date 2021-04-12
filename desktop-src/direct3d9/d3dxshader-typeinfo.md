---
description: 包含成員類型資訊的 helper 結構。
ms.assetid: 5580122d-c700-4632-8fcf-903519f2429e
title: 'D3DXSHADER_TYPEINFO 結構 (D3dx9shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHADER_TYPEINFO
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: 71b9cc893cdcfdc9802aca173627cd9da4f9ca4b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322863"
---
# <a name="d3dxshader_typeinfo-structure"></a>D3DXSHADER \_ TYPEINFO 結構

包含成員類型資訊的 helper 結構。

## <a name="syntax"></a>語法


```C++
typedef struct D3DXSHADER_TYPEINFO {
  WORD  Class;
  WORD  Type;
  WORD  Rows;
  WORD  Columns;
  WORD  Elements;
  WORD  StructMembers;
  DWORD StructMemberInfo;
} D3DXSHADER_TYPEINFO, *LPD3DXSHADER_TYPEINFO;
```



## <a name="members"></a>成員

<dl> <dt>

**類別**
</dt> <dd>

類型： **[ **WORD**](../winprog/windows-data-types.md)**

</dd> <dd>

著色器物件類型。 請參閱 [**D3DXPARAMETER \_ 類別**](./d3dxparameter-class.md)。

</dd> <dt>

**型別**
</dt> <dd>

類型： **[ **WORD**](../winprog/windows-data-types.md)**

</dd> <dd>

資料類型。 請參閱 [**D3DXPARAMETER \_ 類型**](./d3dxparameter-type.md)。

</dd> <dt>

**資料列**
</dt> <dd>

類型： **[ **WORD**](../winprog/windows-data-types.md)**

</dd> <dd>

 (矩陣) 的矩陣資料列數目。

</dd> <dt>

**資料行**
</dt> <dd>

類型： **[ **WORD**](../winprog/windows-data-types.md)**

</dd> <dd>

 (向量和矩陣) 的資料行數目。

</dd> <dt>

**元素**
</dt> <dd>

類型： **[ **WORD**](../winprog/windows-data-types.md)**

</dd> <dd>

陣列維度。

</dd> <dt>

**StructMembers**
</dt> <dd>

類型： **[ **WORD**](../winprog/windows-data-types.md)**

</dd> <dd>

結構成員的數目。

</dd> <dt>

**StructMemberInfo**
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

結構成員資訊的陣列，D3DXSHADER \_ STRUCTMEMBERINFO \[ *StructMembers* \] 。 請參閱 [**D3DXSHADER \_ STRUCTMEMBERINFO**](d3dxshader-structmemberinfo.md)。

</dd> </dl>

## <a name="remarks"></a>備註

類型資訊是 [**D3DXSHADER \_ STRUCTMEMBERINFO**](d3dxshader-structmemberinfo.md)的一部分。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3dx9shader。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 結構](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[**D3DXSHADER \_ CONSTANTINFO**](d3dxshader-constantinfo.md)
</dt> </dl>

 

 
