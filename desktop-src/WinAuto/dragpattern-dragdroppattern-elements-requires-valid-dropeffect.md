---
title: DragPattern/DragDropPattern 元素需要有效的 DropEffect
description: DragPattern/DragDropPattern 元素需要有效的 DropEffect
ms.assetid: 508DD4F3-4878-4A9E-859D-06BBDA505708
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9cd95e1da2d3d05c7499f72c86d454da2832947cafd0150e8f62b2f3e8d56af2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118115676"
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

 

 




