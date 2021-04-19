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
# <a name="dragpatterndragdroppattern-elements-requires-name"></a><span data-ttu-id="8669d-103">DragPattern/DragDropPattern 元素需要名稱</span><span class="sxs-lookup"><span data-stu-id="8669d-103">DragPattern/DragDropPattern elements requires Name</span></span>

## <a name="text"></a><span data-ttu-id="8669d-104">Text</span><span class="sxs-lookup"><span data-stu-id="8669d-104">Text</span></span>

<span data-ttu-id="8669d-105">支援拖放的元素應設定有效的 ' Name '</span><span class="sxs-lookup"><span data-stu-id="8669d-105">Elements that support Drag/Drop should have a valid 'Name' set</span></span>

## <a name="type"></a><span data-ttu-id="8669d-106">類型</span><span class="sxs-lookup"><span data-stu-id="8669d-106">Type</span></span>

<span data-ttu-id="8669d-107">錯誤</span><span class="sxs-lookup"><span data-stu-id="8669d-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="8669d-108">描述</span><span class="sxs-lookup"><span data-stu-id="8669d-108">Description</span></span>

<span data-ttu-id="8669d-109">元素支援 [**IUIAutomationDragPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdragpattern) 或 [**IUIAutomationDropTargetPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdroptargetpattern)，但沒有設定有效的名稱。</span><span class="sxs-lookup"><span data-stu-id="8669d-109">The element supports either [**IUIAutomationDragPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdragpattern) or [**IUIAutomationDropTargetPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdroptargetpattern), but does not have a valid Name set.</span></span>

<span data-ttu-id="8669d-110">這個問題會造成依賴螢幕讀取者的人員遇到問題。</span><span class="sxs-lookup"><span data-stu-id="8669d-110">This issue causes problems for people who rely on a screen-reader.</span></span> <span data-ttu-id="8669d-111">使用者將無法分辨出這個物件的原因，因為讀取的畫面不會讀取有效的名稱，以區分此元素在拖曳時的意義。</span><span class="sxs-lookup"><span data-stu-id="8669d-111">The user will not be able to tell what this object is since the screen read will not read out a valid name to distinguish what this element is when dragging.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="8669d-112">可能的原因</span><span class="sxs-lookup"><span data-stu-id="8669d-112">Possible causes</span></span>

-   <span data-ttu-id="8669d-113">元素或其父系有不正確指派的名稱或標籤。</span><span class="sxs-lookup"><span data-stu-id="8669d-113">The element, or its parent, has an incorrectly assigned name or label.</span></span>
-   <span data-ttu-id="8669d-114">開發人員並不知道螢幕讀取器會讀取名稱和控制項類型。</span><span class="sxs-lookup"><span data-stu-id="8669d-114">A developer is not aware that screen readers read names and control types.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8669d-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="8669d-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8669d-116">**IAccessible：： get \_ accName**</span><span class="sxs-lookup"><span data-stu-id="8669d-116">**IAccessible::get\_accName**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)
</dt> <dt>

[<span data-ttu-id="8669d-117">Name 屬性</span><span class="sxs-lookup"><span data-stu-id="8669d-117">Name Property</span></span>](name-property.md)
</dt> <dt>

[<span data-ttu-id="8669d-118">**UIA \_ NamePropertyId**</span><span class="sxs-lookup"><span data-stu-id="8669d-118">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)
</dt> <dt>

[<span data-ttu-id="8669d-119">**IUIAutomationElement::CurrentName**</span><span class="sxs-lookup"><span data-stu-id="8669d-119">**IUIAutomationElement::CurrentName**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname)
</dt> </dl>

 

 




