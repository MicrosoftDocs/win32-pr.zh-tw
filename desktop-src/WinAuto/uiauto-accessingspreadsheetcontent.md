---
title: 存取試算表內容
description: 本主題說明 Microsoft 消費者介面自動化用戶端應用程式可以如何存取試算表的內容。
ms.assetid: F32EFA46-222B-4A4E-9938-10DE0F6A2CA7
keywords:
- 用戶端，存取試算表內容
- 用戶端，以文字為基礎的控制項
- 用戶端，試算表控制項模式
- 用戶端，SpreadsheetItem 控制項模式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31495086614f34aeff378a8565200fa03f2dad62
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316231"
---
# <a name="accessing-spreadsheet-content"></a><span data-ttu-id="4d259-107">存取試算表內容</span><span class="sxs-lookup"><span data-stu-id="4d259-107">Accessing Spreadsheet Content</span></span>

<span data-ttu-id="4d259-108">包含試算表內容的文字型控制項可以藉由支援 [試算表](uiauto-implementingspreadsheet.md) 和 [SpreadsheetItem](uiauto-implementingspreadsheetitem.md) 控制項模式，讓用戶端存取內容。</span><span class="sxs-lookup"><span data-stu-id="4d259-108">A text-based control that contains spreadsheet content can enable clients to access the content by supporting the [Spreadsheet](uiauto-implementingspreadsheet.md) and [SpreadsheetItem](uiauto-implementingspreadsheetitem.md) control patterns.</span></span> <span data-ttu-id="4d259-109">本主題說明 Microsoft 消費者介面自動化用戶端應用程式可以如何存取試算表的內容。</span><span class="sxs-lookup"><span data-stu-id="4d259-109">This topic describes how Microsoft UI Automation client applications can access the content of a spreadsheet.</span></span>

<span data-ttu-id="4d259-110">若要判斷以文字為基礎的控制項是否支援 [試算表](uiauto-implementingspreadsheet.md) 和 [SpreadsheetItem](uiauto-implementingspreadsheetitem.md) 控制項模式，請先取出控制項的 [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) 介面 (請參閱 [取得消費者介面自動化](uiauto-obtainingelements.md)專案。 ) 接下來，請呼叫 [**IUIAutomationElement：： GetCurrentPattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern) 方法，指定 [**UIA \_ SpreadsheetPatternId**](uiauto-controlpattern-ids.md) 或 [**UIA \_ SpreadsheetItemPatternId**](uiauto-controlpattern-ids.md)的控制項模式識別碼，以及如果控制項支援特定控制項模式，則為 TRUE 的變異。</span><span class="sxs-lookup"><span data-stu-id="4d259-110">To determine whether a text-based control supports the [Spreadsheet](uiauto-implementingspreadsheet.md) and [SpreadsheetItem](uiauto-implementingspreadsheetitem.md) control patterns, first retrieve the [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) interface for the control (see [Obtaining UI Automation Elements](uiauto-obtainingelements.md).) Next, call the [**IUIAutomationElement::GetCurrentPattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern) method, specifying a control pattern identifier of [**UIA\_SpreadsheetPatternId**](uiauto-controlpattern-ids.md) or [**UIA\_SpreadsheetItemPatternId**](uiauto-controlpattern-ids.md), and a variant that receives TRUE if the control supports the particular control pattern.</span></span>

<span data-ttu-id="4d259-111">若要存取試算表內容，請藉由呼叫 [**IUIAutomationElement：： GetCurrentPattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern)方法並指定 [**UIA \_ SpreadsheetPatternId**](uiauto-controlpattern-ids.md)作為控制項模式識別碼，來取出 [**IUIAutomationSpreadsheetPattern**](/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationspreadsheetpattern)介面。</span><span class="sxs-lookup"><span data-stu-id="4d259-111">To access the spreadsheet content, retrieve the [**IUIAutomationSpreadsheetPattern**](/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationspreadsheetpattern) interface by calling [**IUIAutomationElement::GetCurrentPattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern) method and specifying [**UIA\_SpreadsheetPatternId**](uiauto-controlpattern-ids.md) as the control pattern identifier.</span></span> <span data-ttu-id="4d259-112">接下來，使用 [**IUIAutomationSpreadsheetPattern：： GetItemByName**](/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationspreadsheetpattern-getitembyname) 方法來取得特定試算表專案的 [**IUIAutomationSpreadsheetItem**](/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationspreadsheetitempattern) 介面 (通常是資料格) 。</span><span class="sxs-lookup"><span data-stu-id="4d259-112">Next, use the [**IUIAutomationSpreadsheetPattern::GetItemByName**](/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationspreadsheetpattern-getitembyname) method to get the [**IUIAutomationSpreadsheetItem**](/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationspreadsheetitempattern) interface for a particular spreadsheet item (typically a cell).</span></span> <span data-ttu-id="4d259-113">您可以使用 **IUIAutomationSpreadsheetItem** 介面的屬性和方法來取得資料格的公式，以及與資料格相關聯的任何批註。</span><span class="sxs-lookup"><span data-stu-id="4d259-113">Use the properties and methods of the **IUIAutomationSpreadsheetItem** interface to retrieve the formula for the cell, and any annotations associated with the cell.</span></span> <span data-ttu-id="4d259-114">如需有關批註的詳細資訊，請參閱抓取 [批註。](uiauto-usingtextrangeobjects.md)</span><span class="sxs-lookup"><span data-stu-id="4d259-114">For more information about annotations, see [Retrieving Annotations.](uiauto-usingtextrangeobjects.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="4d259-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="4d259-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4d259-116">消費者介面自動化文字內容的支援</span><span class="sxs-lookup"><span data-stu-id="4d259-116">UI Automation Support for Textual Content</span></span>](uiauto-ui-automation-textpattern-overview.md)
</dt> <dt>

[<span data-ttu-id="4d259-117">使用以文字為基礎的控制項</span><span class="sxs-lookup"><span data-stu-id="4d259-117">Working with Text-based Controls</span></span>](uiauto-workingwithtextbasedcontrols.md)
</dt> </dl>

 

 