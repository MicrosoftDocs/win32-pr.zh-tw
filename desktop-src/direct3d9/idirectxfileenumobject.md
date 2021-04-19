---
description: 應用程式會使用 IDirectXFileEnumObject 介面的方法來迴圈處理檔案中的資料物件，並依其全域唯一識別碼 (GUID) 或其名稱來取得資料物件。 已取代。
ms.assetid: 9eefda2a-5b17-4330-8245-63a38c1b1469
title: 'IDirectXFileEnumObject 介面 (DXFile .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileEnumObject
api_type:
- COM
api_location:
- d3dxof.lib
- d3dxof.dll
ms.openlocfilehash: f9220f6e0a406cb4143798787276d7aa6cb5f5d1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106989193"
---
# <a name="idirectxfileenumobject-interface"></a>IDirectXFileEnumObject 介面

應用程式會使用 IDirectXFileEnumObject 介面的方法來迴圈處理檔案中的資料物件，並依其全域唯一識別碼 (GUID) 或其名稱來取得資料物件。 已取代。

## <a name="members"></a>成員

**IDirectXFileEnumObject** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。 **IDirectXFileEnumObject** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IDirectXFileEnumObject** 介面具有這些方法。



| 方法                                                                     | 描述                                                                     |
|:---------------------------------------------------------------------------|:--------------------------------------------------------------------------------|
| [**GetDataObjectById**](idirectxfileenumobject--getdataobjectbyid.md)     | 抓取具有指定之 GUID 的資料物件。 已取代。<br/>   |
| [**GetDataObjectByName**](idirectxfileenumobject--getdataobjectbyname.md) | 抓取具有指定名稱的資料物件。 已取代。<br/>   |
| [**GetNextDataObject**](idirectxfileenumobject--getnextdataobject.md)     | 抓取 DirectX 檔案中的下一個最上層物件。 已取代。<br/> |



 

## <a name="remarks"></a>備註

IDirectXFileEnumObject 介面的 GUID 是 IID \_ IDirectXFileEnumObject。

LPDIRECTXFILEENUMOBJECT 型別定義為這個介面的指標。


```
typedef interface IDirectXFileEnumObject *LPDIRECTXFILEENUMOBJECT;
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>DXFile。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>D3dxof .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[X 檔案介面](dx9-graphics-reference-x-file-interfaces.md)
</dt> </dl>

 

 
