---
title: 'glColorSubTableEXT 函式 (Gl) '
description: GlColorSubTableEXT 函式會指定要取代之目標材質調色板的一部分。
ms.assetid: 21430245-f837-4c7a-944f-b44482254b12
keywords:
- glColorSubTableEXT 函式 OpenGL
topic_type:
- apiref
api_name:
- glColorSubTableEXT
api_location:
- Gl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff6f4b88a355c25df40a847912d4e3352bd87962
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475394"
---
# <a name="glcolorsubtableext-function"></a>glColorSubTableEXT 函式

**GlColorSubTableEXT** 函式會指定要取代之目標材質調色板的一部分。

## <a name="syntax"></a>語法


```C++
void WINAPI glColorSubTableEXT(
         GLenum  target,
         GLsizei start,
         GLsizei count,
         GLenum  format,
         GLenum  type,
   const GLvoid  *data
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*目標* 
</dt> <dd>

要變更其調色板的目標調色板材質。 必須是材質 \_ 1d 或紋理 \_ 2d。

</dd> <dt>

*開始* 
</dt> <dd>

要變更之調色板的起始調色板索引項目。

</dd> <dt>

*計數* 
</dt> <dd>

*開始* 時要變更之調色板的調色板索引項目索引項目數目。 *Count* 參數會決定變更的調色板索引項目範圍。

</dd> <dt>

*format* 
</dt> <dd>

圖元資料的格式。 接受下列符號常數。




| 值 | 意義 | 
|-------|---------|
| <span id="GL_RGBA"></span><span id="gl_rgba"></span><dl><dt><strong>GL_RGBA</strong></dt></dl> | 每個圖元都是四個元件的群組，順序如下：紅色、綠色、藍色、Alpha。 RGBA 格式的決定方式如下： <br /><ol><li><strong>GlColorSubTableEXT</strong>函式會將浮點值直接轉換成具有未指定精確度的內部格式。 帶正負號的整數值會以線性方式對應至內部格式，如此一來，最正面的可表示整數值會對應至1.0，而最大的可表示值會對應至-1.0。 不帶正負號的整數資料的對應方式如下：最大整數值對應至1.0，而零對應至0.0。</li><li><strong>GlColorSubTableEXT</strong>函式會 GL_c_SCALE 將產生的色彩值相乘，並將其新增至 GL_c_BIAS，其中<em>c</em>是紅色、綠色、藍色和 ALPHA，適用于個別的色彩元件。 結果會壓制到 [0，1] 範圍內。</li><li>如果 GL_MAP_COLOR 為 <strong>TRUE</strong>， <strong>glColorSubTableEXT</strong> 會依 GL_PIXEL_MAP_c_TO_c 查閱資料表的大小來調整每個色彩元件，然後以資料表在該資料表中參考的值取代該元件; <em>c</em> 分別為 R、G、B 或 A。</li><li><strong>GlColorSubTableEXT</strong>函式會將目前的點陣位置<em>z</em>座標和材質座標附加至每個圖元，然後將<em>x</em>和<em>y</em>視窗座標指派給第<em>n</em>個片段（例如<em>x</em>），以將產生的 RGBA 色彩轉換成片段： = <em>x</em><sub>r</sub>  +  <em>n</em> mod<em>寬度</em><br /><em>y</em>？ = <em>y</em><sub>r</sub>  + <em>n/寬度</em><br /> 其中 (<em>x</em><sub>r</sub> ， <em>y</em><sub>r</sub> ) 是目前的點陣位置。<br /></li><li>然後，這些圖元片段的處理方式就像是將點、線條或多邊形所產生的片段一樣。 <strong>GlColorSubTableEXT</strong>函式會先套用材質對應、霧化和所有片段作業，然後再將片段寫入畫面格緩衝區。</li></ol> | 
| <span id="GL_RED"></span><span id="gl_red"></span><dl><dt><strong>GL_RED</strong></dt></dl> | 每個圖元都是單一的紅色元件。<br /> <strong>GlColorSubTableEXT</strong>函式會以 RGBA 圖元的紅色元件相同的方式，將這個元件轉換成內部格式，然後將其轉換為具有綠色和藍色的 rgba 圖元（設為0.0），並將 Alpha 設定為1.0。 進行這項轉換之後，圖元的處理方式就像是將它當成 RGBA 圖元讀取一樣。<br /> | 
| <span id="GL_GREEN"></span><span id="gl_green"></span><dl><dt><strong>GL_GREEN</strong></dt></dl> | 每個圖元都是一個綠色的元件。<br /> <strong>GlColorSubTableEXT</strong>函式會以 RGBA 圖元的綠色元件相同的方式，將這個元件轉換成內部格式，然後將其轉換為具有紅色和藍色的 rgba 圖元（設為0.0），並將 Alpha 設定為1.0。 進行這項轉換之後，圖元的處理方式就像是將它當成 RGBA 圖元讀取一樣。<br /> | 
| <span id="GL_BLUE"></span><span id="gl_blue"></span><dl><dt><strong>GL_BLUE</strong></dt></dl> | 每個圖元都是單一藍色元件。<br /> <strong>GlColorSubTableEXT</strong>函式會以 RGBA 圖元 blue 元件的相同方式，將這個元件轉換成內部格式，然後將其轉換為具有紅色和綠色設定為0.0 的 RGBA 圖元，然後將 Alpha 設定為1.0。 進行這項轉換之後，圖元的處理方式就像是將它當成 RGBA 圖元讀取一樣。<br /> | 
| <span id="GL_ALPHA"></span><span id="gl_alpha"></span><dl><dt><strong>GL_ALPHA</strong></dt></dl> | 每個圖元都是單一 Alpha 元件。<br /> <strong>GlColorSubTableEXT</strong>函式會以 RGBA 圖元 Alpha 元件的相同方式，將這個元件轉換成內部格式，然後將它轉換為紅色、綠色和藍色設定為0.0 的 RGBA 圖元。 進行這項轉換之後，圖元的處理方式就像是將它當成 RGBA 圖元讀取一樣。<br /> | 
| <span id="GL_RGB"></span><span id="gl_rgb"></span><dl><dt><strong>GL_RGB</strong></dt></dl> | 每個圖元都是三個元件的群組，順序如下：紅色、綠色、藍色。<br /> <strong>GlColorSubTableEXT</strong>函式會以 RGBA 圖元的 red、綠和 blue 元件的相同方式，將每個元件轉換成內部格式。 色彩三重轉換成將 Alpha 設定為1.0 的 RGBA 圖元。 進行這項轉換之後，圖元的處理方式就像是將它當成 RGBA 圖元讀取一樣。<br /> | 
| <span id="GL_BGR_EXT"></span><span id="gl_bgr_ext"></span><dl><dt><strong>GL_BGR_EXT</strong></dt></dl> | 每個圖元都是三個元件的群組，順序如下：藍色、綠色、紅色。<br /> GL_BGR_EXT 提供的格式符合 Windows 裝置獨立點陣圖 (dib) 的記憶體配置。 因此，您的應用程式可以使用 Windows 函式呼叫和 OpenGL 圖元函式呼叫的相同資料。<br /> | 
| <span id="GL_BGRA_EXT"></span><span id="gl_bgra_ext"></span><dl><dt><strong>GL_BGRA_EXT</strong></dt></dl> | 每個圖元都是四個元件的群組，順序如下： blue、綠、red、Alpha。<br /> GL_BGRA_EXT 提供的格式符合 Windows 裝置獨立點陣圖 (dib) 的記憶體配置。 因此，您的應用程式可以使用 Windows 函式呼叫和 OpenGL 圖元函式呼叫的相同資料。<br /> | 




 

</dd> <dt>

*type* 
</dt> <dd>

*資料* 的資料類型。 接受下列符號常數： GL 不 \_ 帶正負號的 \_ 位元組、gl \_ 位元組、GL 不 \_ 帶正負號 \_ 的 SHORT、gl \_ short、gl 不 \_ 帶正負號 \_ int、gl \_ int 和 gl \_ FLOAT。

下表摘要說明 *型* 別參數之有效常數的意義。



| 值                                                                                                                                                                      | 意義                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span id="GL_UNSIGNED_BYTE"></span><span id="gl_unsigned_byte"></span><dl> <dt>**GL 不 \_ 帶正負號的 \_ 位元組**</dt> </dl>    | 不帶正負號的 8 位元整數<br/>                |
| <span id="GL_BYTE"></span><span id="gl_byte"></span><dl> <dt>**GL \_ 位元組**</dt> </dl>                                | 帶正負號的 8 位元整數<br/>                  |
| <span id="GL_UNSIGNED_SHORT"></span><span id="gl_unsigned_short"></span><dl> <dt>**GL 不 \_ 帶正負號 \_ 簡短**</dt> </dl> | 不帶正負號的 16 位元整數<br/>               |
| <span id="GL_SHORT"></span><span id="gl_short"></span><dl> <dt>**GL \_ 短期**</dt> </dl>                             | 帶正負號的 16 位元整數<br/>                 |
| <span id="GL_UNSIGNED_INT"></span><span id="gl_unsigned_int"></span><dl> <dt>**GL 不 \_ 帶正負號 \_ INT**</dt> </dl>       | 不帶正負號的 32 位元整數<br/>               |
| <span id="GL_INT"></span><span id="gl_int"></span><dl> <dt>**GL \_ INT**</dt> </dl>                                   | 32 位元整數<br/>                        |
| <span id="GL_FLOAT"></span><span id="gl_float"></span><dl> <dt>**GL \_ FLOAT**</dt> </dl>                             | 單精確度浮點值<br/> |



 

</dd> <dt>

*data* 
</dt> <dd>

指向調色板材質資料的指標。 資料會被視為一個調色板專案的立體材質調色板專案的單一圖元。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="error-codes"></a>錯誤碼

[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。



| Name                                                                                              | 意義                                                                                                                               |
|---------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ 無效 \_ 值**</dt> </dl> | *開始* 或 *計數* 是不正確整數。<br/>                                                                                 |
| <dl> <dt>**GL \_ 無效 \_ 列舉**</dt> </dl>  | *目標*、 *格式* 或 *類型* 不是可接受的值。<br/>                                                                    |
| <dl> <dt>**GL \_ 無效 \_ 值**</dt> </dl> | 呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。<br/> |



## <a name="remarks"></a>備註

**GlColorSubTableEXT** 函式會指定要取代之目前目標材質調色板的部分。 不同于 [**glColorTableEXT**](glcolortableext.md)，您無法將 *目標* 參數指定為 proxy 材質選擇區。

> [!Note]  
> **GlColorSubTableEXT** 函式是延伸模組函式，不是標準 OpenGL 程式庫的一部分，而是 GL \_ EXT \_ \_ 材質擴充功能的一部分。 若要檢查您的 OpenGL 執行是否支援 **glColorSubTableEXT**，請) 呼叫 [**glGetString**](glgetstring.md) (GL \_ 延伸模組。 如果它傳回 GL \_ EXT \_ \_ （調色板）材質，則會支援 **glColorSubTableEXT** 。 若要取得擴充函數的函式位址，請呼叫 [**wglGetProcAddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress)。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                      |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                            |
| 標頭<br/>                   | <dl> <dt>Gl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glColorTableEXT**](glcolortableext.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGetColorTableEXT**](glgetcolortableext.md)
</dt> <dt>

[**glGetColorTableParameterfvEXT**](glgetcolortableparameterfvext.md)
</dt> <dt>

[**glGetColorTableParameterivEXT**](glgetcolortableparameterivext.md)
</dt> <dt>

[**glGetString**](glgetstring.md)
</dt> <dt>

[**wglGetProcAddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress)
</dt> </dl>

 

 





