---
title: ARIA 容器角色錯誤
description: ARIA 容器角色錯誤
ms.assetid: AF207293-1172-43D0-B92C-C3070876DF54
keywords:
- AriaContainerRoleErrorId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d02554c868816c05981fa9f008c8f79f0a3eb0f8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932522"
---
# <a name="aria-container-role-error"></a>ARIA 容器角色錯誤

## <a name="text"></a>Text

已定義使用中子 **系的元素** 沒有容器角色 (**combobox**、 **方格**、 **listbox**、 **menu**、 **menubar**、 **radiogroup**、 **tree**、 **treegrid**、 **tablist**、 **row**) 。

## <a name="type"></a>類型

錯誤

## <a name="description"></a>描述

此錯誤適用于具有 **aria activedescendant** 屬性的元素。

元素似乎是已設定 **aria activedescendant** 屬性的容器，但元素的 role 屬性沒有對容器有效的值。

若要修正這個錯誤，請將 **角色** 屬性設定為 Web 協助工具方案可存取的豐富網際網路應用程式 (WAI-ARIA) 角色值對容器元素有效 **：下拉式方塊、****方格**、 **listbox**、 **menu**、 **menubar**、 **radiogroup**、 **tablist**、 **tree** 或 **treegrid**。

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

[ARIA 角色錯誤](aria-role-invalid.md)
</dt> </dl>

 

 




