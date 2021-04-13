---
title: 備份與還原 DRM 授權
description: 備份與還原 DRM 授權
ms.assetid: ec2777e9-76af-43fe-8bd5-4d7532d2fb32
keywords:
- Windows Media Format SDK，備份 DRM 授權
- Windows Media Format SDK，還原 DRM 授權
- Windows Media Format SDK，DRM 授權
- Windows Media Format SDK，DRM 的授權
- Windows Media Format SDK，備份還原功能
- Windows Media Format SDK，授權管理服務
- Windows Media Format SDK，詐騙偵測
- 數位版權管理 (DRM) ，備份授權
- DRM (數位版權管理) ，備份授權
- 數位版權管理 (DRM) ，還原授權
- DRM (數位版權管理) ，還原授權
- 數位版權管理 (DRM) 、授權
- DRM (數位版權管理) 、授權
- 數位版權管理 (DRM) ，備份還原功能
- DRM (數位版權管理) ，備份還原功能
- 數位版權管理 (DRM) ，授權管理服務
- DRM (數位版權管理) ，授權管理服務
- 數位版權管理 (DRM) ，詐騙偵測
- DRM (數位版權管理) ，詐騙偵測
- 備份 DRM 授權
- 還原 DRM 授權
- 授權，DRM
- 授權，備份 DRM
- 授權，還原 DRM
- 備份還原功能
- 授權管理服務
- 詐騙偵測
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7718f03170077f7db624f8a99b8262239a79ca9
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/09/2020
ms.locfileid: "104316651"
---
# <a name="backing-up-and-restoring-of-drm-licenses"></a><span data-ttu-id="87d8e-130">備份與還原 DRM 授權</span><span class="sxs-lookup"><span data-stu-id="87d8e-130">Backing Up and Restoring of DRM Licenses</span></span>

<span data-ttu-id="87d8e-131">使用備份還原功能時，使用者可以將 [*授權*](wmformat-glossary.md) 備份和還原到同一部電腦或其他電腦。</span><span class="sxs-lookup"><span data-stu-id="87d8e-131">With the Backup Restore feature, users can back up and restore [*licenses*](wmformat-glossary.md) to the same computer or to other computers.</span></span> <span data-ttu-id="87d8e-132">這項功能可讓使用者在重新格式化硬碟之後，將授權傳送到新的電腦或回到同一部電腦 (，例如) 。</span><span class="sxs-lookup"><span data-stu-id="87d8e-132">This feature enables users to transfer licenses to a new computer or back to the same computer (after reformatting the hard disk, for example).</span></span> <span data-ttu-id="87d8e-133">此外，使用者也可以在一部以上的電腦上播放受保護的 ASF 檔案。</span><span class="sxs-lookup"><span data-stu-id="87d8e-133">In addition, users can play protected ASF files on more than one computer.</span></span>

<span data-ttu-id="87d8e-134">為了鼓勵合法使用授權，詐騙偵測原則會限制可以還原授權的次數。</span><span class="sxs-lookup"><span data-stu-id="87d8e-134">To encourage legitimate use of a license, a fraud detection policy restricts the number of times a license can be restored.</span></span> <span data-ttu-id="87d8e-135">Microsoft 提供的服務會追蹤已還原授權的電腦數目;如果達到限制，則使用者無法還原授權。</span><span class="sxs-lookup"><span data-stu-id="87d8e-135">Microsoft provides a service that tracks the number of computers to which a license has been restored; if a limit is reached, the user cannot restore the license.</span></span>

## <a name="allowing-or-disallowing-the-right-to-back-up-and-restore"></a><span data-ttu-id="87d8e-136">允許或不允許備份和還原的許可權</span><span class="sxs-lookup"><span data-stu-id="87d8e-136">Allowing or Disallowing the Right to Back Up and Restore</span></span>

<span data-ttu-id="87d8e-137">備份還原功能只適用于提供備份和還原許可權的授權。</span><span class="sxs-lookup"><span data-stu-id="87d8e-137">The Backup Restore feature works only for licenses for which the Backup and Restore right is given.</span></span> <span data-ttu-id="87d8e-138">如果內容擁有者或授權簽發者不想要這項功能，或它們發出的授權包含安全狀態 (例如計數作業或有限的時間) ，則可以不允許這種許可權。</span><span class="sxs-lookup"><span data-stu-id="87d8e-138">If content owners or license issuers do not want this feature, or if they issue licenses that contain a secure state (such as counted operations or limited time), they can disallow this right.</span></span>

<span data-ttu-id="87d8e-139">當授權無法還原，因為使用者沒有許可權，就會將 [*金鑰識別碼*](wmformat-glossary.md) 傳遞至應用程式。</span><span class="sxs-lookup"><span data-stu-id="87d8e-139">When a license cannot be restored because a user does not have the right, a [*key ID*](wmformat-glossary.md) is passed to the application.</span></span> <span data-ttu-id="87d8e-140">使用者至少應該收到某些授權無法備份的通知，但使用者不知道此訊息所參考的授權。</span><span class="sxs-lookup"><span data-stu-id="87d8e-140">At a minimum, the user should be notified that some licenses could not be backed up, although the user does not know which licenses this message refers to.</span></span> <span data-ttu-id="87d8e-141">如果您知道可用受保護檔案的金鑰識別碼，您可以開發更健全的解決方案來通知使用者。</span><span class="sxs-lookup"><span data-stu-id="87d8e-141">If you know the key ID for available protected files, you can develop a more robust solution for informing the user.</span></span>

<span data-ttu-id="87d8e-142">例如，您可以針對在網際網路上提供受保護的歌曲的記錄標籤開發播放機。</span><span class="sxs-lookup"><span data-stu-id="87d8e-142">For example, a player could be developed for a record label that provides protected songs on the Internet.</span></span> <span data-ttu-id="87d8e-143">這些歌曲及其金鑰識別碼可在資料庫中追蹤。</span><span class="sxs-lookup"><span data-stu-id="87d8e-143">These songs and their key IDs could be tracked in a database.</span></span> <span data-ttu-id="87d8e-144">如果某些授權無法備份，播放程式應用程式可以使用金鑰識別碼來查詢資料庫中的歌曲名稱，然後通知使用者無法備份授權的歌曲。</span><span class="sxs-lookup"><span data-stu-id="87d8e-144">If some licenses could not be backed up, the player application could use the key ID to query the database for the name of the songs, then inform the user for which songs the licenses cannot be backed up.</span></span> <span data-ttu-id="87d8e-145">或者，您可以在本機為每位使用者建立音樂媒體櫃，而且金鑰識別碼可以用來取得有關哪些授權無法備份的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="87d8e-145">Or, a music library could be created for each user locally, and the key ID could be used to retrieve more information about which licenses could not be backed up.</span></span>

## <a name="the-license-management-service"></a><span data-ttu-id="87d8e-146">授權管理服務</span><span class="sxs-lookup"><span data-stu-id="87d8e-146">The License Management Service</span></span>

<span data-ttu-id="87d8e-147">當執行備份還原功能時，由 Microsoft 託管的授權管理服務會管理授權的還原。</span><span class="sxs-lookup"><span data-stu-id="87d8e-147">When the Backup Restore feature is implemented, a License Management Service that is hosted by Microsoft manages the restoration of licenses.</span></span>

<span data-ttu-id="87d8e-148">首先，使用者會在應用程式中備份授權，例如選擇功能表選項。</span><span class="sxs-lookup"><span data-stu-id="87d8e-148">First, users back up licenses in the application, for example, by choosing a menu option.</span></span> <span data-ttu-id="87d8e-149">電腦上的所有授權都會備份到指定的位置，例如磁片磁碟機。</span><span class="sxs-lookup"><span data-stu-id="87d8e-149">All licenses on the computer are backed up to a specified location, such as a floppy disk.</span></span> <span data-ttu-id="87d8e-150">然後，使用者會使用應用程式來還原授權，例如，選擇功能表選項並指定其備份位置。</span><span class="sxs-lookup"><span data-stu-id="87d8e-150">Then, users restore licenses by using the application, for example, by choosing a menu option and specifying their backup location.</span></span>

<span data-ttu-id="87d8e-151">此時，使用者必須連線到網際網路。來自應用程式的要求會傳送至授權管理服務。</span><span class="sxs-lookup"><span data-stu-id="87d8e-151">At this point, the user must be connected to the Internet; a request from the application is sent to the License Management Service.</span></span> <span data-ttu-id="87d8e-152">如果備份授權的電腦與原始電腦不同 (或原始電腦已) 重新格式化，則授權管理服務會對新電腦發出新的授權。</span><span class="sxs-lookup"><span data-stu-id="87d8e-152">If the computer from which the license was backed up is different from the original computer (or the original computer has been reformatted), the License Management Service issues a new license to the new computer.</span></span> <span data-ttu-id="87d8e-153">否則，就會重新發出先前發行給該電腦的授權。</span><span class="sxs-lookup"><span data-stu-id="87d8e-153">Otherwise, the license that was previously issued to that computer is reissued.</span></span>

<span data-ttu-id="87d8e-154">因為授權管理服務會抓取使用者的資訊，所以您必須在 [Microsoft 網站](https://www.microsoft.com/licensing/default)上顯示 microsoft 隱私權原則或提供該頁面的連結。</span><span class="sxs-lookup"><span data-stu-id="87d8e-154">Because the License Management Service retrieves information from the user, you must display the Microsoft privacy policy or provide a link to that page at the [Microsoft Web site](https://www.microsoft.com/licensing/default).</span></span>

> [!Note]  
> <span data-ttu-id="87d8e-155">當使用者將授權還原至不同的電腦，而且授權需要使用個人化時，終端使用者必須授權 DRM 元件更新。</span><span class="sxs-lookup"><span data-stu-id="87d8e-155">When an end user restores a license to a different computer and the license requires individualization, the end user must authorize the DRM components to be updated.</span></span> <span data-ttu-id="87d8e-156">您必須在播放程式應用程式中執行程式，以支援這項功能。</span><span class="sxs-lookup"><span data-stu-id="87d8e-156">You must implement a process in your player application to support this feature.</span></span>

 

## <a name="detecting-fraud"></a><span data-ttu-id="87d8e-157">偵測詐騙</span><span class="sxs-lookup"><span data-stu-id="87d8e-157">Detecting Fraud</span></span>

<span data-ttu-id="87d8e-158">允許使用者將授權還原為有限的次數。</span><span class="sxs-lookup"><span data-stu-id="87d8e-158">The user is allowed to restore a license a limited number of times.</span></span> <span data-ttu-id="87d8e-159">每次還原授權時，授權管理服務都會追蹤它，並將該授權的計數遞增一。</span><span class="sxs-lookup"><span data-stu-id="87d8e-159">Each time a license is restored, the License Management Service tracks it and increments the count for that license by one.</span></span> <span data-ttu-id="87d8e-160">將授權還原至先前已還原授權的電腦時 (例如，用來備份授權的電腦) ，則不會增加計數。</span><span class="sxs-lookup"><span data-stu-id="87d8e-160">When restoring a license to a computer to which the license has been restored previously (for example, the computer from which the license was backed up), the count is not increased.</span></span> <span data-ttu-id="87d8e-161">如果電腦有新的作業系統，或已重新安裝作業系統，則會被視為不同的電腦。</span><span class="sxs-lookup"><span data-stu-id="87d8e-161">A computer is considered to be different if it has a new operating system, or the operating system has been re-installed.</span></span>

<span data-ttu-id="87d8e-162">根據 Microsoft 的詐騙偵測原則，當授權經過一定次數的還原時，應用程式會接收來自 DRM 元件的 URL，並負責開啟瀏覽器並顯示網頁，指出可能違反授權合約。</span><span class="sxs-lookup"><span data-stu-id="87d8e-162">In accordance with Microsoft's fraud detection policy, when a license has been restored a certain number of times, the application receives a URL from the DRM components and is responsible for opening a browser and displaying the Web page, which indicates that the license agreement might have been violated.</span></span> <span data-ttu-id="87d8e-163">使用者必須與授權散發者聯繫，之後必須判斷要求是否有效。</span><span class="sxs-lookup"><span data-stu-id="87d8e-163">The user must contact the license distributor, who must then determine whether the request is valid.</span></span>

> [!Note]  
> <span data-ttu-id="87d8e-164">此 SDK 的 x64 版本不支援 DRM。</span><span class="sxs-lookup"><span data-stu-id="87d8e-164">DRM is not supported by the x64-based version of this SDK.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="87d8e-165">相關主題</span><span class="sxs-lookup"><span data-stu-id="87d8e-165">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="87d8e-166">**數位 Rights Management 功能**</span><span class="sxs-lookup"><span data-stu-id="87d8e-166">**Digital Rights Management Features**</span></span>](digital-rights-management-features.md)
</dt> <dt>

[<span data-ttu-id="87d8e-167">**備份和還原授權**</span><span class="sxs-lookup"><span data-stu-id="87d8e-167">**Backing Up and Restoring Licenses**</span></span>](backing-up-and-restoring-licenses.md)
</dt> </dl>

 

 




