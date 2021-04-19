---
description: 在 WMI 基礎結構中， (Winmgmt) 的 WMI 服務是作業系統元件，可做為管理應用程式與 WMI 資料提供者之間的中繼程式。 WMI 存放庫是 WMI 相關靜態資料的儲存區域。
ms.assetid: 6ef157be-fb75-4453-bc20-4568a3dc18c0
ms.tgt_platform: multiple
title: WMI 基礎結構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4370af9ec062ffa845d54eafda054357a76dc07c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106996674"
---
# <a name="wmi-infrastructure"></a><span data-ttu-id="9c788-104">WMI 基礎結構</span><span class="sxs-lookup"><span data-stu-id="9c788-104">WMI Infrastructure</span></span>

<span data-ttu-id="9c788-105">在 WMI 基礎結構中， (Winmgmt) 的 WMI 服務是作業系統元件，可做為管理應用程式與 WMI 資料 [*提供者*](gloss-p.md)之間的中繼程式。</span><span class="sxs-lookup"><span data-stu-id="9c788-105">In the WMI infrastructure, the WMI service (Winmgmt) is the operating system component that acts as the mediator between management applications and WMI data [*providers*](gloss-p.md).</span></span> <span data-ttu-id="9c788-106">[*Wmi 存放庫*](gloss-w.md)是 wmi 相關靜態資料的儲存區域。</span><span class="sxs-lookup"><span data-stu-id="9c788-106">The [*WMI repository*](gloss-w.md) is a storage area for WMI-related static data.</span></span>

<span data-ttu-id="9c788-107">在 (SVCHOST) 的共用服務主機進程內，會將 WMI 服務實作為服務進程。</span><span class="sxs-lookup"><span data-stu-id="9c788-107">The WMI service is implemented as a service process within a shared service host process (SVCHOST).</span></span> <span data-ttu-id="9c788-108">如需詳細資訊，請參閱 [提供者裝載和安全性](provider-hosting-and-security.md)。</span><span class="sxs-lookup"><span data-stu-id="9c788-108">For more information, see [Provider Hosting and Security](provider-hosting-and-security.md).</span></span>

<span data-ttu-id="9c788-109">WMI 服務會在第一個管理應用程式或腳本呼叫以連接至 WMI 命名空間時啟動。</span><span class="sxs-lookup"><span data-stu-id="9c788-109">The WMI service starts when the first management application or script makes a call to connect to a WMI namespace.</span></span> <span data-ttu-id="9c788-110">視設定而定，當管理應用程式未呼叫 WMI 服務時，可能會關閉或進入記憶體不足的設定檔。</span><span class="sxs-lookup"><span data-stu-id="9c788-110">Depending on the setup, the WMI service may shut down or go into a low memory profile when not being called by a management application.</span></span>

<span data-ttu-id="9c788-111">WMI 服務會透過 COM 介面與管理應用程式互動。</span><span class="sxs-lookup"><span data-stu-id="9c788-111">The WMI service interacts with management applications through the COM interface.</span></span> <span data-ttu-id="9c788-112">當應用程式透過介面提出要求時，WMI 會判斷要求是否適用于靜態或動態資料。</span><span class="sxs-lookup"><span data-stu-id="9c788-112">When an application makes a request through the interface, WMI determines whether the request is for static or dynamic data.</span></span> <span data-ttu-id="9c788-113">如果要求牽涉到靜態資料，例如受管理物件的名稱，WMI 就會從存放庫中取出資料。</span><span class="sxs-lookup"><span data-stu-id="9c788-113">If the request involves static data, such as the name of a managed object, WMI retrieves the data from the repository.</span></span> <span data-ttu-id="9c788-114">如果要求牽涉到動態資料，例如受管理物件目前使用的記憶體數量，則 WMI 會將要求傳遞給提供者。</span><span class="sxs-lookup"><span data-stu-id="9c788-114">If the request involves dynamic data, such as the amount of memory a managed object is currently using, WMI passes the request on to a provider.</span></span>

<span data-ttu-id="9c788-115">提供者會向 WMI 服務註冊其位置，這可讓 WMI 路由傳送資料要求。</span><span class="sxs-lookup"><span data-stu-id="9c788-115">Providers register their location with the WMI service, which allows WMI to route data requests.</span></span> <span data-ttu-id="9c788-116">提供者也會註冊對特定作業的支援，例如資料抓取、修改、刪除、列舉或查詢處理。</span><span class="sxs-lookup"><span data-stu-id="9c788-116">A provider also registers support for particular operations, such as data retrieval, modification, deletion, enumeration, or query processing.</span></span> <span data-ttu-id="9c788-117">WMI 服務會使用提供者註冊資訊來比對應用程式要求與適當的提供者。</span><span class="sxs-lookup"><span data-stu-id="9c788-117">The WMI service uses the provider registration information to match application requests with the appropriate provider.</span></span> <span data-ttu-id="9c788-118">WMI 也會視需要使用註冊資訊來載入和卸載提供者。</span><span class="sxs-lookup"><span data-stu-id="9c788-118">WMI also uses the registration information to load and unload providers, as necessary.</span></span> <span data-ttu-id="9c788-119">當提供者完成處理要求時，提供者會將結果傳回給 WMI 服務。</span><span class="sxs-lookup"><span data-stu-id="9c788-119">When a provider finishes processing a request, the provider returns the result back to the WMI service.</span></span> <span data-ttu-id="9c788-120">WMI 接著會透過 COM 介面將結果轉送至應用程式。</span><span class="sxs-lookup"><span data-stu-id="9c788-120">WMI then forwards the result on to the application through the COM interface.</span></span> <span data-ttu-id="9c788-121">如需詳細資訊，請參閱 [將資料提供給 WMI](providing-data-to-wmi.md)。</span><span class="sxs-lookup"><span data-stu-id="9c788-121">For more information, see [Providing Data to WMI](providing-data-to-wmi.md).</span></span>

<span data-ttu-id="9c788-122">WMI 使用 [事件追蹤](/windows/desktop/ETW/event-tracing-portal) (ETW) 來記錄 WMI 服務活動。</span><span class="sxs-lookup"><span data-stu-id="9c788-122">WMI uses [Event Tracing](/windows/desktop/ETW/event-tracing-portal) (ETW) to record WMI service activity.</span></span>

<span data-ttu-id="9c788-123">由於基礎結構會處理提供者與管理應用程式之間的所有流量，因此基礎結構會提供下列功能：</span><span class="sxs-lookup"><span data-stu-id="9c788-123">Because the infrastructure handles all traffic between the providers and the management applications, the infrastructure provides the following features:</span></span>

-   <span data-ttu-id="9c788-124">事件通知支援</span><span class="sxs-lookup"><span data-stu-id="9c788-124">Event Notification Support</span></span>

    <span data-ttu-id="9c788-125">如需詳細資訊，請參閱 [監視事件](monitoring-events.md)。</span><span class="sxs-lookup"><span data-stu-id="9c788-125">For more information, see [Monitoring Events](monitoring-events.md).</span></span>

-   <span data-ttu-id="9c788-126">查詢語言支援</span><span class="sxs-lookup"><span data-stu-id="9c788-126">Query Language Support</span></span>

    <span data-ttu-id="9c788-127">如需詳細資訊，請參閱 [使用 WQL 查詢](querying-with-wql.md)。</span><span class="sxs-lookup"><span data-stu-id="9c788-127">For more information, see [Querying with WQL](querying-with-wql.md).</span></span>

-   <span data-ttu-id="9c788-128">安全性支援</span><span class="sxs-lookup"><span data-stu-id="9c788-128">Security Support</span></span>

    <span data-ttu-id="9c788-129">如需詳細資訊，請參閱 [維護 WMI 安全性](maintaining-wmi-security.md)。</span><span class="sxs-lookup"><span data-stu-id="9c788-129">For more information, see [Maintaining WMI Security](maintaining-wmi-security.md).</span></span>

-   <span data-ttu-id="9c788-130">腳本存取效能計數器資料</span><span class="sxs-lookup"><span data-stu-id="9c788-130">Scripting Access to Performance Counter Data</span></span>

    <span data-ttu-id="9c788-131">如需詳細資訊，請參閱 [監視效能資料](monitoring-performance-data.md)。</span><span class="sxs-lookup"><span data-stu-id="9c788-131">For more information, see [Monitoring Performance Data](monitoring-performance-data.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="9c788-132">相關主題</span><span class="sxs-lookup"><span data-stu-id="9c788-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9c788-133">WMI 架構</span><span class="sxs-lookup"><span data-stu-id="9c788-133">WMI Architecture</span></span>](wmi-architecture.md)
</dt> </dl>

 

 
