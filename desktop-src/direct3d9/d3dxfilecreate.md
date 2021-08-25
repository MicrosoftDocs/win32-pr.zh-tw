---
description: 建立 ID3DXFile 物件的實例。
ms.assetid: c086cb66-b1dc-4180-b966-e9a3b1f36f22
title: 'D3DXFileCreate 函式 (D3DX9Xof) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFileCreate
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: ccafd6e3cffb71cccbdf3025ead6ad2cc012f4d62ecf52405cf82dcda06a1531
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119849788"
---
# <a name="d3dxfilecreate-function"></a>D3DXFileCreate 函式

建立 [**ID3DXFile**](id3dxfile.md) 物件的實例。

## <a name="syntax"></a>語法


```C++
HRESULT STDAPICALLTYPE D3DXFileCreate(
   ID3DXFile **lplpDirectXFile
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*lplpDirectXFile* 
</dt> <dd>

類型： **[ **ID3DXFile**](id3dxfile.md)\*\***

[**ID3DXFile**](id3dxfile.md)介面指標的位址，表示已建立的. x 檔案物件。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果函式成功，則傳回值為 S \_ OK。 如果函式失敗，則傳回值可以是下列其中一項： E \_ 指標、e \_ OUTOFMEMORY。

## <a name="remarks"></a>備註

使用這個函數之後，請使用 [**RegisterTemplates**](id3dxfile--registertemplates.md) 或 [**RegisterEnumTemplates**](id3dxfile--registerenumtemplates.md) 來註冊範本、建立 [**CreateEnumObject**](id3dxfile--createenumobject.md) 來建立列舉值物件，或使用 [**CreateSaveObject**](id3dxfile--createsaveobject.md) 來建立儲存物件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Xof。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>  |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX X 檔案函數](dx9-graphics-reference-d3dx-x-file-functions.md)
</dt> <dt>

[**CreateEnumObject**](id3dxfile--createenumobject.md)
</dt> <dt>

[**CreateSaveObject**](id3dxfile--createsaveobject.md)
</dt> <dt>

[**RegisterEnumTemplates**](id3dxfile--registerenumtemplates.md)
</dt> <dt>

[**RegisterTemplates**](id3dxfile--registertemplates.md)
</dt> </dl>

 

 




