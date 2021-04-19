---
description: Windows 7 和 Windows Server 2008 R2 包含服務的下列全新和更新的程式設計項目。
ms.assetid: 4be7e244-ad4c-440d-b04e-23afb4c7ddf2
title: 適用于 Windows 7 的服務有哪些新功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51bd2e8bfa5426447e24485ed026f27e90fdcaa1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106990444"
---
# <a name="whats-new-in-services-for-windows-7"></a><span data-ttu-id="01871-103">Windows 7 服務的新功能</span><span class="sxs-lookup"><span data-stu-id="01871-103">What's New in Services for Windows 7</span></span>

<span data-ttu-id="01871-104">Windows 7 和 Windows Server 2008 R2 包含服務的下列全新和更新的程式設計項目。</span><span class="sxs-lookup"><span data-stu-id="01871-104">Windows 7 and Windows Server 2008 R2 include the following new and updated programming elements for services.</span></span>

## <a name="new-capabilities"></a><span data-ttu-id="01871-105">新功能</span><span class="sxs-lookup"><span data-stu-id="01871-105">New Capabilities</span></span>

<span data-ttu-id="01871-106">當觸發程式事件發生時，可以註冊以啟動或停止服務。</span><span class="sxs-lookup"><span data-stu-id="01871-106">A service can register to be started or stopped when a trigger event occurs.</span></span> <span data-ttu-id="01871-107">這樣就不需要在系統啟動時啟動服務，或讓服務輪詢或主動等候事件;服務可以在需要時啟動，而不是在是否有要執行的工作時自動啟動。</span><span class="sxs-lookup"><span data-stu-id="01871-107">This eliminates the need for services to start when the system starts, or for services to poll or actively wait for an event; a service can start when it is needed, instead of starting automatically whether or not there is work to do.</span></span> <span data-ttu-id="01871-108">如需詳細資訊，請參閱 [服務觸發程式事件](service-trigger-events.md)。</span><span class="sxs-lookup"><span data-stu-id="01871-108">For more information, see [Service Trigger Events](service-trigger-events.md).</span></span>

## <a name="updated-functions"></a><span data-ttu-id="01871-109">已更新函式</span><span class="sxs-lookup"><span data-stu-id="01871-109">Updated Functions</span></span>



| <span data-ttu-id="01871-110">函式</span><span class="sxs-lookup"><span data-stu-id="01871-110">Function</span></span>                                                        | <span data-ttu-id="01871-111">描述</span><span class="sxs-lookup"><span data-stu-id="01871-111">Description</span></span>                                                                                                                                                                                                                                                                                |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="01871-112">**ChangeServiceConfig**</span><span class="sxs-lookup"><span data-stu-id="01871-112">**ChangeServiceConfig**</span></span>](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga)<br/>   | <span data-ttu-id="01871-113">變更服務的設定參數。</span><span class="sxs-lookup"><span data-stu-id="01871-113">Changes the configuration parameters of a service.</span></span> <span data-ttu-id="01871-114">此函數支援受管理的服務帳戶和虛擬帳戶。</span><span class="sxs-lookup"><span data-stu-id="01871-114">This function supports managed service accounts and virtual accounts.</span></span> <span data-ttu-id="01871-115">如需詳細資訊，請參閱 [服務帳戶的逐步指南](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/dd548356(v=ws.10))。</span><span class="sxs-lookup"><span data-stu-id="01871-115">For more information, see [Service Accounts Step-by-Step Guide](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/dd548356(v=ws.10)).</span></span><br/>                                      |
| [<span data-ttu-id="01871-116">**ChangeServiceConfig2**</span><span class="sxs-lookup"><span data-stu-id="01871-116">**ChangeServiceConfig2**</span></span>](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a)<br/> | <span data-ttu-id="01871-117">變更服務的選擇性設定參數。</span><span class="sxs-lookup"><span data-stu-id="01871-117">Changes the optional configuration parameters of a service.</span></span> <span data-ttu-id="01871-118">此函數支援處理器群組和服務觸發程式事件的新設定資訊層級。</span><span class="sxs-lookup"><span data-stu-id="01871-118">This function supports new configuration information levels for processor groups and service trigger events.</span></span><br/>                                                                                                        |
| [<span data-ttu-id="01871-119">**CreateService**</span><span class="sxs-lookup"><span data-stu-id="01871-119">**CreateService**</span></span>](/windows/desktop/api/Winsvc/nf-winsvc-createservicea)<br/>               | <span data-ttu-id="01871-120">建立服務物件，並將它加入至指定的服務控制管理員資料庫。</span><span class="sxs-lookup"><span data-stu-id="01871-120">Creates a service object and adds it to the specified service control manager database.</span></span> <span data-ttu-id="01871-121">此函數支援受管理的服務帳戶和虛擬帳戶。</span><span class="sxs-lookup"><span data-stu-id="01871-121">This function supports managed service accounts and virtual accounts.</span></span> <span data-ttu-id="01871-122">如需詳細資訊，請參閱 [服務帳戶的逐步指南](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/dd548356(v=ws.10))。</span><span class="sxs-lookup"><span data-stu-id="01871-122">For more information, see [Service Accounts Step-by-Step Guide](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/dd548356(v=ws.10)).</span></span><br/> |
| [<span data-ttu-id="01871-123">**HandlerEx**</span><span class="sxs-lookup"><span data-stu-id="01871-123">**HandlerEx**</span></span>](/windows/desktop/api/WinSvc/nc-winsvc-lphandler_function_ex)<br/>                       | <span data-ttu-id="01871-124">搭配 [**RegisterServiceCtrlHandlerEx**](/windows/desktop/api/Winsvc/nf-winsvc-registerservicectrlhandlerexa) 函式使用的應用程式定義回呼函數。</span><span class="sxs-lookup"><span data-stu-id="01871-124">An application-defined callback function used with the [**RegisterServiceCtrlHandlerEx**](/windows/desktop/api/Winsvc/nf-winsvc-registerservicectrlhandlerexa) function.</span></span> <span data-ttu-id="01871-125">這個回呼函式支援對系統時間變更和服務觸發程式事件進行新的擴充控制程式代碼。</span><span class="sxs-lookup"><span data-stu-id="01871-125">This callback function supports new extended control codes for system time changes and service trigger events.</span></span><br/>                            |
| [<span data-ttu-id="01871-126">**QueryServiceConfig2**</span><span class="sxs-lookup"><span data-stu-id="01871-126">**QueryServiceConfig2**</span></span>](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfig2a)<br/>   | <span data-ttu-id="01871-127">抓取服務的選擇性設定參數。</span><span class="sxs-lookup"><span data-stu-id="01871-127">Retrieves the optional configuration parameters of a service.</span></span> <span data-ttu-id="01871-128">此函數支援處理器群組和服務觸發程式事件的新設定資訊層級。</span><span class="sxs-lookup"><span data-stu-id="01871-128">This function supports new configuration information levels for processor groups and service trigger events.</span></span><br/>                                                                                                      |
| [<span data-ttu-id="01871-129">**>setservicestatus**</span><span class="sxs-lookup"><span data-stu-id="01871-129">**SetServiceStatus**</span></span>](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus)<br/>         | <span data-ttu-id="01871-130">更新呼叫服務的服務控制管理員的狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="01871-130">Updates the service control manager's status information for the calling service.</span></span> <span data-ttu-id="01871-131">此函式支援系統時間變更和服務觸發程式事件的新擴充控制程式代碼。</span><span class="sxs-lookup"><span data-stu-id="01871-131">This function supports new extended control codes for system time changes and service trigger events.</span></span><br/>                                                                                         |



 

## <a name="new-structures"></a><span data-ttu-id="01871-132">新結構</span><span class="sxs-lookup"><span data-stu-id="01871-132">New Structures</span></span>



| <span data-ttu-id="01871-133">結構</span><span class="sxs-lookup"><span data-stu-id="01871-133">Structure</span></span>                                                                                       | <span data-ttu-id="01871-134">Description</span><span class="sxs-lookup"><span data-stu-id="01871-134">Description</span></span>                                                            |
|-------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="01871-135">**服務 \_ TIMECHANGE \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="01871-135">**SERVICE\_TIMECHANGE\_INFO**</span></span>](/windows/desktop/api/winsvc/ns-winsvc-service_timechange_info)<br/>                         | <span data-ttu-id="01871-136">包含系統時間變更設定。</span><span class="sxs-lookup"><span data-stu-id="01871-136">Contains system time change settings.</span></span> <br/>                      |
| [<span data-ttu-id="01871-137">**服務 \_ 觸發程式**</span><span class="sxs-lookup"><span data-stu-id="01871-137">**SERVICE\_TRIGGER**</span></span>](/windows/desktop/api/winsvc/ns-winsvc-service_trigger)<br/>                                          | <span data-ttu-id="01871-138">表示服務觸發程式事件。</span><span class="sxs-lookup"><span data-stu-id="01871-138">Represents a service trigger event.</span></span><br/>                         |
| [<span data-ttu-id="01871-139">**服務 \_ 觸發程式 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="01871-139">**SERVICE\_TRIGGER\_INFO**</span></span>](/windows/desktop/api/winsvc/ns-winsvc-service_trigger_info)<br/>                               | <span data-ttu-id="01871-140">包含服務的觸發程式事件資訊。</span><span class="sxs-lookup"><span data-stu-id="01871-140">Contains trigger event information for a service.</span></span><br/>           |
| [<span data-ttu-id="01871-141">**服務 \_ 觸發程式的 \_ 特定 \_ 資料項目 \_**</span><span class="sxs-lookup"><span data-stu-id="01871-141">**SERVICE\_TRIGGER\_SPECIFIC\_DATA\_ITEM**</span></span>](/windows/desktop/api/winsvc/ns-winsvc-service_trigger_specific_data_item)<br/> | <span data-ttu-id="01871-142">包含服務觸發程式事件的觸發程式特定資料。</span><span class="sxs-lookup"><span data-stu-id="01871-142">Contains trigger-specific data for a service trigger event.</span></span><br/> |



 

 

