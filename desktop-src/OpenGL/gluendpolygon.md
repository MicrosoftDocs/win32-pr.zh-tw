---
title: 'gluEndPolygon 函式 (X.glu 隊) '
description: 'GluBeginPolygon 和 gluEndPolygon 函數會分隔多邊形描述。 |gluEndPolygon 函式 (X.glu 隊) '
ms.assetid: fdb8cc73-c6c3-4377-aa5b-36a79791e7a9
keywords:
- gluEndPolygon 函式 OpenGL
topic_type:
- apiref
api_name:
- gluEndPolygon
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbf69bfb16f9c83462bbe6b53c86f319b3d09623
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106993819"
---
# <a name="gluendpolygon-function"></a>gluEndPolygon 函式

\[**GluEndPolygon** 函式已過時，而且只為了回溯相容性而提供。 **GluEndPolygon** 函式會對應到 **gluTessEndPolygon** ，後面接著 **gluTessEndContour**。\]

[**GluBeginPolygon**](glubeginpolygon.md)和 **gluEndPolygon** 函數會分隔多邊形描述。

## <a name="syntax"></a>語法


```C++
void gluEndPolygon(
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

使用 [**gluBeginPolygon**](glubeginpolygon.md) 和 **gluEndPolygon** 來分隔 nonconvex 多邊形的定義。

1.  呼叫 **gluBeginPolygon**。
2.  藉由呼叫每個頂點的 [**gluTessVertex**](glutessvertex.md) 和 [**gluNextContour**](glunextcontour.md) 來開始每個新的分佈，以定義多邊形的輪廓。
3.  呼叫 **gluEndPolygon** 以發出定義的結尾。

    一旦呼叫 **gluEndPolygon** ，就會鑲嵌多邊形，並透過回呼來描述所產生的三角形。 如需回呼函數的描述，請參閱 [*gluTessCallback*](glutess.md)。

## <a name="examples"></a>範例

下列範例說明具有三角形孔的四邊形：

``` syntax
gluBeginPolygon(tess); 
    gluTessVertex(tess, v1, v1); 
    gluTessVertex(tess, v2, v2); 
    gluTessVertex(tess, v3, v3); 
    gluTessVertex(tess, v4, v4); 
gluNextContour(tess, GLU_INTERIOR); 
    gluTessVertex(tess, v5, v5); 
    gluTessVertex(tess, v6, v6); 
    gluTessVertex(tess, v7, v7); 
gluEndPolygon(tess);
```

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

[**gluNextContour**](glunextcontour.md)
</dt> <dt>

[**gluTessBeginContour**](glutessbegincontour.md)
</dt> <dt>

[**gluTessBeginPolygon**](glutessbeginpolygon.md)
</dt> <dt>

[*gluTessCallback*](glutess.md)
</dt> <dt>

[**gluTessVertex**](glutessvertex.md)
</dt> </dl>

 

 





