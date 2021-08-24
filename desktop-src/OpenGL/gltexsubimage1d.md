---
title: 'glTexSubImage1D 函式 (Gl) '
description: GlTexSubImage1D 函式會指定現有一維材質影像的一部分。 您無法使用 glTexSubImage1D 來定義新的材質。
ms.assetid: e5fcb1a3-96f8-47a6-a9a7-0061faaaa6ac
keywords:
- glTexSubImage1D 函式 OpenGL
topic_type:
- apiref
api_name:
- glTexSubImage1D
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52dcb6c34d0ce48f646ace1db8a5dc0f773b7eb386ac487534a57367e6e72da3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119777738"
---
# <a name="gltexsubimage1d-function"></a>glTexSubImage1D 函式

**GlTexSubImage1D** 函式會指定現有一維材質影像的一部分。 您無法使用 **glTexSubImage1D** 來定義新的材質。

## <a name="syntax"></a>語法


```C++
void WINAPI glTexSubImage1D(
         GLenum  target,
         GLint   level,
         GLint   xoffset,
         GLsizei width,
         GLenum  format,
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

詳細資料層級數目。 層級0是基底映射。 層級 *n* 是第 *n* 個 mipmap 縮減影像。

</dd> <dt>

*xoffset* 
</dt> <dd>

紋理陣列內 *x* 方向的材質位移。

</dd> <dt>

*width* (寬度) 
</dt> <dd>

材質子影像的寬度。

</dd> <dt>

*format* 
</dt> <dd>

圖元資料的格式。 這個參數可以採用下列其中一個符號值。



| 值                                                                                                                                                                         | 意義                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_COLOR_INDEX"></span><span id="gl_color_index"></span><dl> <dt>**GL \_ 色彩 \_ 索引**</dt> </dl>             | 每個元素都是單一值，也就是色彩索引。 它會轉換成固定點格式 (在二進位點的右邊有未指定的0位位數) 、向左或向右移動，視 GL 索引移位的值和正負號而定， \_ \_ 然後新增至 gl \_ 索引 \_ 位移 (查看 [**glPixelTransfer**](glpixeltransfer.md)) 。 產生的索引會使用 GL \_ 圖元 \_ 地圖 \_ i \_ 到 \_ R、gl \_ 圖元 \_ 地圖 \_ i \_ 到 \_ G、gl \_ 圖元 \_ 地圖 \_ i \_ 到 \_ B，以及 gl \_ 圖元 \_ 對應 \_ i 至 \_ \_ 資料表，並壓制至範圍 \[ 0，1 \] ，轉換成一組色彩元件。<br/> |
| <span id="GL_RED"></span><span id="gl_red"></span><dl> <dt>**GL \_ 紅色**</dt> </dl>                                      | 每個元素都是單一的紅色元件。 它會轉換為浮點格式並組合成 RGBA 元素，方法是附加0.0 （適用于綠色和藍色）和1.0 （Alpha）。 接著，每個元件會乘以已簽署的縮放比例 GL \_ c \_ 規模、新增至帶正負號偏差 gl \_ c \_ 偏差，然後壓制至範圍 \[ 0，1 \] (查看 **glPixelTransfer**) 。<br/>                                                                                                                                                                                                |
| <span id="GL_GREEN"></span><span id="gl_green"></span><dl> <dt>**GL \_ 綠**</dt> </dl>                                | 每個元素都是一個綠色的元件。 它會轉換成浮點數格式並組合成 RGBA 元素，方法是附加0.0 （紅色和藍色）和1.0 （Alpha）。 接著，每個元件會乘以已簽署的縮放比例 GL \_ c \_ 規模、新增至帶正負號偏差 gl \_ c \_ 偏差，然後壓制至範圍 \[ 0，1 \] (查看 [**glPixelTransfer**](glpixeltransfer.md)) 。<br/>                                                                                                                                                                         |
| <span id="GL_BLUE"></span><span id="gl_blue"></span><dl> <dt>**GL \_ 藍色**</dt> </dl>                                   | 每個元素都是單一藍色元件。 它會轉換成浮點數格式並組合成 RGBA 元素，方法是附加0.0 （紅色和綠色）和1.0 （Alpha）。 接著，每個元件會乘以已簽署的縮放比例 GL \_ c \_ 規模、新增至帶正負號偏差 gl \_ c \_ 偏差，然後壓制至範圍 \[ 0，1 \] (查看 **glPixelTransfer**) 。<br/>                                                                                                                                                                                                |
| <span id="GL_ALPHA"></span><span id="gl_alpha"></span><dl> <dt>**GL \_ ALPHA**</dt> </dl>                                | 每個元素都是單一 Alpha 元件。 它會轉換成浮點數格式，並藉由附加0.0 的紅色、綠色和藍色來組合成 RGBA 元素。 接著，每個元件會乘以已簽署的縮放比例 GL \_ c \_ 規模、新增至帶正負號偏差 gl \_ c \_ 偏差，然後壓制至範圍 \[ 0，1 \] (查看 [**glPixelTransfer**](glpixeltransfer.md)) 。<br/>                                                                                                                                                                                    |
| <span id="GL_RGB"></span><span id="gl_rgb"></span><dl> <dt>**GL \_ RGB**</dt> </dl>                                      | 每個元素都是 RGB 三重。 它會轉換成浮點數，並藉由附加1.0 的 Alpha 來組合成 RGBA 元素。 接著，每個元件會乘以已簽署的縮放比例 GL \_ c \_ 規模、新增至帶正負號偏差 gl \_ c \_ 偏差，然後壓制至範圍 \[ 0，1 \] (查看 **glPixelTransfer**) 。<br/>                                                                                                                                                                                                                                            |
| <span id="GL_RGBA"></span><span id="gl_rgba"></span><dl> <dt>**GL \_ RGBA**</dt> </dl>                                   | 每個元素都是完整的 RGBA 元素。 它會轉換成浮點數格式。 接著，每個元件會乘以已簽署的縮放比例 GL \_ c \_ 規模、新增至帶正負號偏差 gl \_ c \_ 偏差，然後壓制至範圍 \[ 0，1 \] (查看 **glPixelTransfer**) 。<br/>                                                                                                                                                                                                                                                                                         |
| <span id="GL_LUMINANCE"></span><span id="gl_luminance"></span><dl> <dt>**GL \_ 亮度**</dt> </dl>                    | 每個元素都是單一的亮度值。 它會轉換成浮點數格式，然後將亮度值複寫三次（針對紅色、綠色和藍色），然後附加1.0 （Alpha），以組合成 RGBA 元素。 接著，每個元件會乘以已簽署的縮放比例 GL \_ c \_ 規模、新增至帶正負號偏差 gl \_ c \_ 偏差，然後壓制至範圍 \[ 0，1 \] (查看 [**glPixelTransfer**](glpixeltransfer.md)) 。<br/>                                                                                                                   |
| <span id="GL_LUMINANCE_ALPHA"></span><span id="gl_luminance_alpha"></span><dl> <dt>**GL \_ 亮度 \_ ALPHA**</dt> </dl> | 每個元素都是一組明亮度/Alpha 配對。 它會轉換為浮點格式，然後藉由針對紅色、綠色和藍色複寫亮度值三次，來組合成 RGBA 元素。 接著，每個元件會乘以已簽署的縮放比例 GL \_ c \_ 規模、新增至帶正負號偏差 gl \_ c \_ 偏差，然後壓制至範圍 \[ 0，1 \] (查看 **glPixelTransfer**) 。<br/>                                                                                                                                                                         |



 

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



| 名稱                                                                                                  | 意義                                                                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ 無效 \_ 列舉**</dt> </dl>      | *目標* 不是 GL \_ 紋理 \_ 1d。<br/>                                                                                                                                                                                                                             |
| <dl> <dt>**GL \_ 無效 \_ 列舉**</dt> </dl>      | *格式* 不是可接受的常數。<br/>                                                                                                                                                                                                                        |
| <dl> <dt>**GL \_ 無效 \_ 列舉**</dt> </dl>      | *類型* 不是可接受的常數。<br/>                                                                                                                                                                                                                          |
| <dl> <dt>**GL \_ 無效 \_ 列舉**</dt> </dl>      | *類型* 為 gl \_ 點陣圖， *格式* 不是 gl \_ 色彩 \_ 索引。<br/>                                                                                                                                                                                                  |
| <dl> <dt>**GL \_ 無效 \_ 值**</dt> </dl>     | *層級* 小於零或大於 log2 *max*，其中 *max* 是 GL \_ 最大紋理大小的傳回值 \_ \_ 。<br/>                                                                                                                                          |
| <dl> <dt>**GL \_ 無效 \_ 值**</dt> </dl>     | *xoffset* 小於 *b*，或 *位移*  +  *寬度* 大於 *wb*（其中 *w* 是 GL \_ 材質 \_ 寬度）， *b* 是 \_ \_ 要修改之紋理影像的 GL 材質框線寬度。<br/> 請注意， *w* 包含框線寬度的兩倍。<br/> |
| <dl> <dt>**GL \_ 無效 \_ 值**</dt> </dl>     | *寬度* 小於 *b*，其中 *b* 是材質陣列的框線寬度。<br/>                                                                                                                                                                            |
| <dl> <dt>**GL \_ 無效 \_ 值**</dt> </dl>     | *框線* 不是零或1。<br/>                                                                                                                                                                                                                                   |
| <dl> <dt>**GL \_ 不正確 \_ 操作**</dt> </dl> | 先前的 **glTexImage1D** 作業未定義 texure 陣列。<br/>                                                                                                                                                                                    |
| <dl> <dt>**GL \_ 不正確 \_ 操作**</dt> </dl> | 呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。<br/>                                                                                                                                    |



## <a name="remarks"></a>備註

使用 [**glEnable**](glenable.md) 和 **glDisable** 搭配引數 GL 紋理1d，可啟用基本物件的一維紋理 \_ \_ 。 在紋理期間，指定之材質影像的一部分會對應到每個已啟用的基本類型。 您可以使用 **glTexSubImage1D** 函式，為紋理指定現有一維紋理影像的連續子影像。

*圖元* 所參考的材質會將現有材質陣列的區域取代為 *xoffset* 和 *xoffset* + (*寬度* 1) 包含的 *x* 索引。 此區域無法在原始指定的材質陣列範圍之外包含任何材質。

指定 *寬度* 為零的子影像沒有任何作用，也不會產生錯誤。

紋理在色彩索引模式中沒有任何作用。

一般而言，材質影像可以用與 [**glDrawPixels**](gldrawpixels.md) 命令中的圖元相同的資料格式表示，但 \_ 無法使用 gl 樣板 \_ 索引和 gl \_ 深度 \_ 元件。 [**GlPixelStore**](glpixelstore-functions.md)和 [**glPixelTransfer**](glpixeltransfer.md)模式會以其影響 **glDrawPixels** 的確切方式來影響紋理影像。

下列函式會取出與 **glTexSubImage1D** 相關的資訊：

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

[**glEnable**](glenable.md)
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

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> <dt>

[**glTexParameter**](gltexparameter-functions.md)
</dt> <dt>

[**glTexSubImage2D**](gltexsubimage2d.md)
</dt> </dl>

 

 





