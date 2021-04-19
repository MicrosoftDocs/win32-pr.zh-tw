---
description: 服務控制管理員 (SCM) 會在系統開機時啟動。 這是 (RPC) server 的遠端程序呼叫，因此服務設定和服務控制程式都可以操作遠端電腦上的服務。
ms.assetid: 56ad011d-17c4-4410-b598-6ef47fb3638f
title: 服務控制管理員
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a8a35fd34bd2714d22d40ccf618c89a8b66a6c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973445"
---
# <a name="service-control-manager"></a><span data-ttu-id="4b33e-104">服務控制管理員</span><span class="sxs-lookup"><span data-stu-id="4b33e-104">Service Control Manager</span></span>

<span data-ttu-id="4b33e-105">服務控制管理員 (SCM) 會在系統開機時啟動。</span><span class="sxs-lookup"><span data-stu-id="4b33e-105">The service control manager (SCM) is started at system boot.</span></span> <span data-ttu-id="4b33e-106">這是 (RPC) server 的遠端程序呼叫，因此服務設定和服務控制程式都可以操作遠端電腦上的服務。</span><span class="sxs-lookup"><span data-stu-id="4b33e-106">It is a remote procedure call (RPC) server, so that service configuration and service control programs can manipulate services on remote machines.</span></span>

<span data-ttu-id="4b33e-107">服務函式會為 SCM 所執行的下列工作提供介面：</span><span class="sxs-lookup"><span data-stu-id="4b33e-107">The service functions provide an interface for the following tasks performed by the SCM:</span></span>

-   <span data-ttu-id="4b33e-108">維護已安裝服務的資料庫。</span><span class="sxs-lookup"><span data-stu-id="4b33e-108">Maintaining the database of installed services.</span></span>
-   <span data-ttu-id="4b33e-109">在系統啟動時或依需求啟動服務和驅動程式服務。</span><span class="sxs-lookup"><span data-stu-id="4b33e-109">Starting services and driver services either upon system startup or upon demand.</span></span>
-   <span data-ttu-id="4b33e-110">列舉已安裝的服務和驅動程式服務。</span><span class="sxs-lookup"><span data-stu-id="4b33e-110">Enumerating installed services and driver services.</span></span>
-   <span data-ttu-id="4b33e-111">維護執行中服務和驅動程式服務的狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="4b33e-111">Maintaining status information for running services and driver services.</span></span>
-   <span data-ttu-id="4b33e-112">將控制要求傳送至執行中的服務。</span><span class="sxs-lookup"><span data-stu-id="4b33e-112">Transmitting control requests to running services.</span></span>
-   <span data-ttu-id="4b33e-113">鎖定和解除鎖定服務資料庫。</span><span class="sxs-lookup"><span data-stu-id="4b33e-113">Locking and unlocking the service database.</span></span>

<span data-ttu-id="4b33e-114">下列各節將更詳細地說明 SCM：</span><span class="sxs-lookup"><span data-stu-id="4b33e-114">The following sections describe the SCM in more detail:</span></span>

-   [<span data-ttu-id="4b33e-115">已安裝服務的資料庫</span><span class="sxs-lookup"><span data-stu-id="4b33e-115">Database of Installed Services</span></span>](database-of-installed-services.md)
-   [<span data-ttu-id="4b33e-116">自動啟動服務</span><span class="sxs-lookup"><span data-stu-id="4b33e-116">Automatically Starting Services</span></span>](automatically-starting-services.md)
-   [<span data-ttu-id="4b33e-117">依需求啟動服務</span><span class="sxs-lookup"><span data-stu-id="4b33e-117">Starting Services on Demand</span></span>](starting-services-on-demand.md)
-   [<span data-ttu-id="4b33e-118">服務記錄清單</span><span class="sxs-lookup"><span data-stu-id="4b33e-118">Service Record List</span></span>](service-record-list.md)
-   [<span data-ttu-id="4b33e-119">SCM 控制碼</span><span class="sxs-lookup"><span data-stu-id="4b33e-119">SCM Handles</span></span>](scm-handles.md)

 

 



