---
title: 備份和還原授權
description: 備份和還原授權
ms.assetid: 59be02fe-f207-4161-8765-9a88a8050248
keywords:
- Windows Media Format SDK，備份授權
- Windows Media Format SDK，還原授權
- Windows Media Format SDK、授權備份和還原
- Advanced Systems Format (ASF) ，備份授權
- ASF (Advanced Systems Format) ，備份授權
- Advanced Systems Format (ASF) ，還原授權
- ASF (Advanced Systems Format) ，還原授權
- Advanced Systems Format (ASF) 、授權備份和還原
- ASF (Advanced 系統格式) 、授權備份和還原
- 數位版權管理 (DRM) ，備份授權
- DRM (數位版權管理) ，備份授權
- 數位版權管理 (DRM) ，還原授權
- DRM (數位版權管理) ，還原授權
- 數位版權管理 (DRM) 、授權備份和還原
- DRM (數位版權管理) 、授權備份和還原
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d10d8e76c191225288a1021e08e4c77e7e14f3c6
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "103681416"
---
# <a name="backing-up-and-restoring-licenses"></a><span data-ttu-id="382b1-118">備份和還原授權</span><span class="sxs-lookup"><span data-stu-id="382b1-118">Backing Up and Restoring Licenses</span></span>

<span data-ttu-id="382b1-119">備份和還原程式都是非同步。</span><span class="sxs-lookup"><span data-stu-id="382b1-119">The backup and restore processes are asynchronous.</span></span> <span data-ttu-id="382b1-120">當使用者在應用程式中選取要備份或還原授權的功能表命令或選項時，就會觸發它們。</span><span class="sxs-lookup"><span data-stu-id="382b1-120">They are triggered when the user selects a menu command or option in the application to back up or restore licenses.</span></span> <span data-ttu-id="382b1-121">您應允許使用者指定必須備份和還原授權的位置。</span><span class="sxs-lookup"><span data-stu-id="382b1-121">You should allow the user to specify the locations where licenses must be backed up to and restored from.</span></span>

<span data-ttu-id="382b1-122">若要備份授權：</span><span class="sxs-lookup"><span data-stu-id="382b1-122">To back up licenses:</span></span>

1.  <span data-ttu-id="382b1-123">使用 [**WMCreateBackupRestorer**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatebackuprestorer) 函式來建立備份 restorer 物件。</span><span class="sxs-lookup"><span data-stu-id="382b1-123">Use the [**WMCreateBackupRestorer**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatebackuprestorer) function to create the backup restorer object.</span></span>
2.  <span data-ttu-id="382b1-124">呼叫 [**IWMBackupRestoreProps：： SetProp**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmbackuprestoreprops-setprop) 方法，將備份路徑設定 (您將在其中寫入檔案的位置，例如： \\ 或 D： \\ 授權) 。</span><span class="sxs-lookup"><span data-stu-id="382b1-124">Call the [**IWMBackupRestoreProps::SetProp**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmbackuprestoreprops-setprop) method to set the backup path (the location where you will write the files, such as A:\\ or D:\\Licenses).</span></span>
3.  <span data-ttu-id="382b1-125">呼叫 [**IWMLicenseBackup：： BackupLicenses**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlicensebackup-backuplicenses) 方法，將授權備份至指定的路徑。</span><span class="sxs-lookup"><span data-stu-id="382b1-125">Call the [**IWMLicenseBackup::BackupLicenses**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlicensebackup-backuplicenses) method to back up the licenses to the specified path.</span></span>

<span data-ttu-id="382b1-126">下列事件會傳送至 [**IWMStatusCallback：： OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) 方法：</span><span class="sxs-lookup"><span data-stu-id="382b1-126">The following events are sent to the [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) method:</span></span>

-   <span data-ttu-id="382b1-127">**WMT \_BACKUPRESTORE \_ 開始** 表示備份程式已開始。</span><span class="sxs-lookup"><span data-stu-id="382b1-127">**WMT\_BACKUPRESTORE\_BEGIN** indicates the backup process has started.</span></span>
-   <span data-ttu-id="382b1-128">**WMT \_BACKUPRESTORE \_ END** 表示備份程式已完成。</span><span class="sxs-lookup"><span data-stu-id="382b1-128">**WMT\_BACKUPRESTORE\_END** indicates the backup process has been completed.</span></span>
-   <span data-ttu-id="382b1-129">**WMT \_受限制的 \_ 授權** 表示無法備份一或多個授權，因為內容擁有者不允許該許可權。</span><span class="sxs-lookup"><span data-stu-id="382b1-129">**WMT\_RESTRICTED\_LICENSE** indicates that one or more licenses cannot be backed up because the right has been disallowed by the content owner.</span></span>

<span data-ttu-id="382b1-130">此訊息中也包含金鑰識別碼。</span><span class="sxs-lookup"><span data-stu-id="382b1-130">The key ID is also included in this message.</span></span> <span data-ttu-id="382b1-131">如果您已針對包含金鑰識別碼和中繼資料的受保護檔案執行資料庫，您可以向使用者顯示具有特定標題的訊息 (例如無法備份授權的歌曲標題) 。</span><span class="sxs-lookup"><span data-stu-id="382b1-131">If you have implemented a database for protected files that includes the key ID and metadata, you can display a message to the user with the specific title (such as a song title) for which the license cannot be backed up.</span></span> <span data-ttu-id="382b1-132">否則，訊息必須是泛型，並通知使用者某些授權無法備份。</span><span class="sxs-lookup"><span data-stu-id="382b1-132">Otherwise, the message must be generic and inform the user that some licenses cannot be backed up.</span></span>

<span data-ttu-id="382b1-133">若要還原授權：</span><span class="sxs-lookup"><span data-stu-id="382b1-133">To restore licenses:</span></span>

1.  <span data-ttu-id="382b1-134">使用 **WMCreateBackupRestorer** 函式來建立備份 restorer 物件。</span><span class="sxs-lookup"><span data-stu-id="382b1-134">Use the **WMCreateBackupRestorer** function to create the backup restorer object.</span></span>
2.  <span data-ttu-id="382b1-135">呼叫 **IWMBackupRestoreProps：： SetProp** 方法，將還原路徑設定為備份授權的位置。</span><span class="sxs-lookup"><span data-stu-id="382b1-135">Call the **IWMBackupRestoreProps::SetProp** method to set the restore path to the location where licenses are backed up.</span></span>
3.  <span data-ttu-id="382b1-136">呼叫 [**IWMLicenseRestore：： RestoreLicenses**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlicenserestore-restorelicenses) 方法，從該位置還原授權。</span><span class="sxs-lookup"><span data-stu-id="382b1-136">Call the [**IWMLicenseRestore::RestoreLicenses**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlicenserestore-restorelicenses) method to restore licenses from that location.</span></span>

<span data-ttu-id="382b1-137">下列事件會傳送至 [**IWMStatusCallback：： OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) 方法：</span><span class="sxs-lookup"><span data-stu-id="382b1-137">The following events are sent to the [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) method:</span></span>

-   <span data-ttu-id="382b1-138">**WMT \_BACKUPRESTORE \_ 連接** 表示應用程式正在連線至授權管理服務。</span><span class="sxs-lookup"><span data-stu-id="382b1-138">**WMT\_BACKUPRESTORE\_CONNECTING** indicates that the application is connecting to the License Management Service.</span></span>
-   <span data-ttu-id="382b1-139">**WMT \_BACKUPRESTORE \_ 中斷** 連線表示應用程式正在與授權管理服務中斷連線。</span><span class="sxs-lookup"><span data-stu-id="382b1-139">**WMT\_BACKUPRESTORE\_DISCONNECTING** indicates that the application is disconnecting from the License Management Service.</span></span>
-   <span data-ttu-id="382b1-140">**WMT \_BACKUPRESTORE \_ 開始** 表示還原程式已開始。</span><span class="sxs-lookup"><span data-stu-id="382b1-140">**WMT\_BACKUPRESTORE\_BEGIN** indicates the restore process has started.</span></span>
-   <span data-ttu-id="382b1-141">**WMT \_BACKUPRESTORE \_ END** 表示還原程式已完成。</span><span class="sxs-lookup"><span data-stu-id="382b1-141">**WMT\_BACKUPRESTORE\_END** indicates the restore process has been completed.</span></span>

> [!Note]  
> <span data-ttu-id="382b1-142">此 SDK 的 x64 版本不支援 DRM。</span><span class="sxs-lookup"><span data-stu-id="382b1-142">DRM is not supported by the x64-based version of this SDK.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="382b1-143">相關主題</span><span class="sxs-lookup"><span data-stu-id="382b1-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="382b1-144">**數位 Rights Management 功能**</span><span class="sxs-lookup"><span data-stu-id="382b1-144">**Digital Rights Management Features**</span></span>](digital-rights-management-features.md)
</dt> <dt>

[<span data-ttu-id="382b1-145">**IWMBackupRestoreProps 介面**</span><span class="sxs-lookup"><span data-stu-id="382b1-145">**IWMBackupRestoreProps Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmbackuprestoreprops)
</dt> <dt>

[<span data-ttu-id="382b1-146">**IWMLicenseBackup 介面**</span><span class="sxs-lookup"><span data-stu-id="382b1-146">**IWMLicenseBackup Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicensebackup)
</dt> <dt>

[<span data-ttu-id="382b1-147">**IWMLicenseRestore 介面**</span><span class="sxs-lookup"><span data-stu-id="382b1-147">**IWMLicenseRestore Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicenserestore)
</dt> </dl>

 

 




