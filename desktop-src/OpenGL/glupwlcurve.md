---
title: 'gluPwlCurve 函式 (X.glu 隊) '
description: GluPwlCurve 函式描述分段線性非統一的有理數 B 曲線 (NURBS) 修剪曲線。
ms.assetid: 3d08e7e8-dfdf-447c-9795-bd73299412b5
keywords:
- gluPwlCurve 函式 OpenGL
topic_type:
- apiref
api_name:
- gluPwlCurve
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d15c532659811c7e499369e7798c4b1ceaf842bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106999818"
---
# <a name="glupwlcurve-function"></a>gluPwlCurve 函式

**GluPwlCurve** 函式描述分段線性非統一的有理數 B 曲線 ([NURBS](using-nurbs-curves-and-surfaces.md)) 修剪曲線。

## <a name="syntax"></a>語法


```C++
void WINAPI gluPwlCurve(
   GLUnurbs *nobj,
   GLint    count,
   GLfloat  *array,
   GLint    stride,
   GLenum   type
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*nobj* 
</dt> <dd>

使用 [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)) 建立的 NURBS 物件 (。

</dd> <dt>

*計數* 
</dt> <dd>

曲線上的點數目。

</dd> <dt>

*array* 
</dt> <dd>

包含曲線點的陣列。

</dd> <dt>

*大步* 
</dt> <dd>

位移 (在曲線上的點之間) 的單精確度浮點值數目。

</dd> <dt>

*type* 
</dt> <dd>

曲線的類型。 必須是 X.GLU 隊 \_ MAP1 \_ trim \_ 2 或 x.glu 隊 \_ MAP1 \_ TRIM \_ 3。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="remarks"></a>備註

**GluPwlCurve** 函數描述 NURBS 表面的分段線性修剪曲線。 分段線性曲線包含要修剪的 NURBS 介面之參數空間中的點座標清單。 這些點會與線段連接以形成曲線。 如果曲線是實際曲線的近似值，則點應該夠接近，如此一來，所產生的路徑就會顯示在應用程式中所使用的解析度上。

如果 *type* 是 X.glu 隊 \_ MAP1 \_ TRIM \_ 2，則會以二維 (*u* 和 *v*) 參數空間來描述曲線。 如果它是 X.GLU 隊 \_ MAP1 \_ TRIM \_ 3，則會以二維同質 (*u*、 *v* 和 *w*) 參數空間來描述曲線。 如需修剪曲線的詳細資訊，請參閱 [**gluBeginTrim**](glubegintrim.md)。

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
</dt> </dl>

 

 





