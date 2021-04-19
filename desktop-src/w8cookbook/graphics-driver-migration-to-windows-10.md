---
title: 將圖形驅動程式遷移至 Windows 10
description: Windows 10 媒體和 Windows 10 （例如其前身 Windows 8.1）在 Windows Media 套件或「In Box」中沒有任何協力廠商圖形驅動程式。
ms.assetid: E6240CF0-5A65-4A66-98AE-856C783EB320
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a23d8ae341172223955fcc781f95b7615bcfc867
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106969064"
---
# <a name="graphics-driver-migration-to-windows-10"></a><span data-ttu-id="0fcec-103">將圖形驅動程式遷移至 Windows 10</span><span class="sxs-lookup"><span data-stu-id="0fcec-103">Graphics driver migration to Windows 10</span></span>

<span data-ttu-id="0fcec-104">Windows 10 媒體和 Windows 10 （例如其前身 Windows 8.1）在 Windows Media 套件或「In Box」中沒有任何協力廠商圖形驅動程式。</span><span class="sxs-lookup"><span data-stu-id="0fcec-104">Windows 10 Media and Windows 10, like its predecessor, Windows 8.1, does not have any 3rd party graphics drivers in the Windows media kit or “In Box”.</span></span> <span data-ttu-id="0fcec-105">相反地，系統會在 WU 上布建各式各樣裝置的圖形驅動程式，讓硬體廠商可以更新驅動程式，而不需要變更作業系統映射。</span><span class="sxs-lookup"><span data-stu-id="0fcec-105">Instead, the graphics drivers for a broad range of devices are provisioned on WU, which allows hardware vendors to update drivers without requiring a change to the operating system image.</span></span> <span data-ttu-id="0fcec-106">此外，在 OS 升級期間，不會將現有的驅動程式遷移至 Windows 10 Windows 10 從 Windows 7、Windows 8 或 Windows 8.1。</span><span class="sxs-lookup"><span data-stu-id="0fcec-106">Also, existing drivers are not migrated to Windows 10 during an OS upgrade to Windows 10 from Windows 7, Windows 8 or Windows 8.1.</span></span> <span data-ttu-id="0fcec-107">這也會影響 Windows Server 2012 的升級。</span><span class="sxs-lookup"><span data-stu-id="0fcec-107">This also impacts upgrades from Windows Server 2012.</span></span>

## <a name="upgrades-and-installation"></a><span data-ttu-id="0fcec-108">升級與安裝</span><span class="sxs-lookup"><span data-stu-id="0fcec-108">Upgrades and installation</span></span>

<span data-ttu-id="0fcec-109">針對升級和新的安裝，您必須從 Windows Update (WU) 或相關硬體的 IHV/OEM 網站取得圖形驅動程式。</span><span class="sxs-lookup"><span data-stu-id="0fcec-109">For upgrades and new installations, the graphics drivers must be obtained from Windows Update (WU) or the IHV/OEM web site for the relevant hardware.</span></span> <span data-ttu-id="0fcec-110">這需要網際網路連線。</span><span class="sxs-lookup"><span data-stu-id="0fcec-110">This requires an Internet connection.</span></span> <span data-ttu-id="0fcec-111">WU 上的驅動程式會在使用者將其 Windows 7 或 Windows 8 x 系統升級至 Windows 10 時，由動態更新 (DU) 插入 OS 設定中。</span><span class="sxs-lookup"><span data-stu-id="0fcec-111">The drivers on WU are injected into the OS setup by Dynamic Update (DU) when a user upgrades their Windows 7 or Windows 8.x system to Windows 10.</span></span>

> [!Note]  
> <span data-ttu-id="0fcec-112">這並不適用于已預先安裝 Windows 的系統，例如在零售商店購買的現成電腦。</span><span class="sxs-lookup"><span data-stu-id="0fcec-112">This does not apply to systems which come with Windows pre-installed, e.g. off-the-shelf computers purchased in a retail store.</span></span> <span data-ttu-id="0fcec-113">這些系統已經有 OEM 所安裝的圖形驅動程式。</span><span class="sxs-lookup"><span data-stu-id="0fcec-113">These systems already have the graphics drivers installed by the OEM.</span></span> <span data-ttu-id="0fcec-114">OEM 也可以提供 DVD (，以重新安裝包含驅動程式的 OS) 。</span><span class="sxs-lookup"><span data-stu-id="0fcec-114">The OEM might also supply a DVD (for re-installing the OS) which includes the drivers.</span></span>

 

<span data-ttu-id="0fcec-115">升級至 Windows 10 之後，使用者可能會發現電腦上沒有安裝圖形驅動程式。</span><span class="sxs-lookup"><span data-stu-id="0fcec-115">After upgrading to Windows 10, users might find that there are no graphics drivers installed on their PC.</span></span> <span data-ttu-id="0fcec-116">發生此狀況的幾個可能原因：</span><span class="sxs-lookup"><span data-stu-id="0fcec-116">This can happen for a few reasons:</span></span>

-   <span data-ttu-id="0fcec-117">使用者選擇進行全新安裝，亦即不是升級。</span><span class="sxs-lookup"><span data-stu-id="0fcec-117">The user elected to do a clean install, i.e. not an upgrade.</span></span>
-   <span data-ttu-id="0fcec-118">使用者取消選取了在升級期間檢查更新的選項，亦即，有效停用動態更新 (DU) 。</span><span class="sxs-lookup"><span data-stu-id="0fcec-118">The user de-selected the option to check for updates during the upgrade, i.e. effectively disabled Dynamic Update (DU).</span></span>
-   <span data-ttu-id="0fcec-119">網際網路連線在升級期間無法運作。</span><span class="sxs-lookup"><span data-stu-id="0fcec-119">The Internet connection was not working during the upgrade.</span></span>
-   <span data-ttu-id="0fcec-120">驅動程式安裝失敗。</span><span class="sxs-lookup"><span data-stu-id="0fcec-120">The driver installation failed.</span></span>

<span data-ttu-id="0fcec-121">在全新安裝作業系統之後，電腦上就不會有任何圖形驅動程式，因為 WU 用戶端會自動執行並下載適用的驅動程式。</span><span class="sxs-lookup"><span data-stu-id="0fcec-121">After a clean install of the OS, there will not be any graphics drivers on the PC until the WU client runs automatically and downloads the applicable drivers.</span></span> <span data-ttu-id="0fcec-122">在過渡期間，電腦會執行 Microsoft 基本顯示器介面卡 (MSBDA) ，它的功能有限，例如不支援多個監視器，而且使用者可能會因為硬體驅動程式而發生效能不佳的情況，例如畫面播放速率變慢或影片播放上的撕裂。</span><span class="sxs-lookup"><span data-stu-id="0fcec-122">In the interim the PC will be running the Microsoft Basic Display Adapter (MSBDA), which has limited capabilities, e.g. no support for multiple monitors, and the user might also experience poor performance compared to a hardware driver, e.g. slow frame rate or tearing on video playback.</span></span>

## <a name="manifestations"></a><span data-ttu-id="0fcec-123">表現</span><span class="sxs-lookup"><span data-stu-id="0fcec-123">Manifestations</span></span>

<span data-ttu-id="0fcec-124">針對較舊的電腦 (通常是在 Windows 7) 之前建立的，在 WU 上可能沒有任何驅動程式可 Windows 10 供使用，因為圖形介面卡已達生命週期結束 (EOL) ，且硬體廠商已不再支援。</span><span class="sxs-lookup"><span data-stu-id="0fcec-124">For older PCs (typically built prior to Windows 7), it is possible that there are no drivers for Windows 10 on WU because the graphics adapters have reached End-Of-Life (EOL) and are no longer supported by the hardware vendors.</span></span> <span data-ttu-id="0fcec-125">即使是目前執行 Windows 7 或8.x 的系統，也可能已從先前的 OS 升級，而且可能具有 EOL 圖形介面卡。</span><span class="sxs-lookup"><span data-stu-id="0fcec-125">Even systems currently running Windows 7 or 8.x might have been upgraded from a previous OS and could have EOL graphics adapters.</span></span>

<span data-ttu-id="0fcec-126">較新的電腦可能沒有可用的驅動程式，因為圖形配接器是從較舊的電腦（例如硬體升級期間）傳輸。</span><span class="sxs-lookup"><span data-stu-id="0fcec-126">Newer PCs might not have drivers available because the graphics adapter was transferred from an older computer, e.g. during a hardware upgrade.</span></span> <span data-ttu-id="0fcec-127">如果電腦具有多個圖形介面卡，而使用者在購買新的電腦時仍會保留舊的圖形配接器來使用多個顯示器，通常會發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="0fcec-127">This most often happens for computers with multiple graphics adapters where the user kept an old graphics card when purchasing a new machine in order to use multiple displays.</span></span>

<span data-ttu-id="0fcec-128">一小部分的電腦有另一個可能性，那就是 Windows Update 只有「涵蓋範圍」的驅動程式。</span><span class="sxs-lookup"><span data-stu-id="0fcec-128">Another possibility for a small percentage of machines is that Windows Update only has “coverage” drivers.</span></span> <span data-ttu-id="0fcec-129">這些是缺少 OEM 自訂的一般驅動程式。</span><span class="sxs-lookup"><span data-stu-id="0fcec-129">These are generic drivers that lack OEM customizations.</span></span> <span data-ttu-id="0fcec-130">在升級至 Windows 10 之後，傳遞其中一個驅動程式的使用者可能會發現某些功能已遺失，例如控制螢幕亮度的函式按鍵將不再運作。</span><span class="sxs-lookup"><span data-stu-id="0fcec-130">A user who is delivered one of these drivers after upgrading to Windows 10 might see that some functionality is missing, e.g. function keys for controlling screen brightness no longer work.</span></span>

## <a name="mitigations"></a><span data-ttu-id="0fcec-131">風險降低</span><span class="sxs-lookup"><span data-stu-id="0fcec-131">Mitigations</span></span>

-   <span data-ttu-id="0fcec-132">在升級程式期間，您應該將適當的圖形驅動程式傳遞給 DU，或在升級完成後立即以 WU 傳遞。</span><span class="sxs-lookup"><span data-stu-id="0fcec-132">Suitable graphics drivers should be delivered either by DU during the upgrade process or by WU soon after the upgrade completes.</span></span> <span data-ttu-id="0fcec-133">Oem 必須確保系統映射中包含適當的圖形驅動程式，以便在其電腦上安裝 Windows 10 的出廠預設值。</span><span class="sxs-lookup"><span data-stu-id="0fcec-133">OEMs must ensure that the appropriate graphics drivers are included in the system images used for factory installation of Windows 10 on their computers.</span></span>
-   <span data-ttu-id="0fcec-134">升級之後，使用者可以明確檢查 \\ 驅動程式的設定 Windows Update 但這不是必要的。</span><span class="sxs-lookup"><span data-stu-id="0fcec-134">After an upgrade, the user can explicitly check Settings \\ Windows Update for drivers although this should not be necessary.</span></span> <span data-ttu-id="0fcec-135">在驅動程式中自動安裝驅動程式時強制執行檢查的使用者，如果自動安裝先完成，可能會看到驅動程式安裝失敗。</span><span class="sxs-lookup"><span data-stu-id="0fcec-135">Users who force a check while a driver is being automatically installed in the background might see a driver installation failure if the automatic installation completes first.</span></span> <span data-ttu-id="0fcec-136">請不用理會這一則訊息。</span><span class="sxs-lookup"><span data-stu-id="0fcec-136">This can be ignored.</span></span>
-   <span data-ttu-id="0fcec-137">打算進行 Windows 10 全新安裝的使用者應該先取得相關的驅動程式，然後再安裝或依賴 Windows Update 來提供驅動程式，在這種情況下，他們必須確保其網際網路連線正常運作。</span><span class="sxs-lookup"><span data-stu-id="0fcec-137">Users who intend to do a clean install of Windows 10 should obtain the relevant drivers before installing or rely on Windows Update to supply the drivers later, in which case they must ensure that their Internet connection is working.</span></span>
-   <span data-ttu-id="0fcec-138">針對接收涵蓋範圍驅動程式的電腦，不會緩和遺失的功能。</span><span class="sxs-lookup"><span data-stu-id="0fcec-138">For computers that receive a coverage driver there is no mitigation for missing functionality.</span></span> <span data-ttu-id="0fcec-139">不過，只有在硬體供應商不再維護驅動程式的情況下（也就是數歲的電腦）才會發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="0fcec-139">However, this should only happen in cases where the hardware supplier no longer maintains the drivers, i.e. computers that are several years old.</span></span>

> [!Note]  
> <span data-ttu-id="0fcec-140">針對具有單一顯示器的系統（例如膝上型電腦），許多使用者發現 MSBDA 是可接受的，且不會注意到缺乏硬體驅動程式。</span><span class="sxs-lookup"><span data-stu-id="0fcec-140">For systems with a single display, e.g. a laptop, many users find that MSBDA is acceptable and do not notice the lack of a hardware driver.</span></span> <span data-ttu-id="0fcec-141">在此情況下，不需要緩和措施。</span><span class="sxs-lookup"><span data-stu-id="0fcec-141">No mitigation is required in this case.</span></span>

 

## <a name="solutions"></a><span data-ttu-id="0fcec-142">方案</span><span class="sxs-lookup"><span data-stu-id="0fcec-142">Solutions</span></span>

<span data-ttu-id="0fcec-143">Ihv 和 Oem 將其 Windows 10 graphics 驅動程式上傳至適用于任何想要支援之硬體的 WU 是很重要的。</span><span class="sxs-lookup"><span data-stu-id="0fcec-143">It is critical that IHVs and OEMs upload their Windows 10 graphics drivers to WU for any hardware that they intend to support.</span></span>

<span data-ttu-id="0fcec-144">升級時，使用者應該保留選取 [檢查更新] (預設設定) 。</span><span class="sxs-lookup"><span data-stu-id="0fcec-144">Users should leave “Check for Updates” selected (the default setting) when upgrading.</span></span> <span data-ttu-id="0fcec-145">根據網路連線的速度以及 WU 伺服器上的負載，這可能表示在 OOBE 完成且使用者第一次登入之前，驅動程式不會安裝。</span><span class="sxs-lookup"><span data-stu-id="0fcec-145">Depending on the speed of the network connection and the load on the WU servers, this can mean that the drivers do not get installed until after OOBE has completed and the user has logged in for the first time.</span></span> <span data-ttu-id="0fcec-146">在此同時，使用者可能會注意到某些有限的功能或效能不佳。</span><span class="sxs-lookup"><span data-stu-id="0fcec-146">In the meantime, the user might notice some limited functionality or poor performance.</span></span>

<span data-ttu-id="0fcec-147">使用者必須確保其網際網路連線在啟動升級之前都正常運作，即使它們是使用 media (DVD 或快閃磁片磁碟機) 進行升級。</span><span class="sxs-lookup"><span data-stu-id="0fcec-147">Users must ensure that their Internet connection is working before starting an upgrade even if they are upgrading using media (DVD or Flash Drive).</span></span>

-   <span data-ttu-id="0fcec-148">如果電腦已連線到網際網路，應該會自動下載並安裝適當的驅動程式。</span><span class="sxs-lookup"><span data-stu-id="0fcec-148">If the PC is connected to the Internet, the appropriate drivers should be downloaded and installed automatically.</span></span> <span data-ttu-id="0fcec-149">使用者不需要採取任何動作。</span><span class="sxs-lookup"><span data-stu-id="0fcec-149">The user is not required to take any action.</span></span>
-   <span data-ttu-id="0fcec-150">如果電腦未連線到網際網路，則必須使用已連線到網際網路的電腦，從 IHV 或 OEM 網站下載驅動程式;使用快閃磁片磁碟機或 CD/DVD 傳送至目的電腦;然後手動安裝。</span><span class="sxs-lookup"><span data-stu-id="0fcec-150">If the PC is not connected to the Internet, the drivers must be downloaded from the IHV or OEM web site using an Internet-connected computer; transferred to the target machine using a Flash Drive or CD/DVD; and then installed manually.</span></span>

 

 




