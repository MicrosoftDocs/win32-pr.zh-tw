---
title: Server-Side 設計
description: 伺服器端函式會透過 windows 外部物件與用戶端 wizard 進行通訊。 伺服器端腳本會提供這些函式來回應 wizard 事件，以及取得有關 wizard 的資訊。
ms.assetid: 7cc8b814-f230-4326-a9df-a491ed35483e
keywords:
- 發佈嚮導，伺服器端設計
- '[外部]、[發行] 嚮導'
- 發佈嚮導，window. 外部
- 發佈嚮導，導覽腳本函式
- 腳本，發佈嚮導
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20b3b218bbca297be446016335d90fe717a88bba
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103933245"
---
# <a name="server-side-design"></a><span data-ttu-id="8271c-109">Server-Side 設計</span><span class="sxs-lookup"><span data-stu-id="8271c-109">Server-Side Design</span></span>

<span data-ttu-id="8271c-110">伺服器端函式會透過 **windows 外部** 物件與用戶端 wizard 進行通訊。</span><span class="sxs-lookup"><span data-stu-id="8271c-110">Server-side functions communicate with the client wizard through the **windows.external** object.</span></span> <span data-ttu-id="8271c-111">伺服器端腳本會提供這些函式來回應 wizard 事件，以及取得有關 wizard 的資訊。</span><span class="sxs-lookup"><span data-stu-id="8271c-111">Server-side script provides these functions to respond to wizard events and to retrieve information about the wizard.</span></span>

<span data-ttu-id="8271c-112">本檔涵蓋下列主題。</span><span class="sxs-lookup"><span data-stu-id="8271c-112">The following topics are covered in this document.</span></span>

-   [<span data-ttu-id="8271c-113">執行導覽腳本函數</span><span class="sxs-lookup"><span data-stu-id="8271c-113">Implementing Navigation Script Functions</span></span>](#implementing-navigation-script-functions)
    -   [<span data-ttu-id="8271c-114">OnBack () </span><span class="sxs-lookup"><span data-stu-id="8271c-114">OnBack()</span></span>](#onback)
    -   [<span data-ttu-id="8271c-115">OnNext () </span><span class="sxs-lookup"><span data-stu-id="8271c-115">OnNext()</span></span>](#onnext)
    -   [<span data-ttu-id="8271c-116">OnCancel () </span><span class="sxs-lookup"><span data-stu-id="8271c-116">OnCancel()</span></span>](#oncancel)
-   [<span data-ttu-id="8271c-117">其他方法和屬性</span><span class="sxs-lookup"><span data-stu-id="8271c-117">Other Methods and Properties</span></span>](#other-methods-and-properties)
    -   [<span data-ttu-id="8271c-118">方法</span><span class="sxs-lookup"><span data-stu-id="8271c-118">Methods</span></span>](#methods)
    -   [<span data-ttu-id="8271c-119">屬性</span><span class="sxs-lookup"><span data-stu-id="8271c-119">Properties</span></span>](#properties)
-   [<span data-ttu-id="8271c-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="8271c-120">Related topics</span></span>](#related-topics)

## <a name="implementing-navigation-script-functions"></a><span data-ttu-id="8271c-121">執行導覽腳本函數</span><span class="sxs-lookup"><span data-stu-id="8271c-121">Implementing Navigation Script Functions</span></span>

<span data-ttu-id="8271c-122">每個 HTML 頁面中的伺服器端腳本都會透過 **OnBack**、 **OnNext** 和 **OnCancel** 的函式來回應導覽按鈕。</span><span class="sxs-lookup"><span data-stu-id="8271c-122">Server-side script in each HTML page responds to navigation buttons through functions for **OnBack**, **OnNext**, and **OnCancel**.</span></span> <span data-ttu-id="8271c-123">這些函式必須可透過用戶端上的 **IHTMLDocument：： get \_ 腳本** 存取，而且不會使用任何參數。</span><span class="sxs-lookup"><span data-stu-id="8271c-123">These functions must be accessible through **IHTMLDocument::get\_Script** on the client and take no parameters.</span></span>

### <a name="onback"></a><span data-ttu-id="8271c-124">OnBack () </span><span class="sxs-lookup"><span data-stu-id="8271c-124">OnBack()</span></span>

-   <span data-ttu-id="8271c-125">當使用者按一下嚮導中的 [ **返回** ] 時回應。</span><span class="sxs-lookup"><span data-stu-id="8271c-125">Responds when the user clicks **Back** in the wizard.</span></span>
-   <span data-ttu-id="8271c-126">如果目前的伺服器端頁面是第一個伺服器端頁面，請呼叫 **FinalBack** 來指示用戶端流覽至先前的用戶端頁面。</span><span class="sxs-lookup"><span data-stu-id="8271c-126">If the current server-side page is the first server-side page, call **window.external.FinalBack** to instruct the client to navigate to the previous client-side page.</span></span>
-   <span data-ttu-id="8271c-127">如果目前的伺服器端頁面不是第一個伺服器端頁面，請流覽至先前的伺服器端頁面。</span><span class="sxs-lookup"><span data-stu-id="8271c-127">If the current server-side page is not the first server-side page, navigate to the previous server-side page.</span></span>
-   <span data-ttu-id="8271c-128">每個頁面都必須執行此函數。</span><span class="sxs-lookup"><span data-stu-id="8271c-128">This function must be implemented for each page.</span></span> <span data-ttu-id="8271c-129">任何無法這麼做的頁面都會被視為無效，而且會顯示錯誤頁面。</span><span class="sxs-lookup"><span data-stu-id="8271c-129">Any page that fails to do so is considered invalid and displays an error page.</span></span>

### <a name="onnext"></a><span data-ttu-id="8271c-130">OnNext () </span><span class="sxs-lookup"><span data-stu-id="8271c-130">OnNext()</span></span>

-   <span data-ttu-id="8271c-131">當使用者按一下嚮導中的 **[下一步** ] 時回應。</span><span class="sxs-lookup"><span data-stu-id="8271c-131">Responds when the user clicks **Next** in the wizard.</span></span>
-   <span data-ttu-id="8271c-132">如果目前的伺服器端頁面是最後一個伺服器端頁面，請呼叫 **FinalNext** 來指示用戶端流覽至下一個用戶端頁面，或完成 wizard。</span><span class="sxs-lookup"><span data-stu-id="8271c-132">If the current server-side page is the last server-side page, call **window.external.FinalNext** to instruct the client to navigate to the next client-side page or to complete the wizard.</span></span>
-   <span data-ttu-id="8271c-133">如果目前的伺服器端頁面不是最後一個伺服器端頁面，請流覽至下一個伺服器端頁面。</span><span class="sxs-lookup"><span data-stu-id="8271c-133">If the current server-side page is not the last server-side page, navigate to the next server-side page.</span></span>

### <a name="oncancel"></a><span data-ttu-id="8271c-134">OnCancel () </span><span class="sxs-lookup"><span data-stu-id="8271c-134">OnCancel()</span></span>

-   <span data-ttu-id="8271c-135">當使用者按一下嚮導中的 [ **取消** ] 時回應。</span><span class="sxs-lookup"><span data-stu-id="8271c-135">Responds when the user clicks **Cancel** in the wizard.</span></span>
-   <span data-ttu-id="8271c-136">您應設計 UI，讓使用者可以隨時取消。</span><span class="sxs-lookup"><span data-stu-id="8271c-136">The UI should be designed so the user can cancel at any time.</span></span>
-   <span data-ttu-id="8271c-137">一旦處理 **OnCancel** 函式中的任何處理，用戶端就會關閉嚮導。</span><span class="sxs-lookup"><span data-stu-id="8271c-137">Once any processing in the **OnCancel** function is processed, the client closes the wizard.</span></span>

## <a name="other-methods-and-properties"></a><span data-ttu-id="8271c-138">其他方法和屬性</span><span class="sxs-lookup"><span data-stu-id="8271c-138">Other Methods and Properties</span></span>

<span data-ttu-id="8271c-139">用戶端執行的函式是透過 **windows** 進行存取，就像是屬性一樣。</span><span class="sxs-lookup"><span data-stu-id="8271c-139">Client-implemented functions are accessed through **windows.external**, as are properties.</span></span> <span data-ttu-id="8271c-140">可用的服務如下所示：</span><span class="sxs-lookup"><span data-stu-id="8271c-140">Available services are as follows:</span></span>

### <a name="methods"></a><span data-ttu-id="8271c-141">方法</span><span class="sxs-lookup"><span data-stu-id="8271c-141">Methods</span></span>

-   [<span data-ttu-id="8271c-142">**SetHeaderText**</span><span class="sxs-lookup"><span data-stu-id="8271c-142">**SetHeaderText**</span></span>](/windows/desktop/shell/iwebwizardhost-setheadertext)
-   [<span data-ttu-id="8271c-143">**SetWizardButtons**</span><span class="sxs-lookup"><span data-stu-id="8271c-143">**SetWizardButtons**</span></span>](/windows/desktop/shell/iwebwizardhost-setwizardbuttons)
-   [<span data-ttu-id="8271c-144">**PassportAuthenticate**</span><span class="sxs-lookup"><span data-stu-id="8271c-144">**PassportAuthenticate**</span></span>](/windows/desktop/shell/inewwdevents-passportauthenticate)

### <a name="properties"></a><span data-ttu-id="8271c-145">屬性</span><span class="sxs-lookup"><span data-stu-id="8271c-145">Properties</span></span>

-   <span data-ttu-id="8271c-146">[**標題**](/previous-versions/windows/desktop/legacy/bb774352(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8271c-146">[**Caption**](/previous-versions/windows/desktop/legacy/bb774352(v=vs.85))</span></span>
-   [<span data-ttu-id="8271c-147">**屬性**</span><span class="sxs-lookup"><span data-stu-id="8271c-147">**Property**</span></span>](/windows/desktop/shell/iwebwizardhost-property)

<span data-ttu-id="8271c-148">下列程式碼範例會顯示簡單的 wizard 頁面的伺服器端程式碼，其可執行 web 服務的錯誤頁面。</span><span class="sxs-lookup"><span data-stu-id="8271c-148">The following code sample shows server-side code for a simple wizard page which implements the web service's error page.</span></span>


```
<html>
    <head>
        <script language="JavaScript">
            function window.onload()
            {
                window.external.SetWizardButtons(1, 0, 0);    
                <!-- Back button enabled -->
            }

            function window.onback()
            {
                window.external.FinalBack();
            }
        </script>
    </head>
.
.
.
</html>
                    
```



## <a name="related-topics"></a><span data-ttu-id="8271c-149">相關主題</span><span class="sxs-lookup"><span data-stu-id="8271c-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8271c-150">用戶端設計</span><span class="sxs-lookup"><span data-stu-id="8271c-150">Client-Side Design</span></span>](pubwiz-client.md)
</dt> <dt>

[<span data-ttu-id="8271c-151">註冊服務</span><span class="sxs-lookup"><span data-stu-id="8271c-151">Registering a Service</span></span>](pubwiz-reg.md)
</dt> </dl>

 

 