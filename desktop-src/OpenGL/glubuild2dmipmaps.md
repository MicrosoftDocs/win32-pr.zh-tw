---
title: 'gluBuild2DMipmaps 函式 (X.glu 隊) '
description: GluBuild2DMipmaps 函式會建立 2D mipmap。
ms.assetid: ea19a9b0-baf7-436f-afd5-609bc364b3ba
keywords:
- gluBuild2DMipmaps 函式 OpenGL
topic_type:
- apiref
api_name:
- gluBuild2DMipmaps
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f27dcf3d0e95b0b52d5b7f4c4ce0e5692f3fc856b81d9c1d82c9661a70e2f818
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119489648"
---
# <a name="glubuild2dmipmaps-function"></a>gluBuild2DMipmaps 函式

**GluBuild2DMipmaps** 函式會建立 2d mipmap。

## <a name="syntax"></a>語法


```C++
void WINAPI gluBuild2DMipmaps(
         GLenum target,
         GLint  components,
         GLint  width,
         GLInt  height,
         GLenum format,
         GLenum type,
   const void   *data
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*目標* 
</dt> <dd>

目標材質。 必須是 GL \_ 紋理 \_ 2d。

</dd> <dt>

*元件* 
</dt> <dd>

材質中的色彩元件數目。 必須是1、2、3或4。

</dd> <dt>

*width* (寬度) 
</dt> <dd>

材質影像的寬度。

</dd> <dt>

*height* (高度) 
</dt> <dd>

材質影像的高度。

</dd> <dt>

*format* 
</dt> <dd>

圖元資料的格式。 必須是下列其中一項： GL \_ 色彩 \_ 索引、gl \_ RED、GL \_ 綠、gl \_ BLUE、gl \_ ALPHA、GL \_ RGB、GL \_ RGBA、GL \_ BGR \_ EXT、gl \_ BGRA \_ EXT、gl \_ 亮度或 GL \_ 亮度 \_ ALPHA。

</dd> <dt>

*type* 
</dt> <dd>

*資料* 的資料類型。 必須是下列其中一項： GL 不 \_ 帶正負號的 \_ 位元組、gl \_ 位元組、GL \_ 點陣圖、gl 不 \_ 帶正負號 \_ 的 short、gl \_ short、GL 不 \_ 帶正負號 \_ int、gl \_ int 或 gl \_ FLOAT。

</dd> <dt>

*data* 
</dt> <dd>

記憶體中影像資料的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="remarks"></a>備註

**GluBuild2DMipmaps** 函式會取得輸入影像，並使用 [**gluScaleImage**](gluscaleimage.md)) 來產生所有的 Mipmap (影像，以便輸入影像可作為 mipmapped 材質影像。 若要載入每個影像，請呼叫 [**glTexImage2D**](glteximage2d.md)。 如果輸入影像的尺寸不是二的乘冪，則會調整影像大小，使寬度和高度在 mipmap 產生之前都是兩個的乘冪。

傳回值為零表示成功。 否則，會傳回 X.GLU 隊錯誤碼 (請參閱 [**gluErrorString**](gluerrorstring.md)) 。

如需 *格式* 參數可接受值的描述，請參閱 **glTexImage2D**。 如需 *類型* 可接受值的描述，請參閱 [**glDrawPixels**](gldrawpixels.md)。

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

[**glTexImage2D**](glteximage2d.md)
</dt> <dt>

[**gluBuild1DMipmaps**](glubuild1dmipmaps.md)
</dt> <dt>

[**gluScaleImage**](gluscaleimage.md)
</dt> </dl>

 

 





