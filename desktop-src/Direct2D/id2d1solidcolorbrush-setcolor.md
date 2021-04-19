---
title: ID2D1SolidColorBrush SetColor 方法
description: 指定此單色筆刷的色彩。
ms.assetid: 2900bf72-9641-419c-b0d7-334f14f8a474
keywords:
- SetColor 方法 Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: 580778135e840a69342ff34ffd8e415883317517
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987888"
---
# <a name="id2d1solidcolorbrushsetcolor-methods"></a>ID2D1SolidColorBrush：： SetColor 方法

指定此單色筆刷的色彩。

### <a name="overload-list"></a>多載清單



| 方法                                                                          | 描述                                                |
|:--------------------------------------------------------------------------------|:-----------------------------------------------------------|
| [**SetColor (D2D1 \_ COLOR \_ F&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1solidcolorbrush-setcolor(constd2d1_color_f_))  | 指定此單色筆刷的色彩。 <br/> |
| [**SetColor (D2D1 \_ COLOR \_ F \*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1solidcolorbrush-setcolor(constd2d1_color_f)) | 指定此單色筆刷的色彩。 <br/> |



## <a name="remarks"></a>備註

Direct2D 提供 [**ColorF**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) 類別，以協助建立色彩。 它提供數個 helper 方法來建立色彩，並提供一組或預先定義的色彩。

## <a name="examples"></a>範例

下列程式碼示範如何使用這個方法。


```C++
        m_pSolidColorBrush->SetColor(
            D2D1::ColorF(
                0.0f,
                intensity,
                1.0f - intensity
                ));

        hr = m_pRealization->Fill(
                m_pRT,
                m_pSolidColorBrush,
                m_useRealizations ?
                    REALIZATION_RENDER_MODE_DEFAULT :
                    REALIZATION_RENDER_MODE_FORCE_UNREALIZED
                );
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-------------------------------------------------------------------------------------|
| 程式庫<br/> | <dl> <dt>D2d1 .lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush)
</dt> </dl>

 

