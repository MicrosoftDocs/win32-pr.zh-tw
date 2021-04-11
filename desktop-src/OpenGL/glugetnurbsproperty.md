---
title: 'gluGetNurbsProperty 函式 (X.glu 隊) '
description: GluGetNurbsProperty 函式會取得非統一的有理 B 曲線 (NURBS) 屬性。
ms.assetid: 7dbc75a0-d04e-4794-b3dd-a602addf9dfa
keywords:
- gluGetNurbsProperty 函式 OpenGL
topic_type:
- apiref
api_name:
- gluGetNurbsProperty
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 583da688e3495ebc2eb9d6f71972658c6426469c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094375"
---
# <a name="glugetnurbsproperty-function"></a>gluGetNurbsProperty 函式

**GluGetNurbsProperty** 函式會取得非統一的有理 B 曲線 ([NURBS](using-nurbs-curves-and-surfaces.md)) 屬性。

## <a name="syntax"></a>語法


```C++
void WINAPI gluGetNurbsProperty(
   GLUnurbs *nobj,
   GLenum   property,
   GLfloat  *value
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*nobj* 
</dt> <dd>

使用 [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)) 建立的 NURBS 物件 (。

</dd> <dt>

*property* 
</dt> <dd>

要取出其值的屬性。 下列值有效： X.GLU 隊 \_ 取樣 \_ 容錯、X.glu 隊 \_ 顯示 \_ 模式、X.glu 隊 \_ 剔除、X.GLU 隊 \_ 自動 \_ 載入 \_ 矩陣、X.GLU 隊 \_ 參數 \_ 容錯、X.glu 隊 \_ 取樣 \_ 方法、x.glu 隊 \_ U \_ 步驟和 x.glu 隊 \_ V \_ 步驟。

</dd> <dt>

*value* 
</dt> <dd>

要在其中寫入已命名屬性值之位置的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="remarks"></a>備註

使用 **gluGetNurbsProperty** 來取出儲存在 NURBS 物件中的屬性。 這些屬性會影響 NURBS 曲線和表面的呈現方式。 如需 NURBS 屬性的詳細資訊，請參閱 [**gluNurbsProperty**](glunurbsproperty.md)。

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

[**gluNewNurbsRenderer**](glunewnurbsrenderer.md)
</dt> <dt>

[**gluNurbsProperty**](glunurbsproperty.md)
</dt> </dl>

 

 





