---
description: 應用程式會使用 IDirectXFileSaveObject 介面的方法來建立資料物件，以及儲存範本和資料物件。
ms.assetid: 7948a7d2-b150-45cf-a1fc-5dca21d74770
title: 'IDirectXFileSaveObject 介面 (DXFile .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileSaveObject
api_type:
- COM
api_location:
- d3dxof.lib
- d3dxof.dll
ms.openlocfilehash: 4be69b10037381d4b06466d52483427b6d40499a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106982005"
---
# <a name="idirectxfilesaveobject-interface"></a>IDirectXFileSaveObject 介面

應用程式會使用 IDirectXFileSaveObject 介面的方法來建立資料物件，以及儲存範本和資料物件。 請注意，每個檔案都不需要範本。 例如，您可以將所有範本放入單一 Microsoft DirectX 檔案中，而不是在每個 DirectX 檔案中複製它們。 已取代。

## <a name="members"></a>成員

**IDirectXFileSaveObject** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。 **IDirectXFileSaveObject** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IDirectXFileSaveObject** 介面具有這些方法。



| 方法                                                               | 描述                                                                    |
|:---------------------------------------------------------------------|:-------------------------------------------------------------------------------|
| [**CreateDataObject**](idirectxfilesaveobject--createdataobject.md) | 建立資料物件。 已取代。<br/>                                  |
| [**SaveData**](idirectxfilesaveobject--savedata.md)                 | 將資料物件和其子系儲存至 DirectX 檔案。 已取代。<br/> |
| [**SaveTemplates**](idirectxfilesaveobject--savetemplates.md)       | 將範本儲存至 DirectX 檔案。 已取代。<br/>                      |



 

## <a name="remarks"></a>備註

IDirectXFileSaveObject 介面 (GUID) 的全域唯一識別碼為 **IID \_ IDirectXFileSaveObject**。

**IDirectXFileSaveObject** 介面的取得方式是呼叫 [**IDirectXFile：： CreateSaveObject**](idirectxfile--createsaveobject.md)方法。

**LPDIRECTXFILESAVEOBJECT** 型別定義為這個介面的指標。


```
typedef interface IDirectXFileSaveObject *LPDIRECTXFILESAVEOBJECT;
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

 

 
