---
title: 網路管理的新功能
description: 網路管理的新功能
ms.assetid: f805b662-1807-4703-b27e-4721895fe450
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e688d340b8282015b99ccb3d7fa6404dfa332748
ms.sourcegitcommit: 89f99926f946dc6c5ea600fb7c41f6b19ceac516
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/21/2020
ms.locfileid: "104383233"
---
# <a name="whats-new-in-network-management"></a><span data-ttu-id="c36ee-103">網路管理的新功能</span><span class="sxs-lookup"><span data-stu-id="c36ee-103">What's New in Network Management</span></span>

## <a name="windows-8-and-windows-server-2012"></a><span data-ttu-id="c36ee-104">Windows 8 與 Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c36ee-104">Windows 8 and Windows Server 2012</span></span>

<span data-ttu-id="c36ee-105">Microsoft Windows 8 引進了新的網路管理程式設計功能。</span><span class="sxs-lookup"><span data-stu-id="c36ee-105">Microsoft Windows 8 introduces new Network Management programming features.</span></span> <span data-ttu-id="c36ee-106">這些新的元素擴充了網路管理的功能，可在布建具有 Windows 8 的電腦時，建立離線網域加入作業的布建套件。</span><span class="sxs-lookup"><span data-stu-id="c36ee-106">These new elements extend the capability of Network Management to create provisioning packages for offline domain join operations when provisioning computers with Windows 8.</span></span>

<span data-ttu-id="c36ee-107">以下是新的網路管理功能：</span><span class="sxs-lookup"><span data-stu-id="c36ee-107">The following are new Network Management functions:</span></span>

-   [<span data-ttu-id="c36ee-108">**NetCreateProvisioningPackage**</span><span class="sxs-lookup"><span data-stu-id="c36ee-108">**NetCreateProvisioningPackage**</span></span>](/windows/desktop/api/Lmjoin/nf-lmjoin-netprovisioncomputeraccount)
-   [<span data-ttu-id="c36ee-109">**NetRequestProvisioningPackageInstall**</span><span class="sxs-lookup"><span data-stu-id="c36ee-109">**NetRequestProvisioningPackageInstall**</span></span>](/windows/desktop/api/Lmjoin/nf-lmjoin-netrequestprovisioningpackageinstall)

<span data-ttu-id="c36ee-110">以下是新的網路管理結構：</span><span class="sxs-lookup"><span data-stu-id="c36ee-110">The following are new Network Management structures:</span></span>

-   [<span data-ttu-id="c36ee-111">**NETSETUP 布建 \_ \_ 參數**</span><span class="sxs-lookup"><span data-stu-id="c36ee-111">**NETSETUP\_PROVISIONING\_PARAMS**</span></span>](/windows/desktop/api/Lmjoin/ns-lmjoin-netsetup_provisioning_params)
-   [<span data-ttu-id="c36ee-112">**使用者 \_ 資訊 \_ 24**</span><span class="sxs-lookup"><span data-stu-id="c36ee-112">**USER\_INFO\_24**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_24)

<span data-ttu-id="c36ee-113">[**NetUserGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetinfo)函式已在 Windows 8 上增強，以支援新的資訊層級，並傳回 [**使用者 \_ 資訊 \_ 24**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_24)結構，其中包含連線到網際網路身分識別之帳戶的使用者帳戶資訊。</span><span class="sxs-lookup"><span data-stu-id="c36ee-113">The [**NetUserGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetinfo) function has been enhanced on Windows 8 to support a new information level and return a [**USER\_INFO\_24**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_24) structure with user account information for an account connected to an Internet identity.</span></span>

## <a name="windows-7-and-windows-server-2008-r2"></a><span data-ttu-id="c36ee-114">Windows 7 與 Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c36ee-114">Windows 7 and Windows Server 2008 R2</span></span>

<span data-ttu-id="c36ee-115">Microsoft Windows 7 引進了新的網路管理程式設計功能。</span><span class="sxs-lookup"><span data-stu-id="c36ee-115">Microsoft Windows 7 introduces new Network Management programming features.</span></span> <span data-ttu-id="c36ee-116">這些元素會擴充網路管理的功能，以在使用 Windows 7 布建電腦時允許離線網域加入作業。</span><span class="sxs-lookup"><span data-stu-id="c36ee-116">These elements extend the capability of Network Management to allow offline domain join operations when provisioning computers with Windows 7.</span></span>

<span data-ttu-id="c36ee-117">以下是新的網路管理功能：</span><span class="sxs-lookup"><span data-stu-id="c36ee-117">The following are new Network Management functions:</span></span>

-   [<span data-ttu-id="c36ee-118">**NetProvisionComputerAccount**</span><span class="sxs-lookup"><span data-stu-id="c36ee-118">**NetProvisionComputerAccount**</span></span>](/windows/desktop/api/Lmjoin/nf-lmjoin-netprovisioncomputeraccount)
-   [<span data-ttu-id="c36ee-119">**NetRequestOfflineDomainJoin**</span><span class="sxs-lookup"><span data-stu-id="c36ee-119">**NetRequestOfflineDomainJoin**</span></span>](/windows/desktop/api/Lmjoin/nf-lmjoin-netrequestofflinedomainjoin)

<span data-ttu-id="c36ee-120">下列現有的網路管理功能已增強，可支援其他選項：</span><span class="sxs-lookup"><span data-stu-id="c36ee-120">The following existing Network Management functions were enhanced to support additional options:</span></span>

-   [<span data-ttu-id="c36ee-121">**NetJoinDomain**</span><span class="sxs-lookup"><span data-stu-id="c36ee-121">**NetJoinDomain**</span></span>](/windows/desktop/api/Lmjoin/nf-lmjoin-netjoindomain)

## <a name="windows-server-2003"></a><span data-ttu-id="c36ee-122">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c36ee-122">Windows Server 2003</span></span>

<span data-ttu-id="c36ee-123">Microsoft Windows Server 2003 引進了新的網路管理程式設計功能。</span><span class="sxs-lookup"><span data-stu-id="c36ee-123">Microsoft Windows Server 2003 introduces new Network Management programming features.</span></span> <span data-ttu-id="c36ee-124">這些元素擴充了 Windows Server 2003 和更新版本上網路管理作業的功能。</span><span class="sxs-lookup"><span data-stu-id="c36ee-124">These elements extend the capability of Network Management operations on Windows Server 2003 and later.</span></span>

## <a name="windows-xp"></a><span data-ttu-id="c36ee-125">Windows XP</span><span class="sxs-lookup"><span data-stu-id="c36ee-125">Windows XP</span></span>

<span data-ttu-id="c36ee-126">Microsoft Windows XP 引進了新的網路管理程式設計功能。</span><span class="sxs-lookup"><span data-stu-id="c36ee-126">Microsoft Windows XP introduces new Network Management programming features.</span></span> <span data-ttu-id="c36ee-127">這些元素擴充了 Windows XP 和更新版本上網路管理作業的功能。</span><span class="sxs-lookup"><span data-stu-id="c36ee-127">These elements extend the capability of Network Management operations on Windows XP and later.</span></span>

<span data-ttu-id="c36ee-128">以下是新的網路管理功能：</span><span class="sxs-lookup"><span data-stu-id="c36ee-128">The following are new Network Management functions:</span></span>

-   [<span data-ttu-id="c36ee-129">**NetAddAlternateComputerName**</span><span class="sxs-lookup"><span data-stu-id="c36ee-129">**NetAddAlternateComputerName**</span></span>](/windows/desktop/api/Lmjoin/nf-lmjoin-netaddalternatecomputername)
-   [<span data-ttu-id="c36ee-130">**NetEnumerateComputerNames**</span><span class="sxs-lookup"><span data-stu-id="c36ee-130">**NetEnumerateComputerNames**</span></span>](/windows/desktop/api/Lmjoin/nf-lmjoin-netenumeratecomputernames)
-   [<span data-ttu-id="c36ee-131">**NetRemoveAlternateComputerName**</span><span class="sxs-lookup"><span data-stu-id="c36ee-131">**NetRemoveAlternateComputerName**</span></span>](/windows/desktop/api/Lmjoin/nf-lmjoin-netremovealternatecomputername)
-   [<span data-ttu-id="c36ee-132">**NetSetPrimaryComputerName**</span><span class="sxs-lookup"><span data-stu-id="c36ee-132">**NetSetPrimaryComputerName**</span></span>](/windows/desktop/api/Lmjoin/nf-lmjoin-netsetprimarycomputername)
-   [<span data-ttu-id="c36ee-133">**SetNetScheduleAccountInformation**</span><span class="sxs-lookup"><span data-stu-id="c36ee-133">**SetNetScheduleAccountInformation**</span></span>](/windows/desktop/api/AtAcct/nf-atacct-setnetscheduleaccountinformation)

 

 




