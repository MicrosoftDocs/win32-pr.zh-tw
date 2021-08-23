---
title: 'glLoadName 函式 (Gl) '
description: GlLoadName 函式會將名稱載入至名稱堆疊。
ms.assetid: 8d7d582b-3743-401e-af71-28034e49f3c2
keywords:
- glLoadName 函式 OpenGL
topic_type:
- apiref
api_name:
- glLoadName
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f362862d2d4b57c43e12e522e2dac1767bbd36d88bda4ce3fb27f3c525fb3ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119520388"
---
# <a name="glloadname-function"></a>glLoadName 函式

**GlLoadName** 函式會將名稱載入至名稱堆疊。

## <a name="syntax"></a>語法


```C++
void WINAPI glLoadName(
   GLuint name
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*name* 
</dt> <dd>

將取代名稱堆疊頂端值的名稱。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="error-codes"></a>錯誤碼

[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。



| 名稱                                                                                                  | 意義                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ 不正確 \_ 操作**</dt> </dl> | 當名稱堆疊為空白時，就會呼叫函數。<br/>                                                                    |
| <dl> <dt>**GL \_ 不正確 \_ 操作**</dt> </dl> | 呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。<br/> |



## <a name="remarks"></a>備註

**GlLoadName** 函式會導致 *名稱* 取代名稱堆疊頂端的值，這一開始是空的。 在選取模式期間，會使用名稱堆疊來允許唯一識別的轉譯命令集。 它包含一組排序的不帶正負號的整數。

當轉譯模式並非 GL 選取時，名稱堆疊一律是空的 \_ 。 當轉譯模式不是 GL 時，會忽略 **glLoadName** 的呼叫 \_ 。

下列函式會取出與 **glLoadName** 相關的資訊：

[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 名稱 \_ STACK \_ 深度的 glGet

具有引數 GL \_ 最大 \_ 名稱 \_ STACK \_ 深度的 glGet

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                              |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                    |
| 標頭<br/>                   | <dl> <dt>Gl</dt> </dl>         |
| 程式庫<br/>                  | <dl> <dt>Opengl32 .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glInitNames**](glinitnames.md)
</dt> <dt>

[**glPushName**](glpushname.md)
</dt> <dt>

[**glRenderMode**](glrendermode.md)
</dt> <dt>

[**glSelectBuffer**](glselectbuffer.md)
</dt> </dl>

 

 





