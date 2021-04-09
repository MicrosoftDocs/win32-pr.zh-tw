---
title: 'glPixelMapuiv 函式 (Gl) '
description: GlPixelMapuiv 函式會設定圖元傳輸對應。
ms.assetid: dd0f7881-fdd1-49c2-b68c-21e2f9e5ecd2
keywords:
- glPixelMapuiv 函式 OpenGL
topic_type:
- apiref
api_name:
- glPixelMapuiv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e9b31398060e62fa14cd35afe4f8536dd78f963
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934506"
---
# <a name="glpixelmapuiv-function"></a>glPixelMapuiv 函式

**GlPixelMapuiv** 函式會設定圖元傳輸對應。

## <a name="syntax"></a>語法


```C++
void WINAPI glPixelMapuiv(
         GLenum  map,
         GLsizei mapsize,
   const GLuint  *values
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*map* 
</dt> <dd>

符號對應名稱。 十個地圖如下所示。



| 值                                                                                                                                                                               | 意義                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <span id="GL_PIXEL_MAP_I_TO_I"></span><span id="gl_pixel_map_i_to_i"></span><dl> <dt>**GL \_ 圖元 \_ 對應 \_ I \_ \_**</dt> </dl> | 將色彩索引對應至色彩索引。<br/>       |
| <span id="GL_PIXEL_MAP_S_TO_S"></span><span id="gl_pixel_map_s_to_s"></span><dl> <dt>**GL \_ 圖元 \_ 地圖 \_ S \_ 到 \_ S**</dt> </dl> | 將樣板索引對應至樣板索引。<br/>   |
| <span id="GL_PIXEL_MAP_I_TO_R"></span><span id="gl_pixel_map_i_to_r"></span><dl> <dt>**GL \_ 圖元 \_ 對應 \_ I \_ 到 \_ R**</dt> </dl> | 將色彩索引對應至紅色元件。<br/>      |
| <span id="GL_PIXEL_MAP_I_TO_G"></span><span id="gl_pixel_map_i_to_g"></span><dl> <dt>**GL \_ 圖元 \_ 地圖 \_ I \_ 到 \_ G**</dt> </dl> | 將色彩索引對應至綠色元件。<br/>    |
| <span id="GL_PIXEL_MAP_I_TO_B"></span><span id="gl_pixel_map_i_to_b"></span><dl> <dt>**GL \_ 圖元 \_ 地圖 \_ I \_ 到 \_ B**</dt> </dl> | 將色彩索引對應至藍色元件。<br/>     |
| <span id="GL_PIXEL_MAP_I_TO_A"></span><span id="gl_pixel_map_i_to_a"></span><dl> <dt>**GL \_ 圖元 \_ 對應 \_ I \_ 到 \_**</dt> </dl> | 將色彩索引對應至 Alpha 元件。<br/>    |
| <span id="GL_PIXEL_MAP_R_TO_R"></span><span id="gl_pixel_map_r_to_r"></span><dl> <dt>**GL \_ 圖元 \_ 地圖 \_ R \_ 至 \_ R**</dt> </dl> | 將紅色元件對應至紅色元件。<br/>     |
| <span id="GL_PIXEL_MAP_G_TO_G"></span><span id="gl_pixel_map_g_to_g"></span><dl> <dt>**GL \_ 圖元 \_ 地圖 \_ G \_ 至 \_ G**</dt> </dl> | 將綠色元件對應至綠色元件。<br/> |
| <span id="GL_PIXEL_MAP_B_TO_B"></span><span id="gl_pixel_map_b_to_b"></span><dl> <dt>**GL \_ 圖元 \_ 地圖 \_ B \_ 到 \_ B**</dt> </dl> | 將藍色元件對應至藍色元件。<br/>   |
| <span id="GL_PIXEL_MAP_A_TO_A"></span><span id="gl_pixel_map_a_to_a"></span><dl> <dt>**GL \_ 圖元 \_ 將 \_ A 對應 \_ 至 \_**</dt> </dl> | 將 Alpha 元件對應至 Alpha 元件。<br/> |



 

</dd> <dt>

*mapsize* 
</dt> <dd>

要定義之對應的大小。

</dd> <dt>

*值* 
</dt> <dd>

*Mapsize* 值的陣列。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="error-codes"></a>錯誤碼

[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。



| Name                                                                                                  | 意義                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ 無效 \_ 列舉**</dt> </dl>      | *地圖* 不是可接受的值。<br/>                                                                                                                                                                                |
| <dl> <dt>**GL \_ 無效 \_ 值**</dt> </dl>     | *mapsize* 是負數或大於 GL \_ 圖元 \_ 地圖 \_ 資料表。 <br/>                                                                                                                                                   |
| <dl> <dt>**GL \_ 無效 \_ 值**</dt> </dl>     | *map* was GL \_ 圖元 \_ 地圖 \_ i \_ 到 \_ i、GL \_ 圖元 \_ map \_ s \_ 到 \_ s、gl \_ 圖元 \_ map \_ i \_ 到 \_ R、gl \_ 圖元 \_ map \_ i \_ 到 \_ G、gl 圖元 map i 到 B、gl 圖元 map i 至 \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ a、 *mapsize* 不是2的乘冪。 <br/> |
| <dl> <dt>**GL \_ 不正確 \_ 操作**</dt> </dl> | 呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。 <br/>                                                                                     |



## <a name="remarks"></a>備註

**GlPixelMap** 函數會設定 [**glCopyPixels**](glcopypixels.md)、 [**glCopyTexImage1D**](glcopyteximage1d.md)、 [**glCopyTexImage2D**](glcopyteximage2d.md)、 [**glCopyTexSubImage1D**](glcopytexsubimage1d.md)、 [**glCopyTexSubImage2D、glDrawPixels**](glcopytexsubimage2d.md) [**、**](gldrawpixels.md) [**glReadPixels**](glreadpixels.md) [**、glTexImage1D、**](glteximage1d.md) [**glTexImage2D**](glteximage2d.md)、glTexSubImage1D 和 [**glTexSubImage2D**](gltexsubimage2d.md)所使用的轉譯資料表或 [](gltexsubimage1d.md)*對應*。 這些對應的使用會在 [**glPixelTransfer**](glpixeltransfer.md) 主題中完整描述，部分位於圖元和材質影像命令的主題中。 本主題只會說明對應的規格。

*Map* 參數是符號對應名稱，表示要設定的十個地圖中的其中一個。 *Mapsize* 參數會指定地圖中的專案數，而 *值* 則是 *mapsize* 對應值陣列的指標。

地圖中的專案可以指定為單精確度浮點數、不帶正負號的短整數或不帶正負號的長整數。 將色彩元件值儲存 (所有的對應，但 GL \_ 圖元 \_ 地圖 \_ i \_ 到 \_ i 和 gl 圖元的對應 \_ \_ \_ s \_ \_) 以浮點數格式保留其值，並具有未指定的尾數和指數大小。 [**GlPixelMapfv**](glpixelmap.md)所指定的浮點值會直接轉換成這些對應的內部浮點格式，然後壓制至範圍 \[ 0，1 \] 。 **GlPixelMapusv** 和 **glPixelMapuiv** 指定的不帶正負號的整數值會以線性方式轉換，使可代表的最大整數對應到1.0，而零對應到0.0。

儲存索引、GL \_ 圖元 \_ 地圖 \_ i \_ 到 \_ i 和 GL 圖元圖元地圖的地圖會以 \_ \_ \_ \_ \_ 固定點格式保留其值，並在二進位點右邊指定不指定的位數。 [**GlPixelMapfv**](glpixelmap.md)所指定的浮點值會直接轉換成這些對應的內部固定點格式。 **GlPixelMapusv** 和 **glPixelMapuiv** 指定的不帶正負號的整數值會指定整數值，並在二進位點的右邊加上零。

下表顯示每個對應的初始大小和值。 以色彩或樣板索引編制索引的地圖必須有 *mapsize* = 2 ^ *n* ，部分 *n* 或結果未定義。 每個對應的允許大小上限取決於執行，而且可以藉由呼叫 **glGet** 與引數 GL \_ 最大 \_ 圖元 \_ 地圖 \_ 表格來判斷。 單一最大值適用于所有對應，且至少為32。



| 對應                      | 查閱索引  | 查閱值  | 初始大小 | 初始值 |
|--------------------------|---------------|---------------|--------------|---------------|
| GL \_ 圖元 \_ 對應 \_ I \_ \_ | 色彩索引   | 色彩索引   | 1            | 0.0           |
| GL \_ 圖元 \_ 地圖 \_ S \_ 到 \_ S | 樣板索引 | 樣板索引 | 1            | 0.0           |
| GL \_ 圖元 \_ 對應 \_ I \_ 到 \_ R | 色彩索引   | R             | 1            | 0.0           |
| GL \_ 圖元 \_ 地圖 \_ I \_ 到 \_ G | 色彩索引   | G             | 1            | 0.0           |
| GL \_ 圖元 \_ 地圖 \_ I \_ 到 \_ B | 色彩索引   | B             | 1            | 0.0           |
| GL \_ 圖元 \_ 對應 \_ I \_ 到 \_ | 色彩索引   | A             | 1            | 0.0           |
| GL \_ 圖元 \_ 地圖 \_ R \_ 至 \_ R | R             | R             | 1            | 0.0           |
| GL \_ 圖元 \_ 地圖 \_ G \_ 至 \_ G | G             | G             | 1            | 0.0           |
| GL \_ 圖元 \_ 地圖 \_ B \_ 到 \_ B | B             | B             | 1            | 0.0           |
| GL \_ 圖元 \_ 將 \_ A 對應 \_ 至 \_ | A             | A             | 1            | 0.0           |



 

下列函式會取出與 **glPixelMap** 相關的資訊：

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) 與引數 GL \_ 圖元 \_ 對應 \_ 我 \_ 的 \_ \_ 大小

將引數 GL \_ 圖元 \_ 對應 \_ \_ 到 \_ s \_ 大小的 glGet

使用引數 GL \_ 圖元 \_ 地圖 \_ I \_ 到 \_ R \_ 大小的 glGet

使用引數 GL \_ 圖元 \_ 地圖 \_ I \_ 到 \_ G \_ 大小的 glGet

**glGet** 與引數 GL \_ 圖元 \_ 地圖 \_ I \_ 到 B 的 \_ \_ 大小

**glGet** 與引數 GL \_ 圖元 \_ 對應 \_ I \_ 至 \_ \_ 大小

使用引數 GL \_ 圖元 \_ 地圖 \_ r \_ 至 \_ r \_ 大小的 glGet

具有引數 GL \_ 圖元 \_ 地圖 \_ g \_ 至 \_ g \_ 大小的 glGet

具有引數 GL \_ 圖元 \_ 地圖 \_ b \_ 到 \_ b \_ 大小的 glGet

具有引數 GL \_ 圖元 \_ 的 glGet 對應 \_ \_ 至 \_ \_ 大小

具有引數 GL \_ 最大 \_ 圖元 \_ 地圖 \_ 資料表的 glGet

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

[**glDrawPixels**](gldrawpixels.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glPixelStore**](glpixelstore-functions.md)
</dt> <dt>

[**glPixelTransfer**](glpixeltransfer.md)
</dt> <dt>

[**glReadPixels**](glreadpixels.md)
</dt> <dt>

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> </dl>

 

 





