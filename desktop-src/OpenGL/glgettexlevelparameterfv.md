---
title: 'glGetTexLevelParameterfv 函式 (Gl) '
description: 'GlGetTexLevelParameterfv 和 glGetTexLevelParameteriv 函數會傳回特定詳細資料層級的材質參數值。 |glGetTexLevelParameterfv 函式 (Gl) '
ms.assetid: 5ea91f2e-c0cd-41ee-be95-df096f1c78ef
keywords:
- glGetTexLevelParameterfv 函式 OpenGL
topic_type:
- apiref
api_name:
- glGetTexLevelParameterfv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b4068b6544c334c4ca1c8e6640ccb4752669240cdde16d0522a4e13d06ebc8c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118359774"
---
# <a name="glgettexlevelparameterfv-function"></a>glGetTexLevelParameterfv 函式

**GlGetTexLevelParameterfv** 和 [**glGetTexLevelParameteriv**](glgettexlevelparameteriv.md)函數會傳回特定詳細資料層級的材質參數值。

## <a name="syntax"></a>語法


```C++
void WINAPI glGetTexLevelParameterfv(
   GLenum  target,
   GLint   level,
   GLenum  pname,
   GLfloat *params
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*目標* 
</dt> <dd>

目標材質的符號名稱： GL \_ 紋理 \_ 1D、gl \_ 材質 \_ 2d、gl \_ proxy \_ 材質 \_ 1d 或 gl \_ proxy \_ 材質 \_ 2d。

</dd> <dt>

*level* 
</dt> <dd>

所需影像的詳細層級編號。 層級0是基底映射層級。 層級 *n* 是第 *n* 個 mipmap 縮減影像。

</dd> <dt>

*pname* 
</dt> <dd>

材質參數的符號名稱。 接受下列參數名稱。



| 值                                                                                                                                                                                                  | 意義                                                                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_TEXTURE_WIDTH"></span><span id="gl_texture_width"></span><dl> <dt>**GL \_ 材質 \_ 寬度**</dt> </dl>                                | *Params* 參數會傳回包含紋理影像寬度的單一值。 此值包含紋理影像的框線。<br/>                                                                                                                                          |
| <span id="GL_TEXTURE_HEIGHT"></span><span id="gl_texture_height"></span><dl> <dt>**GL \_ 材質 \_ 高度**</dt> </dl>                             | *Params* 參數會傳回單一值，其中包含紋理影像的高度。 此值包含紋理影像的框線。<br/>                                                                                                                                         |
| <span id="GL_TEXTURE_INTERNAL_FORMAT"></span><span id="gl_texture_internal_format"></span><dl> <dt>**GL \_ 材質 \_ 內部 \_ 格式**</dt> </dl> | *Params* 參數會傳回單一值，以描述材質的材質格式。<br/>                                                                                                                                                                                         |
| <span id="GL_TEXTURE_BORDER"></span><span id="gl_texture_border"></span><dl> <dt>**GL \_ 材質 \_ 框線**</dt> </dl>                             | *Params* 參數會傳回單一值：紋理影像框線的寬度（以圖元為單位）。<br/>                                                                                                                                                                                 |
| <span id="GL_TEXTURE_RED_SIZE"></span><span id="gl_texture_red_size"></span><dl> <dt>**GL \_ 材質 \_ 紅色 \_ 大小**</dt> </dl>                      | 材質 red 元件的內部儲存體解析。 OpenGL 所選擇的解析度將會與使用者使用 [**glTexImage1D**](glteximage1d.md) 或 [**glTexImage2D**](glteximage2d.md)的元件引數所要求的解析度相符。<br/>       |
| <span id="GL_TEXTURE_GREEN_SIZE"></span><span id="gl_texture_green_size"></span><dl> <dt>**GL \_ 材質 \_ 綠 \_ 尺寸**</dt> </dl>                | 材質綠色元件的內部儲存體解析。 OpenGL 所選擇的解析度將會與使用者使用 [**glTexImage1D**](glteximage1d.md) 或 [**glTexImage2D**](glteximage2d.md)的元件引數所要求的解析度相符。<br/>     |
| <span id="GL_TEXTURE_BLUE_SIZE"></span><span id="gl_texture_blue_size"></span><dl> <dt>**GL \_ 材質 \_ 藍色 \_ 大小**</dt> </dl>                   | 材質藍色元件的內部儲存體解析。 OpenGL 所選擇的解析度將會與使用者使用 [**glTexImage1D**](glteximage1d.md) 或 [**glTexImage2D**](glteximage2d.md)的元件引數所要求的解析度相符。<br/>      |
| <span id="GL_TEXTURE_ALPHA_SIZE"></span><span id="gl_texture_alpha_size"></span><dl> <dt>**GL \_ 紋理 \_ ALPHA \_ 大小**</dt> </dl>                | 材質 Alpha 元件的內部儲存體解析。 OpenGL 所選擇的解析度將會與使用者使用 [**glTexImage1D**](glteximage1d.md) 或 [**glTexImage2D**](glteximage2d.md)的元件引數所要求的解析度相符。<br/>     |
| <span id="GL_TEXTURE_LUMINANCE_SIZE"></span><span id="gl_texture_luminance_size"></span><dl> <dt>**GL \_ 紋理 \_ 亮度 \_ 大小**</dt> </dl>    | 材質之明亮元件的內部儲存體解析。 OpenGL 所選擇的解析度將會與使用者使用 [**glTexImage1D**](glteximage1d.md) 或 [**glTexImage2D**](glteximage2d.md)的元件引數所要求的解析度相符。<br/> |
| <span id="GL_TEXTURE_INTENSITY_SIZE"></span><span id="gl_texture_intensity_size"></span><dl> <dt>**GL \_ 材質 \_ 濃度 \_ 大小**</dt> </dl>    | 材質濃度元件的內部儲存體解析。 OpenGL 所選擇的解析度將會與使用者使用 [**glTexImage1D**](glteximage1d.md) 或 [**glTexImage2D**](glteximage2d.md)的元件引數所要求的解析度相符。<br/> |
| <span id="GL_TEXTURE_COMPONENTS"></span><span id="gl_texture_components"></span><dl> <dt>**GL \_ 材質 \_ 元件**</dt> </dl>                 | *Params* 參數會傳回單一值：材質影像中的元件數目。<br/>                                                                                                                                                                                          |



 

</dd> <dt>

*params* 
</dt> <dd>

傳回要求的資料。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="error-codes"></a>錯誤碼

[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。



| Name                                                                                                  | 意義                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ 無效 \_ 列舉**</dt> </dl>      | *target* 或 *pname* 不是可接受的值。<br/>                                                                             |
| <dl> <dt>**GL \_ 無效 \_ 值**</dt> </dl>     | *層級* 小於零或大於 *log* 2 *(max)*，其中 *max* 是 GL \_ 最大 \_ 紋理大小的傳回值 \_ 。<br/>      |
| <dl> <dt>**GL \_ 不正確 \_ 操作**</dt> </dl> | 呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。<br/> |



## <a name="remarks"></a>備註

**GlGetTexLevelParameter** 函式會針對特定的詳細層級值（指定為 *層級*），傳回 *params* 材質參數值。 *目標* 參數會定義目標材質，也就是 gl \_ 紋理 \_ 1d、GL \_ 材質 \_ 2d、gl \_ proxy \_ 材質 \_ 1d 或 gl \_ proxy \_ 材質 \_ 2d，以指定一維或二維紋理。 *Pname* 參數會指定將傳回其值的材質參數。

如果產生錯誤，則不會對 *參數* 的內容進行任何變更。

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

[**glGetTexParameter**](glgettexparameter.md)
</dt> <dt>

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> <dt>

[**glTexParameter**](gltexparameter-functions.md)
</dt> </dl>

 

 





