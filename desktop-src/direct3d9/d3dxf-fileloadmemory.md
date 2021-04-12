---
description: 識別記憶體資料。
ms.assetid: 0ec0597f-d83a-4c1e-b993-30f0bbd64e6b
title: 'D3DXF_FILELOADMEMORY 結構 (D3dx9xof .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXF_FILELOADMEMORY
api_type:
- HeaderDef
api_location:
- d3dx9xof.h
ms.openlocfilehash: a7ad988d9906101db57af6f8f5042766c3e32ccc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103946100"
---
# <a name="d3dxf_fileloadmemory-structure"></a>D3DXF \_ FILELOADMEMORY 結構

識別記憶體資料。

## <a name="syntax"></a>語法


```C++
typedef struct D3DXF_FILELOADMEMORY {
  LPCVOID lpMemory;
  SIZE_T  dSize;
} D3DXF_FILELOADMEMORY, *LPD3DXF_FILELOADMEMORY;
```



## <a name="members"></a>成員

<dl> <dt>

**lpMemory**
</dt> <dd>

類型： **[ **LPCVOID**](../winprog/windows-data-types.md)**

</dd> <dd>

要載入之記憶體區塊的指標。

</dd> <dt>

**dSize**
</dt> <dd>

類型： **[**大小 \_ T**](../winprog/windows-data-types.md)**

</dd> <dd>

要載入之記憶體區塊的大小（以位元組為單位）。

</dd> </dl>

## <a name="remarks"></a>備註

當應用程式使用 [**CreateEnumObject**](id3dxfile--createenumobject.md) 方法並指定 D3DXF \_ FILELOAD FROMMEMORY 旗標時，此結構會識別要從記憶體載入的資料 \_ 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3dx9xof。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX X 檔案結構](dx9-graphics-reference-d3dx-x-file-structures.md)
</dt> </dl>

 

 
