---
title: ARIA 容器角色鍵盤協助工具錯誤
description: ARIA 容器角色鍵盤協助工具錯誤
ms.assetid: 364F26D7-7B65-418B-9DA5-F3B7B59284F7
keywords:
- AriaContainerKeyboardAccessibilityErrorId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 085591e4f4834e8088b5ca199918d621f518e678
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301351"
---
# <a name="aria-container-role-keyboard-accessibility-error"></a><span data-ttu-id="e44e8-104">ARIA 容器角色鍵盤協助工具錯誤</span><span class="sxs-lookup"><span data-stu-id="e44e8-104">ARIA Container Role Keyboard Accessibility Error</span></span>

## <a name="text"></a><span data-ttu-id="e44e8-105">Text</span><span class="sxs-lookup"><span data-stu-id="e44e8-105">Text</span></span>

<span data-ttu-id="e44e8-106">元素是具有使用中子系和自訂滑鼠功能的容器，但沒有對應的鍵盤功能：適用于 **OnKeyDown** 或 **OnKeyPress** 的 JavaScript 事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="e44e8-106">Element is a container with active descendant and custom mouse functionality but without the corresponding keyboard functionality: JavaScript event handlers for **OnKeyDown** or **OnKeyPress**.</span></span>

## <a name="type"></a><span data-ttu-id="e44e8-107">類型</span><span class="sxs-lookup"><span data-stu-id="e44e8-107">Type</span></span>

<span data-ttu-id="e44e8-108">錯誤</span><span class="sxs-lookup"><span data-stu-id="e44e8-108">Error</span></span>

## <a name="description"></a><span data-ttu-id="e44e8-109">描述</span><span class="sxs-lookup"><span data-stu-id="e44e8-109">Description</span></span>

<span data-ttu-id="e44e8-110">此錯誤適用于具有 **aria activedescendant** 屬性的元素。</span><span class="sxs-lookup"><span data-stu-id="e44e8-110">This error applies to elements that have the **aria-activedescendant** attribute.</span></span> <span data-ttu-id="e44e8-111">這些元素有一或多個滑鼠事件處理常式 (**mousemove**、 **mousedown** 或 **mouseup**) ，但缺少對等的鍵盤事件處理常式 (**keydown**、 **keyup** 或 **keypress**) 。</span><span class="sxs-lookup"><span data-stu-id="e44e8-111">These elements have one or more mouse event handlers (**mousemove**, **mousedown** or **mouseup**), but are missing the equivalent keyboard event handlers (**keydown**, **keyup** or **keypress**).</span></span> <span data-ttu-id="e44e8-112">需要鍵盤事件處理常式，以確保使用者可以使用鍵盤叫用專案的功能，並確保元素會維護 **activedescendant** 屬性。</span><span class="sxs-lookup"><span data-stu-id="e44e8-112">The keyboard event handlers are needed to ensure that the user can invoke the element's functionality by using the keyboard, and to ensure that the element maintains the **aria-activedescendant** attribute.</span></span>

<span data-ttu-id="e44e8-113">若要修正這個錯誤，請執行其中一個鍵盤事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="e44e8-113">To fix this error, implement one of the keyboard event handlers.</span></span>

## <a name="example"></a><span data-ttu-id="e44e8-114">範例</span><span class="sxs-lookup"><span data-stu-id="e44e8-114">Example</span></span>


```HTML
<div role="listbox" id="listbox1" tabindex="0" aria-activedescendant="listbox1-1"> 
  <div role="option" id="listbox1-1" class="selected">Item 1</div>
  <div role="option" id="listbox1-2">Item 2</div>
  <div role="option" id="listbox1-3">Item 3</div>
</div>

<script>

   ...

  listbox1.addEventListener('keyup', function(e) {
    var itm = document.getElementById(this.getAttribute('aria-activedescendant'));
    var prev = itm.previousElementSibling;
    var next = itm.nextElementSibling;
    
    if ( e.keyCode  38 && prev ) {
      // Arrow up to move active descendant to the previous item
      itm.removeAttribute('class’);
      prev.setAttribute("class", "selected");
      this.setAttribute ('aria-activedescendant', prev.id)
    } 

    else if ( e.keyCode == 40 && next) {
      // Arrow down to move focus to the next item
      itm.removeAttribute('class’);
      next.setAttribute("class", "selected");
      this.setAttribute ('aria-activedescendant', next.id)
    }
  });      

</script>
```



## <a name="related-topics"></a><span data-ttu-id="e44e8-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="e44e8-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e44e8-116">沒有作用中子系的 ARIA 容器角色 () 鍵盤協助工具錯誤</span><span class="sxs-lookup"><span data-stu-id="e44e8-116">ARIA Container Role (without active descendant) Keyboard Accessibility Error</span></span>](aria-container--no-active-descendants--keyboard-events.md)
</dt> </dl>

 

 




