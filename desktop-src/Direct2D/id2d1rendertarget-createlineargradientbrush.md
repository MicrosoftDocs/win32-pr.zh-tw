---
title: 'ID2D1RenderTarget CreateLinearGradientBrush 方法 (D2d1 .h) '
description: 建立 ID2D1LinearGradientBrush 物件，以使用線性漸層繪製區域。
ms.assetid: dc07113f-ff93-4b0f-8328-02dd481dccb0
keywords:
- CreateLinearGradientBrush 方法 Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 428fcb44ddf50af7b3e78c28e359430bceee2f79
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998747"
---
# <a name="id2d1rendertargetcreatelineargradientbrush-methods"></a>ID2D1RenderTarget：： CreateLinearGradientBrush 方法

建立 [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) 物件，以使用線性漸層繪製區域。

### <a name="overload-list"></a>多載清單



| 方法                                                                                                                                                                                                                       | 描述                                                                                                                                                                      |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateLinearGradientBrush (D2D1 \_ 線性漸層 \_ \_ 筆刷 \_ 屬性&、ID2D1GradientStopCollection \* 、ID2D1LinearGradientBrush \* \*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush))                            | 建立包含指定的漸層停駐點、沒有任何轉換，而且基底不透明度為1.0 的 [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) 。 <br/> |
| [**CreateLinearGradientBrush (D2D1 \_ 線性漸層 \_ \_ 筆刷 \_ 屬性&、D2D1 \_ 筆刷 \_ 屬性&、ID2D1GradientStopCollection \* 、ID2D1LinearGradientBrush \* \*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush))   | 建立 [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) ，其中包含指定的漸層停駐點，並具有指定的轉換和基底不透明度。 <br/> |
| [**CreateLinearGradientBrush (D2D1 \_ 線性漸層 \_ \_ 筆刷 \_ 屬性 \* 、D2D1 \_ 筆刷 \_ 屬性 \* 、ID2D1GradientStopCollection \* 、ID2D1LinearGradientBrush \* \*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush)) | 建立 [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) ，其中包含指定的漸層停駐點，並具有指定的轉換和基底不透明度。 <br/> |



## <a name="examples"></a>範例

如需示範如何建立梯度停駐點，並使用它來定義線性漸層的範例，請參閱 [如何建立線性漸層筆刷](how-to-create-a-linear-gradient-brush.md)。

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

[**CreateGradientStopCollection**](id2d1rendertarget-creategradientstopcollection.md)
</dt> <dt>

[**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection)
</dt> <dt>

[**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush)
</dt> <dt>

[**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush)
</dt> <dt>

[如何建立線性漸層筆刷](how-to-create-a-linear-gradient-brush.md)
</dt> <dt>

[筆刷概觀](direct2d-brushes-overview.md)
</dt> </dl>

�

�
