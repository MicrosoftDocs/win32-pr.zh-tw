---
title: 工作站和工作站使用者功能
description: 網路管理工作站功能會在本機或遠端工作站上執行系統管理工作。
ms.assetid: cc400f43-297b-4ff4-8353-b268839c48b8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd445746bca51abaa0cd72877bdf03dd4d00d338
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106969925"
---
# <a name="workstation-and-workstation-user-functions"></a><span data-ttu-id="01b8d-103">工作站和工作站使用者功能</span><span class="sxs-lookup"><span data-stu-id="01b8d-103">Workstation and Workstation User Functions</span></span>

<span data-ttu-id="01b8d-104">網路管理工作站功能會在本機或遠端工作站上執行系統管理工作。</span><span class="sxs-lookup"><span data-stu-id="01b8d-104">The network management workstation functions perform administrative tasks on a local or remote workstation.</span></span> <span data-ttu-id="01b8d-105">只有在本機或遠端伺服器上具有系統管理員群組成員資格的使用者或應用程式，才可以在工作站上執行系統管理工作，以控制其作業、使用者存取和資源分享。</span><span class="sxs-lookup"><span data-stu-id="01b8d-105">Only a user or application with admin group membership, on a local or remote server, can perform administrative tasks on a workstation to control its operation, user access, and resource sharing.</span></span> <span data-ttu-id="01b8d-106">如需呼叫需要系統管理員許可權之函式的詳細資訊，請參閱 [以特殊許可權](/windows/desktop/SecBP/running-with-special-privileges)執行。</span><span class="sxs-lookup"><span data-stu-id="01b8d-106">For more information about calling functions that require administrator privileges, see [Running with Special Privileges](/windows/desktop/SecBP/running-with-special-privileges).</span></span>

<span data-ttu-id="01b8d-107">工作站功能如下所示。</span><span class="sxs-lookup"><span data-stu-id="01b8d-107">The workstation functions are listed following.</span></span>



| <span data-ttu-id="01b8d-108">函式</span><span class="sxs-lookup"><span data-stu-id="01b8d-108">Function</span></span>                                   | <span data-ttu-id="01b8d-109">描述</span><span class="sxs-lookup"><span data-stu-id="01b8d-109">Description</span></span>                                                             |
|--------------------------------------------|-------------------------------------------------------------------------|
| [<span data-ttu-id="01b8d-110">**NetWkstaGetInfo**</span><span class="sxs-lookup"><span data-stu-id="01b8d-110">**NetWkstaGetInfo**</span></span>](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstagetinfo) | <span data-ttu-id="01b8d-111">傳回工作站設定元素的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="01b8d-111">Returns information about the configuration elements for a workstation.</span></span> |
| [<span data-ttu-id="01b8d-112">**NetWkstaSetInfo**</span><span class="sxs-lookup"><span data-stu-id="01b8d-112">**NetWkstaSetInfo**</span></span>](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstasetinfo) | <span data-ttu-id="01b8d-113">設定工作站。</span><span class="sxs-lookup"><span data-stu-id="01b8d-113">Configures a workstation.</span></span>                                               |



 

<span data-ttu-id="01b8d-114">工作站功能允許存取兩種不同類型的工作站資訊：</span><span class="sxs-lookup"><span data-stu-id="01b8d-114">The workstation functions allow access to two discrete types of workstation information:</span></span>

-   <span data-ttu-id="01b8d-115">系統資訊</span><span class="sxs-lookup"><span data-stu-id="01b8d-115">System information</span></span>
-   <span data-ttu-id="01b8d-116">平臺特定資訊</span><span class="sxs-lookup"><span data-stu-id="01b8d-116">Platform-specific information</span></span>

<span data-ttu-id="01b8d-117">在每一種類型中，資料都會依安全性存取進行分類。</span><span class="sxs-lookup"><span data-stu-id="01b8d-117">Within each type the data is categorized by security access.</span></span> <span data-ttu-id="01b8d-118">可存取來賓的資料是可供使用者存取的資料子集，也就是系統管理員可存取資料的子集。</span><span class="sxs-lookup"><span data-stu-id="01b8d-118">Data that is guest-accessible is a subset of the data that is user-accessible, which is in turn a subset of the admin-accessible data.</span></span>

<span data-ttu-id="01b8d-119">下列層級提供工作站資訊：</span><span class="sxs-lookup"><span data-stu-id="01b8d-119">Workstation information is available at the following levels:</span></span>

-   [<span data-ttu-id="01b8d-120">**WKSTA \_ 資訊 \_ 100**</span><span class="sxs-lookup"><span data-stu-id="01b8d-120">**WKSTA\_INFO\_100**</span></span>](/windows/desktop/api/Lmwksta/ns-lmwksta-wksta_info_100)
-   [<span data-ttu-id="01b8d-121">**WKSTA \_ 資訊 \_ 101**</span><span class="sxs-lookup"><span data-stu-id="01b8d-121">**WKSTA\_INFO\_101**</span></span>](/windows/desktop/api/Lmwksta/ns-lmwksta-wksta_info_101)
-   [<span data-ttu-id="01b8d-122">**WKSTA \_ 資訊 \_ 102**</span><span class="sxs-lookup"><span data-stu-id="01b8d-122">**WKSTA\_INFO\_102**</span></span>](/windows/desktop/api/Lmwksta/ns-lmwksta-wksta_info_102)

<span data-ttu-id="01b8d-123">網路管理工作站使用者功能允許存取使用者特定的資訊。</span><span class="sxs-lookup"><span data-stu-id="01b8d-123">The network management workstation user functions allow access to user-specific information.</span></span> <span data-ttu-id="01b8d-124">使用者特定的資訊與工作站資訊分開，因為工作站上可以有多個使用者。</span><span class="sxs-lookup"><span data-stu-id="01b8d-124">The user-specific information is separated from the workstation information because there can be more than one user on a workstation.</span></span>

<span data-ttu-id="01b8d-125">工作站使用者函式如下所示。</span><span class="sxs-lookup"><span data-stu-id="01b8d-125">The workstation user functions are listed following.</span></span>



| <span data-ttu-id="01b8d-126">函式</span><span class="sxs-lookup"><span data-stu-id="01b8d-126">Function</span></span>                                           | <span data-ttu-id="01b8d-127">描述</span><span class="sxs-lookup"><span data-stu-id="01b8d-127">Description</span></span>                                                                         |
|----------------------------------------------------|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="01b8d-128">**NetWkstaUserEnum**</span><span class="sxs-lookup"><span data-stu-id="01b8d-128">**NetWkstaUserEnum**</span></span>](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstauserenum)       | <span data-ttu-id="01b8d-129">列出所有目前登入工作站的使用者的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="01b8d-129">Lists information about all users currently logged on to the workstation.</span></span>           |
| [<span data-ttu-id="01b8d-130">**NetWkstaUserGetInfo**</span><span class="sxs-lookup"><span data-stu-id="01b8d-130">**NetWkstaUserGetInfo**</span></span>](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstausergetinfo) | <span data-ttu-id="01b8d-131">傳回一個目前登入使用者的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="01b8d-131">Returns information about one currently logged-on user.</span></span>                             |
| [<span data-ttu-id="01b8d-132">**NetWkstaUserSetInfo**</span><span class="sxs-lookup"><span data-stu-id="01b8d-132">**NetWkstaUserSetInfo**</span></span>](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstausersetinfo) | <span data-ttu-id="01b8d-133">設定工作站設定元素的使用者特定資訊。</span><span class="sxs-lookup"><span data-stu-id="01b8d-133">Sets the user-specific information for the configuration elements of a workstation.</span></span> |



 

<span data-ttu-id="01b8d-134">工作站使用者資訊可在下列層級取得：</span><span class="sxs-lookup"><span data-stu-id="01b8d-134">Workstation user information is available at the following levels:</span></span>

-   [<span data-ttu-id="01b8d-135">**WKSTA \_ 使用者 \_ 資訊 \_ 0**</span><span class="sxs-lookup"><span data-stu-id="01b8d-135">**WKSTA\_USER\_INFO\_0**</span></span>](/windows/desktop/api/Lmwksta/ns-lmwksta-wksta_user_info_0)
-   [<span data-ttu-id="01b8d-136">**WKSTA \_ 使用者 \_ 資訊 \_ 1**</span><span class="sxs-lookup"><span data-stu-id="01b8d-136">**WKSTA\_USER\_INFO\_1**</span></span>](/windows/desktop/api/Lmwksta/ns-lmwksta-wksta_user_info_1)
-   [<span data-ttu-id="01b8d-137">**WKSTA \_ 使用者 \_ 資訊 \_ 1101**</span><span class="sxs-lookup"><span data-stu-id="01b8d-137">**WKSTA\_USER\_INFO\_1101**</span></span>](/windows/desktop/api/Lmwksta/ns-lmwksta-wksta_user_info_1101)

 

 