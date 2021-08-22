---
title: 'gluBeginCurve 函式 (X.glu 隊) '
description: 'GluBeginCurve 和 gluEndCurve 函式會分隔非統一的有理數 B 曲線 (NURBS) 曲線定義。 |gluBeginCurve 函式 (X.glu 隊) '
ms.assetid: f7f2e765-1a07-4faa-940c-9cb957dd54d4
keywords:
- gluBeginCurve 函式 OpenGL
topic_type:
- apiref
api_name:
- gluBeginCurve
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 171c6ce95acf7592fcb2c3badccfeb9f2c5d68413f963f7b5043ec63502ee720
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119489738"
---
# <a name="glubegincurve-function"></a>gluBeginCurve 函式

**GluBeginCurve** 和 [**gluEndCurve**](gluendcurve.md)函式會分隔非統一的有理數 B 曲線 ([NURBS](using-nurbs-curves-and-surfaces.md)) 曲線定義。

## <a name="syntax"></a>語法


```C++
void WINAPI gluBeginCurve(
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

使用 **gluBeginCurve** 來標記 NURBS 曲線定義的開頭。 呼叫 **gluBeginCurve** 之後，請對 [**gluNurbsCurve**](glunurbscurve.md) 進行一或多個呼叫，以定義曲線的屬性。 只有其中一個 **gluNurbsCurve** 呼叫必須有 GL \_ MAP1 \_ 頂點 \_ 3 或 gl \_ MAP1 \_ 頂點 \_ 4 的曲線類型。 若要標記 NURBS 曲線定義的結尾，請呼叫 [**gluEndCurve**](gluendcurve.md)。

OpenGL 評估工具是用來將 NURBS 曲線轉譯成一連串的線段。 使用 [**glPushAttrib**](glpushattrib.md) (GL \_ EVAL \_ BIT) 和 [**glPopAttrib**](glpopattrib.md)轉譯時，會保留評估工具狀態。 如需這些呼叫保留之狀態的確切資訊，請參閱 **glPushAttrib**。

## <a name="examples"></a>範例

下列函式會以法線呈現有紋理的 NURBS 曲線;紋理座標和法線也會指定為 NURBS 曲線：

``` syntax
gluBeginCurve(nobj); 
gluNurbsCurve(nobj, . . ., GL_MAP1_TEXTURE_COORD_2); 
gluNurbsCurve(nobj, . . ., GL_MAP1_NORMAL); 
gluNurbsCurve(nobj, . . ., GL_MAP1_VERTEX_4);  
gluEndCurve(nobj);
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

[**glPushAttrib**](glpushattrib.md)
</dt> <dt>

[**gluBeginSurface**](glubeginsurface.md)
</dt> <dt>

[**gluBeginTrim**](glubegintrim.md)
</dt> <dt>

[**gluNewNurbsRenderer**](glunewnurbsrenderer.md)
</dt> <dt>

[**gluNurbsCurve**](glunurbscurve.md)
</dt> </dl>

 

 





