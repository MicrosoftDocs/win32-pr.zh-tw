---
description: 當 WUA 偵測到呼叫端沒有存取介面、方法或屬性的許可權時， \_ 就會傳回 HRESULT E ACCESSDENIED。
ms.assetid: 4535ce8d-c329-4335-8b0a-8f63c22f111d
title: 在 WUA API 中保護介面、方法和屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6680f616e1ca0596aba04edf4f7ddf7615e0c7f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973486"
---
# <a name="securing-interfaces-methods-and-properties-in-the-wua-api"></a><span data-ttu-id="b8baf-103">在 WUA API 中保護介面、方法和屬性</span><span class="sxs-lookup"><span data-stu-id="b8baf-103">Securing Interfaces, Methods, and Properties in the WUA API</span></span>

<span data-ttu-id="b8baf-104">只有屬於下列 Windows 安全性群組的呼叫者，才能存取 Windows Update 代理程式 (WUA) 的某些介面、方法和屬性：</span><span class="sxs-lookup"><span data-stu-id="b8baf-104">Some interfaces, methods, and properties of Windows Update Agent (WUA) are accessible only to callers who belong to the following Windows security groups:</span></span>

-   <span data-ttu-id="b8baf-105">系統管理員</span><span class="sxs-lookup"><span data-stu-id="b8baf-105">Administrator</span></span>
-   <span data-ttu-id="b8baf-106">User</span><span class="sxs-lookup"><span data-stu-id="b8baf-106">User</span></span>
-   <span data-ttu-id="b8baf-107">進階使用者</span><span class="sxs-lookup"><span data-stu-id="b8baf-107">Power User</span></span>

<span data-ttu-id="b8baf-108">當 WUA 偵測到呼叫端沒有存取介面、方法或屬性的許可權時，  \_ 就會傳回 HRESULT E ACCESSDENIED。</span><span class="sxs-lookup"><span data-stu-id="b8baf-108">When WUA detects that a caller does not have permission to access an interface, method, or property, the **HRESULT** E\_ACCESSDENIED is returned.</span></span>

<span data-ttu-id="b8baf-109">系統管理員、使用者和 Power User 安全性群組可以使用下列介面：</span><span class="sxs-lookup"><span data-stu-id="b8baf-109">The following interfaces are available to the Administrator, User, and Power User security groups:</span></span>

-   [<span data-ttu-id="b8baf-110">**IAutomaticUpdates**</span><span class="sxs-lookup"><span data-stu-id="b8baf-110">**IAutomaticUpdates**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iautomaticupdates)
-   [<span data-ttu-id="b8baf-111">**IAutomaticUpdatesSettings**</span><span class="sxs-lookup"><span data-stu-id="b8baf-111">**IAutomaticUpdatesSettings**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iautomaticupdatessettings)
-   [<span data-ttu-id="b8baf-112">**IAutomaticUpdatesSettings2**</span><span class="sxs-lookup"><span data-stu-id="b8baf-112">**IAutomaticUpdatesSettings2**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iautomaticupdatessettings2)
-   [<span data-ttu-id="b8baf-113">**ISystemInformation**</span><span class="sxs-lookup"><span data-stu-id="b8baf-113">**ISystemInformation**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-isysteminformation)
-   [<span data-ttu-id="b8baf-114">**IUpdateSearcher**</span><span class="sxs-lookup"><span data-stu-id="b8baf-114">**IUpdateSearcher**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesearcher)
-   <span data-ttu-id="b8baf-115">[**IUpdateSession**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession)和 [ **IUpdateSession2**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession2)</span><span class="sxs-lookup"><span data-stu-id="b8baf-115">[**IUpdateSession**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession) and [**IUpdateSession2**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession2)</span></span>

> [!Note]  
> <span data-ttu-id="b8baf-116">如果下列條件成立，則搜尋會失敗：</span><span class="sxs-lookup"><span data-stu-id="b8baf-116">If the following conditions are true, a search fails:</span></span>
>
> -   <span data-ttu-id="b8baf-117">不是系統管理員的使用者，會將 [**IUpdateSession2 介面的 UserLocale 屬性**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesession2-get_userlocale) 設定為對應于電腦上未安裝之語言的地區設定。</span><span class="sxs-lookup"><span data-stu-id="b8baf-117">A user who is not an administrator sets the [**UserLocale property of the IUpdateSession2**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesession2-get_userlocale) interface to a locale that corresponds to a language that is not installed on the computer.</span></span>
> -   <span data-ttu-id="b8baf-118">搜尋會使用從 UpdateSession 物件建立的 UpdateSearch 物件。</span><span class="sxs-lookup"><span data-stu-id="b8baf-118">The search uses an UpdateSearch object created from the UpdateSession object.</span></span>

 

<span data-ttu-id="b8baf-119">下列下載介面和方法可供系統管理員和 Power 使用者群組使用：</span><span class="sxs-lookup"><span data-stu-id="b8baf-119">The following download interfaces and methods are available to the Administrator and Power User groups:</span></span>

-   [<span data-ttu-id="b8baf-120">**IUpdateDownloader**</span><span class="sxs-lookup"><span data-stu-id="b8baf-120">**IUpdateDownloader**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdatedownloader)
-   [<span data-ttu-id="b8baf-121">**IUpdate::CopyFromCache**</span><span class="sxs-lookup"><span data-stu-id="b8baf-121">**IUpdate::CopyFromCache**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-copyfromcache)
-   [<span data-ttu-id="b8baf-122">**IAutomaticUpdatesSettings2::CheckPermission**</span><span class="sxs-lookup"><span data-stu-id="b8baf-122">**IAutomaticUpdatesSettings2::CheckPermission**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings2-checkpermission)
    > [!Note]  
    > <span data-ttu-id="b8baf-123">系統管理員、使用者和 power users 都可以呼叫 [**IAutomaticUpdatesSettings2：： CheckPermission**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings2-checkpermission)。</span><span class="sxs-lookup"><span data-stu-id="b8baf-123">Administrators, users, and power users can call [**IAutomaticUpdatesSettings2::CheckPermission**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings2-checkpermission).</span></span>

     

<span data-ttu-id="b8baf-124">下列安裝介面、方法和屬性可供系統管理員群組使用：</span><span class="sxs-lookup"><span data-stu-id="b8baf-124">The following installation interfaces, methods, and properties are available to the Administrator groups:</span></span>

-   [<span data-ttu-id="b8baf-125">**IAutomaticUpdates：:P ause**</span><span class="sxs-lookup"><span data-stu-id="b8baf-125">**IAutomaticUpdates::Pause**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdates-pause)
-   [<span data-ttu-id="b8baf-126">**IAutomaticUpdates：： Resume**</span><span class="sxs-lookup"><span data-stu-id="b8baf-126">**IAutomaticUpdates::Resume**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdates-resume)
-   [<span data-ttu-id="b8baf-127">**IAutomaticUpdates::EnableService**</span><span class="sxs-lookup"><span data-stu-id="b8baf-127">**IAutomaticUpdates::EnableService**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdates-enableservice)
-   [<span data-ttu-id="b8baf-128">**IUpdateInstaller**</span><span class="sxs-lookup"><span data-stu-id="b8baf-128">**IUpdateInstaller**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdateinstaller)
-   [<span data-ttu-id="b8baf-129">**IUpdate 的 IsHidden 屬性**</span><span class="sxs-lookup"><span data-stu-id="b8baf-129">**IsHidden Property of IUpdate**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_ishidden)
    > [!Note]  
    > <span data-ttu-id="b8baf-130">系統管理員、使用者和 power users 可以取出 [**IUpdate 的 IsHidden 屬性**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_ishidden)值。</span><span class="sxs-lookup"><span data-stu-id="b8baf-130">Administrators, users, and power users can retrieve the values of the [**IsHidden Property of IUpdate**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_ishidden).</span></span> <span data-ttu-id="b8baf-131">不過，只有系統管理員和 power users 可以設定這些值。</span><span class="sxs-lookup"><span data-stu-id="b8baf-131">However, only administrators and power users can set the values.</span></span>

     

-   [<span data-ttu-id="b8baf-132">**IUpdate：： AcceptEula**</span><span class="sxs-lookup"><span data-stu-id="b8baf-132">**IUpdate::AcceptEula**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-accepteula)
    > [!Note]  
    > <span data-ttu-id="b8baf-133">系統管理員和 power users 可以呼叫 [**IUpdate 的 AcceptEula 方法**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-accepteula)。</span><span class="sxs-lookup"><span data-stu-id="b8baf-133">Administrators and power users can call the [**AcceptEula method of IUpdate**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-accepteula).</span></span>

     

-   [<span data-ttu-id="b8baf-134">**IAutomaticUpdatesSettings：： Save**</span><span class="sxs-lookup"><span data-stu-id="b8baf-134">**IAutomaticUpdatesSettings::Save**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-save)
-   [<span data-ttu-id="b8baf-135">**IAutomaticUpdatesSettings 的 NotificationLevel 屬性**</span><span class="sxs-lookup"><span data-stu-id="b8baf-135">**NotificationLevel Property of IAutomaticUpdatesSettings**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_notificationlevel)
    > [!Note]  
    > <span data-ttu-id="b8baf-136">系統管理員、使用者和 power users 可以取出 [**IAutomaticUpdatesSettings 的 NotificationLevel 屬性**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_notificationlevel)值。</span><span class="sxs-lookup"><span data-stu-id="b8baf-136">Administrators, users, and power users can retrieve the values of the [**NotificationLevel Property of IAutomaticUpdatesSettings**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_notificationlevel).</span></span> <span data-ttu-id="b8baf-137">不過，只有系統管理員可以設定這些值。</span><span class="sxs-lookup"><span data-stu-id="b8baf-137">However, only administrators can set the values.</span></span>

     

-   [<span data-ttu-id="b8baf-138">**IAutomaticUpdatesSettings 的 ScheduledInstallationDay 屬性**</span><span class="sxs-lookup"><span data-stu-id="b8baf-138">**ScheduledInstallationDay Property of IAutomaticUpdatesSettings**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationday)
    > [!Note]  
    > <span data-ttu-id="b8baf-139">系統管理員、使用者和 power users 可以取出 [**IAutomaticUpdatesSettings 的 ScheduledInstallationDay 屬性**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationday)值。</span><span class="sxs-lookup"><span data-stu-id="b8baf-139">Administrators, users, and power users can retrieve the values of the [**ScheduledInstallationDay Property of IAutomaticUpdatesSettings**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationday).</span></span> <span data-ttu-id="b8baf-140">不過，只有系統管理員可以設定這些值。</span><span class="sxs-lookup"><span data-stu-id="b8baf-140">However, only administrators can set the values.</span></span>

     

-   [<span data-ttu-id="b8baf-141">**IAutomaticUpdatesSettings 的 ScheduledInstallationTime 屬性**</span><span class="sxs-lookup"><span data-stu-id="b8baf-141">**ScheduledInstallationTime Property of IAutomaticUpdatesSettings**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationtime)
    > [!Note]  
    > <span data-ttu-id="b8baf-142">系統管理員、使用者和 power users 可以取出 [**IAutomaticUpdatesSettings 的 ScheduledInstallationTime 屬性**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationtime)值。</span><span class="sxs-lookup"><span data-stu-id="b8baf-142">Administrators, users, and power users can retrieve the values of the [**ScheduledInstallationTime Property of IAutomaticUpdatesSettings**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationtime).</span></span> <span data-ttu-id="b8baf-143">不過，只有系統管理員可以設定這些值。</span><span class="sxs-lookup"><span data-stu-id="b8baf-143">However, only administrators can set the values.</span></span>

     

-   [<span data-ttu-id="b8baf-144">**IAutomaticUpdatesSettings2 的 IncludeRecommendedUpdates 屬性**</span><span class="sxs-lookup"><span data-stu-id="b8baf-144">**IncludeRecommendedUpdates Property of IAutomaticUpdatesSettings2**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings2-get_includerecommendedupdates)
    > [!Note]  
    > <span data-ttu-id="b8baf-145">系統管理員、使用者和 power users 可以取出 [**IAutomaticUpdatesSettings2 的 IncludeRecommendedUpdates 屬性**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings2-get_includerecommendedupdates)值。</span><span class="sxs-lookup"><span data-stu-id="b8baf-145">Administrators, users, and power users can retrieve the values of the [**IncludeRecommendedUpdates Property of IAutomaticUpdatesSettings2**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings2-get_includerecommendedupdates).</span></span> <span data-ttu-id="b8baf-146">不過，只有系統管理員可以設定這些值。</span><span class="sxs-lookup"><span data-stu-id="b8baf-146">However, only administrators can set the values.</span></span>

     

 

 



