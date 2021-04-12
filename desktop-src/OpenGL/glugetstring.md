---
title: 'gluGetString 函式 (X.glu 隊) '
description: GluGetString 函式會取得描述 X.GLU 隊版本號碼或支援之 X.GLU 隊延伸模組呼叫的字串。
ms.assetid: e6d9ce03-3218-4145-8bb5-3989afe62436
keywords:
- gluGetString 函式 OpenGL
topic_type:
- apiref
api_name:
- gluGetString
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 574ed93c9c6f8d1f964e38ee14541d57bd5c34da
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384461"
---
# <a name="glugetstring-function"></a>gluGetString 函式

**GluGetString** 函式會取得描述 x.glu 隊版本號碼或支援之 x.glu 隊延伸模組呼叫的字串。

## <a name="syntax"></a>語法


```C++
const GLubyte* WINAPI gluGetString(
   GLenum name
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*name* 
</dt> <dd>

X.GLU 隊 (X.GLU 隊版本的版本號碼 \_) 或可用的廠商專屬延伸模組呼叫 (X.glu 隊 \_ 延伸模組) 。

</dd> </dl>

## <a name="remarks"></a>備註

**GluGetString** 函式會傳回靜態、以 null 終止之字串的指標。 當 *name* 為 x.glu 隊 \_ 版本時，傳回的字串是代表 x.glu 隊版本號碼的值。 版本號碼的格式如下所示：

``` syntax
<version number><space><vendor-specific information> 
(for example, "1.2.11 Microsoft Windows")
```

版本號碼的格式為「主要 \_ 號碼. 次要 \_ 號碼」或「主要號碼號碼。 \_ \_ 發行號碼」 \_ 。 廠商專屬的資訊是選擇性的，且格式和內容取決於執行。

當 *name* 為 x.glu 隊 \_ EXTENSIONS 時，傳回的字串會包含以空格分隔的支援 x.glu 隊延伸模組名稱清單。 傳回之名稱清單的格式如下所示：

``` syntax
<extension_name><space><extension_name><space> . . .
(for example, "GLU_NURBS GL_TESSELATION")
```

延伸模組名稱不能包含任何空格。

**GluGetString** 函數適用于 x.glu 隊1.1 版或更新版本。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                           |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                 |
| 標頭<br/>                   | <dl> <dt>X.glu 隊。h</dt> </dl>     |
| 程式庫<br/>                  | <dl> <dt>Glu32 .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Glu32.dll</dt> </dl> |



 

 





