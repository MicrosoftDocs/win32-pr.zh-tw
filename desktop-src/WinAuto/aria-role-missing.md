---
title: 具有事件處理常式之元素的 ARIA 角色錯誤
description: 具有事件處理常式之元素的 ARIA 角色錯誤
ms.assetid: 20BB874A-874B-4266-9C7B-49C07D4146DA
keywords:
- AriaContainerRoleErrorMessage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eede416392e8b4cb644938242a9975238118ff07
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/09/2020
ms.locfileid: "104383142"
---
# <a name="aria-role-error-for-elements-with-event-handlers"></a><span data-ttu-id="e5482-104">具有事件處理常式之元素的 ARIA 角色錯誤</span><span class="sxs-lookup"><span data-stu-id="e5482-104">ARIA Role Error for elements with event handlers</span></span>

## <a name="text"></a><span data-ttu-id="e5482-105">Text</span><span class="sxs-lookup"><span data-stu-id="e5482-105">Text</span></span>

<span data-ttu-id="e5482-106">元素有事件處理常式，但未定義有效的 WAI-ARIA 角色。</span><span class="sxs-lookup"><span data-stu-id="e5482-106">Element has an event handler but valid WAI-ARIA role is not defined.</span></span>

## <a name="type"></a><span data-ttu-id="e5482-107">類型</span><span class="sxs-lookup"><span data-stu-id="e5482-107">Type</span></span>

<span data-ttu-id="e5482-108">錯誤</span><span class="sxs-lookup"><span data-stu-id="e5482-108">Error</span></span>

## <a name="description"></a><span data-ttu-id="e5482-109">描述</span><span class="sxs-lookup"><span data-stu-id="e5482-109">Description</span></span>

<span data-ttu-id="e5482-110">此錯誤適用于沒有隱含 Web 協助工具可存取的豐富網際網路應用程式 (WAI-ARIA) 角色的元素。</span><span class="sxs-lookup"><span data-stu-id="e5482-110">This error applies to elements that do not have an implicit Web Accessibility Initiative - Accessible Rich Internet Applications (WAI-ARIA) role.</span></span>

<span data-ttu-id="e5482-111">此錯誤表示專案具有滑鼠或鍵盤事件處理常式 (**按一下**、 **mousedown**、 **mouseup**、 **mousemove**、 **mouseout**、 **滑鼠** 右鍵、 **keyup**、 **keydown** 或 **按鍵**) ，但未設定 [**role**](https://developer.mozilla.org/docs/Web/HTML/Reference) 屬性，而且不是具有隱含 WAI-ARIA 角色的其中一個 HTML 標籤 (例如， **a**、 **button**、 **img**、 **input**、 **select** 等) 。</span><span class="sxs-lookup"><span data-stu-id="e5482-111">This error indicates that an element has a mouse or keyboard event handler (**click**, **mousedown**, **mouseup**, **mousemove**, **mouseout**, **mouseover**, **keyup**, **keydown**, or **keypress**), but doesn’t have the [**role**](https://developer.mozilla.org/docs/Web/HTML/Reference) attribute set, and is not one of the HTML tags that has an implicit WAI-ARIA role (for example, **a**, **button**, **img**, **input**, **select** and so on).</span></span>

<span data-ttu-id="e5482-112">為沒有隱含角色 (（例如 **div** 標記) 的互動式元素設定 [**role**](https://developer.mozilla.org/docs/Web/HTML/Reference)屬性，必須將元素的行為模式公開給螢幕讀取器和其他輔助技術。</span><span class="sxs-lookup"><span data-stu-id="e5482-112">Setting the [**role**](https://developer.mozilla.org/docs/Web/HTML/Reference) attribute for interactive elements that have no implicit role (such as a **div** tag) is necessary to expose the element's behavior patterns to screen readers and other assistive technologies.</span></span>

<span data-ttu-id="e5482-113">若要修正這個錯誤，請將 [**role**](https://developer.mozilla.org/docs/Web/HTML/Reference) 屬性設為有效的 WAI-ARIA 角色，此角色最適合此元素的行為模式和必要屬性。</span><span class="sxs-lookup"><span data-stu-id="e5482-113">To fix this error, set the [**role**](https://developer.mozilla.org/docs/Web/HTML/Reference) attribute to a valid WAI-ARIA role that best fits this element's behavior patterns and required attributes.</span></span> <span data-ttu-id="e5482-114">例如，如果 **div** 標記以按鈕的形式運作，請將角色屬性設定為 "button"。</span><span class="sxs-lookup"><span data-stu-id="e5482-114">For example, if a **div** tag functions as a button, set the role attribute to "button".</span></span>

## <a name="example"></a><span data-ttu-id="e5482-115">範例</span><span class="sxs-lookup"><span data-stu-id="e5482-115">Example</span></span>


```HTML
<!-- Setting role attribute allows screen readers to know it can be clicked -->
<div role="button" tabindex="0" aria-label="Back" onclick="mouseAction(event)" onkeyup="keyAction(event)" >
```



 

 




