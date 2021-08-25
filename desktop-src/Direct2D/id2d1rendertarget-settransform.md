---
title: ID2D1RenderTarget SetTransform 方法
description: 將指定的轉換套用至轉譯目標，並取代現有的轉換。 所有後續繪圖作業都會出現在已轉換的空間中。
ms.assetid: 04799366-6458-40ff-a2fb-5d227eab041d
keywords:
- SetTransform 方法 Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: f23ffcd8d64df02b0be2287a33eff63a6a680200c0e051a15c77958dafd81438
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119873958"
---
# <a name="id2d1rendertargetsettransform-methods"></a>ID2D1RenderTarget：： SetTransform 方法

將指定的轉換套用至轉譯目標，並取代現有的轉換。 所有後續繪圖作業都會出現在已轉換的空間中。

### <a name="overload-list"></a>多載清單



| 方法                                                                                              | 描述                                                                                                                                                                |
|:----------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SetTransform (D2D1 \_ 矩陣 \_ 3X2 \_ F&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settransform(constd2d1_matrix_3x2_f_))  | 將指定的轉換套用至轉譯目標，並取代現有的轉換。 所有後續繪圖作業都會出現在已轉換的空間中。 <br/> |
| [**SetTransform (D2D1 \_ 矩陣 \_ 3X2 \_ F \*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settransform(constd2d1_matrix_3x2_f)) | 將指定的轉換套用至轉譯目標，並取代現有的轉換。 所有後續繪圖作業都會出現在已轉換的空間中。<br/>  |



## <a name="examples"></a>範例

下列範例會使用 **SetTransform** 方法，將旋轉套用至呈現目標。 如需完整範例，請參閱 [如何旋轉物件](how-to-rotate.md)。


```C++
// Apply the rotation transform to the render target.
m_pRenderTarget->SetTransform(
    D2D1::Matrix3x2F::Rotation(
        45.0f,
        D2D1::Point2F(468.0f, 331.5f))
    );
```



如需顯示如何轉換轉譯目標的其他範例，請參閱 [如何調整物件](how-to-scale.md)、 [如何扭曲物件](how-to-skew.md)，以及 [如何轉譯物件](how-to-translate.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-------------------------------------------------------------------------------------|
| 程式庫<br/> | <dl> <dt>D2d1 .lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[轉換總覽](direct2d-transforms-overview.md)
</dt> <dt>

[如何旋轉物件](how-to-rotate.md)
</dt> <dt>

[如何調整物件](how-to-scale.md)
</dt> <dt>

[如何扭曲物件](how-to-skew.md)
</dt> <dt>

[如何轉譯物件](how-to-translate.md)
</dt> <dt>

[如何將多個轉換套用至物件](how-to-apply-multiple-transforms.md)
</dt> </dl>

 

