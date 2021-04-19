---
description: 抓取具有指定名稱的資料物件。 已取代。
ms.assetid: d04d5a45-72d9-4256-8700-378e8139ed36
title: 'IDirectXFileEnumObject：： GetDataObjectByName 方法 (DXFile .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileEnumObject.GetDataObjectByName
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 858097139702770d148765c4c9a57f6522d9633b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106985908"
---
# <a name="idirectxfileenumobjectgetdataobjectbyname-method"></a>IDirectXFileEnumObject：： GetDataObjectByName 方法

抓取具有指定名稱的資料物件。 已取代。

## <a name="syntax"></a>語法


```C++
HRESULT GetDataObjectByName(
  [in]  LPCSTR            szName,
  [out] LPDIRECTXFILEDATA *ppDataObj
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*>szname* \[在\]
</dt> <dd>

類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**

所要求名稱的指標。

</dd> <dt>

*ppDataObj* \[擴展\]
</dt> <dd>

類型： **[ **LPDIRECTXFILEDATA**](idirectxfiledata.md)\***

[**IDirectXFileData**](idirectxfiledata.md)介面指標的位址，表示傳回的檔案資料物件。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為 DXFILE \_ OK。 如果方法失敗，則傳回值可以是下列其中一個值： DXFILEERR \_ BADVALUE，DXFILEERR \_ NOTFOUND。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>DXFile。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>D3dxof .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[IDirectXFileEnumObject](idirectxfileenumobject.md)
</dt> </dl>

 

 
