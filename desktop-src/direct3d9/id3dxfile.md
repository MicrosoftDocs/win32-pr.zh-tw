---
description: 應用程式會使用 ID3DXFile 介面的方法來建立 ID3DXFileEnumObject 和 ID3DXFileSaveObject 介面的實例，以及註冊範本。
ms.assetid: 472d45b1-5c03-4417-a005-91f802667919
title: 'ID3DXFile 介面 (D3DX9Xof .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFile
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 45af79c4fb01c95b25803788f79588a3880fe264
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "107000605"
---
# <a name="id3dxfile-interface"></a>ID3DXFile 介面

應用程式會使用 ID3DXFile 介面的方法來建立 [**ID3DXFileEnumObject**](id3dxfileenumobject.md) 和 [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) 介面的實例，以及註冊範本。

## <a name="members"></a>成員

**ID3DXFile** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。 **ID3DXFile** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**ID3DXFile** 介面具有這些方法。



| 方法                                                            | 描述                                                                                                            |
|:------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------|
| [**CreateEnumObject**](id3dxfile--createenumobject.md)           | 建立將讀取 x.x 檔案的列舉值物件。<br/>                                                      |
| [**CreateSaveObject**](id3dxfile--createsaveobject.md)           | 建立儲存物件，該物件將用來將資料儲存至 x.x 檔案。<br/>                                          |
| [**RegisterEnumTemplates**](id3dxfile--registerenumtemplates.md) | 在給定 [**ID3DXFileEnumObject**](id3dxfileenumobject.md) 列舉物件的情況下註冊自訂範本。<br/> |
| [**RegisterTemplates**](id3dxfile--registertemplates.md)         | 註冊自訂範本。<br/>                                                                                 |



 

## <a name="remarks"></a>備註

ID3DXFile 物件也包含本機範本存放區。 此本機儲存體只能使用 [**ID3DXFile：： RegisterEnumTemplates**](id3dxfile--registerenumtemplates.md) 和 [**ID3DXFile：： RegisterTemplates**](id3dxfile--registertemplates.md) 方法新增至。

使用 [**ID3DXFile：： CreateEnumObject**](id3dxfile--createenumobject.md)和 [**ID3DXFile：： CreateSaveObject**](id3dxfile--createsaveobject.md)建立的 [**ID3DXFileEnumObject**](id3dxfileenumobject.md)和 [**ID3DXFileSaveObject**](id3dxfilesaveobject.md)物件也會利用父 ID3DXFile 物件的範本存放區。

ID3DXFile 介面是藉由呼叫 [**D3DXFileCreate**](d3dxfilecreate.md) 函數來取得。

ID3DXFile 介面 (GUID) 的全域唯一識別碼為 IID \_ ID3DXFile。

LPD3DXFILE 型別定義為 ID3DXFile 介面的指標。


```
typedef interface ID3DXFile *LPD3DXFILE;
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

 

 
