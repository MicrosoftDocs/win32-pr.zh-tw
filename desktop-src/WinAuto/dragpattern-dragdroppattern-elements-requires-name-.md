---
title: DragPattern/DragDropPattern 元素需要名稱
description: DragPattern/DragDropPattern 元素需要名稱
ms.assetid: DEF58FB2-5830-4162-87D0-40DEC1237529
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ecc60eeca59f4754f9c160696cdfa2556c36a5e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106980259"
---
# <a name="dragpatterndragdroppattern-elements-requires-name"></a>DragPattern/DragDropPattern 元素需要名稱

## <a name="text"></a>Text

支援拖放的元素應設定有效的 ' Name '

## <a name="type"></a>類型

錯誤

## <a name="description"></a>描述

元素支援 [**IUIAutomationDragPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdragpattern) 或 [**IUIAutomationDropTargetPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdroptargetpattern)，但沒有設定有效的名稱。

這個問題會造成依賴螢幕讀取者的人員遇到問題。 使用者將無法分辨出這個物件的原因，因為讀取的畫面不會讀取有效的名稱，以區分此元素在拖曳時的意義。

## <a name="possible-causes"></a>可能的原因

-   元素或其父系有不正確指派的名稱或標籤。
-   開發人員並不知道螢幕讀取器會讀取名稱和控制項類型。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IAccessible：： get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)
</dt> <dt>

[Name 屬性](name-property.md)
</dt> <dt>

[**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)
</dt> <dt>

[**IUIAutomationElement::CurrentName**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname)
</dt> </dl>

 

 




