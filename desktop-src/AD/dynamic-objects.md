---
title: 動態物件
description: 在 Windows Server 2003 和更新版本的 Windows 中，Active Directory Domain Services 提供將動態專案儲存在目錄中的支援。
ms.assetid: ac5779b6-f226-414c-92a9-091719b1515b
ms.tgt_platform: multiple
keywords:
- 動態物件廣告
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d521dabda8f82cbdcd46c00b3041f150f390d60c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671339"
---
# <a name="dynamic-objects"></a><span data-ttu-id="0dcbd-104">動態物件</span><span class="sxs-lookup"><span data-stu-id="0dcbd-104">Dynamic Objects</span></span>

<span data-ttu-id="0dcbd-105">在 Windows Server 2003 和更新版本的 Windows 中，Active Directory Domain Services 提供將動態專案儲存在目錄中的支援。</span><span class="sxs-lookup"><span data-stu-id="0dcbd-105">In Windows Server 2003 and later versions of Windows, Active Directory Domain Services provide support for storing dynamic entries in the directory.</span></span> <span data-ttu-id="0dcbd-106">動態專案是目錄中的物件，具有相關聯的存留時間 (TTL) 值。</span><span class="sxs-lookup"><span data-stu-id="0dcbd-106">A dynamic entry is an object in the directory which has an associated time-to-live (TTL) value.</span></span> <span data-ttu-id="0dcbd-107">建立專案時，會設定專案的 TTL。</span><span class="sxs-lookup"><span data-stu-id="0dcbd-107">The TTL for an entry is set when the entry is created.</span></span> <span data-ttu-id="0dcbd-108">存留時間會自動遞減，當它過期時，動態專案就會消失。</span><span class="sxs-lookup"><span data-stu-id="0dcbd-108">The time-to-live is automatically decremented, and when it expires the dynamic entry disappears.</span></span> <span data-ttu-id="0dcbd-109">用戶端可能會藉由重新整理 (修改) 的 TTL 值，使動態專案維持比目前剩餘的存留期還要久。</span><span class="sxs-lookup"><span data-stu-id="0dcbd-109">The client can cause a dynamic entry to remain longer than its current remaining life by refreshing (modifying) its TTL value.</span></span> <span data-ttu-id="0dcbd-110">將動態資料儲存在目錄中的用戶端必須定期重新整理該資料，以防止它消失。</span><span class="sxs-lookup"><span data-stu-id="0dcbd-110">Clients that store dynamic data in the directory must periodically refresh that data to prevent it from disappearing.</span></span>

<span data-ttu-id="0dcbd-111">許多應用程式和服務使用 LDAP 來儲存及存取 Active Directory 伺服器中相對靜態和全球感興趣的資料，也會想要繼續針對其動態資料需求使用 LDAP 存取。</span><span class="sxs-lookup"><span data-stu-id="0dcbd-111">Many applications and services that use LDAP to store and access relatively static and globally interesting data from an Active Directory server would also prefer to continue using LDAP access for their dynamic data needs.</span></span> <span data-ttu-id="0dcbd-112">此外，在某些應用程式中，可能會想要在 DS 中將垃圾收集物件的垃圾收集到目錄服務的使用年限有所限制。</span><span class="sxs-lookup"><span data-stu-id="0dcbd-112">Moreover, for some applications, it may be desirable to off-load the task of garbage-collecting objects in the DS that have a limited useful life to the directory service.</span></span> <span data-ttu-id="0dcbd-113">應用程式目錄分割 (有能力控制複本的放置) 和每個物件的 TTLs，將可提供在 Active Directory Domain Services 中裝載動態資料的功能，進而允許 LDAP 存取它。</span><span class="sxs-lookup"><span data-stu-id="0dcbd-113">Application directory partitions (with the ability for controlled placement of replicas) and per-object TTLs together will provide the capability of hosting dynamic data in Active Directory Domain Services, thus allowing LDAP access to it.</span></span>

<span data-ttu-id="0dcbd-114">名為 **dynamicObject** 的新輔助物件類別（具有 OID = 1.3.6.1.4.1.1466.101.119.2）將在基底 AD 架構中定義，以供動態專案使用。</span><span class="sxs-lookup"><span data-stu-id="0dcbd-114">A new auxiliary object class called **dynamicObject** with OID = 1.3.6.1.4.1.1466.101.119.2 will be defined in the base AD schema to be used by dynamic entries.</span></span> <span data-ttu-id="0dcbd-115">這個輔助類別包含名為 **entryTTL** 的屬性，其 OID = 1.3.6.1.4.1.1466.101.119.3 是系統可能包含的屬性。</span><span class="sxs-lookup"><span data-stu-id="0dcbd-115">This auxiliary class contains the attribute called **entryTTL** with OID = 1.3.6.1.4.1.1466.101.119.3 as a system-may-contain attribute.</span></span> <span data-ttu-id="0dcbd-116">這個屬性的值是在從目錄消失之前，對應的目錄專案將繼續存在的「時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="0dcbd-116">The value of this attribute is the "time in seconds" that the corresponding directory entry will continue to exist before disappearing from the directory.</span></span> <span data-ttu-id="0dcbd-117">如果用戶端未在建立物件時明確提供此屬性的值，則 DS 會提供預設值，如稍後所指定。</span><span class="sxs-lookup"><span data-stu-id="0dcbd-117">If the client does not supply a value for this attribute explicitly at object creation, then the DS provides a default value as specified later.</span></span>

<span data-ttu-id="0dcbd-118">具有 OID = 1.3.6.1.4.1.1466.101.119.1 的新擴充 LDAP 作業，會在目錄中的動態專案重新整理時，定義併發布在根 DSE 物件的 **supportedExtension** 屬性中。</span><span class="sxs-lookup"><span data-stu-id="0dcbd-118">A new extended LDAP operation with OID = 1.3.6.1.4.1.1466.101.119.1 for client refresh of a dynamic entry in the directory will be defined and published in the **supportedExtension** attribute of the root DSE object.</span></span>

<span data-ttu-id="0dcbd-119">在實際的實作為中， **entryTTL** 是一個結構化屬性。</span><span class="sxs-lookup"><span data-stu-id="0dcbd-119">In the actual implementation, **entryTTL** is a constructed attribute.</span></span> <span data-ttu-id="0dcbd-120">實際物件到期時間會儲存為絕對時間，當物件可以在稱為「 **ms-DS-輸入存留時間**」的系統屬性中終結時。</span><span class="sxs-lookup"><span data-stu-id="0dcbd-120">The real object expiration time is stored as an absolute time when the object can be destroyed in a system-only attribute called **ms-DS-Entry-Time-To-Live**.</span></span>

<span data-ttu-id="0dcbd-121">所有動態物件都有下列限制：</span><span class="sxs-lookup"><span data-stu-id="0dcbd-121">All dynamic objects have the following limitations:</span></span>

-   <span data-ttu-id="0dcbd-122">因為已刪除的動態物件的 TTL 即將到期，所以不會留下標記。</span><span class="sxs-lookup"><span data-stu-id="0dcbd-122">A deleted dynamic object due to its TTL expiring does not leave a tombstone behind.</span></span>
-   <span data-ttu-id="0dcbd-123">所有保存動態物件複本的 Dc 都必須在 Windows Server 2003 上執行。</span><span class="sxs-lookup"><span data-stu-id="0dcbd-123">All DCs holding replicas of dynamic objects must run on Windows Server 2003.</span></span>
-   <span data-ttu-id="0dcbd-124">除了設定分割區和架構分割之外，所有磁碟分割都支援具有 TTL 值的動態專案。</span><span class="sxs-lookup"><span data-stu-id="0dcbd-124">Dynamic entries with TTL values are supported in all partitions except the Configuration partition and Schema partition.</span></span>
-   <span data-ttu-id="0dcbd-125">Active Directory Domain Services 不會在根 DSE 物件中發佈選用 **dynamicSubtrees** 屬性，如 RFC 2589 中所述。</span><span class="sxs-lookup"><span data-stu-id="0dcbd-125">Active Directory Domain Services do not publish the optional **dynamicSubtrees** attribute, as described in the RFC 2589, in the root DSE object.</span></span>
-   <span data-ttu-id="0dcbd-126">處理搜尋、比較、加入、刪除、修改和 modifyDN 作業時，動態專案的處理方式類似非動態專案。</span><span class="sxs-lookup"><span data-stu-id="0dcbd-126">Dynamic entries are handled similar to non-dynamic entries when processing search, compare, add, delete, modify, and modifyDN operations.</span></span>
-   <span data-ttu-id="0dcbd-127">沒有任何方法可將靜態專案變更為動態專案，反之亦然。</span><span class="sxs-lookup"><span data-stu-id="0dcbd-127">There is no way to change a static entry into a dynamic entry and vice-versa.</span></span>
-   <span data-ttu-id="0dcbd-128">非動態專案無法加入至動態專案。</span><span class="sxs-lookup"><span data-stu-id="0dcbd-128">A non-dynamic entry cannot be added subordinate to a dynamic entry.</span></span>

 

 




