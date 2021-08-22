---
description: 建立儲存物件。 已取代。
ms.assetid: 50a7dbde-1dd4-4aae-a9ab-97d6f99618c0
title: 'IDirectXFile：： CreateSaveObject 方法 (DXFile .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFile.CreateSaveObject
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: c3646f54b1f232c6eec3e1b3d06441a8e6a7c090f784e3c4c016f7f1bcfc3b03
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119491848"
---
# <a name="idirectxfilecreatesaveobject-method"></a>IDirectXFile：： CreateSaveObject 方法

建立儲存物件。 已取代。

## <a name="syntax"></a>語法


```C++
HRESULT CreateSaveObject(
  [in]          LPCSTR                  szFileName,
  [in]          DXFILEFORMAT            dwFileFormat,
  [out, retval] LPDIRECTXFILESAVEOBJECT *ppSaveObj
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*szFileName* \[在\]
</dt> <dd>

類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**

要用來儲存資料的檔案名指標。

</dd> <dt>

*dwFileFormat* \[在\]
</dt> <dd>

類型： **[ **DXFILEFORMAT**](dxfile.md)**

指出儲存 DirectX 檔案時要使用的格式。 這個值可以是 \_ [DXFILE 常數](dxfile.md)中的其中一個 DXFILEFORMAT xxx 旗標。 如需詳細資訊，請參閱＜備註＞。

</dd> <dt>

*ppSaveObj* \[退出，retval\]
</dt> <dd>

類型： **[ **LPDIRECTXFILESAVEOBJECT**](idirectxfilesaveobject.md)\***

[**IDirectXFileSaveObject**](idirectxfilesaveobject.md)介面指標的位址，表示所建立的儲存物件。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為 DXFILE \_ OK。 如果方法失敗，則傳回值可以是下列其中一項： DXFILEERR \_ BADALLOC、DXFILEERR \_ BADFILE、DXFILEERR \_ BADVALUE。

## <a name="remarks"></a>備註

使用這個方法之後，請使用 [**IDirectXFileSaveObject**](idirectxfilesaveobject.md) 介面的方法來建立資料物件，以及儲存範本或資料。

檔案格式的預設值為 DXFILEFORMAT \_ BINARY。 您可以將檔案格式值結合成邏輯 OR，以建立壓縮的文字或壓縮的二進位檔案。 如果將檔案指定為二進位 (0) 和文字 (1) ，則會將它儲存為文字檔，因為該值將與文本檔案格式值（ (0 + 1 = 1) ）不區分。 如果您指出檔案格式應為文字和壓縮檔案格式，則會先將檔案寫出為文字，然後壓縮。 不過，壓縮文字檔的效率不如二進位文字檔，因此在大部分情況下，您會想要指出二進位檔和壓縮檔案。 設定要壓縮但未指定格式的檔案，將會產生二進位、壓縮檔案。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>DXFile。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>D3dxof .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[IDirectXFile](idirectxfile.md)
</dt> <dt>

[**IDirectXFileSaveObject**](idirectxfilesaveobject.md)
</dt> </dl>

 

 
