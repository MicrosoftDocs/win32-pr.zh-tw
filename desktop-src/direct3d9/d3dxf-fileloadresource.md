---
description: 識別資源資料。
ms.assetid: f2ace2ad-228f-4f76-ab31-16e045e09331
title: 'D3DXF_FILELOADRESOURCE 結構 (D3dx9xof .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXF_FILELOADRESOURCE
api_type:
- HeaderDef
api_location:
- d3dx9xof.h
ms.openlocfilehash: ddc105d3df7732e1572e41c3d9cb47a285caf69cba0a24f6ea65090706394592
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119564928"
---
# <a name="d3dxf_fileloadresource-structure"></a>D3DXF \_ FILELOADRESOURCE 結構

識別資源資料。

## <a name="syntax"></a>語法


```C++
typedef struct D3DXF_FILELOADRESOURCE {
  HMODULE hModule;
  LPCSTR  lpName;
  LPCSTR  lpType;
} D3DXF_FILELOADRESOURCE, *LPD3DXF_FILELOADRESOURCE;
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

類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**

</dd> <dd>

指定要載入之資源名稱的字串指標。 例如，如果資源是網格，則這個成員應指定網格檔案的名稱。

</dd> <dt>

**lpType**
</dt> <dd>

類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**

</dd> <dd>

字串的指標，指定識別資源的使用者定義型別。

</dd> </dl>

## <a name="remarks"></a>備註

當應用程式使用 [**CreateEnumObject**](id3dxfile--createenumobject.md) 方法並指定 [D3DXF \_ FILELOAD \_ FROMRESOURCE](d3dxf.md) 旗標時，此結構會識別要載入的資源。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3dx9xof。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX X 檔案結構](dx9-graphics-reference-d3dx-x-file-structures.md)
</dt> </dl>

 

 
