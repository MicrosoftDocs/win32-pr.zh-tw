---
title: 說明按鈕
description: '[說明] 按鈕是一種控制項，可讓使用者按一下以顯示應用程式說明系統。'
ms.assetid: 5f08a8b2-bc83-4256-bcc4-aecfbd07ea51
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7afc44c9f9a03561f1627067849272509838d7a5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933257"
---
# <a name="help-button"></a><span data-ttu-id="880d1-103">說明按鈕</span><span class="sxs-lookup"><span data-stu-id="880d1-103">Help Button</span></span>

<span data-ttu-id="880d1-104">[說明] 按鈕是一種控制項，可讓使用者按一下以顯示應用程式說明系統。</span><span class="sxs-lookup"><span data-stu-id="880d1-104">The Help Button is a control that the user can click to display the application help system.</span></span>

-   [<span data-ttu-id="880d1-105">詳細資料</span><span class="sxs-lookup"><span data-stu-id="880d1-105">Details</span></span>](#details)
-   [<span data-ttu-id="880d1-106">說明按鈕屬性</span><span class="sxs-lookup"><span data-stu-id="880d1-106">Help Button Properties</span></span>](#help-button-properties)
-   [<span data-ttu-id="880d1-107">相關主題</span><span class="sxs-lookup"><span data-stu-id="880d1-107">Related topics</span></span>](#related-topics)

## <a name="details"></a><span data-ttu-id="880d1-108">詳細資料</span><span class="sxs-lookup"><span data-stu-id="880d1-108">Details</span></span>

<span data-ttu-id="880d1-109">下列螢幕擷取畫面說明功能區的 [說明] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="880d1-109">The following screen shot illustrates the Ribbon Help Button.</span></span>

![顯示 [說明] 按鈕的螢幕擷取畫面。](images/controls/helpbutton.png)

## <a name="help-button-properties"></a><span data-ttu-id="880d1-111">說明按鈕屬性</span><span class="sxs-lookup"><span data-stu-id="880d1-111">Help Button Properties</span></span>

<span data-ttu-id="880d1-112">功能區架構會針對 [說明] 按鈕控制項定義 [屬性索引鍵](windowsribbon-reference-properties.md) 的集合。</span><span class="sxs-lookup"><span data-stu-id="880d1-112">The Ribbon framework defines a collection of [property keys](windowsribbon-reference-properties.md) for the Help Button control.</span></span>

<span data-ttu-id="880d1-113">一般來說，功能區 UI 中的 [說明] 按鈕屬性會透過呼叫 [**IUIFramework：： InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) 方法，使與控制項相關聯的命令失效。</span><span class="sxs-lookup"><span data-stu-id="880d1-113">Typically, a Help Button property is updated in the ribbon UI by invalidating the Command associated with the control through a call to the [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) method.</span></span> <span data-ttu-id="880d1-114">[**IUICommandHandler：： UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty)回呼方法會處理失效事件，並定義屬性更新。</span><span class="sxs-lookup"><span data-stu-id="880d1-114">The invalidation event is handled, and the property updates defined, by the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method.</span></span>

<span data-ttu-id="880d1-115">[**IUICommandHandler：： UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty)回呼方法未執行，而且應用程式會查詢已更新的屬性值，直到架構需要該屬性為止。</span><span class="sxs-lookup"><span data-stu-id="880d1-115">The [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method is not executed, and the application queried for an updated property value, until the property is required by the framework.</span></span> <span data-ttu-id="880d1-116">例如，啟用索引標籤時，以及在功能區 UI 中顯示控制項，或顯示工具提示時。</span><span class="sxs-lookup"><span data-stu-id="880d1-116">For example, when a tab is activated and a control revealed in the ribbon UI, or when a tooltip is displayed.</span></span>

> [!Note]  
> <span data-ttu-id="880d1-117">在某些情況下，可以透過 [**IUIFramework：： GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) 方法抓取屬性，並使用 [**IUIFramework：： SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) 方法進行設定。</span><span class="sxs-lookup"><span data-stu-id="880d1-117">In some cases, a property can be retrieved through the [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) method and set with the [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) method.</span></span>

 

<span data-ttu-id="880d1-118">下表列出與 [說明] 按鈕控制項相關聯的屬性索引鍵。</span><span class="sxs-lookup"><span data-stu-id="880d1-118">The following table lists the property keys that are associated with the Help Button control.</span></span>



| <span data-ttu-id="880d1-119">屬性索引鍵</span><span class="sxs-lookup"><span data-stu-id="880d1-119">Property Key</span></span>                                                                                     | <span data-ttu-id="880d1-120">備註</span><span class="sxs-lookup"><span data-stu-id="880d1-120">Notes</span></span>                                     |
|--------------------------------------------------------------------------------------------------|-------------------------------------------|
| [<span data-ttu-id="880d1-121">UI \_ PKEY \_ 按鍵提示</span><span class="sxs-lookup"><span data-stu-id="880d1-121">UI\_PKEY\_Keytip</span></span>](windowsribbon-reference-properties-uipkey-keytip.md)                         | <span data-ttu-id="880d1-122">只能透過失效進行更新。</span><span class="sxs-lookup"><span data-stu-id="880d1-122">Can only be updated through invalidation.</span></span> |
| [<span data-ttu-id="880d1-123">UI \_ PKEY \_ 標籤</span><span class="sxs-lookup"><span data-stu-id="880d1-123">UI\_PKEY\_Label</span></span>](windowsribbon-reference-properties-uipkey-label.md)                           | <span data-ttu-id="880d1-124">只能透過失效進行更新。</span><span class="sxs-lookup"><span data-stu-id="880d1-124">Can only be updated through invalidation.</span></span> |
| [<span data-ttu-id="880d1-125">UI \_ PKEY \_ TooltipDescription</span><span class="sxs-lookup"><span data-stu-id="880d1-125">UI\_PKEY\_TooltipDescription</span></span>](windowsribbon-reference-properties-uipkey-tooltipdescription.md) | <span data-ttu-id="880d1-126">只能透過失效進行更新。</span><span class="sxs-lookup"><span data-stu-id="880d1-126">Can only be updated through invalidation.</span></span> |
| [<span data-ttu-id="880d1-127">UI \_ PKEY \_ TooltipTitle</span><span class="sxs-lookup"><span data-stu-id="880d1-127">UI\_PKEY\_TooltipTitle</span></span>](windowsribbon-reference-properties-uipkey-tooltiptitle.md)             | <span data-ttu-id="880d1-128">只能透過失效進行更新。</span><span class="sxs-lookup"><span data-stu-id="880d1-128">Can only be updated through invalidation.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="880d1-129">相關主題</span><span class="sxs-lookup"><span data-stu-id="880d1-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="880d1-130">Windows 功能區架構控制項程式庫</span><span class="sxs-lookup"><span data-stu-id="880d1-130">Windows Ribbon Framework Control Library</span></span>](windowsribbon-controls-entry.md)
</dt> <dt>

[<span data-ttu-id="880d1-131">**HelpButton 元素**</span><span class="sxs-lookup"><span data-stu-id="880d1-131">**HelpButton element**</span></span>](windowsribbon-element-helpbutton.md)
</dt> </dl>

 

 