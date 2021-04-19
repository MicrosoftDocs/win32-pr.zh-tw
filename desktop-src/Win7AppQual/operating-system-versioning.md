---
description: .
ms.assetid: 974650d9-504a-4f19-bc71-90fbc92672d9
title: 作業系統版本控制
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44e71cb671e19463ca6137c9b0ce7af04c2793e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106999941"
---
# <a name="operating-system-versioning"></a><span data-ttu-id="76108-103">作業系統版本控制</span><span class="sxs-lookup"><span data-stu-id="76108-103">Operating System Versioning</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="76108-104">受影響的平臺</span><span class="sxs-lookup"><span data-stu-id="76108-104">Affected Platforms</span></span>

<span data-ttu-id="76108-105">**客戶** 端-Windows 7</span><span class="sxs-lookup"><span data-stu-id="76108-105">**Clients** - Windows 7</span></span>  
<span data-ttu-id="76108-106">**伺服器** -Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="76108-106">**Servers** - Windows Server 2008 R2</span></span>  









## <a name="feature-impact"></a><span data-ttu-id="76108-107">功能影響</span><span class="sxs-lookup"><span data-stu-id="76108-107">Feature Impact</span></span>

<span data-ttu-id="76108-108">**嚴重性** -高</span><span class="sxs-lookup"><span data-stu-id="76108-108">**Severity** - High</span></span>  
<span data-ttu-id="76108-109">**頻率** -高</span><span class="sxs-lookup"><span data-stu-id="76108-109">**Frequency** - High</span></span>  









## <a name="description"></a><span data-ttu-id="76108-110">Description</span><span class="sxs-lookup"><span data-stu-id="76108-110">Description</span></span>

<span data-ttu-id="76108-111">Windows 7 和 Windows Server 2008 R2 的內部版本號碼是6.1。</span><span class="sxs-lookup"><span data-stu-id="76108-111">The internal version number for Windows 7 and Windows Server 2008 R2 is 6.1.</span></span> <span data-ttu-id="76108-112">在查詢時，GetVersion 函式現在會將此版本號碼傳回給應用程式。</span><span class="sxs-lookup"><span data-stu-id="76108-112">The GetVersion function will now return this version number to applications when queried.</span></span> <span data-ttu-id="76108-113">這對防毒軟體、備份、公用程式和禁止複製來說特別重要。</span><span class="sxs-lookup"><span data-stu-id="76108-113">This is especially important for AntiVirus, backup, utility applications, and copy protection.</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="76108-114">影響的表現</span><span class="sxs-lookup"><span data-stu-id="76108-114">Manifestation of Impact</span></span>

<span data-ttu-id="76108-115">這項變更的表現是應用程式特定的。</span><span class="sxs-lookup"><span data-stu-id="76108-115">The manifestation of this change is application-specific.</span></span> <span data-ttu-id="76108-116">這表示，任何特別檢查作業系統版本的應用程式都會取得較高的版本號碼，而這可能會導致下列一或多個情況：</span><span class="sxs-lookup"><span data-stu-id="76108-116">This means that any application that specifically checks for the operating system version will get a higher version number, which can lead to one or more of the following situations:</span></span>

-   <span data-ttu-id="76108-117">應用程式安裝程式可能無法安裝應用程式，且應用程式可能無法啟動</span><span class="sxs-lookup"><span data-stu-id="76108-117">Application installers might be unable to install the application, and applications might be unable to start</span></span>
-   <span data-ttu-id="76108-118">應用程式可能會變得不穩定或損毀</span><span class="sxs-lookup"><span data-stu-id="76108-118">Applications might become unstable or crash</span></span>
-   <span data-ttu-id="76108-119">應用程式可能會產生錯誤訊息，但會繼續正常運作</span><span class="sxs-lookup"><span data-stu-id="76108-119">Applications might generate error messages, but continue to function properly</span></span>

## <a name="mitigation"></a><span data-ttu-id="76108-120">降低</span><span class="sxs-lookup"><span data-stu-id="76108-120">Mitigation</span></span>

<span data-ttu-id="76108-121">大部分的應用程式在 Windows 7 和 Windows Server 2008 R2 上都能正常運作，因為 Windows 7 和 Windows Server 2008 R2 中的應用程式相容性很高。</span><span class="sxs-lookup"><span data-stu-id="76108-121">Most applications will function properly on Windows 7 and Windows Server 2008 R2 because the application compatibility in Windows 7 and Windows Server 2008 R2 is very high.</span></span> <span data-ttu-id="76108-122">不過，Windows 7 和 Windows Server 2008 R2 包含檢查作業系統版本之安裝程式和應用程式的相容性檢視。</span><span class="sxs-lookup"><span data-stu-id="76108-122">However, Windows 7 and Windows Server 2008 R2 include a Compatibility View for installers and applications that check for operating system version.</span></span>

<span data-ttu-id="76108-123">若要啟用相容性檢視，使用者可以用滑鼠右鍵按一下快捷方式或可執行檔，然後從 [相容性] 索引標籤套用 Windows XP SP2 或 Windows Vista 相容性檢視。在大多數情況下，這應該可讓應用程式正常運作，而不需要對應用程式進行任何變更。</span><span class="sxs-lookup"><span data-stu-id="76108-123">To enable the compatibility view, users can right-click the shortcut or the executable file, and then apply the Windows XP SP2 or Windows Vista Compatibility View from the Compatibility tab. In most cases, this should enable the application to operate properly without the need for any changes to the application.</span></span>

<span data-ttu-id="76108-124">IT 專業人員也可以套用任何適用的 VersionLie 相容性修正程式，其方式是使用與應用程式相容性工具組一起安裝的相容性系統管理員工具 (ACT) 。</span><span class="sxs-lookup"><span data-stu-id="76108-124">IT Professionals can also apply any of the applicable VersionLie compatibility fixes, by using the Compatibility Administrator tool, which installs with the Application Compatibility Toolkit (ACT).</span></span> <span data-ttu-id="76108-125">例如，如果應用程式無法運作，因為它正在檢查（但找不到） Windows XP® Service Pack 2 (SP2) 版本資訊，WinXPSP2VersionLie 可以套用至應用程式，以將適當的版本號碼資訊傳回給應用程式，而不論電腦上執行的實際作業系統版本為何。</span><span class="sxs-lookup"><span data-stu-id="76108-125">For example, if an application fails to function because it is checking for, but not finding, the Windows XP® with Service Pack 2 (SP2) version information, the WinXPSP2VersionLie can be applied to return the proper version number information to the application, regardless of the actual operating system version that is running on the computer.</span></span> <span data-ttu-id="76108-126">可用的 VersionLie 相容性修正如下：</span><span class="sxs-lookup"><span data-stu-id="76108-126">The available VersionLie compatibility fixes are:</span></span>

-   <span data-ttu-id="76108-127">Win95VersionLie</span><span class="sxs-lookup"><span data-stu-id="76108-127">Win95VersionLie</span></span>
-   <span data-ttu-id="76108-128">Win98VersionLie</span><span class="sxs-lookup"><span data-stu-id="76108-128">Win98VersionLie</span></span>
-   <span data-ttu-id="76108-129">WinNT4SP5VersionLie</span><span class="sxs-lookup"><span data-stu-id="76108-129">WinNT4SP5VersionLie</span></span>
-   <span data-ttu-id="76108-130">Win2000VersionLie</span><span class="sxs-lookup"><span data-stu-id="76108-130">Win2000VersionLie</span></span>
-   <span data-ttu-id="76108-131">Win2000SP1VersionLie</span><span class="sxs-lookup"><span data-stu-id="76108-131">Win2000SP1VersionLie</span></span>
-   <span data-ttu-id="76108-132">Win2000SP2VersionLie</span><span class="sxs-lookup"><span data-stu-id="76108-132">Win2000SP2VersionLie</span></span>
-   <span data-ttu-id="76108-133">Win2000SP3VersionLie</span><span class="sxs-lookup"><span data-stu-id="76108-133">Win2000SP3VersionLie</span></span>
-   <span data-ttu-id="76108-134">WinXPVersionLie</span><span class="sxs-lookup"><span data-stu-id="76108-134">WinXPVersionLie</span></span>
-   <span data-ttu-id="76108-135">WinXPSP1VersionLie</span><span class="sxs-lookup"><span data-stu-id="76108-135">WinXPSP1VersionLie</span></span>
-   <span data-ttu-id="76108-136">WinXPSP2VersionLie</span><span class="sxs-lookup"><span data-stu-id="76108-136">WinXPSP2VersionLie</span></span>
-   <span data-ttu-id="76108-137">VistaRTMVersionLie</span><span class="sxs-lookup"><span data-stu-id="76108-137">VistaRTMVersionLie</span></span>
-   <span data-ttu-id="76108-138">VistaSP1VersionLie</span><span class="sxs-lookup"><span data-stu-id="76108-138">VistaSP1VersionLie</span></span>
-   <span data-ttu-id="76108-139">VistaSP2VersionLie</span><span class="sxs-lookup"><span data-stu-id="76108-139">VistaSP2VersionLie</span></span>
-   <span data-ttu-id="76108-140">Win2K3RTMVersionLie</span><span class="sxs-lookup"><span data-stu-id="76108-140">Win2K3RTMVersionLie</span></span>
-   <span data-ttu-id="76108-141">Win2K3SP1VersionLie</span><span class="sxs-lookup"><span data-stu-id="76108-141">Win2K3SP1VersionLie</span></span>

## <a name="solution"></a><span data-ttu-id="76108-142">解決方法</span><span class="sxs-lookup"><span data-stu-id="76108-142">Solution</span></span>

<span data-ttu-id="76108-143">一般來說，應用程式不應該執行作業系統版本檢查。</span><span class="sxs-lookup"><span data-stu-id="76108-143">Generally, applications should not perform operating system version checks.</span></span> <span data-ttu-id="76108-144">如果應用程式需要特定功能，最好先嘗試尋找該功能，而且只有在遺漏所需的功能時才會失敗。</span><span class="sxs-lookup"><span data-stu-id="76108-144">If an application needs a specific feature, it is preferable to try to find the feature, and fail only if the needed feature is missing.</span></span> <span data-ttu-id="76108-145">應用程式至少應接受大於或等於最低支援作業系統版本的版本號碼。</span><span class="sxs-lookup"><span data-stu-id="76108-145">At a minimum, applications should always accept version numbers greater than or equal to the lowest supported version of the operating system.</span></span> <span data-ttu-id="76108-146">只有在有特定的法律、企業或系統元件需求時，才會發生例外狀況。</span><span class="sxs-lookup"><span data-stu-id="76108-146">Exceptions should occur only if there is a specific legal, business, or system-component requirement.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="76108-147">其他資源的連結</span><span class="sxs-lookup"><span data-stu-id="76108-147">Links to Other Resources</span></span>

-   [<span data-ttu-id="76108-148">應用程式相容性工具組下載</span><span class="sxs-lookup"><span data-stu-id="76108-148">Application Compatibility Toolkit Download</span></span>](/windows-hardware/get-started/adk-install)
-   <span data-ttu-id="76108-149">[已知的相容性修正程式、相容性模式和 AppHelp 訊息](/previous-versions/windows/it-pro/windows-7/cc765984(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="76108-149">[Known Compatibility Fixes, Compatibility Modes, and AppHelp Messages](/previous-versions/windows/it-pro/windows-7/cc765984(v=ws.10))</span></span>

 

 
