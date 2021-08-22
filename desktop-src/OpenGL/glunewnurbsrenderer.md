---
title: 'gluNewNurbsRenderer 函式 (X.glu 隊) '
description: GluNewNurbsRenderer 函式會建立非統一的有理 B 曲線 (NURBS) 物件。
ms.assetid: f47badb0-6b75-4bfd-9771-516668d9e255
keywords:
- gluNewNurbsRenderer 函式 OpenGL
topic_type:
- apiref
api_name:
- gluNewNurbsRenderer
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 089c1a88ac0fe9ac246efd435ae941ba5e66e2412595e4f5f96dc73e85e90478
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118937793"
---
# <a name="glunewnurbsrenderer-function"></a>gluNewNurbsRenderer 函式

**GluNewNurbsRenderer** 函式會建立非統一的有理 B 曲線 ([NURBS](using-nurbs-curves-and-surfaces.md)) 物件。

## <a name="syntax"></a>語法


```C++
GLUnurbs* WINAPI gluNewNurbsRenderer(void);
```



## <a name="parameters"></a>參數

此函式沒有參數。

## <a name="remarks"></a>備註

**GluNewNurbsRenderer** 函式會建立並傳回新的 NURBS 物件的指標。 呼叫 NURBS 轉譯和控制函式時，請參考這個物件。 傳回值為0表示沒有足夠的記憶體可配置給物件。

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

[**gluBeginSurface**](glubeginsurface.md)
</dt> <dt>

[**gluBeginTrim**](glubegintrim.md)
</dt> <dt>

[**gluDeleteNurbsRenderer**](gludeletenurbsrenderer.md)
</dt> <dt>

[*gluNurbsCallback*](glunurbs.md)
</dt> <dt>

[**gluNurbsProperty**](glunurbsproperty.md)
</dt> </dl>

 

 





