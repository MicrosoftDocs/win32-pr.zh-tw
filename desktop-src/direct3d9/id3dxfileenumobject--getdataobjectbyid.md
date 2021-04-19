---
description: 抓取具有指定之 GUID 的資料物件。
ms.assetid: c3d598bd-0646-4f99-8517-4475ef7cd8c9
title: 'ID3DXFileEnumObject：： GetDataObjectById 方法 (D3DX9Xof .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileEnumObject.GetDataObjectById
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 82a74ca4ff472d678ded92aa01f2c2406560955e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106992729"
---
# <a name="id3dxfileenumobjectgetdataobjectbyid-method"></a>ID3DXFileEnumObject：： GetDataObjectById 方法

抓取具有指定之 GUID 的資料物件。

## <a name="syntax"></a>語法


```C++
HRESULT GetDataObjectById(
  [in]  REFGUID        rguid,
  [out] LPD3DXFILEDATA *ppDataObj
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*rguid* \[在\]
</dt> <dd>

類型： **[REFGUID](/openspecs/windows_protocols/ms-oaut/6e7d7108-c213-40bc-8294-ac13fe68fd50)**

參考要求的 GUID。

</dd> <dt>

*ppDataObj* \[擴展\]
</dt> <dd>

類型： **[ **LPD3DXFILEDATA**](id3dxfiledata.md)\***

[**ID3DXFileData**](id3dxfiledata.md)介面指標的位址，表示傳回的檔案資料物件。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為 S \_ OK。 如果方法失敗，則傳回值可以是下列其中一項： DXFILEERR \_ BADVALUE，DXFILEERR \_ NOTFOUND。

## <a name="remarks"></a>備註

使用 [**ID3DXFileData：： GetId**](id3dxfiledata--getid.md) 方法，取得目前檔案資料物件的 GUID rguid。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Xof。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>  |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXFileEnumObject](id3dxfileenumobject.md)
</dt> </dl>

 

 
