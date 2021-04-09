---
title: ARIA Tabindex 錯誤
description: ARIA Tabindex 錯誤
ms.assetid: CCBC56E8-8899-4962-8315-762538CA666C
keywords:
- AriaTabIndexErrorId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acfec56fe1f9f6074579a8b84bccc9dfdef2e1da
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/09/2020
ms.locfileid: "104024265"
---
# <a name="aria-tabindex-error"></a><span data-ttu-id="7bd80-104">ARIA Tabindex 錯誤</span><span class="sxs-lookup"><span data-stu-id="7bd80-104">ARIA Tabindex Error</span></span>

## <a name="text"></a><span data-ttu-id="7bd80-105">Text</span><span class="sxs-lookup"><span data-stu-id="7bd80-105">Text</span></span>

<span data-ttu-id="7bd80-106">元素不是停用的，而且具有 **click** 事件處理常式，但它的 **tabIndex** < 為0，預設不在定位順序中。</span><span class="sxs-lookup"><span data-stu-id="7bd80-106">Element is not disabled and has a **click** event handler but it has **tabIndex** < 0 and is not in the tab order by default.</span></span>

## <a name="type"></a><span data-ttu-id="7bd80-107">類型</span><span class="sxs-lookup"><span data-stu-id="7bd80-107">Type</span></span>

<span data-ttu-id="7bd80-108">錯誤</span><span class="sxs-lookup"><span data-stu-id="7bd80-108">Error</span></span>

## <a name="description"></a><span data-ttu-id="7bd80-109">描述</span><span class="sxs-lookup"><span data-stu-id="7bd80-109">Description</span></span>

<span data-ttu-id="7bd80-110">此錯誤適用于具有 click 事件處理常式且未停用的元素。</span><span class="sxs-lookup"><span data-stu-id="7bd80-110">This error applies to elements that have a click event handler and are not disabled.</span></span> <span data-ttu-id="7bd80-111">這些元素必須在定位順序中。</span><span class="sxs-lookup"><span data-stu-id="7bd80-111">These elements must be in the tab order.</span></span> <span data-ttu-id="7bd80-112">這可確保可以使用 Tab 鍵來觸達元素，這就是螢幕瀏覽器使用者通常流覽 UI 的方式。</span><span class="sxs-lookup"><span data-stu-id="7bd80-112">This ensures that an element can be reached using the Tab key, which is how screen reader users typically navigate the UI.</span></span>

<span data-ttu-id="7bd80-113">若要修正這個錯誤，請將 [**tabindex**](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/tabindex) 屬性設定為等於或大於0的值。</span><span class="sxs-lookup"><span data-stu-id="7bd80-113">To fix this error, set the [**tabindex**](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/tabindex) attribute to a value that is equal to or greater than 0.</span></span> <span data-ttu-id="7bd80-114">根據預設，您不需要針對位於定位順序中的標記明確地設定 **tabindex** 屬性，例如具有 href 屬性 [**的 (（**](https://developer.mozilla.org/docs/Web/HTML/Element/a)例如具有 [**href**](https://developer.mozilla.org/docs/Web/HTML/Attributes)屬性的）) 、[**按鈕**](https://developer.mozilla.org/docs/Web/HTML/Element/button)、[**輸入**](https://developer.mozilla.org/docs/Web/HTML/Element/input) (不包括「隱藏」 ) 、[**選取**](https://developer.mozilla.org/docs/Web/HTML/Element/select)、文字區 [**和**](https://developer.mozilla.org/docs/Web/HTML/Element/textarea)[**區域**](https://developer.mozilla.org/docs/Web/HTML/Element/area) (作為影像地圖) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="7bd80-114">You do not need to explicitly set the **tabindex** attribute for tags that are in the tab order by default, such as [**a**](https://developer.mozilla.org/docs/Web/HTML/Element/a) (with [**href**](https://developer.mozilla.org/docs/Web/HTML/Attributes) attribute), [**button**](https://developer.mozilla.org/docs/Web/HTML/Element/button), [**input**](https://developer.mozilla.org/docs/Web/HTML/Element/input) (excluding "hidden"), [**select**](https://developer.mozilla.org/docs/Web/HTML/Element/select), [**textarea**](https://developer.mozilla.org/docs/Web/HTML/Element/textarea), and [**area**](https://developer.mozilla.org/docs/Web/HTML/Element/area) (as part of the image map).</span></span>

## <a name="example"></a><span data-ttu-id="7bd80-115">範例</span><span class="sxs-lookup"><span data-stu-id="7bd80-115">Example</span></span>


```HTML
<div role="button" tabindex="0" aria-label="Back" onclick="mouseAction(event)" onkeyup="keyAction(event)" >
```



 

 




