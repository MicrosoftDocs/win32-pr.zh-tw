---
title: 缺少 ARIA 範圍控制項屬性
description: 缺少 ARIA 範圍控制項屬性
ms.assetid: B79F6277-5339-406A-B5FC-A3657BFC5034
keywords:
- AriaRangeControlAttributesAbsentId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f8cd32a7a4807f06c26bd013ee3fd294d33cc57
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/09/2020
ms.locfileid: "104024261"
---
# <a name="aria-range-control-attributes-missing"></a>缺少 ARIA 範圍控制項屬性

## <a name="text"></a>Text

元素具有 **progressbar** 或 **滑杆** 角色，但未公開對應的 **aria valuemin** 、 **aria valuemax** 和 **aria valuenow** 屬性。

## <a name="type"></a>類型

錯誤

## <a name="description"></a>描述

此錯誤適用于 [**角色**](https://developer.mozilla.org/docs/Web/HTML/Reference) (隱含或明確) 等於 **progressbar**、**滑杆** 或數值調整器的 **元素。**

根據 Web 協助工具計畫的可存取豐富網際網路應用程式 (WAI-ARIA) 規格，具有 **progressbar**、**滑杆****或調整** 規模角色的元素必須公開 [**ARIA valuemax**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA)、 [**aria valuemin**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA)和 [**aria valuenow**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA)屬性。

若要修正這個錯誤，請設定 [**aria valuemax**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA)、 [**aria valuemin**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA)和 [**aria valuenow**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) 屬性，並動態維護 **aria valuenow** 值，以確保會公開目前的值。 您也應該設定 [**aria valuetext**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) 屬性，以將更多意義新增至公開的 **aria valuenow** 值。

## <a name="example"></a>範例


```HTML
<div role="slider" id="sl" aria-valuemin="1" aria-valuemax="5" aria-valuenow="3" aria-valuetext="good"…>
</div>

<script>
  // This function should be triggered when the slider value changes.
  function manageValue()
  {
    ...
    sl.setAttribute("aria-valuenow", currentValue);
    sl.setAttribute("aria-valuetext", currentValueText);
    ...
  }
</script>
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[ARIA 範圍控制項屬性不相容](aria-range-control-attribute-out-of-range.md)
</dt> </dl>

 

 




