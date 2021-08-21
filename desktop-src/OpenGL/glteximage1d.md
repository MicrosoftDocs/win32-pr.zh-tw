---
title: 'glTexImage1D 函式 (Gl) '
description: GlTexImage1D 函式會指定一維紋理影像。
ms.assetid: 4f537b89-2ea2-4e2e-8c57-c372bf53f12c
keywords:
- glTexImage1D 函式 OpenGL
topic_type:
- apiref
api_name:
- glTexImage1D
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efd443389439b6d012533d3184739dfa849d672d76a8eced0e8ea244601d4122
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119490248"
---
# <a name="glteximage1d-function"></a>glTexImage1D 函式

**GlTexImage1D** 函式會指定一維紋理影像。

## <a name="syntax"></a>語法


```C++
void WINAPI glTexImage1D(
         GLenum  target,
         GLint   level,
         GLint   internalformat,
         GLsizei width,
         GLint   border,
         GLint   format,
         GLenum  type,
   const GLvoid  *pixels
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*目標* 
</dt> <dd>

目標材質。 必須是 GL \_ 紋理 \_ 1d。

</dd> <dt>

*level* 
</dt> <dd>

詳細資料層級數目。 層級0是基底映射層級。 層級 *n* 是第 *n* 個 mipmap 縮減影像。

</dd> <dt>

*internalformat* 
</dt> <dd>

指定材質中的色彩元件數目。 必須是1、2、3或4，或下列其中一個符號常數： GL \_ ALPHA、gl \_ ALPHA4、gl \_ ALPHA8、GL \_ ALPHA12、gl \_ ALPHA16、gl \_ 亮度、gl \_ LUMINANCE4、gl LUMINANCE8、gl LUMINANCE12、GL LUMINANCE16、gl \_ \_ \_ \_ 亮度 \_ ALPHA、gl LUMINANCE4 ALPHA4、GL LUMINANCE6 ALPHA2 \_ \_ \_ \_ 、GL \_ LUMINANCE8 ALPHA8、gl LUMINANCE12 \_ \_ \_ ALPHA4、GL \_ LUMINANCE12 \_ ALPHA12、GL \_ LUMINANCE16 \_ ALPHA16、gl \_ 濃度、gl \_ INTENSITY4、gl \_ INTENSITY8、gl \_ INTENSITY12、gl \_ INTENSITY16、gl \_ RGB、gl \_ R3 G3 B2 \_ \_ 、 \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ gl RGB4、gl RGB5、gl RGB8、gl RGB10、gl RGB12、gl RGB16、gl RGBA、gl RGBA2、gl RGBA4、gl RGB5、gl RGBA8、gl RGB10、gl RGBA12 或 gl RGBA16。

</dd> <dt>

*width* (寬度) 
</dt> <dd>

材質影像的寬度。 必須為一個整數 *n* 的 2 *n* + 2 (*框線*) 。 材質影像的高度為1。

</dd> <dt>

*邊境* 
</dt> <dd>

框線的寬度。 必須是0或1。

</dd> <dt>

*format* 
</dt> <dd>

圖元資料的格式。 它可以假設有九個符號值的其中一個。



| 值                                                                                                                                                                         | 意義                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_COLOR_INDEX"></span><span id="gl_color_index"></span><dl> <dt>**GL \_ 色彩 \_ 索引**</dt> </dl>             | 每個元素都是單一值，也就是色彩索引。 它會轉換成固定點 (，並在二進位點的右邊指定0位不指定的位數) 、向左或向右移動，視 GL 索引移位的值和正負號而定， \_ \_ 然後新增至 gl \_ 索引 \_ 位移 (查看 [**glPixelTransfer**](glpixeltransfer.md)) 。 產生的索引會使用 GL \_ 圖元 \_ 地圖 \_ i \_ 到 \_ R、gl \_ 圖元 \_ 地圖 \_ i \_ 到 \_ G、gl \_ 圖元 \_ 地圖 \_ i \_ 到 \_ B，以及 gl \_ 圖元 \_ 對應 \_ i 至 \_ \_ 資料表，並壓制至範圍 \[ 0，1 \] ，轉換成一組色彩元件。<br/> |
| <span id="GL_RED"></span><span id="gl_red"></span><dl> <dt>**GL \_ 紅色**</dt> </dl>                                      | 每個元素都是單一的紅色元件。 它會轉換成浮點數，並藉由附加適用于綠色和藍色的0.0，以及適用于 Alpha 的1.0，組合成 RGBA 元素。 接著，每個元件會乘以已簽署的縮放比例 GL \_ c \_ 規模、新增至帶正負號偏差 gl \_ c \_ 偏差，然後壓制至範圍 \[ 0，1 \] (查看 **glPixelTransfer**) 。<br/>                                                                                                                                                                                                |
| <span id="GL_GREEN"></span><span id="gl_green"></span><dl> <dt>**GL \_ 綠**</dt> </dl>                                | 每個元素都是一個綠色的元件。 它會轉換成浮點數，並藉由附加適用于紅色和藍色的0.0 和適用于 Alpha 的1.0，組合成 RGBA 元素。 接著，每個元件會乘以已簽署的縮放比例 GL \_ c \_ 規模、新增至帶正負號偏差 gl \_ c \_ 偏差，然後壓制至範圍 \[ 0，1 \] (查看 [**glPixelTransfer**](glpixeltransfer.md)) 。<br/>                                                                                                                                                                         |
| <span id="GL_BLUE"></span><span id="gl_blue"></span><dl> <dt>**GL \_ 藍色**</dt> </dl>                                   | 每個元素都是單一藍色元件。 它會轉換成浮點數並組合成 RGBA 元素，方法是附加0.0 （紅色和綠色）和1.0 （適用于 Alpha）。 接著，每個元件會乘以已簽署的縮放比例 GL \_ c \_ 規模、新增至帶正負號偏差 gl \_ c \_ 偏差，然後壓制至範圍 \[ 0，1 \] (查看 **glPixelTransfer**) 。<br/>                                                                                                                                                                                                |
| <span id="GL_ALPHA"></span><span id="gl_alpha"></span><dl> <dt>**GL \_ ALPHA**</dt> </dl>                                | 每個元素都是單一的紅色元件。 它會轉換成浮點數，並藉由附加0.0 的紅色、綠色和藍色來組合成 RGBA 元素。 接著，每個元件會乘以已簽署的縮放比例 GL \_ c \_ 規模、新增至帶正負號偏差 gl \_ c \_ 偏差，然後壓制至範圍 \[ 0，1 \] (查看 [**glPixelTransfer**](glpixeltransfer.md)) 。<br/>                                                                                                                                                                                      |
| <span id="GL_RGB"></span><span id="gl_rgb"></span><dl> <dt>**GL \_ RGB**</dt> </dl>                                      | 每個元素都是 RGB 三重。 它會轉換成浮點數，並藉由附加1.0 的 Alpha 來組合成 RGBA 元素。 接著，每個元件會乘以已簽署的縮放比例 GL \_ c \_ 規模、新增至帶正負號偏差 gl \_ c \_ 偏差，然後壓制至範圍 \[ 0，1 \] (查看 **glPixelTransfer**) 。<br/>                                                                                                                                                                                                                                     |
| <span id="GL_RGBA"></span><span id="gl_rgba"></span><dl> <dt>**GL \_ RGBA**</dt> </dl>                                   | 每個元素都是完整的 RGBA 元素。 它會轉換成浮點數。 接著，每個元件會乘以已簽署的縮放比例 GL \_ c \_ 規模、新增至帶正負號偏差 gl \_ c \_ 偏差，然後壓制至範圍 \[ 0，1 \] (查看 **glPixelTransfer**) 。<br/>                                                                                                                                                                                                                                                                                         |
| <span id="GL_BGR_EXT"></span><span id="gl_bgr_ext"></span><dl> <dt>**GL \_ BGR \_ EXT**</dt> </dl>                         | 每個圖元都是三個元件的群組，順序如下：藍色、綠色、紅色。<br/> GL \_ BGR \_ EXT 提供的格式符合 Windows 裝置獨立點陣圖 (dib) 的記憶體配置。 因此，您的應用程式可以使用 Windows 函式呼叫和 OpenGL 圖元函式呼叫的相同資料。<br/>                                                                                                                                                                                                                                      |
| <span id="GL_BGRA_EXT"></span><span id="gl_bgra_ext"></span><dl> <dt>**GL \_ BGRA \_ EXT**</dt> </dl>                      | 每個圖元都是四個元件的群組，順序如下： blue、綠、red、Alpha。<br/> GL \_ BGRA \_ EXT 提供的格式符合 Windows 裝置獨立點陣圖 (dib) 的記憶體配置。 因此，您的應用程式可以使用 Windows 函式呼叫和 OpenGL 圖元函式呼叫的相同資料。<br/>                                                                                                                                                                                                                               |
| <span id="GL_LUMINANCE"></span><span id="gl_luminance"></span><dl> <dt>**GL \_ 亮度**</dt> </dl>                    | 每個元素都是單一的亮度值。 它會轉換成浮點數，然後藉由針對紅色、綠色和藍色複寫亮度值三次，然後附加1.0 的 Alpha 元素組合成 RGBA 元素。 接著，每個元件會乘以已簽署的縮放比例 GL \_ c \_ 規模、新增至帶正負號偏差 gl \_ c \_ 偏差，然後壓制至範圍 \[ 0，1 \] (查看 [**glPixelTransfer**](glpixeltransfer.md)) 。<br/>                                                                                                                   |
| <span id="GL_LUMINANCE_ALPHA"></span><span id="gl_luminance_alpha"></span><dl> <dt>**GL \_ 亮度 \_ ALPHA**</dt> </dl> | 每個元素都是一組明亮度/Alpha 配對。 它會轉換成浮點數，然後藉由針對紅色、綠色和藍色複寫亮度值三次，來組合成 RGBA 元素。 接著，每個元件會乘以已簽署的縮放比例 GL \_ c \_ 規模、新增至帶正負號偏差 gl \_ c \_ 偏差，然後壓制至範圍 \[ 0，1 \] (查看 **glPixelTransfer**) 。<br/>                                                                                                                                                                         |



 

</dd> <dt>

*type* 
</dt> <dd>

圖元資料的資料類型。 接受下列符號值： GL \_ 未簽署 \_ 位元組、gl \_ 位元組、GL \_ 點陣圖、gl \_ 未簽署 \_ 短、gl \_ 簡短、GL 不 \_ 帶正負號 \_ int、GL \_ int 和 gl \_ FLOAT。

</dd> <dt>

*圖元* 
</dt> <dd>

記憶體中影像資料的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="error-codes"></a>錯誤碼

[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。



| 名稱                                                                                                  | 意義                                                                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ 無效 \_ 列舉**</dt> </dl>      | *目標* 不是 GL \_ 紋理。<br/>                                                                                                                                                                                    |
| <dl> <dt>**GL \_ 無效 \_ 列舉**</dt> </dl>      | *格式* 不是接受的 *格式* 常數。 只接受 GL 樣板 \_ \_ 索引和 gl \_ 深度 \_ 元件以外的格式常數。 如需可能值的清單，請參閱 *格式* 的參數描述。<br/> |
| <dl> <dt>**GL \_ 無效 \_ 列舉**</dt> </dl>      | *類型* 不是 *類型* 常數。<br/>                                                                                                                                                                                   |
| <dl> <dt>**GL \_ 無效 \_ 列舉**</dt> </dl>      | *類型* 為 gl \_ 點陣圖， *格式* 不是 gl \_ 色彩 \_ 索引。<br/>                                                                                                                                                        |
| <dl> <dt>**GL \_ 無效 \_ 值**</dt> </dl>     | *層級* 小於零或大於 log2 *max*，其中 *max* 是 GL \_ 最大紋理大小的傳回值 \_ \_ 。<br/>                                                                                                 |
| <dl> <dt>**GL \_ 無效 \_ 值**</dt> </dl>     | *internalformat* 不是1、2、3或4。<br/>                                                                                                                                                                         |
| <dl> <dt>**GL \_ 無效 \_ 值**</dt> </dl>     | *寬度* 小於零或大於 2 + GL \_ 的最大 \_ 紋理 \_ 大小，或無法表示為某個整數值 *n* 的 2 *n* + 2 (框線) 。<br/>                                                            |
| <dl> <dt>**GL \_ 無效 \_ 值**</dt> </dl>     | *框線* 不是0或1。<br/>                                                                                                                                                                                            |
| <dl> <dt>**GL \_ 不正確 \_ 操作**</dt> </dl> | 呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。<br/>                                                                                          |



## <a name="remarks"></a>備註

**GlTexImage1D** 函式會指定一維紋理影像。 紋理會將指定之 *材質影像* 的一部分對應到已啟用紋理的每個圖形化基本物件。 使用 [**glEnable**](glenable.md) 和 **glDisable** 搭配引數 GL 紋理1d 來啟用和停用一維紋理 \_ \_ 。

材質影像會以 **glTexImage1D** 定義。 引數描述紋理影像的參數，例如框線寬度、框線寬度、詳細資料層級 (查看 [**glTexParameter**](gltexparameter-functions.md)) ，以及所提供的色彩元件數目。 最後三個引數說明影像在記憶體中的呈現方式。 這些引數等同于用於 [**glDrawPixels**](gldrawpixels.md)的像素格式。

資料會以一系列的帶正負號或不帶正負號的位元組、短路或長，或單精確度浮點值（視 *類型* 而 *定）來* 讀取。 這些值會依 *格式* 組成一組、二、三或四個值，以形成元素。 如果 *type* 是 GL \_ BITMAP，資料會被視為不帶正負號的位元組字串 (且 *格式* 必須是 GL \_ 色彩 \_ 索引) 。 每個資料位元組都會被視為 8 1 位元素，並以 GL 解壓縮 LSB 先決定的位順序， \_ \_ \_ (請參閱 [**glPixelStore**](glpixelstore-functions.md)) 。

材質影像的每個材質元素最多可有四個元件，視 *元件* 而定。 單一元件紋理影像只會使用從 *圖元* 解壓縮之 RGBA 色彩的紅色元件。 雙元件映射會使用 R 和值。 三個元件的影像使用 R、G 和 B 值。 四個元件的映射會使用所有的 RGBA 元件。

紋理在色彩索引模式中沒有任何作用。

材質影像可以用與 [**glDrawPixels**](gldrawpixels.md) 命令中的圖元相同的資料格式表示，但 \_ 無法使用 gl 樣板 \_ 索引和 gl \_ 深度 \_ 元件。 [**GlPixelStore**](glpixelstore-functions.md)和 [**glPixelTransfer**](glpixeltransfer.md)模式會以其影響 **glDrawPixels** 的確切方式來影響紋理影像。

寬度為零的材質影像表示 null 材質。 如果針對詳細資料0指定了 null 材質，就如同已停用紋理一樣。

下列函式會取出與 **glTexImageID** 相關的資訊：

[**glGetTexImage**](glgetteximage.md)

[](glisenabled.md)具有引數 GL \_ 材質 \_ 1d 的 glIsEnabled

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

[**glCopyPixels**](glcopypixels.md)
</dt> <dt>

[**glCopyTexImage1D**](glcopyteximage1d.md)
</dt> <dt>

[**glCopyTexImage2D**](glcopyteximage2d.md)
</dt> <dt>

[**glCopyTexSubImage1D**](glcopytexsubimage1d.md)
</dt> <dt>

[**glCopyTexSubImage2D**](glcopytexsubimage2d.md)
</dt> <dt>

[**glDrawPixels**](gldrawpixels.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glFog**](glfog.md)
</dt> <dt>

[**glGetTexImage**](glgetteximage.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> <dt>

[**glPixelStore**](glpixelstore-functions.md)
</dt> <dt>

[**glPixelTransfer**](glpixeltransfer.md)
</dt> <dt>

[**glTexEnv**](gltexenv-functions.md)
</dt> <dt>

[**glTexGen**](gltexgen-functions.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> <dt>

[**glTexSubImage1D**](gltexsubimage1d.md)
</dt> <dt>

[**glTexSubImage2D**](gltexsubimage2d.md)
</dt> <dt>

[**glTexParameter**](gltexparameter-functions.md)
</dt> </dl>

 

 





