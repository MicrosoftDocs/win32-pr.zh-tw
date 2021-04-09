---
title: 非同步作業
description: 在非同步模式中，應用程式可以執行任何包含內容值的函式，做為它的其中一個參數，而且可以在應用程式等候函式完成其工作時，繼續執行其他命令或函數。
ms.assetid: 4b8ade00-deb3-4d9f-9ceb-5ba3296c8c68
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a7e1d0cf84aa92691e1d926d771ea809d31a171
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682765"
---
# <a name="asynchronous-operation"></a><span data-ttu-id="518d7-103">非同步作業</span><span class="sxs-lookup"><span data-stu-id="518d7-103">Asynchronous Operation</span></span>

<span data-ttu-id="518d7-104">應用程式存取網際網路資源所需的時間量，取決於許多因素，例如使用的連線、資源所在的伺服器，以及嘗試存取資源的使用者數目。</span><span class="sxs-lookup"><span data-stu-id="518d7-104">The amount of time it takes an application to access an Internet resource depends on a number of factors, such as the connection being used, the server on which the resource is located, and the number of users trying to access the resource.</span></span> <span data-ttu-id="518d7-105">針對下載多項資源或處理多項工作的應用程式 (包括一或多個下載) ，等候每個下載完成，再繼續進行下一項工作，會非常沒有效率。</span><span class="sxs-lookup"><span data-stu-id="518d7-105">For applications that download multiple resources or handle multiple tasks (including one or more downloads), waiting for each download to complete before moving on to the next task can be extremely inefficient.</span></span> <span data-ttu-id="518d7-106">若要減少應用程式必須等待的時間，許多 WinINet 函數都可以非同步作業。</span><span class="sxs-lookup"><span data-stu-id="518d7-106">To decrease the amount of time an application has to wait, many of the WinINet functions can operate asynchronously.</span></span>

<span data-ttu-id="518d7-107">在非同步模式中，應用程式可以執行任何包含內容值的函式，做為它的其中一個參數，而且可以在應用程式等候函式完成其工作時，繼續執行其他命令或函數。</span><span class="sxs-lookup"><span data-stu-id="518d7-107">In asynchronous mode, an application can execute any function that includes a context value as one of its parameters and can continue to execute other commands or functions while the application waits for the function to complete its task.</span></span> <span data-ttu-id="518d7-108">當工作完成時，應用程式所提供的狀態回呼函式會在工作進度以及完成時收到通知。</span><span class="sxs-lookup"><span data-stu-id="518d7-108">While the task is completing, a status callback function provided by the application is notified about the progress of the task and when it has completed.</span></span> <span data-ttu-id="518d7-109">目前，狀態回呼函式可以呼叫其他函式，或執行任何其他相依于工作完成的必要工作。</span><span class="sxs-lookup"><span data-stu-id="518d7-109">At this time, the status callback function can call other functions or perform any other required tasks that were dependent on the task's completion.</span></span>

<span data-ttu-id="518d7-110">當您以非同步方式呼叫 WinINet 時，不會 afinity 回呼執行緒：呼叫可能會從一個執行緒開始，但任何其他執行緒都可以接收回呼。</span><span class="sxs-lookup"><span data-stu-id="518d7-110">There is no callback thread afinity when you call WinINet asynchronously: a call might start from one thread, but any other thread can receive the callback.</span></span>

-   [<span data-ttu-id="518d7-111">優點</span><span class="sxs-lookup"><span data-stu-id="518d7-111">Benefits</span></span>](#benefits)
-   [<span data-ttu-id="518d7-112">案例</span><span class="sxs-lookup"><span data-stu-id="518d7-112">Scenarios</span></span>](#scenarios)
-   [<span data-ttu-id="518d7-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="518d7-113">Related Topics</span></span>](#related-topics)

## <a name="benefits"></a><span data-ttu-id="518d7-114">優點</span><span class="sxs-lookup"><span data-stu-id="518d7-114">Benefits</span></span>

<span data-ttu-id="518d7-115">非同步作業有幾個優點。</span><span class="sxs-lookup"><span data-stu-id="518d7-115">There are several benefits to operating asynchronously.</span></span> <span data-ttu-id="518d7-116">例如：</span><span class="sxs-lookup"><span data-stu-id="518d7-116">For example:</span></span>

-   <span data-ttu-id="518d7-117">同時下載多個網際網路資源。</span><span class="sxs-lookup"><span data-stu-id="518d7-117">Downloading multiple Internet resources simultaneously.</span></span>

    <span data-ttu-id="518d7-118">您可以同時連線至多個網際網路資源，並在可用時加以下載。</span><span class="sxs-lookup"><span data-stu-id="518d7-118">You can connect to multiple Internet resources at the same time and download them as they become available.</span></span>

-   <span data-ttu-id="518d7-119">提高應用程式的效能。</span><span class="sxs-lookup"><span data-stu-id="518d7-119">Increasing performance of your application.</span></span>

    <span data-ttu-id="518d7-120">使用 WinINet 函式的應用程式不需要等待要求完成，因此應用程式可以自由執行其他不相依于要求的工作，進而改善應用程式的整體效能。</span><span class="sxs-lookup"><span data-stu-id="518d7-120">An application using the WinINet functions asynchronously does not have to wait until the request is completed, so the application is free to do other tasks that are not dependent on the request, thus improving the application's overall performance.</span></span>

-   <span data-ttu-id="518d7-121">監視下載進度。</span><span class="sxs-lookup"><span data-stu-id="518d7-121">Monitor the progress of the download.</span></span>

    <span data-ttu-id="518d7-122">狀態回呼函式會在處理要求時接收通知。</span><span class="sxs-lookup"><span data-stu-id="518d7-122">The status callback function receives notifications while it is processing a request.</span></span> <span data-ttu-id="518d7-123">如有需要，您的應用程式可以使用該狀態回呼函式所提供的資訊，讓使用者知道作業進度，或中斷花費太長時間才能完成的要求。</span><span class="sxs-lookup"><span data-stu-id="518d7-123">If needed, your application can use the information provided by that status callback function to keep the user informed about the progress of the operation or to interrupt requests that are taking too long to complete.</span></span>

## <a name="scenarios"></a><span data-ttu-id="518d7-124">案例</span><span class="sxs-lookup"><span data-stu-id="518d7-124">Scenarios</span></span>

<span data-ttu-id="518d7-125">假設您的應用程式需要從 Downfall 咖啡 & 茶和第四個咖啡地點下載咖啡價格，並比較價格。</span><span class="sxs-lookup"><span data-stu-id="518d7-125">Let's say your application needs to download coffee prices from the Downfall Coffee & Tea and the Fourth Coffee sites and compare prices.</span></span> <span data-ttu-id="518d7-126">第四個咖啡場所通常會有較慢的回應時間，因此您的應用程式應該先從 Downfall 咖啡 & 茶下載資訊。</span><span class="sxs-lookup"><span data-stu-id="518d7-126">The Fourth Coffee site usually has a slower response time, so your application should download the information from Downfall Coffee & Tea first.</span></span>

<span data-ttu-id="518d7-127">開發應用程式的兩個版本。</span><span class="sxs-lookup"><span data-stu-id="518d7-127">Two versions of the application are developed.</span></span> <span data-ttu-id="518d7-128">其中一個是以同步方式運作，先從 Downfall 咖啡 & 茶網站下載價格，再從第四個咖啡網站下載價格。</span><span class="sxs-lookup"><span data-stu-id="518d7-128">One works synchronously, first downloading the prices from the Downfall Coffee & Tea site and then the prices from the Fourth Coffee site.</span></span> <span data-ttu-id="518d7-129">第二個作業會以非同步方式運作，並將要求傳送至兩個網站，並在可用時下載價格。</span><span class="sxs-lookup"><span data-stu-id="518d7-129">The second works asynchronously, sending requests to both sites and downloading the prices when they become available.</span></span>

<span data-ttu-id="518d7-130">下表說明第四個咖啡網站在特定一天的速度較快時，會發生什麼事。</span><span class="sxs-lookup"><span data-stu-id="518d7-130">The following table illustrates what would happen if the Fourth Coffee site was faster on a particular day.</span></span>



| <span data-ttu-id="518d7-131">事件</span><span class="sxs-lookup"><span data-stu-id="518d7-131">Event</span></span>                                                            | <span data-ttu-id="518d7-132">同步版本</span><span class="sxs-lookup"><span data-stu-id="518d7-132">Synchronous version</span></span>                        | <span data-ttu-id="518d7-133">非同步版本</span><span class="sxs-lookup"><span data-stu-id="518d7-133">Asynchronous version</span></span>                                     |
|------------------------------------------------------------------|--------------------------------------------|----------------------------------------------------------|
| <span data-ttu-id="518d7-134">開始</span><span class="sxs-lookup"><span data-stu-id="518d7-134">Start</span></span>                                                            | <span data-ttu-id="518d7-135">將要求傳送至 Downfall 咖啡 & 茶</span><span class="sxs-lookup"><span data-stu-id="518d7-135">Send request to Downfall Coffee & Tea</span></span>      | <span data-ttu-id="518d7-136">傳送要求以 Downfall 咖啡 & 茶和第四咖啡</span><span class="sxs-lookup"><span data-stu-id="518d7-136">Send requests to Downfall Coffee & Tea and Fourth Coffee</span></span> |
| <span data-ttu-id="518d7-137">從非同步版本到第四個咖啡的要求已完成</span><span class="sxs-lookup"><span data-stu-id="518d7-137">Request from the asynchronous version to Fourth Coffee completed</span></span> | <span data-ttu-id="518d7-138">等候中</span><span class="sxs-lookup"><span data-stu-id="518d7-138">Waiting</span></span>                                    | <span data-ttu-id="518d7-139">下載第四個咖啡的價格</span><span class="sxs-lookup"><span data-stu-id="518d7-139">Download prices from Fourth Coffee</span></span>                       |
| <span data-ttu-id="518d7-140">要求 Downfall 咖啡 & 茶已完成</span><span class="sxs-lookup"><span data-stu-id="518d7-140">Request to Downfall Coffee & Tea completed</span></span>                       | <span data-ttu-id="518d7-141">從 Downfall 咖啡 & 茶下載價格</span><span class="sxs-lookup"><span data-stu-id="518d7-141">Download prices from Downfall Coffee & Tea</span></span> | <span data-ttu-id="518d7-142">從 Downfall 咖啡 & 茶下載價格</span><span class="sxs-lookup"><span data-stu-id="518d7-142">Download prices from Downfall Coffee & Tea</span></span>               |
| <span data-ttu-id="518d7-143">Downfall 咖啡之後 & 茶的價格將會下載</span><span class="sxs-lookup"><span data-stu-id="518d7-143">After Downfall Coffee & Tea's prices are downloaded</span></span>              | <span data-ttu-id="518d7-144">將要求傳送至第四個咖啡</span><span class="sxs-lookup"><span data-stu-id="518d7-144">Send request to Fourth Coffee</span></span>              | <span data-ttu-id="518d7-145">比較價格</span><span class="sxs-lookup"><span data-stu-id="518d7-145">Compare prices</span></span>                                           |
| <span data-ttu-id="518d7-146">非同步版本的比較已完成</span><span class="sxs-lookup"><span data-stu-id="518d7-146">Asynchronous version's comparison completed</span></span>                      | <span data-ttu-id="518d7-147">等候中</span><span class="sxs-lookup"><span data-stu-id="518d7-147">Waiting</span></span>                                    | <span data-ttu-id="518d7-148">作業完成</span><span class="sxs-lookup"><span data-stu-id="518d7-148">Operation complete</span></span>                                       |
| <span data-ttu-id="518d7-149">從同步版本到第四個咖啡的要求已完成</span><span class="sxs-lookup"><span data-stu-id="518d7-149">Request from the synchronous version to Fourth Coffee completed</span></span>  | <span data-ttu-id="518d7-150">下載第四個咖啡的價格</span><span class="sxs-lookup"><span data-stu-id="518d7-150">Download prices from Fourth Coffee</span></span>         | <span data-ttu-id="518d7-151">n/a</span><span class="sxs-lookup"><span data-stu-id="518d7-151">n/a</span></span>                                                      |
| <span data-ttu-id="518d7-152">下載第四次咖啡的價格之後</span><span class="sxs-lookup"><span data-stu-id="518d7-152">After Fourth Coffee's prices are downloaded</span></span>                      | <span data-ttu-id="518d7-153">比較價格</span><span class="sxs-lookup"><span data-stu-id="518d7-153">Compare prices</span></span>                             | <span data-ttu-id="518d7-154">n/a</span><span class="sxs-lookup"><span data-stu-id="518d7-154">n/a</span></span>                                                      |
| <span data-ttu-id="518d7-155">同步版本的比較已完成</span><span class="sxs-lookup"><span data-stu-id="518d7-155">Synchronous version's comparison completed</span></span>                       | <span data-ttu-id="518d7-156">作業完成</span><span class="sxs-lookup"><span data-stu-id="518d7-156">Operation complete</span></span>                         | <span data-ttu-id="518d7-157">n/a</span><span class="sxs-lookup"><span data-stu-id="518d7-157">n/a</span></span>                                                      |



 

<span data-ttu-id="518d7-158">另一個範例是網頁瀏覽器，例如 Microsoft Internet Explorer。</span><span class="sxs-lookup"><span data-stu-id="518d7-158">Another example would be a web browser such as Microsoft Internet Explorer.</span></span> <span data-ttu-id="518d7-159">當瀏覽器下載頁面時，通常需要下載其他資源，例如影像和音效檔。</span><span class="sxs-lookup"><span data-stu-id="518d7-159">When the browser downloads a page, it often needs to download other resources, such as images and sound files.</span></span> <span data-ttu-id="518d7-160">在非同步模式中，頁面和其相關聯的資源可以在可用時同時進行要求和下載，而不是一次要求和下載頁面和每一個資源。</span><span class="sxs-lookup"><span data-stu-id="518d7-160">In asynchronous mode, the page and its associated resources can be requested simultaneously and downloaded as they become available, instead of requesting and downloading the page and each resource one at a time.</span></span>

## <a name="related-topics"></a><span data-ttu-id="518d7-161">[相關主題]</span><span class="sxs-lookup"><span data-stu-id="518d7-161">Related Topics</span></span>

<span data-ttu-id="518d7-162">以下是相關的連結。</span><span class="sxs-lookup"><span data-stu-id="518d7-162">The following are related links.</span></span>

<span data-ttu-id="518d7-163">教學課程</span><span class="sxs-lookup"><span data-stu-id="518d7-163">Tutorials</span></span>

-   [<span data-ttu-id="518d7-164">建立狀態回呼函數</span><span class="sxs-lookup"><span data-stu-id="518d7-164">Creating Status Callback Functions</span></span>](creating-status-callback-functions.md)

<span data-ttu-id="518d7-165">設定非同步作業所需的函數</span><span class="sxs-lookup"><span data-stu-id="518d7-165">Functions needed to set up asynchronous operation</span></span>

-   [<span data-ttu-id="518d7-166">**InternetOpen**</span><span class="sxs-lookup"><span data-stu-id="518d7-166">**InternetOpen**</span></span>](/windows/desktop/api/Wininet/nf-wininet-internetopena)
-   [<span data-ttu-id="518d7-167">**InternetSetStatusCallback**</span><span class="sxs-lookup"><span data-stu-id="518d7-167">**InternetSetStatusCallback**</span></span>](/windows/desktop/api/Wininet/nf-wininet-internetsetstatuscallback)

<span data-ttu-id="518d7-168">可以非同步使用的函式</span><span class="sxs-lookup"><span data-stu-id="518d7-168">Functions that can be used asynchronously</span></span>

-   [<span data-ttu-id="518d7-169">**FtpCreateDirectory**</span><span class="sxs-lookup"><span data-stu-id="518d7-169">**FtpCreateDirectory**</span></span>](/windows/desktop/api/Wininet/nf-wininet-ftpcreatedirectorya)
-   [<span data-ttu-id="518d7-170">**FtpDeleteFile**</span><span class="sxs-lookup"><span data-stu-id="518d7-170">**FtpDeleteFile**</span></span>](/windows/desktop/api/Wininet/nf-wininet-ftpdeletefilea)
-   [<span data-ttu-id="518d7-171">**FtpFindFirstFile**</span><span class="sxs-lookup"><span data-stu-id="518d7-171">**FtpFindFirstFile**</span></span>](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea)
-   [<span data-ttu-id="518d7-172">**FtpGetCurrentDirectory**</span><span class="sxs-lookup"><span data-stu-id="518d7-172">**FtpGetCurrentDirectory**</span></span>](/windows/desktop/api/Wininet/nf-wininet-ftpgetcurrentdirectorya)
-   [<span data-ttu-id="518d7-173">**FtpGetFile**</span><span class="sxs-lookup"><span data-stu-id="518d7-173">**FtpGetFile**</span></span>](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea)
-   [<span data-ttu-id="518d7-174">**FtpOpenFile**</span><span class="sxs-lookup"><span data-stu-id="518d7-174">**FtpOpenFile**</span></span>](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)
-   [<span data-ttu-id="518d7-175">**FtpPutFile**</span><span class="sxs-lookup"><span data-stu-id="518d7-175">**FtpPutFile**</span></span>](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea)
-   [<span data-ttu-id="518d7-176">**FtpRemoveDirectory**</span><span class="sxs-lookup"><span data-stu-id="518d7-176">**FtpRemoveDirectory**</span></span>](/windows/desktop/api/Wininet/nf-wininet-ftpremovedirectorya)
-   [<span data-ttu-id="518d7-177">**FtpRenameFile**</span><span class="sxs-lookup"><span data-stu-id="518d7-177">**FtpRenameFile**</span></span>](/windows/desktop/api/Wininet/nf-wininet-ftprenamefilea)
-   [<span data-ttu-id="518d7-178">**FtpSetCurrentDirectory**</span><span class="sxs-lookup"><span data-stu-id="518d7-178">**FtpSetCurrentDirectory**</span></span>](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya)
-   [<span data-ttu-id="518d7-179">**GopherFindFirstFile**</span><span class="sxs-lookup"><span data-stu-id="518d7-179">**GopherFindFirstFile**</span></span>](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea)
-   [<span data-ttu-id="518d7-180">**GopherOpenFile**</span><span class="sxs-lookup"><span data-stu-id="518d7-180">**GopherOpenFile**</span></span>](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea)
-   [<span data-ttu-id="518d7-181">**HttpEndRequest**</span><span class="sxs-lookup"><span data-stu-id="518d7-181">**HttpEndRequest**</span></span>](/windows/desktop/api/Wininet/nf-wininet-httpendrequesta)
-   [<span data-ttu-id="518d7-182">**HttpOpenRequest**</span><span class="sxs-lookup"><span data-stu-id="518d7-182">**HttpOpenRequest**</span></span>](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)
-   [<span data-ttu-id="518d7-183">**HttpSendRequestEx**</span><span class="sxs-lookup"><span data-stu-id="518d7-183">**HttpSendRequestEx**</span></span>](/windows/desktop/api/Wininet/nf-wininet-httpsendrequestexa)
-   [<span data-ttu-id="518d7-184">**InternetConnect**</span><span class="sxs-lookup"><span data-stu-id="518d7-184">**InternetConnect**</span></span>](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)
-   [<span data-ttu-id="518d7-185">**InternetOpenUrl**</span><span class="sxs-lookup"><span data-stu-id="518d7-185">**InternetOpenUrl**</span></span>](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)
-   [<span data-ttu-id="518d7-186">**InternetReadFileEx**</span><span class="sxs-lookup"><span data-stu-id="518d7-186">**InternetReadFileEx**</span></span>](/windows/desktop/api/Wininet/nf-wininet-internetreadfileexa)

> [!Note]  
> <span data-ttu-id="518d7-187">[**FtpCreateDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpcreatedirectorya)、 [**FtpRemoveDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpremovedirectorya)、 [**FtpSetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya)、 [**FtpGetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpgetcurrentdirectorya)、 [**FtpDeleteFile**](/windows/desktop/api/Wininet/nf-wininet-ftpdeletefilea)和 [**FtpRenameFile**](/windows/desktop/api/Wininet/nf-wininet-ftprenamefilea)函數會使用對 [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)函式的呼叫中所提供的內容值。</span><span class="sxs-lookup"><span data-stu-id="518d7-187">The [**FtpCreateDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpcreatedirectorya), [**FtpRemoveDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpremovedirectorya), [**FtpSetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya), [**FtpGetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpgetcurrentdirectorya), [**FtpDeleteFile**](/windows/desktop/api/Wininet/nf-wininet-ftpdeletefilea), and [**FtpRenameFile**](/windows/desktop/api/Wininet/nf-wininet-ftprenamefilea) functions use the context value provided in the call to the [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) function.</span></span>

 

> [!Note]  
> <span data-ttu-id="518d7-188">WinINet 不支援伺服器實施。</span><span class="sxs-lookup"><span data-stu-id="518d7-188">WinINet does not support server implementations.</span></span> <span data-ttu-id="518d7-189">此外，它不應該從服務使用。</span><span class="sxs-lookup"><span data-stu-id="518d7-189">In addition, it should not be used from a service.</span></span> <span data-ttu-id="518d7-190">針對伺服器執行或服務，請使用 [Microsoft WINDOWS HTTP services (WinHTTP) ](/windows/desktop/WinHttp/winhttp-start-page)。</span><span class="sxs-lookup"><span data-stu-id="518d7-190">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

 

 