---
description: 開機事件收集器 WMI 提供者可讓您存取 Windows Server 上的設定和開機事件集合功能的連接和設定資訊。
ms.assetid: ab9ac8f0-69a5-4a2d-8ee5-1f003aa1bb5b
ms.tgt_platform: multiple
title: 開機事件收集器 WMI 提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a38ef27b2989f856fdcfda82d4ee0e68c3913167
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103846976"
---
# <a name="boot-event-collector-wmi-provider"></a><span data-ttu-id="756d1-103">開機事件收集器 WMI 提供者</span><span class="sxs-lookup"><span data-stu-id="756d1-103">Boot Event Collector WMI Provider</span></span>

## <a name="purpose"></a><span data-ttu-id="756d1-104">目的</span><span class="sxs-lookup"><span data-stu-id="756d1-104">Purpose</span></span>

<span data-ttu-id="756d1-105">開機事件收集器 WMI 提供者可讓您存取 Windows Server 上的設定和開機事件集合功能的連接和設定資訊。</span><span class="sxs-lookup"><span data-stu-id="756d1-105">The Boot Event Collector WMI provider provides access to connection and configuration information for the Setup and Boot Event Collection feature on Windows Server.</span></span> <span data-ttu-id="756d1-106">這可讓您查看目前的連接清單，以及收集器伺服器與其目的電腦之間的連接歷程記錄。</span><span class="sxs-lookup"><span data-stu-id="756d1-106">This allows you to view a list of the current connections and the connection history between a collector server and its target computers.</span></span> <span data-ttu-id="756d1-107">此外，此提供者可讓您管理收集器伺服器的設定。</span><span class="sxs-lookup"><span data-stu-id="756d1-107">In addition, this provider allows you to manage the configuration of a collector server.</span></span>

> [!Note]  
> <span data-ttu-id="756d1-108">開機事件收集器 WMI 提供者會在 BEvtCol.exe 中執行。</span><span class="sxs-lookup"><span data-stu-id="756d1-108">The Boot Event Collector WMI provider is implemented in BEvtCol.exe.</span></span>

 

## <a name="in-this-section"></a><span data-ttu-id="756d1-109">本節內容</span><span class="sxs-lookup"><span data-stu-id="756d1-109">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="756d1-110">**TargetForwarding**</span><span class="sxs-lookup"><span data-stu-id="756d1-110">**TargetForwarding**</span></span>](targetforwarding.md)
</dt> <dd>

<span data-ttu-id="756d1-111">從目的電腦抓取轉送資料。</span><span class="sxs-lookup"><span data-stu-id="756d1-111">Retrieves forwarding data from a target computer.</span></span>

</dd> <dt>

[<span data-ttu-id="756d1-112">**TargetForwardingDestination**</span><span class="sxs-lookup"><span data-stu-id="756d1-112">**TargetForwardingDestination**</span></span>](targetforwardingdestination.md)
</dt> <dd>

<span data-ttu-id="756d1-113">包含所收集資料的已知目的地。</span><span class="sxs-lookup"><span data-stu-id="756d1-113">The known destinations containing the collected data.</span></span> <span data-ttu-id="756d1-114">只有在收集器在啟用狀態記錄檔的情況下才可使用。</span><span class="sxs-lookup"><span data-stu-id="756d1-114">Available only if the collector is running with the status log enabled.</span></span>

</dd> <dt>

[<span data-ttu-id="756d1-115">**TargetForwardingHistory**</span><span class="sxs-lookup"><span data-stu-id="756d1-115">**TargetForwardingHistory**</span></span>](targetforwardinghistory.md)
</dt> <dd>

<span data-ttu-id="756d1-116">目的電腦轉送資料變更的最近歷程記錄。</span><span class="sxs-lookup"><span data-stu-id="756d1-116">The recent history of changes to the forwarding data for a target computer.</span></span>

</dd> <dt>

[<span data-ttu-id="756d1-117">**控制**</span><span class="sxs-lookup"><span data-stu-id="756d1-117">**Control**</span></span>](control.md)
</dt> <dd>

<span data-ttu-id="756d1-118">收集器實例的控制權。</span><span class="sxs-lookup"><span data-stu-id="756d1-118">Control of the collector instance.</span></span> <span data-ttu-id="756d1-119">需要系統管理員 (BA) 許可權。</span><span class="sxs-lookup"><span data-stu-id="756d1-119">Requires the Administrator (BA) privileges.</span></span>

</dd> </dl>

 

 



