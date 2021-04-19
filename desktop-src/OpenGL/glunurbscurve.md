---
title: 'gluNurbsCurve 函式 (X.glu 隊) '
description: GluNurbsCurve 函式會定義非統一有理數 B 曲線 (NURBS) 曲線的形狀。
ms.assetid: d03064a5-26f5-487f-877f-3748646bcb2f
keywords:
- gluNurbsCurve 函式 OpenGL
topic_type:
- apiref
api_name:
- gluNurbsCurve
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c38e3d5fe35e994afa4b5d8b91c4244573132c5b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967726"
---
# <a name="glunurbscurve-function"></a>gluNurbsCurve 函式

**GluNurbsCurve** 函式會定義非統一有理數 B 曲線 ([NURBS](using-nurbs-curves-and-surfaces.md)) 曲線的形狀。

## <a name="syntax"></a>語法


```C++
void WINAPI gluNurbsCurve(
   GLUnurbs *nobj,
   GLint    nknots,
   GLfloat  *knot,
   GLint    stride,
   GLfloat  *ctlarray,
   GLint    order,
   GLenum   type
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*nobj* 
</dt> <dd>

使用 [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)) 建立的 NURBS 物件 (。

</dd> <dt>

*nknots* 
</dt> <dd>

*節點* 中的節點數目。 *Nknots* 參數等於控制點的數目加上順序。

</dd> <dt>

*結* 
</dt> <dd>

*Nknots* nondecreasing 節點值的陣列。

</dd> <dt>

*大步* 
</dt> <dd>

位移 (為連續曲線控制點之間) 的單精確度浮點值數目。

</dd> <dt>

*ctlarray* 
</dt> <dd>

指向控制點陣列的指標。 座標必須與 *類型* 一致。

</dd> <dt>

*order* 
</dt> <dd>

NURBS 曲線的順序。 *Order* 參數等於度數 + 1;因此，三曲線的順序為4。

</dd> <dt>

*type* 
</dt> <dd>

曲線的型別。 如果此曲線定義在 [**gluBeginCurve**](glubegincurve.md) / [**gluEndCurve**](gluendcurve.md)配對內，則該類型可以是任何有效的一維評估工具類型 (例如 GL \_ MAP1 \_ 頂點 \_ 3 或 gl \_ MAP1 \_ COLOR \_ 4) 。 在 [**gluBeginTrim**](glubegintrim.md) / [**gluEndTrim**](gluendtrim.md)配對之間，唯一有效的類型為 x.glu 隊 \_ MAP1 \_ TRIM \_ 2 和 x.glu 隊 \_ MAP1 \_ TRIM \_ 3。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="remarks"></a>備註

當 **gluNurbsCurve** 出現在 **gluBeginCurve** / **gluEndCurve** 配對之間時，它會描述要呈現的曲線。 您可以建立位置、材質和色彩座標的關聯，方法是將它們呈現為 **gluBeginCurve** / **gluEndCurve** 配對之間個別的 gluNurbsCurve。 請勿對單一 **gluBeginCurve** gluEndCurve 配對內的色彩、位置和材質資料進行一個以上的 **gluNurbsCurve** 呼叫 /  。 進行精確的呼叫，以描述曲線的位置 (一 *種* gl \_ MAP1 \_ 頂點 \_ 3 或 gl \_ MAP1 \_ 頂點 \_ 4) 。

當 **gluNurbsCurve** 出現在 [**gluBeginTrim**](glubegintrim.md) / [**gluEndTrim**](gluendtrim.md)配對之間時，它會描述 NURBS 表面上的修剪曲線。 如果 *type* 是 X.glu 隊 \_ MAP1 \_ TRIM \_ 2，則會以二維 (*u* 和 *v*) 參數空間來描述曲線。 如果它是 X.GLU 隊 \_ MAP1 \_ TRIM \_ 3，則會以二維同質 (*u*、 *v* 和 *w*) 參數空間來描述曲線。 如需修剪曲線的詳細討論，請參閱 **gluBeginTrim**。

## <a name="examples"></a>範例

下列函式會以法線呈現有紋理的 NURBS 曲線：

``` syntax
gluBeginCurve(nobj); 
    gluNurbsCurve(nobj, ..., GL_MAP1_TEXTURE_COORD_2); 
    gluNurbsCurve(nobj, ..., GL_MAP1_NORMAL); 
    gluNurbsCurve(nobj, ..., GL_MAP1_VERTEX_4);  
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

[**gluBeginCurve**](glubegincurve.md)
</dt> <dt>

[**gluBeginTrim**](glubegintrim.md)
</dt> <dt>

[**gluEndCurve**](gluendcurve.md)
</dt> <dt>

[**gluEndTrim**](gluendtrim.md)
</dt> <dt>

[**gluNewNurbsRenderer**](glunewnurbsrenderer.md)
</dt> <dt>

[**gluPwlCurve**](glupwlcurve.md)
</dt> </dl>

 

 





