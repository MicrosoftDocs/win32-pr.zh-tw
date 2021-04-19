---
title: 'ID2D1RenderTarget DrawEllipse 方法 (D2d1 .h) '
description: 繪製具有指定維度和筆劃的橢圓形大綱。
ms.assetid: dabbb399-2d72-41c3-8b2f-aea49d7ad0cb
keywords:
- DrawEllipse 方法 Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 9647591b5033b912283500a0ddb1dba20004ec38
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994626"
---
# <a name="id2d1rendertargetdrawellipse-methods"></a>ID2D1RenderTarget：:D rawEllipse 方法

繪製具有指定維度和筆劃的橢圓形大綱。

### <a name="overload-list"></a>多載清單



| 方法                                                                                                                                                                 | 描述                                                                              |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------|
| [**DrawEllipse (D2D1 \_ 橢圓形&、ID2D1Brush \* 、FLOAT、ID2D1StrokeStyle \*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawellipse(constd2d1_ellipse__id2d1brush_float_id2d1strokestyle))  | 使用指定的筆觸樣式繪製指定之橢圓形的輪廓。 <br/> |
| [**DrawEllipse (D2D1 \_ 橢圓形 \* 、ID2D1Brush \* 、FLOAT、ID2D1StrokeStyle \*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawellipse(constd2d1_ellipse__id2d1brush_float_id2d1strokestyle)) | 使用指定的筆觸樣式繪製指定之橢圓形的輪廓。 <br/> |



## <a name="remarks"></a>備註

**DrawEllipse** 方法不會在失敗時傳回錯誤碼。 若要判斷繪圖作業 (如 **DrawEllipse**) 是否失敗，請檢查 [**ID2D1RenderTarget：： EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) 或 [**ID2D1RenderTarget：： Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) 方法所傳回的結果。

## <a name="examples"></a>範例

如需範例，請參閱 [如何繪製和填滿基本圖形](how-to-draw-an-ellipse.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D2d1。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>D2d1 .lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[**FillEllipse**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse_id2d1brush))
</dt> </dl>

�

�
