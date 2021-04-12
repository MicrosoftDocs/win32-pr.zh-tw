---
title: 發佈嚮導簡介
description: Windows XP 引進了 Web 發佈嚮導和線上列印順序 Wizard。
ms.assetid: da3adc24-5b37-48b5-b055-d5bfa572defd
keywords:
- 發佈嚮導，關於
- Web 發佈嚮導，關於
- 線上列印訂購嚮導，關於
- 發佈嚮導，Web 發佈嚮導
- 發佈嚮導，線上列印訂購嚮導
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b4e6d3c515edae23d0e74f550e000bdfdfacf03
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104462985"
---
# <a name="publishing-wizards-introduction"></a><span data-ttu-id="f27e6-108">發佈嚮導簡介</span><span class="sxs-lookup"><span data-stu-id="f27e6-108">Publishing Wizards Introduction</span></span>

<span data-ttu-id="f27e6-109">Windows XP 引進了 Web 發佈嚮導和線上列印順序 Wizard。</span><span class="sxs-lookup"><span data-stu-id="f27e6-109">Windows XP introduces the Web Publishing Wizard and Online Print Ordering Wizard.</span></span> <span data-ttu-id="f27e6-110">根據相同的架構，這些嚮導為使用者提供一個簡單的機制，可將內容發佈至網站，或訂購從數位影像檔進行的列印。</span><span class="sxs-lookup"><span data-stu-id="f27e6-110">Based on the same framework, these wizards provide the user with a simple mechanism for publishing content to a website or for ordering prints made from digital image files.</span></span> <span data-ttu-id="f27e6-111">這些瀏覽器的優點在於能夠在其 wizard 頁面中裝載來自不同提供者的 HTML 內容，讓 [外觀]、[程式] 和 [可用] 使用者選項可以完全由提供者控制，而且可能會隨時變更，而不會影響裝載它們的用戶端 wizard。</span><span class="sxs-lookup"><span data-stu-id="f27e6-111">The advantage of these wizards lies in their ability to host HTML content from different providers within their wizard pages so that the look, procedure, and available user options are fully controlled by the provider and may be altered by them at any time without affecting the client wizard that is hosting them.</span></span> <span data-ttu-id="f27e6-112">雖然這些現有的嚮導都是以非常重要的數位影像來建立的，但架構和概念可用於許多其他用途，例如檔列印服務，或作為與朋友和家人共用影像的方法。</span><span class="sxs-lookup"><span data-stu-id="f27e6-112">While these existing wizards have been created with digital imaging firmly in mind, the framework and concepts can be used for many other purposes such as a document printing service or as a method of sharing images with friends and family.</span></span>

-   [<span data-ttu-id="f27e6-113">它如何運作？</span><span class="sxs-lookup"><span data-stu-id="f27e6-113">How Does It Work?</span></span>](#how-does-it-work)
-   [<span data-ttu-id="f27e6-114">發佈嚮導檔</span><span class="sxs-lookup"><span data-stu-id="f27e6-114">Publishing Wizard Documentation</span></span>](#publishing-wizard-documentation)

## <a name="how-does-it-work"></a><span data-ttu-id="f27e6-115">它如何運作？</span><span class="sxs-lookup"><span data-stu-id="f27e6-115">How Does It Work?</span></span>

<span data-ttu-id="f27e6-116">Web 發佈嚮導和線上列印順序 Wizard 的使用者體驗很類似，但每個 Wizard 的進入點各有不同。</span><span class="sxs-lookup"><span data-stu-id="f27e6-116">The user experience for the Web Publishing Wizard and Online Print Ordering Wizard is similar, but the entry point for each wizard differs.</span></span> <span data-ttu-id="f27e6-117">若為 Web 發佈嚮導，標題為 [將 **此資料夾發佈到網站** ] 的工作，可以從大部分資料夾流覽的左側的 [檔案 **和資料夾** 工作] 清單中取得。</span><span class="sxs-lookup"><span data-stu-id="f27e6-117">For the Web Publishing Wizard, a task titled **Publish this folder to the Web** is available from the **File and Folder Tasks** list to the left of most folder views.</span></span> <span data-ttu-id="f27e6-118">工作的文字會根據選取的內容而有所不同。</span><span class="sxs-lookup"><span data-stu-id="f27e6-118">The text for the task varies based on selected content.</span></span> <span data-ttu-id="f27e6-119">比方說，如果選取檔案，則工作會將 **這個檔案發佈到網站** ，如下列範例所示。</span><span class="sxs-lookup"><span data-stu-id="f27e6-119">For instance, if a file is selected, the task reads **Publish this file to the Web** as shown in the following example.</span></span>

![檔案和資料夾工作](images/shell-pubwiz-tasks.png)

<span data-ttu-id="f27e6-121">使用者按一下工作以啟動精靈。</span><span class="sxs-lookup"><span data-stu-id="f27e6-121">The user clicks the task to launch the wizard.</span></span> <span data-ttu-id="f27e6-122">繼續進行嚮導，使用者會看到提供者清單，如下列範例所示。</span><span class="sxs-lookup"><span data-stu-id="f27e6-122">Proceeding into the wizard, the user is presented with a list of providers as shown in the following example.</span></span> <span data-ttu-id="f27e6-123">網際網路服務提供者 (Isp) 可以開發並註冊自己的提供者頁面，以顯示在此清單中。</span><span class="sxs-lookup"><span data-stu-id="f27e6-123">Internet service providers (ISPs) can develop and register their own provider pages to be displayed in this list.</span></span>

![發佈嚮導提供者清單](images/shell-pubwiz-provs.png)

<span data-ttu-id="f27e6-125">選擇提供者之後，嚮導會連線至該網站，而第一個 HTML 網頁的下載則會在嚮導中顯示。</span><span class="sxs-lookup"><span data-stu-id="f27e6-125">Once a provider is chosen, the wizard connects to that site and the first HTML page downloads for display in the wizard.</span></span> <span data-ttu-id="f27e6-126">如果使用者沒有所選提供者的帳戶，則會有機會設定一個。</span><span class="sxs-lookup"><span data-stu-id="f27e6-126">If users do not have an account with the selected provider, they are given the opportunity to set one up.</span></span>

<span data-ttu-id="f27e6-127">在嚮導的單一頁面中包含多個 HTML 網頁;換句話說，裝載 procession HTML 網頁的 wizard 頁面的控制碼會維持不變。</span><span class="sxs-lookup"><span data-stu-id="f27e6-127">Multiple HTML pages are contained within a single page in the wizard; in other words, the handle of the wizard page hosting that procession of HTML pages remains constant.</span></span> <span data-ttu-id="f27e6-128">HTML 頁面會在中央窗格中公開，就像任何標準的 wizard 頁面一樣。</span><span class="sxs-lookup"><span data-stu-id="f27e6-128">The HTML pages are exposed in the center pane as with any standard wizard page.</span></span> <span data-ttu-id="f27e6-129">提供者網站提供的方法，可控制在顯示 HTML 網頁時，wizard 的 [ **上一頁**]、 **[下一頁**] 和 [ **取消** ] 按鈕的出現位置。</span><span class="sxs-lookup"><span data-stu-id="f27e6-129">The provider site provides methods to control where the wizard's **Back**, **Next**, and **Cancel** buttons lead while the HTML pages are being displayed.</span></span> <span data-ttu-id="f27e6-130">在這些 HTML 網頁中，系統可能會要求使用者指定可複製檔案的資料夾，或儲存他們想要建立之網站的名稱。</span><span class="sxs-lookup"><span data-stu-id="f27e6-130">Within those HTML pages, users might be asked to specify a folder where they can copy files or save the name of a website they wish to create.</span></span> <span data-ttu-id="f27e6-131">當使用者完成所有必要的步驟之後，網站會呼叫方法來開始上傳，然後將控制權歸還給 wizard。</span><span class="sxs-lookup"><span data-stu-id="f27e6-131">After a user has completed all the required steps, the site calls a method to begin the upload, returning control to the wizard.</span></span> <span data-ttu-id="f27e6-132">Wizard 本身會處理上傳和任何的任何附隨圖形，例如進度指標。</span><span class="sxs-lookup"><span data-stu-id="f27e6-132">The wizard itself handles the upload and any attendant graphics such as a progress indicator.</span></span> <span data-ttu-id="f27e6-133">上傳完成之後，提供者網站可以指定 URL，讓使用者可以在關閉嚮導之後進行。</span><span class="sxs-lookup"><span data-stu-id="f27e6-133">After the upload is completed, the provider site can specify a URL where the user can go once the wizard has been closed.</span></span>

<span data-ttu-id="f27e6-134">在 [線上列印順序] 嚮導中，工作 **順序** 只會在 [圖片] 資料夾（例如 [我的圖片]）中看到，如下列範例所示。</span><span class="sxs-lookup"><span data-stu-id="f27e6-134">In the Online Print Ordering Wizard, the task **Order prints online** is seen only in picture folders such as My Pictures, shown in the following example.</span></span> <span data-ttu-id="f27e6-135">不過，此程式與 Web 發佈嚮導非常類似。</span><span class="sxs-lookup"><span data-stu-id="f27e6-135">The process, however, is very similar to the Web Publishing Wizard.</span></span> <span data-ttu-id="f27e6-136">提供者網站會提示使用者提供選項，例如影像選取、列印大小、份數，以及付款資訊。</span><span class="sxs-lookup"><span data-stu-id="f27e6-136">The provider site prompts users for options such as image selection, print sizes, number of copies, and payment information.</span></span>

![圖片工作](images/shell-pubwiz-pix.png)

## <a name="publishing-wizard-documentation"></a><span data-ttu-id="f27e6-138">發佈嚮導檔</span><span class="sxs-lookup"><span data-stu-id="f27e6-138">Publishing Wizard Documentation</span></span>

<span data-ttu-id="f27e6-139">下列檔將詳細討論 Web 發佈嚮導和線上列印順序的 Wizard。</span><span class="sxs-lookup"><span data-stu-id="f27e6-139">The Web Publishing Wizard and Online Print Ordering Wizard are discussed in detail in the following documents.</span></span> <span data-ttu-id="f27e6-140">此外，也會討論如何開發應用程式來裝載這些應用程式。</span><span class="sxs-lookup"><span data-stu-id="f27e6-140">Also discussed are instructions for developing applications to be hosted by them.</span></span>

-   [<span data-ttu-id="f27e6-141">用戶端設計</span><span class="sxs-lookup"><span data-stu-id="f27e6-141">Client-Side Design</span></span>](pubwiz-client.md)
-   [<span data-ttu-id="f27e6-142">伺服器端設計</span><span class="sxs-lookup"><span data-stu-id="f27e6-142">Server-Side Design</span></span>](pubwiz-server.md)
-   [<span data-ttu-id="f27e6-143">註冊服務</span><span class="sxs-lookup"><span data-stu-id="f27e6-143">Registering a Service</span></span>](pubwiz-reg.md)
-   [<span data-ttu-id="f27e6-144">使用傳送資訊清單</span><span class="sxs-lookup"><span data-stu-id="f27e6-144">Using the Transfer Manifest</span></span>](pubwiz-manifest.md)
-   [<span data-ttu-id="f27e6-145">傳送資訊清單架構</span><span class="sxs-lookup"><span data-stu-id="f27e6-145">Transfer Manifest Schema</span></span>](/windows/desktop/shell/interfaces)

 

 