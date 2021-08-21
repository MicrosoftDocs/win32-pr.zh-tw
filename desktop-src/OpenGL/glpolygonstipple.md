---
title: 'glPolygonStipple 函式 (Gl) '
description: GlPolygonStipple 函數會設定多邊形 stippling 模式。
ms.assetid: e066f9cf-36da-4a3b-a34f-2f8a6f5a0ae6
keywords:
- glPolygonStipple 函式 OpenGL
topic_type:
- apiref
api_name:
- glPolygonStipple
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1f9098ab91af5f258f97e0878ae8cbcb19863ec3bc82765c2664683830539fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118614904"
---
# <a name="glpolygonstipple-function"></a>glPolygonStipple 函式

**GlPolygonStipple** 函數會設定多邊形 stippling 模式。

## <a name="syntax"></a>語法


```C++
void WINAPI glPolygonStipple(
   const GLubyte *mask
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*面具* 
</dt> <dd>

32 stipple 模式的指標，會以 [**glDrawPixels**](gldrawpixels.md) 解壓縮圖元的相同方式從記憶體解壓縮。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="error-codes"></a>錯誤碼

[**GlGetError**](glgeterror.md)函式可以取出下列錯誤碼。



| 名稱                                                                                                  | 意義                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ 不正確 \_ 操作**</dt> </dl> | 呼叫 [**glBegin**](glbegin.md) 和對應的 [**glEnd**](glend.md)呼叫之間呼叫了函數。<br/> |



## <a name="remarks"></a>備註

**GlPolygonStipple** 函數會設定多邊形 stippling 模式。 多邊形 stippling，例如行 stippling (查看 [**glLineStipple**](gllinestipple.md)) 、遮罩由點陣產生的特定片段，並建立模式。 Stippling 與多邊形消除鋸齒無關。

*Mask* 參數是 32 stipple 模式的指標，其儲存在記憶體中，就像提供給 **glDrawPixels** 且 *高度* 和 *寬度* 都等於32的圖元資料、GL 色彩索引的圖元 *格式* \_ \_ ，以及 gl 點陣圖的資料 *類型* \_ 。 也就是說，stipple 模式會以非符號位元組封裝的1位色彩索引的32x32 陣列來表示。 [**GlPixelStore**](glpixelstore-functions.md)函式參數（例如 GL \_ 解壓縮 \_ 交換 \_ 位元組和 gl \_ 解壓縮 \_ LSB \_ ）會先影響將位組合成 stipple 模式。 不過，圖元傳輸作業 (shift、offset 和圖元地圖) 不會套用至 stipple 影像。

使用引數 GL 多邊形 STIPPLE，可使用 [**glEnable**](glenable.md) 和 **glDisable** 來啟用和停用多邊形 stippling \_ \_ 。 如果啟用，則只有在 (*x*<sub>w</sub> mod 32) 位在 stipple 模式的第一個資料列中的 (*y*<sub>w</sub> mod 32) 第一個資料列時，才會將具有視窗座標 *x*<sub>w</sub>和 *y*<sub>w</sub>的柵格化多邊形片段傳送至 OpenGL 的下一個階段。 當多邊形 stippling 停用時，就如同 stipple 模式都是一樣。

下列函式會取出與 **glPolygonStipple** 相關的資訊：

[**glGetPolygonStipple**](glgetpolygonstipple.md)

[](glisenabled.md)具有引數 GL \_ 多邊形 \_ STIPPLE 的 glIsEnabled

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

[**glLineStipple**](gllinestipple.md)
</dt> <dt>

[**glPixelStore**](glpixelstore-functions.md)
</dt> <dt>

[**glPixelTransfer**](glpixeltransfer.md)
</dt> </dl>

 

 





