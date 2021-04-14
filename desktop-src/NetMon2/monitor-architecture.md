---
description: 下圖顯示監視器與網路監視器架構的其他元件之間的關聯性。
ms.assetid: cbd6116c-1a95-4ac4-bc79-632ebe198197
title: 監視架構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38c1a36ef19933d888f27079d8d94ddba16bde79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104568628"
---
# <a name="monitor-architecture"></a><span data-ttu-id="22c8d-103">監視架構</span><span class="sxs-lookup"><span data-stu-id="22c8d-103">Monitor Architecture</span></span>

<span data-ttu-id="22c8d-104">下圖顯示 [*監視器*](m.md) 與網路監視器架構的其他元件之間的關聯性。</span><span class="sxs-lookup"><span data-stu-id="22c8d-104">The following figure shows the relationship between [*monitors*](m.md) and other components of the Network Monitor architecture.</span></span>

![監視器與網路監視器的其他元件之間的關聯性](images/nmarch2.png)

<span data-ttu-id="22c8d-106">從 NDIS 驅動程式) 的個別畫面格 (收集網路流量。</span><span class="sxs-lookup"><span data-stu-id="22c8d-106">The network traffic is collected (as individual frames) from the NDIS driver.</span></span> <span data-ttu-id="22c8d-107">網路監視器驅動程式 (Nmnt.sys) 接著將框架路由傳送到網路封包提供者 (NPP) ，進而在即時模式中捕獲資料。</span><span class="sxs-lookup"><span data-stu-id="22c8d-107">The Network Monitor driver (Nmnt.sys) then routes the frames to a network packet provider (NPP), which in turn captures the data in real-time mode.</span></span> <span data-ttu-id="22c8d-108">NPP 是用來捕捉資料的 COM 介面集合。</span><span class="sxs-lookup"><span data-stu-id="22c8d-108">The NPP is a collection of COM interfaces used to capture data.</span></span> <span data-ttu-id="22c8d-109">在此情況下， [**IRTC**](irtc.md) 介面會用來執行即時捕捉。</span><span class="sxs-lookup"><span data-stu-id="22c8d-109">In this case, the [**IRTC**](irtc.md) interface is used to perform a real-time capture.</span></span>

> [!Note]  
> <span data-ttu-id="22c8d-110">NPP 用於延遲和即時的捕獲。</span><span class="sxs-lookup"><span data-stu-id="22c8d-110">The NPP is used for delayed and real-time captures.</span></span> <span data-ttu-id="22c8d-111">若為專家和剖析器所使用的延遲捕捉，則會使用 [**IDelaydC**](idelaydc.md) 介面。</span><span class="sxs-lookup"><span data-stu-id="22c8d-111">For delayed captures used by experts and parsers, the [**IDelaydC**](idelaydc.md) interface is used.</span></span>

 

<span data-ttu-id="22c8d-112">然後，監視器會以即時模式檢查捕捉的資料、偵測特定的網路狀況，並視需要產生事件。</span><span class="sxs-lookup"><span data-stu-id="22c8d-112">The monitor then examines the captured data in real-time mode, detecting specific network conditions and generating events as required.</span></span>

<span data-ttu-id="22c8d-113">監視器應用程式會使用其他三個元件：監視器控制工具、監視器控制服務 (MCSVC) 和事件檢視器：</span><span class="sxs-lookup"><span data-stu-id="22c8d-113">Three other components are used by monitor applications: the Monitor Control Tool, the Monitor Control Service (MCSVC), and the Event Viewer:</span></span>

-   <span data-ttu-id="22c8d-114">監視器控制工具是用來管理您的監視器應用程式。</span><span class="sxs-lookup"><span data-stu-id="22c8d-114">The Monitor Control Tool is used to manage your monitor applications.</span></span> <span data-ttu-id="22c8d-115">這包括設定和執行所有的監視器應用程式。</span><span class="sxs-lookup"><span data-stu-id="22c8d-115">This includes configuring and running all your monitor applications.</span></span>
-   <span data-ttu-id="22c8d-116">監視器控制服務 (MCSVC) 引發事件、提供 WMI 的通訊連結以進行事件的查看，以及協調監視作業的處理。</span><span class="sxs-lookup"><span data-stu-id="22c8d-116">The Monitor Control Service (MCSVC) fires events, provides a communications link to WMI for event viewing, and coordinates the processing of monitor operations.</span></span>
-   <span data-ttu-id="22c8d-117">事件檢視器會顯示監視器控制服務所引發的事件。</span><span class="sxs-lookup"><span data-stu-id="22c8d-117">The Event Viewer displays the events fired by the Monitor Control Service.</span></span>

## <a name="related-topics"></a><span data-ttu-id="22c8d-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="22c8d-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="22c8d-119">**IMonitor**</span><span class="sxs-lookup"><span data-stu-id="22c8d-119">**IMonitor**</span></span>](imonitor.md)
</dt> <dt>

[<span data-ttu-id="22c8d-120">**IMonitorEventer**</span><span class="sxs-lookup"><span data-stu-id="22c8d-120">**IMonitorEventer**</span></span>](imonitoreventer.md)
</dt> <dt>

[<span data-ttu-id="22c8d-121">**IRTC**</span><span class="sxs-lookup"><span data-stu-id="22c8d-121">**IRTC**</span></span>](irtc.md)
</dt> </dl>

 

 



