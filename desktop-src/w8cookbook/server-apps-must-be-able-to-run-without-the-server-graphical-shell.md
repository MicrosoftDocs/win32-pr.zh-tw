---
title: 伺服器圖形化 Shell 限制
description: 伺服器應用程式必須能夠在沒有伺服器圖形化 Shell 的情況下執行
ms.assetid: 8F531497-B64D-4E79-AD7A-790EFDC6ADFE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae2a3002fc2395faba3e07d90a2322c770fe3ee9
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443219"
---
# <a name="server-apps-must-be-able-to-run-without-the-server-graphical-shell"></a><span data-ttu-id="f9e64-103">伺服器應用程式必須能夠在沒有伺服器圖形化 Shell 的情況下執行</span><span class="sxs-lookup"><span data-stu-id="f9e64-103">Server apps must be able to run without the Server Graphical Shell</span></span>

## <a name="platform"></a><span data-ttu-id="f9e64-104">平台</span><span class="sxs-lookup"><span data-stu-id="f9e64-104">Platform</span></span>

<span data-ttu-id="f9e64-105">**伺服器** – Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f9e64-105">**Servers** – Windows Server 2012</span></span> 

## <a name="description"></a><span data-ttu-id="f9e64-106">描述</span><span class="sxs-lookup"><span data-stu-id="f9e64-106">Description</span></span>

<span data-ttu-id="f9e64-107">伺服器圖形化介面（包含 Windows 檔案總管和 Internet Explorer 的功能）預設會安裝在 Windows Server 2012 的「Server 含 GUI」安裝中。</span><span class="sxs-lookup"><span data-stu-id="f9e64-107">Server Graphical Shell, the feature that includes Windows Explorer and Internet Explorer, is installed by default on “Server with a GUI” installations of Windows Server 2012.</span></span> <span data-ttu-id="f9e64-108">您可以卸載伺服器圖形化介面功能，以降低潛在的服務和效能，進而限制伺服器可能產生的重新開機次數，同時仍允許在伺服器本機上執行管理工具。</span><span class="sxs-lookup"><span data-stu-id="f9e64-108">The Server Graphical Shell feature can be uninstalled in order to reduce the potential servicing and performance footprint, thereby limiting the number of reboots that the server may incur, while still allowing management tools to be run locally on the server.</span></span>

<span data-ttu-id="f9e64-109">當系統管理員卸載伺服器圖形化介面之後，伺服器會在基本伺服器介面設定中：</span><span class="sxs-lookup"><span data-stu-id="f9e64-109">After an administrator uninstalls the Server Graphical Shell, the server is in the Minimal Server Interface configuration:</span></span>

![伺服器圖形化 shell 介面設定](images/minimalserverinterface.png)

<span data-ttu-id="f9e64-111">接著，系統管理員可以選擇在最基本的伺服器介面設定中執行 (其中包含一組本機管理工具) （預設值），而不是在伺服器上設定 GUI。</span><span class="sxs-lookup"><span data-stu-id="f9e64-111">Administrators can then opt to run in the Minimal Server Interface configuration (which includes a set of local management tools), as the default, rather than in the Server with a GUI configuration.</span></span> <span data-ttu-id="f9e64-112">這可允許本機監視和管理，同時降低服務的資源使用量和頻率。</span><span class="sxs-lookup"><span data-stu-id="f9e64-112">This allows local monitoring and management, while reducing both resource usage and frequency of servicing.</span></span>

<span data-ttu-id="f9e64-113">系統管理員可以在稍後需要它的功能時，重新安裝伺服器圖形化 Shell。</span><span class="sxs-lookup"><span data-stu-id="f9e64-113">Administrators can reinstall Server Graphical Shell later if they need the functionality within it.</span></span> <span data-ttu-id="f9e64-114"> (系統管理員也可以從 Server Core 安裝開始，並使用功能隨選功能將「建立」至基本伺服器介面設定。 ) </span><span class="sxs-lookup"><span data-stu-id="f9e64-114">(Administrators can also start from a Server Core install, and “build up” to the Minimal Server Interface configuration using the Features On Demand functionality.)</span></span>

<span data-ttu-id="f9e64-115">伺服器應用程式必須能夠在最基本的伺服器介面設定中執行，才能利用降低的資源使用率和服務使用量。</span><span class="sxs-lookup"><span data-stu-id="f9e64-115">Server apps must be capable of running in the Minimal Server Interface configuration to take advantage of the reduced resource utilization and servicing footprint.</span></span> <span data-ttu-id="f9e64-116">這項功能的達成方式是讓系統管理員選擇不安裝需要伺服器圖形化 Shell 的部分應用程式，或偵測伺服器圖形化 Shell 的存在，並停用應用程式的某些層面。</span><span class="sxs-lookup"><span data-stu-id="f9e64-116">This capability can be achieved by allowing the administrator to choose not to install parts of the app that needs the Server Graphical Shell, or by detecting the presence of Server Graphical Shell and disabling some aspects of the app.</span></span>

<span data-ttu-id="f9e64-117">基本伺服器介面具有降低的資源和服務使用量，因為伺服器圖形化介面中包含的許多 Api 和二進位檔無法在此設定中使用。</span><span class="sxs-lookup"><span data-stu-id="f9e64-117">The Minimal Server Interface has a reduced resource and servicing footprint because many APIs and binaries that are included in the Server Graphical Shell are not available in this configuration.</span></span> <span data-ttu-id="f9e64-118">在適當的情況下，伺服器應用程式也應該允許遠端系統管理 (最好透過另一部 Windows Server 或 Windows 用戶端安裝 Windows PowerShell 遠端) 。</span><span class="sxs-lookup"><span data-stu-id="f9e64-118">Where appropriate, server apps should also allow remote administration (preferably via Windows PowerShell Remoting) from another Windows Server or Windows Client installation.</span></span> <span data-ttu-id="f9e64-119">這可讓您更妥善地集中管理基本伺服器介面設定中的一部或多部電腦，或較低使用量設定（例如 Server Core）中的電腦。</span><span class="sxs-lookup"><span data-stu-id="f9e64-119">This enables better centralized administration of one or more machines in the Minimal Server Interface configuration, or of machines in an even lower footprint configuration such as Server Core.</span></span>

## <a name="manifestation"></a><span data-ttu-id="f9e64-120">表現</span><span class="sxs-lookup"><span data-stu-id="f9e64-120">Manifestation</span></span>

<span data-ttu-id="f9e64-121">如果應用程式需要基本伺服器介面設定中未提供的任何 Api 或二進位檔，可能不會在畫面上正確顯示，也可能無法使用。</span><span class="sxs-lookup"><span data-stu-id="f9e64-121">If an app requires any of the APIs or binaries that are not available in the Minimal Server Interface configuration, it may not display properly on the screen and/or be unusable.</span></span>

## <a name="mitigation"></a><span data-ttu-id="f9e64-122">降低</span><span class="sxs-lookup"><span data-stu-id="f9e64-122">Mitigation</span></span>

<span data-ttu-id="f9e64-123">伺服器應用程式開發人員應該找出需要任何移除的 Api 或二進位檔的應用程式部分，並包含伺服器系統管理員的資訊，以識別使用基本伺服器介面時無法正確執行的應用程式元件。</span><span class="sxs-lookup"><span data-stu-id="f9e64-123">Server app developers should identify those parts of their apps that require any of the removed APIs or binaries and include info for the server administrator identifying the parts of the app that won’t run properly when using the Minimal Server Interface.</span></span> <span data-ttu-id="f9e64-124">如果應用程式的這些部分可以選擇性地安裝或不是產品功能的絕對必要元件，則仍可在基本伺服器介面設定下安裝並執行應用程式。</span><span class="sxs-lookup"><span data-stu-id="f9e64-124">If those parts of the app can be optionally installed or are not absolutely required for product functionality, the app can still be installed and run under the Minimal Server Interface configuration.</span></span>

<span data-ttu-id="f9e64-125">如果應用程式完全無法在沒有伺服器圖形化介面的情況下使用，則應記錄這項限制，並指示伺服器系統管理員安裝伺服器圖形化介面。</span><span class="sxs-lookup"><span data-stu-id="f9e64-125">If the app cannot be used at all without the Server Graphical Shell, this limitation should be documented and the server administrator should be instructed to install the Server Graphical Shell.</span></span> <span data-ttu-id="f9e64-126"> (如果新增至 Server Core 安裝，這可能需要使用隨選功能來新增功能。 ) 此外，應用程式應該在啟動時檢查是否有所有必要的檔案可供使用，因為伺服器圖形化介面可以在安裝應用程式之前或之後卸載。</span><span class="sxs-lookup"><span data-stu-id="f9e64-126">(If adding to a Server Core installation, this might require adding features using Features On Demand.) In addition, the app should check on startup that all required files are available, as the Server Graphical Shell can be uninstalled at any time before or after the installation of the app.</span></span>

## <a name="solution"></a><span data-ttu-id="f9e64-127">解決方法</span><span class="sxs-lookup"><span data-stu-id="f9e64-127">Solution</span></span>

<span data-ttu-id="f9e64-128">依賴最小的一組相依性，以及模組化應用程式，讓核心應用程式功能可以運作，而不需要安裝更多重量級使用者介面元件。</span><span class="sxs-lookup"><span data-stu-id="f9e64-128">Rely on the smallest possible set of dependencies, and modularize apps so that the core app functionality can work without requiring more heavyweight user interface components installed.</span></span> <span data-ttu-id="f9e64-129">開發不需要任何已移除之 Api 或二進位檔的應用程式，而是改為依賴基本伺服器介面或 Server Core 內所含的功能。</span><span class="sxs-lookup"><span data-stu-id="f9e64-129">Develop apps that do not require any of the removed APIs or binaries, and rely instead on the functionality contained within the Minimal Server Interface or Server Core.</span></span> <span data-ttu-id="f9e64-130">這樣可減少維護需求，同時提高效能和使用者滿意度。</span><span class="sxs-lookup"><span data-stu-id="f9e64-130">This will reduce maintenance requirements while improving performance and user satisfaction.</span></span>

<span data-ttu-id="f9e64-131">當伺服器圖形化介面可用時，應用程式的某些部分可能會新增重要的功能，應用程式開發人員可以：</span><span class="sxs-lookup"><span data-stu-id="f9e64-131">Where there are parts of an app that might add significant functionality when the Server Graphical Shell is available, app developers can:</span></span>

-   <span data-ttu-id="f9e64-132">允許這些額外的功能，讓您可以選擇性地安裝使用伺服器圖形化介面，以便在基本伺服器介面設定上從安裝中省略</span><span class="sxs-lookup"><span data-stu-id="f9e64-132">Allow these additional features making use of Server Graphical Shell to be optionally installed, so they can be omitted from installations on a Minimal Server Interface configuration</span></span>
-   <span data-ttu-id="f9e64-133">偵測伺服器圖形化 Shell 是否存在，並調整應用程式行為</span><span class="sxs-lookup"><span data-stu-id="f9e64-133">Detect the presence of Server Graphical Shell and adapt the app behavior</span></span>

<span data-ttu-id="f9e64-134">應用程式開發人員也應該確保伺服器應用程式能夠在適當的情況下遠端系統管理。</span><span class="sxs-lookup"><span data-stu-id="f9e64-134">App developers should also ensure that server apps are remotely manageable where possible and appropriate.</span></span>

## <a name="detecting-minimal-server-interface-and-server-core"></a><span data-ttu-id="f9e64-135">偵測基本伺服器介面和 Server Core</span><span class="sxs-lookup"><span data-stu-id="f9e64-135">Detecting Minimal Server Interface and Server Core</span></span>

<span data-ttu-id="f9e64-136">Windows Server 將會為安裝的每個伺服器層級安裝對應的登錄值。</span><span class="sxs-lookup"><span data-stu-id="f9e64-136">Windows Server will install a corresponding registry value for each server level installed.</span></span> <span data-ttu-id="f9e64-137">您可以查詢這些機碼是否存在，以判斷是否已安裝並啟用伺服器圖形化 Shell 或基本伺服器介面功能。</span><span class="sxs-lookup"><span data-stu-id="f9e64-137">You can query for the existence of these keys to determine if the Server Graphical Shell or Minimal Server Interface features are installed and enabled.</span></span>

<span data-ttu-id="f9e64-138">HKEY \_ LOCAL \_ MACHINE \\ SOFTWARE \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Server \\ ServerLevels：</span><span class="sxs-lookup"><span data-stu-id="f9e64-138">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\Server\\ServerLevels:</span></span>



|   &nbsp;         | <span data-ttu-id="f9e64-139">Server Core</span><span class="sxs-lookup"><span data-stu-id="f9e64-139">Server Core</span></span> | <span data-ttu-id="f9e64-140">基本伺服器介面</span><span class="sxs-lookup"><span data-stu-id="f9e64-140">Minimal Server Interface</span></span> | <span data-ttu-id="f9e64-141">伺服器圖形化 Shell</span><span class="sxs-lookup"><span data-stu-id="f9e64-141">Server Graphical Shell</span></span> |
|------------------|-------------|--------------------------|------------------------|
| <span data-ttu-id="f9e64-142">ServerCore = 1</span><span class="sxs-lookup"><span data-stu-id="f9e64-142">ServerCore=1</span></span>     | <span data-ttu-id="f9e64-143">X</span><span class="sxs-lookup"><span data-stu-id="f9e64-143">X</span></span>           | <span data-ttu-id="f9e64-144">X</span><span class="sxs-lookup"><span data-stu-id="f9e64-144">X</span></span>                        | <span data-ttu-id="f9e64-145">X</span><span class="sxs-lookup"><span data-stu-id="f9e64-145">X</span></span>                      |
| <span data-ttu-id="f9e64-146">伺服器-GuiMgmt = 1</span><span class="sxs-lookup"><span data-stu-id="f9e64-146">Server-GuiMgmt=1</span></span> |             | <span data-ttu-id="f9e64-147">X</span><span class="sxs-lookup"><span data-stu-id="f9e64-147">X</span></span>                        | <span data-ttu-id="f9e64-148">X</span><span class="sxs-lookup"><span data-stu-id="f9e64-148">X</span></span>                      |
| <span data-ttu-id="f9e64-149">ServerGuiShell = 1</span><span class="sxs-lookup"><span data-stu-id="f9e64-149">ServerGuiShell=1</span></span> |             |                          | <span data-ttu-id="f9e64-150">X</span><span class="sxs-lookup"><span data-stu-id="f9e64-150">X</span></span>                      |



 

<span data-ttu-id="f9e64-151">上表中的 "X" 代表安裝對應的功能時，將會出現登錄機碼。</span><span class="sxs-lookup"><span data-stu-id="f9e64-151">An “X” in the table above means that registry key will be present when the corresponding feature is installed.</span></span>

<span data-ttu-id="f9e64-152">請注意，這些伺服器層級是加法。如果已安裝伺服器圖形化介面，則為基本伺服器介面和 Server Core。</span><span class="sxs-lookup"><span data-stu-id="f9e64-152">Note that these server levels are additive; if the Server Graphical Shell is installed, so is the Minimal Server Interface and Server Core.</span></span> <span data-ttu-id="f9e64-153">在此情況下，這兩個登錄機碼都將存在。</span><span class="sxs-lookup"><span data-stu-id="f9e64-153">In that case, both registry keys will be present.</span></span>

## <a name="tests"></a><span data-ttu-id="f9e64-154">測試</span><span class="sxs-lookup"><span data-stu-id="f9e64-154">Tests</span></span>

<span data-ttu-id="f9e64-155">檢查您的應用程式程式碼中是否有使用任何已移除 Api 和二進位檔的需求。</span><span class="sxs-lookup"><span data-stu-id="f9e64-155">Inspect your app code for requirements that use any of the removed APIs and binaries.</span></span> <span data-ttu-id="f9e64-156">從「核心應用程式」二進位檔移除任何這些實例之後，請在不包含伺服器圖形化介面的環境中測試您的應用程式。</span><span class="sxs-lookup"><span data-stu-id="f9e64-156">After you have removed any instances of these from “core application” binaries, test your app in an environment that does not include the Server Graphical Shell.</span></span> <span data-ttu-id="f9e64-157">進程監視器等工具可能有助於解決此情況。</span><span class="sxs-lookup"><span data-stu-id="f9e64-157">Tools such as the Process Monitor might help with this.</span></span>

<span data-ttu-id="f9e64-158">如果您無法完全停止使用這些 Api 和二進位檔，請確定您的應用程式在基本伺服器介面或 Server Core 上執行時，正常地失敗。</span><span class="sxs-lookup"><span data-stu-id="f9e64-158">If you cannot completely discontinue use of these APIs and binaries, ensure that your app fails gracefully when run on Minimal Server Interface or Server Core.</span></span>

## <a name="resources"></a><span data-ttu-id="f9e64-159">資源</span><span class="sxs-lookup"><span data-stu-id="f9e64-159">Resources</span></span>

-   <span data-ttu-id="f9e64-160">[MSDN 上的現有伺服器核心檔](/previous-versions/windows/desktop/legacy/ms723891(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f9e64-160">[Existing Server Core docs on MSDN](/previous-versions/windows/desktop/legacy/ms723891(v=vs.85))</span></span>

 

 