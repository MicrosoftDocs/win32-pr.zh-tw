---
title: 'glGetPolygonStipple 函式 (Gl) '
description: GlGetPolygonStipple 函數會傳回多邊形 stipple 模式。
ms.assetid: 95c1ebfa-8465-4bc1-b3f5-eed696a83816
keywords:
- glGetPolygonStipple 函式 OpenGL
topic_type:
- apiref
api_name:
- glGetPolygonStipple
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 643d0ea6b7583f26565ab7b9233f7df1dce9aead
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843232"
---
# <a name="glgetpolygonstipple-function"></a>glGetPolygonStipple 函式

**GlGetPolygonStipple** 函數會傳回多邊形 stipple 模式。

## <a name="syntax"></a>語法


```C++
void WINAPI glGetPolygonStipple(
   GLubyte *mask
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*面具* 
</dt> <dd>

傳回 stipple 模式。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="error-codes"></a>錯誤碼

[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。



| Name                                                                                                  | 意義                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ 不正確 \_ 操作**</dt> </dl> | 呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。<br/> |



## <a name="remarks"></a>備註

**GlGetPolygonStipple** 函數會透過 *mask* 參數傳回32x32 多邊形 stipple 模式。 模式會封裝至記憶體中，如同 [**glReadPixels**](glreadpixels.md) 具有32的 *高度* 和 *寬度* 、gl 點陣圖的 *型* 別 \_ ，以及 gl 色彩索引的 *格式* ， \_ \_ 而且 stipple 模式儲存在內部的32x32 色彩索引緩衝區中。 不過，不同于 **glReadPixels**，圖元傳輸作業 (shift、offset 和圖元地圖) 不會套用至傳回的 stipple 影像。

如果產生錯誤，則不會對 *遮罩* 的內容進行任何變更。

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

[**glPixelStore**](glpixelstore-functions.md)
</dt> <dt>

[**glPixelTransfer**](glpixeltransfer.md)
</dt> <dt>

[**glPolygonStipple**](glpolygonstipple.md)
</dt> <dt>

[**glReadPixels**](glreadpixels.md)
</dt> </dl>

 

 





