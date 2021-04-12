---
title: ARIA 容器 Tabindex 錯誤
description: ARIA 容器 Tabindex 錯誤
ms.assetid: CCEA9490-903D-423D-B9FD-641E8B7D3E0B
keywords:
- AriaContainerTabIndexErrorId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b6af684b401627181aaef656215240a312393f2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372555"
---
# <a name="aria-container-tabindex-error"></a>ARIA 容器 Tabindex 錯誤

## <a name="text"></a>Text

元素是具有已定義之作用中子系的可設定焦點容器，但沒有大於或等於0的 **tabindex** 值。

## <a name="type"></a>類型

錯誤

## <a name="description"></a>描述

此錯誤適用于具有 **aria activedescendant** 屬性、未停用的元素，而且沒有將 **tabindex** 屬性設定為大於或等於0的值。 這些元素必須是定位順序，因為它們負責處理其子項目的鍵盤事件。

若要修正這個錯誤，請將 **tabindex** 屬性設定為大於或等於0的值。

## <a name="example"></a>範例


```HTML
<div role="listbox" id="listbox1" tabindex="0" aria-activedescendant="listbox1-1"> 
       <div role="option" id="listbox1-1" class="selected">Item 1</div> 
       <div role="option" id="listbox1-2">Item 2</div> 

       <div role="option" id="listbox1-3">Item 3</div>
      ... 
<div>
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[沒有作用中子系的 ARIA 容器角色 () Tabindex 錯誤](aria-container--no-active-descendant--tabindex.md)
</dt> </dl>

 

 




