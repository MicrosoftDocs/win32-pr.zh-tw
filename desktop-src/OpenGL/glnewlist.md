---
title: 'glNewList 函式 (Gl) '
description: 'GlNewList 和 glEndList 函數會建立或取代顯示清單。 |glNewList 函式 (Gl) '
ms.assetid: 9c6556d4-855f-4cba-94cc-27b5f1e4607a
keywords:
- glNewList 函式 OpenGL
topic_type:
- apiref
api_name:
- glNewList
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0103baa9786cdfed0d6e999021453e30da5083571c9a2c9054da701977a9493f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119741338"
---
# <a name="glnewlist-function"></a>glNewList 函式

**GlNewList** 和 [**glEndList**](glendlist.md)函數會建立或取代顯示清單。

## <a name="syntax"></a>語法


```C++
void WINAPI glNewList(
   GLuint list,
   GLenum mode
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*list* 
</dt> <dd>

顯示清單名稱。

</dd> <dt>

*mode* 
</dt> <dd>

編譯模式。 接受下列值。



| 值                                                                                                                                                                                      | 意義                                                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span id="GL_COMPILE"></span><span id="gl_compile"></span><dl> <dt>**GL \_ 編譯**</dt> </dl>                                       | 命令只會進行編譯。<br/>                                     |
| <span id="GL_COMPILE_AND_EXECUTE"></span><span id="gl_compile_and_execute"></span><dl> <dt>**GL \_ 編譯 \_ 和 \_ 執行**</dt> </dl> | 命令會在編譯到顯示清單中時執行。<br/> |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="error-codes"></a>錯誤碼

[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。



| 名稱                                                                                                  | 意義                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ 無效 \_ 值**</dt> </dl>     | *清單* 為零。<br/>                                                                                                           |
| <dl> <dt>**GL \_ 無效 \_ 列舉**</dt> </dl>      | *模式* 不是可接受的值。<br/>                                                                                          |
| <dl> <dt>**GL \_ 不正確 \_ 操作**</dt> </dl> | 呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。<br/> |



## <a name="remarks"></a>備註

顯示清單是已儲存以供後續執行的 OpenGL 命令群組。 顯示清單會以 **glNewList** 來建立。 所有後續的命令都會依發出的順序，放在顯示清單中，直到呼叫 **glEndList** 為止。

**GlNewList** 函式有兩個參數。 第一個參數 *list* 是一個正整數，會成為顯示清單的唯一名稱。 您可以使用 [**glGenLists**](glgenlists.md) 來建立和保留名稱，並測試 [**glIsList**](glislist.md)的唯一性。 第二個參數（ *模式*）是可採用上述兩個值之一的符號常數。

某些命令不會編譯到顯示清單中，但是會立即執行，而不論顯示清單模式為何。 這些命令有 [**glColorPointer**](glcolorpointer.md)、 [**glDeleteLists**](gldeletelists.md)、 [**glDisableClientState**](gldisableclientstate.md)、 [**glEdgeFlagPointer**](gledgeflagpointer.md)、 [**glEnableClientState**](glenableclientstate.md)、 [**glFeedbackBuffer**](glfeedbackbuffer.md)、 [**glFinish**](glfinish.md)、 [**glFlush**](glflush.md)、 [**glGenLists**](glgenlists.md)、 [**glIndexPointer**](glindexpointer.md)、 [**glInterleavedArrays**](glinterleavedarrays.md)、 [**glIsEnabled、glIsList**](glisenabled.md) [**、glNormalPointer**](glislist.md) [**、glPopClientAttrib**](glnormalpointer.md) [**、glPixelStore**](glpopclientattrib.md) [**、glPushClientAttrib**](glpixelstore-functions.md) [**、glReadPixels**](glpushclientattrib.md) [**、glRenderMode**](glreadpixels.md)、 [**glSelectBuffer、**](glselectbuffer.md)glTexCoordPointer、glVertexPointer [**、glGet、**](glrendermode.md) [**、、**](gltexcoordpointer.md) [**，以及**](glvertexpointer.md)所有 [](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)常式。

同樣地，當[](glteximage1d.md)第一個引數是 GL [](glteximage2d.md) \_ proxy \_ 材質 \_ 2d 或 gl \_ proxy \_ 材質 \_ 1d 時，glTexImage2D 和 glTexImage1D 會立即執行，而不會編譯成顯示清單。

當遇到 **glEndList** 函式時，會藉由將清單與 [ **glNewList** ] 命令) 中指定的 [唯一名稱] (*清單* 產生關聯，來完成顯示清單定義。 如果已有名稱 *清單* 的顯示清單，則只會在呼叫 **glEndList** 時加以取代。

[**GlCallList**](glcalllist.md)和 [**glCallLists**](glcalllists.md)函數可以輸入到顯示清單中。 **GlCallList** 或 **glCallLists** 所執行的顯示清單或清單中的命令不會包含在所建立的顯示清單中，即使清單建立模式是 GL \_ 編譯 \_ 和執行 \_ 也一樣。

下列函式會抓取 **glNewList** 的相關資訊：

[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 矩陣 \_ 模式的 glGet

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

[**glCallList**](glcalllist.md)
</dt> <dt>

[**glCallLists**](glcalllists.md)
</dt> <dt>

[**glDeleteLists**](gldeletelists.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glEndList**](glendlist.md)
</dt> <dt>

[**glGenLists**](glgenlists.md)
</dt> <dt>

[**glIsList**](glislist.md)
</dt> </dl>

 

 





