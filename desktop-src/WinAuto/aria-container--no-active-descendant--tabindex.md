---
title: 沒有作用中子系的 ARIA 容器角色 () Tabindex 錯誤
description: 沒有作用中子系的 ARIA 容器角色 () Tabindex 錯誤
ms.assetid: E3CCA500-7104-4163-927C-94EA8F1E89D8
keywords:
- AriaContainerWithoutActiveDescendantTabIndexErrorId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a01d3391d93b7e7f146f379bcfecd629e14bce7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183539"
---
# <a name="aria-container-role-without-active-descendant-tabindex-error"></a><span data-ttu-id="edfed-104">沒有作用中子系的 ARIA 容器角色 () Tabindex 錯誤</span><span class="sxs-lookup"><span data-stu-id="edfed-104">ARIA Container Role (without active descendant) Tabindex Error</span></span>

## <a name="text"></a><span data-ttu-id="edfed-105">Text</span><span class="sxs-lookup"><span data-stu-id="edfed-105">Text</span></span>

<span data-ttu-id="edfed-106">元素是未定義作用中子系的可設定焦點容器，但沒有任何子項目的 **tabindex** 大於或等於0。</span><span class="sxs-lookup"><span data-stu-id="edfed-106">Element is a focusable container without active descendant defined, but no child element has **tabindex** greater or equal to 0.</span></span>

## <a name="type"></a><span data-ttu-id="edfed-107">類型</span><span class="sxs-lookup"><span data-stu-id="edfed-107">Type</span></span>

<span data-ttu-id="edfed-108">錯誤</span><span class="sxs-lookup"><span data-stu-id="edfed-108">Error</span></span>

## <a name="description"></a><span data-ttu-id="edfed-109">描述</span><span class="sxs-lookup"><span data-stu-id="edfed-109">Description</span></span>

<span data-ttu-id="edfed-110">此錯誤適用于具有容器角色、沒有 **aria activedescendant** 屬性且未停用的元素。</span><span class="sxs-lookup"><span data-stu-id="edfed-110">This error applies to elements that have a container role, do not have an **aria-activedescendant** attribute, and are not disabled.</span></span> <span data-ttu-id="edfed-111">這些專案會使用稱為「 *浮動索引*」的概念，在子項目之間執行鍵盤導覽。</span><span class="sxs-lookup"><span data-stu-id="edfed-111">These elements implement keyboard navigation among child elements by using the concept known as *roving index*.</span></span> <span data-ttu-id="edfed-112">在此概念中，子專案的 **tabindex** 屬性會動態維護，以確保每次只有一個子專案是定位順序。</span><span class="sxs-lookup"><span data-stu-id="edfed-112">In this concept, the **tabindex** attributes of child elements are maintained dynamically, ensuring that at all times only one child element is in tab order.</span></span>

<span data-ttu-id="edfed-113">若要修正這個錯誤，請將其中一個子項目的 **tabindex** 屬性設定為等於或大於0的值。</span><span class="sxs-lookup"><span data-stu-id="edfed-113">To fix this error, set the **tabindex** attribute of one of the child elements to a value equal to or greater than 0.</span></span>

## <a name="example"></a><span data-ttu-id="edfed-114">範例</span><span class="sxs-lookup"><span data-stu-id="edfed-114">Example</span></span>


```HTML
<div id="listbox" role="listbox1">
  <div role="option" id="listbox1-1" tabindex="0" class="selected">Item 1</div>
  <div role="option" id="listbox1-2">Item 2</div>
  <div role="option" id="listbox1-3">Item 3</div>
</div>

<script>

  ...

  listbox1.addEventListener('keyup', function(e) {
    var itm = e.srcElement;
    var prev = itm.previousElementSibling;
    var next = itm.nextElementSibling;

    if (e.keyCode == 38 && prev) {
      // Arrow up to move focus to the previous item.
      itm.setAttribute('tabindex', '-1');
      prev.setAttribute('tabindex','0');
      prev.focus();
    } 

    else if (e.keyCode == 40 && next) {
      // Arrow down to move focus to the next item.
      itm.setAttribute('tabindex', '-1');
      next.setAttribute('tabindex','0');
      next.focus();
    }
  });

</script>
```



## <a name="related-topics"></a><span data-ttu-id="edfed-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="edfed-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="edfed-116">ARIA 容器 Tabindex 錯誤</span><span class="sxs-lookup"><span data-stu-id="edfed-116">ARIA Container Tabindex Error</span></span>](aria-container-tabindex.md)
</dt> </dl>

 

 




