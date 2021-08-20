---
title: 'gluBuild1DMipmaps 函式 (X.glu 隊) '
description: GluBuild1DMipmaps 函式會建立1個 mipmap。
ms.assetid: 52ed924f-7a72-4458-b1b8-8e5d3021f60a
keywords:
- gluBuild1DMipmaps 函式 OpenGL
topic_type:
- apiref
api_name:
- gluBuild1DMipmaps
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c2b76a37fa7088835ad0238065b0647ff0beb973c1c3ffa1b892f6e0958d97a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119489688"
---
# <a name="glubuild1dmipmaps-function"></a>gluBuild1DMipmaps 函式

**GluBuild1DMipmaps** 函式會建立1個 mipmap。

## <a name="syntax"></a>語法


```C++
void WINAPI gluBuild1DMipmaps(
         GLenum target,
         GLint  components,
         GLint  width,
         GLenum format,
         GLenum type,
   const void   *data
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*目標* 
</dt> <dd>

目標材質。 必須是 GL \_ 紋理 \_ 1d。

</dd> <dt>

*元件* 
</dt> <dd>

材質中的色彩元件數目。 必須是1、2、3或4。

</dd> <dt>

*width* (寬度) 
</dt> <dd>

材質影像的寬度。

</dd> <dt>

*format* 
</dt> <dd>

圖元資料的格式。 下列值有效： GL \_ 色彩 \_ 索引、gl \_ RED、GL \_ 綠、gl \_ BLUE、gl \_ ALPHA、GL \_ RGB、GL \_ RGBA、GL \_ BGR \_ EXT、gl \_ BGRA \_ EXT、gl \_ 亮度或 gl \_ 亮度 \_ ALPHA。

</dd> <dt>

*type* 
</dt> <dd>

*資料* 的資料類型。 下列值有效： GL 不 \_ 帶正負號 \_ 的位元組、gl \_ 位元組、GL \_ 點陣圖、gl \_ 未簽署 \_ 短、gl \_ 簡短、GL 不 \_ 帶正負號 \_ int、gl \_ int 或 GL \_ FLOAT。

</dd> <dt>

*data* 
</dt> <dd>

記憶體中影像資料的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="remarks"></a>備註

**GluBuild1DMipmaps** 函式會取得輸入影像，並使用 [**gluScaleImage**](gluscaleimage.md)) 產生 (的所有 mipmap 影像，以便輸入影像可作為 mipmapped 材質影像使用。 接著會呼叫 [**glTexImage1D**](glteximage1d.md) 函式來載入每個影像。 如果輸入影像的寬度不是2的乘冪，則會在產生 mipmap 之前，將影像調整為最接近的兩次乘冪。

傳回值為零表示成功。 否則，會傳回 X.GLU 隊錯誤碼 (請參閱 [**gluErrorString**](gluerrorstring.md)) 。

如需 *格式* 參數可接受值的描述，請參閱 **glTexImage1D**。 如需 *類型* 參數可接受值的描述，請參閱 [**glDrawPixels**](gldrawpixels.md)。

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

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**gluBuild2DMipmaps**](glubuild2dmipmaps.md)
</dt> <dt>

[**gluScaleImage**](gluscaleimage.md)
</dt> </dl>

 

 





