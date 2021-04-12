---
title: 'glDepthFunc 函式 (Gl) '
description: GlDepthFunc 函數會指定用於深度緩衝區比較的值。
ms.assetid: 6ab8774a-8887-4c1e-b567-4492c0a60cf2
keywords:
- glDepthFunc 函式 OpenGL
topic_type:
- apiref
api_name:
- glDepthFunc
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4dec5130edb0b8ef30af1397be501fa9cd5d5744
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464725"
---
# <a name="gldepthfunc-function"></a>glDepthFunc 函式

**GlDepthFunc** 函數會指定用於深度緩衝區比較的值。

## <a name="syntax"></a>語法


```C++
void WINAPI glDepthFunc(
   GLenum func
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*func* 
</dt> <dd>

指定深度比較函數。 接受下列符號常數。



| 值                                                                                                                                                   | 意義                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span id="GL_NEVER"></span><span id="gl_never"></span><dl> <dt>**GL \_ 永不**</dt> </dl>          | 永遠不會通過。<br/>                                                                                  |
| <span id="GL_LESS"></span><span id="gl_less"></span><dl> <dt>**GL \_ LESS**</dt> </dl>             | 如果連入的 *z* 值小於儲存的 *z* 值，則傳遞。 這是預設值。<br/> |
| <span id="GL_LEQUAL"></span><span id="gl_lequal"></span><dl> <dt>**GL \_ LEQUAL**</dt> </dl>       | 如果連入的 z 值小於或等於儲存的 z 值，則傳遞。<br/>                    |
| <span id="GL_EQUAL"></span><span id="gl_equal"></span><dl> <dt>**GL \_ 相等**</dt> </dl>          | 如果連入的 z 值等於儲存的 z 值，則傳遞。<br/>                                 |
| <span id="GL_GREATER"></span><span id="gl_greater"></span><dl> <dt>**GL \_ 更高**</dt> </dl>    | 如果連入的 z 值大於儲存的 z 值，則傳遞。<br/>                             |
| <span id="GL_NOTEQUAL"></span><span id="gl_notequal"></span><dl> <dt>**GL \_ NOTEQUAL**</dt> </dl> | 如果連入的 z 值不等於儲存的 z 值，則傳遞。<br/>                             |
| <span id="GL_GEQUAL"></span><span id="gl_gequal"></span><dl> <dt>**GL \_ GEQUAL**</dt> </dl>       | 如果連入的 z 值大於或等於儲存的 z 值，則會傳遞。<br/>                 |
| <span id="GL_ALWAYS"></span><span id="gl_always"></span><dl> <dt>**GL \_ 一律**</dt> </dl>       | 一律傳遞。<br/>                                                                                 |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="error-codes"></a>錯誤碼

[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。



| Name                                                                                                  | 意義                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ 不正確 \_ 操作**</dt> </dl> | 呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。<br/> |



## <a name="remarks"></a>備註

**GlDepthFunc** 函式會指定用來比較每個內送圖元 *z* 值與深度緩衝區中的 *z* 值的函式。 只有在啟用深度測試時，才會執行比較。  (參閱[](glenable.md)具有引數 GL \_ 深度測試的 glEnable \_ 。 ) 

一開始，深度測試已停用。

下列函式會取出與 **glDepthFunc** 相關的資訊：

[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 深度 \_ FUNC 的 glGet

[](glisenabled.md)具有引數 GL \_ 深度 \_ 測試的 glIsEnabled

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

[**glDepthRange**](gldepthrange.md)
</dt> <dt>

[**glEnable**](glenable.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> </dl>

 

 





