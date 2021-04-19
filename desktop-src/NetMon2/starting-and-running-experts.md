---
description: 按一下網路監視器 UI 的 [專家] 視窗中的 [執行專家]，即可啟動針對 capture 檔案選取的專家，並呼叫 Run 函數。 啟動時，專家會使用數個專家框架函式來分析 capture 檔案。
ms.assetid: 6b8a66cb-d1d6-4e19-b668-049a03a40804
title: 啟動及執行專家
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bd41472d286727541d26bade1942eb3b6b5c593
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106994564"
---
# <a name="starting-and-running-experts"></a><span data-ttu-id="1d48d-104">啟動及執行專家</span><span class="sxs-lookup"><span data-stu-id="1d48d-104">Starting and Running Experts</span></span>

<span data-ttu-id="1d48d-105">按一下網路監視器 UI 的 [專家] 視窗中的 [ **執行專家** ]，即可啟動針對 capture 檔案選取的專家，並呼叫 [**Run**](run.md) 函數。</span><span class="sxs-lookup"><span data-stu-id="1d48d-105">Clicking **Run Experts** from the Experts window of the Network Monitor UI starts the experts selected for the capture file and calls the [**Run**](run.md) function.</span></span> <span data-ttu-id="1d48d-106">啟動時，專家會使用數個專家框架函式來分析 capture 檔案。</span><span class="sxs-lookup"><span data-stu-id="1d48d-106">When started, the expert analyzes the capture file by using several expert frame functions.</span></span>

<span data-ttu-id="1d48d-107">[**ExpertIndicateStatus**](expertindicatestatus.md)函式會提供專家提供的狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="1d48d-107">The [**ExpertIndicateStatus**](expertindicatestatus.md) function provides status information from the expert.</span></span> <span data-ttu-id="1d48d-108">當您執行網路監視器的專家時，專家狀態視圖視窗會顯示定期更新的狀態資訊 (從0到100% 的完成) 。</span><span class="sxs-lookup"><span data-stu-id="1d48d-108">When you run an expert with Network Monitor, the Expert Status View window displays periodically updated status information (from 0 to 100 percent completion).</span></span>

![專家狀態視圖視窗](images/exview.png)

<span data-ttu-id="1d48d-110">在資料透過 capture 檔案完成通過之前，專家會處於作用中狀態。</span><span class="sxs-lookup"><span data-stu-id="1d48d-110">The expert is active until the data completes its pass though the capture file.</span></span> <span data-ttu-id="1d48d-111">當 pass 完成時，會出現事件檢視器視窗。</span><span class="sxs-lookup"><span data-stu-id="1d48d-111">When the pass is complete, an Event Viewer window appears.</span></span> <span data-ttu-id="1d48d-112">此視窗中的資訊取決於分析資料的專家類型。</span><span class="sxs-lookup"><span data-stu-id="1d48d-112">The information in this window depends on the type of expert that analyzed the data.</span></span> <span data-ttu-id="1d48d-113">下圖顯示內容散發專家的觀點，其中摘要了專家分析的框架資料。</span><span class="sxs-lookup"><span data-stu-id="1d48d-113">The following illustration shows a Property Distribution Expert view, which summarizes the frame data that the expert analyzed.</span></span>

![屬性散發專家觀點](images/exview1.png)

<span data-ttu-id="1d48d-115">第二份報表 (未顯示) ，摘要說明傳輸控制通訊協定 (TCP) 重新傳輸專家的結果。</span><span class="sxs-lookup"><span data-stu-id="1d48d-115">A second report (not shown), summarizes the results of the Transmission Control Protocol (TCP) Retransmit expert.</span></span>

<span data-ttu-id="1d48d-116">您也可以：</span><span class="sxs-lookup"><span data-stu-id="1d48d-116">You can also:</span></span>

-   <span data-ttu-id="1d48d-117">建立事件參考頁面 (ERP) 的專案，以建議使用者偵測到的狀況或問題 (如 [分析] 視窗) 所示。</span><span class="sxs-lookup"><span data-stu-id="1d48d-117">Create an entry for an event reference page (ERP) that advises the user of detected conditions or problems (as shown in the Analysis window).</span></span>
-   <span data-ttu-id="1d48d-118">建立建議的修正或說明資料的專案，以提供其他資訊 (如 [解決方式] 視窗) 所示。</span><span class="sxs-lookup"><span data-stu-id="1d48d-118">Create entries for suggested fixes or explanatory data that provide additional information (as shown in the Resolution window).</span></span>

<span data-ttu-id="1d48d-119">當專家完成其工作之後，網路監視器會從使用中記憶體中移除專家。</span><span class="sxs-lookup"><span data-stu-id="1d48d-119">After the expert completes its task, Network Monitor removes the expert from active memory.</span></span> <span data-ttu-id="1d48d-120">專家應使用平臺軟體發展工具組中包含的受保護記憶體函式 (SDK) ;如果專家在執行時間失敗，這些函式會清除記憶體。</span><span class="sxs-lookup"><span data-stu-id="1d48d-120">Experts should use the protected memory functions included in the Platform Software Development Kit (SDK); these functions clean up memory if the experts fail during run time.</span></span>

 

 



