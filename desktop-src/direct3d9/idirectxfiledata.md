---
description: 應用程式會使用 IDirectXFileData 介面的方法來建立或存取資料物件的直屬階層。
ms.assetid: 8810162f-76a8-45ba-b069-7910fd611a60
title: 'IDirectXFileData 介面 (DXFile .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileData
api_type:
- COM
api_location:
- d3dxof.lib
- d3dxof.dll
ms.openlocfilehash: 72b3ffa54d9ec0362100b2e2f1ac54b417d1425d0e6e311da3f9b5b7d30a553a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118800208"
---
# <a name="idirectxfiledata-interface"></a>IDirectXFileData 介面

應用程式會使用 IDirectXFileData 介面的方法來建立或存取資料物件的直屬階層。 範本限制會決定階層。 範本所允許的資料類型稱為選擇性成員。 選用的成員並不是必要的，但物件可能會遺失重要資訊。 這些選用的成員會儲存為數據物件的子系。 子系可以是另一個資料物件、較早資料物件的參考，或二進位物件。 已取代。

## <a name="members"></a>成員

**IDirectXFileData** 介面繼承自 [**IDirectXFileObject**](idirectxfileobject.md)。 **IDirectXFileData** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IDirectXFileData** 介面具有這些方法。



| 方法                                                         | 描述                                                                                                               |
|:---------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------|
| [**AddBinaryObject**](idirectxfiledata--addbinaryobject.md)   | 建立二進位物件，並將它新增為子物件。 已取代。<br/>                                             |
| [**AddDataObject**](idirectxfiledata--adddataobject.md)       | 將資料物件新增為子物件。 已取代。<br/>                                                              |
| [**AddDataReference**](idirectxfiledata--adddatareference.md) | 建立資料參考物件，並將其新增為子物件。 已取代。<br/>                                        |
| [**GetData**](idirectxfiledata--getdata.md)                   | 抓取其中一個物件成員的資料，或所有成員的資料。 已取代。<br/>                    |
| [**GetNextObject**](idirectxfiledata--getnextobject.md)       | 抓取 DirectX 檔案中的下一個子資料物件、資料參考物件或二進位物件。 已取代。<br/> |
| [**GetType**](idirectxfiledata--gettype.md)                   | 抓取物件之範本的 GUID。 已取代。<br/>                                                       |



 

## <a name="remarks"></a>備註

IDirectXFileData 介面的 GUID 是 IID \_ IDirectXFileData。

LPDIRECTXFILEDATA 型別定義為這個介面的指標。


```
typedef interface IDirectXFileData *LPDIRECTXFILEDATA;
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>DXFile。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>D3dxof .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IDirectXFileObject**](idirectxfileobject.md)
</dt> <dt>

[X 檔案介面](dx9-graphics-reference-x-file-interfaces.md)
</dt> </dl>

 

 




