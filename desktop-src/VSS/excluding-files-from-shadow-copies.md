---
description: 在 Windows Vista 和 Windows Server 2008 和更新版本中，VSS 寫入器或應用程式的開發人員可能會選擇從陰影複製中排除特定檔案。
ms.assetid: 4fe1ae94-7b2f-421a-9009-3a7e88822458
title: 排除陰影複製中的檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c39acf8c92d44bcf8786a880b6ae5eb6a88786809f5af1609dee1b342cd2fb65
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118122103"
---
# <a name="excluding-files-from-shadow-copies"></a>排除陰影複製中的檔案

在 Windows Vista 和 Windows Server 2008 和更新版本中，VSS 寫入器或應用程式的開發人員可能會選擇從陰影複製中排除特定檔案。

「效能影響」和「陰影複製存放區」區域 (也稱為「差異區域」 ) 在陰影複製中使用檔案的方式，與建立陰影複製之後檔案內容中的變更量直接相關。 此外，從陰影複製排除檔案可能會使陰影複製建立變慢。

基於這些理由，只有當檔案很大時，才應該將它從陰影複製中排除，在一個陰影複製和下一個陰影複製之間進行重大變更，而不需要進行備份。

您應該只排除屬於您應用程式的檔案。

如果 \_ \_ \_ \_ 陰影複製內容中未設定 VSS VOLSNAP ATTR，則表示已停用自動復原，而且不可以從陰影複製中排除任何檔案。 如需詳細資訊，請參閱 [**\_ VSS \_ 磁片區快照集 \_ \_ 屬性**](/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes)列舉。

## <a name="using-the-addexcludefilesfromsnapshot-method"></a>使用 AddExcludeFilesFromSnapshot 方法

VSS 寫入器可以從陰影複製中排除檔案，如下所示：

1.  呼叫 [**IVssCreateWriterMetadataEx：： AddExcludeFilesFromSnapshot**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadataex-addexcludefilesfromsnapshot) 方法，以報告要排除的檔案。
2.  在寫入器的 [**CVssWriter：： OnPostSnapshot**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostsnapshot) 方法中，刪除陰影複製中的檔案。

## <a name="using-the-filesnottosnapshot-registry-key"></a>使用 FilesNotToSnapshot 登錄機碼

> [!Note]  
> **FilesNotToSnapshot** 登錄機碼僅供應用程式使用。 嘗試使用此登錄機碼的使用者會遇到下列限制：
>
> -   無法在 Windows Server 上使用舊版功能建立的陰影複製中刪除檔案。
> -   無法從共用資料夾陰影複製中刪除檔案。
> -   它可以從使用 [DiskShadow](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc772172(v=ws.11)) 公用程式所建立的陰影複製中刪除檔案，但它無法從使用 [Vssadmin](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc754968(v=ws.11)) 公用程式所建立的陰影複製中刪除檔案。
> -   檔案會盡可能以各種方式從陰影複製中刪除。 但這表示我們無法保證能將其刪除。

 

VSS 應用程式可以使用下列登錄機碼，在陰影複製建立期間從陰影複製中刪除檔案：

**HKEY \_ LOCAL \_ MACHINE \\ System \\ CurrentControlSet \\ Control \\ BackupRestore \\ FilesNotToSnapshot**

此登錄機碼 \_ \_ 針對可排除其檔案的每個應用程式，都具有 REG 多重 SZ 值。 檔案是以完整路徑指定，可以包含 \* 萬用字元。

在所有情況下，如果沒有任何檔案符合路徑字串，則會忽略此專案。

將檔案新增至適當的登錄機碼值之後，陰影複製優化寫入器會以最佳方式在建立期間從陰影複製中刪除該檔案。

如果無法指定完整路徑，則也可以使用 $UserProfile $ 或 $AllVolumes $ 變數來隱含路徑。 例如：

-   $UserProfile $ \\ Directory \\ 子目錄 \\ 檔案名。\*
-   $AllVolumes $ \\ TemporaryFiles \\ \* 。\*

若要將路徑設為遞迴，請將 "/s" 附加至結尾。 例如：

-   $UserProfile $ \\ Directory \\ 子目錄 \\ 檔案名 \* /s
-   $AllVolumes $ \\ TemporaryFiles \\ \* \* /s

$UserProfile $ 變數會將路徑字串套用至電腦上的所有使用者設定檔。 藉由檢查下列登錄機碼來列舉使用者設定檔：

**HKEY \_ LOCAL \_ MACHINE \\ Software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ ProfileList**

$AllVolumes $ 變數會將路徑字串套用至電腦上的所有陰影複製。 例如，假設路徑為 "$AllVolumes $ \\ TemporaryFiles \\ \* 。 \*/s "，且電腦有三個磁片區： C：、D：和 E:。 如果 C：和 E：包含路徑 " \\ TemporaryFiles \\ "，而磁片區 D：只包含路徑 d： \\ Data，則 \\ 會從 C：的陰影複製中刪除目錄樹狀結構 C： \\ TemporaryFiles \\ ，且目錄樹狀結構 E： \\ TemporaryFiles \\ 會從 E:. 的陰影複製中刪除

系統管理員可以使用下列登錄機碼來停用 $UserProfile $ 變數的擴充：

**HKEY \_ LOCAL \_ MACHINE \\ System \\ CurrentControlSet \\ Services \\ Vss \\ 設定**

在此登錄機碼下，為值名稱指定 DisableUserProfileExpansion、為 \_ 數值型別指定 REG DWORD，並為值資料指定非零值。

## <a name="about-the-filesnottobackup-registry-key"></a>關於 FilesNotToBackup 登錄機碼

**FilesNotToBackup** 登錄機碼可以用來指定備份應用程式不應備份或還原的檔案和目錄名稱。 不過，它不會從陰影複製中排除這些檔案。 如需此登錄機碼的詳細資訊，請參閱 [備份和還原的登錄機碼和值](../backup/registry-keys-for-backup-and-restore.md)。

 

 
