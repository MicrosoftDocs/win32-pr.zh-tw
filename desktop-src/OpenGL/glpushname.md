---
title: 'glPushName 函式 (Gl) '
description: 'GlPushName 和 glPopName 函式會推送並彈出名稱堆疊。 |glPushName 函式 (Gl) '
ms.assetid: e4319018-42c0-4567-b67f-31dbdbee9b13
keywords:
- glPushName 函式 OpenGL
topic_type:
- apiref
api_name:
- glPushName
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ff783a108f5cb1ac34141c6c57f47b16e23531a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106988554"
---
# <a name="glpushname-function"></a>glPushName 函式

**GlPushName** 和 [**glPopName**](glpopname.md)函式會推送並彈出名稱堆疊。

## <a name="syntax"></a>語法


```C++
void WINAPI glPushName(
   GLuint name
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*name* 
</dt> <dd>

將推送至名稱堆疊的名稱。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="error-codes"></a>錯誤碼

[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。



| Name                                                                                                  | 意義                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ 堆疊 \_ 溢位**</dt> </dl>    | 當目前的矩陣堆疊已滿時，就會呼叫函數。<br/>                                                           |
| <dl> <dt>**GL \_ 不正確 \_ 操作**</dt> </dl> | 呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。<br/> |



## <a name="remarks"></a>備註

**GlPushName** 函式會將名稱推送至名稱堆疊，這一開始是空的。 [**GlPopName**](glpopname.md)函式會將一個名稱從堆疊的最上方彈出。 在選取模式期間，會使用名稱堆疊來允許唯一識別的轉譯命令集。 它包含一組排序的不帶正負號的整數。

當轉譯模式並非 GL 選取時，名稱堆疊一律是空的 \_ 。 當轉譯模式不是 GL 時，會忽略 **glPushName** 或 [**glPopName**](glpopname.md) 的呼叫 \_ 。

下列函式會取出 **glPushName** 和 [**glPopName**](glpopname.md)的相關資訊：

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

 

 





