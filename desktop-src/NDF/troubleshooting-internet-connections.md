---
title: 針對網際網路連線進行疑難排解
description: 在此案例中，使用者嘗試使用 HTTPs 通訊協定流覽至 www.msn.com，但無法連接。 您可以使用 Netsh 和網路監視器來收集和查看追蹤，以協助判斷連接失敗的原因。
ms.assetid: e10fcc24-4670-461c-a145-3910c102e81f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 753636c1186243a96e3cef5a4ab73244556daec4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839796"
---
# <a name="troubleshooting-internet-connections"></a><span data-ttu-id="7209d-104">針對網際網路連線進行疑難排解</span><span class="sxs-lookup"><span data-stu-id="7209d-104">Troubleshooting Internet Connections</span></span>

<span data-ttu-id="7209d-105">在此案例中，使用者嘗試使用 HTTPs 通訊協定流覽至 www.msn.com，但無法連接。</span><span class="sxs-lookup"><span data-stu-id="7209d-105">In this scenario, a user is attempting to browse to www.msn.com using the https protocol, but is unable to connect.</span></span> <span data-ttu-id="7209d-106">您可以使用 Netsh 和網路監視器來收集和查看追蹤，以協助判斷連接失敗的原因。</span><span class="sxs-lookup"><span data-stu-id="7209d-106">You can use Netsh and Network Monitor to collect and view traces in order to help determine why the connection failed.</span></span>

<span data-ttu-id="7209d-107">首先，您可以使用 netsh 來啟動追蹤。</span><span class="sxs-lookup"><span data-stu-id="7209d-107">First, you can use netsh to start a trace.</span></span> <span data-ttu-id="7209d-108">輸入 **netsh trace start 情節 = InternetClient tracefile = msn。 etl** 會開始追蹤 InternetClient 案例下啟用的所有提供者，並將結果儲存到名為 msn 的檔案。</span><span class="sxs-lookup"><span data-stu-id="7209d-108">Typing **netsh trace start scenario = InternetClient tracefile=msn.etl** starts tracing for all of the providers enabled under the InternetClient scenario, saving the results to a file named msn.etl.</span></span> <span data-ttu-id="7209d-109">使用網頁瀏覽器嘗試連線到 www.msn.com 之後，輸入 **netsh trace stop** 會終止，並相互關聯追蹤檔案。</span><span class="sxs-lookup"><span data-stu-id="7209d-109">After using a web browser to attempt to reach www.msn.com, typing **netsh trace stop** terminates and correlates the trace file.</span></span>

<span data-ttu-id="7209d-110">然後，您可以在網路監視器中開啟 msn 檔案。</span><span class="sxs-lookup"><span data-stu-id="7209d-110">You can then open the msn.etl file in Network Monitor.</span></span> <span data-ttu-id="7209d-111">事件會依活動識別碼分組在左窗格中。</span><span class="sxs-lookup"><span data-stu-id="7209d-111">The events are grouped by activity ID in the left pane.</span></span> <span data-ttu-id="7209d-112">使用篩選 **描述。包含 ( "msn" )** 只會顯示其通訊協定描述中包含字串 "msn" 的事件。</span><span class="sxs-lookup"><span data-stu-id="7209d-112">Using the filter **description.contains("msn")** will show only those events which include the string "msn" in their protocol description.</span></span>

![使用網路監視器針對網際網路連線進行疑難排解 (1) ](images/internetclient1.png)

<span data-ttu-id="7209d-114">接下來，您可以在 [框架摘要] 中檢查事件，以找出看起來相關的事件。</span><span class="sxs-lookup"><span data-stu-id="7209d-114">Next, you can review the events in the frame summary to identify an event which looks relevant.</span></span> <span data-ttu-id="7209d-115">選取事件之後，以滑鼠右鍵按一下並指向 [尋找對話]，然後按一下 [UTEvent] 以選取 UTEvent 層級的交談。</span><span class="sxs-lookup"><span data-stu-id="7209d-115">After you select the event, right-click and point to Find Conversations, then click UTEvent to select the conversation at the UTEvent level.</span></span>

![使用網路監視器針對網際網路連線進行疑難排解 (2) ](images/internetclient2.png)

<span data-ttu-id="7209d-117">在左窗格中，會反白顯示相關聯的正規化活動，在此案例中為 UTEvent ActivityID 397。</span><span class="sxs-lookup"><span data-stu-id="7209d-117">The associated normalized activity in the left pane is then highlighted, in this case UTEvent ActivityID 397.</span></span>

![使用網路監視器針對網際網路連線進行疑難排解 (3) ](images/internetclient3.png)

<span data-ttu-id="7209d-119">藉由使用網路監視器來查看和篩選追蹤資訊，要檢查的事件數目已從1989減少為96。</span><span class="sxs-lookup"><span data-stu-id="7209d-119">By using Network Monitor to view and filter the trace information, the number of events to examine has been reduced from 1989 to 96.</span></span>

 

 




