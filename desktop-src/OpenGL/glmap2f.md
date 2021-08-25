---
title: 'glMap2f 函式 (Gl) '
description: 'GlMap2f 函數會定義二維評估工具。 |glMap2f 函式 (Gl) '
ms.assetid: 804fbf65-98a8-41af-8c39-5b83f3d341b0
keywords:
- glMap2f 函式 OpenGL
topic_type:
- apiref
api_name:
- glMap2f
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb9f0d33cea662f35cdbbfb0b414d0254883cd619d55832550abdec3668ef070
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119741378"
---
# <a name="glmap2f-function"></a>glMap2f 函式

[**GlMap2d**](glmap2d.md)和 **glMap2f** 函數會定義二維評估工具。

## <a name="syntax"></a>語法


```C++
void WINAPI glMap2f(
         GLenum  target,
         GLfloat u1,
         GLfloat u2,
         GLint   ustride,
         GLint   uorder,
         GLfloat v1,
         GLfloat v2,
         GLint   vstride,
         GLint   vorder,
   const GLfloat *points
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*目標* 
</dt> <dd>

評估工具產生的數值型別。 接受下列符號常數。



| 值                                                                                                                                                                                          | 意義                                                                                                                                                                                                                                                                                                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_MAP2_VERTEX_3"></span><span id="gl_map2_vertex_3"></span><dl> <dt>**GL \_ List.map2 \_ 頂點 \_ 3**</dt> </dl>                       | 每個控制點都是三個表示 *x、y* 和 *z* 的浮點值。 評估對應時，會產生內部 [**glVertex3**](glvertex-functions.md) 命令。<br/>                                                                                                                                         |
| <span id="GL_MAP2_VERTEX_4"></span><span id="gl_map2_vertex_4"></span><dl> <dt>**GL \_ List.map2 \_ 頂點 \_ 4**</dt> </dl>                       | 每個控制點都是四個表示 *x、y、z* 和 *w* 的浮點值。 評估對應時，會產生內部 [**glVertex4**](glvertex-functions.md) 命令。<br/>                                                                                                                                       |
| <span id="GL_MAP2_INDEX"></span><span id="gl_map2_index"></span><dl> <dt>**GL \_ List.map2 \_ 索引**</dt> </dl>                                 | 每個控制點都是代表色彩索引的單一浮點值。 評估對應時，會產生內部 [**glIndex**](glindex-functions.md) 命令。 不過，目前的索引不會更新為這些 **glIndex** 命令的值。<br/>                                                    |
| <span id="GL_MAP2_COLOR_4"></span><span id="gl_map2_color_4"></span><dl> <dt>**GL \_ List.map2 \_ 色彩 \_ 4**</dt> </dl>                          | 每個控制點都是四個浮點值，代表紅色、綠色、藍色和 Alpha。 評估對應時，會產生內部 [**glColor4**](glcolor-functions.md) 命令。 不過，目前的色彩不會更新為這些 **glColor4** 命令的值。<br/>                                       |
| <span id="GL_MAP2_NORMAL"></span><span id="gl_map2_normal"></span><dl> <dt>**GL \_ List.map2 \_ 正常**</dt> </dl>                              | 每個控制點都是三個浮點值，代表一般向量的 *x、y* 和 *z* 元件。 評估對應時，會產生內部 [**glNormal**](glnormal-functions.md) 命令。 不過，目前的一般不會更新為這些 **glNormal** 命令的值。<br/>              |
| <span id="GL_MAP2_TEXTURE_COORD_1"></span><span id="gl_map2_texture_coord_1"></span><dl> <dt>**GL \_ List.map2 \_ 材質 \_ COORD \_ 1**</dt> </dl> | 每個控制點都是代表 *s* 材質座標的單一浮點值。 評估對應時，會產生內部 [**glTexCoord1**](gltexcoord-functions.md) 命令。 不過，目前的材質座標不會更新為這些 **glTexCoord** 命令的值。<br/>              |
| <span id="GL_MAP2_TEXTURE_COORD_2"></span><span id="gl_map2_texture_coord_2"></span><dl> <dt>**GL \_ List.map2 \_ 材質 \_ COORD \_ 2**</dt> </dl> | 每個控制點都是代表 *s* 和 *t* 材質座標的兩個浮點值。 評估對應時，會產生內部 [**glTexCoord2**](gltexcoord-functions.md) 命令。 不過，目前的材質座標不會更新為這些 **glTexCoord** 命令的值。<br/>         |
| <span id="GL_MAP2_TEXTURE_COORD_3"></span><span id="gl_map2_texture_coord_3"></span><dl> <dt>**GL \_ List.map2 \_ 材質 \_ COORD \_ 3**</dt> </dl> | 每個控制點都是三個浮點值，代表 *s、t* 和 *r* 材質座標。 評估對應時，會產生內部 [**glTexCoord3**](gltexcoord-functions.md) 命令。 不過，目前的材質座標不會更新為這些 **glTexCoord** 命令的值。<br/>   |
| <span id="GL_MAP2_TEXTURE_COORD_4"></span><span id="gl_map2_texture_coord_4"></span><dl> <dt>**GL \_ List.map2 \_ 材質 \_ COORD \_ 4**</dt> </dl> | 每個控制點都是四個浮點值，代表 *s、t、r* 和 *q* 材質座標。 評估對應時，會產生內部 [**glTexCoord4**](gltexcoord-functions.md) 命令。 不過，目前的材質座標不會更新為這些 **glTexCoord** 命令的值。<br/> |



 

</dd> <dt>

*u1* 
</dt> <dd>

以 [**glEvalCoord2**](glevalcoord-functions.md)為 u *^ 的雙向* 線性對應，這是由這個命令指定的方程式所評估的兩個變數之一。

</dd> <dt>

*u2* 
</dt> <dd>

以 [**glEvalCoord2**](glevalcoord-functions.md)為 u *^ 的雙向* 線性對應，這是由這個命令指定的方程式所評估的兩個變數之一。

</dd> <dt>

*ustride* 
</dt> <dd>

控制點 **r** *ij* 開頭與控制點 **r 開頭** <sub> (i + 1 \ ) \ j</sub>之間的浮點數或雙精度浮點數，其中 *i* 和 *j* 分別是 *u* 和 *v* 控制點索引。 這可讓控制點內嵌在任意的資料結構中。 唯一的條件約束是特定控制點的值必須佔用連續的記憶體位置。

</dd> <dt>

*uorder* 
</dt> <dd>

*U* 軸中控制點陣列的維度。 必須是正數。

</dd> <dt>

*v1* 
</dt> <dd>

將 *v* 的線性對應（顯示為 [**glEvalCoord2**](glevalcoord-functions.md)）到 *v*^，這是由這個命令指定的方程式所評估的兩個變數之一。

</dd> <dt>

*2* 
</dt> <dd>

將 *v* 的線性對應（顯示為 [**glEvalCoord2**](glevalcoord-functions.md)）到 *v*^，這是由這個命令指定的方程式所評估的兩個變數之一。

</dd> <dt>

*vstride* 
</dt> <dd>

控制點 **r** *ij* 的起點和控制點的開頭之間的浮點數或雙精度浮點數 **r** <sub> (j + 1 \ )</sub>，其中 *i* 和 *j* 分別是 *u* 和 *v* 控制點索引。 這可讓控制點內嵌在任意的資料結構中。 唯一的條件約束是特定控制點的值必須佔用連續的記憶體位置。

</dd> <dt>

*vorder* 
</dt> <dd>

*V* 軸中控制點陣列的維度。 必須是正數。

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
| <dl> <dt>**GL \_ 無效 \_ 值**</dt> </dl>     | *u1* 等於 *u2*，或 *v1* 等於 *v2*。<br/>                                                                         |
| <dl> <dt>**GL \_ 無效 \_ 值**</dt> </dl>     | *Ustride* 或 *vstride* 小於控制點中的值數目。<br/>                                       |
| <dl> <dt>**GL \_ 無效 \_ 值**</dt> </dl>     | *Uorder* 或 *vorder* 小於一或 GL 的 \_ 最大 \_ 評估 \_ 順序。<br/>                                                     |
| <dl> <dt>**GL \_ 不正確 \_ 操作**</dt> </dl> | 呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。<br/> |



## <a name="remarks"></a>備註

評估工具提供一種方式，可使用多項式或有理數多項式對應來產生頂點、法線、材質座標和色彩。 評估工具所產生的值會傳送至 OpenGL 處理的其他階段，就像是使用 [**glVertex**](glvertex-functions.md)、 [**glNormal**](glnormal-functions.md)、 [**glTexCoord**](gltexcoord-functions.md)和 [**glColor**](glcolor-functions.md) 命令呈現一樣，不同的是產生的值不會更新目前的一般、材質座標或色彩。

任何程度的所有多項式或有理多項式曲線都 (最高至 OpenGL 實) 支援的最大程度，可使用評估工具來描述。 這些介面幾乎包括電腦圖形中使用的所有表面，包括 B 曲線表面、NURBS 表面、貝塞爾表面等等。

評估工具會根據 bivariate Bernstein polynomials 來定義表面。 定義 **p** (*u*^，*v*^) 為

![顯示 p () 定義的方程式。](images/map05.png)

其中 **R** *ij* 是控制點， () 是 *我* 的 Bernstein 多項式程度

*n* (*uorder*  =  *n* + 1) 

![顯示等級 n 之 Bernstein 多項式的方程式。](images/map06.png)

而 () 是 *a 度的* *j* Bernstein 多項式 (*vorder*  =  *m* + 1) 

![顯示 Bernstein 多項式度的方程式。](images/map07.png)

回想一下

![顯示等同于1的方等方。](images/map08.png)

**GlMap2** 函式是用來定義基礎以及指定所產生的數值型別。 一旦定義之後，就可以藉由呼叫 [**glEnable**](glenable.md) 和 **glDisable** （具有對應名稱）（ *目標* 的九個預先定義值其中一個）來啟用和停用對應，如上所述。 當 [**glEvalCoord2**](glevalcoord-functions.md) 顯示值 *u* 和 *v* 時，會使用 *u*^ 和 *v*^ 來評估 bivariate Bernstein polynomials，其中

![顯示您 ^ 定義的方程式。](images/map09.png)

及

![顯示 v ^ 定義的方程式。](images/map10.png)

*目標* 參數是一個符號常數，表示以 *點* 提供的控制點種類，以及評估對應時所產生的輸出。

*Ustride*、 *uorder*、 *vstride*、 *vorder* 和 *points* 參數會定義用來存取控制點的陣列定址。 *Points* 參數是第一個控制點的位置，它會佔用一、二、三個或四個連續的記憶體位置，視所定義的對應而定。 陣列中有 *uorder* x *vorder* 控制點。 *Ustride* 參數會指出略過多少 float 或 double 位置，以便將內部記憶體指標從控制點 **r** *Ij* 前移至控制點 **r** <sub> ( \ i + 1 \ ) j</sub>。 *Vstride* 參數會指出略過多少 float 或 double 位置，以將內部記憶體指標從控制點 **r** *Ij* 前移至控制點 **r**<sub>i (j + 1 \ )</sub>。

同樣地，如果所有 OpenGL 命令都接受資料指標，就如同 **glMap2** 在傳回點之前複製 *點* 的內容一樣。 在呼叫 **glMap2** 之後，對 *點* 內容所做的變更不會有任何作用。

下列函式會取出與 **glMap2** 相關的資訊：

[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 最大 \_ EVAL \_ 順序的 glGet

[**glGetMap**](glgetmap.md)

[**glIsEnabled**](glisenabled.md) 與引數 GL \_ list.map2 \_ 頂點 \_ 3

**glIsEnabled** 與引數 GL \_ list.map2 \_ 頂點 \_ 4

具有引數 GL \_ List.map2 \_ 索引的 glIsEnabled

**glIsEnabled** 與引數 GL \_ list.map2 \_ 色彩 \_ 4

**glIsEnabled** 與引數 GL \_ list.map2 \_ NORMAL

**glIsEnabled** 與引數 GL \_ list.map2 \_ 材質 \_ COORD \_ 1

**glIsEnabled** 與引數 GL \_ list.map2 \_ 材質 \_ COORD \_ 2

**glIsEnabled** 與引數 GL \_ list.map2 \_ 材質 \_ COORD \_ 3

**glIsEnabled** 與引數 GL \_ list.map2 \_ 材質 \_ COORD \_ 4

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

[**glMap1**](glmap1.md)
</dt> <dt>

[**glMapGrid**](glmapgrid-functions.md)
</dt> <dt>

[**glNormal**](glnormal-functions.md)
</dt> <dt>

[**glTexCoord**](gltexcoord-functions.md)
</dt> <dt>

[**glVertex**](glvertex-functions.md)
</dt> </dl>

 

 





