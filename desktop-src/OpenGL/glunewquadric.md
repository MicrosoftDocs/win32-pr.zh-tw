---
title: 'gluNewQuadric 函式 (X.glu 隊) '
description: GluNewQuadric 函式會建立 quadric 物件。
ms.assetid: 5a4289bf-b57a-4c74-b0e3-b7536671e4df
keywords:
- gluNewQuadric 函式 OpenGL
topic_type:
- apiref
api_name:
- gluNewQuadric
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: affedc7dcebd2b7925449e22cc1b902e88d936f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934604"
---
# <a name="glunewquadric-function"></a>gluNewQuadric 函式

**GluNewQuadric** 函式會建立 quadric 物件。

## <a name="syntax"></a>語法


```C++
GLUquadric* WINAPI gluNewQuadric(void);
```



## <a name="parameters"></a>參數

此函式沒有參數。

## <a name="remarks"></a>備註

**GluNewQuadric** 函式會建立並傳回新 quadric 物件的指標。 呼叫 quadric 轉譯和控制函式時，請參考這個物件。 傳回值為0表示沒有足夠的記憶體可配置給物件。

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

[**gluCylinder**](glucylinder.md)
</dt> <dt>

[**gluDeleteQuadric**](gludeletequadric.md)
</dt> <dt>

[**gluDisk**](gludisk.md)
</dt> <dt>

[**gluPartialDisk**](glupartialdisk.md)
</dt> <dt>

[*gluQuadricCallback*](gluquadric.md)
</dt> <dt>

[**gluQuadricDrawStyle**](gluquadricdrawstyle.md)
</dt> <dt>

[**gluQuadricNormals**](gluquadricnormals.md)
</dt> <dt>

[**gluQuadricOrientation**](gluquadricorientation.md)
</dt> <dt>

[**gluQuadricTexture**](gluquadrictexture.md)
</dt> <dt>

[**gluSphere**](glusphere.md)
</dt> </dl>

 

 





