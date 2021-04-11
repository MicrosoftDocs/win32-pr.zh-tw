---
title: 封裝、部署及查詢 Windows 應用程式
description: 以程式設計方式建立 Windows 應用程式的應用程式套件，以及安裝、更新、查詢和卸載應用程式套件。
ms.assetid: 4ea65e62-4878-41fd-9ad8-424b1546f02a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bfd1792e0b7b18f0dee04bca6f352e055b20f57
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "104092647"
---
# <a name="packaging-deployment-and-query-of-windows-apps"></a><span data-ttu-id="84632-103">封裝、部署及查詢 Windows 應用程式</span><span class="sxs-lookup"><span data-stu-id="84632-103">Packaging, deployment, and query of Windows apps</span></span>

<span data-ttu-id="84632-104">您可以透過 msix/.appx 應用程式套件（以 OPC 格式為基礎）部署、管理和服務 Windows 應用程式 (包括 UWPs 和桌面) 應用程式。</span><span class="sxs-lookup"><span data-stu-id="84632-104">You deploy, manage, and service Windows apps (including UWPs and desktop apps) through .msix/.appx app packages based on the OPC format.</span></span> <span data-ttu-id="84632-105">每個應用程式套件都包含構成應用程式的檔案，以及描述軟體至 Windows 的資訊清單檔案。</span><span class="sxs-lookup"><span data-stu-id="84632-105">Each app package contains the files that constitute the app, and a manifest file that describes the software to Windows.</span></span>

## <a name="introduction"></a><span data-ttu-id="84632-106">簡介</span><span class="sxs-lookup"><span data-stu-id="84632-106">Introduction</span></span>

<span data-ttu-id="84632-107">開發人員通常會使用 Visual Studio 來建立和簽署應用程式套件。</span><span class="sxs-lookup"><span data-stu-id="84632-107">Typically, developers create and sign app packages using Visual Studio.</span></span> <span data-ttu-id="84632-108">如需詳細資訊，請參閱 [使用 Visual Studio 封裝 UWP 應用程式](/windows/msix/package/packaging-uwp-apps)。</span><span class="sxs-lookup"><span data-stu-id="84632-108">For more info, see [Package a UWP app with Visual Studio](/windows/msix/package/packaging-uwp-apps).</span></span>

<span data-ttu-id="84632-109">Microsoft Store 可讓您輕鬆地建立、提交應用程式，並將其銷售給全球各地的客戶。</span><span class="sxs-lookup"><span data-stu-id="84632-109">The Microsoft Store makes it easy to build, submit, and sell your apps to customers around the world.</span></span> <span data-ttu-id="84632-110">如需詳細資訊，請參閱 [應用程式提交](/windows/uwp/publish/app-submissions)。</span><span class="sxs-lookup"><span data-stu-id="84632-110">For more info, see [App submissions](/windows/uwp/publish/app-submissions).</span></span>

<span data-ttu-id="84632-111">Windows PowerShell Cmdlet 可讓您在不使用存放區的情況下，安裝和管理企業營運 Windows 應用程式。</span><span class="sxs-lookup"><span data-stu-id="84632-111">Windows PowerShell cmdlets enable you to install and manage line-of-business Windows apps without using the Store.</span></span> <span data-ttu-id="84632-112">如需詳細資訊，請參閱 [Appx 模組 Cmdlet](/powershell/module/appx/index?view=win10-ps)。</span><span class="sxs-lookup"><span data-stu-id="84632-112">For more info, see [Appx Module Cmdlets](/powershell/module/appx/index?view=win10-ps).</span></span>

<span data-ttu-id="84632-113">您可以使用封裝、部署和查詢 Api，以程式設計方式執行下列工作：</span><span class="sxs-lookup"><span data-stu-id="84632-113">Using the packaging, deployment, and query APIs, you can programmatically perform these tasks:</span></span>

-   <span data-ttu-id="84632-114">建立 Windows 應用程式的應用程式套件</span><span class="sxs-lookup"><span data-stu-id="84632-114">Create an app package for a Windows app</span></span>
-   <span data-ttu-id="84632-115">部署已封裝的 Windows 應用程式</span><span class="sxs-lookup"><span data-stu-id="84632-115">Deploy a packaged Windows app</span></span>
-   <span data-ttu-id="84632-116">列舉系統上安裝的應用程式套件，並從其資訊清單取得其相關資訊</span><span class="sxs-lookup"><span data-stu-id="84632-116">Enumerate the app packages installed on a system and get information about them from their manifest</span></span>
-   <span data-ttu-id="84632-117">使用應用程式套件的內容</span><span class="sxs-lookup"><span data-stu-id="84632-117">Consume the contents of an app package</span></span>

## <a name="in-this-section"></a><span data-ttu-id="84632-118">本節內容</span><span class="sxs-lookup"><span data-stu-id="84632-118">In this section</span></span>



| <span data-ttu-id="84632-119">主題</span><span class="sxs-lookup"><span data-stu-id="84632-119">Topic</span></span>                                                                                                    | <span data-ttu-id="84632-120">描述</span><span class="sxs-lookup"><span data-stu-id="84632-120">Description</span></span>                                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="84632-121">如何建立應用程式套件 (C++)</span><span class="sxs-lookup"><span data-stu-id="84632-121">How to create an app package (C++)</span></span>](how-to-create-a-package.md)                                        | <span data-ttu-id="84632-122">瞭解如何使用封裝 API 來建立應用程式套件。</span><span class="sxs-lookup"><span data-stu-id="84632-122">Learn how to create an app package using the packaging API.</span></span>                                                                                                                           |
| [<span data-ttu-id="84632-123">如何建立應用程式套件簽署憑證</span><span class="sxs-lookup"><span data-stu-id="84632-123">How to create an app package signing certificate</span></span>](how-to-create-a-package-signing-certificate.md)      | <span data-ttu-id="84632-124">瞭解如何使用 [**MakeCert**](/windows-hardware/drivers/devtest/makecert) 和 [**Pvk2Pfx**](/windows-hardware/drivers/devtest/pvk2pfx) 建立測試程式碼簽署憑證，讓您可以簽署應用程式套件。</span><span class="sxs-lookup"><span data-stu-id="84632-124">Learn how to use [**MakeCert**](/windows-hardware/drivers/devtest/makecert) and [**Pvk2Pfx**](/windows-hardware/drivers/devtest/pvk2pfx) to create a test code signing certificate, so that you can sign your app packages.</span></span> |
| <span data-ttu-id="84632-125">[如何使用 SignTool 簽署應用程式套件](how-to-sign-a-package-using-signtool.md) \(英文\)</span><span class="sxs-lookup"><span data-stu-id="84632-125">[How to sign an app package using SignTool](how-to-sign-a-package-using-signtool.md)</span></span>                    | <span data-ttu-id="84632-126">瞭解如何使用 [**SignTool**](/windows-hardware/drivers/devtest/signtool) 來簽署您的應用程式套件，以便進行部署。</span><span class="sxs-lookup"><span data-stu-id="84632-126">Learn how to use [**SignTool**](/windows-hardware/drivers/devtest/signtool) to sign your app packages so they can be deployed.</span></span>                                                                    |
| [<span data-ttu-id="84632-127">如何針對應用程式封裝簽章錯誤進行疑難排解</span><span class="sxs-lookup"><span data-stu-id="84632-127">How to troubleshoot app package signature errors</span></span>](how-to-troubleshoot-app-package-signature-errors.md) | <span data-ttu-id="84632-128">應用程式部署失敗的原因可能是無法驗證應用程式套件的數位簽章。</span><span class="sxs-lookup"><span data-stu-id="84632-128">An app deployment failure can be caused by a failure to validate the digital signature of the app package.</span></span> <span data-ttu-id="84632-129">瞭解如何辨識這些失敗，以及該怎麼做。</span><span class="sxs-lookup"><span data-stu-id="84632-129">Learn how to recognize these failures, and what to do about them.</span></span>          |
| [<span data-ttu-id="84632-130">如何以程式設計方式簽署應用程式套件 (c + +) </span><span class="sxs-lookup"><span data-stu-id="84632-130">How to programmatically sign an app package (C++)</span></span>](how-to-programmatically-sign-a-package.md)          | <span data-ttu-id="84632-131">瞭解如何使用 [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2) 函數來簽署應用程式套件。</span><span class="sxs-lookup"><span data-stu-id="84632-131">Learn how to sign an app package by using the [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2) function.</span></span>                                                                                   |
| [<span data-ttu-id="84632-132">如何開發使用自訂檔案的 OEM 應用程式</span><span class="sxs-lookup"><span data-stu-id="84632-132">How to develop an OEM app that uses a custom file</span></span>](how-to-develop-oem-app-with-custom-file.md)         | <span data-ttu-id="84632-133">瞭解如何開發使用自訂檔案的應用程式，以將資訊從 OEM 傳遞至應用程式。</span><span class="sxs-lookup"><span data-stu-id="84632-133">Learn how to develop an app that uses a custom file to pass info from the OEM to the app.</span></span>                                                                                             |
| [<span data-ttu-id="84632-134"> (c + +) 解壓縮應用程式套件內容 </span><span class="sxs-lookup"><span data-stu-id="84632-134">Extract app package contents (C++)</span></span>](how-to-extract-content-from-a-package.md)                          | <span data-ttu-id="84632-135">瞭解如何使用封裝 API 從應用程式封裝解壓縮檔案。</span><span class="sxs-lookup"><span data-stu-id="84632-135">Learn how to extract files from an app package using the packaging API.</span></span>                                                                                                               |
| [<span data-ttu-id="84632-136">查詢應用程式封裝資訊清單資訊 (c + +) </span><span class="sxs-lookup"><span data-stu-id="84632-136">Query app package manifest info (C++)</span></span>](how-to-query-package-identity-information.md)                   | <span data-ttu-id="84632-137">瞭解如何使用封裝 API 從應用程式套件資訊清單取得資訊</span><span class="sxs-lookup"><span data-stu-id="84632-137">Learn how to get info from an app package manifest using the packaging API</span></span>                                                                                                            |
| [<span data-ttu-id="84632-138">疑難排解</span><span class="sxs-lookup"><span data-stu-id="84632-138">Troubleshooting</span></span>](troubleshooting.md)                                                                   | <span data-ttu-id="84632-139">提供資訊，協助您針對封裝、部署或查詢應用程式封裝時所遇到的問題進行疑難排解。</span><span class="sxs-lookup"><span data-stu-id="84632-139">Provides info to help you troubleshoot problems you experience when packaging, deploying, or querying an app package.</span></span>                                                                 |
| [<span data-ttu-id="84632-140">封裝 API 參考</span><span class="sxs-lookup"><span data-stu-id="84632-140">Packaging API reference</span></span>](interfaces.md)                                                                | <span data-ttu-id="84632-141">封裝 API 會建立、讀取和寫入應用程式套件。</span><span class="sxs-lookup"><span data-stu-id="84632-141">The packaging API creates, reads, and writes app packages.</span></span>                                                                                                                            |
| [<span data-ttu-id="84632-142">部署 API 參考</span><span class="sxs-lookup"><span data-stu-id="84632-142">Deployment API reference</span></span>](package-deployment-api.md)                                                   | <span data-ttu-id="84632-143">部署 API 會安裝、更新及卸載應用程式套件。</span><span class="sxs-lookup"><span data-stu-id="84632-143">The deployment API installs, updates, and uninstalls app packages.</span></span>                                                                                                                    |
| [<span data-ttu-id="84632-144">查詢 API 參考</span><span class="sxs-lookup"><span data-stu-id="84632-144">Query API reference</span></span>](functions.md)                                                                     | <span data-ttu-id="84632-145">查詢 API 會取得系統上所安裝之應用程式套件的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="84632-145">The query API gets info about the app packages installed on the system.</span></span>                                                                                                               |
| [<span data-ttu-id="84632-146">工具和 PowerShell Cmdlet</span><span class="sxs-lookup"><span data-stu-id="84632-146">Tools and PowerShell cmdlets</span></span>](appx-packaging-tools.md)                                                 | <span data-ttu-id="84632-147">使用這些工具和 Cmdlet 來建立、安裝及管理應用程式套件。</span><span class="sxs-lookup"><span data-stu-id="84632-147">Use these tools and cmdlets to create, install, and manage app packages.</span></span>                                                                                                              |
| [<span data-ttu-id="84632-148">SDK 範例</span><span class="sxs-lookup"><span data-stu-id="84632-148">SDK samples</span></span>](appx-packaging-samples.md)                                                                | <span data-ttu-id="84632-149">下載 SDK 範例，以示範適用于 Windows 應用程式的封裝、部署和查詢 Api。</span><span class="sxs-lookup"><span data-stu-id="84632-149">Download SDK samples that demonstrate the packaging, deployment, and query APIs for Windows apps.</span></span>                                                                               |
| [<span data-ttu-id="84632-150">詞彙</span><span class="sxs-lookup"><span data-stu-id="84632-150">Glossary</span></span>](appx-packaging-glossary.md)                                                                  | <span data-ttu-id="84632-151">深入瞭解封裝、部署及查詢 Windows 應用程式的相關術語。</span><span class="sxs-lookup"><span data-stu-id="84632-151">Learn about the terms related to packaging, deployment, and query of Windows apps.</span></span>                                                                                              |



 

## <a name="related-topics"></a><span data-ttu-id="84632-152">相關主題</span><span class="sxs-lookup"><span data-stu-id="84632-152">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="84632-153">**概念**</span><span class="sxs-lookup"><span data-stu-id="84632-153">**Concepts**</span></span>
</dt> <dt>

<span data-ttu-id="84632-154">[應用程式封裝和部署](/previous-versions/windows/apps/hh464929(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="84632-154">[App packages and deployment](/previous-versions/windows/apps/hh464929(v=win.10))</span></span>
</dt> <dt>

<span data-ttu-id="84632-155">**其他參考**</span><span class="sxs-lookup"><span data-stu-id="84632-155">**Other Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="84632-156">應用程式套件資訊清單結構描述</span><span class="sxs-lookup"><span data-stu-id="84632-156">App package manifest schema</span></span>](/uwp/schemas/appxpackage/appx-package-manifest)
</dt> <dt>

[<span data-ttu-id="84632-157">**ApplicationModel 封裝**</span><span class="sxs-lookup"><span data-stu-id="84632-157">**Windows.ApplicationModel.Package**</span></span>](/uwp/api/Windows.ApplicationModel.Package)
</dt> <dt>

[<span data-ttu-id="84632-158">**ApplicationModel. PackageId**</span><span class="sxs-lookup"><span data-stu-id="84632-158">**Windows.ApplicationModel.PackageId**</span></span>](/uwp/api/Windows.ApplicationModel.PackageId)
</dt> <dt>

[<span data-ttu-id="84632-159">**Windows.Management.Deployment.PackageManager**</span><span class="sxs-lookup"><span data-stu-id="84632-159">**Windows.Management.Deployment.PackageManager**</span></span>](/uwp/api/Windows.Management.Deployment.PackageManager)
</dt> <dt>

[<span data-ttu-id="84632-160">**Windows.Management.Deployment.PackageUserInformation**</span><span class="sxs-lookup"><span data-stu-id="84632-160">**Windows.Management.Deployment.PackageUserInformation**</span></span>](/uwp/api/Windows.Management.Deployment.PackageUserInformation)
</dt> </dl>

 

 