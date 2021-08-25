---
title: ARIA 容器角色鍵盤協助工具錯誤
description: ARIA 容器角色鍵盤協助工具錯誤
ms.assetid: 364F26D7-7B65-418B-9DA5-F3B7B59284F7
keywords:
- AriaContainerKeyboardAccessibilityErrorId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 591098ba6e38836f1f39d13e72495bc1d7a3d5f9fe088873661e3dd3a7e65d4a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120122398"
---
# <a name="aria-container-role-keyboard-accessibility-error"></a>ARIA 容器角色鍵盤協助工具錯誤

## <a name="text"></a>Text

元素是具有使用中子系和自訂滑鼠功能的容器，但沒有對應的鍵盤功能：適用于 **OnKeyDown** 或 **OnKeyPress** 的 JavaScript 事件處理常式。

## <a name="type"></a>類型

錯誤

## <a name="description"></a>描述

此錯誤適用于具有 **aria activedescendant** 屬性的元素。 這些元素有一或多個滑鼠事件處理常式 (**mousemove**、 **mousedown** 或 **mouseup**) ，但缺少對等的鍵盤事件處理常式 (**keydown**、 **keyup** 或 **keypress**) 。 需要鍵盤事件處理常式，以確保使用者可以使用鍵盤叫用專案的功能，並確保元素會維護 **activedescendant** 屬性。

若要修正這個錯誤，請執行其中一個鍵盤事件處理常式。

## <a name="example"></a>範例


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



## <a name="related-topics"></a>相關主題

<dl> <dt>

[沒有作用中子系的 ARIA 容器角色 () 鍵盤協助工具錯誤](aria-container--no-active-descendants--keyboard-events.md)
</dt> </dl>

 

 




