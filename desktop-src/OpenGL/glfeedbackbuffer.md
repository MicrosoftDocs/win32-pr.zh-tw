---
title: 'glFeedbackBuffer 函式 (Gl) '
description: GlFeedbackBuffer 函式會控制意見反應模式。
ms.assetid: fe3773a7-c264-4d49-8f90-1f2319f9af4f
keywords:
- glFeedbackBuffer 函式 OpenGL
topic_type:
- apiref
api_name:
- glFeedbackBuffer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e64b232db640d41ca9a1e1f75d6ab766597d6511
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968177"
---
# <a name="glfeedbackbuffer-function"></a>glFeedbackBuffer 函式

**GlFeedbackBuffer** 函式會控制意見反應模式。

## <a name="syntax"></a>語法


```C++
void WINAPI glFeedbackBuffer(
   GLsizei size,
   GLenum  type,
   GLfloat *buffer
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*size* 
</dt> <dd>

可以寫入至 *緩衝區* 的最大值數目。

</dd> <dt>

*type* 
</dt> <dd>

符號常數，描述將針對每個頂點傳回的資訊。 接受下列符號常數： GL \_ 2d、gl \_ 3D、gl \_ 3D \_ 色彩、gl \_ 3D \_ 色彩 \_ 材質，以及 gl \_ 4d \_ 色彩 \_ 材質。

</dd> <dt>

*緩衝區* 
</dt> <dd>

傳回意見反應資料。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="error-codes"></a>錯誤碼

[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。



| Name                                                                                                  | 意義                                                                                                                                                                                                                |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ 無效 \_ 列舉**</dt> </dl>      | *類型* 不是可接受的值。<br/>                                                                                                                                                                           |
| <dl> <dt>**GL \_ 無效 \_ 列舉**</dt> </dl>      | *大小* 為負數。<br/>                                                                                                                                                                                        |
| <dl> <dt>**GL \_ 不正確 \_ 操作**</dt> </dl> | 當轉譯模式為 GL 意見反應時呼叫 **glFeedbackBuffer** \_ ，或 [](glrendermode.md)在 \_ 至少呼叫 **glFeedbackBuffer** 一次之前，使用引數 GL 回饋來呼叫 glRenderMode。<br/> |
| <dl> <dt>**GL \_ 不正確 \_ 操作**</dt> </dl> | 呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。<br/>                                                                                  |



## <a name="remarks"></a>備註

**GlFeedbackBuffer** 函式會控制意見反應。 意見反應（例如選取專案）是 OpenGL 模式。 您可以透過使用 GL 意見反應來呼叫 [**glRenderMode**](glrendermode.md) 來選取模式 \_ 。 當 OpenGL 處於意見反應模式時，柵格化不會產生任何圖元。 相反地，會將已進行柵格化之基本資訊的相關資訊，使用 OpenGL 送回至應用程式。

**GlFeedbackBuffer** 函數有三個引數：

-   *緩衝區* 是指向放置意見反應資訊之浮點值陣列的指標。
-   *大小* 指出陣列的大小。
-   *類型* 是一個符號常數，描述針對每個頂點回送回的資訊。

您必須藉由呼叫 **glRenderMode** 與引數 GL 意見反應) ，在啟用意見反應模式 (之前發出 **glFeedbackBuffer** \_ 。 設定 GL \_ 意見反應但未建立意見緩衝區，或在 OpenGL 處於意見反應模式時呼叫 **glFeedbackBuffer** ，是一項錯誤。

使用 GL 意見反應以外的參數值來呼叫 [**glRenderMode**](glrendermode.md) ，以將 OpenGL 從意見反應模式中取出 \_ 。 當您在 OpenGL 處於意見反應模式時這麼做時， **glRenderMode** 會傳回回饋陣列中所放置的專案數目。 傳回的值永遠不會超過 *大小*。 如果意見反應資料所需的空間超過 *緩衝區* 可用的空間， **glRenderMode** 會傳回負數值。

在意見反應模式中，每個要進行柵格化的基本物件都會產生一個值區塊，這些值會複製到意見陣列中。 如果這樣做會導致專案數超過最大值，則 **glFeedbackBuffer** 會部分寫入區塊，以便填滿陣列 (如果所有) 都沒有剩餘的空間，並設定溢位旗標。 每個區塊都會以表示基本類型的程式碼開頭，後面接著描述基本頂點和相關資料的值。 **GlFeedbackBuffer** 函式也會寫入點陣圖和圖元矩形的專案。 在多邊形剔除和多邊形的 [**glPolygonMode**](glpolygonmode.md) 解釋之後發生意見反應，因此在意見緩衝區中不會傳回挑選的多邊形。 如果 OpenGL 執行會藉由執行此分解來轉譯多邊形，則會將具有三個以上邊緣的多邊形細分為三角形。

您可以使用 [**glPassThrough**](glpassthrough.md)，在意見緩衝區中插入標記。

以下是寫入意見緩衝區之值區塊的文法。 每個基本類型都會以唯一的識別值來表示，後面接著一些頂點。 多邊形專案包含一個整數值，指出接下來有多少頂點。 頂點會以數個浮點數值的形式送回（由型別決定 *）。* 在 RGBA 模式中，色彩會以四個值的形式送回，而在色彩索引模式中，則會以一個值

feedbackList < feedbackItem feedbackList \| feedbackItem

feedbackItem < 點 \| lineSegment \| 多邊形 \| 點陣圖 \| pixelRectangle \| passThru

點 < GL \_ 點 \_ 權杖頂點

lineSegment < GL \_ line \_ TOKEN 頂點頂點 \| GL \_ line \_ RESET \_ token 頂點頂點

多邊形 < GL \_ 多邊形 \_ TOKEN n polySpec

polySpec < \| polySpec 頂點頂點頂點頂點

< GL \_ 點陣圖 \_ 權杖頂點的點陣圖

pixelRectangle < GL \_ DRAW \_ 圖元 \_ token 頂點 \| \_ 複製 \_ 圖元 \_ token 頂點

passThru < GL \_ \_ 通過 \_ 權杖值

頂點 < 2d \| 3d \| 3dColor \| 3dColorTexture \| 4dColorTexture

2d < 值值

3d < 值值

3dColor < 值的值色彩

3dColorTexture < value 值 color tex

4dColorTexture < value 值 color tex

< rgba 索引的色彩 \|

rgba < 值值值

索引 < 值

tex < value value 值

*Value* 參數是浮點數，而 *n* 是一個浮點整數，可提供多邊形中的頂點數目。 以下是符號浮點數常數： GL \_ 點 \_ 權杖、gl \_ 線路 \_ 權杖、gl \_ 行 \_ 重設 \_ 權杖、gl \_ 多邊形 \_ 權杖、GL \_ 點陣圖 \_ 權杖、gl \_ 描繪 \_ 圖元 \_ 權杖、gl \_ 複製 \_ 圖元 \_ 權杖，以及 \_ 透過權杖的 gl 傳遞 \_ \_ 。 \_ \_ \_ 每當重設 LINE stipple 模式時，就會傳回 GL 行重設權杖。 以頂點傳回的資料取決於意見反應 *類型*。

下表提供 *類型* 和每個頂點的值數目之間的對應; *k* 在色彩索引模式中為1，而在 RGBA 模式中為4。



| 類型                   | 座標        | Color | 紋理 | 總值數目 |
|------------------------|--------------------|-------|---------|------------------------|
| GL \_ 2d                 | *x*、 *y*           |       |         | 2                      |
| GL \_ 3d                 | *x*、 *y*、 *z*      |       |         | 3                      |
| GL \_ 3d \_ 色彩          | *x*、 *y*、 *z*      | *K*   |         | 3 + *k*                |
| GL \_ 3d \_ 色彩 \_ 材質 | *x*、 *y*、 *z*、     | *K*   | 4       | 7 + *k*                |
| GL \_ 4d \_ 色彩 \_ 材質 | *x*、 *y*、 *z*、 *w* | *K*   | 4       | 8 + *k*                |



 

意見反應頂點座標是在視窗座標中，但 *w* 除外，其為裁剪座標。 如果已啟用光源，則意見反應色彩會是淺色。 如果已啟用材質座標產生，則會產生意見紋理座標。 材質矩陣一律會轉換它們。

在顯示清單中使用 **glFeedbackBuffer** 函式時，不會編譯到顯示清單中，而是會立即執行。

下列函式會抓取 **glFeedbackBuffer** 的相關資訊：

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

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glLineStipple**](gllinestipple.md)
</dt> <dt>

[**glPassThrough**](glpassthrough.md)
</dt> <dt>

[**glPolygonMode**](glpolygonmode.md)
</dt> <dt>

[**glRenderMode**](glrendermode.md)
</dt> <dt>

[**glSelectBuffer**](glselectbuffer.md)
</dt> </dl>

 

 





