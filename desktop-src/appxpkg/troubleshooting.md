---
title: 對 Windows 應用程式的封裝、部署及查詢進行疑難排解
description: 使用這些建議來針對封裝、部署或查詢應用程式封裝時所遇到的問題進行疑難排解。
ms.assetid: 38E327C6-0345-4FA6-BCDB-5FA2FCD421FB
ms.topic: article
ms.date: 02/20/2020
manager: dcscontentpm
ms.custom:
- CI 111497
- CSSTroubleshooting
- contperf-fy21q2
ms.openlocfilehash: a2ee7c28e7de2d616bd01e9b5cae0de3c325caf4
ms.sourcegitcommit: 80198645ddacc3c12c72f3814b71ade0f415e705
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/25/2021
ms.locfileid: "106993689"
---
# <a name="troubleshooting-packaging-deployment-and-query-of-windows-apps"></a><span data-ttu-id="b7bc4-103">對 Windows 應用程式的封裝、部署及查詢進行疑難排解</span><span class="sxs-lookup"><span data-stu-id="b7bc4-103">Troubleshooting packaging, deployment, and query of Windows apps</span></span>

<span data-ttu-id="b7bc4-104">使用這些建議來針對您在封裝、部署或查詢 Windows 應用程式套件時所遇到的問題進行疑難排解 ( msix/.appx) 開發人員。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-104">Use these suggestions to troubleshoot problems you experience when packaging, deploying, or querying a Windows app package (.msix/.appx) as a developer.</span></span>

> [!NOTE]
> <span data-ttu-id="b7bc4-105">本文適用于開發人員。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-105">This article is intended for developers.</span></span> <span data-ttu-id="b7bc4-106">如果您不是開發人員，而且您正在尋找 Windows 應用程式安裝錯誤的說明，請參閱 [windows 支援](https://support.microsoft.com/hub/4338813/windows-help?os=windows-10)。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-106">If you are not a developer and you are looking for help with a Windows app installation error, see [Windows support](https://support.microsoft.com/hub/4338813/windows-help?os=windows-10).</span></span>

## <a name="get-diagnostic-information"></a><span data-ttu-id="b7bc4-107">取得診斷資訊</span><span class="sxs-lookup"><span data-stu-id="b7bc4-107">Get diagnostic information</span></span>

<span data-ttu-id="b7bc4-108">當 API 失敗時，它會傳回描述問題的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-108">When an API fails, it returns an error code that describes the problem.</span></span> <span data-ttu-id="b7bc4-109">如果錯誤碼未提供足夠的資訊，您可以在詳細的事件記錄檔中找到更多診斷資訊。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-109">If the error code doesn't provide enough information, you find more diagnostic information in the detailed event logs.</span></span>

<span data-ttu-id="b7bc4-110">若要使用 **事件檢視器** 來存取封裝和部署事件記錄檔，請遵循下列步驟：</span><span class="sxs-lookup"><span data-stu-id="b7bc4-110">To access the packaging and deployment event logs by using **Event Viewer**, follow these steps:</span></span>

1. <span data-ttu-id="b7bc4-111">請執行下列其中一個步驟：</span><span class="sxs-lookup"><span data-stu-id="b7bc4-111">Perform one of the following steps:</span></span>

    * <span data-ttu-id="b7bc4-112">按一下 [Windows] 功能表上的 [ **開始** ]，輸入 **事件檢視器**，然後 **按 enter**。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-112">Click **Start** on the Windows menu, type **Event Viewer**, and **press Enter**.</span></span>
    * <span data-ttu-id="b7bc4-113">執行 **eventvwr.msc services.msc**。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-113">Run **eventvwr.msc**.</span></span>

2. <span data-ttu-id="b7bc4-114">在左側頁面中，展開 [**本機)**  >  **應用程式和服務記錄** 檔] 事件檢視器 ( >  **Microsoft**  >  **Windows**。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-114">In the left page, expand **Event Viewer (Local)** > **Applications and Services Logs** > **Microsoft** > **Windows**.</span></span>
3. <span data-ttu-id="b7bc4-115">檢查下列類別的可用記錄：</span><span class="sxs-lookup"><span data-stu-id="b7bc4-115">Check for available logs under these categories:</span></span>

    * <span data-ttu-id="b7bc4-116">**AppxPackagingOM**  > **Microsoft-Windows-AppxPackaging/Operational**</span><span class="sxs-lookup"><span data-stu-id="b7bc4-116">**AppxPackagingOM** > **Microsoft-Windows-AppxPackaging/Operational**</span></span>
    * <span data-ttu-id="b7bc4-117">**Appxdeployment-server-伺服器**  > **Microsoft-Windows-AppXDeploymentServer/Operational**</span><span class="sxs-lookup"><span data-stu-id="b7bc4-117">**AppXDeployment-Server** > **Microsoft-Windows-AppXDeploymentServer/Operational**</span></span>

<span data-ttu-id="b7bc4-118">從查看 **appxdeployment-server-Server** 底下的記錄開始。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-118">Start by looking at the logs under **AppXDeployment-Server**.</span></span> <span data-ttu-id="b7bc4-119">如果錯誤是由 **0x80073CF0** 或 **ERROR_INSTALL_OPEN_PACKAGE_FAILED** 所造成，則 **AppxpackagingOM** 記錄中可能會有其他詳細資料。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-119">If the error was caused by **0x80073CF0** or **ERROR_INSTALL_OPEN_PACKAGE_FAILED**, additional details may be present in the **AppxpackagingOM** logs.</span></span>

<span data-ttu-id="b7bc4-120">您也可以使用 PowerShell 中的 [AppxLog](/powershell/module/appx/get-appxlog) 命令取得前幾個記錄的事件。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-120">You can also use the [Get-AppxLog](/powershell/module/appx/get-appxlog) command in PowerShell to get the first few logged events.</span></span> <span data-ttu-id="b7bc4-121">下列範例會顯示與最近部署作業相關聯的記錄檔。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-121">The following example displays the logs associated with the most recent deployment operation.</span></span>

```PowerShell
Get-Appxlog
```

<span data-ttu-id="b7bc4-122">下列範例會在另一個視窗中，顯示與互動式資料表中最新部署作業相關聯的記錄檔。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-122">The following example displays the logs associated with the most recent deployment operation in an interactive table in a separate window.</span></span>

```PowerShell
Get-Appxlog | Out-GridView
```

## <a name="common-error-codes"></a><span data-ttu-id="b7bc4-123">常見的錯誤碼</span><span class="sxs-lookup"><span data-stu-id="b7bc4-123">Common error codes</span></span>

<span data-ttu-id="b7bc4-124">下表列出一些最常見的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-124">This table lists some of the most common error codes.</span></span> <span data-ttu-id="b7bc4-125">如果您需要這些錯誤之一的進一步協助，或如果您遇到不在此清單中的錯誤碼，請參閱 [其他說明選項](#get-additional-help)。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-125">If you need further help with one of these errors, or if you're encountering an error code not in this list, see [additional help options](#get-additional-help).</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b7bc4-126">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="b7bc4-126">Error code</span></span></th>
<th><span data-ttu-id="b7bc4-127">值</span><span class="sxs-lookup"><span data-stu-id="b7bc4-127">Value</span></span></th>
<th><span data-ttu-id="b7bc4-128">描述與可能的原因</span><span class="sxs-lookup"><span data-stu-id="b7bc4-128">Description and possible causes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="even">
<td><span data-ttu-id="b7bc4-129"><strong>E_FILENOTFOUND</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-129"><strong>E_FILENOTFOUND</strong></span></span></td>
<td><span data-ttu-id="b7bc4-130">0x80070002</span><span class="sxs-lookup"><span data-stu-id="b7bc4-130">0x80070002</span></span></td>
<td><span data-ttu-id="b7bc4-131">找不到檔案或路徑。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-131">File or path is not found.</span></span> <span data-ttu-id="b7bc4-132">這可能發生在 COM typelib 驗證期間，目錄的路徑實際上必須存在於您的 MSIX 套件中。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-132">This can occur during a COM  typelib validation requires that the path for the directory actually exist within your MSIX package.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b7bc4-133"><strong>ERROR_BAD_FORMAT</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-133"><strong>ERROR_BAD_FORMAT</strong></span></span></td>
<td><span data-ttu-id="b7bc4-134">0x8007000B</span><span class="sxs-lookup"><span data-stu-id="b7bc4-134">0x8007000B</span></span></td>
<td><span data-ttu-id="b7bc4-135">封裝的格式不正確，需要重新建立或重新簽署。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-135">The package isn't correctly formatted and needs to be re-built or re-signed.</span></span><br/> <span data-ttu-id="b7bc4-136">如果簽署憑證主體名稱與 AppxManifest.xml 發行者名稱不相符，您可能會收到此錯誤。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-136">You may get this error if there is a mismatch between the signing certificate subject name and the AppxManifest.xml publisher name.</span></span><br/> <span data-ttu-id="b7bc4-137">請參閱 <a href="how-to-sign-a-package-using-signtool.md">如何使用 SignTool 簽署應用程式套件</a>。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-137">See <a href="how-to-sign-a-package-using-signtool.md">How to sign an app package using SignTool</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b7bc4-138"><strong>E_INVALIDARG</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-138"><strong>E_INVALIDARG</strong></span></span></td>
<td><span data-ttu-id="b7bc4-139">0x80070057</span><span class="sxs-lookup"><span data-stu-id="b7bc4-139">0x80070057</span></span></td>
<td><span data-ttu-id="b7bc4-140">一或多個引數無效。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-140">One or more arguments are not valid.</span></span> <span data-ttu-id="b7bc4-141">如果您檢查 AppXDeployment-Server 事件記錄檔，並看到下列事件：「安裝封裝時，系統無法登錄 repositoryExtension 副檔名，因為發生下列錯誤：參數不正確。」</span><span class="sxs-lookup"><span data-stu-id="b7bc4-141">If you check the AppXDeployment-Server event log and see the following event: "While installing the package, the system failed to register the windows.repositoryExtension extension due to the following error: The parameter is incorrect."</span></span> <br/> <span data-ttu-id="b7bc4-142">如果資訊清單元素 DisplayName 或 Description 包含 Windows 防火牆不允許的字元，您可能會收到這個錯誤;亦即 | 而且全部都是因為 Windows 無法建立套件的 AppContainer 設定檔。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-142">You may get this error if the manifest elements DisplayName or Description contain characters disallowed by Windows firewall; namely  |  and  all , due to which Windows fails to create the AppContainer profile for the package.</span></span> <span data-ttu-id="b7bc4-143">請從資訊清單移除這些字元，並嘗試安裝套件。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-143">Please remove these characters from the manifest and try installing the package.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b7bc4-144"><strong>ERROR_INSTALL_OPEN_</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-144"><strong>ERROR_INSTALL_OPEN_</strong></span></span><br/> <span data-ttu-id="b7bc4-145"><strong>PACKAGE_FAILED</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-145"><strong>PACKAGE_FAILED</strong></span></span><br/></td>
<td><span data-ttu-id="b7bc4-146">0x80073CF0</span><span class="sxs-lookup"><span data-stu-id="b7bc4-146">0x80073CF0</span></span></td>
<td><span data-ttu-id="b7bc4-147">無法開啟封裝。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-147">The package couldn't be opened.</span></span><br/> <span data-ttu-id="b7bc4-148">可能的原因：</span><span class="sxs-lookup"><span data-stu-id="b7bc4-148">Possible causes:</span></span><br/>
<ul>
<li><span data-ttu-id="b7bc4-149">套件未經簽署。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-149">The package is unsigned.</span></span></li>
<li><span data-ttu-id="b7bc4-150">發行者名稱與簽署憑證主體不符。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-150">The publisher name doesn't match the signing certificate subject.</span></span></li>
<li><span data-ttu-id="b7bc4-151">遺漏 file://前置詞，或在指定的位置找不到封裝。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-151">The file:// prefix is missing or the package couldn't be found at the specified location.</span></span></li>
</ul>
<span data-ttu-id="b7bc4-152">如需詳細資訊，請檢查 <strong>AppxPackagingOM</strong> 事件記錄檔。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-152">For more information, check the <strong>AppxPackagingOM</strong> event log.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b7bc4-153"><strong>ERROR_INSTALL_PACKAGE_</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-153"><strong>ERROR_INSTALL_PACKAGE_</strong></span></span><br/> <span data-ttu-id="b7bc4-154"><strong>NOT_FOUND</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-154"><strong>NOT_FOUND</strong></span></span><br/></td>
<td><span data-ttu-id="b7bc4-155">0x80073CF1</span><span class="sxs-lookup"><span data-stu-id="b7bc4-155">0x80073CF1</span></span></td>
<td><span data-ttu-id="b7bc4-156">找不到封裝。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-156">The package couldn't be found.</span></span><br/> <span data-ttu-id="b7bc4-157">移除目前使用者未安裝的封裝時，您可能會收到此錯誤。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-157">You may get this error while removing a package that isn't installed for the current user.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b7bc4-158"><strong>ERROR_INSTALL_INVALID_</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-158"><strong>ERROR_INSTALL_INVALID_</strong></span></span><br/> <span data-ttu-id="b7bc4-159"><strong>包</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-159"><strong>PACKAGE</strong></span></span><br/></td>
<td><span data-ttu-id="b7bc4-160">0x80073CF2</span><span class="sxs-lookup"><span data-stu-id="b7bc4-160">0x80073CF2</span></span></td>
<td><span data-ttu-id="b7bc4-161">封裝資料無效。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-161">The package data isn't valid.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b7bc4-162"><strong>ERROR_INSTALL_RESOLVE_</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-162"><strong>ERROR_INSTALL_RESOLVE_</strong></span></span><br/> <span data-ttu-id="b7bc4-163"><strong>DEPENDENCY_FAILED</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-163"><strong>DEPENDENCY_FAILED</strong></span></span><br/></td>
<td><span data-ttu-id="b7bc4-164">0x80073CF3</span><span class="sxs-lookup"><span data-stu-id="b7bc4-164">0x80073CF3</span></span></td>
<td><span data-ttu-id="b7bc4-165">套件無法通過更新、相依性或衝突的驗證。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-165">The package failed update, dependency, or conflict validation.</span></span><br/> <span data-ttu-id="b7bc4-166">可能的原因：</span><span class="sxs-lookup"><span data-stu-id="b7bc4-166">Possible causes:</span></span><br/>
<ul>
<li><span data-ttu-id="b7bc4-167">傳入的套件與安裝的套件衝突。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-167">The incoming package conflicts with an installed package.</span></span></li>
<li><span data-ttu-id="b7bc4-168">找不到指定的套件相依性。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-168">A specified package dependency can't be found.</span></span></li>
<li><span data-ttu-id="b7bc4-169">套件不支援正確的處理器架構。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-169">The package doesn't support the correct processor architecture.</span></span></li>
</ul>
<span data-ttu-id="b7bc4-170">如需詳細資訊，請檢查 <strong>Appxdeployment-server 伺服器</strong> 事件記錄檔。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-170">For more informtion, check the <strong>AppXDeployment-Server</strong> event log.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b7bc4-171"><strong>ERROR_INSTALL_OUT_</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-171"><strong>ERROR_INSTALL_OUT_</strong></span></span><br/> <span data-ttu-id="b7bc4-172"><strong>OF_DISK_SPACE</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-172"><strong>OF_DISK_SPACE</strong></span></span><br/></td>
<td><span data-ttu-id="b7bc4-173">0x80073CF4</span><span class="sxs-lookup"><span data-stu-id="b7bc4-173">0x80073CF4</span></span></td>
<td><span data-ttu-id="b7bc4-174">您的電腦上沒有足夠的磁碟空間。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-174">There isn't enough disk space on your computer.</span></span> <span data-ttu-id="b7bc4-175">請釋放一些空間，然後再試一次。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-175">Free some space and try again.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b7bc4-176"><strong>ERROR_INSTALL_NETWORK_</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-176"><strong>ERROR_INSTALL_NETWORK_</strong></span></span><br/> <span data-ttu-id="b7bc4-177"><strong>失敗</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-177"><strong>FAILURE</strong></span></span><br/></td>
<td><span data-ttu-id="b7bc4-178">0x80073CF5</span><span class="sxs-lookup"><span data-stu-id="b7bc4-178">0x80073CF5</span></span></td>
<td><span data-ttu-id="b7bc4-179">無法下載套件。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-179">The package can't be downloaded.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b7bc4-180"><strong>ERROR_INSTALL_</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-180"><strong>ERROR_INSTALL_</strong></span></span><br/> <span data-ttu-id="b7bc4-181"><strong>REGISTRATION_FAILURE</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-181"><strong>REGISTRATION_FAILURE</strong></span></span><br/></td>
<td><span data-ttu-id="b7bc4-182">0x80073CF6</span><span class="sxs-lookup"><span data-stu-id="b7bc4-182">0x80073CF6</span></span></td>
<td><span data-ttu-id="b7bc4-183">無法註冊封裝。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-183">The package can't be registered.</span></span><br/> <span data-ttu-id="b7bc4-184">如需詳細資訊，請查看 <strong>Appxdeployment-server 伺服器</strong> 事件記錄檔。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-184">For more information, check the <strong>AppXDeployment-Server</strong> event log.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b7bc4-185"><strong>ERROR_INSTALL_</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-185"><strong>ERROR_INSTALL_</strong></span></span><br/> <span data-ttu-id="b7bc4-186"><strong>DEREGISTRATION_EFAILURE</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-186"><strong>DEREGISTRATION_EFAILURE</strong></span></span><br/></td>
<td><span data-ttu-id="b7bc4-187">0x80073CF7</span><span class="sxs-lookup"><span data-stu-id="b7bc4-187">0x80073CF7</span></span></td>
<td><span data-ttu-id="b7bc4-188">無法取消註冊封裝。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-188">The package can't be unregistered.</span></span><br/> <span data-ttu-id="b7bc4-189">移除封裝時，您可能會收到此錯誤。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-189">You may get this error while removing a package.</span></span><br/> <span data-ttu-id="b7bc4-190">如需詳細資訊，請查看 <strong>Appxdeployment-server 伺服器</strong> 事件記錄檔。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-190">For more information, check the <strong>AppXDeployment-Server</strong> event log.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b7bc4-191"><strong>ERROR_INSTALL_CANCEL</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-191"><strong>ERROR_INSTALL_CANCEL</strong></span></span></td>
<td><span data-ttu-id="b7bc4-192">0x80073CF8</span><span class="sxs-lookup"><span data-stu-id="b7bc4-192">0x80073CF8</span></span></td>
<td><span data-ttu-id="b7bc4-193">使用者已取消安裝要求。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-193">The user canceled the install request.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b7bc4-194"><strong>ERROR_INSTALL_FAILED</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-194"><strong>ERROR_INSTALL_FAILED</strong></span></span></td>
<td><span data-ttu-id="b7bc4-195">0x80073CF9</span><span class="sxs-lookup"><span data-stu-id="b7bc4-195">0x80073CF9</span></span></td>
<td><span data-ttu-id="b7bc4-196">套件安裝失敗。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-196">Package install failed.</span></span> <span data-ttu-id="b7bc4-197">洽詢軟體廠商。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-197">Contact the software vendor.</span></span><br/> <span data-ttu-id="b7bc4-198">如需詳細資訊，請查看 <strong>Appxdeployment-server 伺服器</strong> 事件記錄檔。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-198">For more information, check the <strong>AppXDeployment-Server</strong> event log.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b7bc4-199"><strong>ERROR_REMOVE_FAILED</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-199"><strong>ERROR_REMOVE_FAILED</strong></span></span></td>
<td><span data-ttu-id="b7bc4-200">0x80073CFA</span><span class="sxs-lookup"><span data-stu-id="b7bc4-200">0x80073CFA</span></span></td>
<td><span data-ttu-id="b7bc4-201">封裝移除失敗。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-201">Package removal failed.</span></span><br/> <span data-ttu-id="b7bc4-202">您可能會收到此錯誤，指出在套件卸載期間發生的失敗。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-202">You may get this error for failures that occur during package uninstall.</span></span><br/> <span data-ttu-id="b7bc4-203">如需詳細資訊，請參閱 <a href="/uwp/api/windows.management.deployment.packagemanager.removepackageasync"><strong>RemovePackageAsync</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-203">For more information, see <a href="/uwp/api/windows.management.deployment.packagemanager.removepackageasync"><strong>RemovePackageAsync</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b7bc4-204"><strong>ERROR_PACKAGE_</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-204"><strong>ERROR_PACKAGE_</strong></span></span><br/> <span data-ttu-id="b7bc4-205"><strong>ALREADY_EXISTS</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-205"><strong>ALREADY_EXISTS</strong></span></span><br/></td>
<td><span data-ttu-id="b7bc4-206">0x80073CFB</span><span class="sxs-lookup"><span data-stu-id="b7bc4-206">0x80073CFB</span></span></td>
<td><span data-ttu-id="b7bc4-207">已安裝所提供的套件，因此無法重新安裝該套件。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-207">The provided package is already installed, and reinstallation of the package is blocked.</span></span> <br/> <span data-ttu-id="b7bc4-208">如果您安裝的套件與已經安裝的套件不符，您可能會收到這個錯誤。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-208">You may get this error if installing a package that is not bitwise identical to the package that is already installed.</span></span> <span data-ttu-id="b7bc4-209">請注意，數位簽章也是封裝的一部分。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-209">Note that the digital signature is also part of the package.</span></span> <span data-ttu-id="b7bc4-210">因此，如果已重建或重新簽署套件，它就不再與先前安裝的封裝位相同。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-210">Hence if a package is rebuilt or resigned, it is no longer bitwise identical to the previously installed package.</span></span> <span data-ttu-id="b7bc4-211">有兩個可修正此錯誤的可能選項： (1) 遞增應用程式的版本號碼，然後重建並重新簽署封裝 (2) 移除系統上每個使用者的舊套件，再安裝新的套件。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-211">Two possible options to fix this error are: (1) Increment the version number of the app, then rebuild and resign the package (2) Remove the old package for every user on the system before installing the new package.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b7bc4-212"><strong>ERROR_NEEDS_REMEDIATION</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-212"><strong>ERROR_NEEDS_REMEDIATION</strong></span></span></td>
<td><span data-ttu-id="b7bc4-213">0x80073CFC</span><span class="sxs-lookup"><span data-stu-id="b7bc4-213">0x80073CFC</span></span></td>
<td><span data-ttu-id="b7bc4-214">無法啟動應用程式。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-214">The app can't be started.</span></span> <span data-ttu-id="b7bc4-215">請嘗試重新安裝應用程式。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-215">Try reinstalling the app.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b7bc4-216"><strong>ERROR_INSTALL_</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-216"><strong>ERROR_INSTALL_</strong></span></span><br/> <span data-ttu-id="b7bc4-217"><strong>PREREQUISITE_FAILED</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-217"><strong>PREREQUISITE_FAILED</strong></span></span><br/></td>
<td><span data-ttu-id="b7bc4-218">0x80073CFD</span><span class="sxs-lookup"><span data-stu-id="b7bc4-218">0x80073CFD</span></span></td>
<td><span data-ttu-id="b7bc4-219">無法滿足指定的安裝先決條件。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-219">A specified install prerequisite couldn't be satisfied.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b7bc4-220"><strong>ERROR_PACKAGE_</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-220"><strong>ERROR_PACKAGE_</strong></span></span><br/> <span data-ttu-id="b7bc4-221"><strong>REPOSITORY_CORRUPTED</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-221"><strong>REPOSITORY_CORRUPTED</strong></span></span><br/></td>
<td><span data-ttu-id="b7bc4-222">0x80073CFE</span><span class="sxs-lookup"><span data-stu-id="b7bc4-222">0x80073CFE</span></span></td>
<td><span data-ttu-id="b7bc4-223">套件存放庫已損毀。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-223">The package repository is corrupted.</span></span><br/> <span data-ttu-id="b7bc4-224">如果此登錄機碼參考的資料夾不存在或已損毀，您可能會收到此錯誤：</span><span class="sxs-lookup"><span data-stu-id="b7bc4-224">You may get this error if the folder referenced by this registry key doesn't exist or is corrupted:</span></span> <br/> <span data-ttu-id="b7bc4-225"><strong>HKLM\Software\Microsoft\Windows</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-225"><strong>HKLM\Software\Microsoft\Windows\</strong></span></span><br/> <span data-ttu-id="b7bc4-226"><strong>CurrentVersion\Appx\PackageRepositoryRoot</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-226"><strong>CurrentVersion\Appx\PackageRepositoryRoot</strong></span></span><br/> <span data-ttu-id="b7bc4-227">若要從此狀態復原，請重新整理您的電腦。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-227">To recover from this state, refresh your PC.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b7bc4-228"><strong>ERROR_INSTALL_</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-228"><strong>ERROR_INSTALL_</strong></span></span><br/> <span data-ttu-id="b7bc4-229"><strong>POLICY_FAILURE</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-229"><strong>POLICY_FAILURE</strong></span></span><br/></td>
<td><span data-ttu-id="b7bc4-230">0x80073CFF</span><span class="sxs-lookup"><span data-stu-id="b7bc4-230">0x80073CFF</span></span></td>
<td><span data-ttu-id="b7bc4-231">若要安裝此應用程式，您需要開發人員授權或啟用側載功能的系統。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-231">To install this app, you need a developer license or a sideloading-enabled system.</span></span> <br/> <span data-ttu-id="b7bc4-232">如果套件不符合下列其中一項需求，您可能會收到此錯誤：</span><span class="sxs-lookup"><span data-stu-id="b7bc4-232">You may get this error if the package doesn't meet one of the following requirements:</span></span><br/>
<ul>
<li><span data-ttu-id="b7bc4-233">應用程式會使用 F5 在具有 Windows 開發人員授權的電腦上 Visual Studio 中進行部署。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-233">The app is deployed using F5 in Visual Studio on a computer with a Windows developer license.</span></span></li>
<li><span data-ttu-id="b7bc4-234">封裝會使用 Microsoft 簽章簽署，並部署為 Windows 或 Microsoft Store 的一部分。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-234">The package is signed with a Microsoft signature and deployed as part of Windows or from the Microsoft Store.</span></span></li>
<li><span data-ttu-id="b7bc4-235">封裝會以信任的簽章簽署，並安裝在具有開發人員授權的電腦上、已啟用 AllowAllTrustedApps 原則的已加入網域電腦，或是已啟用 AllowAllTrustedApps 原則的 Windows 側載授權電腦上。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-235">The package is signed with a trusted signature and installed on a computer with a developer license, a domain-joined computer with the AllowAllTrustedApps policy enabled, or a computer with a Windows Sideloading license with the AllowAllTrustedApps policy enabled.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b7bc4-236"><strong>ERROR_PACKAGE_UPDATING</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-236"><strong>ERROR_PACKAGE_UPDATING</strong></span></span></td>
<td><span data-ttu-id="b7bc4-237">0x80073D00</span><span class="sxs-lookup"><span data-stu-id="b7bc4-237">0x80073D00</span></span></td>
<td><span data-ttu-id="b7bc4-238">因為應用程式目前正在更新，所以無法啟動。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-238">The app can't be started because it's currently updating.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b7bc4-239"><strong>ERROR_DEPLOYMENT_</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-239"><strong>ERROR_DEPLOYMENT_</strong></span></span><br/> <span data-ttu-id="b7bc4-240"><strong>BLOCKED_BY_POLICY</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-240"><strong>BLOCKED_BY_POLICY</strong></span></span><br/></td>
<td><span data-ttu-id="b7bc4-241">0x80073D01</span><span class="sxs-lookup"><span data-stu-id="b7bc4-241">0x80073D01</span></span></td>
<td><span data-ttu-id="b7bc4-242">原則封鎖了封裝部署作業。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-242">The package deployment operation is blocked by policy.</span></span> <span data-ttu-id="b7bc4-243">請連絡您的系統管理員。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-243">Contact your system administrator.</span></span><br/> <span data-ttu-id="b7bc4-244">可能的原因：</span><span class="sxs-lookup"><span data-stu-id="b7bc4-244">Possible causes:</span></span><br/>
<ul>
<li><span data-ttu-id="b7bc4-245">應用程式控制原則封鎖了封裝部署。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-245">Package deployment is blocked by Application Control Policies.</span></span></li>
<li><span data-ttu-id="b7bc4-246">封裝部署會被 [ &quot; 允許特殊設定檔中的部署作業] &quot; 原則封鎖。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-246">Package deployment is blocked by the &quot;Allow deployment operations in special profiles&quot; policy.</span></span></li>
</ul>
<span data-ttu-id="b7bc4-247">其中一個可能的原因是漫遊設定檔的需求。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-247">One of the possible reasons is a need for a roaming profile.</span></span> <span data-ttu-id="b7bc4-248">如需有關在使用者帳戶上設定漫遊使用者設定檔的詳細資訊，請參閱 <a href="/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/jj649079(v=ws.11)">部署漫遊使用者設定檔</a>。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-248">For information about setting up Roaming User Profiles on user accounts, see <a href="/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/jj649079(v=ws.11)">Deploy Roaming User Profiles</a>.</span></span> <span data-ttu-id="b7bc4-249">如果您的系統上未設定任何原則，而且您仍然看到此錯誤，可能是您以暫存設定檔登入。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-249">If there are no policies configured on your system and you still see this error, perhaps you are logged in with a temporary profile.</span></span> <span data-ttu-id="b7bc4-250">請登出再重新登入，然後再次嘗試操作。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-250">Log out and log in again, then try the operation again.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b7bc4-251"><strong>ERROR_PACKAGES_IN_USE</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-251"><strong>ERROR_PACKAGES_IN_USE</strong></span></span></td>
<td><span data-ttu-id="b7bc4-252">0x80073D02</span><span class="sxs-lookup"><span data-stu-id="b7bc4-252">0x80073D02</span></span></td>
<td><span data-ttu-id="b7bc4-253">無法安裝封裝，因為它修改的資源目前正在使用中。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-253">The package couldn't be installed because resources it modifies are currently in use.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b7bc4-254"><strong>ERROR_RECOVERY_</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-254"><strong>ERROR_RECOVERY_</strong></span></span><br/> <span data-ttu-id="b7bc4-255"><strong>FILE_CORRUPT</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-255"><strong>FILE_CORRUPT</strong></span></span><br/></td>
<td><span data-ttu-id="b7bc4-256">0x80073D03</span><span class="sxs-lookup"><span data-stu-id="b7bc4-256">0x80073D03</span></span></td>
<td><span data-ttu-id="b7bc4-257">無法復原封裝，因為復原所需的資料已損毀。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-257">The package couldn't be recovered because data that's necessary for recovery is corrupted.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b7bc4-258"><strong>ERROR_INVALID_</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-258"><strong>ERROR_INVALID_</strong></span></span><br/> <span data-ttu-id="b7bc4-259"><strong>STAGED_SIGNATURE</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-259"><strong>STAGED_SIGNATURE</strong></span></span><br/></td>
<td><span data-ttu-id="b7bc4-260">0x80073D04</span><span class="sxs-lookup"><span data-stu-id="b7bc4-260">0x80073D04</span></span></td>
<td><span data-ttu-id="b7bc4-261">簽章無效。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-261">The signature isn't valid.</span></span> <span data-ttu-id="b7bc4-262">若要在開發人員模式下註冊，Appxsignature.p7x. appxsignature.p7x 和 AppxBlockMap.xml 必須有效或不應該存在。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-262">To register in developer mode, AppxSignature.p7x and AppxBlockMap.xml must be valid or shouldn't be present.</span></span><br/> <span data-ttu-id="b7bc4-263">如果您是使用 F5 搭配 Visual Studio 的開發人員，請確定您建立的專案目錄不包含舊版封裝的簽章或區塊對應檔案。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-263">If you are a developer using F5 with Visual Studio, ensure that your built project directory doesn't contain signature or block map files from previous versions of the package.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b7bc4-264"><strong>ERROR_DELETING_EXISTING_</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-264"><strong>ERROR_DELETING_EXISTING_</strong></span></span><br/> <span data-ttu-id="b7bc4-265"><strong>APPLICATIONDATA_STORE_FAILED</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-265"><strong>APPLICATIONDATA_STORE_FAILED</strong></span></span><br/></td>
<td><span data-ttu-id="b7bc4-266">0x80073D05</span><span class="sxs-lookup"><span data-stu-id="b7bc4-266">0x80073D05</span></span></td>
<td><span data-ttu-id="b7bc4-267">刪除封裝先前現有的應用程式資料時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-267">An error occurred while deleting the package's previously existing application data.</span></span><br/> <span data-ttu-id="b7bc4-268">如果 <a href="/previous-versions/hh441475(v=vs.110)">模擬器正在執行</a> ，您可能會收到此錯誤。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-268">You can get this error if the <a href="/previous-versions/hh441475(v=vs.110)">simulator</a> is running.</span></span> <span data-ttu-id="b7bc4-269">關閉模擬器。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-269">Close the simulator.</span></span> <span data-ttu-id="b7bc4-270">如果應用程式資料中有開啟的檔案，您也可以取得此錯誤 (例如，如果您在文字編輯器中開啟記錄檔) 。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-270">You can also get this error if there are files open in the app data (for example, if you have a log file open in a text editor).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b7bc4-271"><strong>ERROR_INSTALL_</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-271"><strong>ERROR_INSTALL_</strong></span></span><br/> <span data-ttu-id="b7bc4-272"><strong>PACKAGE_DOWNGRADE</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-272"><strong>PACKAGE_DOWNGRADE</strong></span></span><br/></td>
<td><span data-ttu-id="b7bc4-273">0x80073D06</span><span class="sxs-lookup"><span data-stu-id="b7bc4-273">0x80073D06</span></span></td>
<td><span data-ttu-id="b7bc4-274">無法安裝封裝，因為已安裝此套件的較高版本。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-274">The package couldn't be installed because a higher version of this package is already installed.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b7bc4-275"><strong>ERROR_SYSTEM_</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-275"><strong>ERROR_SYSTEM_</strong></span></span><br/> <span data-ttu-id="b7bc4-276"><strong>NEEDS_REMEDIATION</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-276"><strong>NEEDS_REMEDIATION</strong></span></span><br/></td>
<td><span data-ttu-id="b7bc4-277">0x80073D07</span><span class="sxs-lookup"><span data-stu-id="b7bc4-277">0x80073D07</span></span></td>
<td><span data-ttu-id="b7bc4-278">偵測到系統二進位檔中有錯誤。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-278">An error in a system binary was detected.</span></span> <span data-ttu-id="b7bc4-279">若要修正此問題，請嘗試重新整理電腦。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-279">To fix the problem, try refreshing the PC.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b7bc4-280"><strong>ERROR_APPX_INTEGRITY_</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-280"><strong>ERROR_APPX_INTEGRITY_</strong></span></span><br/> <span data-ttu-id="b7bc4-281"><strong>FAILURE_EXTERNAL</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-281"><strong>FAILURE_EXTERNAL</strong></span></span><br/></td>
<td><span data-ttu-id="b7bc4-282">0x80073D08</span><span class="sxs-lookup"><span data-stu-id="b7bc4-282">0x80073D08</span></span></td>
<td><span data-ttu-id="b7bc4-283">在系統上偵測到損毀的非 Windows 二進位檔。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-283">A corrupted non-Windows binary was detected on the system.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b7bc4-284"><strong>ERROR_RESILIENCY_</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-284"><strong>ERROR_RESILIENCY_</strong></span></span><br/> <span data-ttu-id="b7bc4-285"><strong>FILE_CORRUPT</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-285"><strong>FILE_CORRUPT</strong></span></span><br/></td>
<td><span data-ttu-id="b7bc4-286">0x80073D09</span><span class="sxs-lookup"><span data-stu-id="b7bc4-286">0x80073D09</span></span></td>
<td><span data-ttu-id="b7bc4-287">因為修復所需的資料已損毀，所以無法繼續操作。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-287">The operation couldn't be resumed because data that's necessary for recovery is corrupted.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b7bc4-288"><strong>ERROR_INSTALL_FIREWALL_</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-288"><strong>ERROR_INSTALL_FIREWALL_</strong></span></span><br/> <span data-ttu-id="b7bc4-289"><strong>SERVICE_NOT_RUNNING</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-289"><strong>SERVICE_NOT_RUNNING</strong></span></span><br/></td>
<td><span data-ttu-id="b7bc4-290">0x80073D0A</span><span class="sxs-lookup"><span data-stu-id="b7bc4-290">0x80073D0A</span></span></td>
<td><span data-ttu-id="b7bc4-291">無法安裝封裝，因為 Windows 防火牆服務未執行。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-291">The package couldn't be installed because the Windows Firewall service isn't running.</span></span> <span data-ttu-id="b7bc4-292">啟用 Windows 防火牆服務，然後再試一次。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-292">Enable the Windows Firewall service and try again.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b7bc4-293"><strong>ERROR_PACKAGE_MOVE_FAILED</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-293"><strong>ERROR_PACKAGE_MOVE_FAILED</strong></span></span></td>
<td><span data-ttu-id="b7bc4-294">0x80073D0B</span><span class="sxs-lookup"><span data-stu-id="b7bc4-294">0x80073D0B</span></span></td>
<td><span data-ttu-id="b7bc4-295">套件移動作業失敗。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-295">The package move operation failed.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b7bc4-296"><strong>ERROR_INSTALL_VOLUME_</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-296"><strong>ERROR_INSTALL_VOLUME_</strong></span></span><br/> <span data-ttu-id="b7bc4-297"><strong>NOT_EMPTY</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-297"><strong>NOT_EMPTY</strong></span></span><br/></td>
<td><span data-ttu-id="b7bc4-298">0x80073D0C</span><span class="sxs-lookup"><span data-stu-id="b7bc4-298">0x80073D0C</span></span></td>
<td><span data-ttu-id="b7bc4-299">部署作業失敗，因為磁片區不是空的。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-299">The deployment operation failed because the volume is not empty.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b7bc4-300"><strong>ERROR_INSTALL_VOLUME_</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-300"><strong>ERROR_INSTALL_VOLUME_</strong></span></span><br/> <span data-ttu-id="b7bc4-301"><strong>OFFLINE</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-301"><strong>OFFLINE</strong></span></span><br/></td>
<td><span data-ttu-id="b7bc4-302">0x80073D0D</span><span class="sxs-lookup"><span data-stu-id="b7bc4-302">0x80073D0D</span></span></td>
<td><span data-ttu-id="b7bc4-303">部署作業失敗，因為磁片區已離線。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-303">The deployment operation failed because the volume is offline.</span></span> <span data-ttu-id="b7bc4-304">針對套件更新，磁片區指的是所有套件版本的已安裝磁片區。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-304">For a package update, the volume refers to the installed volume of all package versions.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b7bc4-305"><strong>ERROR_INSTALL_VOLUME_</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-305"><strong>ERROR_INSTALL_VOLUME_</strong></span></span><br/> <span data-ttu-id="b7bc4-306"><strong>腐敗</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-306"><strong>CORRUPT</strong></span></span><br/></td>
<td><span data-ttu-id="b7bc4-307">0x80073D0E</span><span class="sxs-lookup"><span data-stu-id="b7bc4-307">0x80073D0E</span></span></td>
<td><span data-ttu-id="b7bc4-308">部署作業失敗，因為指定的磁片區已損毀。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-308">The deployment operation failed because the specified volume is corrupt.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b7bc4-309"><strong>ERROR_NEEDS_REGISTRATION</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-309"><strong>ERROR_NEEDS_REGISTRATION</strong></span></span><br/> <strong></strong><br/></td>
<td><span data-ttu-id="b7bc4-310">0x80073D0F</span><span class="sxs-lookup"><span data-stu-id="b7bc4-310">0x80073D0F</span></span></td>
<td><span data-ttu-id="b7bc4-311">部署作業失敗，因為指定的應用程式必須先註冊。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-311">The deployment operation failed because the specified application needs to be registered first.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b7bc4-312"><strong>ERROR_INSTALL_WRONG_</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-312"><strong>ERROR_INSTALL_WRONG_</strong></span></span><br/> <span data-ttu-id="b7bc4-313"><strong>PROCESSOR_ARCHITECTURE</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-313"><strong>PROCESSOR_ARCHITECTURE</strong></span></span><br/></td>
<td><span data-ttu-id="b7bc4-314">0x80073D10</span><span class="sxs-lookup"><span data-stu-id="b7bc4-314">0x80073D10</span></span></td>
<td><span data-ttu-id="b7bc4-315">部署作業失敗，因為封裝的目標處理器架構錯誤。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-315">The deployment operation failed because the package targets the wrong processor architecture.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b7bc4-316"><strong>ERROR_DEV_SIDELOAD_</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-316"><strong>ERROR_DEV_SIDELOAD_</strong></span></span><br/> <span data-ttu-id="b7bc4-317"><strong>LIMIT_EXCEEDED</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-317"><strong>LIMIT_EXCEEDED</strong></span></span><br/></td>
<td><span data-ttu-id="b7bc4-318">0x80073D11</span><span class="sxs-lookup"><span data-stu-id="b7bc4-318">0x80073D11</span></span></td>
<td><span data-ttu-id="b7bc4-319">您已達到此裝置上允許的最大開發人員側載封裝數目。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-319">You have reached the maximum number of developer sideloaded packages allowed on this device.</span></span> <span data-ttu-id="b7bc4-320">請卸載側載套件，然後再試一次。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-320">Please uninstall a sideloaded package and try again.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b7bc4-321"><strong>ERROR_INSTALL_OPTIONAL_</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-321"><strong>ERROR_INSTALL_OPTIONAL_</strong></span></span><br/> <span data-ttu-id="b7bc4-322"><strong>PACKAGE_REQUIRES_</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-322"><strong>PACKAGE_REQUIRES_</strong></span></span><br/> <span data-ttu-id="b7bc4-323"><strong>MAIN_PACKAGE</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-323"><strong>MAIN_PACKAGE</strong></span></span><br/></td>
<td><span data-ttu-id="b7bc4-324">0x80073D12</span><span class="sxs-lookup"><span data-stu-id="b7bc4-324">0x80073D12</span></span></td>
<td><span data-ttu-id="b7bc4-325">需要主要應用程式封裝，才能安裝此選用套件。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-325">A main app package is required to install this optional package.</span></span> <span data-ttu-id="b7bc4-326">請先安裝主要套件，然後再試一次。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-326">Install the main package first and try again.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b7bc4-327"><strong>ERROR_PACKAGE_NOT_</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-327"><strong>ERROR_PACKAGE_NOT_</strong></span></span><br/> <span data-ttu-id="b7bc4-328"><strong>SUPPORTED_ON_FILESYSTEM</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-328"><strong>SUPPORTED_ON_FILESYSTEM</strong></span></span><br/></td>
<td><span data-ttu-id="b7bc4-329">0x80073D13</span><span class="sxs-lookup"><span data-stu-id="b7bc4-329">0x80073D13</span></span></td>
<td><span data-ttu-id="b7bc4-330">此檔案系統不支援此應用程式套件類型。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-330">This app package type is not supported on this filesystem.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b7bc4-331"><strong>ERROR_PACKAGE_MOVE_</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-331"><strong>ERROR_PACKAGE_MOVE_</strong></span></span><br/> <span data-ttu-id="b7bc4-332"><strong>BLOCKED_BY_STREAMING</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-332"><strong>BLOCKED_BY_STREAMING</strong></span></span><br/></td>
<td><span data-ttu-id="b7bc4-333">0x80073D14</span><span class="sxs-lookup"><span data-stu-id="b7bc4-333">0x80073D14</span></span></td>
<td><span data-ttu-id="b7bc4-334">在應用程式完成串流處理之前，會封鎖「套件移動」作業。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-334">Package move operation is blocked until the application has finished streaming.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b7bc4-335"><strong>ERROR_INSTALL_OPTIONAL_</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-335"><strong>ERROR_INSTALL_OPTIONAL_</strong></span></span><br/> <span data-ttu-id="b7bc4-336"><strong>PACKAGE_APPLICATIONID_</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-336"><strong>PACKAGE_APPLICATIONID_</strong></span></span><br/> <span data-ttu-id="b7bc4-337"><strong>NOT_UNIQUE</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-337"><strong>NOT_UNIQUE</strong></span></span><br/></td>
<td><span data-ttu-id="b7bc4-338">0x80073D15</span><span class="sxs-lookup"><span data-stu-id="b7bc4-338">0x80073D15</span></span></td>
<td><span data-ttu-id="b7bc4-339">主要或另一個選用的應用程式套件與此選用套件具有相同的應用程式識別碼。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-339">A main or another optional app package has the same application ID as this optional package.</span></span> <span data-ttu-id="b7bc4-340">變更選用封裝的應用程式識別碼，以避免發生衝突。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-340">Change the application ID for the optional package to avoid conflicts.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b7bc4-341"><strong>ERROR_PACKAGE_STAGING_</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-341"><strong>ERROR_PACKAGE_STAGING_</strong></span></span><br/> <span data-ttu-id="b7bc4-342"><strong>舉 SERVICEREQUESTSTATUSENUM.ONHOLD</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-342"><strong>ONHOLD</strong></span></span><br/></td>
<td><span data-ttu-id="b7bc4-343">0x80073D16</span><span class="sxs-lookup"><span data-stu-id="b7bc4-343">0x80073D16</span></span></td>
<td><span data-ttu-id="b7bc4-344">已保留此暫存會話，以允許設定另一個預備作業的優先順序。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-344">This staging session has been held to allow another staging operation to be prioritized.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b7bc4-345"><strong>ERROR_INSTALL_INVALID_</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-345"><strong>ERROR_INSTALL_INVALID_</strong></span></span><br/> <span data-ttu-id="b7bc4-346"><strong>RELATED_SET_UPDATE</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-346"><strong>RELATED_SET_UPDATE</strong></span></span><br/></td>
<td><span data-ttu-id="b7bc4-347">0x80073D17</span><span class="sxs-lookup"><span data-stu-id="b7bc4-347">0x80073D17</span></span></td>
<td><span data-ttu-id="b7bc4-348">無法更新相關的集合，因為更新的集合無效。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-348">A related set cannot be updated because the updated set is invalid.</span></span> <span data-ttu-id="b7bc4-349">您必須同時更新相關集合中的所有套件。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-349">All packages in the related set must be updated at the same time.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b7bc4-350"><strong>ERROR_INSTALL_OPTIONAL_</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-350"><strong>ERROR_INSTALL_OPTIONAL_</strong></span></span><br/> <span data-ttu-id="b7bc4-351"><strong>PACKAGE_REQUIRES_MAIN_</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-351"><strong>PACKAGE_REQUIRES_MAIN_</strong></span></span><br/> <span data-ttu-id="b7bc4-352"><strong>PACKAGE_FULLTRUST_CAPABILITY</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-352"><strong>PACKAGE_FULLTRUST_CAPABILITY</strong></span></span><br/></td>
<td><span data-ttu-id="b7bc4-353">0x80073D18</span><span class="sxs-lookup"><span data-stu-id="b7bc4-353">0x80073D18</span></span></td>
<td><span data-ttu-id="b7bc4-354">具有 FullTrust 進入點的選用套件需要主要套件具有 <strong>runFullTrust</strong> 功能。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-354">An optional package with a FullTrust entry point requires the main package to have the <strong>runFullTrust</strong> capability.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b7bc4-355"><strong>ERROR_DEPLOYMENT_BLOCKED_</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-355"><strong>ERROR_DEPLOYMENT_BLOCKED_</strong></span></span><br/> <span data-ttu-id="b7bc4-356"><strong>BY_USER_LOG_OFF</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-356"><strong>BY_USER_LOG_OFF</strong></span></span><br/></td>
<td><span data-ttu-id="b7bc4-357">0x80073D19</span><span class="sxs-lookup"><span data-stu-id="b7bc4-357">0x80073D19</span></span></td>
<td><span data-ttu-id="b7bc4-358">發生錯誤，因為使用者已登出。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-358">An error occurred because a user was logged off.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b7bc4-359"><strong>ERROR_PROVISION_OPTIONAL_</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-359"><strong>ERROR_PROVISION_OPTIONAL_</strong></span></span><br/> <span data-ttu-id="b7bc4-360"><strong>PACKAGE_REQUIRES_MAIN_</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-360"><strong>PACKAGE_REQUIRES_MAIN_</strong></span></span><br/> <span data-ttu-id="b7bc4-361"><strong>PACKAGE_PROVISIONED</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-361"><strong>PACKAGE_PROVISIONED</strong></span></span><br/></td>
<td><span data-ttu-id="b7bc4-362">0x80073D1A</span><span class="sxs-lookup"><span data-stu-id="b7bc4-362">0x80073D1A</span></span></td>
<td><span data-ttu-id="b7bc4-363">選用套件布建也需要布建相依性主要套件。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-363">An optional package provision requires the dependency main package to also be provisioned.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b7bc4-364"><strong>ERROR_PACKAGES_REPUTATION_</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-364"><strong>ERROR_PACKAGES_REPUTATION_</strong></span></span><br/> <span data-ttu-id="b7bc4-365"><strong>CHECK_FAILED</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-365"><strong>CHECK_FAILED</strong></span></span><br/></td>
<td><span data-ttu-id="b7bc4-366">0x80073D1B</span><span class="sxs-lookup"><span data-stu-id="b7bc4-366">0x80073D1B</span></span></td>
<td><span data-ttu-id="b7bc4-367">這些套件無法進行 <a href="/windows/security/threat-protection/windows-defender-smartscreen/windows-defender-smartscreen-overview">SmartScreen 信譽檢查</a>。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-367">The packages failed the <a href="/windows/security/threat-protection/windows-defender-smartscreen/windows-defender-smartscreen-overview">SmartScreen reputation check</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b7bc4-368"><strong>ERROR_PACKAGES_REPUTATION_</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-368"><strong>ERROR_PACKAGES_REPUTATION_</strong></span></span><br/> <span data-ttu-id="b7bc4-369"><strong>CHECK_TIMEDOUT</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-369"><strong>CHECK_TIMEDOUT</strong></span></span><br/></td>
<td><span data-ttu-id="b7bc4-370">0x80073D1C</span><span class="sxs-lookup"><span data-stu-id="b7bc4-370">0x80073D1C</span></span></td>
<td><span data-ttu-id="b7bc4-371"><a href="/windows/security/threat-protection/windows-defender-smartscreen/windows-defender-smartscreen-overview">SmartScreen 信譽檢查</a>作業已超時。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-371">The <a href="/windows/security/threat-protection/windows-defender-smartscreen/windows-defender-smartscreen-overview">SmartScreen reputation check</a> operation timed out.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b7bc4-372"><strong>ERROR_DEPLOYMENT_OPTION_</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-372"><strong>ERROR_DEPLOYMENT_OPTION_</strong></span></span><br/> <span data-ttu-id="b7bc4-373"><strong>NOT_SUPPORTED</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-373"><strong>NOT_SUPPORTED</strong></span></span><br/></td>
<td><span data-ttu-id="b7bc4-374">0x80073D1D</span><span class="sxs-lookup"><span data-stu-id="b7bc4-374">0x80073D1D</span></span></td>
<td><span data-ttu-id="b7bc4-375">不支援目前的部署選項。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-375">The current deployment option is not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b7bc4-376"><strong>ERROR_APPINSTALLER_</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-376"><strong>ERROR_APPINSTALLER_</strong></span></span><br/> <span data-ttu-id="b7bc4-377"><strong>ACTI加值稅ION_BLOCKED</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-377"><strong>ACTIVATION_BLOCKED</strong></span></span><br/></td>
<td><span data-ttu-id="b7bc4-378">0x80073D1E</span><span class="sxs-lookup"><span data-stu-id="b7bc4-378">0x80073D1E</span></span></td>
<td><span data-ttu-id="b7bc4-379">因為此應用程式的 appinstaller 更新設定，所以已封鎖啟用。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-379">Activation is blocked due to the .appinstaller update settings for this app.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b7bc4-380"><strong>ERROR_REGISTRATION_FROM_</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-380"><strong>ERROR_REGISTRATION_FROM_</strong></span></span><br/> <span data-ttu-id="b7bc4-381"><strong>REMOTE_DRIVE_NOT_SUPPORTED</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-381"><strong>REMOTE_DRIVE_NOT_SUPPORTED</strong></span></span><br/></td>
<td><span data-ttu-id="b7bc4-382">0x80073D1F</span><span class="sxs-lookup"><span data-stu-id="b7bc4-382">0x80073D1F</span></span></td>
<td><span data-ttu-id="b7bc4-383">不支援遠端磁片磁碟機。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-383">Remote drives are not supported.</span></span> <span data-ttu-id="b7bc4-384">使用<strong> \\ server\share</strong>來註冊遠端封裝。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-384">Use <strong>\\server\share</strong> to register a remote package.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b7bc4-385"><strong>ERROR_APPX_RAW_</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-385"><strong>ERROR_APPX_RAW_</strong></span></span><br/> <span data-ttu-id="b7bc4-386"><strong>DATA_WRITE_FAILED</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-386"><strong>DATA_WRITE_FAILED</strong></span></span><br/></td>
<td><span data-ttu-id="b7bc4-387">0x80073D20</span><span class="sxs-lookup"><span data-stu-id="b7bc4-387">0x80073D20</span></span></td>
<td><span data-ttu-id="b7bc4-388">無法處理並將下載的套件資料寫入磁片。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-388">Failed to process and write downloaded package data to disk.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b7bc4-389"><strong>ERROR_DEPLOYMENT_BLOCKED_</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-389"><strong>ERROR_DEPLOYMENT_BLOCKED_</strong></span></span><br/> <span data-ttu-id="b7bc4-390"><strong>BY_VOLUME_POLICY_PACKAGE</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-390"><strong>BY_VOLUME_POLICY_PACKAGE</strong></span></span><br/></td>
<td><span data-ttu-id="b7bc4-391">0x80073D21</span><span class="sxs-lookup"><span data-stu-id="b7bc4-391">0x80073D21</span></span></td>
<td><span data-ttu-id="b7bc4-392">因為每個套件系列的原則限制了非系統磁片區上的部署，所以部署作業已遭到封鎖。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-392">The deployment operation was blocked due to a per-package-family policy restricting deployments on a non-system volume.</span></span> <span data-ttu-id="b7bc4-393">針對每個原則，此應用程式必須安裝到系統磁片磁碟機，但不會設為預設值。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-393">Per policy, this app must be installed to the system drive, but that's not set as the default.</span></span> <span data-ttu-id="b7bc4-394">在 [存放裝置設定] 中，讓系統磁片磁碟機成為儲存新內容的預設位置，然後重試安裝。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-394">In Storage settings, make the system drive the default location to save new content, then retry the install.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b7bc4-395"><strong>ERROR_DEPLOYMENT_BLOCKED_</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-395"><strong>ERROR_DEPLOYMENT_BLOCKED_</strong></span></span><br/> <span data-ttu-id="b7bc4-396"><strong>BY_VOLUME_POLICY_MACHINE</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-396"><strong>BY_VOLUME_POLICY_MACHINE</strong></span></span><br/></td>
<td><span data-ttu-id="b7bc4-397">0x80073D22</span><span class="sxs-lookup"><span data-stu-id="b7bc4-397">0x80073D22</span></span></td>
<td><span data-ttu-id="b7bc4-398">因為電腦範圍內的原則限制了非系統磁片區上的部署，所以部署作業已遭到封鎖。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-398">The deployment operation was blocked due to a machine-wide policy restricting deployments on a non-system volume.</span></span> <span data-ttu-id="b7bc4-399">針對每個原則，此應用程式必須安裝到系統磁片磁碟機，但不會設為預設值。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-399">Per policy, this app must be installed to the system drive, but that's not set as the default.</span></span> <span data-ttu-id="b7bc4-400">在 [存放裝置設定] 中，讓系統磁片磁碟機成為儲存新內容的預設位置，然後重試安裝。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-400">In Storage settings, make the system drive the default location to save new content, then retry the install.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b7bc4-401"><strong>ERROR_DEPLOYMENT_BLOCKED_</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-401"><strong>ERROR_DEPLOYMENT_BLOCKED_</strong></span></span><br/> <span data-ttu-id="b7bc4-402"><strong>BY_PROFILE_POLICY</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-402"><strong>BY_PROFILE_POLICY</strong></span></span><br/></td>
<td><span data-ttu-id="b7bc4-403">0x80073D23</span><span class="sxs-lookup"><span data-stu-id="b7bc4-403">0x80073D23</span></span></td>
<td><span data-ttu-id="b7bc4-404">因為不允許特殊設定檔部署，所以已封鎖部署作業 (特殊設定檔是使用者設定檔，在使用者登出) 之後將會捨棄變更。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-404">The deployment operation was blocked because special profile deployment is not allowed (special profiles are user profiles where changes are discarded after the user signs out).</span></span> <span data-ttu-id="b7bc4-405">請嘗試登入不是特殊設定檔的帳戶。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-405">Try logging into an account that is not a special profile.</span></span> <span data-ttu-id="b7bc4-406">您可以嘗試登出並重新登入目前的帳戶，或嘗試登入其他帳戶。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-406">You can try logging out and logging back into the current account, or try logging into a different account.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b7bc4-407"><strong>ERROR_DEPLOYMENT_FAILED_</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-407"><strong>ERROR_DEPLOYMENT_FAILED_</strong></span></span><br/> <span data-ttu-id="b7bc4-408"><strong>CONFLICTING_MUTABLE_PACKAGE_</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-408"><strong>CONFLICTING_MUTABLE_PACKAGE_</strong></span></span><br/> <span data-ttu-id="b7bc4-409"><strong>目錄</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-409"><strong>DIRECTORY</strong></span></span><br/></td>
<td><span data-ttu-id="b7bc4-410">0x80073D24</span><span class="sxs-lookup"><span data-stu-id="b7bc4-410">0x80073D24</span></span></td>
<td><span data-ttu-id="b7bc4-411">部署作業失敗，因為有衝突的套件可變動 <a href="/uwp/schemas/appxpackage/uapmanifestschema/element-desktop6-mutablepackagedirectory">套件目錄</a>。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-411">The deployment operation failed due to a conflicting package's <a href="/uwp/schemas/appxpackage/uapmanifestschema/element-desktop6-mutablepackagedirectory">mutable package directory</a>.</span></span> <span data-ttu-id="b7bc4-412">若要安裝此套件，請移除具有衝突可變動套件目錄的現有套件。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-412">To install this package, remove the existing package with the conflicting mutable package directory.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b7bc4-413"><strong>ERROR_SINGLETON_RESOURCE_</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-413"><strong>ERROR_SINGLETON_RESOURCE_</strong></span></span><br/> <span data-ttu-id="b7bc4-414"><strong>INSTALLED_IN_ACTIVE_USER</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-414"><strong>INSTALLED_IN_ACTIVE_USER</strong></span></span><br/></td>
<td><span data-ttu-id="b7bc4-415">0x80073D25</span><span class="sxs-lookup"><span data-stu-id="b7bc4-415">0x80073D25</span></span></td>
<td><span data-ttu-id="b7bc4-416">套件安裝失敗，因為指定了單一資源，且已安裝該套件的另一個使用者登入。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-416">The package installation failed because a singleton resource was specified and another user with that package installed is logged in.</span></span> <span data-ttu-id="b7bc4-417">確定已安裝套件的所有作用中使用者都已登出，然後重試安裝。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-417">Make sure that all active users with the package installed are logged out and retry installation.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b7bc4-418">ERROR_DIFFERENT_VERSION_<strong></strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-418">ERROR_DIFFERENT_VERSION_<strong></strong></span></span><br/> <span data-ttu-id="b7bc4-419"><strong>OF_PACKAGED_SERVICE_INSTALLED</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-419"><strong>OF_PACKAGED_SERVICE_INSTALLED</strong></span></span><br/></td>
<td><span data-ttu-id="b7bc4-420">0x80073D26</span><span class="sxs-lookup"><span data-stu-id="b7bc4-420">0x80073D26</span></span></td>
<td><span data-ttu-id="b7bc4-421">套件安裝失敗，因為安裝了不同版本的服務。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-421">The package installation failed because a different version of the service is installed.</span></span> <span data-ttu-id="b7bc4-422">請嘗試安裝較新版本的套件。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-422">Try installing a newer version of the package.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b7bc4-423"><strong>ERROR_SERVICE_EXISTS_</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-423"><strong>ERROR_SERVICE_EXISTS_</strong></span></span><br/> <span data-ttu-id="b7bc4-424"><strong>AS_NON_PACKAGED_SERVICE</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-424"><strong>AS_NON_PACKAGED_SERVICE</strong></span></span><br/></td>
<td><span data-ttu-id="b7bc4-425">0x80073D27</span><span class="sxs-lookup"><span data-stu-id="b7bc4-425">0x80073D27</span></span></td>
<td><span data-ttu-id="b7bc4-426">套件安裝失敗，因為服務的版本存在於 msix/.appx 套件之外。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-426">The package installation failed because a version of the service exists outside of an .msix/.appx package.</span></span> <span data-ttu-id="b7bc4-427">請洽詢您的軟體廠商。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-427">Contact your software vendor.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b7bc4-428"><strong>ERROR_PACKAGED_SERVICE_</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-428"><strong>ERROR_PACKAGED_SERVICE_</strong></span></span><br/> <span data-ttu-id="b7bc4-429"><strong>REQUIRES_ADMIN_PRIVILEGES</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-429"><strong>REQUIRES_ADMIN_PRIVILEGES</strong></span></span><br/></td>
<td><span data-ttu-id="b7bc4-430">0x80073D28</span><span class="sxs-lookup"><span data-stu-id="b7bc4-430">0x80073D28</span></span></td>
<td><span data-ttu-id="b7bc4-431">套件安裝失敗，因為需要系統管理員許可權。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-431">The package installation failed because administrator privileges are required.</span></span> <span data-ttu-id="b7bc4-432">請洽詢系統管理員以安裝此套件。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-432">Contact an administrator to install this package.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b7bc4-433"><strong>ERROR_REDIRECTION_TO_</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-433"><strong>ERROR_REDIRECTION_TO_</strong></span></span><br/> <span data-ttu-id="b7bc4-434"><strong>DEFAULT_ACCOUNT_NOT_ALLOWED</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-434"><strong>DEFAULT_ACCOUNT_NOT_ALLOWED</strong></span></span><br/></td>
<td><span data-ttu-id="b7bc4-435">0x80073D29</span><span class="sxs-lookup"><span data-stu-id="b7bc4-435">0x80073D29</span></span></td>
<td><span data-ttu-id="b7bc4-436">封裝部署失敗，因為當呼叫者未這麼做時，此作業會重新導向至預設帳戶。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-436">The package deployment failed because the operation would have redirected to default account, when the caller said not to do so.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b7bc4-437"><strong>ERROR_PACKAGE_LACKS_</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-437"><strong>ERROR_PACKAGE_LACKS_</strong></span></span><br/> <span data-ttu-id="b7bc4-438"><strong>CAPABILITY_TO_DEPLOY_ON_HOST</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-438"><strong>CAPABILITY_TO_DEPLOY_ON_HOST</strong></span></span><br/></td>
<td><span data-ttu-id="b7bc4-439">0x80073D2A</span><span class="sxs-lookup"><span data-stu-id="b7bc4-439">0x80073D2A</span></span></td>
<td><span data-ttu-id="b7bc4-440">封裝部署失敗，因為封裝需要能夠以原生方式將此主機設為目標。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-440">The package deployment failed because the package requires a capability to natively target this host.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b7bc4-441"><strong>ERROR_UNSIGNED_PACKAGE_</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-441"><strong>ERROR_UNSIGNED_PACKAGE_</strong></span></span><br/> <span data-ttu-id="b7bc4-442"><strong>INVALID_CONTENT</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-442"><strong>INVALID_CONTENT</strong></span></span><br/></td>
<td><span data-ttu-id="b7bc4-443">0x80073D2B</span><span class="sxs-lookup"><span data-stu-id="b7bc4-443">0x80073D2B</span></span></td>
<td><span data-ttu-id="b7bc4-444">封裝部署失敗，因為它的內容對未簽署的套件無效。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-444">The package deployment failed because its content is not valid for an unsigned package.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b7bc4-445"><strong>ERROR_UNSIGNED_PACKAGE_</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-445"><strong>ERROR_UNSIGNED_PACKAGE_</strong></span></span><br/> <span data-ttu-id="b7bc4-446"><strong>INVALID_PUBLISHER_NAMESPACE</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-446"><strong>INVALID_PUBLISHER_NAMESPACE</strong></span></span><br/></td>
<td><span data-ttu-id="b7bc4-447">0x80073D2C</span><span class="sxs-lookup"><span data-stu-id="b7bc4-447">0x80073D2C</span></span></td>
<td><span data-ttu-id="b7bc4-448">封裝部署失敗，因為它的發行者不在未簽署的命名空間中。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-448">The package deployment failed because its publisher is not in the unsigned namespace.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b7bc4-449"><strong>ERROR_SIGNED_PACKAGE_</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-449"><strong>ERROR_SIGNED_PACKAGE_</strong></span></span><br/> <span data-ttu-id="b7bc4-450"><strong>INVALID_PUBLISHER_NAMESPACE</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-450"><strong>INVALID_PUBLISHER_NAMESPACE</strong></span></span><br/></td>
<td><span data-ttu-id="b7bc4-451">0x80073D2D</span><span class="sxs-lookup"><span data-stu-id="b7bc4-451">0x80073D2D</span></span></td>
<td><span data-ttu-id="b7bc4-452">封裝部署失敗，因為它的發行者不在已簽署的命名空間中。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-452">The package deployment failed because its publisher is not in the signed namespace.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b7bc4-453"><strong>ERROR_PACKAGE_EXTERNAL_</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-453"><strong>ERROR_PACKAGE_EXTERNAL_</strong></span></span><br/> <span data-ttu-id="b7bc4-454"><strong>LOCATION_NOT_ALLOWED</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-454"><strong>LOCATION_NOT_ALLOWED</strong></span></span><br/></td>
<td><span data-ttu-id="b7bc4-455">0x80073D2E</span><span class="sxs-lookup"><span data-stu-id="b7bc4-455">0x80073D2E</span></span></td>
<td><span data-ttu-id="b7bc4-456">封裝部署失敗，因為它的發行者不在已簽署的命名空間中。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-456">The package deployment failed because its publisher is not in the signed namespace.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b7bc4-457"><strong>ERROR_INSTALL_FULLTRUST_</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-457"><strong>ERROR_INSTALL_FULLTRUST_</strong></span></span><br/> <span data-ttu-id="b7bc4-458"><strong>HOSTRUNTIME_REQUIRES_MAIN_</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-458"><strong>HOSTRUNTIME_REQUIRES_MAIN_</strong></span></span><br/> <span data-ttu-id="b7bc4-459"><strong>PACKAGE_FULLTRUST_CAPABILITY</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-459"><strong>PACKAGE_FULLTRUST_CAPABILITY</strong></span></span><br/></td>
<td><span data-ttu-id="b7bc4-460">0x80073D2F</span><span class="sxs-lookup"><span data-stu-id="b7bc4-460">0x80073D2F</span></span></td>
<td><span data-ttu-id="b7bc4-461">解析為具有完全信任內容之套件的主機執行時間相依性，需要主要套件具有 <strong>runFullTrust</strong> 功能。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-461">A host runtime dependency resolving to a package with full trust content requires the main package to have the <strong>runFullTrust</strong> capability.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b7bc4-462"><strong>APPX_E_PACKAGING_INTERNAL</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-462"><strong>APPX_E_PACKAGING_INTERNAL</strong></span></span></td>
<td><span data-ttu-id="b7bc4-463">0x80080200</span><span class="sxs-lookup"><span data-stu-id="b7bc4-463">0x80080200</span></span></td>
<td><span data-ttu-id="b7bc4-464">封裝 API 遇到內部錯誤。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-464">The packaging API has encountered an internal error.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b7bc4-465"><strong>APPX_E_INTERLEAVING_</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-465"><strong>APPX_E_INTERLEAVING_</strong></span></span><br/> <span data-ttu-id="b7bc4-466"><strong>NOT_ALLOWED</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-466"><strong>NOT_ALLOWED</strong></span></span><br/></td>
<td><span data-ttu-id="b7bc4-467">0x80080201</span><span class="sxs-lookup"><span data-stu-id="b7bc4-467">0x80080201</span></span></td>
<td><span data-ttu-id="b7bc4-468">封裝無效，因為它的內容是交錯的。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-468">The package isn't valid because its contents are interleaved.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b7bc4-469"><strong>APPX_E_RELATIONSHIPS_</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-469"><strong>APPX_E_RELATIONSHIPS_</strong></span></span><br/> <span data-ttu-id="b7bc4-470"><strong>NOT_ALLOWED</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-470"><strong>NOT_ALLOWED</strong></span></span><br/></td>
<td><span data-ttu-id="b7bc4-471">0x80080202</span><span class="sxs-lookup"><span data-stu-id="b7bc4-471">0x80080202</span></span></td>
<td><span data-ttu-id="b7bc4-472">封裝無效，因為它包含 OPC 關聯性。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-472">The package isn't valid because it contains OPC relationships.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b7bc4-473"><strong>APPX_E_MISSING_</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-473"><strong>APPX_E_MISSING_</strong></span></span><br/> <span data-ttu-id="b7bc4-474"><strong>REQUIRED_FILE</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-474"><strong>REQUIRED_FILE</strong></span></span><br/></td>
<td><span data-ttu-id="b7bc4-475">0x80080203</span><span class="sxs-lookup"><span data-stu-id="b7bc4-475">0x80080203</span></span></td>
<td><span data-ttu-id="b7bc4-476">封裝無效，因為它遺漏資訊清單或區塊對應，或存在程式碼完整性檔案，但遺失簽章檔案。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-476">The package isn't valid because it's missing a manifest or block map, or a code integrity file is present but a signature file is missing.</span></span><br/> <span data-ttu-id="b7bc4-477">請確定封裝未遺失其中一個或多個必要的檔案：</span><span class="sxs-lookup"><span data-stu-id="b7bc4-477">Ensure that the package isn't missing one or more of these required files:</span></span><br/>
<ul>
<li><span data-ttu-id="b7bc4-478">\AppxManifest.xml</span><span class="sxs-lookup"><span data-stu-id="b7bc4-478">\AppxManifest.xml</span></span></li>
<li><span data-ttu-id="b7bc4-479">\AppxBlockMap.xml</span><span class="sxs-lookup"><span data-stu-id="b7bc4-479">\AppxBlockMap.xml</span></span></li>
</ul>
<span data-ttu-id="b7bc4-480">如果封裝包含 \AppxMetadata\CodeIntegrity.cat，它也必須包含 \AppxSignature.p7x。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-480">If the package contains \AppxMetadata\CodeIntegrity.cat, it must also contain \AppxSignature.p7x.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b7bc4-481"><strong>APPX_E_INVALID_MANIFEST</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-481"><strong>APPX_E_INVALID_MANIFEST</strong></span></span></td>
<td><span data-ttu-id="b7bc4-482">0x80080204</span><span class="sxs-lookup"><span data-stu-id="b7bc4-482">0x80080204</span></span></td>
<td><span data-ttu-id="b7bc4-483">封裝的 AppxManifest.xml 檔無效。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-483">The package's AppxManifest.xml file isn't valid.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b7bc4-484"><strong>APPX_E_INVALID_BLOCKMAP</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-484"><strong>APPX_E_INVALID_BLOCKMAP</strong></span></span></td>
<td><span data-ttu-id="b7bc4-485">0x80080205</span><span class="sxs-lookup"><span data-stu-id="b7bc4-485">0x80080205</span></span></td>
<td><span data-ttu-id="b7bc4-486">封裝的 AppxBlockMap.xml 檔無效。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-486">The package's AppxBlockMap.xml file isn't valid.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b7bc4-487"><strong>APPX_E_CORRUPT_CONTENT</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-487"><strong>APPX_E_CORRUPT_CONTENT</strong></span></span></td>
<td><span data-ttu-id="b7bc4-488">0x80080206</span><span class="sxs-lookup"><span data-stu-id="b7bc4-488">0x80080206</span></span></td>
<td><span data-ttu-id="b7bc4-489">無法讀取套件內容，因為它已損毀。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-489">The package contents can't be read because it's corrupted.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b7bc4-490"><strong>APPX_E_BLOCK_</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-490"><strong>APPX_E_BLOCK_</strong></span></span><br/> <span data-ttu-id="b7bc4-491"><strong>HASH_INVALID</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-491"><strong>HASH_INVALID</strong></span></span><br/></td>
<td><span data-ttu-id="b7bc4-492">0x80080207</span><span class="sxs-lookup"><span data-stu-id="b7bc4-492">0x80080207</span></span></td>
<td><span data-ttu-id="b7bc4-493">區塊的計算雜湊值不符合區塊對應中儲存的值。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-493">The computed hash value of the block doesn't match the has value stored in the block map.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b7bc4-494"><strong>APPX_E_REQUESTED_</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-494"><strong>APPX_E_REQUESTED_</strong></span></span><br/> <span data-ttu-id="b7bc4-495"><strong>RANGE_TOO_LARGE</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-495"><strong>RANGE_TOO_LARGE</strong></span></span><br/></td>
<td><span data-ttu-id="b7bc4-496">0x80080208</span><span class="sxs-lookup"><span data-stu-id="b7bc4-496">0x80080208</span></span></td>
<td><span data-ttu-id="b7bc4-497">當轉譯成區塊的位元組範圍時，要求的位元組範圍超過 4 GB。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-497">The requested byte range is over 4 GB when translated to a byte range of blocks.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b7bc4-498"><strong>TRUST_E_NOSIGNATURE</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-498"><strong>TRUST_E_NOSIGNATURE</strong></span></span></td>
<td><span data-ttu-id="b7bc4-499">0x800B0100</span><span class="sxs-lookup"><span data-stu-id="b7bc4-499">0x800B0100</span></span></td>
<td><span data-ttu-id="b7bc4-500">主體中沒有簽章。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-500">No signature is present in the subject.</span></span><br/> <span data-ttu-id="b7bc4-501">如果封裝未簽署或簽章無效，您可能會收到此錯誤。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-501">You may get this error if the package is unsigned or the signature isn't valid.</span></span> <span data-ttu-id="b7bc4-502">必須簽署套件才能進行部署。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-502">The package must be signed to be deployed.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b7bc4-503"><strong>CERT_E_UNTRUSTEDROOT</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-503"><strong>CERT_E_UNTRUSTEDROOT</strong></span></span></td>
<td><span data-ttu-id="b7bc4-504">0x800B0109</span><span class="sxs-lookup"><span data-stu-id="b7bc4-504">0x800B0109</span></span></td>
<td><span data-ttu-id="b7bc4-505">憑證鏈已處理，但在信任提供者不信任的根憑證中終止。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-505">A certificate chain processed, but terminated in a root certificate which isn't trusted by the trust provider.</span></span><br/> <span data-ttu-id="b7bc4-506">請參閱 <a href="/previous-versions/br230260(v=vs.110)">簽署封裝</a>。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-506">See <a href="/previous-versions/br230260(v=vs.110)">Signing a package</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b7bc4-507"><strong>CERT_E_CHAINING</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-507"><strong>CERT_E_CHAINING</strong></span></span></td>
<td><span data-ttu-id="b7bc4-508">0x800B010A</span><span class="sxs-lookup"><span data-stu-id="b7bc4-508">0x800B010A</span></span></td>
<td><span data-ttu-id="b7bc4-509">無法建立信任的根憑證授權單位的憑證鏈。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-509">A certificate chain couldn't be built to a trusted root certification authority.</span></span><br/> <span data-ttu-id="b7bc4-510">請參閱 <a href="/previous-versions/br230260(v=vs.110)">簽署封裝</a>。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-510">See <a href="/previous-versions/br230260(v=vs.110)">Signing a package</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b7bc4-511"><strong>APPX_E_INVALID_</strong> </span><span class="sxs-lookup"><span data-stu-id="b7bc4-511"><strong>APPX_E_INVALID_</strong> </span></span><br/> <span data-ttu-id="b7bc4-512"><strong>SIP_CLIENT_DATA</strong> </span><span class="sxs-lookup"><span data-stu-id="b7bc4-512"><strong>SIP_CLIENT_DATA</strong> </span></span><br/></td>
<td><span data-ttu-id="b7bc4-513">0x80080209</span><span class="sxs-lookup"><span data-stu-id="b7bc4-513">0x80080209</span></span></td>
<td><span data-ttu-id="b7bc4-514">用來簽署封裝的 <a href="/windows/win32/api/mssip/ns-mssip-sip_subjectinfo"><strong>SIP_SUBJECTINFO</strong></a>結構未包含必要的資料</span><span class="sxs-lookup"><span data-stu-id="b7bc4-514">The <a href="/windows/win32/api/mssip/ns-mssip-sip_subjectinfo"><strong>SIP_SUBJECTINFO</strong></a>structure used to sign the package didn't contain the required data</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b7bc4-515"><strong>APPX_E_INVALID_</strong> </span><span class="sxs-lookup"><span data-stu-id="b7bc4-515"><strong>APPX_E_INVALID_</strong> </span></span><br/> <span data-ttu-id="b7bc4-516"><strong>KEY_INFO</strong> </span><span class="sxs-lookup"><span data-stu-id="b7bc4-516"><strong>KEY_INFO</strong> </span></span><br/></td>
<td><span data-ttu-id="b7bc4-517">0x8008020A</span><span class="sxs-lookup"><span data-stu-id="b7bc4-517">0x8008020A</span></span></td>
<td><span data-ttu-id="b7bc4-518">用來加密或解密封裝的 <a href="/windows/win32/api/appxpackaging/ns-appxpackaging-appx_key_info"><strong>APPX_KEY_INFO</strong></a> 結構包含不正確資料。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-518">The <a href="/windows/win32/api/appxpackaging/ns-appxpackaging-appx_key_info"><strong>APPX_KEY_INFO</strong></a> structure used to encrypt or decrypt the package contains invalid data.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b7bc4-519"><strong>APPX_E_INVALID_</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-519"><strong>APPX_E_INVALID_</strong></span></span><br/> <span data-ttu-id="b7bc4-520"><strong>CONTENTGROUPMAP</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-520"><strong>CONTENTGROUPMAP</strong></span></span><br/></td>
<td><span data-ttu-id="b7bc4-521">0x8008020B</span><span class="sxs-lookup"><span data-stu-id="b7bc4-521">0x8008020B</span></span></td>
<td><span data-ttu-id="b7bc4-522">Msix/.appx 套件的內容群組對應無效。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-522">The .msix/.appx package's content group map is invalid.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b7bc4-523"><strong>APPX_E_INVALID_</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-523"><strong>APPX_E_INVALID_</strong></span></span><br/> <span data-ttu-id="b7bc4-524"><strong>APPINSTALLER</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-524"><strong>APPINSTALLER</strong></span></span><br/></td>
<td><span data-ttu-id="b7bc4-525">0x8008020C</span><span class="sxs-lookup"><span data-stu-id="b7bc4-525">0x8008020C</span></span></td>
<td><span data-ttu-id="b7bc4-526">封裝的 <a href="/windows/msix/app-installer/app-installer-root">appinstaller</a> 檔無效。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-526">The <a href="/windows/msix/app-installer/app-installer-root">.appinstaller file</a> for the package is invalid.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b7bc4-527"><strong>APPX_E_DELTA_BASELINE_</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-527"><strong>APPX_E_DELTA_BASELINE_</strong></span></span><br/> <span data-ttu-id="b7bc4-528"><strong>VERSION_MISMATCH</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-528"><strong>VERSION_MISMATCH</strong></span></span><br/></td>
<td><span data-ttu-id="b7bc4-529">0x8008020D</span><span class="sxs-lookup"><span data-stu-id="b7bc4-529">0x8008020D</span></span></td>
<td><span data-ttu-id="b7bc4-530">差異套件中的基準套件版本與要更新之基準套件中的版本不相符。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-530">The baseline package version in delta package does not match the version in the baseline package to be updated.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b7bc4-531"><strong>APPX_E_DELTA_PACKAGE_</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-531"><strong>APPX_E_DELTA_PACKAGE_</strong></span></span><br/> <span data-ttu-id="b7bc4-532"><strong>MISSING_FILE</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-532"><strong>MISSING_FILE</strong></span></span><br/></td>
<td><span data-ttu-id="b7bc4-533">0x8008020E</span><span class="sxs-lookup"><span data-stu-id="b7bc4-533">0x8008020E</span></span></td>
<td><span data-ttu-id="b7bc4-534">差異套件遺漏更新套件中的檔案。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-534">The delta package is missing a file from the updated package.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b7bc4-535"><strong>APPX_E_INVALID_</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-535"><strong>APPX_E_INVALID_</strong></span></span><br/> <span data-ttu-id="b7bc4-536"><strong>DELTA_PACKAGE</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-536"><strong>DELTA_PACKAGE</strong></span></span><br/></td>
<td><span data-ttu-id="b7bc4-537">0x8008020F</span><span class="sxs-lookup"><span data-stu-id="b7bc4-537">0x8008020F</span></span></td>
<td><span data-ttu-id="b7bc4-538">差異套件無效。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-538">The delta package is invalid.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b7bc4-539"><strong>APPX_E_DELTA_APPENDED_</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-539"><strong>APPX_E_DELTA_APPENDED_</strong></span></span><br/> <span data-ttu-id="b7bc4-540"><strong>PACKAGE_NOT_ALLOWED</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-540"><strong>PACKAGE_NOT_ALLOWED</strong></span></span><br/></td>
<td><span data-ttu-id="b7bc4-541">0x80080210</span><span class="sxs-lookup"><span data-stu-id="b7bc4-541">0x80080210</span></span></td>
<td><span data-ttu-id="b7bc4-542">目前的作業不允許差異附加的封裝。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-542">The delta appended package is not allowed for the current operation.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b7bc4-543"><strong>APPX_E_INVALID_</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-543"><strong>APPX_E_INVALID_</strong></span></span><br/> <span data-ttu-id="b7bc4-544"><strong>PACKAGING_LAYOUT</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-544"><strong>PACKAGING_LAYOUT</strong></span></span><br/></td>
<td><span data-ttu-id="b7bc4-545">0x80080211</span><span class="sxs-lookup"><span data-stu-id="b7bc4-545">0x80080211</span></span></td>
<td><span data-ttu-id="b7bc4-546">封裝設定檔案無效。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-546">The packaging layout file is invalid.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b7bc4-547"><strong>APPX_E_INVALID_</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-547"><strong>APPX_E_INVALID_</strong></span></span><br/> <span data-ttu-id="b7bc4-548"><strong>PACKAGESIGNCONFIG</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-548"><strong>PACKAGESIGNCONFIG</strong></span></span><br/></td>
<td><span data-ttu-id="b7bc4-549">0x80080212</span><span class="sxs-lookup"><span data-stu-id="b7bc4-549">0x80080212</span></span></td>
<td><span data-ttu-id="b7bc4-550">PackageSignConfig 檔無效。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-550">The packageSignConfig file is invalid.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b7bc4-551"><strong>APPX_E_RESOURCESPRI_</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-551"><strong>APPX_E_RESOURCESPRI_</strong></span></span><br/> <span data-ttu-id="b7bc4-552"><strong>NOT_ALLOWED</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-552"><strong>NOT_ALLOWED</strong></span></span><br/></td>
<td><span data-ttu-id="b7bc4-553">0x80080213</span><span class="sxs-lookup"><span data-stu-id="b7bc4-553">0x80080213</span></span></td>
<td><span data-ttu-id="b7bc4-554">當套件資訊清單中沒有任何資源元素時，不允許使用 .resources 檔。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-554">The resources.pri file is not allowed when there are no resource elements in the package manifest.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b7bc4-555"><strong>APPX_E_FILE_</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-555"><strong>APPX_E_FILE_</strong></span></span><br/> <span data-ttu-id="b7bc4-556"><strong>COMPRESSION_MISMATCH</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-556"><strong>COMPRESSION_MISMATCH</strong></span></span><br/></td>
<td><span data-ttu-id="b7bc4-557">0x80080214</span><span class="sxs-lookup"><span data-stu-id="b7bc4-557">0x80080214</span></span></td>
<td><span data-ttu-id="b7bc4-558">基準中的檔案壓縮狀態和更新的封裝不符。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-558">The compression state of file in baseline and updated package does not match.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b7bc4-559"><strong>APPX_E_INVALID_</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-559"><strong>APPX_E_INVALID_</strong></span></span><br/> <span data-ttu-id="b7bc4-560"><strong>PAYLOAD_PACKAGE_EXTENSION</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-560"><strong>PAYLOAD_PACKAGE_EXTENSION</strong></span></span><br/></td>
<td><span data-ttu-id="b7bc4-561">0x80080215</span><span class="sxs-lookup"><span data-stu-id="b7bc4-561">0x80080215</span></span></td>
<td><span data-ttu-id="b7bc4-562">若是以較舊平臺為目標的裝載套件，則不允許使用非 .appx 延伸模組。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-562">Non .appx extensions are not allowed for payload packages targeting older platforms.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b7bc4-563"><strong>APPX_E_INVALID_</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-563"><strong>APPX_E_INVALID_</strong></span></span><br/> <span data-ttu-id="b7bc4-564"><strong>ENCRYPTION_EXCLUSION_FILE_LIST</strong></span><span class="sxs-lookup"><span data-stu-id="b7bc4-564"><strong>ENCRYPTION_EXCLUSION_FILE_LIST</strong></span></span><br/></td>
<td><span data-ttu-id="b7bc4-565">0x80080216</span><span class="sxs-lookup"><span data-stu-id="b7bc4-565">0x80080216</span></span></td>
<td><span data-ttu-id="b7bc4-566">EncryptionExclusionFileList 檔無效。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-566">The encryptionExclusionFileList file is invalid.</span></span><br/></td>
</tr>
</tbody>
</table>

## <a name="applications-dont-start-and-their-names-are-dimmed"></a><span data-ttu-id="b7bc4-567">應用程式無法啟動，而且其名稱會呈現暗灰色</span><span class="sxs-lookup"><span data-stu-id="b7bc4-567">Applications don't start and their names are dimmed</span></span>

<span data-ttu-id="b7bc4-568">在以 Windows 10 為基礎的電腦上，您無法啟動某些應用程式，且應用程式名稱會呈現暗灰色。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-568">On a Windows 10-based computer, you cannot start some applications, and the application names appear dimmed.</span></span>

![某些應用程式名稱在 [開始] 功能表中會顯示為暗灰色](./images/app-names-dimmed.png)

<span data-ttu-id="b7bc4-570">當您選取灰色名稱來嘗試開啟應用程式時，可能會收到下列其中一個錯誤訊息：</span><span class="sxs-lookup"><span data-stu-id="b7bc4-570">When you try to open an application by selecting the dimmed name, you may receive one of the following error messages:</span></span>

> <span data-ttu-id="b7bc4-571">發生問題 \<*application name*> 。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-571">There's a problem with \<*application name*>.</span></span> <span data-ttu-id="b7bc4-572">請洽詢您的系統管理員，瞭解如何修復或重新安裝</span><span class="sxs-lookup"><span data-stu-id="b7bc4-572">Contact your system administrator about repairing or reinstalling it</span></span>  
> <span data-ttu-id="b7bc4-573">錯誤：無法開啟此應用程式</span><span class="sxs-lookup"><span data-stu-id="b7bc4-573">Error: This app can't open</span></span>

<span data-ttu-id="b7bc4-574">此外，下列事件專案會記錄在 **應用程式和 Services\Microsoft\Windows\Apps** 下的「TWinUI/Operational」記錄檔中：</span><span class="sxs-lookup"><span data-stu-id="b7bc4-574">Additionally, the following event entries are logged in the "Microsoft-Windows-TWinUI/Operational" log under **Applications and Services\Microsoft\Windows\Apps**:</span></span>

> <span data-ttu-id="b7bc4-575">記錄檔名稱： Microsoft-Windows-TWinUI/Operational</span><span class="sxs-lookup"><span data-stu-id="b7bc4-575">Log Name: Microsoft-Windows-TWinUI/Operational</span></span>  
> <span data-ttu-id="b7bc4-576">來源： Microsoft-Windows-沉浸式 Shell</span><span class="sxs-lookup"><span data-stu-id="b7bc4-576">Source: Microsoft-Windows-Immersive-Shell</span></span>  
> <span data-ttu-id="b7bc4-577">日期： <*日期*></span><span class="sxs-lookup"><span data-stu-id="b7bc4-577">Date: <*date*></span></span>  
> <span data-ttu-id="b7bc4-578">事件識別碼：5960</span><span class="sxs-lookup"><span data-stu-id="b7bc4-578">Event ID: 5960</span></span>  
> <span data-ttu-id="b7bc4-579">工作分類： (5960) </span><span class="sxs-lookup"><span data-stu-id="b7bc4-579">Task Category: (5960)</span></span>  
> <span data-ttu-id="b7bc4-580">層級：錯誤</span><span class="sxs-lookup"><span data-stu-id="b7bc4-580">Level: Error</span></span>  
> <span data-ttu-id="b7bc4-581">關鍵字：</span><span class="sxs-lookup"><span data-stu-id="b7bc4-581">Keywords:</span></span>  
> <span data-ttu-id="b7bc4-582">描述：</span><span class="sxs-lookup"><span data-stu-id="b7bc4-582">Description:</span></span>  
> <span data-ttu-id="b7bc4-583">應用程式的啟用 Microsoft.BingNews_8wekyb3d8bbwe！適用于 Windows 的 AppexNews。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-583">Activation of the app Microsoft.BingNews_8wekyb3d8bbwe!AppexNews for the Windows.</span></span> <span data-ttu-id="b7bc4-584">因為啟動合約的套件處於狀態：已修改，所以已封鎖其錯誤0x80073CFC。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-584">Launch contract was blocked with error 0x80073CFC because its package is in state: Modified.</span></span>  

### <a name="cause"></a><span data-ttu-id="b7bc4-585">原因</span><span class="sxs-lookup"><span data-stu-id="b7bc4-585">Cause</span></span>

<span data-ttu-id="b7bc4-586">發生此問題的原因是已修改應用程式對應套件狀態值的登錄專案。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-586">This issue occurs because the registry entry for the status value of application's corresponding package was modified.</span></span>

### <a name="resolution"></a><span data-ttu-id="b7bc4-587">解決方案</span><span class="sxs-lookup"><span data-stu-id="b7bc4-587">Resolution</span></span>

> [!WARNING]
> <span data-ttu-id="b7bc4-588">如果您使用登錄編輯程式或使用其他方法不正確地修改登錄，則可能會發生嚴重問題。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-588">Serious problems might occur if you modify the registry incorrectly by using Registry Editor or by using another method.</span></span> <span data-ttu-id="b7bc4-589">您可能必須重新安裝作業系統才能解決問題。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-589">These problems might require that you reinstall the operating system.</span></span> <span data-ttu-id="b7bc4-590">Microsoft 無法保證可以解決這些問題。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-590">Microsoft cannot guarantee that these problems can be solved.</span></span> <span data-ttu-id="b7bc4-591">您必須自行承擔修改登錄的風險。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-591">Modify the registry at your own risk.</span></span>

<span data-ttu-id="b7bc4-592">若要修正此問題：</span><span class="sxs-lookup"><span data-stu-id="b7bc4-592">To fix this issue:</span></span>

1. <span data-ttu-id="b7bc4-593">啟動登錄編輯程式，然後找出 **HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\AppModel\StateChange\PackageList** 子機碼。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-593">Start Registry Editor, and then locate the **HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\AppModel\StateChange\PackageList** subkey.</span></span>
2. <span data-ttu-id="b7bc4-594">若要備份子機碼資料，請以滑鼠右鍵按一下 **PackageList**，選取 [ **匯出**]，然後將資料儲存為登錄檔。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-594">To back up the subkey data, right-click **PackageList**, select **Export**, and then save the data as a registry file.</span></span>
3. <span data-ttu-id="b7bc4-595">針對事件識別碼5960記錄專案中列出的每個應用程式，請遵循下列步驟：</span><span class="sxs-lookup"><span data-stu-id="b7bc4-595">For each of the applications that are listed in the Event ID 5960 log entries, follow these steps:</span></span>  
   1. <span data-ttu-id="b7bc4-596">找出 **PackageStatus** 專案。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-596">Locate the **PackageStatus** entry.</span></span>
   2. <span data-ttu-id="b7bc4-597">將 **PackageStatus** 的值設定為零 (**0**) 。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-597">Set the value of **PackageStatus** to zero (**0**).</span></span>
   > [!NOTE]  
   > <span data-ttu-id="b7bc4-598">如果 **PackageList** 下的應用程式沒有任何專案，則問題有一些其他原因。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-598">If there are no entries for the application under **PackageList**, then the issue has some other cause.</span></span> <span data-ttu-id="b7bc4-599">在本文的範例事件案例中，完整的子機碼是 **HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\AppModel\StateChange\PackageList\Microsoft.BingNews_8wekyb3d8bbwe!AppexNews\PackageStatus**</span><span class="sxs-lookup"><span data-stu-id="b7bc4-599">In the case of the example event in this article, the full subkey is **HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\AppModel\StateChange\PackageList\Microsoft.BingNews_8wekyb3d8bbwe!AppexNews\PackageStatus**</span></span>
4. <span data-ttu-id="b7bc4-600">重新啟動電腦。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-600">Restart the computer.</span></span>

## <a name="get-additional-help"></a><span data-ttu-id="b7bc4-601">取得其他說明</span><span class="sxs-lookup"><span data-stu-id="b7bc4-601">Get additional help</span></span>

<span data-ttu-id="b7bc4-602">如果您需要進一步協助解決問題，請在封裝、部署或查詢 Windows 應用程式套件 ( msix/.appx) 時遇到問題。如需開發人員，請參閱這些額外的開發人員支援資源。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-602">If you need further help with resolving a problem you are experience when packaging, deploying, or querying a Windows app package (.msix/.appx) as a developer, refer to these additional developer support resources.</span></span>

- <span data-ttu-id="b7bc4-603">[Microsoft 問&a](/answers/topics/uwp.html?filter=all&sort=active) 提供專家和 Microsoft 工程師的相關和及時解答您的技術問題。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-603">[Microsoft Q&A](/answers/topics/uwp.html?filter=all&sort=active) offers relevant and timely answers to your technical problems from a community of experts and Microsoft engineers.</span></span>
- <span data-ttu-id="b7bc4-604">如需有關開發問題的社區協助，我們有 [論壇](https://social.msdn.microsoft.com/Forums/newthread?category=windowsapps&forum=wpdevelop&prof=required)和 [StackOverflow](https://stackoverflow.com/questions)。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-604">For community assistance with development questions, there are our [forums](https://social.msdn.microsoft.com/Forums/newthread?category=windowsapps&forum=wpdevelop&prof=required), and [StackOverflow](https://stackoverflow.com/questions).</span></span>
- <span data-ttu-id="b7bc4-605">[Windows 開發人員支援](https://developer.microsoft.com/windows/support)網站說明其他支援選項。</span><span class="sxs-lookup"><span data-stu-id="b7bc4-605">The [Windows developer support](https://developer.microsoft.com/windows/support) site explains other support options.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b7bc4-606">相關主題</span><span class="sxs-lookup"><span data-stu-id="b7bc4-606">Related topics</span></span>

- <span data-ttu-id="b7bc4-607">[如何使用 SignTool 簽署應用程式套件](how-to-sign-a-package-using-signtool.md) \(英文\)</span><span class="sxs-lookup"><span data-stu-id="b7bc4-607">[How to sign an app package using SignTool](how-to-sign-a-package-using-signtool.md)</span></span>
- [<span data-ttu-id="b7bc4-608">如何針對應用程式封裝簽章錯誤進行疑難排解</span><span class="sxs-lookup"><span data-stu-id="b7bc4-608">How to troubleshoot app package signature errors</span></span>](how-to-troubleshoot-app-package-signature-errors.md)
