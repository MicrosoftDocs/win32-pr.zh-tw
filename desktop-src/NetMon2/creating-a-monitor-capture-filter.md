---
description: 建立可搭配網路監視器的捕獲篩選是五個步驟的程式。
ms.assetid: 04be791c-43c5-44c2-8ab0-799a99974bf6
title: 建立監視捕獲篩選
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 097a8276bd6a1f311b343787b3f06175d9b7091f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106986917"
---
# <a name="creating-a-monitor-capture-filter"></a><span data-ttu-id="223d3-103">建立監視捕獲篩選</span><span class="sxs-lookup"><span data-stu-id="223d3-103">Creating a Monitor Capture Filter</span></span>

<span data-ttu-id="223d3-104">建立可搭配網路監視器的捕獲篩選是五個步驟的程式：</span><span class="sxs-lookup"><span data-stu-id="223d3-104">Creating a capture filter that works with Network Monitor is a five-step process:</span></span>

-   [<span data-ttu-id="223d3-105">設定 Etype 或 SAP 篩選器</span><span class="sxs-lookup"><span data-stu-id="223d3-105">Setting the Etype or SAP Filter</span></span>](writing-etypesap-filter-portion.md)
-   [<span data-ttu-id="223d3-106">寫入 ADDRESSTABLE 篩選</span><span class="sxs-lookup"><span data-stu-id="223d3-106">Writing ADDRESSTABLE Filter</span></span>](writing-addresstable-filter-portion.md)
-   [<span data-ttu-id="223d3-107">撰寫 PATTERNMATCH 篩選</span><span class="sxs-lookup"><span data-stu-id="223d3-107">Writing the PATTERNMATCH Filter</span></span>](writing-the-patternmatch-filter.md)
-   [<span data-ttu-id="223d3-108">裁剪框架</span><span class="sxs-lookup"><span data-stu-id="223d3-108">Clipping a Frame</span></span>](clipping-a-frame.md)
-   [<span data-ttu-id="223d3-109">執行捕獲篩選器程式碼</span><span class="sxs-lookup"><span data-stu-id="223d3-109">Implementing the Capture Filter Code</span></span>](implementing-the-capture-filter-code.md)

<span data-ttu-id="223d3-110">「 [*捕獲篩選*](c.md) 」是一系列 NPP BLOB 的新增專案，可選取要傳回給監視器的畫面。</span><span class="sxs-lookup"><span data-stu-id="223d3-110">A [*capture filter*](c.md) is a series of additions to the NPP BLOB that selects which frames are passed back to the monitor.</span></span> <span data-ttu-id="223d3-111">如果監視未改變 NPP BLOB，則 NPP 會進入混合模式，並將所有網路流量傳送至監視器。</span><span class="sxs-lookup"><span data-stu-id="223d3-111">If a monitor does not alter the NPP BLOB, then the NPP will go into promiscuous mode and send all network traffic to the monitor.</span></span> <span data-ttu-id="223d3-112">如果 NPP 可以減少傳至驅動程式的資料，就能發揮最高效率，因此監視器應該建立一個 capture 篩選器。</span><span class="sxs-lookup"><span data-stu-id="223d3-112">The NPP is most efficient if it can reduce the data handed up to a driver, so a monitor should create a capture filter.</span></span> <span data-ttu-id="223d3-113">監視會藉由在 [DoConfigure](imonitor-doconfigure.md) 函式的呼叫中寫入 NPP BLOB 來設定其捕捉篩選。</span><span class="sxs-lookup"><span data-stu-id="223d3-113">A monitor sets its capture filter by writing to the NPP BLOB in the call to the [DoConfigure](imonitor-doconfigure.md) function.</span></span> <span data-ttu-id="223d3-114">然後，MCSVC 會使用 NPP BLOB 來呼叫 NPP。</span><span class="sxs-lookup"><span data-stu-id="223d3-114">The MCSVC then calls the NPP with the NPP BLOB.</span></span> <span data-ttu-id="223d3-115">如需有關 capture 篩選器、NPPs 上的[網路封包提供者](network-packet-providers.md)，以及 blob 函式上[網路監視器 blob](network-monitor-blobs.md)的詳細資訊，請參閱「取得[篩選](capture-filters.md)」。</span><span class="sxs-lookup"><span data-stu-id="223d3-115">See [Capture Filters](capture-filters.md) for more details on the capture filter, [Network Packet Providers](network-packet-providers.md) on NPPs, and [Network Monitor Blobs](network-monitor-blobs.md) on BLOB functions.</span></span>

 

 



