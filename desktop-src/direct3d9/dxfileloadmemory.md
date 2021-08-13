---
description: 識別記憶體資料。 已取代。
ms.assetid: fe791e13-d5de-425f-b68f-80db8b332cc6
title: 'DXFILELOADMEMORY 結構 (DXFile .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DXFILELOADMEMORY
api_type:
- HeaderDef
api_location:
- DXFile.h
ms.openlocfilehash: 3de6db80e12197f3ad61dd845519be7f532d320765c491cba7a8219ee701af05
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119407458"
---
# <a name="dxfileloadmemory-structure"></a>DXFILELOADMEMORY 結構

識別記憶體資料。 已取代。

## <a name="syntax"></a>語法


```C++
typedef struct DXFILELOADMEMORY {
  LPVOID lpMemory;
  DWORD  dSize;
} DXFILELOADMEMORY, *LPDXFILELOADMEMORY;
```



## <a name="members"></a>成員

<dl> <dt>

**lpMemory**
</dt> <dd>

類型： **[ **LPVOID**](../winprog/windows-data-types.md)**

</dd> <dd>

要載入之記憶體區塊的指標。

</dd> <dt>

**dSize**
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

要載入之記憶體區塊的大小（以位元組為單位）。

</dd> </dl>

## <a name="remarks"></a>備註

當應用程式使用 [**CreateEnumObject**](idirectxfile--createenumobject.md) 方法並指定 DXFILELOAD FROMMEMORY 時，此結構會識別要載入的資源 \_ 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>DXFile。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[X 檔案結構](dx9-graphics-reference-x-file-structures.md)
</dt> <dt>

[**CreateEnumObject**](idirectxfile--createenumobject.md)
</dt> <dt>

[DXFILE 常數](dxfile.md)
</dt> </dl>

 

 
