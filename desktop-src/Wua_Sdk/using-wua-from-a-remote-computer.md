---
description: 遠端電腦上的使用者或遠端電腦上執行的應用程式，都可以使用 Windows Update 代理程式 (WUA) API。 不過，遠端使用者或應用程式必須具備系統管理員許可權。
ms.assetid: 15f86590-bed8-4506-916d-43b0bac5db2a
title: 從遠端電腦使用 WUA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bb14c019e48d6c36b210633ab9d57dcd157585a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973213"
---
# <a name="using-wua-from-a-remote-computer"></a><span data-ttu-id="427ec-104">從遠端電腦使用 WUA</span><span class="sxs-lookup"><span data-stu-id="427ec-104">Using WUA From a Remote Computer</span></span>

<span data-ttu-id="427ec-105">遠端電腦上的使用者或遠端電腦上執行的應用程式，都可以使用 Windows Update 代理程式 (WUA) API。</span><span class="sxs-lookup"><span data-stu-id="427ec-105">The Windows Update Agent (WUA) API can be used by a user on a remote computer or by an application that is running on a remote computer.</span></span> <span data-ttu-id="427ec-106">不過，遠端使用者或應用程式必須具備系統管理員許可權。</span><span class="sxs-lookup"><span data-stu-id="427ec-106">However, the remote user or application must have administrator privileges.</span></span>

<span data-ttu-id="427ec-107">下列清單包含遠端使用者和應用程式可用的介面：</span><span class="sxs-lookup"><span data-stu-id="427ec-107">The following list contains interfaces that are available to remote users and applications:</span></span>

-   [<span data-ttu-id="427ec-108">**IUpdateSession**</span><span class="sxs-lookup"><span data-stu-id="427ec-108">**IUpdateSession**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession)
-   [<span data-ttu-id="427ec-109">**IUpdateSession2**</span><span class="sxs-lookup"><span data-stu-id="427ec-109">**IUpdateSession2**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession2)
-   [<span data-ttu-id="427ec-110">**IUpdateSearcher**</span><span class="sxs-lookup"><span data-stu-id="427ec-110">**IUpdateSearcher**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesearcher)
-   [<span data-ttu-id="427ec-111">**IAutomaticUpdates**</span><span class="sxs-lookup"><span data-stu-id="427ec-111">**IAutomaticUpdates**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iautomaticupdates)
-   [<span data-ttu-id="427ec-112">**ISearchResult**</span><span class="sxs-lookup"><span data-stu-id="427ec-112">**ISearchResult**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-isearchresult)
-   [<span data-ttu-id="427ec-113">**IUpdateCollection**</span><span class="sxs-lookup"><span data-stu-id="427ec-113">**IUpdateCollection**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdatecollection)
-   [<span data-ttu-id="427ec-114">**IUpdate**</span><span class="sxs-lookup"><span data-stu-id="427ec-114">**IUpdate**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdate)
-   [<span data-ttu-id="427ec-115">**IUpdate2**</span><span class="sxs-lookup"><span data-stu-id="427ec-115">**IUpdate2**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdate2)
-   [<span data-ttu-id="427ec-116">**IWindowsDriverUpdate**</span><span class="sxs-lookup"><span data-stu-id="427ec-116">**IWindowsDriverUpdate**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iwindowsdriverupdate)
-   [<span data-ttu-id="427ec-117">**IWindowsDriverUpdate2**</span><span class="sxs-lookup"><span data-stu-id="427ec-117">**IWindowsDriverUpdate2**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iwindowsdriverupdate2)
-   [<span data-ttu-id="427ec-118">**IUpdateIdentity**</span><span class="sxs-lookup"><span data-stu-id="427ec-118">**IUpdateIdentity**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdateidentity)
-   [<span data-ttu-id="427ec-119">**IImageInformation**</span><span class="sxs-lookup"><span data-stu-id="427ec-119">**IImageInformation**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iimageinformation)
-   [<span data-ttu-id="427ec-120">**IInstallationBehavior**</span><span class="sxs-lookup"><span data-stu-id="427ec-120">**IInstallationBehavior**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationbehavior)
-   [<span data-ttu-id="427ec-121">**IStringCollection**</span><span class="sxs-lookup"><span data-stu-id="427ec-121">**IStringCollection**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-istringcollection)
-   [<span data-ttu-id="427ec-122">**IUpdateHistoryEntryCollection**</span><span class="sxs-lookup"><span data-stu-id="427ec-122">**IUpdateHistoryEntryCollection**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdatehistoryentrycollection)
-   [<span data-ttu-id="427ec-123">**IUpdateHistoryEntry**</span><span class="sxs-lookup"><span data-stu-id="427ec-123">**IUpdateHistoryEntry**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdatehistoryentry)
-   [<span data-ttu-id="427ec-124">**ICategoryCollection**</span><span class="sxs-lookup"><span data-stu-id="427ec-124">**ICategoryCollection**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-icategorycollection)
-   [<span data-ttu-id="427ec-125">**ICategory**</span><span class="sxs-lookup"><span data-stu-id="427ec-125">**ICategory**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-icategory)
-   [<span data-ttu-id="427ec-126">**IUpdateExceptionCollection**</span><span class="sxs-lookup"><span data-stu-id="427ec-126">**IUpdateExceptionCollection**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdateexceptioncollection)
-   [<span data-ttu-id="427ec-127">**IUpdateException**</span><span class="sxs-lookup"><span data-stu-id="427ec-127">**IUpdateException**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdateexception)
-   [<span data-ttu-id="427ec-128">**IUpdateDownloadContentCollection**</span><span class="sxs-lookup"><span data-stu-id="427ec-128">**IUpdateDownloadContentCollection**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdatedownloadcontentcollection)
-   [<span data-ttu-id="427ec-129">**IUpdateDownloadContent**</span><span class="sxs-lookup"><span data-stu-id="427ec-129">**IUpdateDownloadContent**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdatedownloadcontent)
-   [<span data-ttu-id="427ec-130">**IUpdateServiceManager**</span><span class="sxs-lookup"><span data-stu-id="427ec-130">**IUpdateServiceManager**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservicemanager)
-   [<span data-ttu-id="427ec-131">**IUpdateServiceCollection**</span><span class="sxs-lookup"><span data-stu-id="427ec-131">**IUpdateServiceCollection**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservicecollection)
-   [<span data-ttu-id="427ec-132">**IUpdateService**</span><span class="sxs-lookup"><span data-stu-id="427ec-132">**IUpdateService**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservice)
-   [<span data-ttu-id="427ec-133">**IWindowsUpdateAgentInfo**</span><span class="sxs-lookup"><span data-stu-id="427ec-133">**IWindowsUpdateAgentInfo**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iwindowsupdateagentinfo)

<span data-ttu-id="427ec-134">下列清單包含遠端使用者和應用程式無法使用的介面和屬性：</span><span class="sxs-lookup"><span data-stu-id="427ec-134">The following list contains interfaces and properties that are not available to remote users and applications:</span></span>

-   [<span data-ttu-id="427ec-135">**IUpdateSession::CreateUpdateDownloader**</span><span class="sxs-lookup"><span data-stu-id="427ec-135">**IUpdateSession::CreateUpdateDownloader**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesession-createupdatedownloader)
-   [<span data-ttu-id="427ec-136">**IUpdateSession::CreateUpdateInstaller**</span><span class="sxs-lookup"><span data-stu-id="427ec-136">**IUpdateSession::CreateUpdateInstaller**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesession-createupdateinstaller)
-   [<span data-ttu-id="427ec-137">**IUpdateSession 的 WebProxy 屬性**</span><span class="sxs-lookup"><span data-stu-id="427ec-137">**WebProxy Property of IUpdateSession**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesession-get_webproxy)
-   [<span data-ttu-id="427ec-138">**IUpdateSearcher::BeginSearch**</span><span class="sxs-lookup"><span data-stu-id="427ec-138">**IUpdateSearcher::BeginSearch**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-beginsearch)
-   [<span data-ttu-id="427ec-139">**IUpdateSearcher::EndSearch**</span><span class="sxs-lookup"><span data-stu-id="427ec-139">**IUpdateSearcher::EndSearch**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-endsearch)
-   <span data-ttu-id="427ec-140">IUpdate (**IsHidden** [**的 IsHidden 屬性**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_ishidden)在遠端呼叫時是唯讀的。 ) </span><span class="sxs-lookup"><span data-stu-id="427ec-140">[**IsHidden Property of IUpdate**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_ishidden) (**IsHidden** is read-only when it is called remotely.)</span></span>
-   [<span data-ttu-id="427ec-141">**IUpdate：： AcceptEula**</span><span class="sxs-lookup"><span data-stu-id="427ec-141">**IUpdate::AcceptEula**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-accepteula)
-   [<span data-ttu-id="427ec-142">**IUpdate::CopyFromCache**</span><span class="sxs-lookup"><span data-stu-id="427ec-142">**IUpdate::CopyFromCache**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-copyfromcache)
-   [<span data-ttu-id="427ec-143">**IUpdate2::CopyToCache**</span><span class="sxs-lookup"><span data-stu-id="427ec-143">**IUpdate2::CopyToCache**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdate2-copytocache)
-   [<span data-ttu-id="427ec-144">**IWindowsDriverUpdate2::CopyToCache**</span><span class="sxs-lookup"><span data-stu-id="427ec-144">**IWindowsDriverUpdate2::CopyToCache**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsdriverupdate2-copytocache)
-   [<span data-ttu-id="427ec-145">**IUpdateServiceManager：： AddService**</span><span class="sxs-lookup"><span data-stu-id="427ec-145">**IUpdateServiceManager::AddService**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-addservice)
-   [<span data-ttu-id="427ec-146">**IUpdateServiceManager::RegisterServiceWithAU**</span><span class="sxs-lookup"><span data-stu-id="427ec-146">**IUpdateServiceManager::RegisterServiceWithAU**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-registerservicewithau)
-   [<span data-ttu-id="427ec-147">**IUpdateServiceManager::UnregisterServiceWithAU**</span><span class="sxs-lookup"><span data-stu-id="427ec-147">**IUpdateServiceManager::UnregisterServiceWithAU**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-unregisterservicewithau)
-   [<span data-ttu-id="427ec-148">**IAutomaticUpdate：:P ause**</span><span class="sxs-lookup"><span data-stu-id="427ec-148">**IAutomaticUpdate::Pause**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdates-pause)
-   [<span data-ttu-id="427ec-149">**IAutomaticUpdates：： Resume**</span><span class="sxs-lookup"><span data-stu-id="427ec-149">**IAutomaticUpdates::Resume**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdates-resume)
-   [<span data-ttu-id="427ec-150">**IAutomaticUpdates::ShowSettingsDialog**</span><span class="sxs-lookup"><span data-stu-id="427ec-150">**IAutomaticUpdates::ShowSettingsDialog**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdates-showsettingsdialog)
-   [<span data-ttu-id="427ec-151">**IAutomaticUpdates 的 Settings 屬性**</span><span class="sxs-lookup"><span data-stu-id="427ec-151">**Settings Property of IAutomaticUpdates**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdates-get_settings)
-   [<span data-ttu-id="427ec-152">**IAutomaticUpdates 的 ServiceEnabled 屬性**</span><span class="sxs-lookup"><span data-stu-id="427ec-152">**ServiceEnabled Property of IAutomaticUpdates**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdates-get_serviceenabled)
-   [<span data-ttu-id="427ec-153">**IAutomaticUpdates::EnableService**</span><span class="sxs-lookup"><span data-stu-id="427ec-153">**IAutomaticUpdates::EnableService**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdates-enableservice)
-   [<span data-ttu-id="427ec-154">**ISystemInformation**</span><span class="sxs-lookup"><span data-stu-id="427ec-154">**ISystemInformation**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-isysteminformation)

<span data-ttu-id="427ec-155">您必須將下列埠和例外狀況新增至適用于 Windows Vista 和 Windows Server 2008 的 Windows 防火牆設定，才能從遠端呼叫 WUA API。</span><span class="sxs-lookup"><span data-stu-id="427ec-155">The following ports and exceptions must be added to the Windows firewall settings for Windows Vista and Windows Server 2008 for the WUA API to be called remotely.</span></span>

<dl> <dt>

<span data-ttu-id="427ec-156"><span id="Exception_1"></span><span id="exception_1"></span><span id="EXCEPTION_1"></span>例外狀況1</span><span class="sxs-lookup"><span data-stu-id="427ec-156"><span id="Exception_1"></span><span id="exception_1"></span><span id="EXCEPTION_1"></span>Exception 1</span></span>
</dt> <dd> <dl> <dd><span data-ttu-id="427ec-157">本機埠：135</span><span class="sxs-lookup"><span data-stu-id="427ec-157">Local port: 135</span></span></dd> <dd><span data-ttu-id="427ec-158">遠端埠：全部</span><span class="sxs-lookup"><span data-stu-id="427ec-158">Remote port: ALL</span></span></dd> <dd><span data-ttu-id="427ec-159">通訊協定編號：6</span><span class="sxs-lookup"><span data-stu-id="427ec-159">Protocol number: 6</span></span></dd> <dd><span data-ttu-id="427ec-160">可執行檔：% windir% \\ system32 \\svchost.exe</span><span class="sxs-lookup"><span data-stu-id="427ec-160">Executable: %windir%\\system32\\svchost.exe</span></span></dd> <dd><span data-ttu-id="427ec-161">服務： rpcss</span><span class="sxs-lookup"><span data-stu-id="427ec-161">Service: rpcss</span></span></dd> <dd><span data-ttu-id="427ec-162">遠端許可權：系統管理員</span><span class="sxs-lookup"><span data-stu-id="427ec-162">Remote privilege: Administrator</span></span></dd> </dl> </dd> <dt>

<span data-ttu-id="427ec-163"><span id="Exception_2"></span><span id="exception_2"></span><span id="EXCEPTION_2"></span>例外狀況2</span><span class="sxs-lookup"><span data-stu-id="427ec-163"><span id="Exception_2"></span><span id="exception_2"></span><span id="EXCEPTION_2"></span>Exception 2</span></span>
</dt> <dd> <dl> <dd><span data-ttu-id="427ec-164">本機埠：動態 RPC</span><span class="sxs-lookup"><span data-stu-id="427ec-164">Local port: Dynamic RPC</span></span></dd> <dd><span data-ttu-id="427ec-165">遠端埠：全部</span><span class="sxs-lookup"><span data-stu-id="427ec-165">Remote port: ALL</span></span></dd> <dd><span data-ttu-id="427ec-166">通訊協定編號：6</span><span class="sxs-lookup"><span data-stu-id="427ec-166">Protocol number: 6</span></span></dd> <dd><span data-ttu-id="427ec-167">可執行檔：% windir% \\ system32 \\dllhost.exe</span><span class="sxs-lookup"><span data-stu-id="427ec-167">Executable: %windir%\\system32\\dllhost.exe</span></span></dd> <dd><span data-ttu-id="427ec-168">遠端許可權：系統管理員</span><span class="sxs-lookup"><span data-stu-id="427ec-168">Remote privilege: Administrator</span></span></dd> </dl> </dd> </dl>

<span data-ttu-id="427ec-169">下列清單包含可用於設定 Windows 防火牆設定的工具：</span><span class="sxs-lookup"><span data-stu-id="427ec-169">The following list contains tools that can be used to configure Windows Firewall settings:</span></span>

-   <span data-ttu-id="427ec-170">[具有進階安全性的 Windows 防火牆] 嵌入式管理單元</span><span class="sxs-lookup"><span data-stu-id="427ec-170">Windows Firewall with Advanced Security snap-in</span></span>
-   <span data-ttu-id="427ec-171">群組原則</span><span class="sxs-lookup"><span data-stu-id="427ec-171">Group Policy</span></span>
-   <span data-ttu-id="427ec-172">Netsh advfirewall 命令列工具</span><span class="sxs-lookup"><span data-stu-id="427ec-172">Netsh advfirewall command-line tool</span></span>

<span data-ttu-id="427ec-173">如需如何使用工具來設定 Windows 防火牆設定的詳細資訊，請參閱使用 [具有 Advanced Security 的 Windows 防火牆開始使用](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc748991(v=ws.10))。</span><span class="sxs-lookup"><span data-stu-id="427ec-173">For more information about how to use tools to configure Windows Firewall settings, see [Getting Started with Windows Firewall with Advanced Security](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc748991(v=ws.10)).</span></span>

 

 
