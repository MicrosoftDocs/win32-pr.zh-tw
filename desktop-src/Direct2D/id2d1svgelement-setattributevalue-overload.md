---
title: 'ID2D1SvgElement SetAttributeValue 方法 (D2d1svg .h) '
description: 設定這個元素的屬性。
ms.assetid: 33403a07-28d1-4138-ea7f-04f3ac42a8f7
keywords:
- SetAttributeValue 方法 Direct2D
topic_type:
- apiref
api_location:
- d2d1svg.h
api_type:
- HeaderDef
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: c49f224d364523653e13fb7b6cc141e8e8c6eca7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000862"
---
# <a name="id2d1svgelementsetattributevalue-methods"></a>ID2D1SvgElement：： SetAttributeValue 方法

設定這個元素的屬性。

### <a name="overload-list"></a>多載清單



| 方法                                                                                                                      | 描述                                                                                                                                                 |
|:----------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SetAttributeValue (PCWSTR，FLOAT)**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-setattributevalue(pcwstr_float))                                             | 使用 float 設定這個元素的屬性。<br/>                                                                                                 |
| [**SetAttributeValue (PCWSTR、D2D1 \_ COLOR \_ F &)**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-setattributevalue(pcwstr_constd2d1_color_f_))                                  | 將這個元素的屬性設定為色彩。<br/>                                                                                                    |
| [**SetAttributeValue (PCWSTR、D2D1 \_ 填滿 \_ 模式)**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-setattributevalue(pcwstr_d2d1_fill_mode))                                  | 將這個元素的屬性設定為填滿模式。 這個方法可以用來設定「填滿規則」或「剪輯規則」屬性的值。<br/>         |
| [**SetAttributeValue (PCWSTR、D2D1 \_ SVG \_ 顯示)**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-setattributevalue(pcwstr_d2d1_svg_display))                                | 取得這個元素的屬性做為顯示值。 這個方法可以用來取得顯示內容的值。<br/>                          |
| [**SetAttributeValue (PCWSTR、D2D1 \_ 擴充 \_ 模式)**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-setattributevalue(pcwstr_d2d1_extend_mode))                               | 將這個元素的屬性設定為延伸模式值。 這個方法可以用來設定 spreadMethod 屬性的值。<br/>                 |
| [**SetAttributeValue (PCWSTR、D2D1 \_ SVG \_ 溢位)**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-setattributevalue(pcwstr_d2d1_svg_overflow))                               | 將這個元素的屬性設定為溢位值。 這個方法可以用來設定溢位屬性的值。<br/>                       |
| [**SetAttributeValue (PCWSTR、D2D1 \_ SVG \_ 行 \_ 帽)**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-setattributevalue(pcwstr_d2d1_svg_line_cap))                             | 將這個元素的屬性設定為線條端點值。 這個方法可以用來設定 linecap 屬性的值。<br/>                  |
| [**SetAttributeValue (PCWSTR、D2D1 \_ SVG \_ 長度 &)**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-setattributevalue(pcwstr_constd2d1_svg_length_))                              | 將這個元素的屬性設定為長度值。<br/>                                                                                             |
| [**SetAttributeValue (PCWSTR、D2D1 \_ SVG \_ LINE \_ JOIN)**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-setattributevalue(pcwstr_d2d1_svg_line_join))                             | 將這個元素的屬性設定為行聯結值。 這個方法可以用來設定 linejoin 屬性的值。<br/>                |
| [**SetAttributeValue (PCWSTR、D2D1 \_ SVG \_ 單位 \_ 類型)**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-setattributevalue(pcwstr_d2d1_svg_unit_type))                            | 將這個元素的屬性設定為單位類型值。 這個方法可以用來設定 gradientUnits 或 clipPathUnits 屬性的值。<br/>  |
| [**SetAttributeValue (PCWSTR、ID2D1SvgAttribute \*)**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-setattributevalue(pcwstr_id2d1svgattribute))                              | 使用介面設定這個元素的屬性。<br/>                                                                                            |
| [**SetAttributeValue (PCWSTR、D2D1 \_ SVG \_ 可見度)**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-setattributevalue(pcwstr_d2d1_svg_visibility))                            | 將這個元素的屬性設定為可見度值。 這個方法可以用來設定 visibility 屬性的值。<br/>                    |
| [**SetAttributeValue (PCWSTR、D2D1 \_ MATRIX \_ 3X2 \_ F &)**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-setattributevalue(pcwstr_constd2d1_matrix_3x2_f_))                           | 將這個元素的屬性設定為矩陣值。 這個方法可以用來設定轉換或 gradientTransform 屬性的值。<br/>     |
| [**SetAttributeValue (PCWSTR、D2D1 \_ SVG \_ 保持 \_ 外觀 \_ 比例 &)**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-setattributevalue(pcwstr_constd2d1_svg_preserve_aspect_ratio_))             | 將這個元素的屬性設定為保留長寬比值。 這個方法可以用來設定 preserveAspectRatio 屬性的值。<br/> |
| [**SetAttributeValue (PCWSTR、D2D1 \_ SVG \_ 屬性 \_ 字串 \_ 類型、PCWSTR)**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-setattributevalue(pcwstr_d2d1_svg_attribute_string_type_pcwstr))          | 使用字串設定這個元素的屬性。 <br/>                                                                                               |
| [**SetAttributeValue (PCWSTR、D2D1 \_ SVG \_ ATTRIBUTE \_ POD \_ TYPE、void \* 、UINT32)**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-setattributevalue(pcwstr_d2d1_svg_attribute_pod_type_constvoid_uint32)) | 使用 POD 類型設定這個專案的屬性。<br/>                                                                                              |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|--------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D2d1svg。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ID2D1SvgElement**](/windows/win32/api/d2d1svg/nn-d2d1svg-id2d1svgelement)
</dt> </dl>

�

�
