---
title: ARIA 容器角色錯誤
description: ARIA 容器角色錯誤
ms.assetid: AF207293-1172-43D0-B92C-C3070876DF54
keywords:
- AriaContainerRoleErrorId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 507f094a5f7270565de0426b50afd6aef699607d857ef1ba7ed3d6c8bb1a1a2c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119759828"
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

 

 




