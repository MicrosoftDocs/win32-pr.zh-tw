---
title: 'glRasterPos4s 函式 (Gl) '
description: '指定圖元作業的點陣位置。 |glRasterPos4s 函式 (Gl) '
ms.assetid: 60e6ced4-a542-4189-a3da-eed36f81cafb
keywords:
- glRasterPos4s 函式 OpenGL
topic_type:
- apiref
api_name:
- glRasterPos4s
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d3d46eba3121f28fcab3eb256c038e4dd2b18d27c7537a92bd76b33f641f761
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118614594"
---
# <a name="glrasterpos4s-function"></a>glRasterPos4s 函式

指定圖元作業的點陣位置。

## <a name="syntax"></a>語法


```C++
void WINAPI glRasterPos4s(
   GLshort x,
   GLshort y,
   GLshort z,
   GLshort w
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*x* 
</dt> <dd>

指定目前點陣位置的 x 座標。

</dd> <dt>

*y* 
</dt> <dd>

指定目前點陣位置的 y 座標。

</dd> <dt>

*z* 
</dt> <dd>

指定目前點陣位置的 z 座標。

</dd> <dt>

*w* 
</dt> <dd>

目前點陣位置的 w 座標。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="remarks"></a>備註

OpenGL 會在視窗座標中維持立體的位置。 這個位置（稱為點陣定位）會以子圖元精確度來維持。 它是用來放置圖元和點陣圖寫入作業。 請參閱 [**glBitmap**](glbitmap.md)、 [**glDrawPixels**](gldrawpixels.md)和 [**glCopyPixels**](glcopypixels.md)。

目前的點陣位置包含三個視窗座標 (*x、y、z*) 、剪輯座標（ *w* 值）、眼睛座標距離、有效位，以及相關聯的色彩資料和材質座標。 *W* 座標是剪輯座標，因為 *w* 不會投影至視窗座標。 [GlRasterPos4](glrasterpos-functions.md)函式會明確指定物件座標 *x、y、z* 和 *w* 。 GlRasterPos3 函式會明確指定物件座標 *x、y* 和 *z* ，而 *w* 會隱含地設定為一。 GlRasterPos2 函式會使用 *x* 和 *y* 的引數值，同時將 *z* 和 *w* 隱含設定為零和1。

[GlRasterPos](glrasterpos-functions.md)所呈現的物件座標就如同[glVertex](glvertex-functions.md)命令的座標一樣。 它們是由目前的模型和投射矩陣進行轉換，並且傳遞至剪切階段。 如果頂點未挑選，則會進行投影並調整為視窗座標（這會成為新的目前點陣位置），並設定 GL \_ 目前的 \_ 點陣 \_ 定位 \_ 有效旗標。 如果頂點是挑選，則會清除有效位，而且不會定義目前的點陣位置和相關聯的色彩和材質座標。

目前的點陣位置也包含一些相關聯的色彩資料和材質座標。 如果已啟用光源，則在 \_ \_ \_ RGBA 模式中使用 gl 目前的點陣色彩，或 \_ 在 [ \_ 色彩索引模式] 中將 [gl 目前的點陣 \_ 索引] 設定為 [光線計算] 所產生的色彩 (請參閱 [glLight](gllight-functions.md)、 [glLightModel](gllightmodel-functions.md)和 [**glShadeModel**](glshademodel.md)) 。 如果停用光源，目前的色彩 (在 RGBA 模式下，狀態變數 GL \_ 目前 \_ 色彩) 或色彩索引 (處於色彩索引模式時，狀態變數 gl \_ 目前 \_ 索引) 會用來更新目前的點陣色彩。

同樣地， \_ \_ \_ \_ 根據紋理矩陣和材質產生函式，會將 gl 目前的點陣材質 coords 更新為 gl \_ 目前材質 coords 的函式 \_ \_ (查看 [glTexGen](gltexgen-functions.md)) 。 最後，從眼睛座標系統的原點到頂點的距離（僅由模型矩陣轉換）會取代 GL \_ 目前的 \_ 點陣 \_ 距離。

一開始，目前的點陣位置是 (0、0、0、1) 、目前的點陣距離為0、已設定有效位、相關聯的 RGBA 色彩 (1、1、1、1) 、相關聯的色彩索引為1，且相關聯的材質座標為 (0、0、0、1) 。 在 RGBA 模式中， \_ GL \_ 目前 \_ 的點陣索引一律為 1; 在色彩索引模式中，目前的點陣 RGBA 色彩一律會維持其初始值。

> [!Note]  
> [GlRasterPos](glrasterpos-functions.md)和 by [**glBitmap**](glbitmap.md)都會修改點陣位置。

 

> [!Note]  
> 當點陣位置座標無效時，會忽略以點陣位置為基礎的繪製命令 (也就是不會導致 OpenGL 狀態) 的變更。

 

下列函式會取出與 [glRasterPos](glrasterpos-functions.md)相關的資訊：

<dl>

[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 目前 \_ 點陣 \_ 位置的 glGet  
[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 目前 \_ 點陣 \_ 位置 \_ 有效的 glGet  
[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 目前 \_ 點陣 \_ 距離的 glGet  
[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 目前 \_ 點陣 \_ 色彩的 glGet  
[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 目前 \_ 點陣 \_ 索引的 glGet  
[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 目前 \_ 點陣 \_ 材質紋理 \_ 的 glGet  
</dl>

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

[**glBitmap**](glbitmap.md)
</dt> <dt>

[**glCopyPixels**](glcopypixels.md)
</dt> <dt>

[**glDrawPixels**](gldrawpixels.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[glLight](gllight-functions.md)
</dt> <dt>

[glLightModel](gllightmodel-functions.md)
</dt> <dt>

[**glShadeModel**](glshademodel.md)
</dt> <dt>

[**glTexCoord**](gltexcoord-functions.md)
</dt> <dt>

[glTexGen](gltexgen-functions.md)
</dt> <dt>

[glVertex](glvertex-functions.md)
</dt> </dl>

 

 





