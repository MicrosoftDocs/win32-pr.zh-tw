---
title: 'ID2D1RenderTarget CreateRadialGradientBrush 方法 (D2d1 .h) '
description: 建立 ID2D1RadialGradientBrush 物件，這個物件可以用來繪製具有放射狀漸層的區域。
ms.assetid: 985a4c1b-d29b-46ed-bc55-6dcd313718a8
keywords:
- CreateRadialGradientBrush 方法 Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: b32c384e55f8c6ac17551c290c36e1130c05d5939fd5cf56116410ddac37320f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108818"
---
# <a name="id2d1rendertargetcreateradialgradientbrush-methods"></a>ID2D1RenderTarget：： CreateRadialGradientBrush 方法

建立 [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) 物件，這個物件可以用來繪製具有放射狀漸層的區域。

### <a name="overload-list"></a>多載清單



| 方法                                                                                                                                                                                                                       | 描述                                                                                                                                                                      |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateRadialGradientBrush (D2D1 \_ 放射漸層 \_ \_ 筆刷 \_ 屬性&、ID2D1GradientStopCollection \* 、ID2D1RadialGradientBrush \* \*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createradialgradientbrush(constd2d1_radial_gradient_brush_properties__id2d1gradientstopcollection_id2d1radialgradientbrush))                            | 建立包含指定的漸層停駐點、沒有任何轉換，而且基底不透明度為1.0 的 [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) 。 <br/> |
| [**CreateRadialGradientBrush (D2D1 \_ 放射漸層 \_ \_ 筆刷 \_ 屬性&、D2D1 \_ 筆刷 \_ 屬性&、ID2D1GradientStopCollection \* 、ID2D1RadialGradientBrush \* \*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createradialgradientbrush(constd2d1_radial_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1radialgradientbrush))   | 建立 [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) ，其中包含指定的漸層停駐點，並具有指定的轉換和基底不透明度。 <br/> |
| [**CreateRadialGradientBrush (D2D1 \_ 放射漸層 \_ \_ 筆刷 \_ 屬性 \* 、D2D1 \_ 筆刷 \_ 屬性 \* 、ID2D1GradientStopCollection \* 、ID2D1RadialGradientBrush \* \*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createradialgradientbrush(constd2d1_radial_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1radialgradientbrush)) | 建立 [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) ，其中包含指定的漸層停駐點，並具有指定的轉換和基底不透明度。 <br/> |



## <a name="examples"></a>範例

如需範例，請參閱 [如何建立放射狀漸層筆刷](how-to-create-a-radial-gradient-brush.md)。

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

[如何建立放射狀漸層筆刷](how-to-create-a-radial-gradient-brush.md)
</dt> <dt>

[筆刷概觀](direct2d-brushes-overview.md)
</dt> </dl>

�

�
