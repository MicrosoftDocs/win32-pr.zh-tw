---
title: 'gluNurbsSurface 函式 (X.glu 隊) '
description: GluNurbsSurface 函式會定義非統一有理數 B 曲線 (NURBS) 介面的形狀。
ms.assetid: ee86376c-26ba-49a9-b0b0-4ca936b6614b
keywords:
- gluNurbsSurface 函式 OpenGL
topic_type:
- apiref
api_name:
- gluNurbsSurface
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50f56232ac891cbdfba18195741d875ecc5436112772ed4fa665903374e96602
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119554188"
---
# <a name="glunurbssurface-function"></a>gluNurbsSurface 函式

**GluNurbsSurface** 函式會定義非統一有理數 B 曲線 ([NURBS](using-nurbs-curves-and-surfaces.md)) 介面的形狀。

## <a name="syntax"></a>語法


```C++
void WINAPI gluNurbsSurface(
   GLUnurbs *nobj,
   GLint    sknot_count,
   float    *sknot,
   GLint    tknot_count,
   GLfloat  *tknot,
   GLint    s_stride,
   GLint    t_stride,
   GLfloat  *ctlarray,
   GLint    sorder,
   GLint    torder,
   GLenum   type
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*nobj* 
</dt> <dd>

使用 [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)) 建立的 NURBS 物件 (。

</dd> <dt>

*sknot \_ 計數* 
</dt> <dd>

參數 *u* 方向中的節點數目。

</dd> <dt>

*sknot* 
</dt> <dd>

*Sknot \_ 計數* 的陣列會以參數 *u* 方向 nondecreasing 節點值。

</dd> <dt>

*tknot \_ 計數* 
</dt> <dd>

參數化 *v* 方向中的節點數目。

</dd> <dt>

*tknot* 
</dt> <dd>

*Tknot \_ 計數* 的陣列會 nondecreasing 在參數化 *v* 方向中的節點值。

</dd> <dt>

*s \_ stride* 
</dt> <dd>

位移 (為 *ctlarray* 中參數 *u* 方向的連續控制點之間的單一 precisionfloating 點) 值。

</dd> <dt>

*t \_ stride* 
</dt> <dd>

單一 precisionfloating 點值中的位移 (在 *ctlarray* 的參數式 *v* 方向的連續控制點之間) 。

</dd> <dt>

*ctlarray* 
</dt> <dd>

陣列，包含 NURBS 表面的控制點。 參數 *u* 和 *v* 方向中連續控制點之間的位移，會由 *s \_ stride* 和 *t \_ stride* 提供。

</dd> <dt>

*sorder* 
</dt> <dd>

NURBS 介面在參數 *u* 方向的順序。 順序比角度多一點，因此以 *u* 為立方的表面有 *u* 階4。

</dd> <dt>

*torder* 
</dt> <dd>

NURBS 介面在參數化 *v* 方向的順序。 順序比角度多一點，因此 *v* 中的三個平面的 *v* 順序為4。

</dd> <dt>

*type* 
</dt> <dd>

介面的類型。 *類型* 參數可以是任何有效的二維評估工具類型 (例如 GL \_ list.map2 \_ 頂點 \_ 3 或 gl \_ list.map2 \_ COLOR \_ 4) 。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="remarks"></a>備註

在 NURBS 介面定義中使用 **gluNurbsSurface** ，以描述在任何修剪) 之前 (的 nurbs 介面圖形。 若要標記 NURBS 介面定義的開頭，請使用 [**gluBeginSurface**](glubeginsurface.md) 函數。 若要標記 NURBS 介面定義的結尾，請使用 [**gluEndSurface**](gluendsurface.md) 函數。 只在 NURBS 介面定義中呼叫 **gluNurbsSurface** 。

您可以將位置、材質和色彩座標與介面產生關聯，方法是在 **gluBeginSurface** gluEndSurface 配對之間呈現個別的 **gluNurbsSurface** /  。 在單一 **gluBeginSurface** / **gluEndSurface** 配對中，您只能對 **gluNurbsSurface** 進行色彩、位置和材質資料的單一呼叫。 只需進行一次呼叫，就能描述 (*類型* 為 gl \_ list.map2 \_ 頂點 \_ 3 或 gl \_ list.map2 \_ 頂點 \_ 4) 的介面位置。

您可以使用 GluNurbsCurve 和 GluPwlCurve 函式，在對 [**gluBeginTrim**](glubegintrim.md)和 [**gluEndTrim**](gluendtrim.md)的呼叫之間使用 [](glunurbscurve.md)和 [](glupwlcurve.md)函數來修剪 NURBS 介面。

在 *u* 方向中有 *sknot \_ 計數* 節點的 **gluNurbsSurface** ，以及訂單 *sorder* 和 *torder* 的 *v* 方向中的 *tknot \_ 計數* 節點，必須具有 (*sknot \_ count*  - *sorder*) multipied by (*tknot \_ count*  - *torder*) 控制點。

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

[**gluBeginSurface**](glubeginsurface.md)
</dt> <dt>

[**gluBeginTrim**](glubegintrim.md)
</dt> <dt>

[**gluEndSurface**](gluendsurface.md)
</dt> <dt>

[**gluEndTrim**](gluendtrim.md)
</dt> <dt>

[**gluNewNurbsRenderer**](glunewnurbsrenderer.md)
</dt> <dt>

[**gluNurbsCurve**](glunurbscurve.md)
</dt> <dt>

[**gluPwlCurve**](glupwlcurve.md)
</dt> </dl>

 

 





