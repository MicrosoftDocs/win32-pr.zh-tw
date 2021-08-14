---
description: 包含成員結構資訊的 helper 結構。
ms.assetid: 2fbe5e97-047e-48bf-9413-dd297632288a
title: 'D3DXSHADER_STRUCTMEMBERINFO 結構 (D3dx9shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHADER_STRUCTMEMBERINFO
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: 6f41c3d1911a046165d929bee50ef4e0b5691cebee9d90007bc367636e343731
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118524211"
---
# <a name="d3dxshader_structmemberinfo-structure"></a>D3DXSHADER \_ STRUCTMEMBERINFO 結構

包含成員結構資訊的 helper 結構。

## <a name="syntax"></a>語法


```C++
typedef struct D3DXSHADER_STRUCTMEMBERINFO {
  DWORD Name;
  DWORD TypeInfo;
} D3DXSHADER_STRUCTMEMBERINFO, *LPD3DXSHADER_STRUCTMEMBERINFO;
```



## <a name="members"></a>成員

<dl> <dt>

**名稱**
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

從這個結構開頭算起的位移（以位元組為單位），指向包含結構成員名稱的字串。

</dd> <dt>

**TypeInfo**
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

從這個結構開頭算起的位移（以位元組為單位），指向包含型別資訊的字串。 請參閱 [**D3DXSHADER \_ TYPEINFO**](d3dxshader-typeinfo.md)。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3dx9shader。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 結構](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[**D3DXSHADER \_ TYPEINFO**](d3dxshader-typeinfo.md)
</dt> </dl>

 

 
