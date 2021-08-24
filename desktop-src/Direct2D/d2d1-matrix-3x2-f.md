---
title: 'D2D1_MATRIX_3X2_F (D2d1) '
description: 表示 3 x 2 矩陣。
ms.assetid: f05d7555-6482-4eea-950f-7b443892cc1f
keywords:
- D2D1_MATRIX_3X2_F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d4e8a50e17c4c740c427d21df27e3c1d9cf8226df5edc1b98f15cbe920c401c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119260488"
---
# <a name="d2d1_matrix_3x2_f"></a>D2D1 \_ 矩陣 \_ 3X2 \_ F

表示 3 x 2 矩陣。


```C++
typedef D2D_MATRIX_3X2_F D2D1_MATRIX_3X2_F;
```



## <a name="remarks"></a>備註

**D2D1 \_矩陣 \_ 3X2** 是 [**D2D \_ 矩陣 \_ 3X2 \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_3x2_f) 結構的新名稱。 如需矩陣所提供的欄位清單，請參閱 [**D2D \_ 矩陣 \_ 3X2 \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_3x2_f)。

為了簡化常見的矩陣作業，Direct2D 會提供 [**D2D1：： Matrix3x2F**](/windows/win32/api/d2d1helper/nl-d2d1helper-matrix3x2f) 類別，這是衍生自 [**D2D1 \_ 矩陣 \_ 3X2**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_3x2_f) 結構的類別。 **Matrix3x2F** 類別提供一組 helper 方法來執行一般工作，例如建立平移或扭曲矩陣。

## <a name="examples"></a>範例

下列範例會使用 [**D2D1：： Matrix3x2F：：輪替**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-rotation)方法來建立旋轉矩陣，以旋轉正方形中央的正方形45度，然後將矩陣傳遞給轉譯目標 (*m \_ pRenderTarget*) 的 [**SetTransform**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f_))方法。

下圖顯示將上述旋轉轉換套用至正方形的效果。 原始正方形是虛線外框，而旋轉的正方形是實心的外框。

![正方形的圖，與原始正方形的中心旋轉45度](images/rotate-ovw.png)


```C++
    // Create a rectangle.
    D2D1_RECT_F rectangle = D2D1::Rect(438.0f, 301.5f, 498.0f, 361.5f);

    // Draw the rectangle.
    m_pRenderTarget->DrawRectangle(
        rectangle,
        m_pOriginalShapeBrush,
        1.0f,
        m_pStrokeStyleDash
        );

    // Apply the rotation transform to the render target.
    m_pRenderTarget->SetTransform(
        D2D1::Matrix3x2F::Rotation(
            45.0f,
            D2D1::Point2F(468.0f, 331.5f))
        );

    // Fill the rectangle.
    m_pRenderTarget->FillRectangle(rectangle, m_pFillBrush);

    // Draw the transformed rectangle.
    m_pRenderTarget->DrawRectangle(rectangle, m_pTransformedShapeBrush);

```



此範例中省略了程式碼。 如需轉換的詳細資訊，請參閱 [轉換總覽](direct2d-transforms-overview.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 7、Windows vista （含 SP2），以及適用于 Windows Vista \[ desktop apps \| UWP 應用程式的平臺更新\]<br/>                          |
| 最低支援的伺服器<br/> | Windowsserver 2008 R2、Windows server 2008 SP2 和 Windows Server 的平臺更新 2008 \[ 桌面應用程式 \| UWP 應用程式\]<br/> |
| 支援的最小電話<br/>  | Windows Phone 8.1 \[ Windows Phone Silverlight 8.1 和 Windows 執行階段應用程式\]<br/>                                                  |
| 標頭<br/>                   | <dl> <dt>D2d1。h</dt> </dl>                                                        |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**D2D1::Matrix3x2F**](/windows/win32/api/d2d1helper/nl-d2d1helper-matrix3x2f)
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

[**D2D \_ 矩陣 \_ 3X2 \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_3x2_f)
</dt> </dl>

 

