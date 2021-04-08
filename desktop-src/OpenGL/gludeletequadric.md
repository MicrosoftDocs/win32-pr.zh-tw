---
title: 'gluDeleteQuadric 函式 (X.glu 隊) '
description: GluDeleteQuadric 函式會終結 quadric 物件。
ms.assetid: 09efd887-0fe8-4a56-bc6f-2177a4930035
keywords:
- gluDeleteQuadric 函式 OpenGL
topic_type:
- apiref
api_name:
- gluDeleteQuadric
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b5ee85e943cd958e394efb191932393d228d948
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686090"
---
# <a name="gludeletequadric-function"></a>gluDeleteQuadric 函式

**GluDeleteQuadric** 函式會終結 quadric 物件。

## <a name="syntax"></a>語法


```C++
void WINAPI gluDeleteQuadric(
   GLUquadricObj *state
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*state* 
</dt> <dd>

要終結 (使用 [**gluNewQuadric**](glunewquadric.md)) 所建立的 quadric 物件。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="remarks"></a>備註

**GluDeleteQuadric** 函式會終結 quadric 物件，並釋放其使用的任何記憶體。 在您呼叫 **gluDeleteQuadric** 之後，就無法再使用 *狀態* 。

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

[**gluNewQuadric**](glunewquadric.md)
</dt> </dl>

 

 





