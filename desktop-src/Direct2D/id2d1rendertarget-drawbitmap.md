---
title: ID2D1RenderTarget DrawBitmap 方法
description: 繪製指定的 ID2D1Bitmap。
ms.assetid: 241df698-ca5e-4d94-902a-a9e140820c14
keywords:
- DrawBitmap 方法 Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: d82bbf557d7e53f06f614afbba578de40c789953
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989530"
---
# <a name="id2d1rendertargetdrawbitmap-methods"></a>ID2D1RenderTarget：:D rawBitmap 方法

繪製指定的 [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap)。

### <a name="overload-list"></a>多載清單



| 方法                                                                                                                                                                                                                       | 描述                                                                                     |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------|
| [**DrawBitmap (ID2D1Bitmap \* 、D2D1 \_ RECT \_ F&、FLOAT、D2D1 \_ 點陣圖 \_ 插補 \_ 模式、D2D1 \_ RECT \_ F&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawbitmap(id2d1bitmap_constd2d1_rect_f__float_d2d1_bitmap_interpolation_mode_constd2d1_rect_f_))   | 將指定的點陣圖調整為指定矩形的大小之後，繪製該點陣圖。 <br/> |
| [**DrawBitmap (ID2D1Bitmap \* 、D2D1 \_ RECT \_ F&、FLOAT、D2D1 \_ 點陣圖 \_ 插補 \_ 模式、D2D1 \_ RECT \_ F \*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawbitmap(id2d1bitmap_constd2d1_rect_f__float_d2d1_bitmap_interpolation_mode_constd2d1_rect_f))  | 將指定的點陣圖調整為指定矩形的大小之後，繪製該點陣圖。 <br/> |
| [**DrawBitmap (ID2D1Bitmap \* 、D2D1 \_ RECT \_ F \* 、FLOAT、D2D1 \_ 點陣圖 \_ 插補 \_ 模式、D2D1 \_ RECT \_ F \*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawbitmap(id2d1bitmap_constd2d1_rect_f_float_d2d1_bitmap_interpolation_mode_constd2d1_rect_f)) | 將指定的點陣圖調整為指定矩形的大小之後，繪製該點陣圖。 <br/> |



## <a name="remarks"></a>備註

如果失敗，這個方法不會傳回錯誤碼。 若要判斷繪圖作業 (如 **DrawBitmap**) 是否失敗，請檢查 [**ID2D1RenderTarget：： EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) 或 [**ID2D1RenderTarget：： Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) 方法所傳回的結果。

## <a name="examples"></a>範例

如需範例，請參閱 [如何繪製點陣圖](how-to-draw-a-bitmap.md)。 如需示範如何從資源或檔案載入點陣圖的範例，請參閱如何從 [資源載入](how-to-load-a-bitmap-from-a-resource.md) 點陣圖，以及 [如何從](how-to-load-a-direct2d-bitmap-from-a-file.md)檔案載入點陣圖。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-------------------------------------------------------------------------------------|
| 程式庫<br/> | <dl> <dt>D2d1 .lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[如何繪製點陣圖](how-to-draw-a-bitmap.md)
</dt> <dt>

[如何從資源載入點陣圖](how-to-load-a-bitmap-from-a-resource.md)
</dt> <dt>

[如何從檔案載入點陣圖](how-to-load-a-direct2d-bitmap-from-a-file.md)
</dt> </dl>

 

