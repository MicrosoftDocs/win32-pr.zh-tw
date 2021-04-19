---
description: 應用程式會使用 ID3DXFileSaveObject 介面的方法，將. x 檔案寫入至磁片，以及加入和儲存資料物件和範本。
ms.assetid: 1131c151-fa21-4654-9776-484922d58487
title: 'ID3DXFileSaveObject 介面 (D3DX9Xof .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveObject
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f8d657c327c75045cf4feb2080a2e57d80f752df
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106976481"
---
# <a name="id3dxfilesaveobject-interface"></a>ID3DXFileSaveObject 介面

應用程式會使用 ID3DXFileSaveObject 介面的方法，將. x 檔案寫入至磁片，以及加入和儲存資料物件和範本。

## <a name="members"></a>成員

**ID3DXFileSaveObject** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。 **ID3DXFileSaveObject** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**ID3DXFileSaveObject** 介面具有這些方法。



| 方法                                                      | 描述                                                                                                                  |
|:------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------|
| [**AddDataObject**](id3dxfilesaveobject--adddataobject.md) | 將資料物件新增為 [**ID3DXFileSaveData**](id3dxfilesavedata.md) 物件的子系。<br/>                       |
| [**GetFile**](id3dxfilesaveobject--getfile.md)             | 取得建立這個 **ID3DXFileSaveObject** 物件之物件的 [**ID3DXFile**](id3dxfile.md)介面。<br/> |
| [**儲存**](id3dxfilesaveobject--save.md)                   | 將資料物件和其子系儲存至磁片上的. x 檔案。<br/>                                                        |



 

## <a name="remarks"></a>備註

每個檔案都不需要範本。 例如，您可以將所有範本放入單一的. x 檔案中，而不是在每個. x 檔案中複製它們。

ID3DXFileSaveObject 介面的取得方式是呼叫 [**ID3DXFile：： CreateSaveObject**](id3dxfile--createsaveobject.md) 方法。

ID3DXFileSaveObject 介面 (GUID) 的全域唯一識別碼為 IID \_ ID3DXFileSaveObject。

LPD3DXFILESAVEOBJECT 型別定義為這個介面的指標。


```
typedef interface ID3DXFileSaveObject *LPD3DXFILESAVEOBJECT;
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

 

 
