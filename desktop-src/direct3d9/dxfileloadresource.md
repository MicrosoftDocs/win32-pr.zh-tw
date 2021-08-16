---
description: 識別資源資料。 已取代。
ms.assetid: acb379c7-ac80-412f-8891-d5917b3f8da4
title: 'DXFILELOADRESOURCE 結構 (DXFile .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DXFILELOADRESOURCE
api_type:
- HeaderDef
api_location:
- DXFile.h
ms.openlocfilehash: 54d0072d7c87f6d26483faf8c591ea7651eff29b411643eb9848de11ff50d899
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118803035"
---
# <a name="dxfileloadresource-structure"></a>DXFILELOADRESOURCE 結構

識別資源資料。 已取代。

## <a name="syntax"></a>語法


```C++
typedef struct DXFILELOADRESOURCE {
  HMODULE hModule;
  LPCTSTR lpName;
  LPCTSTR lpType;
} DXFILELOADRESOURCE, *LPDXFILELOADRESOURCE;
```



## <a name="members"></a>成員

<dl> <dt>

**hModule**
</dt> <dd>

類型： **[ **HMODULE**](../winprog/windows-data-types.md)**

</dd> <dd>

模組的控制碼，其中包含要載入的資源。 如果這個成員是 **Null**，則資源必須附加至將使用它的可執行檔。

</dd> <dt>

**lpName**
</dt> <dd>

類型： **[ **LPCTSTR**](../winprog/windows-data-types.md)**

</dd> <dd>

指定要載入之資源名稱的字串指標。 例如，如果資源是網格，則這個成員應指定網格檔案的名稱。

</dd> <dt>

**lpType**
</dt> <dd>

類型： **[ **LPCTSTR**](../winprog/windows-data-types.md)**

</dd> <dd>

字串的指標，指定識別資源的使用者定義型別。

</dd> </dl>

## <a name="remarks"></a>備註

當應用程式使用 [**CreateEnumObject**](idirectxfile--createenumobject.md) 方法並指定 DXFILELOAD FROMRESOURCE 時，此結構會識別要載入的資源 \_ 。

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

 

 
