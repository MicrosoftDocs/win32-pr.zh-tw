---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 26e7eaae-f540-47d1-99ec-6af0fd223039
title: 'D (磁碟區陰影複製服務) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3910a2fb09688e26b33b586f4558c05cb804688645486dfec751c9839fcff278
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998028"
---
# <a name="d-volume-shadow-copy-service"></a>D (磁碟區陰影複製服務) 

[](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) D [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) [](vssgloss-v.md) [W](vssgloss-w.md) X Y Z

<dl> <dt>

<span id="base.vssgloss_database_component"></span><span id="BASE.VSSGLOSS_DATABASE_COMPONENT"></span>**資料庫元件**
</dt> <dd>

資料庫所使用的檔案群組，由寫入器定義，以在備份和還原作業期間，必須當做一個單位來處理。 另請參閱 [*元件*](vssgloss-c.md)、檔案 [*群組元件*](vssgloss-f.md)。

</dd> <dt>

<span id="base.vssgloss_default_provider"></span><span id="BASE.VSSGLOSS_DEFAULT_PROVIDER"></span>**預設提供者**
</dt> <dd>

請參閱 [*系統提供者*](vssgloss-s.md)。

</dd> <dt>

<span id="base.vssgloss_deleted_shadow_copy"></span><span id="BASE.VSSGLOSS_DELETED_SHADOW_COPY"></span>**刪除陰影複製**
</dt> <dd>

已刪除的陰影複製完全無法存取，而且在未來的任何時間都不得供存取。

</dd> <dt>

<span id="base.vssgloss_dependency"></span><span id="BASE.VSSGLOSS_DEPENDENCY"></span>**依賴**
</dt> <dd>

請參閱 [*元件*](vssgloss-c.md)相依性。

</dd> <dt>

<span id="base.vssgloss_device_object"></span><span id="BASE.VSSGLOSS_DEVICE_OBJECT"></span>**裝置物件**
</dt> <dd>

字串，表示陰影複製之磁片區的 "root"。 您可以在原始磁片區上的對應路徑前面加上裝置物件字串，以參考陰影複製的磁片區上的檔案和目錄。 以 [**VSS \_ 快照 \_**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop)集架構結構的 **m \_ pwszSnapshotDeviceObject** 成員的形式取得，裝置物件沒有反斜線 ( " \\ " ) 。

</dd> <dt>

<span id="base.vssgloss_diff_area"></span><span id="BASE.VSSGLOSS_DIFF_AREA"></span>**差異區域**
</dt> <dd>

儲存 *差異資料* 之磁片區上的位置。 這也稱為陰影複製儲存空間。

</dd> <dt>

<span id="base.vssgloss_differenced_files"></span><span id="BASE.VSSGLOSS_DIFFERENCED_FILES"></span>**差異檔案**
</dt> <dd>

在增量或差異備份作業中，藉由更新整個檔案所執行的檔案， (，而不是使用部分檔案支援) 來修改這些檔案的區段。 比方說，如果要執行差異備份，則會將整個檔案 (而不只是修改過的區段) 複製到備份媒體，而該檔案是差異的檔案。 另請參閱 [*增量備份作業*](vssgloss-i.md)、 *差異備份作業*、 [*部分檔案支援*](vssgloss-p.md)。

</dd> <dt>

<span id="base.vssgloss_differential_backup_operations"></span><span id="BASE.VSSGLOSS_DIFFERENTIAL_BACKUP_OPERATIONS"></span>**差異備份作業**
</dt> <dd>

只有儲存上次完整備份之後所建立或變更的檔案才會執行備份或還原作業。 另請參閱 [*增量備份作業*](vssgloss-i.md)、 [*部分檔案支援*](vssgloss-p.md)、 *差異* 檔案。

</dd> <dt>

<span id="base.vssgloss_differential_data"></span><span id="BASE.VSSGLOSS_DIFFERENTIAL_DATA"></span>**差異資料**
</dt> <dd>

可套用至原始磁片區以產生陰影複製磁片區的資料。 這也稱為「寫入時複製」資料，但本檔使用「差異資料」一詞。

</dd> <dt>

<span id="base.vssgloss_directed_targeting"></span><span id="BASE.VSSGLOSS_DIRECTED_TARGETING"></span>**導向目標**
</dt> <dd>

寫入器表示在還原檔案時，它 (應重新對應來源檔案) 的還原模式。 檔案可能會還原至新的還原位置和/或其資料的範圍，還原至與還原位置不同的位移。

</dd> </dl>

 

 



