---
description: 管理著色器常數資料表的協助程式結構。 這也可以使用 ID3DXConstantTable 來完成。
ms.assetid: cc6d66e4-c600-420b-b7b5-1bd10ecb22f9
title: 'D3DXSHADER_CONSTANTTABLE 結構 (D3dx9shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHADER_CONSTANTTABLE
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: f423eba3187c6bbc5c17d4ba9284e4e1b2048a016b8a11744b83b46e4d8522af
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120027288"
---
# <a name="d3dxshader_constanttable-structure"></a>D3DXSHADER \_ CONSTANTTABLE 結構

管理著色器常數資料表的協助程式結構。 這也可以使用 [**ID3DXConstantTable**](id3dxconstanttable.md)來完成。

## <a name="syntax"></a>語法


```C++
typedef struct D3DXSHADER_CONSTANTTABLE {
  DWORD Size;
  DWORD Creator;
  DWORD Version;
  DWORD Constants;
  DWORD ConstantInfo;
  DWORD Flags;
  DWORD Target;
} D3DXSHADER_CONSTANTTABLE, *LPD3DXSHADER_CONSTANTTABLE;
```



## <a name="members"></a>成員

<dl> <dt>

**大小**
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

結構的大小。 請參閱＜備註＞。

</dd> <dt>

**建立者**
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

從這個結構開頭算起的位移（以位元組為單位），指向包含建立者名稱的字串。

</dd> <dt>

**版本**
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

著色器版本。

</dd> <dt>

**常數**
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

常數的數目。

</dd> <dt>

**ConstantInfo**
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

常數資訊的陣列，D3DXSHADER \_ CONSTANTINFO \[ *常數* \] 。 請參閱 [**D3DXSHADER \_ CONSTANTINFO**](d3dxshader-constantinfo.md)。

</dd> <dt>

**旗標**
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

用來編譯著色器的 [D3DXSHADER 旗](d3dxshader-flags.md) 標旗標。

</dd> <dt>

**Target**
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

包含目標之字串的位移。

</dd> </dl>

## <a name="remarks"></a>備註

著色器常數資訊會包含在以 tab 分隔的批註資料表中。 所有位移都會以位元組為單位，從結構的開頭算起。 常數資料表中的專案會依建立者的遞增順序排序。

您可以使用 [**ID3DXConstantTable**](id3dxconstanttable.md) 介面來管理著色器常數資料表。 或者，您也可以使用 **D3DXSHADER \_ CONSTANTTABLE** 來管理常數資料表。

此大小成員通常會使用下列程式初始化：


```
D3DXSHADER_CONSTANTTABLE constantTable;
constantTable.Size = sizeof(D3DXSHADER_CONSTANTTABLE)
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3dx9shader。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 結構](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[**D3DXGetShaderConstantTable**](d3dxgetshaderconstanttable.md)
</dt> </dl>

 

 
