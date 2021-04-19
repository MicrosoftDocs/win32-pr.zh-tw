---
title: 'glGetTexParameterfv 函式 (Gl) '
description: 'GlGetTexParameterfv 和 glGetTexParameteriv 函數會傳回材質參數值。 |glGetTexParameterfv 函式 (Gl) '
ms.assetid: 616292ea-222c-4efe-bb69-3058d9c99910
keywords:
- glGetTexParameterfv 函式 OpenGL
topic_type:
- apiref
api_name:
- glGetTexParameterfv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b0af6e5fd91d38240dd3463b9440333b5da431d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106993835"
---
# <a name="glgettexparameterfv-function"></a>glGetTexParameterfv 函式

**GlGetTexParameterfv** 和 [**glGetTexParameteriv**](glgettexparameteriv.md)函數會傳回材質參數值。

## <a name="syntax"></a>語法


```C++
void WINAPI glGetTexParameterfv(
   GLenum  target,
   GLenum  pname,
   GLfloat *params
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*目標* 
</dt> <dd>

目標材質的符號名稱。 \_ \_ 已接受 gl 材質1D 和 gl \_ 材質 \_ 2d。

</dd> <dt>

*pname* 
</dt> <dd>

材質參數的符號名稱。 接受下列值。



| 值                                                                                                                                                                                         | 意義                                                                                                                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_TEXTURE_MAG_FILTER"></span><span id="gl_texture_mag_filter"></span><dl> <dt>**GL \_ 紋理 \_ MAG \_ 篩選**</dt> </dl>       | 傳回單一值材質放大篩選準則（符號常數）。<br/>                                                                                                                                                                                                                                                                                                      |
| <span id="GL_TEXTURE_MIN_FILTER"></span><span id="gl_texture_min_filter"></span><dl> <dt>**GL \_ 材質 \_ 最小 \_ 篩選**</dt> </dl>       | 傳回單一值紋理縮制篩選（符號常數）。<br/>                                                                                                                                                                                                                                                                                                       |
| <span id="GL_TEXTURE_WRAP_S"></span><span id="gl_texture_wrap_s"></span><dl> <dt>**GL \_ 材質 \_ 換行 \_**</dt> </dl>                   | 傳回紋理座標 *s* 的單一值換行函式，這是一個符號常數。<br/>                                                                                                                                                                                                                                                                                      |
| <span id="GL_TEXTURE_WRAP_T"></span><span id="gl_texture_wrap_t"></span><dl> <dt>**GL \_ 紋理 \_ WRAP \_ T**</dt> </dl>                   | 傳回紋理座標 *t*（符號常數）的單一值包裝函式。<br/>                                                                                                                                                                                                                                                                                      |
| <span id="GL_TEXTURE_BORDER_COLOR"></span><span id="gl_texture_border_color"></span><dl> <dt>**GL \_ 紋理 \_ 框線 \_ 色彩**</dt> </dl> | 傳回四個整數或浮點數，這些數位組成材質框線的 RGBA 色彩。 浮點值會傳回範圍 \[ 0，1 \] 。 整數值會傳回為內部浮點表示的線性對應，因此，1.0 對應至最正面的可表示整數，而-1.0 對應至最大的可表示整數。<br/> |
| <span id="GL_TEXTURE_PRIORITY"></span><span id="gl_texture_priority"></span><dl> <dt>**GL \_ 材質 \_ 優先順序**</dt> </dl>              | 傳回目標材質 (的居住優先權，或系結至它) 的命名材質。 初始值為1。 請參閱 [**glPrioritizeTextures**](glprioritizetextures.md)。<br/>                                                                                                                                                                                                        |
| <span id="GL_TEXTURE_RESIDENT"></span><span id="gl_texture_resident"></span><dl> <dt>**GL \_ 材質 \_ 常駐**</dt> </dl>              | 傳回目標材質的居住狀態。 如果在 params 中傳回的值為 GL \_ ，則紋理會在材質記憶體中。 請參閱 [**glAreTexturesResident**](glaretexturesresident.md)。<br/>                                                                                                                                                                           |



 

</dd> <dt>

*params* 
</dt> <dd>

傳回材質參數。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="error-codes"></a>錯誤碼

[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。



| Name                                                                                                  | 意義                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ 無效 \_ 列舉**</dt> </dl>      | *目標* 或 *名稱* 不是可接受的值。<br/>                                                                              |
| <dl> <dt>**GL \_ 不正確 \_ 操作**</dt> </dl> | 呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。<br/> |



## <a name="remarks"></a>備註

**GlGetTexParameter** 函式會以 *params* 傳回指定為 *pname* 的材質參數值或值。 *目標* 參數會定義目標材質，也就是 gl \_ 材質 \_ 1d 或 gl \_ 材質 \_ 2d，以指定一維或二維紋理。 *Pname* 參數會接受與 [**glTexParameter**](gltexparameter-functions.md)相同的符號，並具有相同的解釋。

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

[**glTexParameter**](gltexparameter-functions.md)
</dt> </dl>

 

 





