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
# <a name="backing-up-and-restoring-licenses"></a>備份和還原授權

備份和還原程式都是非同步。 當使用者在應用程式中選取要備份或還原授權的功能表命令或選項時，就會觸發它們。 您應允許使用者指定必須備份和還原授權的位置。

若要備份授權：

1.  使用 [**WMCreateBackupRestorer**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatebackuprestorer) 函式來建立備份 restorer 物件。
2.  呼叫 [**IWMBackupRestoreProps：： SetProp**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmbackuprestoreprops-setprop) 方法，將備份路徑設定 (您將在其中寫入檔案的位置，例如： \\ 或 D： \\ 授權) 。
3.  呼叫 [**IWMLicenseBackup：： BackupLicenses**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlicensebackup-backuplicenses) 方法，將授權備份至指定的路徑。

下列事件會傳送至 [**IWMStatusCallback：： OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) 方法：

-   **WMT \_BACKUPRESTORE \_ 開始** 表示備份程式已開始。
-   **WMT \_BACKUPRESTORE \_ END** 表示備份程式已完成。
-   **WMT \_受限制的 \_ 授權** 表示無法備份一或多個授權，因為內容擁有者不允許該許可權。

此訊息中也包含金鑰識別碼。 如果您已針對包含金鑰識別碼和中繼資料的受保護檔案執行資料庫，您可以向使用者顯示具有特定標題的訊息 (例如無法備份授權的歌曲標題) 。 否則，訊息必須是泛型，並通知使用者某些授權無法備份。

若要還原授權：

1.  使用 **WMCreateBackupRestorer** 函式來建立備份 restorer 物件。
2.  呼叫 **IWMBackupRestoreProps：： SetProp** 方法，將還原路徑設定為備份授權的位置。
3.  呼叫 [**IWMLicenseRestore：： RestoreLicenses**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlicenserestore-restorelicenses) 方法，從該位置還原授權。

下列事件會傳送至 [**IWMStatusCallback：： OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) 方法：

-   **WMT \_BACKUPRESTORE \_ 連接** 表示應用程式正在連線至授權管理服務。
-   **WMT \_BACKUPRESTORE \_ 中斷** 連線表示應用程式正在與授權管理服務中斷連線。
-   **WMT \_BACKUPRESTORE \_ 開始** 表示還原程式已開始。
-   **WMT \_BACKUPRESTORE \_ END** 表示還原程式已完成。

> [!Note]  
> 此 SDK 的 x64 版本不支援 DRM。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**數位 Rights Management 功能**](digital-rights-management-features.md)
</dt> <dt>

[**IWMBackupRestoreProps 介面**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmbackuprestoreprops)
</dt> <dt>

[**IWMLicenseBackup 介面**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicensebackup)
</dt> <dt>

[**IWMLicenseRestore 介面**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicenserestore)
</dt> </dl>

 

 




