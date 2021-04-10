---
description: 視安裝程式傳遞給處理常式的訊息類型參數中提供的按鈕類型而定， (UI) 處理常式的外部使用者介面可以傳回任意數目的值給 Windows Installer。
ms.assetid: a918082d-709d-4b4f-ae3b-5f16ed0ca910
title: 從外部消費者介面處理常式傳回值
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b466f6bc3cc034551a01bd2b87caa7292824e0e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691779"
---
# <a name="returning-values-from-an-external-user-interface-handler"></a><span data-ttu-id="9ab5f-103">從外部消費者介面處理常式傳回值</span><span class="sxs-lookup"><span data-stu-id="9ab5f-103">Returning Values from an External User Interface Handler</span></span>

<span data-ttu-id="9ab5f-104">視安裝程式傳遞給處理常式的訊息類型參數中提供的按鈕類型而定， (UI) 處理常式的外部使用者介面可以傳回任意數目的值給 Windows Installer。</span><span class="sxs-lookup"><span data-stu-id="9ab5f-104">An external user interface (UI) handler can return any number of values to Windows Installer depending on the button type provided in the message type parameter the installer passes to the handler.</span></span>

<span data-ttu-id="9ab5f-105">外部 UI 處理常式可以在任何時間都傳回值–1和0，因為這些值與按鈕類型無關。</span><span class="sxs-lookup"><span data-stu-id="9ab5f-105">The external UI handler can return the values –1 and 0 at any time because these are not related to the button types.</span></span> <span data-ttu-id="9ab5f-106">傳回值-1 表示外部 UI 處理常式發生內部錯誤。</span><span class="sxs-lookup"><span data-stu-id="9ab5f-106">A return value of –1 indicates that an internal error occurred in the external UI handler.</span></span> <span data-ttu-id="9ab5f-107">傳回值0表示外部 UI 處理常式尚未處理安裝程式訊息，而且安裝程式必須改為處理訊息。</span><span class="sxs-lookup"><span data-stu-id="9ab5f-107">A return value of 0 indicates that the external UI handler has not handled the installer message and the installer must handle the message instead.</span></span>

<span data-ttu-id="9ab5f-108">對於不包含按鈕類型的訊息（例如 INSTALLMESSAGE \_ ACTIONDATA 和 INSTALLMESSAGE \_ 進度），傳回 IDCANCEL 會取消安裝。</span><span class="sxs-lookup"><span data-stu-id="9ab5f-108">For messages that do not include a button type, such as INSTALLMESSAGE\_ACTIONDATA and INSTALLMESSAGE\_PROGRESS, returning IDCANCEL cancels the installation.</span></span> <span data-ttu-id="9ab5f-109">傳回 IDOK 會通知安裝程式，訊息是由外部 UI 處理常式所處理。</span><span class="sxs-lookup"><span data-stu-id="9ab5f-109">Returning IDOK notifies the installer that the message was handled by the external UI handler.</span></span>

<span data-ttu-id="9ab5f-110">其餘的傳回值（如下所述）與訊息類型所包含的按鈕類型直接相關。</span><span class="sxs-lookup"><span data-stu-id="9ab5f-110">The remaining return values, as described below, are directly related to the button types that are included with the message type.</span></span>



| <span data-ttu-id="9ab5f-111">外部 UI 傳回值</span><span class="sxs-lookup"><span data-stu-id="9ab5f-111">External UI return value</span></span> | <span data-ttu-id="9ab5f-112">意義</span><span class="sxs-lookup"><span data-stu-id="9ab5f-112">Meaning</span></span>                                                                                                |
|--------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ab5f-113">IDOK</span><span class="sxs-lookup"><span data-stu-id="9ab5f-113">IDOK</span></span>                     | <span data-ttu-id="9ab5f-114">使用者已按下 [ **確定]** 按鈕。</span><span class="sxs-lookup"><span data-stu-id="9ab5f-114">The **OK** button was pressed by the user.</span></span> <span data-ttu-id="9ab5f-115">已瞭解訊息資訊。</span><span class="sxs-lookup"><span data-stu-id="9ab5f-115">The message information was understood.</span></span>                     |
| <span data-ttu-id="9ab5f-116">IDCANCEL</span><span class="sxs-lookup"><span data-stu-id="9ab5f-116">IDCANCEL</span></span>                 | <span data-ttu-id="9ab5f-117">已按下 [ **取消** ] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="9ab5f-117">The **CANCEL** button was pressed.</span></span> <span data-ttu-id="9ab5f-118">取消安裝。</span><span class="sxs-lookup"><span data-stu-id="9ab5f-118">Cancel the installation.</span></span>                                            |
| <span data-ttu-id="9ab5f-119">IDABORT</span><span class="sxs-lookup"><span data-stu-id="9ab5f-119">IDABORT</span></span>                  | <span data-ttu-id="9ab5f-120">已按下 [ **中止** ] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="9ab5f-120">The **ABORT** button was pressed.</span></span> <span data-ttu-id="9ab5f-121">中止安裝。</span><span class="sxs-lookup"><span data-stu-id="9ab5f-121">Abort the installation.</span></span>                                              |
| <span data-ttu-id="9ab5f-122">IDRETRY</span><span class="sxs-lookup"><span data-stu-id="9ab5f-122">IDRETRY</span></span>                  | <span data-ttu-id="9ab5f-123">已按下 [ **重試** ] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="9ab5f-123">The **RETRY** button was pressed.</span></span> <span data-ttu-id="9ab5f-124">請重試此動作。</span><span class="sxs-lookup"><span data-stu-id="9ab5f-124">Try the action again.</span></span>                                                |
| <span data-ttu-id="9ab5f-125">IDIGNORE</span><span class="sxs-lookup"><span data-stu-id="9ab5f-125">IDIGNORE</span></span>                 | <span data-ttu-id="9ab5f-126">已按下 [ **忽略** ] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="9ab5f-126">The **IGNORE** button was pressed.</span></span> <span data-ttu-id="9ab5f-127">忽略錯誤並繼續。</span><span class="sxs-lookup"><span data-stu-id="9ab5f-127">Ignore the error and continue.</span></span>                                      |
| <span data-ttu-id="9ab5f-128">IDYES</span><span class="sxs-lookup"><span data-stu-id="9ab5f-128">IDYES</span></span>                    | <span data-ttu-id="9ab5f-129">已按下 [ **是]** 按鈕。</span><span class="sxs-lookup"><span data-stu-id="9ab5f-129">The **YES** button was pressed.</span></span> <span data-ttu-id="9ab5f-130">肯定回應，繼續目前的事件順序。</span><span class="sxs-lookup"><span data-stu-id="9ab5f-130">The affirmative response, continue with current sequence of events..</span></span>   |
| <span data-ttu-id="9ab5f-131">IDNO</span><span class="sxs-lookup"><span data-stu-id="9ab5f-131">IDNO</span></span>                     | <span data-ttu-id="9ab5f-132">未按下 [ **否** ] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="9ab5f-132">The **NO** button was pressed.</span></span> <span data-ttu-id="9ab5f-133">負值回應不會繼續目前的事件順序。</span><span class="sxs-lookup"><span data-stu-id="9ab5f-133">The negative response, do not continue with current sequence of events.</span></span> |



 

<span data-ttu-id="9ab5f-134">例如，如果外部 UI 處理常式傳送了具有 MB \_ ABORTRETRYIGNORE 訊息方塊樣式旗標的訊息，則外部 ui 處理常式可能會傳回下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="9ab5f-134">For example, if the external UI handler is sent a message with the MB\_ABORTRETRYIGNORE message box styles flag, the external UI handler can return one of the following values:</span></span>

-   <span data-ttu-id="9ab5f-135">– 1 (外部 UI 處理常式的錯誤) </span><span class="sxs-lookup"><span data-stu-id="9ab5f-135">–1 (error in external UI handler)</span></span>
-   <span data-ttu-id="9ab5f-136">0 (不會在外部 UI 處理常式中採取任何動作，讓 Windows Installer 處理它) </span><span class="sxs-lookup"><span data-stu-id="9ab5f-136">0 (no action taken in external UI handler, let Windows Installer handle it)</span></span>
-   <span data-ttu-id="9ab5f-137">已按下 IDABORT (**中止** 按鈕) </span><span class="sxs-lookup"><span data-stu-id="9ab5f-137">IDABORT (**ABORT** button pressed)</span></span>
-   <span data-ttu-id="9ab5f-138">已按下 IDRETRY (**重試** 按鈕) </span><span class="sxs-lookup"><span data-stu-id="9ab5f-138">IDRETRY (**RETRY** button pressed)</span></span>
-   <span data-ttu-id="9ab5f-139">IDIGNORE (**略** 過已按下的按鈕) </span><span class="sxs-lookup"><span data-stu-id="9ab5f-139">IDIGNORE (**IGNORE** button pressed)</span></span>

 

 



