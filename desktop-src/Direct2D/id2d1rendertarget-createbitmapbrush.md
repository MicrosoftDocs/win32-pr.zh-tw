---
title: ID2D1RenderTarget CreateBitmapBrush 方法
description: 從指定的點陣圖建立 ID2D1BitmapBrush。
ms.assetid: 7f6ef07e-4271-4605-aced-f191a0fe65af
keywords:
- CreateBitmapBrush 方法 Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: fcd512393a3f037cd3def40d4aa55003d9fddcef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996199"
---
# <a name="id2d1rendertargetcreatebitmapbrush-methods"></a>ID2D1RenderTarget：： CreateBitmapBrush 方法

從指定的點陣圖建立 [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) 。

### <a name="overload-list"></a>多載清單



| 方法                                                                                                                                                                                                                                                               | 描述                                                                                                                                                                                      |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateBitmapBrush (ID2D1Bitmap \* 、D2D1 \_ 點陣圖 \_ 筆刷 \_ 屬性&、D2D1 \_ 筆刷 \_ 屬性&、ID2D1BitmapBrush \* \*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createbitmap(d2d1_size_u_constvoid_uint32_constd2d1_bitmap_properties_id2d1bitmap))   | 從指定的點陣圖建立 [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) 。<br/>                                                                                                    |
| [**CreateBitmapBrush (ID2D1Bitmap \* 、D2D1 \_ 點陣圖 \_ 筆刷 \_ 屬性 \* 、D2D1 \_ 筆刷 \_ 屬性 \* 、ID2D1BitmapBrush \* \*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createbitmapbrush(id2d1bitmap_constd2d1_bitmap_brush_properties_constd2d1_brush_properties_id2d1bitmapbrush)) | 從指定的點陣圖建立 [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) 。<br/>                                                                                                    |
| [**CreateBitmapBrush (ID2D1Bitmap \* 、ID2D1BitmapBrush \* \*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createbitmapbrush(id2d1bitmap_id2d1bitmapbrush))                                                                                                                        | 從指定的點陣圖建立 [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) 。 筆刷會針對其擴充模式、插補模式、不透明度和轉換使用預設值。<br/> |
| [**CreateBitmapBrush (ID2D1Bitmap \* 、D2D1 \_ 點陣圖 \_ 筆刷 \_ 屬性&、ID2D1BitmapBrush \* \*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createbitmapbrush(id2d1bitmap_constd2d1_bitmap_brush_properties__id2d1bitmapbrush))                                                      | 從指定的點陣圖建立 [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) 。 筆刷會使用預設值作為其不透明度和轉換。<br/>                                   |



## <a name="examples"></a>範例

如需顯示如何使用點陣圖筆刷繪製區域的範例，請參閱 [如何建立點陣圖筆刷](how-to-create-a-bitmap-brush.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-------------------------------------------------------------------------------------|
| 程式庫<br/> | <dl> <dt>D2d1 .lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[如何建立點陣圖筆刷](how-to-create-a-bitmap-brush.md)
</dt> <dt>

[筆刷概觀](direct2d-brushes-overview.md)
</dt> </dl>

 

