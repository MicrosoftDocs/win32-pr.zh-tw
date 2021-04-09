---
title: 'glPushAttrib 函式 (Gl) '
description: 推送屬性堆疊。
ms.assetid: 3c7b93cc-2112-4771-b422-a244821447e5
keywords:
- glPushAttrib 函式 OpenGL
topic_type:
- apiref
api_name:
- glPushAttrib
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e0bc15b85ddca3bdbe5f6774b5368c6f0cde8dd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024779"
---
# <a name="glpushattrib-function"></a>glPushAttrib 函式

推送屬性堆疊。

## <a name="syntax"></a>語法


```C++
void WINAPI glPushAttrib(
   GLbitfield mask
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*面具* 
</dt> <dd>

表示要儲存哪些屬性的遮罩。 符號遮罩常數和其相關聯的 OpenGL 狀態如下 (縮排的段落會列出哪些屬性會儲存) ：

<dl> <dt>

<span id="GL_ACCUM_BUFFER_BIT_"></span><span id="gl_accum_buffer_bit_"></span>GL \_ ACCUM \_ 緩衝區 \_ 位 
</dt> <dd>

累積緩衝區清除值

</dd> <dt>

<span id="GL_COLOR_BUFFER_BIT"></span><span id="gl_color_buffer_bit"></span>GL \_ 色彩 \_ 緩衝區 \_ 位
</dt> <dd>

GL \_ ALPHA \_ 測試啟用位

Alpha 測試函數和參考值

GL \_ BLEND 啟用位

混合來源和目的地函數

GL \_ 遞色啟用位

GL \_ 描繪 \_ 緩衝區設定

GL \_ 邏輯 \_ OP 啟用位

邏輯 op 函數

色彩模式和索引模式清除值

色彩模式和索引模式 writemasks

</dd> <dt>

<span id="GL_CURRENT_BIT"></span><span id="gl_current_bit"></span>GL \_ 目前 \_ 位
</dt> <dd>

目前的 RGBA 色彩

目前的色彩索引

目前的一般向量

目前的材質座標

目前的點陣位置 GL \_ 目前的 \_ 點陣 \_ 位置 \_ 有效旗標

與目前點陣位置相關聯的 RGBA 色彩

與目前點陣位置相關聯的色彩索引

與目前點陣位置相關聯的材質座標

GL \_ EDGE \_ 旗標旗標

</dd> <dt>

<span id="GL_DEPTH_BUFFER_BIT"></span><span id="gl_depth_buffer_bit"></span>GL \_ 深度 \_ 緩衝區 \_ 位
</dt> <dd>

GL \_ 深度 \_ 測試啟用位

深度緩衝區測試函式

深度緩衝區清除值

GL \_ 深度 \_ WRITEMASK 啟用位

</dd> <dt>

<span id="GL_ENABLE_BIT"></span><span id="gl_enable_bit"></span>GL \_ 啟用 \_ 位
</dt> <dd>

GL \_ ALPHA \_ 測試旗標

GL \_ 自動 \_ 正常旗標

GL \_ BLEND 旗標

啟用使用者可定義裁剪平面的位

GL \_ 色彩 \_ 材質

GL \_ 挑選 \_ 臉部旗標

GL \_ 深度 \_ 測試旗標

GL \_ 遞色旗標

GL \_ 霧化旗標

GL \_ 燈 0 <= *i* < GL \_ 最大 \_ 燈

GL \_ 照明旗標

GL \_ 行 \_ 平滑旗標

GL \_ 線 \_ STIPPLE 旗標

GL \_ 色彩 \_ 邏輯 \_ OP 旗標

GL \_ 索引 \_ 邏輯 \_ OP 旗標

GL \_ MAP1 \_ x，其中 x 是地圖類型

GL \_ list.map2 \_ x，其中 x 是地圖類型

GL \_ 標準化旗標

GL \_ 點 \_ 平滑旗標

GL \_ 多邊形 \_ 位移 \_ 線旗標

GL \_ 多邊形 \_ 位移 \_ 填滿旗標

GL \_ 多邊形 \_ 位移 \_ 點旗標

GL \_ 多邊形 \_ 平滑旗標

GL \_ 多邊形 \_ STIPPLE 旗標

GL \_ 剪式 \_ 測試旗標

GL \_ 樣板 \_ 測試旗標

GL \_ 材質 \_ 1d 旗標

GL \_ 材質 \_ 2d 旗標

旗標 GL \_ 材質 \_ GEN x， \_ 其中 x 是 S、T、R 或 Q

</dd> <dt>

<span id="GL_EVAL_BIT"></span><span id="gl_eval_bit"></span>GL \_ EVAL \_ BIT
</dt> <dd>

GL \_ MAP1 \_ x 啟用 bits，其中 x 是地圖類型

GL \_ list.map2 \_ x 啟用 bits，其中 x 是地圖類型

立體格線端點和部門

2d 格線端點和部門

GL \_ AUTO \_ 正常啟用位

</dd> <dt>

<span id="GL_FOG_BIT"></span><span id="gl_fog_bit"></span>GL \_ 霧化 \_ 位
</dt> <dd>

GL \_ 霧化啟用旗標

霧化色彩

霧化密度

線性霧化開始

線性霧化結束

霧化索引

GL \_ 霧化 \_ 模式值

</dd> <dt>

<span id="GL_HINT_BIT"></span><span id="gl_hint_bit"></span>GL \_ 提示 \_ 位
</dt> <dd>

GL \_ 透視圖 \_ 校正 \_ 提示設定

GL \_ 點 \_ 平滑 \_ 提示設定

GL \_ LINE \_ 平滑 \_ 提示設定

GL \_ 多邊形 \_ 平滑 \_ 提示設定

GL \_ 霧化 \_ 提示設定

</dd> <dt>

<span id="GL_LIGHTING_BIT"></span><span id="gl_lighting_bit"></span>GL \_ 照明 \_ 位
</dt> <dd>

GL \_ 色彩 \_ 材質啟用位

GL \_ 色 \_ 材質 \_ 臉部值

追蹤目前色彩的色彩材質參數

環境場景色彩

GL \_ LIGHT \_ 模型 \_ 本機 \_ 檢視器值

GL \_ LIGHT \_ 模型 \_ 雙 \_ 側設定

GL \_ 照明啟用位

為每個光線啟用位

每個光線的環境、擴散和反射濃度

每個光線的方向、位置、指數和截止角度

每個光線的常數、線性和二次衰減因素

每個材質的環境、擴散、反射和放射色彩

每個材質的環境、擴散和反射色彩索引

每個材質 GL \_ 陰影 \_ 模型設定的反射指數

</dd> <dt>

<span id="GL_LINE_BIT_"></span><span id="gl_line_bit_"></span>GL \_ 行 \_ 位 
</dt> <dd>

GL \_ 行 \_ 平滑旗標

GL \_ LINE \_ STIPPLE enable bit

Line stipple pattern 和 repeat 計數器

線條寬度

</dd> <dt>

<span id="GL_LIST_BIT"></span><span id="gl_list_bit"></span>GL \_ 清單 \_ 位
</dt> <dd>

GL \_ 清單 \_ 基礎設定

</dd> <dt>

<span id="GL_PIXEL_MODE_BIT"></span><span id="gl_pixel_mode_bit"></span>GL \_ 圖元 \_ 模式 \_ 位
</dt> <dd>

GL \_ red \_ 偏差和 gl \_ red \_ SCALE 設定

GL \_ 綠 \_ 偏差和 gl \_ 綠色 \_ 刻度值

GL \_ 藍色 \_ 偏差和 gl \_ 藍色 \_ 調整

GL \_ Alpha \_ 偏差和 gl \_ Alpha \_ 刻度

GL \_ 深度 \_ 偏差和 gl \_ 深度 \_ 調整

GL \_ 索引 \_ 位移和 gl \_ 索引 \_ 移位值

GL \_ 地圖 \_ 色彩和 gl \_ 地圖樣板 \_ 旗標

GL \_ zoom \_ X 和 gl \_ zoom 縮放 \_ Y 因素

GL \_ 讀取 \_ 緩衝區設定

</dd> <dt>

<span id="GL_POINT_BIT"></span><span id="gl_point_bit"></span>GL \_ 點 \_ 位
</dt> <dd>

GL \_ 點 \_ 平滑旗標

點大小

</dd> <dt>

<span id="GL_POLYGON_BIT"></span><span id="gl_polygon_bit"></span>GL \_ 多邊形 \_ 位
</dt> <dd>

GL \_ 精選 \_ 臉部啟用位

GL \_ 挑選 \_ 臉部 \_ 模式值

GL \_ 正面 \_ 臉部指標

GL \_ 多邊形 \_ 模式設定

GL \_ 多邊形 \_ 平滑旗標

GL \_ 多邊形 \_ STIPPLE 啟用位

GL \_ 多邊形 \_ 位移 \_ 填滿旗標

GL \_ 多邊形 \_ 位移 \_ 線旗標

GL \_ 多邊形 \_ 位移 \_ 點旗標

GL \_ 多邊形 \_ 位移 \_ 因數

GL \_ 多邊形 \_ 位移 \_ 單位

</dd> <dt>

<span id="GL_POLYGON_STIPPLE_BIT"></span><span id="gl_polygon_stipple_bit"></span>GL \_ 多邊形 \_ STIPPLE \_ 位
</dt> <dd>

多邊形 stipple 影像

</dd> <dt>

<span id="GL_SCISSOR_BIT"></span><span id="gl_scissor_bit"></span>GL \_ 剪式 \_ 位
</dt> <dd>

GL \_ 剪式 \_ 測試旗標

剪式方塊

</dd> <dt>

<span id="GL_STENCIL_BUFFER_BIT"></span><span id="gl_stencil_buffer_bit"></span>GL \_ 樣板 \_ 緩衝區 \_ 位
</dt> <dd>

GL \_ 樣板 \_ 測試啟用位

樣板函數和參考值

樣板值遮罩

樣板失敗、傳遞和深度緩衝區傳遞動作

樣板緩衝區清除值

樣板緩衝區 writemask

</dd> <dt>

<span id="GL_TEXTURE_BIT"></span><span id="gl_texture_bit"></span>GL \_ 材質 \_ 位
</dt> <dd>

啟用四個材質座標的位

每個材質影像的框線色彩

每個材質影像的縮制函式

每個材質影像的縮放功能

每個材質影像的材質座標和換行模式

每個材質環境的色彩和模式

啟用 bits GL \_ 紋理 \_ GEN \_ *x*;*x* 是 S、T、R 和 Q

\_ \_ \_ S、T、R 和 Q 的 GL 材質 GEN 模式設定

S、T、R 和 Q 的 glTexGen 平面方程式

</dd> <dt>

<span id="GL_TRANSFORM_BIT"></span><span id="gl_transform_bit"></span>GL \_ 轉換 \_ 位
</dt> <dd>

六個裁剪平面的係數

啟用使用者可定義裁剪平面的位

GL \_ 矩陣 \_ 模式值

GL \_ 標準化旗標

</dd> <dt>

<span id="GL_VIEWPORT_BIT"></span><span id="gl_viewport_bit"></span>GL \_ 區 \_ 位
</dt> <dd>

深度範圍 (近和遠) 

視口原點和範圍

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="error-codes"></a>錯誤碼

[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。



| Name                                                                                                  | 意義                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ 堆疊 \_ 溢位**</dt> </dl>    | 當屬性堆疊已滿時，就會呼叫函數。<br/>                                                                |
| <dl> <dt>**GL \_ 不正確 \_ 操作**</dt> </dl> | 呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。<br/> |



## <a name="remarks"></a>備註

**GlPushAttrib** 函式會採用一個引數，此遮罩會指出要在屬性堆疊上儲存的狀態變數群組。 符號常數用來設定遮罩中的位。 Mask 參數通常是藉由將邏輯 **OR** 運算套用至這些常數中的數個來構成。 您可以使用特殊遮罩 GL \_ 所有的 \_ ATTRIB \_ 位來儲存所有可堆疊的狀態。

[**GlPopAttrib**](glpopattrib.md)函式會還原使用 last **glPushAttrib** 命令所儲存之狀態變數的值。 未儲存的會保持不變。

將屬性推送至完整堆疊，或從空白堆疊取出屬性是錯誤的。 在任一種情況下，都會設定錯誤旗標，且不會對 OpenGL 狀態進行其他變更。

一開始，屬性堆疊是空的。

並非所有 OpenGL 狀態的值都可以儲存在屬性堆疊上。 例如，您無法儲存圖元 pack 和解除封裝狀態、轉譯模式狀態，以及選取和意見反應狀態。

屬性堆疊的深度取決於執行，但必須至少為16。

下列函式會取出 **glPushAttrib** 和 [**glPopAttrib**](glpopattrib.md)的相關資訊：

[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ ATTRIB \_ STACK \_ 深度的 glGet

[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 最大 \_ ATTRIB 參數 \_ 堆疊 \_ 深度的 glGet

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

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glGetClipPlane**](glgetclipplane.md)
</dt> <dt>

[**glGetError**](glgeterror.md)
</dt> <dt>

[**glGetLight**](glgetlight.md)
</dt> <dt>

[**glGetMap**](glgetmap.md)
</dt> <dt>

[**glGetMaterial**](glgetmaterial.md)
</dt> <dt>

[**glGetPixelMap**](glgetpixelmap.md)
</dt> <dt>

[**glGetPolygonStipple**](glgetpolygonstipple.md)
</dt> <dt>

[**glGetString**](glgetstring.md)
</dt> <dt>

[**glGetTexEnv**](glgettexenv.md)
</dt> <dt>

[**glGetTexGen**](glgettexgen.md)
</dt> <dt>

[**glGetTexImage**](glgetteximage.md)
</dt> <dt>

[**glGetTexLevelParameter**](glgettexlevelparameter.md)
</dt> <dt>

[**glGetTexParameter**](glgettexparameter.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> </dl>

 

 





