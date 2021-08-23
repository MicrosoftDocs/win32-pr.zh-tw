---
title: 'glFogfv 函式 (Gl) '
description: 'GlFogfv 函數會指定霧化參數。 |glFogfv 函式 (Gl) '
ms.assetid: a2243ff4-4f3a-4b8c-b4fb-ce2cd74815e4
keywords:
- glFogfv 函式 OpenGL
topic_type:
- apiref
api_name:
- glFogfv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5da9c921af1a69e41c1fd38a633fccad43cd685974be2de81f4275b8388a496f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119625368"
---
# <a name="glfogfv-function"></a>glFogfv 函式

**GlFogfv** 函數會指定霧化參數。

## <a name="syntax"></a>語法


```C++
void WINAPI glFogfv(
         GLenum  pname,
   const GLfloat *params
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pname* 
</dt> <dd>

指定霧化參數。

接受下列其中一個值。



| 值                                                                                                                                                             | 意義                                                                                                                                                                                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_FOG_MODE"></span><span id="gl_fog_mode"></span><dl> <dt>**GL \_ 霧化 \_ 模式**</dt> </dl>          | *Params* 參數是浮點值，可指定用來計算霧化 blend 因數 *f* 的方程式。 接受三個符號常數： GL \_ 線性、gl \_ EXP 和 GL \_ EXP2。 對應到這些符號常數的方會定義于下列備註區段中。 預設的霧化模式為 GL \_ EXP。<br/>                                                                           |
| <span id="GL_FOG_DENSITY"></span><span id="gl_fog_density"></span><dl> <dt>**GL \_ 霧化 \_ 密度**</dt> </dl> | *Params* 參數是浮點值，可指定 *密度*、兩個指數霧化方程式中所使用的霧化密度。 只接受非負的密度。 預設的霧化密度為1.0。<br/>                                                                                                                                                                                                              |
| <span id="GL_FOG_START"></span><span id="gl_fog_start"></span><dl> <dt>**GL \_ 霧化 \_ 開始**</dt> </dl>       | *Params* 參數是浮點值，可指定線性霧化方程式中所使用的 *開始* 和近距離。 預設接近距離為0.0。<br/>                                                                                                                                                                                                                                                            |
| <span id="GL_FOG_END"></span><span id="gl_fog_end"></span><dl> <dt>**GL \_ 霧化 \_ 結束**</dt> </dl>             | *Params* 參數是浮點值，可指定線性霧化方程式中所使用的 *結束* 距離。 預設距離為1.0。<br/>                                                                                                                                                                                                                                                                |
| <span id="GL_FOG_INDEX"></span><span id="gl_fog_index"></span><dl> <dt>**GL \_ 霧化 \_ 索引**</dt> </dl>       | *Params* 參數是指定 *i*<sub>f</sub>的浮點數值（霧化色彩索引）。 預設的霧化索引為0.0。<br/>                                                                                                                                                                                                                                                                                     |
| <span id="GL_FOG_COLOR"></span><span id="gl_fog_color"></span><dl> <dt>**GL \_ 霧化 \_ 色彩**</dt> </dl>       | *Params* 參數包含四個浮點值，可指定 *C*<sub>f</sub> （霧化色彩）。 整數值會以線性方式對應，因此最正面的可表示值會對應至1.0，而最大的可表示值會對應至-1.0。 浮點值會直接對應。 轉換之後，會將所有色彩元件壓制至範圍 \[ 0、1 \] 。 預設的霧化色彩是 (0、0、0、0) 。<br/> |



 

</dd> <dt>

*params* 
</dt> <dd>

指定要指派給 *pname* 的值。 GL \_ 霧化 \_ 色彩需要四個值的陣列。 所有其他參數都接受僅包含單一值的陣列。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="error-codes"></a>錯誤碼

[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。



| 名稱                                                                                                  | 意義                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ 無效 \_ 列舉**</dt> </dl>      | *pname* 不是可接受的值。<br/>                                                                                         |
| <dl> <dt>**GL \_ 不正確 \_ 操作**</dt> </dl> | 呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。<br/> |



## <a name="remarks"></a>備註

您可以使用引數 GL 霧化來啟用和停用 [**glEnable**](glenable.md) 和 [**glDisable**](gldisable.md)的霧化 \_ 。 啟用時，霧化會影響點陣化幾何、點陣圖和圖元區塊，但不會影響緩衝區清除作業。

**GlFogfv** 函式會將 *params* 中的值或值指派給 *pname* 所指定的霧化參數。

霧化會使用混色因數 *f* 來混合霧化色彩與每個柵格化圖元片段的 posttexturing 色彩。 第三種方式是以三種方式的其中一種來計算，視霧化 *模式而定* 。 讓 *z* 成為從原點到所 fogged 之片段的眼睛距離。 GL \_ 線性模糊的方程式如下：

![顯示 GL_LINEAR 霧化值的方程式。](images/fog01.png)

GL \_ EXP 霧化的方程式如下：

![顯示 GL_EXP 霧化模式中混合因數值的方程式。](images/fog02.png)

GL \_ EXP2 霧化的方程式是：

![顯示 GL_EXP2 霧化模式中混合因數值的方程式。](images/fog03.png)

不論霧化模式為何， *f* 都是在計算後壓制至範圍 \[ 0、1 \] 。 然後，如果 OpenGL 處於 RGBA 色彩模式，則會將片段的色彩 *C*<sub>r</sub> 取代為

![顯示 fogged 片段色彩的方程式，做為混色因數和霧化色彩的函式。](images/fog04.png)

在色彩索引模式中，片段的色彩索引 *i*<sub>r</sub> 會取代為

![顯示 fogged 片段之色彩索引的方程式，做為混合因數和索引色彩的函式。](images/fog05.png)

下列函式會取出與 **glFog** 函數相關的資訊：

[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 霧化 \_ 色彩的 glGet

具有引數 GL \_ 霧化 \_ 索引的 glGet

具有引數 GL \_ 霧化 \_ 密度的 glGet

具有引數 GL \_ 霧化 \_ 開始的 glGet

具有引數 GL \_ 霧化 \_ END 的 glGet

具有引數 GL \_ 霧化 \_ 模式的 glGet

[](glisenabled.md)具有引數 GL \_ 霧化的 glIsEnabled

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

[**glDisable**](gldisable.md)
</dt> <dt>

[**glEnable**](glenable.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> </dl>

 

 





