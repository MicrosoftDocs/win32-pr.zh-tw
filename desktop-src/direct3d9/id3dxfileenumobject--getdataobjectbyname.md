---
description: 抓取具有指定名稱的資料物件。
ms.assetid: ed53d871-24e8-4c51-8897-1055ef8a9af1
title: 'ID3DXFileEnumObject：： GetDataObjectByName 方法 (D3DX9Xof .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileEnumObject.GetDataObjectByName
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: f42c82fb2eeedf6c1ec6c0f8099e6fbc1f6bac8d9e96bafbb6a94bacbf8f20e5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119951538"
---
# <a name="id3dxfileenumobjectgetdataobjectbyname-method"></a>ID3DXFileEnumObject：： GetDataObjectByName 方法

抓取具有指定名稱的資料物件。

## <a name="syntax"></a>語法


```C++
HRESULT GetDataObjectByName(
  [in]  LPCSTR        szName,
  [out] ID3DXFileData **ppObj
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*>szname* \[在\]
</dt> <dd>

類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**

所要求名稱的指標。

</dd> <dt>

*ppObj* \[擴展\]
</dt> <dd>

類型： **[ **ID3DXFileData**](id3dxfiledata.md)\*\***

[**ID3DXFileData**](id3dxfiledata.md)介面指標的位址，表示傳回的檔案資料物件。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為 S \_ OK。 如果方法失敗，則傳回值可以是下列其中一項： DXFILEERR \_ BADVALUE，DXFILEERR \_ NOTFOUND。

## <a name="remarks"></a>備註

使用 [**ID3DXFileData：： GetName**](id3dxfiledata--getname.md) 方法，取得目前檔案資料物件的名稱 >szname。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Xof。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>  |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXFileEnumObject](id3dxfileenumobject.md)
</dt> </dl>

 

 
