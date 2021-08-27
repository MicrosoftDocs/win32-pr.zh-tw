---
title: ID2D1SvgElement GetAttributeValue 方法
description: 取得這個元素的屬性。
ms.assetid: 2f6ca40a-6c78-9c60-c06a-a31f6edf7663
keywords:
- GetAttributeValue 方法 Direct2D
topic_type:
- apiref
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
api_location: ''
ms.openlocfilehash: cfc85f2af132c52a95f196aa6e0722b4d75ccc9bc8a4b7a1abb992cc581a6f32
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120076848"
---
# <a name="id2d1svgelementgetattributevalue-methods"></a>ID2D1SvgElement：： GetAttributeValue 方法

取得這個元素的屬性。

### <a name="overload-list"></a>多載清單



| 方法                                                                                                                     | 描述                                                                                                                                                 |
|:---------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetAttributeValue (PCWSTR，FLOAT \*)**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_float))                                         | 取得這個元素的屬性（float）。<br/>                                                                                                    |
| [**GetAttributeValue (PCWSTR，D2D1 \_ COLOR \_ F \*)**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig)                                | 取得這個元素的屬性做為色彩。<br/>                                                                                                    |
| [**GetAttributeValue (PCWSTR、REFIID、void \* \*)**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_refiid_void))                                | 取得這個專案的屬性，做為介面型別。 <br/>                                                                                         |
| [**GetAttributeValue (PCWSTR、D2D1 \_ 填滿 \_ 模式 \*)**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_fill_mode))                              | 取得這個元素的屬性做為填滿模式。 這個方法可以用來取得填滿規則或剪輯規則屬性的值。<br/>             |
| [**GetAttributeValue (PCWSTR、ID2D1SvgPaint \* \*)**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_id2d1svgpaint))                              | 取得這個元素的屬性做為繪製。 這個方法可以用來取得填滿或筆觸屬性的值。<br/>                         |
| [**GetAttributeValue (PCWSTR、D2D1 \_ SVG \_ 長度 \*)**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_svg_length))                            | 取得這個元素的屬性做為長度值。<br/>                                                                                             |
| [**GetAttributeValue (PCWSTR、D2D1 \_ SVG \_ 顯示 \*)**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_svg_display))                            | 取得這個元素的屬性做為顯示值。 這個方法可以用來取得顯示內容的值。<br/>                          |
| [**GetAttributeValue (PCWSTR、D2D1 \_ 擴充 \_ 模式 \*)**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_extend_mode))                           | 取得這個專案的屬性，做為擴充模式值。 這個方法可以用來取得 spreadMethod 屬性的值。<br/>                  |
| [**GetAttributeValue (PCWSTR、D2D1 \_ SVG \_ 溢位 \*)**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_svg_overflow))                           | 取得這個元素的屬性做為溢位值。 這個方法可以用來取得溢位屬性的值。<br/>                       |
| [**GetAttributeValue (PCWSTR、D2D1 \_ SVG \_ 行 \_ 帽 \*)**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_svg_line_cap))                         | 取得這個元素的屬性做為行端點值。 這個方法可以用來取得 linecap 屬性的值。<br/>                  |
| [**GetAttributeValue (PCWSTR、D2D1 \_ MATRIX \_ 3X2 \_ F \*)**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_matrix_3x2_f))                         | 取得這個專案的屬性（attribute）作為矩陣值。 這個方法可以用來取得轉換或 gradientTransform 屬性的值。<br/>     |
| [**GetAttributeValue (PCWSTR、ID2D1SvgPathData \* \*)**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_id2d1svgpathdata))                           | 取得這個元素的屬性做為路徑資料。 這個方法可以用來取得 path 元素上 d 屬性的值。<br/>                   |
| [**GetAttributeValue (PCWSTR、D2D1 \_ SVG \_ LINE \_ JOIN \*)**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_svg_line_join))                         | 取得這個專案的屬性，做為行聯結值。 這個方法可以用來取得 linejoin 屬性的值。<br/>                |
| [**GetAttributeValue (PCWSTR、D2D1 \_ SVG \_ 單位 \_ 類型 \*)**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_svg_unit_type))                        | 取得這個元素的屬性做為單位類型值。 這個方法可以用來取得 gradientUnits 或 clipPathUnits 屬性的值。<br/>  |
| [**GetAttributeValue (PCWSTR、ID2D1SvgAttribute \* \*)**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_id2d1svgattribute))                          | 取得這個元素的屬性。<br/>                                                                                                               |
| [**GetAttributeValue (PCWSTR、D2D1 \_ SVG \_ 可見度 \*)**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_svg_visibility))                        | 取得這個元素的屬性做為可見度值。 這個方法可以用來取得可見度屬性的值。<br/>                    |
| [**GetAttributeValue (PCWSTR、ID2D1SvgStrokeDashArray \* \*)**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_id2d1svgstrokedasharray))                    | 取得這個專案的屬性，做為筆觸虛線陣列。 這個方法可以用來取得 dasharray 屬性的值。<br/>             |
| [**GetAttributeValue (PCWSTR、ID2D1SvgPointCollection \* \*)**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_id2d1svgpointcollection))                    | 取得這個元素的屬性為點。 這個方法可以用來取得多邊形或聚合線條元素上 points 屬性的值。<br/>  |
| [**GetAttributeValue (PCWSTR、D2D1 \_ SVG \_ 保留 \_ 外觀 \_ 比例 \*)**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_svg_preserve_aspect_ratio))           | 取得這個專案的屬性，做為保留外觀比例值。 這個方法可以用來取得 preserveAspectRatio 屬性的值。<br/> |
| [**GetAttributeValue (PCWSTR、D2D1 \_ SVG \_ ATTRIBUTE \_ POD \_ TYPE、void \* 、UINT32)**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_svg_attribute_pod_type_void_uint32)) | 取得這個元素的屬性做為 POD 類型。<br/>                                                                                                 |
| [**GetAttributeValue (PCWSTR、D2D1 \_ SVG \_ 屬性 \_ 字串 \_ 類型、PWSTR、UINT32)**](/windows/win32/api/d2d1svg/nf-d2d1svg-id2d1svgelement-getattributevalue(pcwstr_d2d1_color_f))  | 取得這個專案的屬性做為字串。 <br/>                                                                                                  |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ID2D1SvgElement**](/windows/win32/api/d2d1svg/nn-d2d1svg-id2d1svgelement)
</dt> </dl>

 

