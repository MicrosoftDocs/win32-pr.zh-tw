---
description: 常數資料表中常數的描述。
ms.assetid: d1970536-7195-4270-a1b9-b082ebe4f17f
title: 'D3DXCONSTANT_DESC 結構 (D3dx9shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCONSTANT_DESC
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: d737fa1d95a119668602aeb056e15bc4248200aa
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106990024"
---
# <a name="d3dxconstant_desc-structure"></a>D3DXCONSTANT \_ DESC 結構

常數資料表中常數的描述。

## <a name="syntax"></a>語法


```C++
typedef struct D3DXCONSTANT_DESC {
  LPCSTR              Name;
  D3DXREGISTER_SET    RegisterSet;
  UINT                RegisterIndex;
  UINT                RegisterCount;
  D3DXPARAMETER_CLASS Class;
  D3DXPARAMETER_TYPE  Type;
  UINT                Rows;
  UINT                Columns;
  UINT                Elements;
  UINT                StructMembers;
  UINT                Bytes;
  LPCVOID             DefaultValue;
} D3DXCONSTANT_DESC, *LPD3DXCONSTANT_DESC;
```



## <a name="members"></a>成員

<dl> <dt>

**名稱**
</dt> <dd>

類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**

</dd> <dd>

常數的名稱。

</dd> <dt>

**RegisterSet**
</dt> <dd>

類型： **[ **D3DXREGISTER \_ 集**](./d3dxregister-set.md)**

</dd> <dd>

常數資料類型。 請參閱 [**D3DXREGISTER \_ SET**](./d3dxregister-set.md)。

</dd> <dt>

**RegisterIndex**
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

資料表中常數的以零為基底的索引。

</dd> <dt>

**RegisterCount**
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

包含資料的暫存器數目。

</dd> <dt>

**類別**
</dt> <dd>

Type： **[ **D3DXPARAMETER \_ 類別**](./d3dxparameter-class.md)**

</dd> <dd>

Parameter 類別。 請參閱 [**D3DXPARAMETER \_ 類別**](./d3dxparameter-class.md)。

</dd> <dt>

**型別**
</dt> <dd>

類型： **[ **D3DXPARAMETER \_ 類型**](./d3dxparameter-type.md)**

</dd> <dd>

參數類型。 請參閱 [**D3DXPARAMETER \_ 類型**](./d3dxparameter-type.md)。

</dd> <dt>

**資料列**
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

資料列數目。

</dd> <dt>

**資料行**
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

資料行數目。

</dd> <dt>

**元素**
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

陣列中的元素數目。

</dd> <dt>

**StructMembers**
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

結構成員子參數的數目。

</dd> <dt>

**Bytes**
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

資料大小（位元組數）。

</dd> <dt>

**DefaultValue**
</dt> <dd>

類型： **[ **LPCVOID**](../winprog/windows-data-types.md)**

</dd> <dd>

預設值的指標。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3dx9shader。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 結構](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[**D3DXCONSTANTTABLE \_ DESC**](d3dxconstanttable-desc.md)
</dt> </dl>

 

 
