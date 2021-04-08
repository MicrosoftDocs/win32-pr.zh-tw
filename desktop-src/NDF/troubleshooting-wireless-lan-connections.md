---
title: 無線區域網路連線疑難排解
description: 在此案例中，使用者嘗試連線到無線區域網路，但無法連線。 您可以使用 Netsh 和網路監視器來收集和查看追蹤，以協助判斷連接失敗的原因。
ms.assetid: 558dae83-aa16-4751-a497-d7a0da01ce5d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55878afcee0091634415d4dbc465d1b143f46057
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021921"
---
# <a name="troubleshooting-wireless-lan-connections"></a><span data-ttu-id="f8295-104">無線區域網路連線疑難排解</span><span class="sxs-lookup"><span data-stu-id="f8295-104">Troubleshooting Wireless LAN Connections</span></span>

<span data-ttu-id="f8295-105">在此案例中，使用者嘗試連線到無線區域網路，但無法連線。</span><span class="sxs-lookup"><span data-stu-id="f8295-105">In this scenario, a user is attempting to connect to a wireless LAN, but is unable to connect.</span></span> <span data-ttu-id="f8295-106">您可以使用 Netsh 和網路監視器來收集和查看追蹤，以協助判斷連接失敗的原因。</span><span class="sxs-lookup"><span data-stu-id="f8295-106">You can use Netsh and Network Monitor to collect and view traces in order to help determine why the connection failed.</span></span>

<span data-ttu-id="f8295-107">首先，您可以使用 netsh 來啟動追蹤。</span><span class="sxs-lookup"><span data-stu-id="f8295-107">First, you can use netsh to start a trace.</span></span> <span data-ttu-id="f8295-108">輸入 **netsh trace start 情節 = wlan tracefile = wlanwpp。 etl** 會開始追蹤在 wlan 案例下啟用的所有提供者，並將結果儲存至名為 wlanwpp 的檔案。</span><span class="sxs-lookup"><span data-stu-id="f8295-108">Typing **netsh trace start scenario = wlan tracefile=wlanwpp.etl** starts tracing for all of the providers enabled under the WLAN scenario, saving the results to a file named wlanwpp.etl.</span></span> <span data-ttu-id="f8295-109">嘗試連接到無線區域網路之後，輸入 **netsh trace stop** 會終止，並相互關聯追蹤檔案。</span><span class="sxs-lookup"><span data-stu-id="f8295-109">After attempting to connect to the wireless LAN, typing **netsh trace stop** terminates and correlates the trace file.</span></span>

<span data-ttu-id="f8295-110">然後，您可以在網路監視器中開啟 wlanwpp。</span><span class="sxs-lookup"><span data-stu-id="f8295-110">You can then open the wlanwpp.etl file in Network Monitor.</span></span> <span data-ttu-id="f8295-111">事件會依活動識別碼分組在左窗格中。</span><span class="sxs-lookup"><span data-stu-id="f8295-111">The events are grouped by activity ID in the left pane.</span></span>

![使用網路監視器 (1) 疑難排解無線區域網路連線](images/1wlan.png)

<span data-ttu-id="f8295-113">ETL 包含其他已啟用之網路提供者的許多追蹤。</span><span class="sxs-lookup"><span data-stu-id="f8295-113">The ETL contains lot of traces from other network providers that are enabled.</span></span> <span data-ttu-id="f8295-114">您可以套用篩選器，只顯示與 **WLAN \_ MicrosoftWindowsWlanAutoConfig** 提供者相關的事件。</span><span class="sxs-lookup"><span data-stu-id="f8295-114">You can apply a filter to display only those events which are relevant to the **WLAN\_MicrosoftWindowsWlanAutoConfig** provider.</span></span>

![使用網路監視器 (2) 的無線區域網路連線疑難排解](images/2wlan.png)

<span data-ttu-id="f8295-116">套用篩選之後，您可以檢查 [框架摘要] 中的事件，以找出看起來相關的事件。</span><span class="sxs-lookup"><span data-stu-id="f8295-116">After the filter has been applied, you can review the events in the frame summary to identify an event which looks relevant.</span></span> <span data-ttu-id="f8295-117">選取事件之後，以滑鼠右鍵按一下並指向 [尋找對話]，然後按一下 [NetEvent]。</span><span class="sxs-lookup"><span data-stu-id="f8295-117">After you select the event, right-click and point to Find Conversations, then click NetEvent.</span></span>

![使用網路監視器 (3) 疑難排解無線區域網路連線](images/3wlan.png)

<span data-ttu-id="f8295-119">展開左窗格中的活動識別碼下的專案，可讓您查看連接嘗試的所有其他相關提供者。</span><span class="sxs-lookup"><span data-stu-id="f8295-119">Expanding the items under an activity ID in the left pane will allow you to view all of the other relevant providers for the connection attempt.</span></span> <span data-ttu-id="f8295-120">若要查看其他提供者的事件，請在 [**顯示篩選**] 窗格中按一下 [**移除**]，以移除所有篩選。</span><span class="sxs-lookup"><span data-stu-id="f8295-120">To view the events from other providers, all filters are removed by clicking **Remove** in the **Display Filter** pane.</span></span> <span data-ttu-id="f8295-121">您可以藉由在畫面格摘要中滾動來分析追蹤，視需要選取其他事件來收集詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="f8295-121">The traces can be analyzed by scrolling through the frame summary, selecting additional events as needed to gather more information.</span></span> <span data-ttu-id="f8295-122">在此情況下，[畫面格詳細資料] 窗格會提供失敗原因的資訊，這是因為使用者輸入錯誤的通過金鑰。</span><span class="sxs-lookup"><span data-stu-id="f8295-122">In this case, the Frame Details pane provides information that the failure is due to key exchange failure, most likely due to the user entering the wrong pass key.</span></span>

 

 




