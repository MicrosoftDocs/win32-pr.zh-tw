---
title: ID2D1RenderTarget CreateBitmapFromWicBitmap 方法
description: 藉由複製指定的 Microsoft Windows 影像處理元件 (WIC) 點陣圖來建立 ID2D1Bitmap。
ms.assetid: 463fc2f9-8ec6-47e8-8d48-a9015616e656
keywords:
- CreateBitmapFromWicBitmap 方法 Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: 23ad055beab9f24c39f032a3e28456c231480c68
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982267"
---
# <a name="id2d1rendertargetcreatebitmapfromwicbitmap-methods"></a>ID2D1RenderTarget：： CreateBitmapFromWicBitmap 方法

藉由複製指定的 Microsoft Windows 影像處理元件 (WIC) 點陣圖來建立 [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) 。

### <a name="overload-list"></a>多載清單



| 方法                                                                                                                                                                                                              | 描述                                                                                                                         |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateBitmapFromWicBitmap (IWICBitmapSource \* 、ID2D1Bitmap \* \*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createbitmapfromwicbitmap(iwicbitmapsource_id2d1bitmap))                                                       | 藉由複製指定的 Microsoft Windows 影像處理元件 (WIC) 點陣圖來建立 [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) 。<br/>  |
| [**CreateBitmapFromWicBitmap (IWICBitmapSource \* 、D2D1 \_ BITMAP \_ 屬性&、ID2D1Bitmap \* \*)**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapfromwicbitmap(iwicbitmapsource_constd2d1_bitmap_properties1__id2d1bitmap1))  | 藉由複製指定的 Microsoft Windows 影像處理元件 (WIC) 點陣圖來建立 [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) 。<br/> |
| [**CreateBitmapFromWicBitmap (IWICBitmapSource \* 、D2D1 \_ BITMAP \_ PROPERTIES \* 、ID2D1Bitmap \* \*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createbitmapfromwicbitmap(iwicbitmapsource_constd2d1_bitmap_properties_id2d1bitmap)) | 藉由複製指定的 Microsoft Windows 影像處理元件 (WIC) 點陣圖來建立 [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) 。<br/> |



## <a name="remarks"></a>備註

Direct2D 必須先轉換成支援的像素格式和 Alpha 模式，才能載入 WIC 映射。 如需支援的像素格式和 Alpha 模式清單，請參閱 [支援的像素格式和 Alpha 模式](supported-pixel-formats-and-alpha-modes.md)。

## <a name="examples"></a>範例

如需範例，請參閱 [如何從檔案載入點陣圖](how-to-load-a-direct2d-bitmap-from-a-file.md) ，以及 [如何從資源載入點陣圖](how-to-load-a-bitmap-from-a-resource.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-------------------------------------------------------------------------------------|
| 程式庫<br/> | <dl> <dt>D2d1 .lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap)
</dt> <dt>

[如何從檔案載入點陣圖](how-to-load-a-direct2d-bitmap-from-a-file.md)
</dt> <dt>

[支援的像素格式和 Alpha 模式](supported-pixel-formats-and-alpha-modes.md)
</dt> </dl>

 

