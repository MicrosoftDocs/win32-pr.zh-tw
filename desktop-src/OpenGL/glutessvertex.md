---
title: 'gluTessVertex 函式 (X.glu 隊) '
description: GluTessVertex 函數會指定多邊形上的頂點。
ms.assetid: 9c555b32-5257-4eeb-9323-ccad59591097
keywords:
- gluTessVertex 函式 OpenGL
topic_type:
- apiref
api_name:
- gluTessVertex
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51b3b1dd666fd965e7b6536a20a794481c534ed3e42594017093ee161a067e15
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119488418"
---
# <a name="glutessvertex-function"></a>gluTessVertex 函式

**GluTessVertex** 函數會指定多邊形上的頂點。

## <a name="syntax"></a>語法


```C++
void WINAPI gluTessVertex(
   GLUtesselator *tess,
   GLdouble      coords[3],
   void          *data
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*苔 絲* 
</dt> <dd>

使用 [**gluNewTess**](glunewtess.md)) 建立的鑲嵌式物件 (。

</dd> <dt>

*coords* 
</dt> <dd>

頂點的位置。

</dd> <dt>

*data* 
</dt> <dd>

使用頂點回呼傳回給程式的指標 (如 [*gluTessCallback*](glutess.md)) 所指定。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="remarks"></a>備註

**GluTessVertex** 函式會在使用者所定義的多邊形上描述頂點。 後續的 **gluTessVertex** 呼叫會描述封閉的輪廓。 例如，若要描述四邊形，請呼叫 **gluTessVertex** 四次。 您只能呼叫 [**gluTessBeginContour**](glutessbegincontour.md)和 [**GluTessEndContour**](glutessendcontour.md)之間的 **gluTessVertex** 。

*資料* 參數通常會指向包含頂點位置的結構，以及其他每個頂點的屬性，例如色彩和一般。 在鑲嵌之後，會透過 X.GLU 隊頂點回呼將指標傳回給程式 \_ gluTessCallback (請參閱[](glutess.md)) 。

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

[**gluTessBeginContour**](glutessbegincontour.md)
</dt> <dt>

[**gluTessBeginPolygon**](glubeginpolygon.md)
</dt> <dt>

[*gluTessCallback*](glutess.md)
</dt> <dt>

[**gluTessEndContour**](glutessendcontour.md)
</dt> <dt>

[**gluTessNormal**](glutessnormal.md)
</dt> <dt>

[**gluTessProperty**](glutessproperty.md)
</dt> </dl>

 

 





