---
title: DragPattern/DragDropPattern 元素需要有效的 DropEffect
description: DragPattern/DragDropPattern 元素需要有效的 DropEffect
ms.assetid: 508DD4F3-4878-4A9E-859D-06BBDA505708
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33acda19732e2ebd96182023fce9641012b50d6b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103670976"
---
# <a name="dragpatterndragdroppattern-elements-requires-valid-dropeffect"></a>DragPattern/DragDropPattern 元素需要有效的 DropEffect

## <a name="text"></a>Text

支援拖放的元素應設定有效的 ' DropEffect '

## <a name="type"></a>類型

錯誤

## <a name="description"></a>描述

元素支援 [**IUIAutomationDragPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdragpattern) 或 [**IUIAutomationDropTargetPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdroptargetpattern)，但沒有有效的 [**DropEffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect) 屬性集。

這個問題會造成依賴螢幕讀取者的人員遇到問題。 使用者將無法分辨這個物件在拖曳時的效果。

## <a name="possible-causes"></a>可能的原因

-   元素或其父系尚未建立 [**DropEffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect) ，或 [**DropEffects**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffects) 不正確指派的名稱或標籤。
-   開發人員並不知道螢幕讀取器會讀取 DropEffect (s) 。

 

 




