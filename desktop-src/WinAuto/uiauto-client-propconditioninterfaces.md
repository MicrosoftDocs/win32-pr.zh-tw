---
title: 用戶端的屬性條件介面
description: 本節說明適用于 Microsoft Win32 應用程式之消費者介面自動化用戶端的屬性條件介面。
ms.assetid: cea34e47-03a9-4ff9-9019-427a2a3e13d6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00f840706d4f9e340cae86813a4992400791dccd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023565"
---
# <a name="property-condition-interfaces-for-clients"></a><span data-ttu-id="c49a8-103">用戶端的屬性條件介面</span><span class="sxs-lookup"><span data-stu-id="c49a8-103">Property Condition Interfaces for Clients</span></span>

<span data-ttu-id="c49a8-104">本節說明適用于 Microsoft Win32 應用程式之消費者介面自動化用戶端的屬性條件介面。</span><span class="sxs-lookup"><span data-stu-id="c49a8-104">This section describes property condition interfaces for UI Automation clients for Microsoft Win32 applications.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="c49a8-105">本節內容</span><span class="sxs-lookup"><span data-stu-id="c49a8-105">In this section</span></span>



| <span data-ttu-id="c49a8-106">介面</span><span class="sxs-lookup"><span data-stu-id="c49a8-106">Interface</span></span>                                                                                  | <span data-ttu-id="c49a8-107">描述</span><span class="sxs-lookup"><span data-stu-id="c49a8-107">Description</span></span>                                                                                                                                                        |
|--------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c49a8-108">**IUIAutomationAndCondition**</span><span class="sxs-lookup"><span data-stu-id="c49a8-108">**IUIAutomationAndCondition**</span></span>](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationandcondition)<br/>           | <span data-ttu-id="c49a8-109">公開屬性和方法，Microsoft 消費者介面自動化用戶端應用程式可以使用這些屬性和方法來取得和屬性條件的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="c49a8-109">Exposes properties and methods that Microsoft UI Automation client applications can use to retrieve information about an AND-based property condition.</span></span> <br/> |
| [<span data-ttu-id="c49a8-110">**IUIAutomationBoolCondition**</span><span class="sxs-lookup"><span data-stu-id="c49a8-110">**IUIAutomationBoolCondition**</span></span>](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationboolcondition)<br/>         | <span data-ttu-id="c49a8-111">表示可以是 **TRUE** 的條件 (選取所有元素) 或 **FALSE** (不會選取) 的任何元素。</span><span class="sxs-lookup"><span data-stu-id="c49a8-111">Represents a condition that can be either **TRUE** (selects all elements) or **FALSE** (selects no elements).</span></span><br/>                                           |
| [<span data-ttu-id="c49a8-112">**IUIAutomationCondition**</span><span class="sxs-lookup"><span data-stu-id="c49a8-112">**IUIAutomationCondition**</span></span>](/windows/win32/api/uiautomationclient/nn-uiautomationclient-iuiautomationcondition)<br/>                 | <span data-ttu-id="c49a8-113">這是搜尋消費者介面自動化樹狀結構中的專案時，用來進行篩選的條件主要介面。</span><span class="sxs-lookup"><span data-stu-id="c49a8-113">This is the primary interface for conditions used in filtering when searching for elements in the UI Automation tree.</span></span><br/>                                   |
| [<span data-ttu-id="c49a8-114">**IUIAutomationNotCondition**</span><span class="sxs-lookup"><span data-stu-id="c49a8-114">**IUIAutomationNotCondition**</span></span>](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationnotcondition)<br/>           | <span data-ttu-id="c49a8-115">表示另一個條件中負的條件。</span><span class="sxs-lookup"><span data-stu-id="c49a8-115">Represents a condition that is the negative of another condition.</span></span><br/>                                                                                       |
| [<span data-ttu-id="c49a8-116">**IUIAutomationOrCondition**</span><span class="sxs-lookup"><span data-stu-id="c49a8-116">**IUIAutomationOrCondition**</span></span>](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationorcondition)<br/>             | <span data-ttu-id="c49a8-117">表示由多個條件所組成的條件，至少其中一個條件必須為 true。</span><span class="sxs-lookup"><span data-stu-id="c49a8-117">Represents a condition made up of multiple conditions, at least one of which must be true.</span></span><br/>                                                              |
| [<span data-ttu-id="c49a8-118">**IUIAutomationPropertyCondition**</span><span class="sxs-lookup"><span data-stu-id="c49a8-118">**IUIAutomationPropertyCondition**</span></span>](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationpropertycondition)<br/> | <span data-ttu-id="c49a8-119">表示以用來尋找消費者介面自動化元素的屬性值為基礎的條件。</span><span class="sxs-lookup"><span data-stu-id="c49a8-119">Represents a condition based on a property value that is used to find UI Automation elements.</span></span><br/>                                                           |



 

## <a name="related-topics"></a><span data-ttu-id="c49a8-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="c49a8-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c49a8-121">消費者介面自動化用戶端</span><span class="sxs-lookup"><span data-stu-id="c49a8-121">UI Automation Clients</span></span>](uiauto-entry-uiautoclientsforwin32apps.md)
</dt> </dl>

 

