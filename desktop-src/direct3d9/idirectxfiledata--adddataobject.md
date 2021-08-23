---
description: 將資料物件新增為子物件。 已取代。
ms.assetid: 43771dd6-c17f-4376-9b0a-459ba61ff4c5
title: 'IDirectXFileData：： AddDataObject 方法 (DXFile .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileData.AddDataObject
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: db11f5f3c0d9078663c87db8948bc483ab05d229cd4d7fd0950efaf5143e1408
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119491828"
---
# <a name="idirectxfiledataadddataobject-method"></a>IDirectXFileData：： AddDataObject 方法

將資料物件新增為子物件。 已取代。

## <a name="syntax"></a>語法


```C++
HRESULT AddDataObject(
  [in] LPDIRECTXFILEDATA pDataObj
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pDataObj* \[在\]
</dt> <dd>

類型： **[ **LPDIRECTXFILEDATA**](idirectxfiledata.md)**

[**IDirectXFileData**](idirectxfiledata.md)介面的指標，代表要新增為子物件的檔案資料物件。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為 DXFILE \_ OK。 如果方法失敗，則傳回值可以是下列其中一個值。DXFILEERR \_ BADALLOC DXFILEERR \_ BADVALUE

## <a name="remarks"></a>備註

在呼叫這個方法之前，請使用 [**IDirectXFileSaveObject：： CreateDataObject**](idirectxfilesaveobject--createdataobject.md) 方法來建立 [**IDirectXFileData**](idirectxfiledata.md) 物件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>DXFile。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>D3dxof .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[IDirectXFileData](idirectxfiledata.md)
</dt> <dt>

[**IDirectXFileSaveObject::CreateDataObject**](idirectxfilesaveobject--createdataobject.md)
</dt> </dl>

 

 




