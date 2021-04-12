---
title: 'gluGetTessProperty 函式 (X.glu 隊) '
description: GluGetTessProperty 函式會取得鑲嵌式物件屬性。
ms.assetid: 6aa565d8-2257-4259-a959-b7d806a7ed96
keywords:
- gluGetTessProperty 函式 OpenGL
topic_type:
- apiref
api_name:
- gluGetTessProperty
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 482f32b227dbcf0c2a62405e344aa719bb4b9e17
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384458"
---
# <a name="glugettessproperty-function"></a>gluGetTessProperty 函式

**GluGetTessProperty** 函式會取得鑲嵌式物件屬性。

## <a name="syntax"></a>語法


```C++
void WINAPI gluGetTessProperty(
   GLUtesselator *tess,
   GLenum        which,
   GLdouble      *value
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*苔 絲* 
</dt> <dd>

使用 [**gluNewTess**](glunewtess.md)) 建立的鑲嵌式物件 (。

</dd> <dt>

*頻率* 
</dt> <dd>

要取出其值的屬性。 下列值有效： X.GLU 隊 \_ TESS \_ 繞組 \_ RULE、x.glu 隊 \_ TESS \_ 界限 \_ ，以及 x.glu 隊 \_ TESS \_ 容錯。

</dd> <dt>

*value* 
</dt> <dd>

要在其中寫入已命名屬性值之位置的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="remarks"></a>備註

使用 **gluGetTessProperty** 來取出鑲嵌物件中儲存的屬性。 這些屬性會影響鑲嵌式物件的解讀和轉譯方式。 如需屬性的內容和其用途的詳細資訊，請參閱 [**gluTessProperty**](glutessproperty.md)。

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

[**gluNewTess**](glunewtess.md)
</dt> <dt>

[**gluTessProperty**](glutessproperty.md)
</dt> </dl>

 

 





