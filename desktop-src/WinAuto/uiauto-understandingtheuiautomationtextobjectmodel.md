---
title: 瞭解消費者介面自動化 Text 物件模型
description: 本主題說明 Microsoft 消費者介面自動化用戶端應用程式如何存取以文字為基礎之控制項的文字內容。
ms.assetid: 8545EBA3-6995-4336-A197-27CE3A3339EE
keywords:
- 用戶端，瞭解消費者介面自動化 text 物件模型
- 用戶端，以文字為基礎的控制項
- 用戶端、文字範圍
- 用戶端、文字控制項模式
- 用戶端、TextRange 控制項模式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f6dae1fc5ca02af69ab3d5386461e6bd7a864d4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672427"
---
# <a name="understanding-the-ui-automation-text-object-model"></a><span data-ttu-id="4e513-108">瞭解消費者介面自動化 Text 物件模型</span><span class="sxs-lookup"><span data-stu-id="4e513-108">Understanding the UI Automation Text Object Model</span></span>

<span data-ttu-id="4e513-109">本主題說明 Microsoft 消費者介面自動化用戶端應用程式如何存取以文字為基礎之控制項的文字內容。</span><span class="sxs-lookup"><span data-stu-id="4e513-109">This topic describes how Microsoft UI Automation client applications access the textual content of a text-based control.</span></span>

-   [<span data-ttu-id="4e513-110">控制項特定的物件模型</span><span class="sxs-lookup"><span data-stu-id="4e513-110">Control-specific Object Model</span></span>](#control-specific-object-model)
-   [<span data-ttu-id="4e513-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="4e513-111">Related topics</span></span>](#related-topics)

<span data-ttu-id="4e513-112">以文字為基礎的控制項透過簡單的文字物件模型，將文字內容公開給消費者介面自動化用戶端應用程式。</span><span class="sxs-lookup"><span data-stu-id="4e513-112">Text-based controls expose textual content to UI Automation client applications through a simple text object model.</span></span> <span data-ttu-id="4e513-113">用戶端應用程式可以透過 [text 和 TextRange](uiauto-about-text-and-textrange-patterns.md) 控制項模式介面（包括 [**IUIAutomationTextPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextpattern) 和 [**IUIAutomationTextRange**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextrange)）來存取 text 物件模型。</span><span class="sxs-lookup"><span data-stu-id="4e513-113">Client applications have access to the text object model through the [Text and TextRange](uiauto-about-text-and-textrange-patterns.md) control pattern interfaces, including [**IUIAutomationTextPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextpattern) and [**IUIAutomationTextRange**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextrange).</span></span> <span data-ttu-id="4e513-114">用戶端應用程式可以使用這些介面，從以文字為基礎的控制項取出文字內容、文字屬性和内嵌物件，例如資料表和超連結。</span><span class="sxs-lookup"><span data-stu-id="4e513-114">Client applications can use these interfaces to retrieve textual content, text attributes, and embedded objects such as tables and hyperlinks from text-based controls.</span></span>

<span data-ttu-id="4e513-115">支援消費者介面自動化 text 物件模型的控制項類型包括 [編輯](uiauto-supporteditcontroltype.md) 和 [檔](uiauto-supportdocumentcontroltype.md) 控制項類型。</span><span class="sxs-lookup"><span data-stu-id="4e513-115">Control types that support the UI Automation text object model include the [Edit](uiauto-supporteditcontroltype.md) and [Document](uiauto-supportdocumentcontroltype.md) control types.</span></span> <span data-ttu-id="4e513-116">其他控制項類型（例如 [工具提示](uiauto-supporttooltipcontroltype.md) 和 [文字](uiauto-supporttextcontroltype.md) ）也可能支援 text 物件模型，但不一定要這樣做。</span><span class="sxs-lookup"><span data-stu-id="4e513-116">Other control types such as [ToolTip](uiauto-supporttooltipcontroltype.md) and [Text](uiauto-supporttextcontroltype.md) might also support the text object model, but they are not required to.</span></span>

> [!Note]  
> <span data-ttu-id="4e513-117">消費者介面自動化的 text 物件模型並未提供插入或修改文字的方法。</span><span class="sxs-lookup"><span data-stu-id="4e513-117">The UI Automation text object model does not provide a means to insert or modify text.</span></span> <span data-ttu-id="4e513-118">不過，某些控制項可透過 [**IUIAutomationValuePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationvaluepattern) 介面或透過直接鍵盤輸入來插入或修改文字。</span><span class="sxs-lookup"><span data-stu-id="4e513-118">However, some controls enable text to be inserted or modified either through the [**IUIAutomationValuePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationvaluepattern) interface, or through direct keyboard input.</span></span>

 

## <a name="control-specific-object-model"></a><span data-ttu-id="4e513-119">控制項特定的物件模型</span><span class="sxs-lookup"><span data-stu-id="4e513-119">Control-specific Object Model</span></span>

<span data-ttu-id="4e513-120">以文字為基礎的控制項，其本身檔物件模型 (DOM) 可以藉由執行 [system.collections.objectmodel.observablecollection](uiauto-implementingobjectmodel.md) 控制項模式來公開 DOM。</span><span class="sxs-lookup"><span data-stu-id="4e513-120">A text-based control that implements its own Document Object Model (DOM) can expose the DOM by implementing the [ObjectModel](uiauto-implementingobjectmodel.md) control pattern.</span></span> <span data-ttu-id="4e513-121">公開 DOM 可讓用戶端應用程式更能存取及控制以文字為基礎的控制項內容。</span><span class="sxs-lookup"><span data-stu-id="4e513-121">Exposing the DOM can give client applications greater access to, and control over, the content of a text-based control.</span></span>

<span data-ttu-id="4e513-122">用戶端應用程式可以藉由抓取控制項的 [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) 介面，來探索特定以文字為基礎的控制項是否會實作為 DOM。</span><span class="sxs-lookup"><span data-stu-id="4e513-122">A client application can discover whether a particular text-based control implements a DOM by retrieving the control's [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) interface.</span></span> <span data-ttu-id="4e513-123">然後，呼叫 [**IUIAutomationElement：： GetCurrentPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue) 方法，並指定 [**UIA \_ IsObjectModelPatternAvailablePropertyId**](uiauto-control-pattern-availability-propids.md) 屬性識別碼，以及如果控制項執行 DOM，則會收到 TRUE 的變異。</span><span class="sxs-lookup"><span data-stu-id="4e513-123">Then, call the [**IUIAutomationElement::GetCurrentPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue) method, specifying the [**UIA\_IsObjectModelPatternAvailablePropertyId**](uiauto-control-pattern-availability-propids.md) property identifier, and a variant that receives TRUE if the control implements a DOM.</span></span>

<span data-ttu-id="4e513-124">若要存取 DOM，請呼叫 [**IUIAutomationElement：： GetCurrentPattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern) 方法，並指定 [**UIA \_ ObjectModelPatternId**](uiauto-controlpattern-ids.md) 控制項模式識別碼，以及接收 [**IUIAutomationObjectModelPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationobjectmodelpattern) 介面的變數。</span><span class="sxs-lookup"><span data-stu-id="4e513-124">To access the DOM, call the [**IUIAutomationElement::GetCurrentPattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern) method, specifying the [**UIA\_ObjectModelPatternId**](uiauto-controlpattern-ids.md) control pattern identifier and a variable that receives the [**IUIAutomationObjectModelPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationobjectmodelpattern) interface.</span></span> <span data-ttu-id="4e513-125">呼叫 [**IUIAutomationObjectModelPattern：： GetUnderlyingObjectModel**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationobjectmodelpattern-getunderlyingobjectmodel) 方法以取出 DOM 介面。</span><span class="sxs-lookup"><span data-stu-id="4e513-125">Call the [**IUIAutomationObjectModelPattern::GetUnderlyingObjectModel**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationobjectmodelpattern-getunderlyingobjectmodel) method to retrieve the DOM interface.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4e513-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="4e513-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4e513-127">Text 和 TextRange 控制項模式</span><span class="sxs-lookup"><span data-stu-id="4e513-127">Text and TextRange Control Patterns</span></span>](uiauto-implementingtextandtextrange.md)
</dt> <dt>

[<span data-ttu-id="4e513-128">消費者介面自動化文字內容的支援</span><span class="sxs-lookup"><span data-stu-id="4e513-128">UI Automation Support for Textual Content</span></span>](uiauto-ui-automation-textpattern-overview.md)
</dt> <dt>

[<span data-ttu-id="4e513-129">使用以文字為基礎的控制項</span><span class="sxs-lookup"><span data-stu-id="4e513-129">Working with Text-based Controls</span></span>](uiauto-workingwithtextbasedcontrols.md)
</dt> </dl>

 

 




