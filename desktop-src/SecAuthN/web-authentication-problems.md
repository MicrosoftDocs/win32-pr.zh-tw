---
description: 本主題說明針對您的網頁使用 Web 驗證訊息代理程式 Api 的疑難排解秘訣。
ms.assetid: 25A024AA-9A70-40A5-BF5E-452FD148D0D2
title: Web 驗證問題
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cc4611461effd9cbc5546059e71fc8ca3f1f0be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104555480"
---
# <a name="web-authentication-problems"></a><span data-ttu-id="1a097-103">Web 驗證問題</span><span class="sxs-lookup"><span data-stu-id="1a097-103">Web authentication problems</span></span>

<span data-ttu-id="1a097-104">本主題說明針對您的網頁使用 Web 驗證訊息代理程式 Api 的疑難排解秘訣。</span><span class="sxs-lookup"><span data-stu-id="1a097-104">This topic describes troubleshooting tips for using the Web Authentication Broker APIs for your web pages.</span></span>

-   [<span data-ttu-id="1a097-105">操作記錄</span><span class="sxs-lookup"><span data-stu-id="1a097-105">Operational logs</span></span>](#operational-logs)
-   [<span data-ttu-id="1a097-106">使用 Fiddler 搭配 Web 驗證訊息代理程式</span><span class="sxs-lookup"><span data-stu-id="1a097-106">Using Fiddler with Web Authentication Broker</span></span>](#using-fiddler-with-web-authentication-broker)
-   [<span data-ttu-id="1a097-107">相關主題</span><span class="sxs-lookup"><span data-stu-id="1a097-107">Related topics</span></span>](#related-topics)

## <a name="operational-logs"></a><span data-ttu-id="1a097-108">作業記錄</span><span class="sxs-lookup"><span data-stu-id="1a097-108">Operational logs</span></span>

<span data-ttu-id="1a097-109">通常您可以透過使用作業記錄來判斷哪裡出問題。</span><span class="sxs-lookup"><span data-stu-id="1a097-109">Often you can determine what is not working by using the operational logs.</span></span> <span data-ttu-id="1a097-110">有一個專屬的事件記錄檔頻道可供 Microsoft Windows WebAuth \\ 操作，讓網站開發人員瞭解 Web 驗證訊息代理程式處理網頁的方式。</span><span class="sxs-lookup"><span data-stu-id="1a097-110">There is a dedicated event log channel Microsoft-Windows-WebAuth\\Operational that allows website developers to understand how their web pages are being processed by the Web Authentication Broker.</span></span> <span data-ttu-id="1a097-111">若要啟用它，請啟動 eventvwr.exe，並在應用程式和服務 \\ Microsoft \\ Windows WebAuth 下啟用操作記錄 \\ 。</span><span class="sxs-lookup"><span data-stu-id="1a097-111">To enable it, launch eventvwr.exe and enable Operational log under the Application and Services\\Microsoft\\Windows\\WebAuth.</span></span> <span data-ttu-id="1a097-112">此外，Web 驗證訊息代理程式會將唯一字串附加至使用者代理字串，以在 Web 服務器上識別其本身。</span><span class="sxs-lookup"><span data-stu-id="1a097-112">Also, the Web Authentication Broker appends a unique string to the user agent string to identify itself on the web server.</span></span> <span data-ttu-id="1a097-113">這個字串是 "MSAuthHost/1.0"。</span><span class="sxs-lookup"><span data-stu-id="1a097-113">The string is "MSAuthHost/1.0".</span></span> <span data-ttu-id="1a097-114">請注意，版本號碼在日後可能會有變更，因此在程式碼中不應該依據該版本號碼。</span><span class="sxs-lookup"><span data-stu-id="1a097-114">Note that the version number may change in the future, so you should not to depend on that version number in your code.</span></span> <span data-ttu-id="1a097-115">完整使用者代理程式字串的範例如下：</span><span class="sxs-lookup"><span data-stu-id="1a097-115">An example of the full user agent string is as follows:</span></span>

`User-Agent: Mozilla/5.0 (compatible; MSIE 10.0; Windows NT 6.2; Win64; x64; Trident/6.0; MSAuthHost/1.0)`

<span data-ttu-id="1a097-116">使用操作記錄的範例</span><span class="sxs-lookup"><span data-stu-id="1a097-116">Example of using operational logs</span></span>

1.  <span data-ttu-id="1a097-117">啟用操作記錄</span><span class="sxs-lookup"><span data-stu-id="1a097-117">Enable operational logs</span></span>
2.  <span data-ttu-id="1a097-118">執行 Contoso 社交應用程式</span><span class="sxs-lookup"><span data-stu-id="1a097-118">Run Contoso social application</span></span>![顯示 WebAuth 作業記錄的事件檢視器](images/wab-figure15.png)
3.  <span data-ttu-id="1a097-120">產生的記錄專案可以用來更詳細地瞭解 Web 驗證訊息代理程式的行為。</span><span class="sxs-lookup"><span data-stu-id="1a097-120">The generated logs entries can be used to understand the behavior of Web Authentication Broker in greater detail.</span></span> <span data-ttu-id="1a097-121">在此情況下，這些可能包括：</span><span class="sxs-lookup"><span data-stu-id="1a097-121">In this case, these can include:</span></span>
    -   <span data-ttu-id="1a097-122">瀏覽開始：記錄 AuthHost 何時啟動，並且包含開始和終止 URL 的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="1a097-122">Navigation Start: Logs when the AuthHost is started and contains information about the start and termination URLs.</span></span>
    -   ![說明「瀏覽開始」的詳細資料](images/wab-figure16.png)
    -   <span data-ttu-id="1a097-124">瀏覽完成：記錄網頁載入完成。</span><span class="sxs-lookup"><span data-stu-id="1a097-124">Navigation Complete: Logs the completion of loading a web page.</span></span>
    -   <span data-ttu-id="1a097-125">Meta 標記：記錄何時遇到 meta-tag，包含詳細資料。</span><span class="sxs-lookup"><span data-stu-id="1a097-125">Meta Tag: Logs when a meta-tag is encountered including the details.</span></span>
    -   <span data-ttu-id="1a097-126">瀏覽終止：使用者終止瀏覽。</span><span class="sxs-lookup"><span data-stu-id="1a097-126">Navigation Terminate: Navigation terminated by the user.</span></span>
    -   <span data-ttu-id="1a097-127">瀏覽錯誤：AuthHost 在 URL 遇到瀏覽錯誤，包含 HttpStatusCode。</span><span class="sxs-lookup"><span data-stu-id="1a097-127">Navigation Error: AuthHost encounters a navigation error at a URL including HttpStatusCode.</span></span>
    -   <span data-ttu-id="1a097-128">瀏覽結束：遇到終止 URL。</span><span class="sxs-lookup"><span data-stu-id="1a097-128">Navigation End: Terminating URL is encountered.</span></span>

## <a name="using-fiddler-with-web-authentication-broker"></a><span data-ttu-id="1a097-129">使用 Fiddler 搭配 Web 驗證訊息代理程式</span><span class="sxs-lookup"><span data-stu-id="1a097-129">Using Fiddler with Web Authentication Broker</span></span>

<span data-ttu-id="1a097-130">Fiddler web 偵錯工具可以與 Windows 8 apps 搭配使用。</span><span class="sxs-lookup"><span data-stu-id="1a097-130">The Fiddler web debugger can be used with Windows 8 apps.</span></span>

1.  <span data-ttu-id="1a097-131">由於 AuthHost 是在自己的 App 容器中執行以給予私人網路功能，因此您必須設定登錄機碼：Windows Registry Editor Version 5.00</span><span class="sxs-lookup"><span data-stu-id="1a097-131">Since the AuthHost runs in its own app container to give it the private network capability, you must set a registry key: Windows Registry Editor Version 5.00</span></span>

    <span data-ttu-id="1a097-132">**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **影像檔執行選項** \\ **authhost.exe** \\ **EnablePrivateNetwork** = 00000001</span><span class="sxs-lookup"><span data-stu-id="1a097-132">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**Windows NT**\\**CurrentVersion**\\**Image File Execution Options**\\**authhost.exe**\\**EnablePrivateNetwork** = 00000001</span></span><dl> <dt>

                     Data type
</dt> <dd>                     <span data-ttu-id="1a097-133">DWORD</span><span class="sxs-lookup"><span data-stu-id="1a097-133">DWORD</span></span></dd> </dl>

2.  <span data-ttu-id="1a097-134">為 AuthHost 新增一個規則，因為它負責產生輸出流量。</span><span class="sxs-lookup"><span data-stu-id="1a097-134">Add a rule for the AuthHost as this is what is generating the outbound traffic.</span></span>
    ```cmd
    CheckNetIsolation.exe LoopbackExempt -a -n=microsoft.windows.authhost.a.p_8wekyb3d8bbwe
    CheckNetIsolation.exe LoopbackExempt -a -n=microsoft.windows.authhost.sso.p_8wekyb3d8bbwe
    CheckNetIsolation.exe LoopbackExempt -a -n=microsoft.windows.authhost.sso.c_8wekyb3d8bbwe
    D:\Windows\System32>CheckNetIsolation.exe LoopbackExempt -s
    List Loopback Exempted AppContainers
    [1] -----------------------------------------------------------------
        Name: microsoft.windows.authhost.sso.c_8wekyb3d8bbwe
        SID:  S-1-15-2-1973105767-3975693666-32999980-3747492175-1074076486-3102532000-500629349
    [2] -----------------------------------------------------------------
        Name: microsoft.windows.authhost.sso.p_8wekyb3d8bbwe
        SID:  S-1-15-2-166260-4150837609-3669066492-3071230600-3743290616-3683681078-2492089544
    [3] -----------------------------------------------------------------
        Name: microsoft.windows.authhost.a.p_8wekyb3d8bbwe
        SID:  S-1-15-2-3506084497-1208594716-3384433646-2514033508-1838198150-1980605558-3480344935
    ```

    

3.  <span data-ttu-id="1a097-135">將連入流量防火牆規則新增到 Fiddler。</span><span class="sxs-lookup"><span data-stu-id="1a097-135">Add a firewall rule for incoming traffic to Fiddler.</span></span>

<span data-ttu-id="1a097-136">如需詳細資訊，請參閱 [使用 Fiddler web 偵錯工具搭配 Windows Store 應用程式的 Blog](/archive/blogs/fiddler/revisiting-fiddler-and-win8-immersive-applications)。</span><span class="sxs-lookup"><span data-stu-id="1a097-136">For more information, see [Blog on using Fiddler web debugger with Windows Store apps](/archive/blogs/fiddler/revisiting-fiddler-and-win8-immersive-applications).</span></span>

## <a name="related-topics"></a><span data-ttu-id="1a097-137">相關主題</span><span class="sxs-lookup"><span data-stu-id="1a097-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1a097-138">網頁開發的考量</span><span class="sxs-lookup"><span data-stu-id="1a097-138">Considerations for the web page development</span></span>](considerations-for-the-web-page-development.md)
</dt> <dt>

[<span data-ttu-id="1a097-139">Web 驗證訊息代理程式的常見問題</span><span class="sxs-lookup"><span data-stu-id="1a097-139">FAQ for Web Authentication Broker</span></span>](faq-for-web-authentication-broker.md)
</dt> <dt>

[<span data-ttu-id="1a097-140">Web Authentication Broker SDK 範例應用程式</span><span class="sxs-lookup"><span data-stu-id="1a097-140">Web Authentication Broker SDK sample app</span></span>](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker)
</dt> <dt>

[<span data-ttu-id="1a097-141">**Windows.Security.Authentication.Web**</span><span class="sxs-lookup"><span data-stu-id="1a097-141">**Windows.Security.Authentication.Web**</span></span>](/uwp/api/Windows.Security.Authentication.Web?view=winrt-19041)
</dt> </dl>

 

 
