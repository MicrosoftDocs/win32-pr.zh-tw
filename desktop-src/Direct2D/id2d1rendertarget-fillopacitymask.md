---
title: ID2D1RenderTarget FillOpacityMask 方法
description: 將指定點陣圖所描述的不透明度遮罩套用至筆刷，然後使用該筆刷來繪製轉譯目標的區域。
ms.assetid: a5e56d8a-2929-4f7b-b1c4-fb358c202721
keywords:
- FillOpacityMask 方法 Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: 362043696e4cbd21dd64783f210cf2e24066645e7dac5e303a16cd83abb31307
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119874078"
---
# <a name="id2d1rendertargetfillopacitymask-methods"></a>ID2D1RenderTarget：： FillOpacityMask 方法

將指定點陣圖所描述的不透明度遮罩套用至筆刷，然後使用該筆刷來繪製轉譯目標的區域。

### <a name="overload-list"></a>多載清單



| 方法                                                                                                                                                                                                                          | 描述                                                                                                                                   |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------|
| [**FillOpacityMask (ID2D1Bitmap \* 、ID2D1Brush \* 、D2D1 \_ 不透明度 \_ 遮罩 \_ 內容、D2D \_ rect \_ f&、D2D \_ rect \_ f&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillopacitymask(id2d1bitmap_id2d1brush_d2d1_opacity_mask_content_constd2d1_rect_f__constd2d1_rect_f_))       | 將指定點陣圖所描述的不透明度遮罩套用至筆刷，然後使用該筆刷來繪製轉譯目標的區域。 <br/> |
| [**FillOpacityMask (ID2D1Bitmap \* 、ID2D1Brush \* 、D2D1 \_ 不透明度 \_ 遮罩 \_ 內容、 \_ D2D rect \_ f \* 、D2D \_ rect \_ f \*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillopacitymask(id2d1bitmap_id2d1brush_d2d1_opacity_mask_content_constd2d1_rect_f_constd2d1_rect_f)) | 將指定點陣圖所描述的不透明度遮罩套用至筆刷，然後使用該筆刷來繪製轉譯目標的區域。 <br/> |



## <a name="remarks"></a>備註

為了讓這個方法正常運作，轉譯目標必須使用 [**D2D1 的消除鋸齒 \_ \_ 模式 \_ 別名**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_antialias_mode) 消除鋸齒模式。 您可以藉由呼叫 [**ID2D1RenderTarget：： SetAntialiasMode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-setantialiasmode) 方法來設定消除鋸齒模式。

如果失敗，這個方法不會傳回錯誤碼。 若要判斷繪圖作業 (如 **FillOpacityMask**) 是否失敗，請檢查 [**ID2D1RenderTarget：： EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) 或 [**ID2D1RenderTarget：： Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) 方法所傳回的結果。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-------------------------------------------------------------------------------------|
| 程式庫<br/> | <dl> <dt>D2d1 .lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> </dl>

 

