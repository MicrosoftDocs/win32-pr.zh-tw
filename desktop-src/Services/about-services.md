---
description: 服務控制管理員 (SCM) 維護已安裝之服務和驅動程式服務的資料庫，並提供統一且安全的方式來控制它們。
ms.assetid: a3af8340-d367-417b-9759-7282edf1d694
title: 關於服務
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87aeec6dfcdc4e2dc0cc0ab3ef084b7927b2c3bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944613"
---
# <a name="about-services"></a><span data-ttu-id="35995-103">關於服務</span><span class="sxs-lookup"><span data-stu-id="35995-103">About Services</span></span>

<span data-ttu-id="35995-104">[服務控制管理員](service-control-manager.md) (SCM) 維護已安裝之服務和驅動程式服務的資料庫，並提供統一且安全的方式來控制它們。</span><span class="sxs-lookup"><span data-stu-id="35995-104">The [service control manager](service-control-manager.md) (SCM) maintains a database of installed services and driver services, and provides a unified and secure means of controlling them.</span></span> <span data-ttu-id="35995-105">資料庫包含每個服務或驅動程式服務應如何啟動的資訊。</span><span class="sxs-lookup"><span data-stu-id="35995-105">The database includes information on how each service or driver service should be started.</span></span> <span data-ttu-id="35995-106">它也可讓系統管理員自訂每個服務的安全性需求，進而控制服務的存取。</span><span class="sxs-lookup"><span data-stu-id="35995-106">It also enables system administrators to customize security requirements for each service and thereby control access to the service.</span></span>

<span data-ttu-id="35995-107">下列類型的程式會使用 SCM 提供的函式。</span><span class="sxs-lookup"><span data-stu-id="35995-107">The following types of programs use the functions provided by the SCM.</span></span>



| <span data-ttu-id="35995-108">類型</span><span class="sxs-lookup"><span data-stu-id="35995-108">Type</span></span>                          | <span data-ttu-id="35995-109">Description</span><span class="sxs-lookup"><span data-stu-id="35995-109">Description</span></span>                                                                                                                                                                                                                                                                                                                               |
|-------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35995-110">服務方案</span><span class="sxs-lookup"><span data-stu-id="35995-110">Service program</span></span>               | <span data-ttu-id="35995-111">為一或多個服務提供可執行程式碼的程式。</span><span class="sxs-lookup"><span data-stu-id="35995-111">A program that provides executable code for one or more services.</span></span> <span data-ttu-id="35995-112">服務程式會使用連接至 SCM 的函式，並將狀態資訊傳送至 SCM。</span><span class="sxs-lookup"><span data-stu-id="35995-112">Service programs use functions that connect to the SCM and send status information to the SCM.</span></span>                                                                                                                                                                          |
| <span data-ttu-id="35995-113">服務設定計劃</span><span class="sxs-lookup"><span data-stu-id="35995-113">Service configuration program</span></span> | <span data-ttu-id="35995-114">查詢或修改服務資料庫的程式。</span><span class="sxs-lookup"><span data-stu-id="35995-114">A program that queries or modifies the services database.</span></span> <span data-ttu-id="35995-115">服務設定程式使用的函式會開啟資料庫、安裝或刪除資料庫中的服務，以及查詢或修改已安裝服務的設定和安全性參數。</span><span class="sxs-lookup"><span data-stu-id="35995-115">Service configuration programs use functions that open the database, install or delete services in the database, and query or modify the configuration and security parameters for installed services.</span></span> <span data-ttu-id="35995-116">服務設定程式會同時管理服務和驅動程式服務。</span><span class="sxs-lookup"><span data-stu-id="35995-116">Service configuration programs manage both services and driver services.</span></span> |
| <span data-ttu-id="35995-117">服務控制程式</span><span class="sxs-lookup"><span data-stu-id="35995-117">Service control program</span></span>       | <span data-ttu-id="35995-118">啟動及控制服務和驅動程式服務的程式。</span><span class="sxs-lookup"><span data-stu-id="35995-118">A program that starts and controls services and driver services.</span></span> <span data-ttu-id="35995-119">服務控制程式會使用將要求傳送至 SCM 的函式，這會執行要求。</span><span class="sxs-lookup"><span data-stu-id="35995-119">Service control programs use functions that send requests to the SCM, which carries out the request.</span></span>                                                                                                                                                                     |



 

<span data-ttu-id="35995-120">本總覽將討論下列主題：</span><span class="sxs-lookup"><span data-stu-id="35995-120">This overview discusses the following topics:</span></span>

-   [<span data-ttu-id="35995-121">服務控制管理員</span><span class="sxs-lookup"><span data-stu-id="35995-121">Service Control Manager</span></span>](service-control-manager.md)
-   [<span data-ttu-id="35995-122">服務程式</span><span class="sxs-lookup"><span data-stu-id="35995-122">Service Programs</span></span>](service-programs.md)
-   [<span data-ttu-id="35995-123">服務設定程式</span><span class="sxs-lookup"><span data-stu-id="35995-123">Service Configuration Programs</span></span>](service-configuration-programs.md)
-   [<span data-ttu-id="35995-124">服務控制程式</span><span class="sxs-lookup"><span data-stu-id="35995-124">Service Control Programs</span></span>](service-control-programs.md)
-   [<span data-ttu-id="35995-125">服務使用者帳戶</span><span class="sxs-lookup"><span data-stu-id="35995-125">Service User Accounts</span></span>](service-user-accounts.md)
-   [<span data-ttu-id="35995-126">互動式服務</span><span class="sxs-lookup"><span data-stu-id="35995-126">Interactive Services</span></span>](interactive-services.md)
-   [<span data-ttu-id="35995-127">服務安全性與存取權限</span><span class="sxs-lookup"><span data-stu-id="35995-127">Service Security and Access Rights</span></span>](service-security-and-access-rights.md)
-   [<span data-ttu-id="35995-128">對服務進行偵錯</span><span class="sxs-lookup"><span data-stu-id="35995-128">Debugging a Service</span></span>](debugging-a-service.md)
-   [<span data-ttu-id="35995-129">服務觸發程式事件</span><span class="sxs-lookup"><span data-stu-id="35995-129">Service Trigger Events</span></span>](service-trigger-events.md)

 

 



