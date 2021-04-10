---
description: SCM 會在登錄中維護已安裝服務的資料庫。
ms.assetid: 70f24e15-2607-4c32-9192-a9413b74558b
title: 已安裝服務的資料庫
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d24a92712d6713e2ca31dbc4b768e3b7c2983ffc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944939"
---
# <a name="database-of-installed-services"></a><span data-ttu-id="67825-103">已安裝服務的資料庫</span><span class="sxs-lookup"><span data-stu-id="67825-103">Database of Installed Services</span></span>

<span data-ttu-id="67825-104">SCM 會在登錄中維護已安裝服務的資料庫。</span><span class="sxs-lookup"><span data-stu-id="67825-104">The SCM maintains a database of installed services in the registry.</span></span> <span data-ttu-id="67825-105">資料庫是由新增、修改或設定服務的 SCM 和程式所使用。</span><span class="sxs-lookup"><span data-stu-id="67825-105">The database is used by the SCM and programs that add, modify, or configure services.</span></span> <span data-ttu-id="67825-106">以下是此資料庫的登錄機碼： **HKEY \_ LOCAL \_ MACHINE \\ SYSTEM \\ CurrentControlSet \\ Services**。</span><span class="sxs-lookup"><span data-stu-id="67825-106">The following is the registry key for this database: **HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\Services**.</span></span>

<span data-ttu-id="67825-107">此機碼包含每個已安裝服務和驅動程式服務的子機碼。</span><span class="sxs-lookup"><span data-stu-id="67825-107">This key contains a subkey for each installed service and driver service.</span></span> <span data-ttu-id="67825-108">子機碼的名稱是服務的名稱，當服務設定程式安裝服務時，會由 [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) 函式所指定。</span><span class="sxs-lookup"><span data-stu-id="67825-108">The name of the subkey is the name of the service, as specified by the [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) function when the service was installed by a service configuration program.</span></span>

<span data-ttu-id="67825-109">安裝系統時，會建立資料庫的初始複本。</span><span class="sxs-lookup"><span data-stu-id="67825-109">An initial copy of the database is created when the system is installed.</span></span> <span data-ttu-id="67825-110">資料庫包含系統開機期間所需設備磁碟機的專案。</span><span class="sxs-lookup"><span data-stu-id="67825-110">The database contains entries for the device drivers required during system boot.</span></span> <span data-ttu-id="67825-111">資料庫包含每個已安裝服務和驅動程式服務的下列資訊：</span><span class="sxs-lookup"><span data-stu-id="67825-111">The database includes the following information about each installed service and driver service:</span></span>

-   <span data-ttu-id="67825-112">服務類型。</span><span class="sxs-lookup"><span data-stu-id="67825-112">The service type.</span></span> <span data-ttu-id="67825-113">這會指出服務是否在自己的進程中執行，或與其他服務共用進程。</span><span class="sxs-lookup"><span data-stu-id="67825-113">This indicates whether the service executes in its own process or shares a process with other services.</span></span> <span data-ttu-id="67825-114">針對驅動程式服務，這會指出服務是核心驅動程式還是檔案系統驅動程式。</span><span class="sxs-lookup"><span data-stu-id="67825-114">For driver services, this indicates whether the service is a kernel driver or a file system driver.</span></span>
-   <span data-ttu-id="67825-115">開始類型。</span><span class="sxs-lookup"><span data-stu-id="67825-115">The start type.</span></span> <span data-ttu-id="67825-116">這表示服務或驅動程式服務是否會在系統啟動時自動啟動 (自動啟動服務) 或在服務控制程式要求時是否啟動 SCM (需求啟動服務) 。</span><span class="sxs-lookup"><span data-stu-id="67825-116">This indicates whether the service or driver service is started automatically at system startup (auto-start service) or whether the SCM starts it when requested by a service control program (demand-start service).</span></span> <span data-ttu-id="67825-117">啟動類型也可以表示服務或驅動程式服務已停用，在這種情況下無法啟動。</span><span class="sxs-lookup"><span data-stu-id="67825-117">The start type can also indicate that the service or driver service is disabled, in which case it cannot be started.</span></span>
-   <span data-ttu-id="67825-118">錯誤控制層級。</span><span class="sxs-lookup"><span data-stu-id="67825-118">The error control level.</span></span> <span data-ttu-id="67825-119">如果服務或驅動程式服務在系統啟動時無法啟動，並決定啟動程式將採取的動作，這會指定錯誤的嚴重性。</span><span class="sxs-lookup"><span data-stu-id="67825-119">This specifies the severity of the error if the service or driver service fails to start during system startup and determines the action that the startup program will take.</span></span>
-   <span data-ttu-id="67825-120">可執行檔的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="67825-120">The fully qualified path of the executable file.</span></span> <span data-ttu-id="67825-121">副檔名為。適用于服務和的 EXE。SYS for 驅動程式服務。</span><span class="sxs-lookup"><span data-stu-id="67825-121">The filename extension is .EXE for services and .SYS for driver services.</span></span>
-   <span data-ttu-id="67825-122">選用的相依性資訊，用來判斷啟動服務或驅動程式服務的正確順序。</span><span class="sxs-lookup"><span data-stu-id="67825-122">Optional dependency information used to determine the proper order for starting services or driver services.</span></span> <span data-ttu-id="67825-123">針對服務，這項資訊可以包含 SCM 必須啟動的服務清單，才能啟動指定的服務、服務所屬的載入順序群組名稱，以及指出服務在其載入順序群組中之啟動順序的標記識別項。</span><span class="sxs-lookup"><span data-stu-id="67825-123">For services, this information can include a list of services that the SCM must start before it can start the specified service, the name of a load ordering group that the service is part of, and a tag identifier that indicates the start order of the service in its load ordering group.</span></span> <span data-ttu-id="67825-124">針對驅動程式服務，這項資訊包含必須在指定的驅動程式之前啟動的驅動程式清單。</span><span class="sxs-lookup"><span data-stu-id="67825-124">For driver services, this information includes a list of drivers that must be started before the specified driver.</span></span>
-   <span data-ttu-id="67825-125">針對服務，選擇性的帳戶名稱和密碼。</span><span class="sxs-lookup"><span data-stu-id="67825-125">For services, an optional account name and password.</span></span> <span data-ttu-id="67825-126">服務程式會在此帳戶的內容中執行。</span><span class="sxs-lookup"><span data-stu-id="67825-126">The service program runs in the context of this account.</span></span> <span data-ttu-id="67825-127">如果未指定任何帳戶，服務會在 [LocalSystem 帳戶](localsystem-account.md)內容中執行。</span><span class="sxs-lookup"><span data-stu-id="67825-127">If no account is specified, the service executes in the context of the [LocalSystem account](localsystem-account.md).</span></span>
-   <span data-ttu-id="67825-128">針對驅動程式服務，選用的驅動程式物件名稱 (例如， \\ FileSystem \\ Rdr 或 \\ driver \\ Xns) ，由 i/o 系統用來載入設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="67825-128">For driver services, an optional driver object name (for example, \\FileSystem\\Rdr or \\Driver\\Xns), used by the I/O system to load the device driver.</span></span> <span data-ttu-id="67825-129">如果未指定名稱，則 i/o 系統會根據驅動程式服務名稱建立預設名稱。</span><span class="sxs-lookup"><span data-stu-id="67825-129">If no name is specified, the I/O system creates a default name based on the driver service name.</span></span>

> [!Note]  
> <span data-ttu-id="67825-130">此資料庫也稱為服務資料庫或 SCM 資料庫。</span><span class="sxs-lookup"><span data-stu-id="67825-130">This database is also known as the ServicesActive database or the SCM database.</span></span> <span data-ttu-id="67825-131">您必須使用 SCM 提供的函式，而不是直接修改資料庫。</span><span class="sxs-lookup"><span data-stu-id="67825-131">You must use the functions provided by the SCM, instead of modifying the database directly.</span></span>

 

 

 



