---
title: 'glCopyTexImage2D 函式 (Gl) '
description: GlCopyTexImage2D 函式會將圖元從畫面格緩衝區複製到二維紋理影像。
ms.assetid: 4b9d7be6-054d-4590-b3f0-a2a670786c4b
keywords:
- glCopyTexImage2D 函式 OpenGL
topic_type:
- apiref
api_name:
- glCopyTexImage2D
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e91481e94d247f5572ac2a65093c4af825c720200aee6daf3e429fad2a70886
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118617211"
---
# <a name="glcopyteximage2d-function"></a>glCopyTexImage2D 函式

**GlCopyTexImage2D** 函式會將圖元從畫面格緩衝區複製到二維紋理影像。

## <a name="syntax"></a>語法


```C++
void WINAPI glCopyTexImage2D(
   GLenum  target,
   GLint   level,
   GLenum  internalFormat,
   GLint   x,
   GLint   y,
   GLsizei width,
   GLsizei height,
   GLint   border
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*目標* 
</dt> <dd>

將變更影像資料的目標。 必須具有值 GL \_ 紋理 \_ 2d。

</dd> <dt>

*level* 
</dt> <dd>

詳細資料層級數目。 層級0是基底映射。 層級 *n* 是第 *n* 個 mipmap 縮減影像。

</dd> <dt>

*internalFormat* 
</dt> <dd>

材質資料的內部格式和解析度。 *InternalFormat* 不接受值1、2、3和4。 參數可以採用下列其中一個符號值。



| 常數                 | R 位 | G 位 | B 位 | 位 | L 位 | I 位 |
|--------------------------|--------|--------|--------|--------|--------|--------|
| GL \_ ALPHA                |        |        |        |        |        |        |
| GL \_ ALPHA4               |        |        |        | 4      |        |        |
| GL \_ ALPHA8               |        |        |        | 8      |        |        |
| GL \_ ALPHA12              |        |        |        | 12     |        |        |
| GL \_ ALPHA16              |        |        |        | 16     |        |        |
| GL \_ 亮度            |        |        |        |        |        |        |
| GL \_ LUMINANCE4           |        |        |        |        | 4      |        |
| GL \_ LUMINANCE8           |        |        |        |        | 8      |        |
| GL \_ LUMINANCE12          |        |        |        |        | 12     |        |
| GL \_ LUMINANCE16          |        |        |        |        | 16     |        |
| GL \_ 亮度 \_ ALPHA     |        |        |        |        |        |        |
| GL \_ LUMINANCE4 \_ ALPHA4   |        |        |        | 4      | 4      |        |
| GL \_ LUMINANCE6 \_ ALPHA2   |        |        |        | 2      | 6      |        |
| GL \_ LUMINANCE8 \_ ALPHA8   |        |        |        | 8      | 8      |        |
| GL \_ LUMINANCE12 \_ ALPHA4  |        |        |        | 4      | 12     |        |
| GL \_ LUMINANCE12 \_ ALPHA12 |        |        |        | 12     | 12     |        |
| GL \_ LUMINANCE16 \_ ALPHA16 |        |        |        | 16     | 16     |        |
| GL \_ 濃度            |        |        |        |        |        |        |
| GL \_ INTENSITY4           |        |        |        |        |        | 4      |
| GL \_ INTENSITY8           |        |        |        |        |        | 8      |
| GL \_ INTENSITY12          |        |        |        |        |        | 12     |
| GL \_ INTENSITY16          |        |        |        |        |        | 16     |
| GL \_ RGB                  |        |        |        |        |        |        |
| GL \_ R3 \_ G3 \_ B2           | 3      | 3      | 2      |        |        |        |
| GL \_ RGB4                 | 4      | 4      | 4      |        |        |        |
| GL \_ RGB5                 | 5      | 5      | 5      |        |        |        |
| GL \_ RGB8                 | 8      | 8      | 8      |        |        |        |
| GL \_ RGB10                | 10     | 10     | 10     |        |        |        |
| GL \_ RGB12                | 12     | 12     | 12     |        |        |        |
| GL \_ RGB16                | 16     | 16     | 16     |        |        |        |
| GL \_ RGBA                 |        |        |        |        |        |        |
| GL \_ RGBA2                | 2      | 2      | 2      | 2      |        |        |
| GL \_ RGBA4                | 4      | 4      | 4      | 4      |        |        |
| GL \_ RGB5 \_ A1             | 5      | 5      | 5      | 1      |        |        |
| GL \_ RGBA8                | 8      | 8      | 8      | 8      |        |        |
| GL \_ RGB10 \_ A2            | 10     | 10     | 10     | 2      |        |        |
| GL \_ RGBA12               | 12     | 12     | 12     | 12     |        |        |
| GL \_ RGBA16               | 16     | 16     | 16     | 16     |        |        |



 

</dd> <dt>

*x* 
</dt> <dd>

要複製之圖元矩形區域左下角的視窗 x 平面座標。

</dd> <dt>

*y* 
</dt> <dd>

要複製之圖元矩形區域左下角的視窗 y 平面座標。

</dd> <dt>

*width* (寬度) 
</dt> <dd>

材質影像的寬度。 必須為 \* 某個整數 *n* 的 2n + 2 個 *框線*。

</dd> <dt>

*height* (高度) 
</dt> <dd>

材質影像的高度。 必須為 \* 某個整數 *n* 的 2n + 2 個 *框線*。

</dd> <dt>

*邊境* 
</dt> <dd>

框線的寬度。 必須是零或1。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="error-codes"></a>錯誤碼

[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。



| 名稱                                                                                                  | 意義                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ 無效 \_ 列舉**</dt> </dl>      | *目標* 不是可接受的值。<br/>                                                                                                               |
| <dl> <dt>**GL \_ 無效 \_ 值**</dt> </dl>     | *層級* 小於零或大於 log2 *max*，其中 *max* 是 GL \_ 最大紋理大小的傳回值 \_ \_ 。<br/>                               |
| <dl> <dt>**GL \_ 無效 \_ 值**</dt> </dl>     | *框線* 不是零或1。<br/>                                                                                                                       |
| <dl> <dt>**GL \_ 無效 \_ 值**</dt> </dl>     | *寬度* 小於零、大於 2 + GL \_ 最大 \_ 紋理 \_ 大小，或 *寬度* 不能表示為 \* 某個整數 *n* 的 2n + 2 *框線*。<br/> |
| <dl> <dt>**GL \_ 不正確 \_ 操作**</dt> </dl> | 呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。<br/>                        |



## <a name="remarks"></a>備註

**GlCopyTexImage2D** 函式會使用來自目前畫面格緩衝區的圖元來定義二維紋理影像，而不是從主儲存體（例如 [**glTexImage2D**](glteximage2d.md)的情況下）。

使用以 *層級* 指定的 mipmap 層級，會將材質陣列定義為圖元的矩形，其左上角位於座標 *x* 和 *y*、寬度等於 *寬度* + (2 \* *框線*) ，以及高度等於 *高度* + (2 \* *框線*) 。 材質陣列的內部格式是以 *internalFormat* 參數指定。

**GlCopyTexImage2D** 函式會使用與 [**glCopyPixels**](glcopypixels.md)相同的方式來處理資料列中的圖元，但在最後轉換圖元之前，所有圖元元件值都會壓制至範圍 \[ 0、1， \] 並轉換成紋理陣列中儲存的材質內部格式。 圖元排序是以對應于較低 *s* 和 *t* 紋理座標的較低 *x* 和 *y* 座標來決定。 如果目前畫面格緩衝區中指定資料列內的任何圖元都在與目前轉譯內容相關聯的視窗之外，則其值為未定義。

您不能在顯示清單中包含 **glCopyTexImage2D** 的呼叫。

> [!Note]  
> **GlCopyTexImage2D** 函數僅適用于 OpenGL 1.1 版或更新版本。

 

紋理在色彩索引模式中沒有任何作用。 [**GlPixelStore**](glpixelstore-functions.md)和 [**glPixelTransfer**](glpixeltransfer.md)函式會以完全影響 [**glDrawPixels**](gldrawpixels.md)的方式來影響紋理影像。

下列函式會抓取 **glCopyTexImage2D** 的相關資訊：

[](glisenabled.md)具有引數 GL \_ 材質 \_ 2d 的 glIsEnabled

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

[**glCopyTexImage1D**](glcopyteximage1d.md)
</dt> <dt>

[**glDrawPixels**](gldrawpixels.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glFog**](glfog.md)
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
</dt> </dl>

 

 





