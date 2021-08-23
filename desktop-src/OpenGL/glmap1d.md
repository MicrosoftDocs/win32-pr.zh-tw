---
title: 'glMap1d 函式 (Gl) '
description: 'GlMap1d 函數會定義一維評估工具。 |glMap1d 函式 (Gl) '
ms.assetid: 65f8b099-597c-4300-a7d1-3dabdd19e6cb
keywords:
- glMap1d 函式 OpenGL
topic_type:
- apiref
api_name:
- glMap1d
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90f1d17312cae14da955641d0009235a45fa23e65a3a04e35f692a4bb5418722
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119520428"
---
# <a name="glmap1d-function"></a>glMap1d 函式

**GlMap1d** 和 [**glMap1f**](glmap1f.md)函數會定義一維評估工具。

## <a name="syntax"></a>語法


```C++
void WINAPI glMap1d(
         GLenum   target,
         GLdouble u1,
         GLdouble u2,
         GLint    stride,
         GLint    order,
   const GLdouble *points
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*目標* 
</dt> <dd>

評估工具產生的數值型別。 符號常數。 *目標* 參數是一個符號常數，表示以 *點* 提供的控制點種類，以及評估對應時所產生的輸出。 它可以假設有九個預先定義的值。



| 值                                                                                                                                                                                          | 意義                                                                                                                                                                                                                                                                                                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_MAP1_VERTEX_3"></span><span id="gl_map1_vertex_3"></span><dl> <dt>**GL \_ MAP1 \_ 頂點 \_ 3**</dt> </dl>                       | 每個控制點都是三個表示 *x、y* 和 *z* 的浮點值。 評估對應時，會產生內部 [**glVertex3**](glvertex-functions.md) 命令。<br/>                                                                                                                                         |
| <span id="GL_MAP1_VERTEX_4"></span><span id="gl_map1_vertex_4"></span><dl> <dt>**GL \_ MAP1 \_ 頂點 \_ 4**</dt> </dl>                       | 每個控制點都是四個表示 *x、y、z* 和 *w* 的浮點值。 評估對應時，會產生內部 [**glVertex4**](glvertex-functions.md) 命令。<br/>                                                                                                                                       |
| <span id="GL_MAP1_INDEX"></span><span id="gl_map1_index"></span><dl> <dt>**GL \_ MAP1 \_ 索引**</dt> </dl>                                 | 每個控制點都是代表色彩索引的單一浮點值。 評估對應時，會產生內部 [**glIndex**](glindex-functions.md) 命令。 不過，目前的索引不會以這些 **glIndex** 命令的值更新。<br/>                                                    |
| <span id="GL_MAP1_COLOR_4"></span><span id="gl_map1_color_4"></span><dl> <dt>**GL \_ MAP1 \_ 色彩 \_ 4**</dt> </dl>                          | 每個控制點都是四個浮點值，代表紅色、綠色、藍色和 Alpha。 評估對應時，會產生內部 [**glColor4**](glcolor-functions.md) 命令。 不過，目前的色彩不會更新為這些 **glColor4** 命令的值。<br/>                                       |
| <span id="GL_MAP1_NORMAL"></span><span id="gl_map1_normal"></span><dl> <dt>**GL \_ MAP1 \_ 正常**</dt> </dl>                              | 每個控制點都是三個浮點值，代表一般向量的 *x、y* 和 *z* 元件。 評估對應時，會產生內部 [**glNormal**](glnormal-functions.md) 命令。 不過，目前的一般不會以這些 **glNormal** 命令的值更新。<br/>              |
| <span id="GL_MAP1_TEXTURE_COORD_1"></span><span id="gl_map1_texture_coord_1"></span><dl> <dt>**GL \_ MAP1 \_ 材質 \_ COORD \_ 1**</dt> </dl> | 每個控制點都是代表 *s* 材質座標的單一浮點值。 評估對應時，會產生內部 [**glTexCoord1**](gltexcoord-functions.md) 命令。 不過，目前的材質座標不會更新為這些 **glTexCoord** 命令的值。<br/>              |
| <span id="GL_MAP1_TEXTURE_COORD_2"></span><span id="gl_map1_texture_coord_2"></span><dl> <dt>**GL \_ MAP1 \_ 材質 \_ COORD \_ 2**</dt> </dl> | 每個控制點都是代表 *s* 和 *t* 材質座標的兩個浮點值。 評估對應時，會產生內部 [**glTexCoord2**](gltexcoord-functions.md) 命令。 不過，目前的材質座標不會更新為這些 **glTexCoord** 命令的值。<br/>         |
| <span id="GL_MAP1_TEXTURE_COORD_3"></span><span id="gl_map1_texture_coord_3"></span><dl> <dt>**GL \_ MAP1 \_ 材質 \_ COORD \_ 3**</dt> </dl> | 每個控制點都是三個浮點值，代表 *s、t* 和 *r* 材質座標。 評估對應時，會產生內部 [**glTexCoord3**](gltexcoord-functions.md) 命令。 不過，目前的材質座標不會更新為這些 **glTexCoord** 命令的值。<br/>   |
| <span id="GL_MAP1_TEXTURE_COORD_4"></span><span id="gl_map1_texture_coord_4"></span><dl> <dt>**GL \_ MAP1 \_ 材質 \_ COORD \_ 4**</dt> </dl> | 每個控制點都是四個浮點值，代表 *s、t、r* 和 *q* 材質座標。 評估對應時，會產生內部 [**glTexCoord4**](gltexcoord-functions.md) 命令。 不過，目前的材質座標不會更新為這些 **glTexCoord** 命令的值。<br/> |



 

</dd> <dt>

*u1* 
</dt> <dd>

*U* 的線性對應（顯示為 [**glEvalCoord1**](glevalcoord-functions.md)）到 *u*^，這是由這個命令指定的方程式所評估的變數。

</dd> <dt>

*u2* 
</dt> <dd>

*U* 的線性對應（顯示為 [**glEvalCoord1**](glevalcoord-functions.md)）到 *u*^，這是由這個命令指定的方程式所評估的變數。

</dd> <dt>

*大步* 
</dt> <dd>

*點* 的開頭或雙精度浮點數之間的浮點數，或資料結構中的下一個控制點開始之間的浮點數。 這可讓控制點內嵌在任意的資料結構中。 唯一的條件約束是特定控制點的值必須佔用連續的記憶體位置。

</dd> <dt>

*order* 
</dt> <dd>

控制點的數目。 必須是正數。

</dd> <dt>

*點* 
</dt> <dd>

指向控制項點陣列的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="error-codes"></a>錯誤碼

[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。



| 名稱                                                                                                  | 意義                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ 無效 \_ 列舉**</dt> </dl>      | *目標* 不是可接受的值。<br/>                                                                                        |
| <dl> <dt>**GL \_ 無效 \_ 值**</dt> </dl>     | *u1* 等於 *u2*。<br/>                                                                                                    |
| <dl> <dt>**GL \_ 無效 \_ 值**</dt> </dl>     | *stride* 小於控制點中的值數目。<br/>                                                            |
| <dl> <dt>**GL \_ 無效 \_ 值**</dt> </dl>     | *順序* 小於一或 GL 的 \_ 最大 \_ 評估 \_ 順序。<br/>                                                                         |
| <dl> <dt>**GL \_ 不正確 \_ 操作**</dt> </dl> | 呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。<br/> |



## <a name="remarks"></a>備註

評估工具提供一種方式，可使用多項式或有理數多項式對應來產生頂點、法線、材質座標和色彩。 評估工具所產生的值會傳送至 OpenGL 處理的其他階段，就像是使用 [**glVertex**](glvertex-functions.md)、 [**glNormal**](glnormal-functions.md)、 [**glTexCoord**](gltexcoord-functions.md)和 [**glColor**](glcolor-functions.md) 命令來呈現一樣，不過產生的值不會更新目前的一般、材質座標或色彩。

任何程度的所有多項式或有理多項式曲線都 (最高至 OpenGL 實) 支援的最大程度，可使用評估工具來描述。 這些幾乎包括電腦圖形中使用的所有曲線，包括 B 曲線、貝茲曲線、Hermite 曲線等等。

評估工具會根據 Bernstein polynomials 來定義曲線。 將 **p** () 定義為

![顯示 p () 定義的方程式。](images/map01.png)

其中， **R**_i_ 是控制點， () 是 *i* *n* (*order*  = *n* + 1) 的 Bernstein 多項式：

![顯示等級 n 之 Bernstein 多項式的方程式。](images/map02.png)

回想一下

![顯示等同于1的方等方。](images/map03.png)

**GlMap1** 函式是用來定義基礎以及指定所產生的數值型別。 一旦定義之後，就可以藉由呼叫 [**glEnable**](glenable.md) 和 **glDisable** （具有對應名稱）來啟用和停用對應，上述的 *目標* 有九個預先定義的值。 [GlEvalCoord1](glevalcoord-functions.md)函數會評估已啟用的一維對應。 當 **glEvalCoord1** 顯示值 *u* 時，就會使用 *u*^ 來評估 Bernstein 函數，其中

![顯示您 ^ 定義的方程式。](images/map04.png)

*Stride*、 *order* 和 *points* 參數會定義用來存取控制點的陣列定址。 *Points* 參數是第一個控制點的位置，它會佔用一、二、三個或四個連續的記憶體位置，視所定義的對應而定。 *Order* 參數是陣列中的控制點數目。 *Stride* 參數會告訴要將內部記憶體指標前進到下一個控制點的浮點或雙位置數目。

同樣地，如果所有 OpenGL 命令都接受資料指標，就如同 **glMap1** 在傳回點之前複製 *點* 的內容一樣。 在呼叫 **glMap1** 之後，對 *點* 內容所做的變更不會有任何作用。

下列函式會取出與 **glMap1** 相關的資訊：

[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 最大 \_ EVAL \_ 順序的 glGet

[**glGetMap**](glgetmap.md)

[**glIsEnabled**](glisenabled.md) 與引數 GL \_ MAP1 \_ 頂點 \_ 3

**glIsEnabled** 與引數 GL \_ MAP1 \_ 頂點 \_ 4

具有引數 GL \_ MAP1 \_ 索引的 glIsEnabled

**glIsEnabled** 與引數 GL \_ MAP1 \_ 色彩 \_ 4

**glIsEnabled** 與引數 GL \_ MAP1 \_ NORMAL

**glIsEnabled** 與引數 GL \_ MAP1 \_ 材質 \_ COORD \_ 1

**glIsEnabled** 與引數 GL \_ MAP1 \_ 材質 \_ COORD \_ 2

**glIsEnabled** 與引數 GL \_ MAP1 \_ 材質 \_ COORD \_ 3

**glIsEnabled** 與引數 GL \_ MAP1 \_ 材質 \_ COORD \_ 4

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

[**glColor**](glcolor-functions.md)
</dt> <dt>

[**glEnable**](glenable.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glEvalCoord**](glevalcoord-functions.md)
</dt> <dt>

[**glEvalMesh**](glevalmesh-functions.md)
</dt> <dt>

[**glEvalPoint**](glevalpoint.md)
</dt> <dt>

[**glMap2**](glmap2.md)
</dt> <dt>

[**glMapGrid**](glmapgrid-functions.md)
</dt> <dt>

[**glNormal**](glnormal-functions.md)
</dt> <dt>

[**glTexCoord**](gltexcoord-functions.md)
</dt> <dt>

[**glVertex**](glvertex-functions.md)
</dt> </dl>

 

 





