---
title: 'gluQuadricCallback 函式 (X.glu 隊) '
description: GluQuadricCallback 函數會定義 quadric 物件的回呼。
ms.assetid: 1f1e9fe9-7239-419c-92b6-af2534850ac5
keywords:
- gluQuadricCallback 函式 OpenGL
topic_type:
- apiref
api_name:
- gluQuadricCallback
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36ce32bf041a59f272b18ebe17916963c4e5fd8d208da9d739468c88b9286dfc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119488788"
---
# <a name="gluquadriccallback-function"></a>gluQuadricCallback 函式

**GluQuadricCallback** 函數會定義 quadric 物件的回呼。

## <a name="syntax"></a>語法


```C++
void WINAPI gluQuadricCallback(
   GLUquadric *qobj,
   GLenum     which,
   void (CALLBACK *fn)()
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*qobj* 
</dt> <dd>

Quadric 物件 (使用 [**gluNewQuadric**](glunewquadric.md)) 建立。

</dd> <dt>

*頻率* 
</dt> <dd>

要定義的回呼。 唯一有效的值為 X.GLU 隊 \_ 錯誤。



| 值                                                                                                                                             | 意義                                                                                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GLU_ERROR"></span><span id="glu_error"></span><dl> <dt>**X.GLU 隊 \_ 錯誤**</dt> </dl> | 遇到錯誤時，會呼叫 **gluQuadricCallback** 函數。 其單一引數的類型為 **GLenum**，它會指出發生的特定錯誤。 描述這些錯誤的字元字串可以使用 [**gluErrorString**](gluerrorstring.md) 呼叫來抓取。<br/> |



 

</dd> <dt>

*Fn* 
</dt> <dd>

要呼叫的函式。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="remarks"></a>備註

使用 **gluQuadricCallback** 來定義 quadric 物件所要使用的新回呼。 如果已定義指定的回呼，則會予以取代。 如果 *fn* 為 **Null**，則會清除任何現有的回呼。

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

[**gluNewQuadric**](glunewquadric.md)
</dt> </dl>

 

 





