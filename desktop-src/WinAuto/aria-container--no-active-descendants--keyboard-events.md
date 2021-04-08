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
# <a name="aria-container-role-without-active-descendant-keyboard-accessibility-error"></a>沒有作用中子系的 ARIA 容器角色 () 鍵盤協助工具錯誤

## <a name="text"></a>Text

專案是未定義作用中子系的可設定焦點容器，**而不是** /  / 在容器上或其中一個子項目) 的 (都沒有。

## <a name="type"></a>類型

錯誤

## <a name="description"></a>描述

此錯誤適用于具有容器角色、沒有 **aria activedescendant** 屬性且未停用的元素。 這些專案會使用稱為「 *浮動索引*」的概念，在子項目之間執行鍵盤導覽。 在此概念中，子專案的 **tabindex** 屬性會動態維護，以確保每次只有一個子專案是定位順序。

這個錯誤表示沒有 **activedescendant** 屬性且未停用的容器元素，無法供鍵盤使用者存取。 因為容器沒有必要的鍵盤事件處理常式 (**keydown**、 **keyup** 或 **keypress**) ，而且沒有任何容器的子專案，所以此問題存在。

若要修正這個錯誤，請為容器或其中一個子項目定義 **keydown**、 **keyup** 或 **keypress** 事件處理常式。

## <a name="example"></a>範例


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



## <a name="related-topics"></a>相關主題

<dl> <dt>

[ARIA 容器角色鍵盤協助工具錯誤](aria-container-keyboard-events.md)
</dt> </dl>

 

 




