---
title: 追蹤變更
description: 某些應用程式必須維持儲存在 Active Directory 目錄服務和其他資料中的特定資料之間的一致性。
ms.assetid: f4539482-1170-4c0c-b817-b39e58049d39
ms.tgt_platform: multiple
keywords:
- Active Directory，使用追蹤變更
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dc772f883b97eb4e7305b39f0a582448a8bc021
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "103933038"
---
# <a name="tracking-changes"></a><span data-ttu-id="93547-104">追蹤變更</span><span class="sxs-lookup"><span data-stu-id="93547-104">Tracking Changes</span></span>

<span data-ttu-id="93547-105">某些應用程式必須維持儲存在 Active Directory 目錄服務和其他資料中的特定資料之間的一致性。</span><span class="sxs-lookup"><span data-stu-id="93547-105">Some applications must maintain consistency between specific data stored in the Active Directory directory service and other data.</span></span> <span data-ttu-id="93547-106">其他資料可能儲存在目錄、SQL Server 資料表、檔案或登錄中。</span><span class="sxs-lookup"><span data-stu-id="93547-106">The other data might be stored in the directory, in a SQL Server table, in a file, or in the registry.</span></span> <span data-ttu-id="93547-107">當儲存在目錄中的資料變更時，可能需要變更其他資料，才能保持一致。</span><span class="sxs-lookup"><span data-stu-id="93547-107">When data stored in the directory changes, the other data may be required to change in order to remain consistent.</span></span> <span data-ttu-id="93547-108">具有這項需求的應用程式包括：</span><span class="sxs-lookup"><span data-stu-id="93547-108">Applications that have this requirement include:</span></span>

<span data-ttu-id="93547-109">本節不涵蓋監視應用程式所使用的機制。</span><span class="sxs-lookup"><span data-stu-id="93547-109">This section does not cover mechanisms used by monitoring applications.</span></span> <span data-ttu-id="93547-110">這些應用程式會監視目錄變更，而不是為了維護不同存放區之間的一致資料，而是系統管理工具。</span><span class="sxs-lookup"><span data-stu-id="93547-110">These are applications that monitor directory changes not for the purpose of maintaining consistent data between separate stores, but as a system management tool.</span></span> <span data-ttu-id="93547-111">雖然監視應用程式可以使用支援變更追蹤應用程式的相同機制，但是下列機制特別針對監視應用程式而設計：</span><span class="sxs-lookup"><span data-stu-id="93547-111">Although monitoring applications can use the same mechanisms that support change-tracking applications, the following mechanisms are specifically designed for monitoring applications:</span></span>

-   <span data-ttu-id="93547-112">安全性審核。</span><span class="sxs-lookup"><span data-stu-id="93547-112">Security auditing.</span></span> <span data-ttu-id="93547-113">藉由修改系統存取控制清單 (SACL) 部分的物件安全描述項，您可能會對指定網域控制站上的物件進行存取，以在該 DC 上的安全性事件記錄檔中產生審核記錄。</span><span class="sxs-lookup"><span data-stu-id="93547-113">By modifying the system access-control list (SACL) portion of an object security descriptor, you can cause accesses to the object on a given domain controller to generate audit records in the security event log on that DC.</span></span> <span data-ttu-id="93547-114">您可以同時審核讀取、寫入或兩者。您可以審核整個物件或特定屬性。</span><span class="sxs-lookup"><span data-stu-id="93547-114">You can audit reads, writes, or both; you can audit the entire object or specific attributes.</span></span> <span data-ttu-id="93547-115">如需詳細資訊，請參閱抓取 [物件的 SACL](retrieving-an-objectampaposs-sacl.md) 和 [審核產生](/windows/desktop/SecAuthZ/audit-generation)。</span><span class="sxs-lookup"><span data-stu-id="93547-115">For more information, see [Retrieving an Object's SACL](retrieving-an-objectampaposs-sacl.md) and [Audit Generation](/windows/desktop/SecAuthZ/audit-generation).</span></span>
-   <span data-ttu-id="93547-116">事件記錄。</span><span class="sxs-lookup"><span data-stu-id="93547-116">Event logging.</span></span> <span data-ttu-id="93547-117">藉由修改指定網域控制站上的登錄設定，您可以變更記錄到目錄服務事件記錄檔的事件種類。</span><span class="sxs-lookup"><span data-stu-id="93547-117">By modifying registry settings on a given domain controller, you can change the kinds of events logged to the directory service event log.</span></span> <span data-ttu-id="93547-118">明確地說，若要記錄所有修改，請將下列登錄機碼底下的 **8 目錄存取** 值設定為4。</span><span class="sxs-lookup"><span data-stu-id="93547-118">Specifically, to log all modifications, set the **8 Directory Access** value under the following registry key to 4.</span></span>

    ```
    HKEY_LOCAL_MACHINE
       SYSTEM
          CurrentControlSet
             Services
                NTDS
                   Diagnostics
    ```

    <span data-ttu-id="93547-119">如需詳細資訊，請參閱 [事件記錄](/windows/desktop/EventLog/event-logging)。</span><span class="sxs-lookup"><span data-stu-id="93547-119">For more information, see [Event Logging](/windows/desktop/EventLog/event-logging).</span></span>

-   <span data-ttu-id="93547-120">事件追蹤。</span><span class="sxs-lookup"><span data-stu-id="93547-120">Event tracing.</span></span> <span data-ttu-id="93547-121">Windows 2000 引進了事件追蹤 API，可在軟體或硬體中追蹤和記錄感興趣的事件。</span><span class="sxs-lookup"><span data-stu-id="93547-121">Windows 2000 introduced an Event Tracing API for tracing and logging interesting events in software or hardware.</span></span> <span data-ttu-id="93547-122">Windows 作業系統和 Active Directory Domain Services 特別支援使用事件追蹤來進行容量規劃和詳細的效能分析。</span><span class="sxs-lookup"><span data-stu-id="93547-122">The Windows operating system, and Active Directory Domain Services in particular, support the use of event tracing for capacity planning and detailed performance analysis.</span></span> <span data-ttu-id="93547-123">如需詳細資訊，請參閱 ADSI 中的 [事件追蹤](/windows/desktop/ETW/event-tracing-portal) 和 [事件追蹤](/windows/desktop/ADSI/adsi-and-etw)。</span><span class="sxs-lookup"><span data-stu-id="93547-123">For more information, see [Event Tracing](/windows/desktop/ETW/event-tracing-portal) and [Event Tracing in ADSI](/windows/desktop/ADSI/adsi-and-etw).</span></span>

<span data-ttu-id="93547-124">本節包含下列主題：</span><span class="sxs-lookup"><span data-stu-id="93547-124">This section includes the following topics:</span></span>

-   [<span data-ttu-id="93547-125">變更追蹤技術總覽</span><span class="sxs-lookup"><span data-stu-id="93547-125">Overview of Change Tracking Techniques</span></span>](overview-of-change-tracking-techniques.md)
-   [<span data-ttu-id="93547-126">Active Directory Domain Services 中的變更通知</span><span class="sxs-lookup"><span data-stu-id="93547-126">Change Notifications in Active Directory Domain Services</span></span>](change-notifications-in-active-directory-domain-services.md)
-   [<span data-ttu-id="93547-127">使用 DirSync 控制項輪詢變更</span><span class="sxs-lookup"><span data-stu-id="93547-127">Polling for Changes Using the DirSync Control</span></span>](polling-for-changes-using-the-dirsync-control.md)
-   [<span data-ttu-id="93547-128">使用 USNChanged 輪詢變更</span><span class="sxs-lookup"><span data-stu-id="93547-128">Polling for Changes Using USNChanged</span></span>](polling-for-changes-using-usnchanged.md)

 

 