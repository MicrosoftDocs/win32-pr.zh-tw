---
title: 'glPopName 函式 (Gl) '
description: 'GlPushName 和 glPopName 函式會推送並彈出名稱堆疊。 |glPopName 函式 (Gl) '
ms.assetid: ee741188-b275-4839-a89d-4d988c547d07
keywords:
- glPopName 函式 OpenGL
topic_type:
- apiref
api_name:
- glPopName
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe30aa09d401fc8ef35a3671e02a898776af26111ae0f8e31cd1f6ad3bff70b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119290168"
---
# <a name="glpopname-function"></a>glPopName 函式

[**GlPushName**](glpushname.md)和 **glPopName** 函式會推送並彈出名稱堆疊。

## <a name="syntax"></a>語法


```C++
void WINAPI glPopName(void);
```



## <a name="parameters"></a>參數

此函式沒有參數。

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="error-codes"></a>錯誤碼

[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。



| 名稱                                                                                                  | 意義                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ 堆疊 \_ 下溢**</dt> </dl>   | 當目前的矩陣堆疊只包含單一矩陣時，會呼叫此函式。<br/>                                     |
| <dl> <dt>**GL \_ 不正確 \_ 操作**</dt> </dl> | 呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。<br/> |



## <a name="remarks"></a>備註

[**GlPushName**](glpushname.md)函式會將名稱推送至名稱堆疊，這一開始是空的。 **GlPopName** 函式會將一個名稱從堆疊的最上方彈出。 在選取模式期間，會使用名稱堆疊來允許唯一識別的轉譯命令集。 它包含一組排序的不帶正負號的整數。

當轉譯模式並非 GL 選取時，名稱堆疊一律是空的 \_ 。 當轉譯模式不是 GL 時，會忽略 [**glPushName**](glpushname.md) 或 **glPopName** 的呼叫 \_ 。

下列函式會取出 [**glPushName**](glpushname.md) 和 **glPopName** 的相關資訊：

[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 名稱 \_ STACK \_ 深度的 glGet

[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 最大 \_ 名稱 \_ STACK \_ 深度的 glGet

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

[**glLoadName**](glloadname.md)
</dt> <dt>

[**glRenderMode**](glrendermode.md)
</dt> <dt>

[**glSelectBuffer**](glselectbuffer.md)
</dt> </dl>

 

 





