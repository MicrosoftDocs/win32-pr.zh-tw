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
# <a name="aria-range-control-attributes-missing"></a><span data-ttu-id="04939-104">缺少 ARIA 範圍控制項屬性</span><span class="sxs-lookup"><span data-stu-id="04939-104">ARIA Range Control Attributes Missing</span></span>

## <a name="text"></a><span data-ttu-id="04939-105">Text</span><span class="sxs-lookup"><span data-stu-id="04939-105">Text</span></span>

<span data-ttu-id="04939-106">元素具有 **progressbar** 或 **滑杆** 角色，但未公開對應的 **aria valuemin** 、 **aria valuemax** 和 **aria valuenow** 屬性。</span><span class="sxs-lookup"><span data-stu-id="04939-106">Element has **progressbar** or **slider** role but is not exposing corresponding **aria-valuemin** , **aria-valuemax** , and **aria-valuenow** attributes.</span></span>

## <a name="type"></a><span data-ttu-id="04939-107">類型</span><span class="sxs-lookup"><span data-stu-id="04939-107">Type</span></span>

<span data-ttu-id="04939-108">錯誤</span><span class="sxs-lookup"><span data-stu-id="04939-108">Error</span></span>

## <a name="description"></a><span data-ttu-id="04939-109">描述</span><span class="sxs-lookup"><span data-stu-id="04939-109">Description</span></span>

<span data-ttu-id="04939-110">此錯誤適用于 [**角色**](https://developer.mozilla.org/docs/Web/HTML/Reference) (隱含或明確) 等於 **progressbar**、**滑杆** 或數值調整器的 **元素。**</span><span class="sxs-lookup"><span data-stu-id="04939-110">This error applies to elements that have a [**role**](https://developer.mozilla.org/docs/Web/HTML/Reference) (implicit or explicit) that is equal to **progressbar**, **slider**, or **spinbutton**.</span></span>

<span data-ttu-id="04939-111">根據 Web 協助工具計畫的可存取豐富網際網路應用程式 (WAI-ARIA) 規格，具有 **progressbar**、**滑杆\*\*\*\*或調整** 規模角色的元素必須公開 [**ARIA valuemax**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA)、 [**aria valuemin**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA)和 [**aria valuenow**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA)屬性。</span><span class="sxs-lookup"><span data-stu-id="04939-111">According to the Web Accessibility Initiative - Accessible Rich Internet Applications (WAI-ARIA) specification, elements that have the **progressbar**, **slider**, or **spinbutton** role must expose the [**aria-valuemax**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA), [**aria-valuemin**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA), and [**aria-valuenow**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) attributes.</span></span>

<span data-ttu-id="04939-112">若要修正這個錯誤，請設定 [**aria valuemax**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA)、 [**aria valuemin**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA)和 [**aria valuenow**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) 屬性，並動態維護 **aria valuenow** 值，以確保會公開目前的值。</span><span class="sxs-lookup"><span data-stu-id="04939-112">To fix this error, set the [**aria-valuemax**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA), [**aria-valuemin**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA), and [**aria-valuenow**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) attributes, and dynamically maintain the **aria-valuenow** value to ensure that the current value is exposed.</span></span> <span data-ttu-id="04939-113">您也應該設定 [**aria valuetext**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) 屬性，以將更多意義新增至公開的 **aria valuenow** 值。</span><span class="sxs-lookup"><span data-stu-id="04939-113">You should also set the [**aria-valuetext**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) attribute to add more meaning to the exposed **aria-valuenow** value.</span></span>

## <a name="example"></a><span data-ttu-id="04939-114">範例</span><span class="sxs-lookup"><span data-stu-id="04939-114">Example</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="04939-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="04939-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="04939-116">ARIA 範圍控制項屬性不相容</span><span class="sxs-lookup"><span data-stu-id="04939-116">ARIA Range Control Attributes Incompatible</span></span>](aria-range-control-attribute-out-of-range.md)
</dt> </dl>

 

 




