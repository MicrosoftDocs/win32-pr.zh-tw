---
title: 桌面視窗管理員一律開啟
description: 桌面視窗管理員一律開啟
ms.assetid: 36E2DD1B-E480-47A9-850B-3057119641C0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f855635615dee734b9a719d4e51d3ead663d144e
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/01/2020
ms.locfileid: "104316591"
---
# <a name="desktop-window-manager-is-always-on"></a><span data-ttu-id="0eaec-103">桌面視窗管理員一律開啟</span><span class="sxs-lookup"><span data-stu-id="0eaec-103">Desktop Window Manager is always on</span></span>

## <a name="platforms"></a><span data-ttu-id="0eaec-104">平台</span><span class="sxs-lookup"><span data-stu-id="0eaec-104">Platforms</span></span>

<span data-ttu-id="0eaec-105">**用戶端** – Windows 8</span><span class="sxs-lookup"><span data-stu-id="0eaec-105">**Clients** – Windows 8</span></span>  
<span data-ttu-id="0eaec-106">**伺服器** – Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0eaec-106">**Servers** – Windows Server 2012</span></span>  


## <a name="description"></a><span data-ttu-id="0eaec-107">Description</span><span class="sxs-lookup"><span data-stu-id="0eaec-107">Description</span></span>

<span data-ttu-id="0eaec-108">在 Windows 8 中，桌面視窗管理員 (DWM) 一律為開啟狀態，且使用者和應用程式無法停用。</span><span class="sxs-lookup"><span data-stu-id="0eaec-108">In Windows 8, Desktop Window Manager (DWM) is always ON and cannot be disabled by end users and apps.</span></span> <span data-ttu-id="0eaec-109">在 Windows 7 中，會使用 DWM 來撰寫桌面。</span><span class="sxs-lookup"><span data-stu-id="0eaec-109">As in Windows 7, DWM is used to compose the desktop.</span></span> <span data-ttu-id="0eaec-110">除了在 Windows 7 中啟用的經驗之外，現在 DWM 桌面組合還可讓所有主題的桌面電腦群組合、支援3D 立體視覺，以及管理、隔離和保護 Windows Store 應用程式的體驗。</span><span class="sxs-lookup"><span data-stu-id="0eaec-110">In addition to experiences enabled in Windows 7, now DWM desktop composition enables desktop composition for all themes, support for Stereoscopic 3D, and management, separation, and protection of the experience with Windows Store apps.</span></span>

<span data-ttu-id="0eaec-111">**所有主題的桌面組合**</span><span class="sxs-lookup"><span data-stu-id="0eaec-111">**Desktop composition for all themes**</span></span>

<span data-ttu-id="0eaec-112">在 Windows Vista 和 Windows 7 中，只會使用 AERO 半透明主題來啟用桌面組合。</span><span class="sxs-lookup"><span data-stu-id="0eaec-112">In Windows Vista and Windows 7, desktop composition is enabled only with the AERO Glass Theme.</span></span> <span data-ttu-id="0eaec-113">因此，Windows 傳統和高對比主題的使用者無法使用桌面組合啟用的體驗，例如 Windows Flip、高解析度的自動調整 (DPI) 調整、縮圖預覽和全螢幕放大鏡。</span><span class="sxs-lookup"><span data-stu-id="0eaec-113">Hence users of Windows Classic and high contrast themes cannot use experiences enabled by desktop composition such as Windows Flip, automatic scaling for high resolution (DPI) scaling, thumbnail Preview and full screen magnifier.</span></span> <span data-ttu-id="0eaec-114">此外，在這些舊版的 Windows 中，應用程式開發人員必須撰寫和維護多個程式碼路徑–一個是啟用桌面電腦群組合，另一個則停用桌面電腦群組合。</span><span class="sxs-lookup"><span data-stu-id="0eaec-114">In addition, in these earlier versions of Windows, app developers must write and maintain multiple code paths – one where desktop composition is enabled and another where desktop composition is disabled.</span></span>

<span data-ttu-id="0eaec-115">使用 Windows 8 時，會為所有主題啟用桌面電腦群組合。</span><span class="sxs-lookup"><span data-stu-id="0eaec-115">With Windows 8, desktop composition is enabled for all themes.</span></span> <span data-ttu-id="0eaec-116">Windows 傳統和高對比主題的使用者可以使用桌面電腦群組合啟用的體驗，例如 Windows Flip、高解析度的自動調整 (DPI) 調整、縮圖預覽，以及全螢幕放大鏡。</span><span class="sxs-lookup"><span data-stu-id="0eaec-116">Users of Windows Classic and high contrast themes can use the experiences enabled by desktop composition such as Windows Flip, automatic scaling for high resolution (DPI) scaling, thumbnail previews, and full screen magnifier.</span></span> <span data-ttu-id="0eaec-117">此外，開發人員不需要撰寫和維護多個程式碼路徑，進而簡化開發。</span><span class="sxs-lookup"><span data-stu-id="0eaec-117">In addition, developers don’t need to write and maintain multiple code paths, thereby simplifying development.</span></span>

<span data-ttu-id="0eaec-118">**支援 stereoscopic 3D**</span><span class="sxs-lookup"><span data-stu-id="0eaec-118">**Support for stereoscopic 3D**</span></span>

<span data-ttu-id="0eaec-119">DWM 桌面組合支援轉譯和呈現視窗化和全螢幕 stereoscopic 3D 應用程式內容。</span><span class="sxs-lookup"><span data-stu-id="0eaec-119">DWM desktop composition supports rendering and presentation of windowed and full-screen stereoscopic 3D app content.</span></span>

<span data-ttu-id="0eaec-120">**管理、隔離和保護 Windows Store 應用程式的體驗**</span><span class="sxs-lookup"><span data-stu-id="0eaec-120">**Management, separation and protection of the experience with Windows Store apps**</span></span>

<span data-ttu-id="0eaec-121">DWM 桌面電腦群組合可讓您從 Windows Store 應用程式視窗管理和分隔桌面應用程式視窗，以從新的 Windows Store 應用程式視窗區隔和保護傳統型應用程式視窗。</span><span class="sxs-lookup"><span data-stu-id="0eaec-121">DWM desktop composition enables separation and protection of desktop app windows from the new Windows Store app windows by managing and separating the desktop app windows from the Windows Store app windows.</span></span> <span data-ttu-id="0eaec-122">由於桌面電腦群組合負責管理所有的應用程式視窗，因此停用桌面組合可能會導致非預期的行為。</span><span class="sxs-lookup"><span data-stu-id="0eaec-122">Since desktop composition is responsible for managing all app windows, disabling desktop composition can result in unexpected behavior.</span></span> <span data-ttu-id="0eaec-123">此外，桌面電腦群組合負責撰寫新的 [開始] 功能表，以及構成新 Windows 作業系統核心特性的其他視窗動畫。</span><span class="sxs-lookup"><span data-stu-id="0eaec-123">In addition desktop composition is responsible for composing the new Start menu as well as additional window animations that form the core personality of the new Windows operating system.</span></span>

## <a name="controlling-desktop-composition"></a><span data-ttu-id="0eaec-124">控制桌面電腦群組合</span><span class="sxs-lookup"><span data-stu-id="0eaec-124">Controlling desktop composition</span></span>

<span data-ttu-id="0eaec-125">在 Windows Vista 和 Windows 7 中，桌面電腦群組合在許多案例中都已停用。</span><span class="sxs-lookup"><span data-stu-id="0eaec-125">In Windows Vista and Windows 7, desktop composition is disabled in a number of scenarios.</span></span> <span data-ttu-id="0eaec-126">在 Windows 8 中，DWM 桌面組合是核心作業系統元件，無法停用。</span><span class="sxs-lookup"><span data-stu-id="0eaec-126">In Windows 8, DWM desktop composition is a core operating system component and cannot be disabled.</span></span> <span data-ttu-id="0eaec-127">但有一些例外狀況，桌面電腦群組合永遠開啟;它會在使用者登入之前啟動，並在會話持續期間維持使用中狀態。</span><span class="sxs-lookup"><span data-stu-id="0eaec-127">With a few exceptions, desktop composition is always on; it’s started before the user logon and remains active for the duration of a session.</span></span> <span data-ttu-id="0eaec-128">本節說明 Windows 8 如何在 Windows 7 中停用桌面電腦群組合的案例。</span><span class="sxs-lookup"><span data-stu-id="0eaec-128">This section describes how Windows 8 treats the scenarios in Windows 7 where desktop composition is disabled.</span></span>

<span data-ttu-id="0eaec-129">**伺服器 SKU 和特定用戶端 Sku**</span><span class="sxs-lookup"><span data-stu-id="0eaec-129">**Server SKU and certain client SKUs**</span></span>

<span data-ttu-id="0eaec-130">在 Windows 8 中，所有伺服器和用戶端 Sku 都會啟用桌面組合。</span><span class="sxs-lookup"><span data-stu-id="0eaec-130">In Windows 8, all server and client SKUs have desktop composition enabled.</span></span> <span data-ttu-id="0eaec-131">這樣可確保伺服器管理員和使用者可以受益于桌面電腦群組合所啟用的體驗。</span><span class="sxs-lookup"><span data-stu-id="0eaec-131">This ensures that server admins and users can benefit from the experiences enabled by desktop composition.</span></span>

<span data-ttu-id="0eaec-132">**桌面撰寫的基本需求**</span><span class="sxs-lookup"><span data-stu-id="0eaec-132">**Fundamental requirements for desktop composition**</span></span>

<span data-ttu-id="0eaec-133">Windows 8 可透過 WDDM 驅動程式支援和系統色彩深度，確保符合圖形介面卡和系統色彩深度需求。</span><span class="sxs-lookup"><span data-stu-id="0eaec-133">Windows 8 ensures that graphics adapter and system color depth requirements are met through WDDM driver support and system color depth.</span></span>

<span data-ttu-id="0eaec-134">**WDDM 驅動程式支援**</span><span class="sxs-lookup"><span data-stu-id="0eaec-134">**WDDM driver support**</span></span>

<span data-ttu-id="0eaec-135">如果系統沒有符合 WDDM 規範的圖形驅動程式，Windows 8 會使用 Microsoft 基本顯示器介面卡作為預設介面卡。</span><span class="sxs-lookup"><span data-stu-id="0eaec-135">If a system does not have a WDDM-compliant graphics driver, Windows 8 uses Microsoft Basic Display Adapter as the default adapter.</span></span> <span data-ttu-id="0eaec-136">由於 DWM 一律會在預設介面卡上執行，因此當 WDDM 相容的圖形驅動程式無法使用時，它會選擇 [Microsoft 基本顯示器介面卡] 來撰寫桌面 (是否未在系統上安裝或停用) 。</span><span class="sxs-lookup"><span data-stu-id="0eaec-136">Since DWM always runs on the default adapter, it will choose Microsoft Basic Display Adapter to compose the desktop when a WDDM-compliant graphics driver is not available (whether not installed or disabled) on the system.</span></span>

<span data-ttu-id="0eaec-137">Microsoft 基本顯示器介面卡是使用 CPU 而不是 GPU 來執行所有繪圖的軟體轉譯器。</span><span class="sxs-lookup"><span data-stu-id="0eaec-137">Microsoft Basic Display Adapter is a software rasterizer that uses the CPU rather than the GPU to perform all the drawing.</span></span> <span data-ttu-id="0eaec-138">請注意，在 Microsoft 基本顯示器介面卡上的桌面組合效能 (特別是在 GPU 上執行桌面電腦群組合時的動畫) 可能不會像這樣。</span><span class="sxs-lookup"><span data-stu-id="0eaec-138">Note that the performance of desktop composition on Microsoft Basic Display Adapter (especially animations) may not be as smooth as when running desktop composition on a GPU.</span></span>

<span data-ttu-id="0eaec-139">**系統色彩深度**</span><span class="sxs-lookup"><span data-stu-id="0eaec-139">**System color depth**</span></span>

<span data-ttu-id="0eaec-140">除非色彩深度設定為每圖元32位，否則無法執行桌面電腦群組合。</span><span class="sxs-lookup"><span data-stu-id="0eaec-140">Desktop Composition cannot run unless the color depth is set to 32 bits per pixel.</span></span> <span data-ttu-id="0eaec-141">在 Windows 7 中，您可以在下列情況下變更系統的色彩深度：</span><span class="sxs-lookup"><span data-stu-id="0eaec-141">In Windows 7 the color depth of the system can be changed in these scenarios:</span></span>

-   <span data-ttu-id="0eaec-142">終端使用者使用 Windows 顯示控制台或協力廠商控制台來變更系統色彩</span><span class="sxs-lookup"><span data-stu-id="0eaec-142">An end user uses the Windows Display control panel or a 3rd party control panel to change the system color</span></span>
-   <span data-ttu-id="0eaec-143">終端使用者執行的應用程式會透過公用 API 變更系統的色彩深度</span><span class="sxs-lookup"><span data-stu-id="0eaec-143">An end user runs an app that changes the color depth of the system through a public API</span></span>

<span data-ttu-id="0eaec-144">不同于 Windows 7，Windows 8 不支援每圖元32位以外的色彩深度。</span><span class="sxs-lookup"><span data-stu-id="0eaec-144">Unlike Windows 7, Windows 8 does not support color depth other than 32 bits per pixel.</span></span> <span data-ttu-id="0eaec-145">使用者無法再使用 [控制台] 來變更系統的色彩深度。</span><span class="sxs-lookup"><span data-stu-id="0eaec-145">The user can no longer change the color depth of the system by using the control panel.</span></span>

<span data-ttu-id="0eaec-146">此外，應用程式開發人員無法使用 Api 來變更系統的色彩深度。</span><span class="sxs-lookup"><span data-stu-id="0eaec-146">In addition, app developers cannot use APIs to change the color depth of the system.</span></span> <span data-ttu-id="0eaec-147">Windows 8 將會偵測到嘗試將系統的色彩深度變更為每圖元32位的應用程式，並通知使用者必須套用應用程式相容性填充碼，才能執行應用程式。</span><span class="sxs-lookup"><span data-stu-id="0eaec-147">Windows 8 will detect apps that try to change the color depth of the system to less than 32 bits per pixel, and inform the user that an app compatibility shim must be applied to run the apps.</span></span> <span data-ttu-id="0eaec-148">從使用者確認之後，應用程式相容性填充碼會套用，而填充碼會將低色彩模式虛擬化到應用程式，同時讓系統以每圖元32位執行。</span><span class="sxs-lookup"><span data-stu-id="0eaec-148">After confirmation from the user, the app compatibility shim is applied and the shim virtualizes the low color mode to the app while keeping the system running at 32 bits per pixel.</span></span>

<span data-ttu-id="0eaec-149">**WinSAT**</span><span class="sxs-lookup"><span data-stu-id="0eaec-149">**WinSAT**</span></span>

<span data-ttu-id="0eaec-150">在 Windows 8 中，桌面電腦群組合不會相依于 WinSAT 分數。</span><span class="sxs-lookup"><span data-stu-id="0eaec-150">In Windows 8, desktop composition does not depend on WinSAT scores.</span></span> <span data-ttu-id="0eaec-151">此外，WinSAT 不再包含 DWM 評定。</span><span class="sxs-lookup"><span data-stu-id="0eaec-151">Moreover, WinSAT no longer includes DWM assessment.</span></span>

<span data-ttu-id="0eaec-152">**應用程式相容性與使用者動作**</span><span class="sxs-lookup"><span data-stu-id="0eaec-152">**App compatibility and user action**</span></span>

<span data-ttu-id="0eaec-153">在 Windows 8：</span><span class="sxs-lookup"><span data-stu-id="0eaec-153">In Windows 8:</span></span>

-   <span data-ttu-id="0eaec-154">移除存在於視窗7中的桌面撰寫的所有選項</span><span class="sxs-lookup"><span data-stu-id="0eaec-154">All of the options for disabling desktop composition that exist in Window 7 are removed</span></span>
-   <span data-ttu-id="0eaec-155">桌面電腦群組合負責撰寫所有主題</span><span class="sxs-lookup"><span data-stu-id="0eaec-155">Desktop composition is responsible for composing all themes</span></span>
-   <span data-ttu-id="0eaec-156">應用程式無法使用 DwmEnableComposition 來停用桌面組合。</span><span class="sxs-lookup"><span data-stu-id="0eaec-156">Apps cannot use DwmEnableComposition to disable desktop composition.</span></span> <span data-ttu-id="0eaec-157">為了維持回溯相容性，呼叫此 API 將會傳回成功;不過，桌面電腦群組合未停用</span><span class="sxs-lookup"><span data-stu-id="0eaec-157">In order to maintain backward compatibility, a call to this API will return success; however, desktop composition is not disabled</span></span>
-   <span data-ttu-id="0eaec-158">已移除「停用桌面撰寫」填充碼</span><span class="sxs-lookup"><span data-stu-id="0eaec-158">The "Disable desktop composition" shim is removed</span></span>
-   <span data-ttu-id="0eaec-159">移除 [應用程式屬性] 對話方塊的 [相容性] 索引標籤中的 [停用桌面組合] 選項</span><span class="sxs-lookup"><span data-stu-id="0eaec-159">The option to "Disable desktop composition" from the compatibility tab of the Application Properties dialogue box is removed</span></span>

<span data-ttu-id="0eaec-160">**應用程式會使用鏡像驅動程式進行遠端處理**</span><span class="sxs-lookup"><span data-stu-id="0eaec-160">**An app uses a mirroring driver for remoting**</span></span>

<span data-ttu-id="0eaec-161">在 Windows 8：</span><span class="sxs-lookup"><span data-stu-id="0eaec-161">In Windows 8:</span></span>

-   <span data-ttu-id="0eaec-162">不支援遠端處理案例的鏡像驅動程式;雖然大部分使用鏡像驅動程式的現有應用程式都應該繼續運作，因為支援基礎結構 Windows 8 中的現有鏡像驅動程式所需的變更，也就是使用鏡像驅動程式的部分功能或應用程式可能無法運作</span><span class="sxs-lookup"><span data-stu-id="0eaec-162">Does not support mirror drivers for remoting scenarios; while most of the existing apps that use mirror drivers should continue to work, due to the infrastructural change required to support existing mirror drivers in Windows 8 with DWM ON, some features or apps that use mirror drivers may not work</span></span>
-   <span data-ttu-id="0eaec-163">針對使用鏡像驅動程式進行遠端處理案例的應用程式開發人員，支援桌面複製 Api。</span><span class="sxs-lookup"><span data-stu-id="0eaec-163">Does support Desktop Duplication APIs for app developers who use mirror drivers for remoting scenarios.</span></span>
-   <span data-ttu-id="0eaec-164">不支援現有的協助工具鏡像驅動程式</span><span class="sxs-lookup"><span data-stu-id="0eaec-164">Does not support existing Accessibility Mirror Drivers</span></span>
-   <span data-ttu-id="0eaec-165">現有鏡像驅動程式必須更新，以確保它們與 Windows 8 相容</span><span class="sxs-lookup"><span data-stu-id="0eaec-165">Existing Mirror Drivers must be updated to ensure that they are compatible with Windows 8</span></span>

<span data-ttu-id="0eaec-166">**遠端桌面連線**</span><span class="sxs-lookup"><span data-stu-id="0eaec-166">**Remote desktop connection**</span></span>

<span data-ttu-id="0eaec-167">在 Windows 8 中，一律會啟用遠端桌面連線的桌面組合。</span><span class="sxs-lookup"><span data-stu-id="0eaec-167">In Windows 8, desktop composition is always enabled for a remote desktop connection.</span></span> <span data-ttu-id="0eaec-168">連接到 Windows 8 遠端電腦的用戶端電腦一律會啟用遠端桌面會話的桌面電腦群組合，而不考慮 Windows 用戶端版本。</span><span class="sxs-lookup"><span data-stu-id="0eaec-168">A client computer connecting to a Windows 8 remote computer will always get desktop composition enabled for the remote desktop session irrespective of the Windows client version.</span></span> <span data-ttu-id="0eaec-169">用戶端電腦上的多個監視器以及遠端應用程式會話都支援桌面電腦群組合。</span><span class="sxs-lookup"><span data-stu-id="0eaec-169">Desktop composition is supported for multiple monitors on the client machine as well as for the remote app session.</span></span>

<span data-ttu-id="0eaec-170">此外，連接到 Windows 8 遠端電腦時，遠端桌面連線用戶端中的這些設定將不會生效：</span><span class="sxs-lookup"><span data-stu-id="0eaec-170">In addition, when connecting to a Windows 8 remote computer, these settings in the Remote Desktop Connection client do not take effect:</span></span>

-   <span data-ttu-id="0eaec-171">色彩深度</span><span class="sxs-lookup"><span data-stu-id="0eaec-171">Color depth</span></span>
-   <span data-ttu-id="0eaec-172">[啟用組合] 核取方塊</span><span class="sxs-lookup"><span data-stu-id="0eaec-172">"Enable composition” checkbox</span></span>

<span data-ttu-id="0eaec-173">連接的色彩深度一律設定為每圖元32位，且桌面組合一律為啟用狀態。</span><span class="sxs-lookup"><span data-stu-id="0eaec-173">The color depth of the connection is always set to 32 bits per pixel and desktop composition is always enabled.</span></span>

 

 




