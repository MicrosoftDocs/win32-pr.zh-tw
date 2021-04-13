---
title: 多播群組管理員函數
description: 以下是用來向多播群組管理員註冊的功能
ms.assetid: d4374ced-06ea-49dd-8f52-0d06612aa4c3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bbc3dbcfe24e63283907e5e68f211fd1f4cb6e3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311121"
---
# <a name="multicast-group-manager-functions"></a><span data-ttu-id="9c686-103">多播群組管理員函數</span><span class="sxs-lookup"><span data-stu-id="9c686-103">Multicast Group Manager Functions</span></span>

<span data-ttu-id="9c686-104">以下是用來向多播群組管理員註冊的函數：</span><span class="sxs-lookup"><span data-stu-id="9c686-104">The following functions are used to register with the multicast group manager:</span></span>

[<span data-ttu-id="9c686-105">**MgmRegisterMProtocol**</span><span class="sxs-lookup"><span data-stu-id="9c686-105">**MgmRegisterMProtocol**</span></span>](/windows/desktop/api/Mgm/nf-mgm-mgmregistermprotocol)

[<span data-ttu-id="9c686-106">**MgmDeRegisterMProtocol**</span><span class="sxs-lookup"><span data-stu-id="9c686-106">**MgmDeRegisterMProtocol**</span></span>](/windows/desktop/api/Mgm/nf-mgm-mgmderegistermprotocol)

<span data-ttu-id="9c686-107">以下是用來管理介面擁有權的函式：</span><span class="sxs-lookup"><span data-stu-id="9c686-107">The following functions are used to manage interface ownership:</span></span>

[<span data-ttu-id="9c686-108">**MgmGetProtocolOnInterface**</span><span class="sxs-lookup"><span data-stu-id="9c686-108">**MgmGetProtocolOnInterface**</span></span>](/windows/desktop/api/Mgm/nf-mgm-mgmgetprotocoloninterface)

[<span data-ttu-id="9c686-109">**MgmTakeInterfaceOwnership**</span><span class="sxs-lookup"><span data-stu-id="9c686-109">**MgmTakeInterfaceOwnership**</span></span>](/windows/desktop/api/Mgm/nf-mgm-mgmtakeinterfaceownership)

[<span data-ttu-id="9c686-110">**MgmReleaseInterfaceOwnership**</span><span class="sxs-lookup"><span data-stu-id="9c686-110">**MgmReleaseInterfaceOwnership**</span></span>](/windows/desktop/api/Mgm/nf-mgm-mgmreleaseinterfaceownership)

<span data-ttu-id="9c686-111">以下是用來管理群組成員資格的函數：</span><span class="sxs-lookup"><span data-stu-id="9c686-111">The following functions are used to manage group membership:</span></span>

[<span data-ttu-id="9c686-112">**MgmAddGroupMembershipEntry**</span><span class="sxs-lookup"><span data-stu-id="9c686-112">**MgmAddGroupMembershipEntry**</span></span>](/windows/desktop/api/Mgm/nf-mgm-mgmaddgroupmembershipentry)

[<span data-ttu-id="9c686-113">**MgmDeleteGroupMembershipEntry**</span><span class="sxs-lookup"><span data-stu-id="9c686-113">**MgmDeleteGroupMembershipEntry**</span></span>](/windows/desktop/api/Mgm/nf-mgm-mgmdeletegroupmembershipentry)

<span data-ttu-id="9c686-114">下列函式可用來取得多播轉送專案 (MFEs) 和 MFE 統計資料：</span><span class="sxs-lookup"><span data-stu-id="9c686-114">The following functions are used to obtain multicast forwarding entries (MFEs) and MFE statistics:</span></span>

[<span data-ttu-id="9c686-115">**MgmGetFirstMfe**</span><span class="sxs-lookup"><span data-stu-id="9c686-115">**MgmGetFirstMfe**</span></span>](/windows/desktop/api/Mgm/nf-mgm-mgmgetfirstmfe)

[<span data-ttu-id="9c686-116">**MgmGetNextMfe**</span><span class="sxs-lookup"><span data-stu-id="9c686-116">**MgmGetNextMfe**</span></span>](/windows/desktop/api/Mgm/nf-mgm-mgmgetnextmfe)

[<span data-ttu-id="9c686-117">**MgmGetMfe**</span><span class="sxs-lookup"><span data-stu-id="9c686-117">**MgmGetMfe**</span></span>](/windows/desktop/api/Mgm/nf-mgm-mgmgetmfe)

[<span data-ttu-id="9c686-118">**MgmGetFirstMfeStats**</span><span class="sxs-lookup"><span data-stu-id="9c686-118">**MgmGetFirstMfeStats**</span></span>](/windows/desktop/api/Mgm/nf-mgm-mgmgetfirstmfestats)

[<span data-ttu-id="9c686-119">**MgmGetNextMfeStats**</span><span class="sxs-lookup"><span data-stu-id="9c686-119">**MgmGetNextMfeStats**</span></span>](/windows/desktop/api/Mgm/nf-mgm-mgmgetnextmfestats)

[<span data-ttu-id="9c686-120">**MgmGetMfeStats**</span><span class="sxs-lookup"><span data-stu-id="9c686-120">**MgmGetMfeStats**</span></span>](/windows/desktop/api/Mgm/nf-mgm-mgmgetmfestats)

<span data-ttu-id="9c686-121">下列函式是用來修改 MFEs：</span><span class="sxs-lookup"><span data-stu-id="9c686-121">The following function is used to modify MFEs:</span></span>

[<span data-ttu-id="9c686-122">**MgmSetMfe**</span><span class="sxs-lookup"><span data-stu-id="9c686-122">**MgmSetMfe**</span></span>](/windows/desktop/api/Mgm/nf-mgm-mgmsetmfe)

<span data-ttu-id="9c686-123">下列函式會用來取得已加入的群組清單：</span><span class="sxs-lookup"><span data-stu-id="9c686-123">The following functions are used obtain a list of groups that have been joined:</span></span>

[<span data-ttu-id="9c686-124">**MgmGroupEnumerationStart**</span><span class="sxs-lookup"><span data-stu-id="9c686-124">**MgmGroupEnumerationStart**</span></span>](/windows/desktop/api/Mgm/nf-mgm-mgmgroupenumerationstart)

[<span data-ttu-id="9c686-125">**MgmGroupEnumerationGetNext**</span><span class="sxs-lookup"><span data-stu-id="9c686-125">**MgmGroupEnumerationGetNext**</span></span>](/windows/desktop/api/Mgm/nf-mgm-mgmgroupenumerationgetnext)

[<span data-ttu-id="9c686-126">**MgmGroupEnumerationEnd**</span><span class="sxs-lookup"><span data-stu-id="9c686-126">**MgmGroupEnumerationEnd**</span></span>](/windows/desktop/api/Mgm/nf-mgm-mgmgroupenumerationend)

 

 




