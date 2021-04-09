---
title: 'glBitmap 函式 (Gl) '
description: GlBitmap 函式會繪製點陣圖。
ms.assetid: 3cd8e41b-016b-4610-833a-048b5e50ae7c
keywords:
- glBitmap 函式 OpenGL
topic_type:
- apiref
api_name:
- glBitmap
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7aeb97bb16a1e3c4c29d1dfb1a5320c02f44404d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025202"
---
# <a name="glbitmap-function"></a>glBitmap 函式

**GlBitmap** 函式會繪製點陣圖。

## <a name="syntax"></a>語法


```C++
void WINAPI glBitmap(
         GLSizei width,
         GLSizei height,
         GLfloat xorig,
         GLfloat yorig,
         GLfloat xmove,
         GLfloat ymove,
   const GLubyte *bitmap
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*width* (寬度) 
</dt> <dd>

點陣圖影像的圖元寬度。

</dd> <dt>

*height* (高度) 
</dt> <dd>

點陣圖影像的圖元高度。

</dd> <dt>

*xorig* 
</dt> <dd>

點陣圖影像中原點的 *x* 位置。 來源是以點陣圖左下角來測量，而右邊和向上方向則是正軸。

</dd> <dt>

*yorig* 
</dt> <dd>

點陣圖影像中原點的 *y* 位置。 來源是以點陣圖左下角來測量，而右邊和向上方向則是正軸。

</dd> <dt>

*xmove* 
</dt> <dd>

繪製點陣圖之後要加入目前點陣位置的 *x* 位移。

</dd> <dt>

*ymove* 
</dt> <dd>

繪製點陣圖之後要加入目前點陣位置的 *y* 位移。

</dd> <dt>

*點陣圖* 
</dt> <dd>

點陣圖影像的位址。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="error-codes"></a>錯誤碼

[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。



| Name                                                                                                  | 意義                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ 無效 \_ 值**</dt> </dl>     | *寬度* 或 *高度* 為負數。<br/>                                                                                           |
| <dl> <dt>**GL \_ 不正確 \_ 操作**</dt> </dl> | 呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。<br/> |



## <a name="remarks"></a>備註

點陣圖是二進位影像。 繪製時，點陣圖的位置相對於目前的點陣位置，而點陣圖中對應至1s 的畫面格緩衝區圖元則是使用目前的點陣色彩或索引來撰寫。 不會修改對應至點陣圖中零的框架緩衝區圖元。

點陣圖影像的解讀方式就像是 [**glDrawPixels**](gldrawpixels.md) 函式的影像資料，其 *寬度* 和 *高度* 對應于該函式的寬度和高度引數，以及將 *type* 設定為 GL \_ 點陣圖，並將 *格式* 設定為 gl \_ 色彩 \_ 索引。 使用 [**glPixelStore**](glpixelstore-functions.md) 指定的模式會影響點陣圖影像資料的解讀;使用 [**glPixelTransfer**](glpixeltransfer.md) 指定的模式則否。

如果目前的點陣位置無效，則會忽略 **glBitmap** 。 否則，點陣圖影像的左下角會位於下列視窗座標：

*x*<sub>w</sub>  =  *x*<sub>r</sub> *x*？

*y*<sub>w</sub>  =  *y*<sub>r</sub> *y*？

在這些座標中， (*x*<sub>r</sub> 、 *y*<sub>r</sub> ) 是點陣位置，而 (*x*？ ， *y*？ ) 是點陣圖原點。 然後會為點陣圖影像中對應至1的每個圖元產生片段。 這些片段會使用目前的點陣 *z* 座標、色彩或色彩索引，以及目前的點陣材質座標來產生。 然後，系統會將它們視為由點、線條或多邊形產生，包括紋理對應、fogging，以及 Alpha 和深度測試等所有的每個片段作業。

繪製點陣圖之後，目前點陣位置的 *x* 和 *y* 座標會以 *xmove* 和 *ymove* 位移。 目前點陣位置的 *z* 座標或目前的點陣色彩、索引或材質座標都不會進行任何變更。

下列函式會取出與 **glBitmap** 函數相關的資訊：

[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 目前 \_ 點陣 \_ 位置的 glGet

 

具有引數 GL \_ 目前 \_ 點陣 \_ 色彩的 glGet

 

具有引數 GL \_ 目前 \_ 點陣 \_ 索引的 glGet

 

具有引數 GL \_ 目前 \_ 點陣 \_ 材質紋理 \_ 的 glGet

 

具有引數 GL \_ 目前 \_ 點陣 \_ 位置 \_ 有效的 glGet

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

[**glDrawPixels**](gldrawpixels.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glPixelStore**](glpixelstore-functions.md)
</dt> <dt>

[**glPixelTransfer**](glpixeltransfer.md)
</dt> <dt>

[**glRasterPos**](glrasterpos-functions.md)
</dt> </dl>

 

 





