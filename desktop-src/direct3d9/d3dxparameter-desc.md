---
description: 描述用於效果物件的參數。
ms.assetid: 60d19b52-67ef-4903-bbde-922a8fac1ad8
title: 'D3DXPARAMETER_DESC 結構 (D3dx9effect .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPARAMETER_DESC
api_type:
- HeaderDef
api_location:
- d3dx9effect.h
ms.openlocfilehash: a12541e9bfb33979b11f8198e218a3eb474f948aeb8c74982a5369eed782eaa3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119631148"
---
# <a name="d3dxparameter_desc-structure"></a>D3DXPARAMETER \_ DESC 結構

描述用於效果物件的參數。

## <a name="syntax"></a>語法


```C++
typedef struct D3DXPARAMETER_DESC {
  LPCSTR              Name;
  LPCSTR              Semantic;
  D3DXPARAMETER_CLASS Class;
  D3DXPARAMETER_TYPE  Type;
  UINT                Rows;
  UINT                Columns;
  UINT                Elements;
  UINT                Annotations;
  UINT                StructMembers;
  DWORD               Flags;
  UINT                Bytes;
} D3DXPARAMETER_DESC, *LPD3DXPARAMETER_DESC;
```



## <a name="members"></a>成員

<dl> <dt>

**名稱**
</dt> <dd>

類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**

</dd> <dd>

參數的名稱。

</dd> <dt>

**語義**
</dt> <dd>

類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**

</dd> <dd>

語義意義，也稱為使用方式。

</dd> <dt>

**類別**
</dt> <dd>

Type： **[ **D3DXPARAMETER \_ 類別**](./d3dxparameter-class.md)**

</dd> <dd>

Parameter 類別。 將此值設定為 [**D3DXPARAMETER \_ 類別**](./d3dxparameter-class.md)中的其中一個值。

</dd> <dt>

**類型**
</dt> <dd>

類型： **[ **D3DXPARAMETER \_ 類型**](./d3dxparameter-type.md)**

</dd> <dd>

參數類型。 將此值設定為 [ [**D3DXPARAMETER \_ 類型**](./d3dxparameter-type.md)] 中的其中一個值。

</dd> <dt>

**資料列**
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

陣列中的資料列數目。

</dd> <dt>

**資料行**
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

陣列中的資料行數目。

</dd> <dt>

**元素**
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

陣列中的元素數目。

</dd> <dt>

**註解**
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

注釋的數目。

</dd> <dt>

**StructMembers**
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

結構成員的數目。

</dd> <dt>

**旗標**
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

參數屬性。 請參閱 [效果常數](dx9-graphics-reference-effects-constants.md)。

</dd> <dt>

**Bytes**
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

參數的大小（以位元組為單位）。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3dx9effect。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[效果結構](dx9-graphics-reference-effects-structures.md)
</dt> </dl>

 

 
