---
title: 'glPixelZoom 函式 (Gl) '
description: GlPixelZoom 函式會指定圖元縮放因數。
ms.assetid: 57ead7d8-0502-46b4-9f66-dbb3cb75b0f9
keywords:
- glPixelZoom 函式 OpenGL
topic_type:
- apiref
api_name:
- glPixelZoom
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 065e1735ca0228046cfb08e2fb441d3cdc02af74
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "106986006"
---
# <a name="glpixelzoom-function"></a>glPixelZoom 函式

**GlPixelZoom** 函式會指定圖元縮放因數。

## <a name="syntax"></a>語法


```C++
void WINAPI glPixelZoom(
   GLfloat xfactor,
   GLfloat yfactor
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*xfactor* 
</dt> <dd>

圖元寫入作業的 *x* 縮放比例。

</dd> <dt>

*yfactor* 
</dt> <dd>

圖元寫入作業的 *y* 縮放係數。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="error-codes"></a>錯誤碼

[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。



| Name                                                                                                  | 意義                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ 不正確 \_ 操作**</dt> </dl> | 呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。<br/> |



## <a name="remarks"></a>備註

**GlPixelZoom** 函式會指定 *x* 和 *y* 縮放因數的值。 執行 [**glDrawPixels**](gldrawpixels.md) 或 [**glCopyPixels**](glcopypixels.md)時，如果 (*x*<sub>r</sub> ，*y*<sub>r</sub> ) 是目前的點陣位置，而指定的元素位於圖元矩形的第 *n* 個數據列和第 *m* 個數據行中，則其中心位於矩形中的圖元，而矩形的邊角為

![顯示要取代之圖元位置的方程式。](images/pix05.png)

是取代的候選項目。 中心位於這個矩形區域底部或左邊緣的任何圖元也會一併修改。

圖元縮放因數不限於正值。 負縮放因數會反映目前點陣位置的結果影像。

下列函式會取出與 **glPixelZoom** 相關的資訊：

[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ ZOOM \_ X 的 glGet

具有引數 GL \_ ZOOM \_ Y 的 glGet

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
</dt> </dl>

 

 





