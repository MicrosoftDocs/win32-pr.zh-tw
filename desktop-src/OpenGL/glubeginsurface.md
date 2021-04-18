---
title: 'gluBeginSurface 函式 (X.glu 隊) '
description: 'GluBeginSurface 和 gluEndSurface 函式會分隔非統一的有理 B 曲線 (NURBS) 介面定義。 |gluBeginSurface 函式 (X.glu 隊) '
ms.assetid: 7189f05e-0c4d-4f82-8a82-a51fcc51b202
keywords:
- gluBeginSurface 函式 OpenGL
topic_type:
- apiref
api_name:
- gluBeginSurface
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7bbd09030290f78fac987a52cddd977a502dda06
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106976428"
---
# <a name="glubeginsurface-function"></a>gluBeginSurface 函式

**GluBeginSurface** 和 [**gluEndSurface**](gluendsurface.md)函式會分隔非統一的有理 B 曲線 ([NURBS](using-nurbs-curves-and-surfaces.md)) 介面定義。

## <a name="syntax"></a>語法


```C++
void WINAPI gluBeginSurface(
   GLUnurbs *nobj
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*nobj* 
</dt> <dd>

使用 [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)) 建立的 NURBS 物件 (。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="remarks"></a>備註

**GluBeginSurface** 和 **gluEndSurface** 函式會標記 NURBS 介面定義的開頭和結尾，這些定義是使用對 **gluNurbsSurface** 的呼叫所定義。

1.  呼叫 **gluBeginSurface** 以標記 NURBS 介面定義的開頭。
2.  對 **gluNurbsSurface** 進行一或多個呼叫，以定義介面的屬性。

    只有其中一個 **gluNurbsSurface** 呼叫必須具有 GL \_ list.map2 \_ 頂點 \_ 3 或 gl \_ list.map2 \_ 頂點 \_ 4 的介面類別型。

3.  若要標記 NURBS 介面定義的結尾，請呼叫 **gluEndSurface**。

[**GluBeginTrim**](glubegintrim.md)、 [**gluPwlCurve**](glupwlcurve.md)、 [**GLUNURBSCURVE**](glunurbscurve.md)和 [**gluEndTrim**](gluendtrim.md)函數支援 NURBS 表面的修剪。

使用 OpenGL 評估工具將 NURBS 表面轉譯為一組多邊形。 使用 [**glPushAttrib**](glpushattrib.md) (GL \_ EVAL \_ BIT) 和 [**glPopAttrib**](glpopattrib.md)在轉譯期間保留評估工具狀態。

## <a name="examples"></a>範例

下列函式會以法線呈現紋理的 NURBS 介面;材質座標和法線也會描述為 NURBS 表面：

``` syntax
gluBeginSurface(nobj); 
    gluNurbsSurface(nobj, . . ., GL_MAP2_TEXTURE_COORD_2); 
    gluNurbsSurface(nobj, . . ., GL_MAP2_NORMAL); 
    gluNurbsSurface(nobj, . . ., GL_MAP2_VERTEX_4); 
gluEndSurface(nobj);
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

[**gluBeginCurve**](glubegincurve.md)
</dt> <dt>

[**gluBeginTrim**](glubegintrim.md)
</dt> <dt>

[**gluNewNurbsRenderer**](glunewnurbsrenderer.md)
</dt> <dt>

[**gluNurbsCurve**](glunurbscurve.md)
</dt> <dt>

[**gluNurbsSurface**](glunurbssurface.md)
</dt> <dt>

[**gluPwlCurve**](glupwlcurve.md)
</dt> </dl>

 

 





