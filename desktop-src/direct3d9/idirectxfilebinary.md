---
description: 應用程式會使用 IDirectXFileBinary 介面的方法來讀取和取出二進位資料的相關資訊。 已取代。
ms.assetid: 43b20ab3-67b2-4717-ad90-0bf4ddb3207e
title: 'IDirectXFileBinary 介面 (DXFile .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileBinary
api_type:
- COM
api_location:
- d3dxof.lib
- d3dxof.dll
ms.openlocfilehash: 46e0da3a0cb03d3769e7888706a48fbf00786471afed285ce54c629285ac158c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118292407"
---
# <a name="idirectxfilebinary-interface"></a>IDirectXFileBinary 介面

應用程式會使用 IDirectXFileBinary 介面的方法來讀取和取出二進位資料的相關資訊。 已取代。

## <a name="members"></a>成員

**IDirectXFileBinary** 介面繼承自 [**IDirectXFileObject**](idirectxfileobject.md)。 **IDirectXFileBinary** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IDirectXFileBinary** 介面具有這些方法。



| 方法                                                 | 描述                                                                                                 |
|:-------------------------------------------------------|:------------------------------------------------------------------------------------------------------------|
| [**GetMimeType**](idirectxfilebinary--getmimetype.md) | 抓取多用途網際網路郵件延伸 (MIME) 類型的二進位資料。 已取代。<br/> |
| [**GetSize**](idirectxfilebinary--getsize.md)         | 捕獲二進位資料的大小。 已取代。<br/>                                               |
| [**讀**](idirectxfilebinary--read.md)               | 讀取二進位資料。 已取代。<br/>                                                               |



 

## <a name="remarks"></a>備註

IDirectXFileBinary 介面的 GUID 是 IID \_ IDirectXFileBinary。

LPDIRECTXFileBinary 型別定義為這個介面的指標。


```
typedef interface IDirectXFileBinary *LPDIRECTXFILEBINARY;
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

 

 




