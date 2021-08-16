---
description: 描述效果物件。
ms.assetid: 161d3e7a-213a-4a83-a1b5-837b0aab96bf
title: 'D3DXEFFECT_DESC 結構 (D3dx9effect .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXEFFECT_DESC
api_type:
- HeaderDef
api_location:
- d3dx9effect.h
ms.openlocfilehash: 0b30ad0348a5c799690d668e036724d30808c2998eee9d762fa2ad3fc8106c91
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118298591"
---
# <a name="d3dxeffect_desc-structure"></a>D3DXEFFECT \_ DESC 結構

描述效果物件。

## <a name="syntax"></a>語法


```C++
typedef struct D3DXEFFECT_DESC {
  LPCSTR Creator;
  UINT   Parameters;
  UINT   Techniques;
  UINT   Functions;
} D3DXEFFECT_DESC, *LPD3DXEFFECT_DESC;
```



## <a name="members"></a>成員

<dl> <dt>

**建立者**
</dt> <dd>

類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**

</dd> <dd>

字串，其中包含效果建立者的名稱。

</dd> <dt>

**參數**
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

用於效果的參數數目。

</dd> <dt>

**技術**
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

可以呈現效果的技術數目。

</dd> <dt>

**函數**
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

可以呈現效果的函式數目。

</dd> </dl>

## <a name="remarks"></a>備註

效果物件可以包含相同效果的多種轉譯技巧和參數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3dx9effect。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[效果結構](dx9-graphics-reference-effects-structures.md)
</dt> </dl>

 

 
