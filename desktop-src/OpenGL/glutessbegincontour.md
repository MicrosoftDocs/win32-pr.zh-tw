---
title: 'gluTessBeginContour 函式 (X.glu 隊) '
description: 'GluTessBeginContour 和 gluTessEndContour 函式會分隔分佈描述。 |gluTessBeginContour 函式 (X.glu 隊) '
ms.assetid: 4008ce9c-86e7-4b24-9bda-5915f469596a
keywords:
- gluTessBeginContour 函式 OpenGL
topic_type:
- apiref
api_name:
- gluTessBeginContour
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2edc46eb3aa1be6b37c9276bcfd1c2b951162722689b0d0affc358a71119736f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118937469"
---
# <a name="glutessbegincontour-function"></a>gluTessBeginContour 函式

**GluTessBeginContour** 和 [**gluTessEndContour**](glutessendcontour.md)函式會分隔分佈描述。

## <a name="syntax"></a>語法


```C++
void WINAPI gluTessBeginContour(
   GLUtesselator *tess
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*苔 絲* 
</dt> <dd>

使用 [**gluNewTess**](glunewtess.md)) 建立的鑲嵌式物件 (。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="remarks"></a>備註

**GluTessBeginContour** 和 [**gluTessEndPolygon**](glutessendpolygon.md)函數會分隔多邊形輪廓的定義。 在每個 **gluTessBeginContour** / **gluTessEndPolygon** 配對中，可能會有零或多個對 [**gluTessVertex**](glutessvertex.md)的呼叫。 頂點會指定封閉的輪廓 (每個分佈的最後一個頂點都會自動連結至第一個) 。 您只能在 [**gluTessBeginPolygon**](glutessbeginpolygon.md)和 **GluTessEndPolygon** 之間呼叫 **gluTessBeginContour** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                           |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                 |
| 標頭<br/>                   | <dl> <dt>X.glu 隊。h</dt> </dl>     |
| 程式庫<br/>                  | <dl> <dt>Glu32 .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Glu32.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**gluNewTess**](glunewtess.md)
</dt> <dt>

[**gluTessBeginPolygon**](glutessbeginpolygon.md)
</dt> <dt>

[*gluTessCallback*](glutess.md)
</dt> <dt>

[**gluTessEndPolygon**](glutessendpolygon.md)
</dt> <dt>

[**gluTessNormal**](glutessnormal.md)
</dt> <dt>

[**gluTessProperty**](glutessproperty.md)
</dt> <dt>

[**gluTessVertex**](glutessvertex.md)
</dt> </dl>

 

 





