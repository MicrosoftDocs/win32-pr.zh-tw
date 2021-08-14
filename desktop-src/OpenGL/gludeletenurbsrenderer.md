---
title: 'gluDeleteNurbsRenderer 函式 (X.glu 隊) '
description: GluDeleteNurbsRenderer 函式會終結非統一的有理 B 曲線 (NURBS) 物件。
ms.assetid: 77063dcb-90b8-47e4-8b00-e1c46cf4f712
keywords:
- gluDeleteNurbsRenderer 函式 OpenGL
topic_type:
- apiref
api_name:
- gluDeleteNurbsRenderer
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b114c6d67452468f3b8b92e443580d8d6f06c7df8bc1b6647916c210d204955
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118613015"
---
# <a name="gludeletenurbsrenderer-function"></a>gluDeleteNurbsRenderer 函式

**GluDeleteNurbsRenderer** 函式會終結非統一的有理 B 曲線 ([NURBS](using-nurbs-curves-and-surfaces.md)) 物件。

## <a name="syntax"></a>語法


```C++
void WINAPI gluDeleteNurbsRenderer(
   GLUnurbs *nobj
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*nobj* 
</dt> <dd>

要終結 (使用 **gluNewNurbsRenderer**) 所建立的 NURBS 物件。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="remarks"></a>備註

**GluDeleteNurbsRenderer** 函式會終結 NURBS 物件，並釋放其使用的任何記憶體。 當您呼叫 **gluDeleteNurbsRenderer** 之後，就無法再使用 *nobj* 。

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
</dt> </dl>

 

 





