---
title: 'glGetColorTableParameterfvEXT 函式 (Gl) '
description: 'GlGetColorTableParameterfvEXT 和 glGetColorTableParameterivEXT 函數會從色彩資料表取得調色板參數。 |glGetColorTableParameterfvEXT 函式 (Gl) '
ms.assetid: e78051aa-4233-413c-8838-0741b54eab0e
keywords:
- glGetColorTableParameterfvEXT 函式 OpenGL
topic_type:
- apiref
api_name:
- glGetColorTableParameterfvEXT
api_location:
- Gl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e7cd93c45c602b35e88fe28c467943829669d329f75007607783ece06f1b51b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118615768"
---
# <a name="glgetcolortableparameterfvext-function"></a>glGetColorTableParameterfvEXT 函式

**GlGetColorTableParameterfvEXT** 和 [**glGetColorTableParameterivEXT**](glgetcolortableparameterivext.md)函數會從色彩資料表取得調色板參數。

## <a name="syntax"></a>語法


```C++
void WINAPI glGetColorTableParameterfvEXT(
   GLenum  target,
   GLenum  pname,
   GLfloat *params
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*目標* 
</dt> <dd>

您要取得參數資料之調色板的目標紋理。 必須是材質 \_ 1d、材質 \_ 2D、proxy \_ 材質 \_ 1d 或 proxy \_ 材質 \_ 2d。

</dd> <dt>

*pname* 
</dt> <dd>

*參數* 所指向之調色板參數資料類型的符號常數。

以下是接受的符號常數及其意義。



| 值                                                                                                                                                                                                             | 意義                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_COLOR_TABLE_FORMAT_EXT"></span><span id="gl_color_table_format_ext"></span><dl> <dt>**GL \_ 色彩 \_ 表 \_ 格式 \_ EXT**</dt> </dl>              | 傳回最新的 [**glColorTableEXT**](glcolortableext.md) 呼叫所指定的內部格式或預設值。<br/> |
| <span id="GL_COLOR_TABLE_WIDTH_EXT"></span><span id="gl_color_table_width_ext"></span><dl> <dt>**GL \_ 色彩 \_ 資料表 \_ 寬度 \_ EXT**</dt> </dl>                 | 傳回目前調色板的寬度。<br/>                                                                                         |
| <span id="GL_COLOR_TABLE_RED_SIZE_EXT"></span><span id="gl_color_table_red_size_ext"></span><dl> <dt>**GL \_ 色彩 \_ 表 \_ 紅色 \_ 大小 \_ EXT**</dt> </dl>       | 傳回在內部用來儲存調色板資料之紅色元件的實際大小。<br/>                                           |
| <span id="GL_COLOR_TABLE_GREEN_SIZE_EXT"></span><span id="gl_color_table_green_size_ext"></span><dl> <dt>**GL \_ 色彩 \_ 表 \_ 綠色 \_ 大小 \_ EXT**</dt> </dl> | 傳回在內部用來儲存調色板資料之綠色元件的實際大小。<br/>                                         |
| <span id="GL_COLOR_TABLE_BLUE_SIZE_EXT"></span><span id="gl_color_table_blue_size_ext"></span><dl> <dt>**GL \_ 色彩 \_ 表 \_ 藍色 \_ 大小 \_ EXT**</dt> </dl>    | 傳回在內部用來儲存調色板資料藍色元件的實際大小。<br/>                                          |
| <span id="GL_COLOR_TABLE_ALPHA_SIZE_EXT"></span><span id="gl_color_table_alpha_size_ext"></span><dl> <dt>**GL \_ 色彩 \_ 表 \_ ALPHA \_ 大小 \_ EXT**</dt> </dl> | 傳回在內部用來儲存調色板資料 Alpha 元件的實際大小。<br/>                                         |



 

</dd> <dt>

*params* 
</dt> <dd>

指向 *pname* 參數所指定的色彩資料表參數資料。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="remarks"></a>備註

您可以使用 **glGetColorTableParameterivEXT** 和 **glGetColorTableParameterfvEXT** 函式，從以 [**glColorTableEXT**](glcolortableext.md) 為目標材質調色板設定的色彩資料表中取出特定的參數資料。 此外，您也可以使用這些函數來判斷 **glGetColorTableEXT** 傳回的色彩資料表專案數目。

當 *目標* 參數為 GL \_ proxy \_ 材質 \_ 1d 或 GL \_ proxy \_ 材質 \_ 2d，且執行不支援針對 *格式* 或 *寬度* 指定的值時， **glColorTableEXT** 可能無法建立要求的色彩表。 在此情況下，color 資料表是空的，而且所有取出的參數都是零。 您可以藉由使用 proxy 目標呼叫 **glColorTableEXT** ，然後呼叫 **glGetColorTableParameterivEXT** 或 **glGetColorTableParameterfvEXT** 來判斷 width 參數是否符合 **GlColorTableEXT** 所設定的，來判斷 OpenGL 是否支援特定的色彩表格式和大小。 如果取出的寬度為零，則 **glColorTable** 的色彩表格要求會失敗。 如果取出的寬度不是零，您可以使用紋理1d 或材質2d 的真實目標來呼叫 **glColorTable** ， \_ \_ 以設定色彩表。

**GlGetColorTableParameterivEXT** 和 **glGetColorTableParameterfvEXT** 函式是延伸函式，這些函式不是標準 OpenGL 程式庫的一部分，而是 GL \_ EXT \_ 材質擴充功能的一部分 \_ 。 若要檢查 OpenGL 的執行是否支援 **glGetColorTableParameterivEXT** 和 **glGetColorTableParameterfvEXT**，請) **(** GL 延伸模組呼叫 [**glGetString**](glgetstring.md) \_ ****。 如果它傳回 GL \_ EXT \_ \_ （調色板）材質，則支援 **glGetColorTableParameterivEXT** 和 **glGetColorTableParameterfvEXT** 。 若要取得擴充函數的函式位址，請呼叫 [**wglGetProcAddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                      |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                            |
| 標頭<br/>                   | <dl> <dt>Gl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**glColorSubTableEXT**](glcolorsubtableext.md)
</dt> <dt>

[**glColorTableEXT**](glcolortableext.md)
</dt> <dt>

[**glGetColorTableEXT**](glgetcolortableext.md)
</dt> <dt>

[**glGetColorTableParameterivEXT**](glgetcolortableparameterivext.md)
</dt> <dt>

[**wglGetProcAddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress)
</dt> </dl>

 

 





