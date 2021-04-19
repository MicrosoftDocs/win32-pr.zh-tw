---
title: 用戶端的事件處理介面
description: 本節說明非受控消費者介面自動化用戶端應用程式的事件處理介面。
ms.assetid: ce9c4044-f46b-42b7-af44-05aee728a0e8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 458be6fcf5ce47f285d46c0e61f80e0897f15613
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106994942"
---
# <a name="event-handling-interfaces-for-clients"></a><span data-ttu-id="c4822-103">用戶端的事件處理介面</span><span class="sxs-lookup"><span data-stu-id="c4822-103">Event Handling Interfaces for Clients</span></span>

<span data-ttu-id="c4822-104">本節說明非受控消費者介面自動化用戶端應用程式的事件處理介面。</span><span class="sxs-lookup"><span data-stu-id="c4822-104">This section describes the event handling interfaces for unmanaged UI Automation client applications.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="c4822-105">本節內容</span><span class="sxs-lookup"><span data-stu-id="c4822-105">In this section</span></span>



| <span data-ttu-id="c4822-106">介面</span><span class="sxs-lookup"><span data-stu-id="c4822-106">Interface</span></span>                                                                                                              | <span data-ttu-id="c4822-107">描述</span><span class="sxs-lookup"><span data-stu-id="c4822-107">Description</span></span>                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c4822-108">**IUIAutomationChangesEventHandler**</span><span class="sxs-lookup"><span data-stu-id="c4822-108">**IUIAutomationChangesEventHandler**</span></span>](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationchangeseventhandler)<br/>                         | <span data-ttu-id="c4822-109">公開方法，以處理變更屬性時所發生的 Microsoft 消費者介面自動化事件。</span><span class="sxs-lookup"><span data-stu-id="c4822-109">Exposes a method to handle Microsoft UI Automation events that occur when a property is changed.</span></span><br/>                      |
| [<span data-ttu-id="c4822-110">**IUIAutomationEventHandler**</span><span class="sxs-lookup"><span data-stu-id="c4822-110">**IUIAutomationEventHandler**</span></span>](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationeventhandler)<br/>                                       | <span data-ttu-id="c4822-111">公開處理消費者介面自動化事件的方法。</span><span class="sxs-lookup"><span data-stu-id="c4822-111">Exposes a method to handle UI Automation events.</span></span><br/>                                                                      |
| [<span data-ttu-id="c4822-112">**IUIAutomationFocusChangedEventHandler**</span><span class="sxs-lookup"><span data-stu-id="c4822-112">**IUIAutomationFocusChangedEventHandler**</span></span>](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationfocuschangedeventhandler)<br/>               | <span data-ttu-id="c4822-113">公開方法，以處理鍵盤焦點移至另一個消費者介面自動化專案時所引發的事件。</span><span class="sxs-lookup"><span data-stu-id="c4822-113">Exposes a method to handle events that are raised when the keyboard focus moves to another UI Automation element.</span></span><br/>     |
| [<span data-ttu-id="c4822-114">**IUIAutomationNotificationEventHandler**</span><span class="sxs-lookup"><span data-stu-id="c4822-114">**IUIAutomationNotificationEventHandler**</span></span>](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationnotificationeventhandler)<br/>               | <span data-ttu-id="c4822-115">公開處理消費者介面自動化通知事件的方法。</span><span class="sxs-lookup"><span data-stu-id="c4822-115">Exposes a method to handle UI Automation notification events.</span></span><br/>                                                         |
| [<span data-ttu-id="c4822-116">**IUIAutomationPropertyChangedEventHandler**</span><span class="sxs-lookup"><span data-stu-id="c4822-116">**IUIAutomationPropertyChangedEventHandler**</span></span>](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationpropertychangedeventhandler)<br/>         | <span data-ttu-id="c4822-117">公開方法，以處理屬性變更時所發生的消費者介面自動化事件。</span><span class="sxs-lookup"><span data-stu-id="c4822-117">Exposes a method to handle UI Automation events that occur when a property is changed.</span></span><br/>                                |
| [<span data-ttu-id="c4822-118">**IUIAutomationStructureChangedEventHandler**</span><span class="sxs-lookup"><span data-stu-id="c4822-118">**IUIAutomationStructureChangedEventHandler**</span></span>](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationstructurechangedeventhandler)<br/>       | <span data-ttu-id="c4822-119">公開方法，以處理消費者介面自動化樹狀結構變更時所發生的事件。</span><span class="sxs-lookup"><span data-stu-id="c4822-119">Exposes a method to handle events that occur when the UI Automation tree structure is changed.</span></span><br/>                        |
| [<span data-ttu-id="c4822-120">**IUIAutomationTextEditTextChangedEventHandler**</span><span class="sxs-lookup"><span data-stu-id="c4822-120">**IUIAutomationTextEditTextChangedEventHandler**</span></span>](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextedittextchangedeventhandler)<br/> | <span data-ttu-id="c4822-121">公開方法，以處理當消費者介面自動化從文字編輯控制項報告文字變更的事件時所發生的事件。</span><span class="sxs-lookup"><span data-stu-id="c4822-121">Exposes a method to handle events that occur when UI Automation reports a text-changed event from text edit controls.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="c4822-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="c4822-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c4822-123">消費者介面自動化用戶端</span><span class="sxs-lookup"><span data-stu-id="c4822-123">UI Automation Clients</span></span>](uiauto-entry-uiautoclientsforwin32apps.md)
</dt> </dl>

 

 





