---
title: 'gluErrorString 函式 (X.glu 隊) '
description: GluErrorString 函式會從 OpenGL 或 X.GLU 隊錯誤碼產生錯誤字串。 錯誤字串僅為 ANSI。
ms.assetid: 6d71a6d5-ac00-49f9-a56c-cfeeb88963eb
keywords:
- gluErrorString 函式 OpenGL
topic_type:
- apiref
api_name:
- gluErrorString
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0cdcfad0e2a943bf3a475317f32d37921878a8f8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685812"
---
# <a name="gluerrorstring-function"></a>gluErrorString 函式

**GluErrorString** 函式會從 OPENGL 或 x.glu 隊錯誤碼產生錯誤字串。 錯誤字串僅為 ANSI。

## <a name="syntax"></a>語法


```C++
const GLubyte* WINAPI gluErrorString(
   GLenum errCode
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*errCode* 
</dt> <dd>

OpenGL 或 X.GLU 隊錯誤碼。

</dd> </dl>

## <a name="remarks"></a>備註

**GluErrorString** 函式會從 OPENGL 或 x.glu 隊錯誤碼產生錯誤字串。 字串採用 ISO 拉丁1格式。 例如， **gluErrorString** (GL \_ 記憶體不足) 會傳回「 \_ \_ 記憶體不足」字串。

標準 X.GLU 隊錯誤碼為 X.GLU 隊 \_ 無效 \_ 的列舉、X.glu 隊 \_ 無效 \_ 的值，以及 x.glu 隊 \_ \_ 記憶體不足 \_ 。 某些其他 X.GLU 隊函數可以透過回呼傳回特製化的錯誤碼。 如需 OpenGL 錯誤碼清單，請參閱 [**glGetError**](glgeterror.md)。

**GluErrorString** 函式只會產生 ANSI 的錯誤字串。 可能的話，請使用 **gluErrorStringWIN**，允許 ANSI 或 Unicode 錯誤字串。 這可讓您更輕鬆地將程式當地語系化以與其他語言搭配使用。

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

[**glGetError**](glgeterror.md)
</dt> <dt>

[*gluNurbsCallback*](glunurbs.md)
</dt> <dt>

[*gluQuadricCallback*](gluquadric.md)
</dt> <dt>

[*gluTessCallback*](glutess.md)
</dt> </dl>

 

 





