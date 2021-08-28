---
title: 'gluNurbsCallback 函式 (X.glu 隊) '
description: GluNurbsCallback 函式會定義非統一有理數 B 曲線 (NURBS) 物件的回呼。
ms.assetid: 1e9afc00-57c6-459e-a9fc-463f45df2084
keywords:
- gluNurbsCallback 函式 OpenGL
topic_type:
- apiref
api_name:
- gluNurbsCallback
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1da7ebc999d44911cb345b051213a12865e608db7b7fe66e33eb1bb567ef7a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119519498"
---
# <a name="glunurbscallback-function"></a>gluNurbsCallback 函式

**GluNurbsCallback** 函式會定義非統一有理數 B 曲線 ([NURBS](using-nurbs-curves-and-surfaces.md)) 物件的回呼。

## <a name="syntax"></a>語法


```C++
void WINAPI gluNurbsCallback(
   GLUnurbs *nobj,
   GLenum   which,
   void (CALLBACK *fn)()
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*nobj* 
</dt> <dd>

使用 [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)) 建立的 NURBS 物件 (。

</dd> <dt>

*頻率* 
</dt> <dd>

要定義的回呼。 唯一有效的值為 X.GLU 隊 \_ 錯誤。 X.GLU 隊錯誤的意義 \_ 表示當發生錯誤時，會呼叫錯誤函式。 其單一引數的類型為 **GLenum**，它會指出發生的特定錯誤。 X.GLU 隊 \_ nurbs \_ ERROR1 透過 X.glu 隊 \_ NURBS ERROR37，是唯一的37錯誤 \_ 。 描述這些錯誤的字元字串可使用 [**gluErrorString**](gluerrorstring.md)來加以取出。

</dd> <dt>

*Fn* 
</dt> <dd>

回呼函數的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="remarks"></a>備註

使用 **gluNurbsCallback** 來定義由 NURBS 物件使用的回呼。 如果已定義指定的回呼，則會予以取代。 如果 *fn* 為 **Null**，則會清除任何現有的回呼。

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

[**gluErrorString**](gluerrorstring.md)
</dt> <dt>

[**gluNewNurbsRenderer**](glunewnurbsrenderer.md)
</dt> </dl>

 

 





