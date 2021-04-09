---
title: 建立 CUIAutomation 物件
description: 本節說明如何藉由具現化可執行 IUIAutomation 的物件來開始撰寫 Microsoft 消費者介面自動化用戶端應用程式。
ms.assetid: 9b90da60-0204-48c1-bb16-ff4a843bac67
keywords:
- 用戶端，建立 CUIAutomation 物件
- 用戶端，CUIAutomation 物件
- 消費者介面自動化，CUIAutomation 物件
- 消費者介面自動化，建立 CUIAutomation 物件
- 建立 CUIAutomation 物件
- CUIAutomation 物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8162dac5276bbb22d00413276482cca34334fda5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933297"
---
# <a name="creating-the-cuiautomation-object"></a><span data-ttu-id="32a1e-109">建立 CUIAutomation 物件</span><span class="sxs-lookup"><span data-stu-id="32a1e-109">Creating the CUIAutomation Object</span></span>

<span data-ttu-id="32a1e-110">本節說明如何藉由具現化可執行 [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation)的物件來開始撰寫 Microsoft 消費者介面自動化用戶端應用程式。</span><span class="sxs-lookup"><span data-stu-id="32a1e-110">This section describes how to get started writing a Microsoft UI Automation client application by instantiating an object that implements [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation).</span></span>

<span data-ttu-id="32a1e-111">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="32a1e-111">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="32a1e-112">CUIAutomation 物件</span><span class="sxs-lookup"><span data-stu-id="32a1e-112">The CUIAutomation Object</span></span>](#the-cuiautomation-object)
-   [<span data-ttu-id="32a1e-113">建立物件</span><span class="sxs-lookup"><span data-stu-id="32a1e-113">Creating the Object</span></span>](#creating-the-object)
-   [<span data-ttu-id="32a1e-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="32a1e-114">Related topics</span></span>](#related-topics)

## <a name="the-cuiautomation-object"></a><span data-ttu-id="32a1e-115">CUIAutomation 物件</span><span class="sxs-lookup"><span data-stu-id="32a1e-115">The CUIAutomation Object</span></span>

<span data-ttu-id="32a1e-116">使用消費者介面自動化的第一個步驟是建立 [**CUIAutomation**](/previous-versions/windows/desktop/legacy/ff384838(v=vs.85)) 類別的物件。</span><span class="sxs-lookup"><span data-stu-id="32a1e-116">The first step in using UI Automation is to create an object of the [**CUIAutomation**](/previous-versions/windows/desktop/legacy/ff384838(v=vs.85)) class.</span></span> <span data-ttu-id="32a1e-117">此物件會公開 [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) 介面，也就是用戶端應用程式使用的所有其他物件和介面的閘道。</span><span class="sxs-lookup"><span data-stu-id="32a1e-117">This object exposes the [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) interface, which is the gateway to all the other objects and interfaces that are used by client applications.</span></span> <span data-ttu-id="32a1e-118">此外， **IUIAutomation** 可用於下列工作：</span><span class="sxs-lookup"><span data-stu-id="32a1e-118">Among other things, **IUIAutomation** is used for the following tasks:</span></span>

-   <span data-ttu-id="32a1e-119">訂閱事件。</span><span class="sxs-lookup"><span data-stu-id="32a1e-119">Subscribing to events.</span></span>
-   <span data-ttu-id="32a1e-120">建立條件。</span><span class="sxs-lookup"><span data-stu-id="32a1e-120">Creating conditions.</span></span> <span data-ttu-id="32a1e-121">條件是用來縮小消費者介面自動化元素搜尋範圍的物件。</span><span class="sxs-lookup"><span data-stu-id="32a1e-121">Conditions are objects used to narrow the scope of searches for UI Automation elements.</span></span>
-   <span data-ttu-id="32a1e-122">從桌面 (根項目) ，或從螢幕座標或視窗控點，直接取得消費者介面自動化專案。</span><span class="sxs-lookup"><span data-stu-id="32a1e-122">Obtaining UI Automation elements directly from the desktop (the root element), or from screen coordinates or window handles.</span></span>
-   <span data-ttu-id="32a1e-123">建立可用於導覽消費者介面自動化專案階層的樹狀瀏覽目錄者物件。</span><span class="sxs-lookup"><span data-stu-id="32a1e-123">Creating tree walker objects that can be used to navigate the hierarchy of UI Automation elements.</span></span>
-   <span data-ttu-id="32a1e-124">轉換資料類型。</span><span class="sxs-lookup"><span data-stu-id="32a1e-124">Converting data types.</span></span>

## <a name="creating-the-object"></a><span data-ttu-id="32a1e-125">建立物件</span><span class="sxs-lookup"><span data-stu-id="32a1e-125">Creating the Object</span></span>

<span data-ttu-id="32a1e-126">若要開始在您的應用程式中使用消費者介面自動化，請執行下列步驟：</span><span class="sxs-lookup"><span data-stu-id="32a1e-126">To get started using UI Automation in your application, take the following steps:</span></span>

-   <span data-ttu-id="32a1e-127">在您的專案標頭中包含 UIAutomation。</span><span class="sxs-lookup"><span data-stu-id="32a1e-127">Include UIAutomation.h in your project headers.</span></span> <span data-ttu-id="32a1e-128">UIAutomation 會帶入定義 API 的其他標頭。</span><span class="sxs-lookup"><span data-stu-id="32a1e-128">UIAutomation.h brings in the other headers that define the API.</span></span>
-   <span data-ttu-id="32a1e-129">宣告 [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation)的指標。</span><span class="sxs-lookup"><span data-stu-id="32a1e-129">Declare a pointer to [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation).</span></span>
-   <span data-ttu-id="32a1e-130"> (COM) 初始化元件物件模型。</span><span class="sxs-lookup"><span data-stu-id="32a1e-130">Initialize the Component Object Model (COM).</span></span>
-   <span data-ttu-id="32a1e-131">建立 [**CUIAutomation**](/previous-versions/windows/desktop/legacy/ff384838(v=vs.85)) 的實例，並在您的指標中取出 [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) 介面。</span><span class="sxs-lookup"><span data-stu-id="32a1e-131">Create an instance of [**CUIAutomation**](/previous-versions/windows/desktop/legacy/ff384838(v=vs.85)) and retrieve the [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) interface in your pointer.</span></span>

<span data-ttu-id="32a1e-132">下列範例函數會初始化 COM，然後建立 [**CUIAutomation**](/previous-versions/windows/desktop/legacy/ff384838(v=vs.85))物件，並在 *ppAutomation* 指標中抓取 [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation)介面。</span><span class="sxs-lookup"><span data-stu-id="32a1e-132">The following example function initializes COM, and then creates the [**CUIAutomation**](/previous-versions/windows/desktop/legacy/ff384838(v=vs.85)) object, retrieving the [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) interface in the *ppAutomation* pointer.</span></span>


```C++
#include <uiautomation.h>

// CoInitialize must be called before calling this function, and the  
// caller must release the returned pointer when finished with it.
// 
HRESULT InitializeUIAutomation(IUIAutomation **ppAutomation)
{
    return CoCreateInstance(CLSID_CUIAutomation, NULL,
        CLSCTX_INPROC_SERVER, IID_IUIAutomation, 
        reinterpret_cast<void**>(ppAutomation));
}
```



## <a name="related-topics"></a><span data-ttu-id="32a1e-133">相關主題</span><span class="sxs-lookup"><span data-stu-id="32a1e-133">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="32a1e-134">**概念**</span><span class="sxs-lookup"><span data-stu-id="32a1e-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="32a1e-135">UI 自動化事件概觀</span><span class="sxs-lookup"><span data-stu-id="32a1e-135">UI Automation Events Overview</span></span>](uiauto-eventsoverview.md)
</dt> <dt>

[<span data-ttu-id="32a1e-136">取得 UI 自動化項目</span><span class="sxs-lookup"><span data-stu-id="32a1e-136">Obtaining UI Automation Elements</span></span>](uiauto-obtainingelements.md)
</dt> </dl>

 

 