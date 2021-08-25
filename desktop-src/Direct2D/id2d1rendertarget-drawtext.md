---
title: ID2D1RenderTarget DrawText 方法
description: 使用 IDWriteTextFormat 物件所提供的格式資訊，繪製指定的文字。
ms.assetid: 7cda7854-f9df-48d3-bc62-6aaee769e6f9
keywords:
- DrawText 方法 Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: 430607b09795be249a05398b1bfb749e9be45ae517c6374e001a4c3042bf316f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119874188"
---
# <a name="id2d1rendertargetdrawtext-methods"></a>ID2D1RenderTarget：:D rawText 方法

使用 [**IDWriteTextFormat**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextformat) 物件所提供的格式資訊，繪製指定的文字。

### <a name="overload-list"></a>多載清單



| 方法                                                                                                                                                                                                                                                                               | 描述                                                                                                                                     |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DrawText (WCHAR \* 、IDWriteTextFormat \* 、D2D1 \_ RECT \_ F&、ID2D1Brush \* 、D2D1 \_ DRAW \_ text \_ 選項、DWRITE \_ 文字 \_ 測量 \_ 方法)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode))  | 使用 [**IDWriteTextFormat**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextformat) 物件所提供的格式資訊，繪製指定的文字。<br/>  |
| [**DrawText (WCHAR \* 、IDWriteTextFormat \* 、D2D1 \_ RECT \_ F \* 、ID2D1Brush \* 、D2D1 \_ DRAW \_ text \_ 選項、DWRITE \_ TEXT \_ 測量 \_ 方法)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f_id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) | 使用 [**IDWriteTextFormat**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextformat) 物件所提供的格式資訊，繪製指定的文字。 <br/> |



## <a name="remarks"></a>備註

若要使用 Direct2D 來繪製文字，請針對具有單一格式的文字使用 [**ID2D1RenderTarget：:D rawtext**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) 方法，或者，如果您需要多種格式、先進的 OpenType 功能或點擊測試，請使用 [**ID2D1RenderTarget：:D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) 方法。 這些方法會使用 DirectWrite API 來提供高品質的文字顯示。

如果失敗，這個方法不會傳回錯誤碼。 若要判斷繪圖作業 (如 **DrawText**) 是否失敗，請檢查 [**ID2D1RenderTarget：： EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) 或 [**ID2D1RenderTarget：： Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) 方法所傳回的結果。

## <a name="examples"></a>範例

如需範例，請參閱 [如何繪製文字](how-to--draw-text.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-------------------------------------------------------------------------------------|
| 程式庫<br/> | <dl> <dt>D2d1 .lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[**IDWriteTextFormat**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextformat)
</dt> <dt>

[如何繪製文字](how-to--draw-text.md)
</dt> <dt>

[文字格式設定和版面配置總覽](/windows/desktop/DirectWrite/text-formatting-and-layout)
</dt> </dl>

 

