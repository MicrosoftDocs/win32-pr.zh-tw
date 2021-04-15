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
# <a name="aria-role-error-for-elements-with-event-handlers"></a>具有事件處理常式之元素的 ARIA 角色錯誤

## <a name="text"></a>Text

元素有事件處理常式，但未定義有效的 WAI-ARIA 角色。

## <a name="type"></a>類型

錯誤

## <a name="description"></a>描述

此錯誤適用于沒有隱含 Web 協助工具可存取的豐富網際網路應用程式 (WAI-ARIA) 角色的元素。

此錯誤表示專案具有滑鼠或鍵盤事件處理常式 (**按一下**、 **mousedown**、 **mouseup**、 **mousemove**、 **mouseout**、 **滑鼠** 右鍵、 **keyup**、 **keydown** 或 **按鍵**) ，但未設定 [**role**](https://developer.mozilla.org/docs/Web/HTML/Reference) 屬性，而且不是具有隱含 WAI-ARIA 角色的其中一個 HTML 標籤 (例如， **a**、 **button**、 **img**、 **input**、 **select** 等) 。

為沒有隱含角色 (（例如 **div** 標記) 的互動式元素設定 [**role**](https://developer.mozilla.org/docs/Web/HTML/Reference)屬性，必須將元素的行為模式公開給螢幕讀取器和其他輔助技術。

若要修正這個錯誤，請將 [**role**](https://developer.mozilla.org/docs/Web/HTML/Reference) 屬性設為有效的 WAI-ARIA 角色，此角色最適合此元素的行為模式和必要屬性。 例如，如果 **div** 標記以按鈕的形式運作，請將角色屬性設定為 "button"。

## <a name="example"></a>範例


```HTML
<!-- Setting role attribute allows screen readers to know it can be clicked -->
<div role="button" tabindex="0" aria-label="Back" onclick="mouseAction(event)" onkeyup="keyAction(event)" >
```



 

 




