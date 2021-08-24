---
title: 'glRenderMode 函式 (Gl) '
description: GlRenderMode 函式會設定點陣化模式。
ms.assetid: bcbc3bba-c552-425b-8284-6cadff0c9f56
keywords:
- glRenderMode 函式 OpenGL
topic_type:
- apiref
api_name:
- glRenderMode
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93eb3c7e2d7f4a6d261632e0f010cf0e1c7a2410a5a8364a6cf1fd65f36ada99
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119777928"
---
# <a name="glrendermode-function"></a>glRenderMode 函式

**GlRenderMode** 函式會設定點陣化模式。

## <a name="syntax"></a>語法


```C++
GLint WINAPI glRenderMode(
   GLenum mode
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*mode* 
</dt> <dd>

點陣化模式。 接受下列三個值。 預設值為 GL \_ RENDER。



| 值                                                                                                                                                   | 意義                                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_RENDER"></span><span id="gl_render"></span><dl> <dt>**GL \_ 轉譯**</dt> </dl>       | 轉譯模式。 基本專案會進行柵格化，並產生會寫入畫面格緩衝區中的圖元片段。 這是一般模式，也是預設模式。<br/>                                                                                                                                                                                                      |
| <span id="GL_SELECT"></span><span id="gl_select"></span><dl> <dt>**GL \_ 選取**</dt> </dl>       | 選取模式。 不會產生任何圖元片段，也不會對畫面格緩衝區內容進行任何變更。 相反地，當轉譯模式為 GL 轉譯時，所要繪製的基本名稱記錄 \_ ，會在選取的緩衝區中傳回， (在輸入選取模式之前，請參閱 [**glSelectBuffer**](glselectbuffer.md)) 。<br/>               |
| <span id="GL_FEEDBACK"></span><span id="gl_feedback"></span><dl> <dt>**GL \_ 意見反應**</dt> </dl> | 意見反應模式。 不會產生任何圖元片段，也不會對畫面格緩衝區內容進行任何變更。 相反地，已繪製之頂點的座標和屬性 \_ 會在意見反應緩衝區中傳回，該緩衝區必須建立， (在輸入意見反應模式之前，請參閱 [**glFeedbackBuffer**](glfeedbackbuffer.md)) 。<br/> |



 

</dd> </dl>

## <a name="error-codes"></a>錯誤碼

[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。



| 名稱                                                                                                  | 意義                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ 無效 \_ 列舉**</dt> </dl>      | *模式* 不是三個接受的值之一。<br/>                                                                                     |
| <dl> <dt>**GL \_ 不正確 \_ 操作**</dt> </dl> | 呼叫函式時，會使用引數 GL SELECT 來呼叫該函式， \_ 然後至少呼叫 [**glSelectBuffer**](glselectbuffer.md) 一次。<br/>       |
| <dl> <dt>**GL \_ 不正確 \_ 操作**</dt> </dl> | 在 \_ 呼叫至少一次 [**glBeedbackBuffer**](glfeedbackbuffer.md) 之前，會使用引數 GL 回饋來呼叫函數。<br/> |
| <dl> <dt>**GL \_ 不正確 \_ 操作**</dt> </dl> | 呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。<br/>       |



## <a name="remarks"></a>備註

**GlRenderMode** 函式會採用一個引數，也就是可採用上述三個預先定義值之一的 *模式*。

**GlRenderMode** 函式的傳回值是由在呼叫 **glRenderMode** 時的轉譯模式來決定，而不是透過 *模式* 來決定。 針對三種轉譯模式傳回的值如下所示。



| 值        | 意義                                                                 |
|--------------|-------------------------------------------------------------------------|
| GL \_ 轉譯   | 零個。                                                                   |
| GL \_ 選取   | 傳送至選取緩衝區的點擊記錄數。             |
| GL \_ 意見反應 |  (不是頂點的值數目) 傳送至意見緩衝區。 |



 

如需有關選取專案和意見反應作業的詳細資訊，請參閱 [**glSelectBuffer**](glselectbuffer.md) 和 [**glFeedbackBuffer**](glfeedbackbuffer.md) 。

如果產生錯誤，不論目前的轉譯模式為何， **glRenderMode** 都會傳回零。

下列函式會抓取 **glRenderMode** 的相關資訊：

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

[**glInitNames**](glinitnames.md)
</dt> <dt>

[**glLoadName**](glloadname.md)
</dt> <dt>

[**glPassThrough**](glpassthrough.md)
</dt> <dt>

[**glPushName**](glpushname.md)
</dt> <dt>

[**glSelectBuffer**](glselectbuffer.md)
</dt> </dl>

 

 





