---
description: .
ms.assetid: 49bdfdfa-c77e-4a57-8079-bf4ff6b5010b
title: Microsoft Message Queuing (MSMQ) 改善的佇列處理
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffcc566c4c4ea461fdd9c4634b26ff69f239f03e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944454"
---
# <a name="microsoft-message-queuing-msmq---improved-queue-handling"></a><span data-ttu-id="eecf9-103">Microsoft Message Queuing (MSMQ) 改善的佇列處理</span><span class="sxs-lookup"><span data-stu-id="eecf9-103">Microsoft Message Queuing (MSMQ) - Improved Queue Handling</span></span>

## <a name="platforms"></a><span data-ttu-id="eecf9-104">平台</span><span class="sxs-lookup"><span data-stu-id="eecf9-104">Platforms</span></span>

<span data-ttu-id="eecf9-105">**客戶** 端-Windows 7</span><span class="sxs-lookup"><span data-stu-id="eecf9-105">**Clients** - Windows 7</span></span>  
<span data-ttu-id="eecf9-106">**伺服器** -Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="eecf9-106">**Servers** - Windows Server 2008 R2</span></span>  









## <a name="feature-impact"></a><span data-ttu-id="eecf9-107">功能影響</span><span class="sxs-lookup"><span data-stu-id="eecf9-107">Feature Impact</span></span>

 <span data-ttu-id="eecf9-108">**嚴重性** -低</span><span class="sxs-lookup"><span data-stu-id="eecf9-108">**Severity** - Low</span></span>  
<span data-ttu-id="eecf9-109">**頻率** -低</span><span class="sxs-lookup"><span data-stu-id="eecf9-109">**Frequency** - Low</span></span>  





## <a name="description"></a><span data-ttu-id="eecf9-110">Description</span><span class="sxs-lookup"><span data-stu-id="eecf9-110">Description</span></span>

<span data-ttu-id="eecf9-111">MSMQ 服務不會對可在系統上建立的佇列數目施加硬性限制。</span><span class="sxs-lookup"><span data-stu-id="eecf9-111">MSMQ Service does not put a hard limit on the number of queues that can be created on a system.</span></span> <span data-ttu-id="eecf9-112">但是，當建立大量的佇列時，系統的效能會受到影響。</span><span class="sxs-lookup"><span data-stu-id="eecf9-112">However, the performance of the system is impacted when a large number of queues is created.</span></span> <span data-ttu-id="eecf9-113">具體來說，當有超過一千個佇列時，MSMQ 服務的啟動時間會以指數方式增加，而產生明顯的影響。</span><span class="sxs-lookup"><span data-stu-id="eecf9-113">Specifically, when there are more than a few thousand queues, the start-up time of the MSMQ Service increases exponentially resulting in a visible impact.</span></span>

<span data-ttu-id="eecf9-114">Microsoft 已將 Windows 7 中的 MSMQ 服務優化，以降低將佇列載入至記憶體的查閱負荷。</span><span class="sxs-lookup"><span data-stu-id="eecf9-114">Microsoft has optimized the MSMQ Service start-up in Windows 7 to reduce the lookup overhead for loading the queues into memory.</span></span> <span data-ttu-id="eecf9-115">即使在系統中建立了數千個佇列，這項優化也導致 MSMQ 服務的啟動時間大幅改進。</span><span class="sxs-lookup"><span data-stu-id="eecf9-115">This optimization has led to a dramatic improvement of the start-up time of the MSMQ Service even when several thousand queues are created in the system.</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="eecf9-116">影響的表現</span><span class="sxs-lookup"><span data-stu-id="eecf9-116">Manifestation of Impact</span></span>

<span data-ttu-id="eecf9-117">這項效能改進不會影響任何現有應用程式的功能。</span><span class="sxs-lookup"><span data-stu-id="eecf9-117">This performance improvement does not impact the functionality of any existing application.</span></span>

## <a name="leveraging-the-changed-feature"></a><span data-ttu-id="eecf9-118">利用變更的功能</span><span class="sxs-lookup"><span data-stu-id="eecf9-118">Leveraging the Changed Feature</span></span>

<span data-ttu-id="eecf9-119">在 Windows 7 上使用 MSMQ 的應用程式開發人員現在可以建立其解決方案的架構，而不會限制佇列數目。</span><span class="sxs-lookup"><span data-stu-id="eecf9-119">Application developers using MSMQ on Windows 7 can now architect their solutions without limiting the number of queues.</span></span> <span data-ttu-id="eecf9-120">請注意，佇列的數目仍會影響 MSMQ 伺服器的整體效能，但效能影響現在是以線性而非指數的比例進行。</span><span class="sxs-lookup"><span data-stu-id="eecf9-120">Note that the number of queues still affects overall performance of the MSMQ Server, but the performance impact is now on a linear rather than exponential scale.</span></span>

## <a name="compatibility-performance-reliability-and-usability-tests"></a><span data-ttu-id="eecf9-121">相容性、效能、可靠性和可用性測試</span><span class="sxs-lookup"><span data-stu-id="eecf9-121">Compatibility, Performance, Reliability, and Usability Tests</span></span>

<span data-ttu-id="eecf9-122">如果您使用大量的佇列，請在測試平臺上模擬生產環境、監視效能，以及分析服務的啟動時間，以及在測試系統中出現大量佇列和訊息的訊息輸送量。</span><span class="sxs-lookup"><span data-stu-id="eecf9-122">If you use a large number of queues, simulate the production environment on a test bed, monitor performance, and analyze the service start-up time and the message throughput with a large number of queues and messages present in the test system.</span></span>

 

 



