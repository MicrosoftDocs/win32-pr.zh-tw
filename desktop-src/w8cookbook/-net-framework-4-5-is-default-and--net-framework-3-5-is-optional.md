---
title: .NET Framework 預設設定
description: .NET Framework 4.5 是預設值，.NET Framework 3.5 是選擇性的
ms.assetid: 19B53C82-812A-49AC-87C6-C08E7C199208
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab1f91acc8739b2c660bfb1ba1392ea192511d1c
ms.sourcegitcommit: 46376be61d3fa308f9b1a06d7e2fa122a39755af
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/10/2020
ms.locfileid: "106991112"
---
# <a name="net-framework-45-is-default-and-net-framework-35-is-optional"></a><span data-ttu-id="8c15b-103">.NET Framework 4.5 是預設值，.NET Framework 3.5 是選擇性的</span><span class="sxs-lookup"><span data-stu-id="8c15b-103">.NET Framework 4.5 is default and .NET Framework 3.5 is optional</span></span>

## <a name="platforms"></a><span data-ttu-id="8c15b-104">平台</span><span class="sxs-lookup"><span data-stu-id="8c15b-104">Platforms</span></span>

<span data-ttu-id="8c15b-105">**用戶端**   Windows 8</span><span class="sxs-lookup"><span data-stu-id="8c15b-105">**Clients**   Windows 8</span></span>  
<span data-ttu-id="8c15b-106">**伺服器**   Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8c15b-106">**Servers**   Windows Server 2012</span></span>  

## <a name="description"></a><span data-ttu-id="8c15b-107">Description</span><span class="sxs-lookup"><span data-stu-id="8c15b-107">Description</span></span>

<span data-ttu-id="8c15b-108">預設會在 Windows 8 中啟用 .NET Framework 4.5。</span><span class="sxs-lookup"><span data-stu-id="8c15b-108">.NET Framework 4.5 is enabled by default in Windows 8.</span></span> <span data-ttu-id="8c15b-109">Windows 8 預設不包含 .NET 3.5，但 Windows 8 安裝媒體上有提供適用于 .NET 3.5 的檔案做為選擇性功能。</span><span class="sxs-lookup"><span data-stu-id="8c15b-109">Windows 8 does not include .NET 3.5 by default, but the files for .NET 3.5 are available on the Windows 8 installation media as an optional feature.</span></span>

<span data-ttu-id="8c15b-110">如果使用者是從 Windows 7 升級至 Windows 8，.NET Framework 3.5 已完全啟用，以確保電腦上的任何應用程式都能正常運作。</span><span class="sxs-lookup"><span data-stu-id="8c15b-110">If the user is upgrading from Windows 7 to Windows 8, .NET Framework 3.5 is fully enabled to ensure that any apps on the computer continue to work correctly.</span></span>

## <a name="manifestation"></a><span data-ttu-id="8c15b-111">表現</span><span class="sxs-lookup"><span data-stu-id="8c15b-111">Manifestation</span></span>

<span data-ttu-id="8c15b-112">如果使用者執行 Windows 8 的全新安裝，然後安裝需要 .NET Framework 3.5 (或 2.0) 的應用程式，則會觸發必要 .NET 3.5 檔案的要求。</span><span class="sxs-lookup"><span data-stu-id="8c15b-112">If the user performs a clean installation of Windows 8, and then installs apps that require .NET Framework 3.5 (or 2.0), they will trigger a request for the necessary .NET 3.5 files.</span></span> <span data-ttu-id="8c15b-113">通常會在要求使用者提供許可權) 之後，從 Windows Update (下載遺失的檔案，但如果不能存取 Windows Update，除非已指定遺漏檔案的替代來源，否則啟用 .NET Framework 3.5 將會失敗。</span><span class="sxs-lookup"><span data-stu-id="8c15b-113">Normally the missing files will be downloaded from Windows Update (after asking the user for permission), but if access to Windows Update is not possible, enabling .NET Framework 3.5 will fail unless an alternate source for the missing files has been specified.</span></span>

## <a name="mitigation"></a><span data-ttu-id="8c15b-114">降低</span><span class="sxs-lookup"><span data-stu-id="8c15b-114">Mitigation</span></span>

<span data-ttu-id="8c15b-115">若只要使用全新的 Windows 8 安裝在測試電腦上啟用 .NET Framework 3.5：</span><span class="sxs-lookup"><span data-stu-id="8c15b-115">To enable .NET Framework 3.5 on only test machines with clean installs of Windows 8:</span></span>

1.  <span data-ttu-id="8c15b-116">\\ \\ \\ 從裝載的作業系統組建 ISO 映像將來源 sxs 複製到 dotnet35 或類似資料夾。</span><span class="sxs-lookup"><span data-stu-id="8c15b-116">Copy \\sources\\sxs\\ from the mounted operating system build ISO image to dotnet35 or similar folder.</span></span> <span data-ttu-id="8c15b-117">例如：</span><span class="sxs-lookup"><span data-stu-id="8c15b-117">For example:</span></span>
    ```
    xcopy e:\sources\sxs\*.* c:\dotnet35 /s
    ```



2.  <span data-ttu-id="8c15b-118">使用系統管理員許可權來執行此命令列：</span><span class="sxs-lookup"><span data-stu-id="8c15b-118">Execute this command line using admin privileges:</span></span>
    ```
    Dism.exe /online /enable-feature /featurename:NetFX3 /All /Source:c:\dotnet35 /LimitAccess

    ```



> [!Note]  
> <span data-ttu-id="8c15b-119">\\因為這不是支援的機制，所以不能使用來源 SxS 資料夾做為轉散發機制。</span><span class="sxs-lookup"><span data-stu-id="8c15b-119">The sources\\SxS folder must not be used as a redistribution mechanism since this is not a supported mechanism.</span></span>



## <a name="solution"></a><span data-ttu-id="8c15b-120">解決方法</span><span class="sxs-lookup"><span data-stu-id="8c15b-120">Solution</span></span>

<span data-ttu-id="8c15b-121">**針對取用者：**</span><span class="sxs-lookup"><span data-stu-id="8c15b-121">**For consumers:**</span></span>

<span data-ttu-id="8c15b-122">Windows 8 包含一種機制，可在嘗試安裝可轉散發套件或需要 .NET 3.5 的應用程式安裝程式叫用可轉散發套件時，自動啟用 .NET Framework 3.5。</span><span class="sxs-lookup"><span data-stu-id="8c15b-122">Windows 8 includes a mechanism that automatically enables .NET Framework 3.5 when attempting to install the redistributable package or when an application installer that needs .NET 3.5 invokes the redistributable.</span></span>

<span data-ttu-id="8c15b-123">**針對應用程式開發人員 (和 IT 系統管理員) ：**</span><span class="sxs-lookup"><span data-stu-id="8c15b-123">**For App developers (and IT Administrators):**</span></span>

<span data-ttu-id="8c15b-124">IT 系統管理員可以根據已安裝的) ，將 .NET 3.5 應用程式設定為在 .NET 3.5 或 .NET 4.5 (上執行。</span><span class="sxs-lookup"><span data-stu-id="8c15b-124">IT administrators can configure .NET 3.5 apps to run on either .NET 3.5 or .NET 4.5 (depending on what's already installed).</span></span> <span data-ttu-id="8c15b-125">若要在3.5 或4.5 上執行受管理的應用程式，只需在應用程式佈建檔中新增一個區段。</span><span class="sxs-lookup"><span data-stu-id="8c15b-125">In order to run a managed app on either 3.5 or 4.5, just add a section in the application configuration file.</span></span> <span data-ttu-id="8c15b-126">這可確保如果已安裝 .NET 3.5，應用程式將會在 .NET 3.5 上執行;否則，應用程式將會在 .NET 4.5 上執行。</span><span class="sxs-lookup"><span data-stu-id="8c15b-126">This will ensure that if .NET 3.5 is installed, the app will run on .NET 3.5; otherwise the app will run on .NET 4.5.</span></span> <span data-ttu-id="8c15b-127">以下提供設定檔中其他區段的範例：</span><span class="sxs-lookup"><span data-stu-id="8c15b-127">An example of the additional section in the configuration file is provided below:</span></span>


```
<configuration>
   <startup>
      <supportedRuntime version="v2.0.50727"/>
      <supportedRuntime version="v4.0" sku=".NETFramework,Version=v4.5"/>
   </startup>
</configuration>
```



<span data-ttu-id="8c15b-128">**針對企業 Oem：**</span><span class="sxs-lookup"><span data-stu-id="8c15b-128">**For enterprise OEMs:**</span></span>

<span data-ttu-id="8c15b-129">若要為 EEAP 組建和沒有 Windows Update 存取權的應用程式啟用 .NET Framework 3.5：</span><span class="sxs-lookup"><span data-stu-id="8c15b-129">To enable .NET Framework 3.5 for EEAP builds and for applications that do not have access to Windows Update:</span></span>

1.  <span data-ttu-id="8c15b-130">\\ \\ \\ 從裝載的作業系統組建 ISO 映像將來源 sxs 複製到 dotnet35 或類似的資料夾。</span><span class="sxs-lookup"><span data-stu-id="8c15b-130">Copy \\sources\\sxs\\ from the mounted OS build ISO image to the dotnet35 or similar folder.</span></span> <span data-ttu-id="8c15b-131">例如：</span><span class="sxs-lookup"><span data-stu-id="8c15b-131">For example:</span></span>
    ```
    xcopy e:\sources\sxs\*.* c:\dotnet35 /s
    ```



2.  <span data-ttu-id="8c15b-132">設定 regkey：</span><span class="sxs-lookup"><span data-stu-id="8c15b-132">Set the regkey:</span></span>
    ```
    [HKLM\SOFTWARE\Microsoft\Windows\CurrentVersion\Policies\Servicing]
     LocalSourcePath = c:\dotnet35
    ```



<span data-ttu-id="8c15b-133">**適用于企業：**</span><span class="sxs-lookup"><span data-stu-id="8c15b-133">**For enterprises:**</span></span>

<span data-ttu-id="8c15b-134">針對設定為使用 WSUS 進行服務的電腦，您可以設定登錄專案以允許電腦使用 Windows Update 來啟用 .NET 3.5，而不是 WSUS (服務仍會從 WSUS 執行（如果您這樣做) ）。</span><span class="sxs-lookup"><span data-stu-id="8c15b-134">For machines that are configured to use WSUS for servicing, you can set a registry entry to allow the machine to use Windows Update for enabling .NET 3.5 instead of WSUS (servicing will still be done from WSUS if you do this).</span></span>

-   <span data-ttu-id="8c15b-135">設定 regkey：</span><span class="sxs-lookup"><span data-stu-id="8c15b-135">Set the regkey:</span></span>
    ```
    [HKLM\SOFTWARE\Microsoft\Windows\CurrentVersion\Policies\Servicing]  RepairContentServerSource =DWORD(2)
    ```



<span data-ttu-id="8c15b-136">此登錄專案也可以透過群組原則 (本機電腦原則-> 電腦設定-> 系統管理範本 > 系統設定。</span><span class="sxs-lookup"><span data-stu-id="8c15b-136">This registry entry can also be set via Group Policy (Local Computer Policy -> Computer Configuration -> Administrative Templates -> System.</span></span> <span data-ttu-id="8c15b-137">選取 [指定選用元件安裝和元件修復的設定]。</span><span class="sxs-lookup"><span data-stu-id="8c15b-137">Select the setting  Specify settings for optional component installation and component repair .</span></span>

<span data-ttu-id="8c15b-138">如果您選取 [連絡人] Windows Update 直接下載修復內容，而不是 Windows Server Update Services (WSUS) ，則任何新增 Windows 功能的嘗試 (例如 .NET Framework 3.5) 或修復功能都會從 Windows Update 觸發檔案下載。</span><span class="sxs-lookup"><span data-stu-id="8c15b-138">If you select  Contact Windows Update directly to download repair content instead of Windows Server Update Services (WSUS) , any attempts to add Windows features (for example, .NET Framework 3.5) or repair features will trigger file downloads from Windows Update.</span></span> <span data-ttu-id="8c15b-139">目的電腦需要此選項的網際網路和 WU 存取權。</span><span class="sxs-lookup"><span data-stu-id="8c15b-139">Target computers require Internet and WU access for this option.</span></span> <span data-ttu-id="8c15b-140">正常的服務作業如果已設定為來源，則會繼續使用 WSUS。</span><span class="sxs-lookup"><span data-stu-id="8c15b-140">Normal servicing operations continue to use WSUS if it has been configured as a source.</span></span>

<span data-ttu-id="8c15b-141">**關於透過登錄專案設定本機來源位置的注意事項**</span><span class="sxs-lookup"><span data-stu-id="8c15b-141">**A note regarding setting local source location via registry entries**</span></span>

<span data-ttu-id="8c15b-142">IT 系統管理員可以透過登錄專案設定 .NET 3.5 檔案的本機來源位置 (s) ，讓使用者可以使用 [新增/移除 Windows 功能] 對話方塊來啟用具有遺失承載的功能，而不需指定來源位置。</span><span class="sxs-lookup"><span data-stu-id="8c15b-142">IT administrators can set local source location(s) for .NET 3.5 files via a registry entry, so that users can use the Add/Remove Windows Features dialog to enable features with missing payload without having to specify a source location.</span></span> <span data-ttu-id="8c15b-143">您可以透過群組原則來控制登錄專案的值。</span><span class="sxs-lookup"><span data-stu-id="8c15b-143">The value of the registry entry can be controlled via group policy.</span></span>

<span data-ttu-id="8c15b-144">支援此登錄專案：</span><span class="sxs-lookup"><span data-stu-id="8c15b-144">This registry entry is supported:</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="8c15b-145">進入</span><span class="sxs-lookup"><span data-stu-id="8c15b-145">Entry</span></span></th>
<th><span data-ttu-id="8c15b-146">類型</span><span class="sxs-lookup"><span data-stu-id="8c15b-146">Type</span></span></th>
<th><span data-ttu-id="8c15b-147">Description</span><span class="sxs-lookup"><span data-stu-id="8c15b-147">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8c15b-148">本機來源路徑</span><span class="sxs-lookup"><span data-stu-id="8c15b-148">Local Source Path</span></span></td>
<td><span data-ttu-id="8c15b-149"> REG_EXPAND_SZ </span><span class="sxs-lookup"><span data-stu-id="8c15b-149">REG_EXPAND_SZ</span></span></td>
<td><span data-ttu-id="8c15b-150">預設會使用本機來源路徑)  (s。</span><span class="sxs-lookup"><span data-stu-id="8c15b-150">Local source path(s) to be used by default.</span></span> <span data-ttu-id="8c15b-151">可以指定多個路徑;它們應該以; 分隔。</span><span class="sxs-lookup"><span data-stu-id="8c15b-151">Multiple paths can be specified; they should be separated by  ; .</span></span> <span data-ttu-id="8c15b-152">系統會依照指定的順序來搜尋位置。</span><span class="sxs-lookup"><span data-stu-id="8c15b-152">Locations will be searched in the order they are specified.</span></span> <br/> <span data-ttu-id="8c15b-153">在 DISM 命令列上指定的本機來源位置 (s) ，優先于此登錄專案中指定的位置。</span><span class="sxs-lookup"><span data-stu-id="8c15b-153">Local source location(s) that are specified on the DISM command line, take precedence over locations specified in this registry entry.</span></span> <span data-ttu-id="8c15b-154">您可以在此登錄專案中指定資料夾位置。</span><span class="sxs-lookup"><span data-stu-id="8c15b-154">Folder locations can be specified in this registry entry.</span></span> <br/> <span data-ttu-id="8c15b-155">您可以使用 Wim，但路徑必須是 WIM 檔案;不需要掛接它，例如：</span><span class="sxs-lookup"><span data-stu-id="8c15b-155">WIMs can be used, but the path must be to the WIM file; there is no need to mount it, for example:</span></span> <br/> <dl> <span data-ttu-id="8c15b-156">wim： \\ machine\share\file.wim：1</span><span class="sxs-lookup"><span data-stu-id="8c15b-156">wim:\\machine\share\file.wim:1</span></span><br />
</dl> <span data-ttu-id="8c15b-157">請注意結尾的1。</span><span class="sxs-lookup"><span data-stu-id="8c15b-157">Notice the  1  at the end.</span></span> <span data-ttu-id="8c15b-158">您必須指定要在 WIM 檔案中使用之映射的數值索引。</span><span class="sxs-lookup"><span data-stu-id="8c15b-158">You must specify the numerical index of the image you want to use in the WIM file.</span></span> <br/> <span data-ttu-id="8c15b-159">若為掛接的 WIM，來源路徑必須參考掛接映射的 windows 目錄，而不是指向掛接點 (例如：/source： <mount_point> \windows，而不是/source： <mount_point>) 。</span><span class="sxs-lookup"><span data-stu-id="8c15b-159">For a mounted WIM, the source path needs to refer to the windows directory of the mounted image, rather than to the mount point (for example: /source:<mount_point>\windows rather than /source:<mount_point>).</span></span> <br/></td>
</tr>
</tbody>
</table>





## <a name="resources"></a><span data-ttu-id="8c15b-160">資源</span><span class="sxs-lookup"><span data-stu-id="8c15b-160">Resources</span></span>

<dl>

[<span data-ttu-id="8c15b-161">執行以登錄為基礎的原則</span><span class="sxs-lookup"><span data-stu-id="8c15b-161">Implementing Registry-based Policy</span></span>](/previous-versions/windows/desktop/Policy/implementing-registry-based-policy)  
</dl>