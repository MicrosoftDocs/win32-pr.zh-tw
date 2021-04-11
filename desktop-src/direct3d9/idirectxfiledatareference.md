---
description: 應用程式會使用 IDirectXFileDataReference 介面的方法來支援資料參考物件。
ms.assetid: e0f6046f-36d9-4a13-9a0c-0738ebb2e569
title: 'IDirectXFileDataReference 介面 (DXFile .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileDataReference
api_type:
- COM
api_location:
- d3dxof.lib
- d3dxof.dll
ms.openlocfilehash: d04d2367f914c2e8d64a3c9c64fb55df1e51e47c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104116309"
---
# <a name="idirectxfiledatareference-interface"></a>IDirectXFileDataReference 介面

應用程式會使用 IDirectXFileDataReference 介面的方法來支援資料參考物件。 資料參考物件會參考先前在檔案中定義的資料物件。 這可讓您多次使用相同的物件，而不需要在檔案中重複。 已取代。

## <a name="members"></a>成員

**IDirectXFileDataReference** 介面繼承自 [**IDirectXFileObject**](idirectxfileobject.md)。 **IDirectXFileDataReference** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IDirectXFileDataReference** 介面具有這些方法。



| 方法                                                | 描述                                      |
|:------------------------------------------------------|:-------------------------------------------------|
| [**解決**](idirectxfiledatareference--resolve.md) | 解析資料參考。 已取代。<br/> |



 

## <a name="remarks"></a>備註

確定物件是資料參考物件之後，請使用 [**IDirectXFileDataReference：： Resolve**](idirectxfiledatareference--resolve.md) 方法來取出先前在檔案中定義的參考物件。 如需如何識別資料參考物件的詳細資訊，請參閱 [**IDirectXFileData**](idirectxfiledata.md) 介面。

IDirectXFileDataReference 介面的 GUID 是 IID \_ IDirectXFileDataReference。

LPDIRECTXFILEDataReference 型別定義為這個介面的指標。


```
typedef interface IDirectXFileDataReference *LPDIRECTXFILEDATAREFERENCE;
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

 

 




