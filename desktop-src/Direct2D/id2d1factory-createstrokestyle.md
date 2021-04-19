---
title: ID2D1Factory CreateStrokeStyle 方法
description: 建立描述開始端點、虛線模式和其他筆劃功能的 ID2D1StrokeStyle。
ms.assetid: cc7bd68b-a6eb-4d05-b331-032ce80f375c
keywords:
- CreateStrokeStyle 方法 Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: 09a578cafe6795bbf742d9dac114365d6e850586
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994900"
---
# <a name="id2d1factorycreatestrokestyle-methods"></a>ID2D1Factory：： CreateStrokeStyle 方法

建立描述開始端點、虛線模式和其他筆劃功能的 [**ID2D1StrokeStyle**](/windows/win32/api/d2d1/nn-d2d1-id2d1strokestyle) 。

### <a name="overload-list"></a>多載清單



| 方法                                                                                                                                                                                                  | 描述                                                                                                                                |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateStrokeStyle (D2D1 \_ 筆觸 \_ 樣式 \_ 屬性&、FLOAT \* 、UINT、ID2D1StrokeStyle \* \*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createstrokestyle(constd2d1_stroke_style_properties__constfloat_uint32_id2d1strokestyle))  | 建立描述開始端點、虛線模式和其他筆劃功能的 [**ID2D1StrokeStyle**](/windows/win32/api/d2d1/nn-d2d1-id2d1strokestyle) 。<br/> |
| [**CreateStrokeStyle (D2D1 \_ 筆觸 \_ 樣式 \_ 屬性 \* 、FLOAT \* 、UINT、ID2D1StrokeStyle \* \*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createstrokestyle(constd2d1_stroke_style_properties_constfloat_uint32_id2d1strokestyle)) | 建立描述開始端點、虛線模式和其他筆劃功能的 [**ID2D1StrokeStyle**](/windows/win32/api/d2d1/nn-d2d1-id2d1strokestyle) 。<br/> |



## <a name="examples"></a>範例

下列範例會建立使用自訂虛線模式的筆觸。


```C++
// Dash array for dashStyle D2D1_DASH_STYLE_CUSTOM
float dashes[] = {1.0f, 2.0f, 2.0f, 3.0f, 2.0f, 2.0f};

// Stroke Style with Dash Style -- Custom
if (SUCCEEDED(hr))
{
    hr = m_pD2DFactory->CreateStrokeStyle(
        D2D1::StrokeStyleProperties(
            D2D1_CAP_STYLE_FLAT,
            D2D1_CAP_STYLE_FLAT,
            D2D1_CAP_STYLE_ROUND,
            D2D1_LINE_JOIN_MITER,
            10.0f,
            D2D1_DASH_STYLE_CUSTOM,
            0.0f),
        dashes,
        ARRAYSIZE(dashes),
        &m_pStrokeStyleCustomOffsetZero
        );
}
```



下一個範例會在繪製線條時使用筆觸樣式。


```C++
m_pRenderTarget->DrawLine(
    D2D1::Point2F(0, 310),
    D2D1::Point2F(200, 310),
    m_pCornflowerBlueBrush,
    10.0f,
    m_pStrokeStyleCustomOffsetZero
    );
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-------------------------------------------------------------------------------------|
| 程式庫<br/> | <dl> <dt>D2d1 .lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)
</dt> </dl>

 

