---
title: 'gluScaleImage 函式 (X.glu 隊) '
description: GluScaleImage 函式會將影像調整為任意大小。
ms.assetid: f47191e8-b22d-4f6a-949a-9c7782d6d338
keywords:
- gluScaleImage 函式 OpenGL
topic_type:
- apiref
api_name:
- gluScaleImage
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7da95f1545996a83adeb27deaceb7fab6290005e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104383837"
---
# <a name="gluscaleimage-function"></a>gluScaleImage 函式

**GluScaleImage** 函式會將影像調整為任意大小。

## <a name="syntax"></a>語法


```C++
int WINAPI gluScaleImage(
         GLenum format,
         GLint  widthin,
         GLint  heightin,
         GLenum typein,
   const void   *datain,
         GLint  widthout,
         GLint  heightout,
         GLenum typeout,
         void   *dataout
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*format* 
</dt> <dd>

圖元資料的格式。 下列符號值有效： GL \_ 色彩 \_ 索引、gl 樣板 \_ \_ 索引、GL \_ 深度 \_ 元件、GL \_ RED、gl \_ 綠、gl \_ BLUE、GL \_ ALPHA、GL \_ RGB、GL \_ RGBA、GL \_ BGR \_ EXT、gl \_ BGRA \_ EXT、gl \_ 亮度，以及 gl \_ 亮度 \_ ALPHA。

</dd> <dt>

*widthin* 
</dt> <dd>

調整的來源影像寬度。

</dd> <dt>

*heightin* 
</dt> <dd>

調整的來源影像高度。

</dd> <dt>

*typein* 
</dt> <dd>

*描述* 的資料類型。 必須是下列其中一項： GL 不 \_ 帶正負號的 \_ 位元組、gl \_ 位元組、GL \_ 點陣圖、gl 不 \_ 帶正負號 \_ 的 short、gl \_ short、GL 不 \_ 帶正負號 \_ int、gl \_ int 或 gl \_ FLOAT。

</dd> <dt>

*描述* 
</dt> <dd>

來源影像的指標。

</dd> <dt>

*widthout* 
</dt> <dd>

目的地影像的寬度。

</dd> <dt>

*heightout* 
</dt> <dd>

目的地影像的高度。

</dd> <dt>

*typeout* 
</dt> <dd>

*Dataout* 的資料類型。 必須是下列其中一項： GL 不 \_ 帶正負號的 \_ 位元組、gl \_ 位元組、GL \_ 點陣圖、gl 不 \_ 帶正負號 \_ 的 short、gl \_ short、GL 不 \_ 帶正負號 \_ int、gl \_ int 或 gl \_ FLOAT。

</dd> <dt>

*dataout* 
</dt> <dd>

目的地影像的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果此函式成功，則傳回值為零。

如果函式失敗，則傳回值為 X.GLU 隊錯誤碼 (查看 [**gluErrorString**](gluerrorstring.md)) 。

## <a name="remarks"></a>備註

**GluScaleImage** 函式會使用適當的圖元存放區模式來調整圖元影像，以將資料從來源影像解壓縮，並將資料封裝到目的地影像。

壓縮影像時， **gluScaleImage** 會使用 box 篩選器來取樣來源影像，並建立目的地影像的圖元。 放大影像時，來源影像的圖元會以線性方式插入，以建立目的映射。

如需 *format*、 *typein* 和 *typeout* 參數可接受值的描述，請參閱 [**glReadPixels**](glreadpixels.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                           |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                 |
| 標頭<br/>                   | <dl> <dt>X.glu 隊。h</dt> </dl>     |
| 程式庫<br/>                  | <dl> <dt>Glu32 .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Glu32.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**glDrawPixels**](gldrawpixels.md)
</dt> <dt>

[**glReadPixels**](glreadpixels.md)
</dt> <dt>

[**gluBuild1DMipmaps**](glubuild1dmipmaps.md)
</dt> <dt>

[**gluBuild2DMipmaps**](glubuild2dmipmaps.md)
</dt> <dt>

[**gluErrorString**](gluerrorstring.md)
</dt> </dl>

 

 





