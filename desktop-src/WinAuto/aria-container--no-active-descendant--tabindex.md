---
title: 沒有作用中子系的 ARIA 容器角色 () Tabindex 錯誤
description: 沒有作用中子系的 ARIA 容器角色 () Tabindex 錯誤
ms.assetid: E3CCA500-7104-4163-927C-94EA8F1E89D8
keywords:
- AriaContainerWithoutActiveDescendantTabIndexErrorId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6eb2198b5ad28cf8a2dd1c625342fef399eefbe3f93ed5e09f4796e06d16338
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118994338"
---
# <a name="aria-container-role-without-active-descendant-tabindex-error"></a>沒有作用中子系的 ARIA 容器角色 () Tabindex 錯誤

## <a name="text"></a>Text

元素是未定義作用中子系的可設定焦點容器，但沒有任何子項目的 **tabindex** 大於或等於0。

## <a name="type"></a>類型

錯誤

## <a name="description"></a>描述

此錯誤適用于具有容器角色、沒有 **aria activedescendant** 屬性且未停用的元素。 這些專案會使用稱為「 *浮動索引*」的概念，在子項目之間執行鍵盤導覽。 在此概念中，子專案的 **tabindex** 屬性會動態維護，以確保每次只有一個子專案是定位順序。

若要修正這個錯誤，請將其中一個子項目的 **tabindex** 屬性設定為等於或大於0的值。

## <a name="example"></a>範例


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



## <a name="related-topics"></a>相關主題

<dl> <dt>

[ARIA 容器 Tabindex 錯誤](aria-container-tabindex.md)
</dt> </dl>

 

 




