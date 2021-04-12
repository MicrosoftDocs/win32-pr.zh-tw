---
description: 應用程式會使用 ID3DXFileEnumObject 介面的方法，迴圈流覽檔案中的子檔案資料物件，並依其全域唯一識別碼 (GUID) 或其名稱來取得子物件。
ms.assetid: 23b28f07-5832-4163-953b-615d20e781f6
title: 'ID3DXFileEnumObject 介面 (D3DX9Xof .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileEnumObject
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f9b28f94c8d514f81aaa51426557c825da91c4bf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103946153"
---
# <a name="id3dxfileenumobject-interface"></a>ID3DXFileEnumObject 介面

應用程式會使用 ID3DXFileEnumObject 介面的方法，迴圈流覽檔案中的子檔案資料物件，並依其全域唯一識別碼 (GUID) 或其名稱來取得子物件。

## <a name="members"></a>成員

**ID3DXFileEnumObject** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。 **ID3DXFileEnumObject** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**ID3DXFileEnumObject** 介面具有這些方法。



| 方法                                                                  | 描述                                                                |
|:------------------------------------------------------------------------|:---------------------------------------------------------------------------|
| [**System.windows.media.visualtreehelper.getchild**](id3dxfileenumobject--getchild.md)                       | 抓取這個檔案資料物件中的子物件。<br/>              |
| [**GetChildren**](id3dxfileenumobject--getchildren.md)                 | 抓取這個檔案資料物件中的子物件數目。<br/> |
| [**GetDataObjectById**](id3dxfileenumobject--getdataobjectbyid.md)     | 抓取具有指定之 GUID 的資料物件。<br/>          |
| [**GetDataObjectByName**](id3dxfileenumobject--getdataobjectbyname.md) | 抓取具有指定名稱的資料物件。<br/>          |
| [**GetFile**](id3dxfileenumobject--getfile.md)                         | 抓取 [**ID3DXFile**](id3dxfile.md) 物件。<br/>            |



 

## <a name="remarks"></a>備註

ID3DXFileEnumObject 介面的 GUID 是 IID \_ ID3DXFileEnumObject。

LPD3DXFILEENUMOBJECT 型別定義為這個介面的指標。


```
typedef interface ID3DXFileEnumObject *LPD3DXFILEENUMOBJECT;
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Xof。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>  |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX X 檔案介面](dx9-graphics-reference-d3dx-x-file-interfaces.md)
</dt> </dl>

 

 
