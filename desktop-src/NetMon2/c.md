---
description: 以字母 C 為開頭網路監視器詞彙的詞彙。
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 9e0b9f77-8a47-4724-b08c-fac3b6e23afc
title: 'C (網路監視器) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b06dd8ccd4d4c3382e7f7f7bb4426320bfcd8d4f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106981556"
---
# <a name="c-network-monitor"></a><span data-ttu-id="2ab2e-103">C (網路監視器) </span><span class="sxs-lookup"><span data-stu-id="2ab2e-103">C (Network Monitor)</span></span>

<dl> <dt>

<span data-ttu-id="2ab2e-104"><span id="_netmon_capture_gly"></span><span id="_NETMON_CAPTURE_GLY"></span>**捕獲**</span><span class="sxs-lookup"><span data-stu-id="2ab2e-104"><span id="_netmon_capture_gly"></span><span id="_NETMON_CAPTURE_GLY"></span>**capture**</span></span>
</dt> <dd>

<span data-ttu-id="2ab2e-105">在畫面格中收集的網路流量資料。</span><span class="sxs-lookup"><span data-stu-id="2ab2e-105">Network traffic data that is collected in frames.</span></span> <span data-ttu-id="2ab2e-106">網路封包提供者 (NPP) 執行捕獲。</span><span class="sxs-lookup"><span data-stu-id="2ab2e-106">A network packet provider (NPP) performs a capture.</span></span> <span data-ttu-id="2ab2e-107">另請參閱 [*延遲的捕獲*](d.md)和 *即時捕獲*</span><span class="sxs-lookup"><span data-stu-id="2ab2e-107">See also [*delayed capture*](d.md), and *real-time capture*</span></span>

</dd> <dt>

<span data-ttu-id="2ab2e-108"><span id="_netmon_capture_file_gly"></span><span id="_NETMON_CAPTURE_FILE_GLY"></span>**capture 檔案**</span><span class="sxs-lookup"><span data-stu-id="2ab2e-108"><span id="_netmon_capture_file_gly"></span><span id="_NETMON_CAPTURE_FILE_GLY"></span>**capture file**</span></span>
</dt> <dd>

<span data-ttu-id="2ab2e-109">網路監視器建立以儲存已捕捉資料的檔案。</span><span class="sxs-lookup"><span data-stu-id="2ab2e-109">A file that Network Monitor creates to store captured data.</span></span> <span data-ttu-id="2ab2e-110">Cap 副檔名會識別 capture 檔。</span><span class="sxs-lookup"><span data-stu-id="2ab2e-110">The .cap file name extension identifies a capture file.</span></span> <span data-ttu-id="2ab2e-111">網路監視器隨機產生 capture 檔案名，但您可以在儲存 capture 檔案時變更檔案名。</span><span class="sxs-lookup"><span data-stu-id="2ab2e-111">Network Monitor randomly generates a capture file name, but you can change the file name when you save the capture file.</span></span>

<span data-ttu-id="2ab2e-112">網路監視器會在每次捕捉程式啟動時建立 capture 檔案，然後在捕獲程式期間讓檔案保持開啟。</span><span class="sxs-lookup"><span data-stu-id="2ab2e-112">Network Monitor creates a capture file each time the capture process starts, and then keeps the file open during the capture process.</span></span> <span data-ttu-id="2ab2e-113">在停用捕捉程式並關閉 capture 檔案之前，您無法存取 capture 檔案的內容。</span><span class="sxs-lookup"><span data-stu-id="2ab2e-113">You cannot access the contents of a capture file until the capture process is stopped and the capture file is closed.</span></span>

</dd> <dt>

<span data-ttu-id="2ab2e-114"><span id="_netmon_capture_filter_gly"></span><span id="_NETMON_CAPTURE_FILTER_GLY"></span>**capture 篩選**</span><span class="sxs-lookup"><span data-stu-id="2ab2e-114"><span id="_netmon_capture_filter_gly"></span><span id="_NETMON_CAPTURE_FILTER_GLY"></span>**capture filter**</span></span>
</dt> <dd>

<span data-ttu-id="2ab2e-115">一組網路監視器函式，用來限制網路封包提供者 (NPP) 應用程式所使用的內送框架。</span><span class="sxs-lookup"><span data-stu-id="2ab2e-115">A set of Network Monitor functions used to restrict incoming frames that a network packet provider (NPP) application uses.</span></span>

</dd> <dt>

<span data-ttu-id="2ab2e-116"><span id="_netmon_capture_trigger_gly"></span><span id="_NETMON_CAPTURE_TRIGGER_GLY"></span>**capture 觸發程式**</span><span class="sxs-lookup"><span data-stu-id="2ab2e-116"><span id="_netmon_capture_trigger_gly"></span><span id="_NETMON_CAPTURE_TRIGGER_GLY"></span>**capture trigger**</span></span>
</dt> <dd>

<span data-ttu-id="2ab2e-117">設定為停止 capture 進程的觸發程式事件。</span><span class="sxs-lookup"><span data-stu-id="2ab2e-117">A trigger event that is set to stop the capture process.</span></span> <span data-ttu-id="2ab2e-118">Capture 觸發程式事件可以是暫時的捕獲檔案，該檔案會被導向至已捕捉到的框架中所發生的特定層級或資料模式。</span><span class="sxs-lookup"><span data-stu-id="2ab2e-118">The capture trigger event can be a temporary capture file that is directed to a specific level or data pattern that occurs in a captured frame.</span></span>

</dd> <dt>

<span data-ttu-id="2ab2e-119"><span id="_netmon_captured_data_gly"></span><span id="_NETMON_CAPTURED_DATA_GLY"></span>**已捕獲資料**</span><span class="sxs-lookup"><span data-stu-id="2ab2e-119"><span id="_netmon_captured_data_gly"></span><span id="_NETMON_CAPTURED_DATA_GLY"></span>**captured data**</span></span>
</dt> <dd>

<span data-ttu-id="2ab2e-120">具有一組已定義準則的框架。</span><span class="sxs-lookup"><span data-stu-id="2ab2e-120">Frames that have a defined set of criteria.</span></span> <span data-ttu-id="2ab2e-121">資料框架包含在暫時性的捕獲檔案中。</span><span class="sxs-lookup"><span data-stu-id="2ab2e-121">The data frames are contained in a temporary capture file.</span></span>

</dd> <dt>

<span data-ttu-id="2ab2e-122"><span id="_netmon_conversation_statistics_gly"></span><span id="_NETMON_CONVERSATION_STATISTICS_GLY"></span>**對話統計資料**</span><span class="sxs-lookup"><span data-stu-id="2ab2e-122"><span id="_netmon_conversation_statistics_gly"></span><span id="_NETMON_CONVERSATION_STATISTICS_GLY"></span>**conversation statistics**</span></span>
</dt> <dd>

<span data-ttu-id="2ab2e-123">在捕捉期間儲存的網路流量統計資料。</span><span class="sxs-lookup"><span data-stu-id="2ab2e-123">Statistics of network traffic saved during a capture.</span></span> <span data-ttu-id="2ab2e-124">這些統計資料包括捕捉程式啟動時開始的站和會話資訊，並且在捕捉停止時結束。</span><span class="sxs-lookup"><span data-stu-id="2ab2e-124">These statistics include station and session information beginning when the capture process starts, and ending when the capture stops.</span></span> <span data-ttu-id="2ab2e-125">如果您暫停捕捉程式，網路監視器會在繼續處理時繼續新增統計資料。</span><span class="sxs-lookup"><span data-stu-id="2ab2e-125">If you pause the capture process, Network Monitor continues to add statistics when you resume the process.</span></span> <span data-ttu-id="2ab2e-126">若要取得對話統計資料，請針對您所使用的介面呼叫 **GetConversationStatistics** 方法。</span><span class="sxs-lookup"><span data-stu-id="2ab2e-126">To retrieve conversation statistics, call the **GetConversationStatistics** method for the interface you are using.</span></span>

</dd> </dl>

 

 



