---
title: 'gluTessEndPolygon 函式 (X.glu 隊) '
description: 'GluTessBeginPolygon 和 gluTessEndPolygon 函數會分隔多邊形描述。 |gluTessEndPolygon 函式 (X.glu 隊) '
ms.assetid: c9ae2075-59d7-4c1a-b720-0aa05954525c
keywords:
- gluTessEndPolygon 函式 OpenGL
topic_type:
- apiref
api_name:
- gluTessEndPolygon
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8353f9176e5bdb64dc0e3cd21bd42735e57b541b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106989152"
---
# <a name="glutessendpolygon-function"></a>gluTessEndPolygon 函式

[**GluTessBeginPolygon**](glutessbeginpolygon.md)和 **gluTessEndPolygon** 函數會分隔多邊形描述。

## <a name="syntax"></a>語法


```C++
void WINAPI gluTessEndPolygon(
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

[**GluTessBeginPolygon**](glutessbeginpolygon.md)和 **gluTessEndPolygon** 函數會分隔 nonconvex 多邊形的定義。 在每個 **gluTessBeginPolygon**  /  **gluTessEndPolygon** 配對中，包含一或多個對 [**gluTessBeginContour**](glutessbegincontour.md)的呼叫。 在每個分佈中，有零或多個 [**gluTessVertex**](glutessvertex.md)呼叫。 頂點會指定封閉的輪廓 (每個分佈的最後一個頂點都會自動連結至第一個) 。

*多邊形 \_ 資料* 參數是程式設計人員定義資料結構的指標。 如果指定了適當的回呼 (請參閱 [*gluTessCallback*](glutess.md)) ，此指標會傳回給回呼函式或函式，讓它成為儲存每個多邊形資訊的便利方式。

當您呼叫 **gluTessEndPolygon** 時，多邊形會是鑲嵌，而產生的三角形會透過回呼來描述。 如需回呼函數的描述，請參閱 [*gluTessCallback*](glutess.md)。

## <a name="examples"></a>範例

以下說明具有三角形孔的四邊形：

``` syntax
gluTessBeginPolygon(tobj, NULL); 
  gluTessBeginContour(tobj); 
    gluTessVertex(tobj, v1, v1); 
    gluTessVertex(tobj, v2, v2); 
    gluTessVertex(tobj, v3, v3); 
    gluTessVertex(tobj, v4, v4); 
  gluTessEndContour(tobj); 
  gluTessBeginContour(tobj); 
    gluTessVertex(tobj, v5, v5); 
    gluTessVertex(tobj, v6, v6); 
    gluTessVertex(tobj, v7, v7); 
  gluTessEndContour(tobj); 
gluTessEndPolygon(tobj);
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

[**gluTessBeginContour**](glutessbegincontour.md)
</dt> <dt>

[*gluTessCallback*](glutess.md)
</dt> <dt>

[**gluTessEndContour**](glutessendcontour.md)
</dt> <dt>

[**gluTessNormal**](glutessnormal.md)
</dt> <dt>

[**gluTessProperty**](glutessproperty.md)
</dt> <dt>

[**gluTessVertex**](glutessvertex.md)
</dt> </dl>

 

 





