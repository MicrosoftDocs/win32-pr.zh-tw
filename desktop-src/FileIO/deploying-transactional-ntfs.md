---
description: 在交易式 NTFS 中快取控制項。
ms.assetid: 0fd272ee-cf5f-4ba9-b8aa-ff0016f51d4b
title: 部署交易式 NTFS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd7c44e0ad3b83854e56d18171072a7cb4615d5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943851"
---
# <a name="deploying-transactional-ntfs"></a>部署交易式 NTFS

交易式 NTFS (TxF) ，就像大多數的交易機制一樣，視資料寫入的正確順序而定。 確保適當的寫入順序需要明確控制資料快取。 為了滿足這項需求，TxF 要求磁片磁碟機必須執行屬於標準化磁片磁碟機介面（例如 SCSI、SATA 和 ATA）一部分的快取控制機制。

TxF 使用的快取控制機制是稱為「強制單位存取」 (FUA) 函數的旗標。 此旗標指定磁片磁碟機應該先將資料寫入至穩定的媒體儲存體，才能完成信號。 在交易內的某些關鍵點上，TxF 需要發出 FUA，以確保在發生電源中斷時，不會遺失成功回復交易所需的部分控制資料。

伺服器類別磁片磁碟機 (SCSI 和光纖通道) 一般支援 FUA 旗標。 從 Vista 開始，Windows 僅支援 SCSI 和光纖通道磁片的 FUA 旗標。

在商用磁片磁碟機上 (ATA/SATA/USB) ，TxF 的弱點有一段期間，在這段期間內，磁片磁碟機電源失敗會導致 TxF 無法正確回復交易，因此除非已停用磁片磁碟機的寫入快取，否則資料會保持不一致的狀態。

某些主機匯流排介面卡 (Hba) 和儲存控制器 (例如，RAID 系統) 有內建的電池支援快取。 因為這些裝置會在發生電源錯誤時保留快取的資料，所以任何連接到它們的磁片都不需要接受 FUA 旗標。 此外，電源供應器受到不斷電供應系統供應 (UPS) 保護的磁片不需要接受 FUA 旗標。 這是因為 UPS 會維持足夠的電源，足以讓磁片將快取排清至媒體。

停用磁片磁碟機的寫入快取，可避免磁片磁碟機接受 FUA 旗標的需求。 您可以藉由向磁片發出 [**IOCTL 磁片集快取 \_ \_ \_ \_ 資訊**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_disk_set_cache_information) 控制項程式碼，來停用磁片的寫入快取。 寫入快取 (開啟/關閉) 將會在系統重新開機時保留。 發出此控制項程式碼對於發出至該磁片的所有 i/o 都會有相當大的效能影響，這很可能會造成顯著的效能降低。 在部署之前，應該謹慎考慮使用此控制項程式碼。

> [!Note]  
> 為了讓 TxF 能以一致的方式保護資料的完整性，系統必須符合下列其中一個準則：
>
> -   使用伺服器類別磁片 (SCSI、光纖通道) 。
> -   確定磁片已連接到電池支援的快取 HBA。
> -   使用儲存體控制器 (例如，RAID 系統) 作為存放裝置。
> -   確定磁片的電源受到 UPS 的保護。
> -   確定磁片的寫入快取功能已停用。

 

 

 



