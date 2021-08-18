---
description: 建立將讀取 x.x 檔案的列舉值物件。
ms.assetid: 86d05eab-601c-4beb-9dbe-c23fa524871c
title: 'ID3DXFile：： CreateEnumObject 方法 (D3DX9Xof .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFile.CreateEnumObject
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 528ab441da6cd4370de4ecad5d8490e6e74b5977672d0c7d4126cea1b7bab8fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119044396"
---
# <a name="id3dxfilecreateenumobject-method"></a>ID3DXFile：： CreateEnumObject 方法

建立將讀取 x.x 檔案的列舉值物件。

## <a name="syntax"></a>語法


```C++
HRESULT CreateEnumObject(
  [out] LPCVOID               pvSource,
  [in]  D3DXF_FILELOADOPTIONS loadflags,
  [out] ID3DXFileEnumObject   **ppEnumObj
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pvSource* \[擴展\]
</dt> <dd>

類型： **[ **LPCVOID**](../winprog/windows-data-types.md)**

資料來源。 任一：

-   檔案名
-   [**D3DXF \_ FILELOADMEMORY**](d3dxf-fileloadmemory.md)結構
-   [**D3DXF \_ FILELOADRESOURCE**](d3dxf-fileloadresource.md)結構

取決於 loadflags 的值。

</dd> <dt>

*loadflags* \[在\]
</dt> <dd>

類型： **[D3DXF \_ FILELOADOPTIONS](d3dxf.md)**

指定資料來源的值。 這個值可以是其中一個 [D3DXF \_ FILELOADOPTIONS](d3dxf.md) 旗標。

</dd> <dt>

*ppEnumObj* \[擴展\]
</dt> <dd>

類型： **[ **ID3DXFileEnumObject**](id3dxfileenumobject.md)\*\***

[**ID3DXFileEnumObject**](id3dxfileenumobject.md)介面指標的位址，表示已建立的枚舉器物件。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為 S \_ OK。 如果方法失敗，則傳回值可以是下列其中一項： D3DXFERR \_ BADVALUE，D3DXFERR \_ PARSEERROR。

## <a name="remarks"></a>備註

使用這個方法之後，請使用其中一個 [**ID3DXFileEnumObject**](id3dxfileenumobject.md) 方法來取出資料物件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Xof。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>  |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXFile](id3dxfile.md)
</dt> <dt>

[**ID3DXFileEnumObject**](id3dxfileenumobject.md)
</dt> </dl>

 

 
