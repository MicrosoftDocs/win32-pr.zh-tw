---
title: 'glPassThrough 函式 (Gl) '
description: GlPassThrough 函式會在意見緩衝區中放置標記。
ms.assetid: 14664ac6-eb25-46ae-86d8-7ece31df103f
keywords:
- glPassThrough 函式 OpenGL
topic_type:
- apiref
api_name:
- glPassThrough
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5edf1b0fb2dbda1ef1e0a2c4b9ab67b8e7e6305998a8f5a6de9c461e4e148bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118615415"
---
# <a name="glpassthrough-function"></a>glPassThrough 函式

**GlPassThrough** 函式會在意見緩衝區中放置標記。

## <a name="syntax"></a>語法


```C++
void WINAPI glPassThrough(
   GLfloat token
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*token* 
</dt> <dd>

要放置在意見緩衝區中的標記值。 它會以下列唯一的識別值表示。



| 值                                                                                                                                                                                   | 意義                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_PASS_THROUGH_TOKEN"></span><span id="gl_pass_through_token"></span><dl> <dt>**GL \_ \_ 通過 \_ 權杖**</dt> </dl> | 會維護 **glPassThrough** 命令與圖形基本規格的相對順序。<br/> |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="error-codes"></a>錯誤碼

[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。



| 名稱                                                                                                  | 意義                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ 不正確 \_ 操作**</dt> </dl> | 呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。<br/> |



## <a name="remarks"></a>備註

意見反應是藉由使用 GL 意見反應來呼叫 [**glRenderMode**](glrendermode.md) ，而選取的 OpenGL 轉譯模式 \_ 。 當 OpenGL 處於意見反應模式時，柵格化不會產生任何圖元。 相反地，會將已點陣化之基本資訊的相關資訊，由 OpenGL 送回至應用程式。 如需意見反應緩衝區和其中的值的描述，請參閱 [**glFeedbackBuffer**](glfeedbackbuffer.md) 。

**GlPassThrough** 函式會在意見反應模式中執行時，在意見緩衝區中插入使用者定義標記。 *Token* 參數的傳回方式就如同它是基本。

如果 OpenGL 不在意見反應模式中，則會忽略 **glPassThrough** 函式。

下列函式會抓取 **glPassThrough** 的相關資訊：

[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 轉譯 \_ 模式的 glGet

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

[**glFeedbackBuffer**](glfeedbackbuffer.md)
</dt> <dt>

[**glRenderMode**](glrendermode.md)
</dt> </dl>

 

 





