---
title: ID2D1Factory CreateWicBitmapRenderTarget 方法
description: 建立呈現至 Microsoft Windows 影像處理元件 (WIC) 點陣圖的轉譯目標。
ms.assetid: 93141743-c11d-40b4-83c5-07c9066836c7
keywords:
- CreateWicBitmapRenderTarget 方法 Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: 177f5459d8245292e2962e502882bb86643f3f8b777efd8a336fde5f8c671897
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119698178"
---
# <a name="id2d1factorycreatewicbitmaprendertarget-methods"></a>ID2D1Factory：： CreateWicBitmapRenderTarget 方法

建立呈現至 Microsoft Windows 影像處理元件 (WIC) 點陣圖的轉譯目標。

### <a name="overload-list"></a>多載清單



| 方法                                                                                                                                                                                                                            | 描述                                                                                            |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------|
| [**CreateWicBitmapRenderTarget (IWICBitmap \* 、D2D1 \_ 轉譯 \_ 目標 \_ 屬性 \* 、ID2D1RenderTarget \* \*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createwicbitmaprendertarget(iwicbitmap_constd2d1_render_target_properties_id2d1rendertarget)) | 建立呈現至 Microsoft Windows 影像處理元件 (WIC) 點陣圖的轉譯目標。<br/> |
| [**CreateWicBitmapRenderTarget (IWICBitmap \* 、D2D1 \_ 轉譯 \_ 目標 \_ 屬性&、ID2D1RenderTarget \* \*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createwicbitmaprendertarget(iwicbitmap_constd2d1_render_target_properties__id2d1rendertarget))  | 建立呈現至 Microsoft Windows 影像處理元件 (WIC) 點陣圖的轉譯目標。<br/> |



## <a name="remarks"></a>備註

您的應用程式應該建立轉譯目標一次，並在應用程式的存留期內保存它們，或在收到 [**D2DERR \_ 重新建立 \_ 目標**](direct2d-error-codes.md) 錯誤之前保留。 當您收到此錯誤時，您必須重新建立轉譯目標 (以及它所建立) 的任何資源。

**注意**  Windows Phone 上不支援此方法，而且在裝置上呼叫時將會失敗，並出現錯誤碼 0x8899000b ( 此作業 ) 沒有硬體轉譯裝置可用。 因為 Windows Phone Emulator 支援變形轉譯，所以在模擬器上使用不同的錯誤碼（0x88982f80 (wincodec \_ err unsupporteDPIxelformat) ）呼叫時，這個方法將會失敗 \_ 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-------------------------------------------------------------------------------------|
| 程式庫<br/> | <dl> <dt>D2d1 .lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)
</dt> </dl>

 

