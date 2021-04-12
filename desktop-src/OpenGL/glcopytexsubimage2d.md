---
title: 'glCopyTexSubImage2D 函式 (Gl) '
description: GlCopyTexSubImage2D 函式會從畫面格緩衝區複製二維紋理影像的子影像。
ms.assetid: cbb644d4-6a23-4d66-8599-5f8b48e9b91f
keywords:
- glCopyTexSubImage2D 函式 OpenGL
topic_type:
- apiref
api_name:
- glCopyTexSubImage2D
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c966d031bb154b59cc54ae2e5d254347aa88d2a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384818"
---
# <a name="glcopytexsubimage2d-function"></a>glCopyTexSubImage2D 函式

**GlCopyTexSubImage2D** 函式會從畫面格緩衝區複製二維紋理影像的子影像。

## <a name="syntax"></a>語法


```C++
void WINAPI glCopyTexSubImage2D(
   GLenum  target,
   GLint   level,
   GLint   xoffset,
   GLint   yoffset,
   GLint   x,
   GLint   y,
   GLsizei width,
   GLsizei height
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

*xoffset* 
</dt> <dd>

紋理陣列內 *x* 方向的材質位移。

</dd> <dt>

*yoffset* 
</dt> <dd>

紋理陣列中 *y* 方向的材質位移。

</dd> <dt>

*x* 
</dt> <dd>

要複製之圖元資料列左下角的視窗 x 平面座標。

</dd> <dt>

*y* 
</dt> <dd>

要複製之圖元資料列左下角的視窗 y 平面座標。

</dd> <dt>

*width* (寬度) 
</dt> <dd>

材質影像的子影像寬度。 指定寬度為零的材質子影像沒有任何作用。

</dd> <dt>

*height* (高度) 
</dt> <dd>

材質影像子影像的高度。 指定寬度為零的材質子影像沒有任何作用。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="error-codes"></a>錯誤碼

[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。



| Name                                                                                                  | 意義                                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ 無效 \_ 列舉**</dt> </dl>      | *目標* 不是可接受的值。<br/>                                                                                                                                                                                                                                                                              |
| <dl> <dt>**GL \_ 無效 \_ 值**</dt> </dl>     | *層級* 小於零或大於 *log* 2 (*max*) ，其中 *max* 是 GL \_ 最大 \_ 紋理大小的傳回值 \_ 。<br/>                                                                                                                                                                                          |
| <dl> <dt>**GL \_ 無效 \_ 值**</dt> </dl>     | *xoffset* 小於 *框線* 或 (*xoffset*  +  *寬度*)  (大於框線  +  ) 、 *yoffset* 小於 *框線*，或 (*yoffset*  +  *高度*) 大於 (*h*  +  *框線*) ，其中 *w* 是 gl \_ 紋理 \_ 寬度和 *框線* 是 gl \_ 材質 \_ 框線。 請注意， *w* 包含 *框線* 寬度的兩倍。<br/> |
| <dl> <dt>**GL \_ 無效 \_ 值**</dt> </dl>     | *寬度* 小於 *框線* 或 *y* 小於 *框線*，其中 *框線* 是材質陣列的框線寬度。<br/>                                                                                                                                                                                           |
| <dl> <dt>**GL \_ 不正確 \_ 操作**</dt> </dl> | 材質陣列未由先前的 [**glTexImage1D**](glteximage1d.md) 作業定義。<br/>                                                                                                                                                                                                                  |
| <dl> <dt>**GL \_ 不正確 \_ 操作**</dt> </dl> | 呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。<br/>                                                                                                                                                                                       |



## <a name="remarks"></a>備註

**GlCopyTexSubImage2D** 函式會將二維材質影像的矩形部分取代為目前畫面格緩衝區的圖元，而不是從主儲存體（例如 [**glTexSubImage2D**](gltexsubimage2d.md)的情況下）。

以 *x* 和 *y* 視窗座標為開頭的圖元矩形，其維度 *寬度* 和 *高度* 會以 *xoffset* 至 *xoffset* + (*寬度* -1) 的索引來取代材質陣列的部分， *而索引則* 是透過 *yoffset* + (*寬度* -1) 在 *層級* 所指定的 mipmap 層級進行。 紋理陣列中的目的地矩形不能包含原始指定之材質陣列以外的任何材質。

**GlCopyTexSubImage2D** 函式會使用與 [**glCopyPixels**](glcopypixels.md)相同的方式來處理資料列中的圖元，但在圖元的最後轉換之前，所有圖元元件值都會壓制至範圍 \[ 0、1， \] 並轉換為紋理陣列中儲存的材質內部格式。 圖元順序是以對應于較低材質座標的較低 *x* 座標來決定。 如果目前畫面格緩衝區中指定資料列內的任何圖元都在與目前轉譯內容相關聯的視窗之外，則其值為未定義。

如果目前畫面格緩衝區之指定矩形內的任何圖元都在與目前轉譯內容相關聯的讀取視窗之外，則為這些圖元取得的值未定義。 不會變更指定之材質陣列的 *internalFormat*、 *width*、 *height* 或 *border* 參數，也不會材質指定之材質子影像以外的值。

您不能在顯示清單中包含 **glCopyTexSubImage2D** 的呼叫。

> [!Note]  
> **GlCopyTexSubImage2D** 函數僅適用于 OpenGL 1.1 版或更新版本。

 

紋理在色彩索引模式中沒有任何作用。 [**GlPixelStore**](glpixelstore-functions.md)和 [**glPixelTransfer**](glpixeltransfer.md)函式會以實際的方式影響材質影像，其影響使用 [**glDrawPixels**](gldrawpixels.md)繪製圖元的方式。

下列函式會取出與 **glCopyTexSubImage2D** 相關的資訊：

[**glGetTexImage**](glgetteximage.md)

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

[**glCopyPixels**](glcopypixels.md)
</dt> <dt>

[**glCopyTexSubImage1D**](glcopytexsubimage1d.md)
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

[**glTexImage2D**](glteximage2d.md)
</dt> <dt>

[**glTexSubImage2D**](gltexsubimage2d.md)
</dt> <dt>

[**glTexParameter**](gltexparameter-functions.md)
</dt> </dl>

 

 





