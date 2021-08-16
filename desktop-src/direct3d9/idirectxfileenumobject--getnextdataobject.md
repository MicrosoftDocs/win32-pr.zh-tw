---
description: 抓取 DirectX 檔案中的下一個最上層物件。 已取代。
ms.assetid: 91cd3205-5603-4a62-aab2-7ef4adb9e6d1
title: 'IDirectXFileEnumObject：： GetNextDataObject 方法 (DXFile .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileEnumObject.GetNextDataObject
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 42d95fcee1b431f5121389d7bb6595e5c53ca56298c75ed6010ee86733c310e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119985128"
---
# <a name="idirectxfileenumobjectgetnextdataobject-method"></a>IDirectXFileEnumObject：： GetNextDataObject 方法

抓取 DirectX 檔案中的下一個最上層物件。 已取代。

## <a name="syntax"></a>語法


```C++
HRESULT GetNextDataObject(
  [out] LPDIRECTXFILEDATA *ppDataObj
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ppDataObj* \[擴展\]
</dt> <dd>

類型： **[ **LPDIRECTXFILEDATA**](idirectxfiledata.md)\***

[**IDirectXFileData**](idirectxfiledata.md)介面指標的位址，表示傳回的檔案資料物件。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為 DXFILE \_ OK。 如果方法失敗，則傳回值可以是下列其中一個值： DXFILEERR \_ BADVALUE、DXFILEERR \_ NOMOREOBJECTS

## <a name="remarks"></a>備註

最上層物件一律是資料物件。 資料參考物件和二進位物件只能是資料物件的子系。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>DXFile。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>D3dxof .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[IDirectXFileEnumObject](idirectxfileenumobject.md)
</dt> </dl>

 

 




