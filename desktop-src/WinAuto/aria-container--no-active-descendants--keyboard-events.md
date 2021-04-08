---
title: 沒有作用中子系的 ARIA 容器角色 () 鍵盤協助工具錯誤
description: 沒有作用中子系的 ARIA 容器角色 () 鍵盤協助工具錯誤
ms.assetid: 15EDD3CC-FC2A-42FC-95DD-B04D9AF3515E
keywords:
- AriaContainerWithoutActiveDescendantKeyboardAccessiblityId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d9e30e0194f156426e2b61aa774ac1f3e0f5b91
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840003"
---
# <a name="aria-container-role-without-active-descendant-keyboard-accessibility-error"></a><span data-ttu-id="f3837-104">沒有作用中子系的 ARIA 容器角色 () 鍵盤協助工具錯誤</span><span class="sxs-lookup"><span data-stu-id="f3837-104">ARIA Container Role (without active descendant) Keyboard Accessibility Error</span></span>

## <a name="text"></a><span data-ttu-id="f3837-105">Text</span><span class="sxs-lookup"><span data-stu-id="f3837-105">Text</span></span>

<span data-ttu-id="f3837-106">專案是未定義作用中子系的可設定焦點容器，**而不是** /  / 在容器上或其中一個子項目) 的 (都沒有。</span><span class="sxs-lookup"><span data-stu-id="f3837-106">Element is a focusable container without active descendant defined and without **OnKeyDown**/**OnKeyPress**/**OnKeyUp** event handlers (neither on container nor on one of child elements).</span></span>

## <a name="type"></a><span data-ttu-id="f3837-107">類型</span><span class="sxs-lookup"><span data-stu-id="f3837-107">Type</span></span>

<span data-ttu-id="f3837-108">錯誤</span><span class="sxs-lookup"><span data-stu-id="f3837-108">Error</span></span>

## <a name="description"></a><span data-ttu-id="f3837-109">描述</span><span class="sxs-lookup"><span data-stu-id="f3837-109">Description</span></span>

<span data-ttu-id="f3837-110">此錯誤適用于具有容器角色、沒有 **aria activedescendant** 屬性且未停用的元素。</span><span class="sxs-lookup"><span data-stu-id="f3837-110">This error applies to elements that have a container role, do not have an **aria-activedescendant** attribute, and are not disabled.</span></span> <span data-ttu-id="f3837-111">這些專案會使用稱為「 *浮動索引*」的概念，在子項目之間執行鍵盤導覽。</span><span class="sxs-lookup"><span data-stu-id="f3837-111">These elements implement keyboard navigation among child elements by using the concept known as *roving index*.</span></span> <span data-ttu-id="f3837-112">在此概念中，子專案的 **tabindex** 屬性會動態維護，以確保每次只有一個子專案是定位順序。</span><span class="sxs-lookup"><span data-stu-id="f3837-112">In this concept, the **tabindex** attributes of child elements are maintained dynamically, ensuring that at all times only one child element is in tab order.</span></span>

<span data-ttu-id="f3837-113">這個錯誤表示沒有 **activedescendant** 屬性且未停用的容器元素，無法供鍵盤使用者存取。</span><span class="sxs-lookup"><span data-stu-id="f3837-113">This error indicates that a container element that does not have the **aria-activedescendant** attribute, and that is not disabled, is not accessible to keyboard users.</span></span> <span data-ttu-id="f3837-114">因為容器沒有必要的鍵盤事件處理常式 (**keydown**、 **keyup** 或 **keypress**) ，而且沒有任何容器的子專案，所以此問題存在。</span><span class="sxs-lookup"><span data-stu-id="f3837-114">The problem exists because the container does not have the needed keyboard event handlers (**keydown**, **keyup**, or **keypress**), and neither do any of the container's child elements.</span></span>

<span data-ttu-id="f3837-115">若要修正這個錯誤，請為容器或其中一個子項目定義 **keydown**、 **keyup** 或 **keypress** 事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="f3837-115">To fix this error, define a **keydown**, **keyup**, or **keypress** event handler for the container or one of its child elements.</span></span>

## <a name="example"></a><span data-ttu-id="f3837-116">範例</span><span class="sxs-lookup"><span data-stu-id="f3837-116">Example</span></span>


```HTML
<div role="listbox" id="listbox1" >
  <div role="option" id="listbox1-1" tabindex="0" class="selected">Item 1</div>
  <div role="option" id="listbox1-2">Item 2</div>
  <div role="option" id="listbox1-3">Item 3</div>
  ...
<div>

<script>

  ...

  listbox1.addEventListener('keyup', function(e) {
    var itm = e.srcElement;
    var prev = itm.previousElementSibling;
    var next = itm.nextElementSibling;

    if (e.keyCode == 38 && prev) {
      // On arrow up move focus to the previous item.
      itm.setAttribute('tabindex', '-1');
      prev.setAttribute('tabindex','0');
      prev.focus();
    }

    else if (e.keyCode == 40 && next) {
      // On arrow down move focus to the next item.
      itm.setAttribute('tabindex', '-1');
      next.setAttribute('tabindex','0');
      next.focus();
    }
  });

</script>
```



## <a name="related-topics"></a><span data-ttu-id="f3837-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="f3837-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f3837-118">ARIA 容器角色鍵盤協助工具錯誤</span><span class="sxs-lookup"><span data-stu-id="f3837-118">ARIA Container Role Keyboard Accessibility Error</span></span>](aria-container-keyboard-events.md)
</dt> </dl>

 

 




