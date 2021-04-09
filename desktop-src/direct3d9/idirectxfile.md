---
description: 應用程式會使用 IDirectXFile 介面的方法來建立 IDirectXFileEnumObject 和 IDirectXFileSaveObject 介面的實例，以及註冊範本。 已取代。
ms.assetid: c4e800dc-72a9-4b91-9c89-ee76764b1bb9
title: 'IDirectXFile 介面 (DXFile .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFile
api_type:
- COM
api_location:
- d3dxof.lib
- d3dxof.dll
ms.openlocfilehash: 0a1e084108580277432aaeb61086b43a97dbd9f7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103854060"
---
# <a name="idirectxfile-interface"></a>IDirectXFile 介面

應用程式會使用 IDirectXFile 介面的方法來建立 [**IDirectXFileEnumObject**](idirectxfileenumobject.md) 和 [**IDirectXFileSaveObject**](idirectxfilesaveobject.md) 介面的實例，以及註冊範本。 已取代。

## <a name="members"></a>成員

**IDirectXFile** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。 **IDirectXFile** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IDirectXFile** 介面具有這些方法。



| 方法                                                       | 描述                                          |
|:-------------------------------------------------------------|:-----------------------------------------------------|
| [**CreateEnumObject**](idirectxfile--createenumobject.md)   | 建立列舉值物件。 已取代。<br/> |
| [**CreateSaveObject**](idirectxfile--createsaveobject.md)   | 建立儲存物件。 已取代。<br/>        |
| [**RegisterTemplates**](idirectxfile--registertemplates.md) | 註冊自訂範本。 已取代。<br/>   |



 

## <a name="remarks"></a>備註

IDirectXFile 介面 (GUID) 的全域唯一識別碼為 IID \_ IDirectXFile。

IDirectXFile 介面是藉由呼叫 [**DirectXFileCreate**](directxfilecreate.md) 函數來取得。

LPDIRECTXFILE 型別定義為這個介面的指標。


```
typedef interface IDirectXFile *LPDIRECTXFILE;
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

 

 
