---
title: 缺少 ARIA 範圍控制項屬性
description: 缺少 ARIA 範圍控制項屬性
ms.assetid: B79F6277-5339-406A-B5FC-A3657BFC5034
keywords:
- AriaRangeControlAttributesAbsentId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b44e4e5c69ea6971846ed9ef5f3a6108bb488c6effb21a6cbc75953ed1bb780e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119645117"
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

 

 




