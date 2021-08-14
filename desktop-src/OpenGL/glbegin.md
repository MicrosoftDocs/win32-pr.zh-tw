---
title: 'glBegin 函式 (Gl) '
description: 'GlBegin 和 glend 函式會分隔基本或類似基本類型群組的頂點。 |glBegin 函式 (Gl) '
ms.assetid: 8e8e98f8-89e8-40f5-89c1-492c9e3bbd74
keywords:
- glBegin 函式 OpenGL
topic_type:
- apiref
api_name:
- glBegin
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c497542e345b412bdc7955870405e6ee6cfe0503cee22f9320a031e835853345
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118361153"
---
# <a name="glbegin-function"></a>glBegin 函式

**GlBegin** 和 [**glend**](glend.md)函式會分隔基本或類似基本類型群組的頂點。

## <a name="syntax"></a>語法


```C++
void WINAPI glBegin(
   GLenum mode
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*mode* 
</dt> <dd>

將從 **glBegin** 和後續 [**glend**](glend.md)之間顯示的頂點建立的基本或基本。 以下是接受的符號常數及其意義：



| 值                                                                                                                                                                      | 意義                                                                                                                                                                                                                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_POINTS"></span><span id="gl_points"></span><dl> <dt>**GL \_ 點**</dt> </dl>                          | 將每個頂點視為單一點。 頂點 *n* 定義點 *n*。 會繪製 *N* 個點。<br/>                                                                                                                                                                                                                                                                                                      |
| <span id="GL_LINES"></span><span id="gl_lines"></span><dl> <dt>**GL \_ 行**</dt> </dl>                             | 將每一對頂點視為獨立的線段。 頂點 *2n-1* 和 *2n* 定義第 *n* 行。 會繪製 *N/2* 行。<br/>                                                                                                                                                                                                                                                                |
| <span id="GL_LINE_STRIP"></span><span id="gl_line_strip"></span><dl> <dt>**GL \_ 行 \_ 帶**</dt> </dl>             | 從第一個頂點到最後一個頂點，繪製一組連接的線段。 頂點 *n* 和 *n + 1* 定義行 *n*。 會繪製 *n-1* 行。<br/>                                                                                                                                                                                                                                                   |
| <span id="GL_LINE_LOOP"></span><span id="gl_line_loop"></span><dl> <dt>**GL \_ 線路 \_ 迴圈**</dt> </dl>                | 繪製從第一個頂點到最後一個頂點的已連接線段群組，然後回到第一個頂點。 頂點 *n* 和 *n + 1* 定義行 *n*。 但是，最後一行是由頂點 *N* 和 *1* 所定義。 會繪製 *N* 行。<br/>                                                                                                                                                                 |
| <span id="GL_TRIANGLES"></span><span id="gl_triangles"></span><dl> <dt>**GL \_ 三角形**</dt> </dl>                 | 將每個三個頂點視為獨立的三角形。 頂點 *3n-2*、 *3n-1* 和 *3n* 定義三角形 *n*。 會繪製 *N/3* 個三角形。<br/>                                                                                                                                                                                                                                              |
| <span id="GL_TRIANGLE_STRIP"></span><span id="gl_triangle_strip"></span><dl> <dt>**GL \_ 三角形 \_ 條紋**</dt> </dl> | 繪製一組已連接的三角形。 針對前兩個頂點之後所呈現的每個頂點，各定義一個三角形。 若是奇數 *n*、頂點 *n*、 *n + 1* 和 *n + 2* ，請定義三角形 *n*。 針對偶數 *，* 頂點 *n + 1*、 *n* 和 *n + 2* 定義三角形 *n*。 會繪製 *N-2* 個三角形。<br/>                                                                                                  |
| <span id="GL_TRIANGLE_FAN"></span><span id="gl_triangle_fan"></span><dl> <dt>**GL \_ 三角形 \_ 風扇**</dt> </dl>       | 繪製一組已連接的三角形。 針對前兩個頂點之後所呈現的每個頂點，各定義一個三角形。 頂點 *1*、 *n + 1*、 *n + 2* 定義三角形 *n*。 會繪製 *N-2* 個三角形。<br/>                                                                                                                                                                                         |
| <span id="GL_QUADS"></span><span id="gl_quads"></span><dl> <dt>**GL \_ 四邊形**</dt> </dl>                             | 將四個頂點的每個群組視為獨立四邊形。 頂點 *4n-3*、 *4n-2*、 *4n-1* 和 *4n* 定義四邊形 *n*。 會繪製 *N/4* quadrilaterals。<br/>                                                                                                                                                                                                                  |
| <span id="GL_QUAD_STRIP"></span><span id="gl_quad_strip"></span><dl> <dt>**GL \_ 四 \_ 條**</dt> </dl>             | 繪製連接的 quadrilaterals 群組。 針對第一組之後所顯示的每一對頂點，定義一個四邊形。 頂點 *2n-1*、 *2n*、 *2n + 2* 和 *2n + 1* 定義四邊形 *n*。 會繪製 *N/2-1* 個 quadrilaterals。 請注意，用來從資料四邊形中建立頂點的順序，與獨立資料所使用的順序不同。<br/> |
| <span id="GL_POLYGON"></span><span id="gl_polygon"></span><dl> <dt>**GL \_ 多邊形**</dt> </dl>                       | 繪製單一的凸邊。 頂點 *1* 到 *N* 定義了這個多邊形。<br/>                                                                                                                                                                                                                                                                                                                  |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="error-codes"></a>錯誤碼

[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。



| Name                                                                                                  | 意義                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ 無效 \_ 列舉**</dt> </dl>      | *模式* 已設定為不接受的值。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <dl> <dt>**GL \_ 不正確 \_ 操作**</dt> </dl> | [GlVertex](glvertex-functions.md)、 [glColor](glcolor-functions.md)、 [glIndex](glindex-functions.md)、 [glNormal](glnormal-functions.md)、 [glTexCoord](gltexcoord-functions.md)、 [glEvalCoord](glevalcoord-functions.md)、 [glEvalPoint](glevalpoint.md)、 [glMaterial](glmaterial-functions.md)、 [glEdgeFlag](gledgeflag-functions.md)、 [**glCallList**](glcalllist.md)或 [**glCallLists**](glcalllists.md)以外的函式會在 **glBegin** 與對應的 [**glend**](glend.md)之間呼叫。 函數 **glend** 是在呼叫對應的 **glBegin** 之前呼叫，或在 **glBegin** / **glend** 序列內呼叫 glBegin。 <br/> |



## <a name="remarks"></a>備註

**GlBegin** 和 [**glend**](glend.md)函式會分隔定義基本或類似基本類型群組的頂點。 **GlBegin** 函式會接受單一引數，以指定頂點所組成的10個基本類型。 從1開始，將 *n* 做為整數計數，而 *n* 則是指定的頂點總數，如下所示：

-   您只能在 **glBegin** 與 [**Glend**](glend.md)之間使用 OpenGL 函數的子集。 您可以使用的函數如下：

    [**glVertex**](glvertex-functions.md)

     

    [**glColor**](glcolor-functions.md)

     

    [**glIndex**](glindex-functions.md)

     

    [**glNormal**](glnormal-functions.md)

     

    [**glTexCoord**](gltexcoord-functions.md)

     

    [**glEvalCoord**](glevalcoord-functions.md)

     

    [**glEvalPoint**](glevalpoint.md)

     

    [**glMaterial**](glmaterial-functions.md)

     

    [**glEdgeFlag**](gledgeflag-functions.md)

    您也可以使用 [**glCallList**](glcalllist.md) 或 [**glCallLists**](glcalllists.md) 來執行只包含上述函式的顯示清單。 如果在 **glBegin** 和 [**glend**](glend.md)之間呼叫任何其他 OpenGL 函數，則會設定錯誤旗標，並忽略函式。

-   無論在 **glBegin** 中為 *模式* 選擇的值為何，您可以在 **glBegin** 和 [**glend**](glend.md)之間定義的頂點數目沒有任何限制。 未完整指定的線條、三角形、quadrilaterals 和多邊形都不會繪製。 當提供的頂點太少以指定單一基本或指定了不正確的頂點倍數時，不完整的規格結果。 忽略不完整的基本類型;繪製完整的基本專案。
-   每個基本類型頂點的最小規格為： 

    | 頂點的最小數目 | 基本類型 |
    |----------------------------|-------------------|
    | 1                          | 點             |
    | 2                          | line              |
    | 3                          | 三角形          |
    | 4                          | 四邊形     |
    | 3                          | 多邊形           |

    

     

-   需要特定多個頂點的模式為 GL \_ 行 (2) 、gl \_ 三角形 (3) 、gl \_ 四邊形 (4) 和 GL 四 \_ \_ 個 () 。

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

[**glCallList**](glcalllist.md)
</dt> <dt>

[**glCallLists**](glcalllists.md)
</dt> <dt>

[**glColor**](glcolor-functions.md)
</dt> <dt>

[**glEdgeFlag**](gledgeflag-functions.md)
</dt> <dt>

[**glEnd**](/windows/desktop/OpenGL/glend)
</dt> <dt>

[**glEvalCoord**](glevalcoord-functions.md)
</dt> <dt>

[**glEvalPoint**](glevalpoint.md)
</dt> <dt>

[**glIndex**](glindex-functions.md)
</dt> <dt>

[**glMaterial**](glmaterial-functions.md)
</dt> <dt>

[**glNormal**](glnormal-functions.md)
</dt> <dt>

[**glTexCoord**](gltexcoord-functions.md)
</dt> <dt>

[**glVertex**](glvertex-functions.md)
</dt> </dl>

 

