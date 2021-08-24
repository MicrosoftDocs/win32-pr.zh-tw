---
description: 常數資料表的描述。
ms.assetid: 848b328a-95a4-4fd0-a7d4-4fb0e5d14f64
title: 'D3DXCONSTANTTABLE_DESC 結構 (D3dx9shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCONSTANTTABLE_DESC
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: 9fb881ce0871165d9df394bf8a76326b4f5d644692217b1bb901438b90cf7cef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894058"
---
# <a name="d3dxconstanttable_desc-structure"></a>D3DXCONSTANTTABLE \_ DESC 結構

常數資料表的描述。

## <a name="syntax"></a>語法


```C++
typedef struct D3DXCONSTANTTABLE_DESC {
  LPCSTR Creator;
  DWORD  Version;
  UINT   Constants;
} D3DXCONSTANTTABLE_DESC, *LPD3DXCONSTANTTABLE_DESC;
```



## <a name="members"></a>成員

<dl> <dt>

**建立者**
</dt> <dd>

類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**

</dd> <dd>

常數資料表建立者的名稱。

</dd> <dt>

**版本**
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

著色器版本。

</dd> <dt>

**常數**
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

常數資料表中的常數數目。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3dx9shader。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 結構](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[**D3DXCONSTANT \_ DESC**](d3dxconstant-desc.md)
</dt> </dl>

 

 
