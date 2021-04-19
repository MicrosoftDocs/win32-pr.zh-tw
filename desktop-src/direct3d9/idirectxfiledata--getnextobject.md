---
description: 抓取 DirectX 檔案中的下一個子資料物件、資料參考物件或二進位物件。 已取代。
ms.assetid: 8232e911-6552-4b2b-a9c2-59e6a13a0d9b
title: 'IDirectXFileData：： GetNextObject 方法 (DXFile .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileData.GetNextObject
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: e03351068cdc4f8fca28c612b7bb4c546125a4cc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106997412"
---
# <a name="idirectxfiledatagetnextobject-method"></a>IDirectXFileData：： GetNextObject 方法

抓取 DirectX 檔案中的下一個子資料物件、資料參考物件或二進位物件。 已取代。

## <a name="syntax"></a>語法


```C++
HRESULT GetNextObject(
  [out, retval] LPDIRECTXFILEOBJECT *ppChildObj
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ppChildObj* \[退出，retval\]
</dt> <dd>

類型： **[ **LPDIRECTXFILEOBJECT**](idirectxfileobject.md)\***

[**IDirectXFileObject**](idirectxfileobject.md)介面指標的位址，表示傳回的子物件的檔案物件介面。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為 DXFILE \_ OK。 如果方法失敗，則傳回值可以是下列其中一個值： DXFILEERR \_ BADVALUE，DXFILEERR \_ NOMOREOBJECTS。

## <a name="remarks"></a>備註

若要判斷抓取的物件類型，請使用 QueryInterface 來查詢已抓取的物件，以支援 [**IDirectXFileData**](idirectxfiledata.md)、 [**IDirectXFileDataReference**](idirectxfiledatareference.md)或 [**IDirectXFileBinary**](idirectxfilebinary.md) 介面。 支援的介面表示 (資料、資料參考或二進位) 的物件類型。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>DXFile。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>D3dxof .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IDirectXFileBinary**](idirectxfilebinary.md)
</dt> <dt>

[**IDirectXFileData**](idirectxfiledata.md)
</dt> <dt>

[**IDirectXFileDataReference**](idirectxfiledatareference.md)
</dt> </dl>

 

 




