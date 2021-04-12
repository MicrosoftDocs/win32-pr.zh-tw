---
title: 還原點
description: 系統會建立還原點，以允許使用者選擇先前的系統狀態。 每個還原點都包含將系統還原至所選狀態所需的必要資訊。 還原點會在對系統進行金鑰變更之前建立。
ms.assetid: 5f68b377-4293-493e-afaf-f4414c2af1fb
author: Teresa-Motiv
ms.author: v-tea
ms.topic: article
ms.date: 12/06/2019
manager: dcscontentpm
ms.custom: CSSTroubleshooting
ms.openlocfilehash: 6ef1aba7d1cb018bb3fa4f32d868828ef2ac4d1b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316093"
---
# <a name="restore-points"></a><span data-ttu-id="78f0d-105">還原點</span><span class="sxs-lookup"><span data-stu-id="78f0d-105">Restore points</span></span>

<span data-ttu-id="78f0d-106">系統會建立還原點，讓使用者選取先前的系統狀態。</span><span class="sxs-lookup"><span data-stu-id="78f0d-106">Restore points are created to let users select a previous system state.</span></span> <span data-ttu-id="78f0d-107">每個還原點都包含將系統還原至所選狀態所需的資訊。</span><span class="sxs-lookup"><span data-stu-id="78f0d-107">Each restore point contains the required information to restore the system to the selected state.</span></span> <span data-ttu-id="78f0d-108">還原點會在對系統進行金鑰變更之前建立。</span><span class="sxs-lookup"><span data-stu-id="78f0d-108">Restore points are created before key changes are made to the system.</span></span>

<span data-ttu-id="78f0d-109">系統還原會自動管理配置給還原點的磁碟空間。</span><span class="sxs-lookup"><span data-stu-id="78f0d-109">System Restore automatically manages the disk space that is allocated for restore points.</span></span> <span data-ttu-id="78f0d-110">它會清除最舊的還原點，以騰出空間給新的還原點。</span><span class="sxs-lookup"><span data-stu-id="78f0d-110">It purges the oldest restore points to make room for new ones.</span></span> <span data-ttu-id="78f0d-111">系統還原會根據硬碟的大小和電腦執行的 Windows 版本配置空間，如下表所示。</span><span class="sxs-lookup"><span data-stu-id="78f0d-111">System Restore allocates space based on the size of the hard disk and the version of Windows that the computer runs, as shown in the following table.</span></span>

|<span data-ttu-id="78f0d-112">Windows 版本</span><span class="sxs-lookup"><span data-stu-id="78f0d-112">Windows version</span></span> |<span data-ttu-id="78f0d-113">硬碟 &nbsp; 大小</span><span class="sxs-lookup"><span data-stu-id="78f0d-113">Hard&nbsp;disk size</span></span> |<span data-ttu-id="78f0d-114">系統還原空間</span><span class="sxs-lookup"><span data-stu-id="78f0d-114">System Restore space</span></span> |
| --- | --- | --- |
|<span data-ttu-id="78f0d-115">Windows 7 和更新版本</span><span class="sxs-lookup"><span data-stu-id="78f0d-115">Windows 7 and later versions</span></span> | <span data-ttu-id="78f0d-116">> 64 GB</span><span class="sxs-lookup"><span data-stu-id="78f0d-116">> 64 GB</span></span> |<span data-ttu-id="78f0d-117">最多五% 的總磁碟空間，最大值為 10 GB，以較少者為准</span><span class="sxs-lookup"><span data-stu-id="78f0d-117">Up to five percent of total disk space or a maximum of 10 GB, whichever is less</span></span> |
|  | <span data-ttu-id="78f0d-118">&le; 64 GB</span><span class="sxs-lookup"><span data-stu-id="78f0d-118">&le; 64 GB</span></span> |<span data-ttu-id="78f0d-119">最多三% 的總磁碟空間</span><span class="sxs-lookup"><span data-stu-id="78f0d-119">Up to three percent of total disk space</span></span> |
|<span data-ttu-id="78f0d-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="78f0d-120">Windows Vista</span></span> |  |<span data-ttu-id="78f0d-121">最多15% 的總磁碟空間，或最多30% 的可用磁碟空間，以較少者為准</span><span class="sxs-lookup"><span data-stu-id="78f0d-121">Up to 15 percent of the total disk space or a maximum of 30 percent of available disk space, whichever is less</span></span> |
|<span data-ttu-id="78f0d-122">Windows XP</span><span class="sxs-lookup"><span data-stu-id="78f0d-122">Windows XP</span></span> | <span data-ttu-id="78f0d-123">>4 GB</span><span class="sxs-lookup"><span data-stu-id="78f0d-123">>4 GB</span></span> |<span data-ttu-id="78f0d-124">最多12% 的總磁碟空間</span><span class="sxs-lookup"><span data-stu-id="78f0d-124">Up to 12 percent of total disk space</span></span><br /><br /><span data-ttu-id="78f0d-125">若要變更 Windows XP 中的最大儲存空間限制，請使用主控台中的 [ **系統** ] 專案。</span><span class="sxs-lookup"><span data-stu-id="78f0d-125">To change the maximum storage limit in Windows XP, use the **System** item in Control Panel.</span></span> |
|  | <span data-ttu-id="78f0d-126">\< 4 GB</span><span class="sxs-lookup"><span data-stu-id="78f0d-126">\< 4 GB</span></span> |<span data-ttu-id="78f0d-127">最高 400 MB</span><span class="sxs-lookup"><span data-stu-id="78f0d-127">Up to 400 MB</span></span> |

## <a name="event-triggered-restore-points"></a><span data-ttu-id="78f0d-128">事件觸發的還原點</span><span class="sxs-lookup"><span data-stu-id="78f0d-128">Event-triggered restore points</span></span>

<span data-ttu-id="78f0d-129">系統還原會在發生下列任何事件之前自動建立還原點：</span><span class="sxs-lookup"><span data-stu-id="78f0d-129">System Restore automatically creates a restore point before any of the following events occur:</span></span>

- <span data-ttu-id="78f0d-130">**應用程式安裝** (只適用于使用系統還原相容安裝程式) 的應用程式。</span><span class="sxs-lookup"><span data-stu-id="78f0d-130">**Application installation** (applies only to applications that use a System Restore-compliant installer).</span></span> <span data-ttu-id="78f0d-131">如果應用程式安裝造成系統問題，使用者可以將系統還原到安裝之前的狀態。</span><span class="sxs-lookup"><span data-stu-id="78f0d-131">If the application installation causes system problems, the user can restore the system to a state that precedes the installation.</span></span>
- <span data-ttu-id="78f0d-132">**Windows Update 或自動更新安裝**。</span><span class="sxs-lookup"><span data-stu-id="78f0d-132">**Windows Update or AutoUpdate installation**.</span></span> <span data-ttu-id="78f0d-133">Windows Update (之前稱為「自動更新」) 會自動下載並安裝 Windows 更新。</span><span class="sxs-lookup"><span data-stu-id="78f0d-133">Windows Update (previously known as AutoUpdate) automatically downloads and installs Windows updates.</span></span> <span data-ttu-id="78f0d-134">此外，它還提供簡單的方式讓使用者手動下載及安裝更新。</span><span class="sxs-lookup"><span data-stu-id="78f0d-134">Additionally, it provides an easy way for users to manually download and install updates.</span></span> <span data-ttu-id="78f0d-135">系統還原會在安裝更新之前（不論是自動或手動）建立還原點。</span><span class="sxs-lookup"><span data-stu-id="78f0d-135">System Restore creates a restore point before an update is installed, whether automatically or manually.</span></span>
- <span data-ttu-id="78f0d-136">**系統還原** 作業。</span><span class="sxs-lookup"><span data-stu-id="78f0d-136">**System restore operation**.</span></span> <span data-ttu-id="78f0d-137">系統還原會在啟動任何還原作業之前，自動建立還原點做為備份。</span><span class="sxs-lookup"><span data-stu-id="78f0d-137">System Restore automatically creates a restore point as a backup before any restore operation starts.</span></span> <span data-ttu-id="78f0d-138">例如，假設使用者不小心將 Windows 還原為不正確的還原點。</span><span class="sxs-lookup"><span data-stu-id="78f0d-138">For example, assume that a user accidentally restores Windows to an incorrect restore point.</span></span> <span data-ttu-id="78f0d-139">若要復原該還原，使用者可以將視窗還原至第一個還原點之前的還原點。</span><span class="sxs-lookup"><span data-stu-id="78f0d-139">To undo that restoration, the user can restore Windows to a restore point that is previous to the first restore point.</span></span> <span data-ttu-id="78f0d-140">當 Windows 還原為初始狀態之後，使用者就可以重複此程式，這次請選取正確的還原點。</span><span class="sxs-lookup"><span data-stu-id="78f0d-140">After Windows has been restored to its initial state, the user can repeat the process, this time selecting the correct restore point.</span></span>

## <a name="scheduled-restore-points"></a><span data-ttu-id="78f0d-141">排程的還原點</span><span class="sxs-lookup"><span data-stu-id="78f0d-141">Scheduled restore points</span></span>

<span data-ttu-id="78f0d-142">使用者可以設定系統還原，以定期間隔建立還原點。</span><span class="sxs-lookup"><span data-stu-id="78f0d-142">Users can configure System Restore to create restore points at regular intervals.</span></span> <span data-ttu-id="78f0d-143">使用者也可以隨時從系統還原的使用者介面中，手動建立並命名還原點。</span><span class="sxs-lookup"><span data-stu-id="78f0d-143">Users can also manually create and name a restore point at any time from within the System Restore user interface.</span></span> <span data-ttu-id="78f0d-144">這些還原點會儲存並壓縮，並且可在還原點清單中使用。</span><span class="sxs-lookup"><span data-stu-id="78f0d-144">These restore points are saved and compressed, and are available in the list of restore points.</span></span>

<span data-ttu-id="78f0d-145">在 Windows 7 和更新版本中，只有在前七天沒有建立任何其他還原點時，系統還原才會建立排定的還原點。</span><span class="sxs-lookup"><span data-stu-id="78f0d-145">In Windows 7 and later versions, System Restore creates a scheduled restore point only if no other restore points have been created in the previous seven days.</span></span> <span data-ttu-id="78f0d-146">在 Windows Vista 中，如果當天沒有建立其他還原點，系統還原會每24小時建立一個檢查點。</span><span class="sxs-lookup"><span data-stu-id="78f0d-146">In Windows Vista, System Restore creates a checkpoint every 24 hours if no other restore points were created on that day.</span></span> <span data-ttu-id="78f0d-147">在 Windows XP 中，系統還原每24小時會建立一個檢查點，而不考慮其他作業。</span><span class="sxs-lookup"><span data-stu-id="78f0d-147">In Windows XP, System Restore creates a checkpoint every 24 hours, regardless of other operations.</span></span>

## <a name="known-issue-you-cannot-restore-the-system-to-a-restore-point-after-you-install-a-windows-10-update"></a><span data-ttu-id="78f0d-148">已知問題：安裝 Windows 10 更新之後，您無法將系統還原到還原點</span><span class="sxs-lookup"><span data-stu-id="78f0d-148">Known issue: You cannot restore the system to a restore point after you install a Windows 10 update</span></span>

<span data-ttu-id="78f0d-149">考慮下列案例：</span><span class="sxs-lookup"><span data-stu-id="78f0d-149">Consider the following scenario:</span></span>

1. <span data-ttu-id="78f0d-150">您可以在乾淨的電腦上安裝 Windows 10。</span><span class="sxs-lookup"><span data-stu-id="78f0d-150">You install Windows 10 on a clean computer.</span></span>
1. <span data-ttu-id="78f0d-151">您會開啟 [系統保護]，然後建立名為 "R1" 的系統還原點。</span><span class="sxs-lookup"><span data-stu-id="78f0d-151">You turn on system protection, and then create a system restore point that is named "R1."</span></span>
1. <span data-ttu-id="78f0d-152">您可以安裝一或多個 Windows 10 更新。</span><span class="sxs-lookup"><span data-stu-id="78f0d-152">You install one or more Windows 10 updates.</span></span>
1. <span data-ttu-id="78f0d-153">在更新完成安裝之後，您會將系統還原至「R1」還原點。</span><span class="sxs-lookup"><span data-stu-id="78f0d-153">After the updates finish installing, you restore the system to the "R1" restore point.</span></span>

<span data-ttu-id="78f0d-154">在此案例中，系統不會還原至「R1」還原點。</span><span class="sxs-lookup"><span data-stu-id="78f0d-154">In this scenario, the system is not restored to the "R1" restore point.</span></span> <span data-ttu-id="78f0d-155">相反地，電腦會發生停止錯誤 (0xc000021a) 。</span><span class="sxs-lookup"><span data-stu-id="78f0d-155">Instead, the computer experiences a Stop error (0xc000021a).</span></span> <span data-ttu-id="78f0d-156">您重新開機電腦，但系統無法返回 Windows 桌面。</span><span class="sxs-lookup"><span data-stu-id="78f0d-156">You restart the computer, but the system cannot return to the Windows desktop.</span></span>

### <a name="cause"></a><span data-ttu-id="78f0d-157">原因</span><span class="sxs-lookup"><span data-stu-id="78f0d-157">Cause</span></span>

<span data-ttu-id="78f0d-158">這是 Windows 10 的已知問題。</span><span class="sxs-lookup"><span data-stu-id="78f0d-158">This is a known issue in Windows 10.</span></span>

<span data-ttu-id="78f0d-159">在系統還原過程中，Windows 會暫時暫存正在使用中的檔案還原。</span><span class="sxs-lookup"><span data-stu-id="78f0d-159">During the system restore process, Windows temporarily stages the restoration of files that are in use.</span></span> <span data-ttu-id="78f0d-160">然後，它會將資訊儲存在登錄中。</span><span class="sxs-lookup"><span data-stu-id="78f0d-160">It then saves the information in the registry.</span></span> <span data-ttu-id="78f0d-161">當電腦重新開機時，它會完成暫存的操作。</span><span class="sxs-lookup"><span data-stu-id="78f0d-161">When the computer restarts, it completes the staged operation.</span></span>

<span data-ttu-id="78f0d-162">在此情況下，Windows 會在電腦重新開機時還原類別目錄檔案，以及將驅動程式 ( sys) 檔案的階段。</span><span class="sxs-lookup"><span data-stu-id="78f0d-162">In this situation, Windows restores the catalog files and stages the driver (.sys) files to be restored when the computer restarts.</span></span> <span data-ttu-id="78f0d-163">但是，當電腦重新開機時，Windows 會先載入現有的驅動程式，然後再還原較新版的驅動程式。</span><span class="sxs-lookup"><span data-stu-id="78f0d-163">However, when the computer restarts, Windows loads the existing drivers before it restores the later versions of the drivers.</span></span> <span data-ttu-id="78f0d-164">因為驅動程式版本不符合已還原類別目錄檔案的版本，所以會停止重新開機進程。</span><span class="sxs-lookup"><span data-stu-id="78f0d-164">Because the driver versions do not match the versions of the restored catalog files, the restart process stops.</span></span>

### <a name="workaround"></a><span data-ttu-id="78f0d-165">因應措施</span><span class="sxs-lookup"><span data-stu-id="78f0d-165">Workaround</span></span>

<span data-ttu-id="78f0d-166">**從失敗的重新開機復原並繼續還原程式**</span><span class="sxs-lookup"><span data-stu-id="78f0d-166">**To recover from the failed restart and continue the restore process**</span></span>

<span data-ttu-id="78f0d-167">發生失敗後，請重新開機電腦，直到進入 Windows 修復環境 (WinRE) 。</span><span class="sxs-lookup"><span data-stu-id="78f0d-167">After the failure occurs, restart the computer until it enters the Windows Recovery Environment (WinRE).</span></span> <span data-ttu-id="78f0d-168">若要這樣做，您可能必須使用硬體重新開機切換，而且可能需要重新開機多次。</span><span class="sxs-lookup"><span data-stu-id="78f0d-168">To do this, you may have to use a hardware restart switch, and you may have to restart multiple times.</span></span>

<span data-ttu-id="78f0d-169">在 Windows 修復環境中：</span><span class="sxs-lookup"><span data-stu-id="78f0d-169">In the Windows Recovery Environment:</span></span>

1. <span data-ttu-id="78f0d-170">選取 [**疑難排解**  >  **Advanced options**  >  **更多修復選項**  >  **啟動設定**]，然後選取 [**立即重新開機**]。</span><span class="sxs-lookup"><span data-stu-id="78f0d-170">Select **Troubleshoot** > **Advanced options** > **More recovery options** > **Startup settings**, and then select **Restart now**.</span></span>
1. <span data-ttu-id="78f0d-171">在啟動設定清單中，選取 [ **停用驅動程式** 簽章強制]。</span><span class="sxs-lookup"><span data-stu-id="78f0d-171">In the list of startup settings, select **Disable driver signature enforcement**.</span></span>
   > [!NOTE]  
   > <span data-ttu-id="78f0d-172">您可能必須使用 F7 鍵來選取此設定。</span><span class="sxs-lookup"><span data-stu-id="78f0d-172">You may have to use the F7 key to select this setting.</span></span>
1. <span data-ttu-id="78f0d-173">讓啟動進程繼續進行。</span><span class="sxs-lookup"><span data-stu-id="78f0d-173">Let the startup process continue.</span></span> <span data-ttu-id="78f0d-174">當 Windows 重新開機時，系統還原程式應繼續執行並完成。</span><span class="sxs-lookup"><span data-stu-id="78f0d-174">When Windows restarts, the system restore process should resume and finish.</span></span>

<span data-ttu-id="78f0d-175">這些步驟會將電腦還原到其「R1」狀態。</span><span class="sxs-lookup"><span data-stu-id="78f0d-175">These steps restore the computer to its "R1" state.</span></span>

<span data-ttu-id="78f0d-176">**從失敗的重新開機復原**</span><span class="sxs-lookup"><span data-stu-id="78f0d-176">**To recover from the failed restart**</span></span>

<span data-ttu-id="78f0d-177">若要從失敗的重新開機復原並復原還原程式，請遵循下列步驟：</span><span class="sxs-lookup"><span data-stu-id="78f0d-177">To recover from the failed restart and roll back the restore process, follow these steps:</span></span>

1. <span data-ttu-id="78f0d-178">如先前程式中所述，重新開機電腦，然後輸入 WinRE。</span><span class="sxs-lookup"><span data-stu-id="78f0d-178">As described in the previous procedure, restart the computer and then enter WinRE.</span></span>  
1. <span data-ttu-id="78f0d-179">在 Windows 修復環境中，選取 [**疑難排解**  >  **Advanced options**  >  **系統還原**]，然後選取 [**復原系統還原**]。</span><span class="sxs-lookup"><span data-stu-id="78f0d-179">In the Windows Recovery Environment, select **Troubleshoot** > **Advanced options** > **System restore**, and then select **Undo system restore**.</span></span>

<span data-ttu-id="78f0d-180">這些步驟會在您開始還原程式之前，將電腦恢復為其所在的狀態。</span><span class="sxs-lookup"><span data-stu-id="78f0d-180">These steps return the computer to the state that it was in before you started the restore process.</span></span>

<span data-ttu-id="78f0d-181">**使用 WinRE 將 Windows 還原至還原點**</span><span class="sxs-lookup"><span data-stu-id="78f0d-181">**To restore Windows to a restore point by using WinRE**</span></span>

<span data-ttu-id="78f0d-182">若要在受影響的電腦上啟動系統還原 wizard，請使用 WinRE，而不是 [ **設定** ] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="78f0d-182">To start the System Restore wizard on an affected computer, use WinRE instead of the **Settings** dialog box.</span></span> <span data-ttu-id="78f0d-183">若要這樣做，請遵循下列步驟：</span><span class="sxs-lookup"><span data-stu-id="78f0d-183">To do this, follow these steps:</span></span>

1. <span data-ttu-id="78f0d-184">選取 [**啟動**  >  **設定**  >  **更新 & 安全性** 復原]  >  \*\*\*\*。</span><span class="sxs-lookup"><span data-stu-id="78f0d-184">Select **Start** > **Settings** > **Update & Security** > **Recovery**.</span></span>
1. <span data-ttu-id="78f0d-185">在 [ **Advanced options**] 底下，選取 [ **立即重新開機**]。</span><span class="sxs-lookup"><span data-stu-id="78f0d-185">Under **Advanced options**, select **Restart now**.</span></span>
1. <span data-ttu-id="78f0d-186">WinRE 開始之後，請選取 [**疑難排解**  >  **Advanced options**  >  **系統還原**]。</span><span class="sxs-lookup"><span data-stu-id="78f0d-186">After WinRE starts, select **Troubleshoot** > **Advanced options** > **System restore**.</span></span>
1. <span data-ttu-id="78f0d-187">輸入您的修復金鑰（顯示在畫面上），然後依照系統還原 wizard 中的指示進行。</span><span class="sxs-lookup"><span data-stu-id="78f0d-187">Enter your recovery key as it is shown on the screen, and then follow the instructions in the System Restore wizard.</span></span>

### <a name="references"></a><span data-ttu-id="78f0d-188">參考資料</span><span class="sxs-lookup"><span data-stu-id="78f0d-188">References</span></span>

<span data-ttu-id="78f0d-189">如需有關如何使用 WinRE 的詳細資訊，請參閱下列文章：</span><span class="sxs-lookup"><span data-stu-id="78f0d-189">For more information about how to use WinRE, see the following articles:</span></span>

- [<span data-ttu-id="78f0d-190">Windows 修復環境 (Windows RE)</span><span class="sxs-lookup"><span data-stu-id="78f0d-190">Windows Recovery Environment (Windows RE)</span></span>](/windows-hardware/manufacture/desktop/windows-recovery-environment--windows-re--technical-reference)
- [<span data-ttu-id="78f0d-191">在 Windows 10 中以安全模式啟動電腦</span><span class="sxs-lookup"><span data-stu-id="78f0d-191">Start your PC in safe mode in Windows 10</span></span>](https://support.microsoft.com/help/12376) 