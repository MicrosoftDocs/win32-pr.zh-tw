---
title: 伺服器和工作站上網路管理功能的需求
description: 如果您在伺服器或工作站上呼叫本主題所列的其中一個網路管理功能，則會將不同的存取需求套用至資訊查詢和資訊更新。
ms.assetid: 05ff1771-8058-4c86-8f45-735bf41dc128
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b06e516aa06465c67966cc076a0ca524d4ae4003
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842640"
---
# <a name="requirements-for-network-management-functions-on-servers-and-workstations"></a><span data-ttu-id="78b45-103">伺服器和工作站上網路管理功能的需求</span><span class="sxs-lookup"><span data-stu-id="78b45-103">Requirements for Network Management Functions on Servers and Workstations</span></span>

<span data-ttu-id="78b45-104">如果您在伺服器或工作站上呼叫本主題所列的其中一個網路管理功能，則會將不同的存取需求套用至資訊查詢和資訊更新。</span><span class="sxs-lookup"><span data-stu-id="78b45-104">If you call one of the network management functions listed in this topic on a server or workstation, different access requirements apply to information queries and information updates.</span></span>

## <a name="queries"></a><span data-ttu-id="78b45-105">查詢</span><span class="sxs-lookup"><span data-stu-id="78b45-105">Queries</span></span>

<span data-ttu-id="78b45-106">如果您呼叫下列其中一項功能，在伺服器或工作站上執行查詢，則所有已驗證的使用者預設都可以讀取和列舉資訊。</span><span class="sxs-lookup"><span data-stu-id="78b45-106">If you call one of the following functions to perform a query on a server or workstation, by default, all authenticated users can read and enumerate the information.</span></span>

-   <span data-ttu-id="78b45-107">[**NetGroupEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupenum)、 [**NetGroupGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupgetinfo)、 [**NetGroupGetUsers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupgetusers)</span><span class="sxs-lookup"><span data-stu-id="78b45-107">[**NetGroupEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupenum), [**NetGroupGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupgetinfo), [**NetGroupGetUsers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupgetusers)</span></span>
-   <span data-ttu-id="78b45-108">[**NetLocalGroupEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupenum)、 [**NetLocalGroupGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupgetinfo)、 [**NetLocalGroupGetMembers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupgetmembers)</span><span class="sxs-lookup"><span data-stu-id="78b45-108">[**NetLocalGroupEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupenum), [**NetLocalGroupGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupgetinfo), [**NetLocalGroupGetMembers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupgetmembers)</span></span>
-   [<span data-ttu-id="78b45-109">**NetQueryDisplayInformation**</span><span class="sxs-lookup"><span data-stu-id="78b45-109">**NetQueryDisplayInformation**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netquerydisplayinformation)
-   <span data-ttu-id="78b45-110">[**NetSessionGetInfo**](/windows/desktop/api/lmshare/nf-lmshare-netsessiongetinfo) (層級1和2僅) </span><span class="sxs-lookup"><span data-stu-id="78b45-110">[**NetSessionGetInfo**](/windows/desktop/api/lmshare/nf-lmshare-netsessiongetinfo) (levels 1 and 2 only)</span></span>
-   <span data-ttu-id="78b45-111">[**NetShareEnum**](/windows/desktop/api/lmshare/nf-lmshare-netshareenum) (層級2和502僅) </span><span class="sxs-lookup"><span data-stu-id="78b45-111">[**NetShareEnum**](/windows/desktop/api/lmshare/nf-lmshare-netshareenum) (levels 2 and 502 only)</span></span>
-   <span data-ttu-id="78b45-112">[**NetUserEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserenum)、 [**NetUserGetGroups**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetgroups)、 [**NetUserGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetinfo)、 [**NetUserGetLocalGroups**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetlocalgroups)、 [**NetUserModalsGet**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusermodalsget)</span><span class="sxs-lookup"><span data-stu-id="78b45-112">[**NetUserEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserenum), [**NetUserGetGroups**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetgroups), [**NetUserGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetinfo), [**NetUserGetLocalGroups**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetlocalgroups), [**NetUserModalsGet**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusermodalsget)</span></span>
-   <span data-ttu-id="78b45-113">[**NetWkstaGetInfo**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstagetinfo)、 [ **NetWkstaUserEnum**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstauserenum)</span><span class="sxs-lookup"><span data-stu-id="78b45-113">[**NetWkstaGetInfo**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstagetinfo), [**NetWkstaUserEnum**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstauserenum)</span></span>

<span data-ttu-id="78b45-114">以下是讀取和列舉資訊時，匿名存取的其他相關資訊。</span><span class="sxs-lookup"><span data-stu-id="78b45-114">Following is additional information about anonymous access when reading and enumerating information.</span></span>

<span data-ttu-id="78b45-115">**Windows Server 2003 和 WINDOWS XP：** 如果 EveryoneIncludesAnonymous 原則設定允許匿名存取，就可以匿名存取訊號。</span><span class="sxs-lookup"><span data-stu-id="78b45-115">**Windows Server 2003 and Windows XP:** Anonymous access to information is possible if the EveryoneIncludesAnonymous policy setting allows anonymous access.</span></span>

<span data-ttu-id="78b45-116">**Windows 2000：** 如果機原則設定允許匿名存取，則可以匿名存取安全物件。</span><span class="sxs-lookup"><span data-stu-id="78b45-116">**Windows 2000:** Anonymous access to securable objects is possible if the RestrictAnonymous policy setting allows anonymous access.</span></span> <span data-ttu-id="78b45-117">您可以將登錄中的下列機碼設定為值1，以限制匿名存取。</span><span class="sxs-lookup"><span data-stu-id="78b45-117">You can restrict anonymous access by setting the following key in the registry to the value 1.</span></span>

<span data-ttu-id="78b45-118">**HKEY \_LOCAL \_ MACHINE \\ System \\ CurrentControlSet \\ Control \\ Lsa** \\ **機**= 1</span><span class="sxs-lookup"><span data-stu-id="78b45-118">**HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Control\\Lsa**\\**RestrictAnonymous** = 1</span></span>

<span data-ttu-id="78b45-119">如需詳細資訊，請參閱 Microsoft 知識庫中的下列文章：</span><span class="sxs-lookup"><span data-stu-id="78b45-119">For more information, see the following article in the Microsoft Knowledge Base:</span></span>

<span data-ttu-id="78b45-120">文章識別碼： [Q246261](https://support.microsoft.com/kb/246261)</span><span class="sxs-lookup"><span data-stu-id="78b45-120">ARTICLE ID: [Q246261](https://support.microsoft.com/kb/246261)</span></span>

<span data-ttu-id="78b45-121">標題：如何使用機登錄值。</span><span class="sxs-lookup"><span data-stu-id="78b45-121">TITLE: How to use the RestrictAnonymous registry Value.</span></span>

## <a name="updates"></a><span data-ttu-id="78b45-122">更新</span><span class="sxs-lookup"><span data-stu-id="78b45-122">Updates</span></span>

<span data-ttu-id="78b45-123">依預設，只有系統管理員和 Power Users 可以寫入資訊。</span><span class="sxs-lookup"><span data-stu-id="78b45-123">By default, only Administrators and Power Users can write information.</span></span>

<span data-ttu-id="78b45-124">如需控制安全物件之存取的詳細資訊，請參閱 [存取控制](/windows/desktop/SecAuthZ/access-control)、 [許可權](/windows/desktop/SecAuthZ/privileges)和 [安全物件](/windows/desktop/SecAuthZ/securable-objects)。</span><span class="sxs-lookup"><span data-stu-id="78b45-124">For more information about controlling access to securable objects, see [Access Control](/windows/desktop/SecAuthZ/access-control), [Privileges](/windows/desktop/SecAuthZ/privileges), and [Securable Objects](/windows/desktop/SecAuthZ/securable-objects).</span></span> <span data-ttu-id="78b45-125">如需呼叫需要系統管理員許可權之函式的詳細資訊，請參閱 [以特殊許可權](/windows/desktop/SecBP/running-with-special-privileges)執行。</span><span class="sxs-lookup"><span data-stu-id="78b45-125">For more information about calling functions that require administrator privileges, see [Running with Special Privileges](/windows/desktop/SecBP/running-with-special-privileges).</span></span>

 

 