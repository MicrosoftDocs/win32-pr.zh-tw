---
description: .
ms.assetid: 25d07e42-b5eb-4f72-b4b1-0ebb881644ba
title: 登錄機碼上的額外 Windows 資源保護
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb048a45324e52c9b9319f52f95b64361b95bbfd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979416"
---
# <a name="additional-windows-resource-protection-on-registry-keys"></a><span data-ttu-id="b421b-103">登錄機碼上的額外 Windows 資源保護</span><span class="sxs-lookup"><span data-stu-id="b421b-103">Additional Windows Resource Protection on Registry Keys</span></span>

## <a name="platform"></a><span data-ttu-id="b421b-104">平台</span><span class="sxs-lookup"><span data-stu-id="b421b-104">Platform</span></span>

<span data-ttu-id="b421b-105">**客戶** 端-Windows 7</span><span class="sxs-lookup"><span data-stu-id="b421b-105">**Clients** - Windows 7</span></span>  
<span data-ttu-id="b421b-106">**伺服器** -Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b421b-106">**Servers** - Windows Server 2008 R2</span></span>  









## <a name="feature-impact"></a><span data-ttu-id="b421b-107">功能影響</span><span class="sxs-lookup"><span data-stu-id="b421b-107">Feature Impact</span></span>

<span data-ttu-id="b421b-108">**嚴重性** -中</span><span class="sxs-lookup"><span data-stu-id="b421b-108">**Severity** - Medium</span></span>  
<span data-ttu-id="b421b-109">**頻率** -低</span><span class="sxs-lookup"><span data-stu-id="b421b-109">**Frequency** - Low</span></span>  


## <a name="description"></a><span data-ttu-id="b421b-110">Description</span><span class="sxs-lookup"><span data-stu-id="b421b-110">Description</span></span>

<span data-ttu-id="b421b-111">額外的系統資源已在 Windows 7 中新增 Windows 資源保護 (WRP) 設定，使其成為唯讀設定。</span><span class="sxs-lookup"><span data-stu-id="b421b-111">Additional system resources have added Windows Resource Protection (WRP) settings in Windows 7, making them read-only settings.</span></span> <span data-ttu-id="b421b-112">大部分接收新增保護的資源都是系統 COM 伺服器金鑰，雖然有些功能已新增目標資源保護。</span><span class="sxs-lookup"><span data-stu-id="b421b-112">The vast majority of resources that received added protection are system COM server keys, although some features have added targeted resource protection.</span></span> <span data-ttu-id="b421b-113">Microsoft 變更了這些資源，以保護系統和其他應用程式免于彼此中斷，並提供一致且穩定的平臺，讓應用程式可在其上可靠地執行。</span><span class="sxs-lookup"><span data-stu-id="b421b-113">Microsoft changed these resources in order to protect the system and other applications from breaking each other and to provide a consistent, stable platform upon which applications can reliably run.</span></span> <span data-ttu-id="b421b-114">在過去，應用程式可以提供自訂檔案，並使用未受保護的 COM 註冊來變更系統。</span><span class="sxs-lookup"><span data-stu-id="b421b-114">In the past, applications could provide custom files and use the unprotected COM registration to change the system.</span></span> <span data-ttu-id="b421b-115">在舊版的應用程式中，這可能會降級系統執行時間，或變更其他應用程式需要正常運作的介面。</span><span class="sxs-lookup"><span data-stu-id="b421b-115">In the case of older applications, this can downgrade system runtimes or change the interface upon which other applications needed to work properly.</span></span> <span data-ttu-id="b421b-116">在最糟的情況下，這類安裝可能會導致系統失敗或一段時間的降級。</span><span class="sxs-lookup"><span data-stu-id="b421b-116">In the worst case, such installations could cause system failure or degradation over time.</span></span> <span data-ttu-id="b421b-117">為了提供更好的體驗和更穩定的應用程式平臺，我們鎖定了這些註冊，因此只有 Microsoft update 可以變更系統元件。</span><span class="sxs-lookup"><span data-stu-id="b421b-117">To provide a better experience and a more stable application platform, we locked down these registrations so that only Microsoft updates could change system components.</span></span>

<span data-ttu-id="b421b-118">因為大部分的資源變更都是系統所使用的 COM 金鑰，所以這項變更不會影響大部分的應用程式。</span><span class="sxs-lookup"><span data-stu-id="b421b-118">Since most resources changed are COM keys used by the system, this change will not affect the majority of applications.</span></span> <span data-ttu-id="b421b-119">雖然我們預期大部分的應用程式在 Windows 7 上都有更佳的體驗，因為這些變更的結果，應用程式的一小部分可能會受到負面影響。</span><span class="sxs-lookup"><span data-stu-id="b421b-119">While we expect most applications to have a better experience on Windows 7 as a result of these changes, a small subset of applications may be negatively affected.</span></span> <span data-ttu-id="b421b-120">系統的應用程式相容性層級會自動通知應用程式變更設定，即使因為它是受保護的資源而失敗，也會自動解決安裝問題。</span><span class="sxs-lookup"><span data-stu-id="b421b-120">The system's application compatibility layers will automatically resolve setup problems by always telling the application that it succeeded in changing a setting, even if it failed due to it being a protected resource.</span></span> <span data-ttu-id="b421b-121">這可防止應用程式設定中斷，但如果需要變更設定才能讓應用程式正常運作，則可能會造成問題。</span><span class="sxs-lookup"><span data-stu-id="b421b-121">This prevents application setups from breaking but may cause problems if the setting needed to be changed in order for the application to function properly.</span></span>

## <a name="manifestation"></a><span data-ttu-id="b421b-122">表現</span><span class="sxs-lookup"><span data-stu-id="b421b-122">Manifestation</span></span>

<span data-ttu-id="b421b-123">在 Windows 7 之前，應用程式可能已修改這些設定。</span><span class="sxs-lookup"><span data-stu-id="b421b-123">Applications may have modified these settings prior to Windows 7.</span></span> <span data-ttu-id="b421b-124">在 Windows 7 上安裝時，應用程式可能會發現某些功能不再適用，因為這些設定未反映出應用程式的預期。</span><span class="sxs-lookup"><span data-stu-id="b421b-124">Upon installing on Windows 7, applications may find certain features no longer work because the settings did not reflect what the application expected.</span></span>

<span data-ttu-id="b421b-125">在兩種情況下，應用程式可能會遇到與此新增保護相關的問題：</span><span class="sxs-lookup"><span data-stu-id="b421b-125">There are two scenarios in which applications may encounter problems related to this added protection:</span></span>

-   <span data-ttu-id="b421b-126">可能已使用現在保護的設定做為資料存放區，或做為罕見或非預期的擴充點的應用程式</span><span class="sxs-lookup"><span data-stu-id="b421b-126">Applications that may have been using the now-protected settings as a data store or as a rare or unintended extensibility point</span></span>
-   <span data-ttu-id="b421b-127">在罕見的情況下，用來識別應用程式設定的偵測機制可能無法辨識特定的設定，因此可能不會套用應用程式相容性緩和層</span><span class="sxs-lookup"><span data-stu-id="b421b-127">In rare cases, the detection mechanism used to identify application setups may not recognize a particular setup and so the application compatibility mitigation layer may not be applied</span></span>

## <a name="mitigation"></a><span data-ttu-id="b421b-128">降低</span><span class="sxs-lookup"><span data-stu-id="b421b-128">Mitigation</span></span>

<span data-ttu-id="b421b-129">風險降低的主要方法是系統的應用程式相容性層，在偵測到應用程式時，它會自動套用至應用程式的相容性層。</span><span class="sxs-lookup"><span data-stu-id="b421b-129">The primary means of mitigation is the system's application compatibility layer, which is automatically applied to application setups when detected.</span></span> <span data-ttu-id="b421b-130">您也可以使用應用程式屬性中的 [相容性] 索引標籤，手動將它套用至任何應用程式。</span><span class="sxs-lookup"><span data-stu-id="b421b-130">You can also manually apply it to any application using the compatibility tab in the application's properties.</span></span>

<span data-ttu-id="b421b-131">這一層會藉由攔截登錄作業來解決此問題。</span><span class="sxs-lookup"><span data-stu-id="b421b-131">This layer resolves the problem by intercepting registry operations.</span></span> <span data-ttu-id="b421b-132">如果應用程式嘗試修改唯讀 (WRP) 設定，即使設定未真正變更，該層仍一律會傳回成功。</span><span class="sxs-lookup"><span data-stu-id="b421b-132">In the case where the application was attempting to modify a read-only (WRP) setting, the layer always returns success, even though the setting was not really changed.</span></span> <span data-ttu-id="b421b-133">針對大部分的應用程式，這不會造成任何問題。</span><span class="sxs-lookup"><span data-stu-id="b421b-133">For most applications, this will cause no problems.</span></span> <span data-ttu-id="b421b-134">不過，應用程式可能需要變更該設定才能正常運作，也就是上述的第一種案例。</span><span class="sxs-lookup"><span data-stu-id="b421b-134">However, there is a possibility that the application needed that setting changed in order to function properly, which is the first scenario described above.</span></span>

## <a name="solution"></a><span data-ttu-id="b421b-135">解決方法</span><span class="sxs-lookup"><span data-stu-id="b421b-135">Solution</span></span>

<span data-ttu-id="b421b-136">在上述兩個案例中：</span><span class="sxs-lookup"><span data-stu-id="b421b-136">For the two scenarios identified above:</span></span>

-   <span data-ttu-id="b421b-137">如果應用程式需要可寫入的金鑰才能運作或使用資料存放區，則除了變更應用程式之外，不會再寫入至該位置的解決方案。</span><span class="sxs-lookup"><span data-stu-id="b421b-137">If the application requires the key to be writable in order to function or use the data store, there is no solution other than changing the application so that it no longer writes to that location.</span></span>
-   <span data-ttu-id="b421b-138">如果相容性層未套用至安裝程式，則應該偵測並提供安裝失敗，並將其提供給應用程式並重新執行。</span><span class="sxs-lookup"><span data-stu-id="b421b-138">If the compatibility layer was not applied to a setup, the setup failure should be detected and offered to be applied and re-run.</span></span> <span data-ttu-id="b421b-139">應用程式也可以在相容性模式下執行，在這種情況下，一律會套用緩和層。</span><span class="sxs-lookup"><span data-stu-id="b421b-139">Applications can also run in compatibility mode, in which case the mitigation layer is always applied.</span></span>

## <a name="compatibility-tests"></a><span data-ttu-id="b421b-140">相容性測試</span><span class="sxs-lookup"><span data-stu-id="b421b-140">Compatibility Tests</span></span>

<span data-ttu-id="b421b-141">如何偵測應用程式是否已套用 WRP 緩和：</span><span class="sxs-lookup"><span data-stu-id="b421b-141">How to detect if an application had WRP mitigation applied to it:</span></span>

-   <span data-ttu-id="b421b-142">Windows Installer 知道 WRP;它會自動且無訊息地忽略寫入或修改受保護資源的嘗試。</span><span class="sxs-lookup"><span data-stu-id="b421b-142">Windows Installer is aware of WRP; it automatically and silently ignores attempts to write or modify a protected resource.</span></span> <span data-ttu-id="b421b-143">如果應用程式是隨 Windows Installer 安裝，且已啟用記錄功能，則會記錄每個登錄機碼寫入作業的警告，因為它是受 WRP 保護的資源，所以會被忽略。</span><span class="sxs-lookup"><span data-stu-id="b421b-143">If the application was installed with Windows Installer and logging was enabled, then a warning will be logged for each registry key write operation that was ignored due to its being a WRP-protected resource.</span></span>
-   <span data-ttu-id="b421b-144">WRP API 會併入 SfCIsKeyProtected，可查詢登錄機碼是否在目前的系統上受到 WRP 保護。</span><span class="sxs-lookup"><span data-stu-id="b421b-144">The WRP API incorporates SfCIsKeyProtected, which can query if a registry key is WRP-protected on the current system.</span></span> <span data-ttu-id="b421b-145">如需使用此 API 的詳細資訊，請參閱下列連結中的 WRP 專案。</span><span class="sxs-lookup"><span data-stu-id="b421b-145">See the WRP entry in MSDN in the links below for additional information on using this API.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="b421b-146">其他資源的連結</span><span class="sxs-lookup"><span data-stu-id="b421b-146">Links to Other Resources</span></span>

<dl>

[<span data-ttu-id="b421b-147">Windows 資源保護</span><span class="sxs-lookup"><span data-stu-id="b421b-147">Windows Resource Protection</span></span>](/windows/desktop/Wfp/windows-resource-protection-portal)  
</dl>

 

 
