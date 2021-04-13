---
description: 下列清單指出 Windows Server 2003 Service Pack 1 (SP1) 中磁碟區陰影複製服務介面的新增和變更：
ms.assetid: 9e0dba98-5d23-444d-bd2f-cb72de8fb2d2
title: Windows Server 2003 SP1 中 VSS 的新功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 559b51d5b019d9d57aa154c4728ef5c8f4bb19d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104469096"
---
# <a name="whats-new-in-vss-in-windows-server-2003-sp1"></a>Windows Server 2003 SP1 中 VSS 的新功能

下列清單指出 Windows Server 2003 Service Pack 1 (SP1) 中磁碟區陰影複製服務介面的新增和變更：

## <a name="auto-recovery"></a>自動復原

[*自動*](vssgloss-a.md) 復原讓寫入器有時間更新陰影複製中的元件，再將陰影複製永久變更為唯讀。 例如，資料庫可能需要復原所有陰影複製的任何未完成交易 (資料庫寫入器會為資料庫元件) 設定 **VSS \_ CF \_ 備份 \_** 復原旗標。 由要求者起始的自動復原允許精細的還原 (例如，還原資料庫中的一個資料表或郵件伺服器上的一個資料夾) 或復原以支援資料採礦，以執行對生產伺服器而言太慢的分析 (要求者會將 **VSS \_ VOLSNAP \_ ATTR \_ 復原復原 \_** 新增至陰影複製內容。 ) 自動復原與可傳送的陰影複製不相容，但使用以可 [轉移陰影複製磁片](fast-recovery-using-transportable-shadow-copied-volumes.md)區的快速復原來支援相同的功能。

下列程式設計項目有變更可支援自動復原：

類別方法

-   [**CVssWriter::GetSnapshotDeviceName**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-getsnapshotdevicename)
-   [**CVssWriter::OnPostSnapshot**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostsnapshot)

列舉

-   [**VSS \_ 元件 \_ 旗標**](/windows/desktop/api/VsWriter/ne-vswriter-vss_component_flags)
-   [**\_VSS \_ 磁片區 \_ 快照集 \_ 屬性**](/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes)

介面方法

-   [**IVssProviderCreateSnapshotSet：:P reFinalCommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-prefinalcommitsnapshots)
-   [**IVssProviderCreateSnapshotSet：:P ostFinalCommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-postfinalcommitsnapshots)

## <a name="full-support-for-transportable-shadow-copies"></a>完整支援可轉移的陰影複製

所有版本的 Windows Server 2003 SP1 都支援可轉移的陰影複製。 如需詳細資訊，請參閱匯 [入可傳送的陰影複製磁片](importing-transportable-shadow-copied-volumes.md)區。

## <a name="fast-recovery-using-transportable-shadow-copied-volumes"></a>使用可轉移陰影複製的磁片區快速復原

[使用可轉移陰影複製的磁片區快速復原](fast-recovery-using-transportable-shadow-copied-volumes.md)

## <a name="shadow-copy-storage-area-management"></a>陰影複製存放區域管理

[**IVssSnapshotMgmt2**](/windows/desktop/api/VsMgmt/nn-vsmgmt-ivsssnapshotmgmt2)

 

 



