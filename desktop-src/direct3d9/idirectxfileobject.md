---
description: 應用程式會使用 IDirectXFileObject 介面的方法，來取得 Microsoft DirectX 檔案物件的相關資訊。 已取代。
ms.assetid: 015d2c4e-4a25-40da-b88a-bad0c4e20e09
title: 'IDirectXFileObject 介面 (DXFile .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileObject
api_type:
- COM
api_location:
- d3dxof.lib
- d3dxof.dll
ms.openlocfilehash: 3aa0ffffb8766707841fa0a4a5ec54fe0db9caf1d86b885afc36bffa5f8352d8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119951298"
---
# <a name="idirectxfileobject-interface"></a>IDirectXFileObject 介面

應用程式會使用 IDirectXFileObject 介面的方法，來取得 Microsoft DirectX 檔案物件的相關資訊。 已取代。

## <a name="members"></a>成員

**IDirectXFileObject** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。 **IDirectXFileObject** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IDirectXFileObject** 介面具有這些方法。



| 方法                                         | 描述                                                                                   |
|:-----------------------------------------------|:----------------------------------------------------------------------------------------------|
| [**GetId**](idirectxfileobject--getid.md)     | 抓取識別 DirectX 檔案物件的 GUID 指標。 已取代。<br/> |
| [**GetName**](idirectxfileobject--getname.md) | 捕獲 DirectX 檔案物件名稱的指標。 已取代。<br/>                   |



 

## <a name="remarks"></a>備註

IDirectXFileObject 介面的 GUID 是 IID \_ IDirectXFileObject。

LPDIRECTXFILEOBJECT 型別定義為這個介面的指標。


```
typedef interface IDirectXFileObject *LPDIRECTXFILEOBJECT;
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

 

 
