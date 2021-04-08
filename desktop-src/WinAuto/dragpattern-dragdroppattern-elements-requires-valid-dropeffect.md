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
# <a name="dragpatterndragdroppattern-elements-requires-valid-dropeffect"></a><span data-ttu-id="a1da7-103">DragPattern/DragDropPattern 元素需要有效的 DropEffect</span><span class="sxs-lookup"><span data-stu-id="a1da7-103">DragPattern/DragDropPattern elements requires valid DropEffect</span></span>

## <a name="text"></a><span data-ttu-id="a1da7-104">Text</span><span class="sxs-lookup"><span data-stu-id="a1da7-104">Text</span></span>

<span data-ttu-id="a1da7-105">支援拖放的元素應設定有效的 ' DropEffect '</span><span class="sxs-lookup"><span data-stu-id="a1da7-105">Elements that support Drag/Drop should have a valid 'DropEffect' set</span></span>

## <a name="type"></a><span data-ttu-id="a1da7-106">類型</span><span class="sxs-lookup"><span data-stu-id="a1da7-106">Type</span></span>

<span data-ttu-id="a1da7-107">錯誤</span><span class="sxs-lookup"><span data-stu-id="a1da7-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="a1da7-108">描述</span><span class="sxs-lookup"><span data-stu-id="a1da7-108">Description</span></span>

<span data-ttu-id="a1da7-109">元素支援 [**IUIAutomationDragPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdragpattern) 或 [**IUIAutomationDropTargetPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdroptargetpattern)，但沒有有效的 [**DropEffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect) 屬性集。</span><span class="sxs-lookup"><span data-stu-id="a1da7-109">The element supports either [**IUIAutomationDragPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdragpattern) or [**IUIAutomationDropTargetPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdroptargetpattern), but does not have a valid [**DropEffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect) property set.</span></span>

<span data-ttu-id="a1da7-110">這個問題會造成依賴螢幕讀取者的人員遇到問題。</span><span class="sxs-lookup"><span data-stu-id="a1da7-110">This issue causes problems for people who rely on a screen-reader.</span></span> <span data-ttu-id="a1da7-111">使用者將無法分辨這個物件在拖曳時的效果。</span><span class="sxs-lookup"><span data-stu-id="a1da7-111">The user will not be able to tell what effect this object has when dragging.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="a1da7-112">可能的原因</span><span class="sxs-lookup"><span data-stu-id="a1da7-112">Possible causes</span></span>

-   <span data-ttu-id="a1da7-113">元素或其父系尚未建立 [**DropEffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect) ，或 [**DropEffects**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffects) 不正確指派的名稱或標籤。</span><span class="sxs-lookup"><span data-stu-id="a1da7-113">The element, or its parent, has not created the [**DropEffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect) or [**DropEffects**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffects) an incorrectly assigned name or label.</span></span>
-   <span data-ttu-id="a1da7-114">開發人員並不知道螢幕讀取器會讀取 DropEffect (s) 。</span><span class="sxs-lookup"><span data-stu-id="a1da7-114">A developer is not aware that screen readers read DropEffect(s).</span></span>

 

 




