---
description: 建立儲存物件，該物件將用來將資料儲存至 x.x 檔案。
ms.assetid: da064e83-605f-4c86-985d-9a0961c18e01
title: 'ID3DXFile：： CreateSaveObject 方法 (D3DX9Xof .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFile.CreateSaveObject
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: d7c5b3de020ad50abfd8834aabbdc8e6e848d71d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106985534"
---
# <a name="id3dxfilecreatesaveobject-method"></a>ID3DXFile：： CreateSaveObject 方法

建立儲存物件，該物件將用來將資料儲存至 x.x 檔案。

## <a name="syntax"></a>語法


```C++
HRESULT CreateSaveObject(
  [in]  LPCVOID               pData,
  [in]  D3DXF_FILESAVEOPTIONS flags,
  [in]  D3DXF_FILEFORMAT      dwFileFormat,
  [out] ID3DXFileSaveObject   **ppSaveObj
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*.pdata* \[在\]
</dt> <dd>

類型： **[ **LPCVOID**](../winprog/windows-data-types.md)**

要用來儲存資料的檔案名指標。

</dd> <dt>

*旗標* \[在\]
</dt> <dd>

類型： **[D3DXF \_ FILESAVEOPTIONS](d3dxf.md)**

值，指定要儲存資料的檔案名。 這個值可以是其中一個 [ [儲存選項](d3dxf.md) ] 旗標。

</dd> <dt>

*dwFileFormat* \[在\]
</dt> <dd>

類型： **[D3DXF \_ >fileformat](d3dxf.md)**

指出儲存. x 檔案時要使用的格式。 這個值可以是其中一個 [檔案格式](d3dxf.md) 旗標。 如需詳細資訊，請參閱＜備註＞。

</dd> <dt>

*ppSaveObj* \[擴展\]
</dt> <dd>

類型： **[ **ID3DXFileSaveObject**](id3dxfilesaveobject.md)\*\***

[**ID3DXFileSaveObject**](id3dxfilesaveobject.md)介面指標的位址，表示所建立的儲存物件。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為 S \_ OK。 如果方法失敗，則傳回值可以是下列其中一項： D3DXFERR \_ BADVALUE，D3DXFERR \_ PARSEERROR。

## <a name="remarks"></a>備註

使用這個方法之後，請使用 [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) 介面的方法來建立資料物件，以及儲存範本或資料。

針對已儲存的檔案格式 *dwFileFormat*，必須指定 [檔案格式](d3dxf.md) 中的其中一個二進位檔、舊版二進位檔或文字旗標。 您可以使用選擇性的 D3DXF \_ >fileformat 壓縮旗標來壓縮檔案 \_ 。

您可以將檔案格式值結合成邏輯 OR，以建立壓縮的文字或壓縮的二進位檔案。 如果您指出檔案格式應該是文字並壓縮檔案，則會先將檔案寫出為文字，然後壓縮。 不過，壓縮的文字檔不如二進位文字檔一樣有效率;因此，在大部分情況下，您會想要指出二進位和壓縮。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Xof。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>  |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXFile](id3dxfile.md)
</dt> <dt>

[**ID3DXFileSaveObject**](id3dxfilesaveobject.md)
</dt> </dl>

 

 
