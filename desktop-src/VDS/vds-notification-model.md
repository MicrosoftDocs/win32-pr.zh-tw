---
description: VDS 通知
ms.assetid: a0841215-3eb0-4769-b320-4da25b535362
title: VDS 通知
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa99751912f110a77b061d50134135413baf2894
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/04/2021
ms.locfileid: "104566017"
---
# <a name="vds-notifications"></a>VDS 通知

\[從 Windows 8 和 Windows Server 2012 開始， [虛擬磁碟服務](virtual-disk-service-portal.md) COM 介面會被 [Windows 儲存體管理 API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)取代。\]

提供者可以將事件通知傳送至 VDS，而 VDS 也可以將通知轉寄給應用程式。 VDS 使用的通知模型類似于 COM 物件所使用的連接點模型。

VDS 會產生事件的服務通知，例如磁碟機號指派或未配置磁片的抵達。 當 VDS 將磁片配置給提供者之後，提供者會負責產生相關聯的通知。 下圖顯示 VDS 通知模型中所使用的介面和方法。

![顯示介面和方法的圖表， (在應用程式、虛擬磁碟服務和 V D S 提供者之間) 的建議、OnLoad 和 OnNotify。](images/vdsnotification.png)

為了接收通知，VDS 會藉由呼叫 [**IVdsProviderPrivate：： OnLoad**](/windows/desktop/api/VdsHwPrv/nf-vdshwprv-ivdsproviderprivate-onload)方法並將指標傳遞至介面，向提供者物件註冊其 [**IVdsAdviseSink**](/windows/desktop/api/Vds/nn-vds-ivdsadvisesink)介面。 當發生通知事件（例如新磁片區或磁片磁碟機的抵達）時，提供者會將適當的通知結構以 [**IVdsAdviseSink：： OnNotify**](/windows/desktop/api/Vds/nf-vds-ivdsadvisesink-onnotify) 方法參數傳遞至 VDS。

應用程式和 VDS 之間的處理常式很類似。 具體來說，若要接收通知，應用程式會藉由呼叫 [**IVdsService：： Advise**](/windows/desktop/api/Vds/nf-vds-ivdsservice-advise)方法，並將指標傳遞至介面，向 VDS 註冊其 [**IVdsAdviseSink**](/windows/desktop/api/Vds/nn-vds-ivdsadvisesink)介面。 當 VDS 收到來自提供者的通知時，它會將適當的通知結構傳遞給註冊的應用程式，以做為 [**IVdsAdviseSink：： OnNotify**](/windows/desktop/api/Vds/nf-vds-ivdsadvisesink-onnotify) 方法參數。

> [!Note]  
> 呼叫「 [**建議**](/windows/desktop/api/Vds/nf-vds-ivdsservice-advise) 」的應用程式最後必須呼叫 [**IVdsService：： Unadvise**](/windows/desktop/api/Vds/nf-vds-ivdsservice-unadvise) 方法。 在理想的情況下，它應該會在不再需要接收通知時立即呼叫 **Unadvise** 。

 

接下來的表格會依物件類型列出提供者產生的通知。



| Object     | 通知                              | 值 | 事件描述的連結                                             |
|------------|-------------------------------------------|-------|-----------------------------------------------------------------------|
| Pack       | **VDS 的 \_ NF-E \_ 套件 \_ 抵達**                 | 1     | [**VDS \_ 套件 \_ 通知**](/windows/desktop/api/Vds/ns-vds-vds_pack_notification)              |
| Pack       | **VDS 的 \_ NF-E \_ 套件部門 \_**                 | 2     | [**VDS \_ 套件 \_ 通知**](/windows/desktop/api/Vds/ns-vds-vds_pack_notification)              |
| Pack       | **VDS \_ NF-E \_ PACK \_ 修改**                 | 3     | [**VDS \_ 套件 \_ 通知**](/windows/desktop/api/Vds/ns-vds-vds_pack_notification)              |
| 磁碟區     | **VDS \_ NF-E \_ 磁片區 \_ 抵達**               | 4     | [**VDS \_ 大量 \_ 通知**](/windows/desktop/api/Vds/ns-vds-vds_volume_notification)          |
| 磁碟區     | **VDS \_ NF-E \_ VOLUME \_ 起飛**               | 5     | [**VDS \_ 大量 \_ 通知**](/windows/desktop/api/Vds/ns-vds-vds_volume_notification)          |
| 磁碟區     | **VDS \_ NF-E \_ 磁片區 \_ 修改**               | 6     | [**VDS \_ 大量 \_ 通知**](/windows/desktop/api/Vds/ns-vds-vds_volume_notification)          |
| 磁碟區     | **VDS \_ NF-E \_ 磁片區 \_ 重建 \_ 進度** | 7     | [**VDS \_ 大量 \_ 通知**](/windows/desktop/api/Vds/ns-vds-vds_volume_notification)          |
| 磁碟       | **VDS \_ NF-E \_ 磁片 \_ 送達**                 | 8     | [**VDS \_ 磁片 \_ 通知**](/windows/desktop/api/Vds/ns-vds-vds_disk_notification)              |
| 磁碟       | **VDS \_ NF-E \_ 磁片 \_ 部門**                 | 9     | [**VDS \_ 磁片 \_ 通知**](/windows/desktop/api/Vds/ns-vds-vds_disk_notification)              |
| 磁碟       | **VDS \_ NF-E \_ 磁片 \_ 修改**                 | 10    | [**VDS \_ 磁片 \_ 通知**](/windows/desktop/api/Vds/ns-vds-vds_disk_notification)              |
| 資料分割  | **VDS \_ NF-E \_ 磁碟分割 \_ 抵達**            | 11    | [**VDS \_ 分割區 \_ 通知**](/windows/desktop/api/Vds/ns-vds-vds_partition_notification)    |
| 資料分割  | **VDS \_ NF-E \_ 分割 \_ 區**            | 12    | [**VDS \_ 分割區 \_ 通知**](/windows/desktop/api/Vds/ns-vds-vds_partition_notification)    |
| 資料分割  | **VDS \_ NF-E \_ 磁碟分割 \_ 修改**            | 13    | [**VDS \_ 分割區 \_ 通知**](/windows/desktop/api/Vds/ns-vds-vds_partition_notification)    |
| Subsystem  | **VDS \_ NF-E \_ \_ 系統 \_ 抵達**          | 101   | [**VDS \_ 子系統 \_ 系統 \_ 通知**](/windows/desktop/api/Vds/ns-vds-vds_sub_system_notification) |
| Subsystem  | **VDS \_ NF-E \_ \_ 系統的 \_ 起飛**          | 102   | [**VDS \_ 子系統 \_ 系統 \_ 通知**](/windows/desktop/api/Vds/ns-vds-vds_sub_system_notification) |
| Subsystem  | **VDS \_ NF-E \_ \_ 系統 \_ 修改**          | 151   | [**VDS \_ 子系統 \_ 系統 \_ 通知**](/windows/desktop/api/Vds/ns-vds-vds_sub_system_notification) |
| 控制器 | **VDS \_ NF-E \_ 控制器 \_ 抵達**           | 103   | [**VDS \_ 控制器 \_ 通知**](/windows/desktop/api/Vds/ns-vds-vds_controller_notification)  |
| 控制器 | **VDS \_ NF-E \_ 控制器 \_ 起飛**           | 104   | [**VDS \_ 控制器 \_ 通知**](/windows/desktop/api/Vds/ns-vds-vds_controller_notification)  |
| 控制器 | **VDS \_ NF-E \_ 控制器 \_ 修改**           | 350   | [**VDS \_ 控制器 \_ 通知**](/windows/desktop/api/Vds/ns-vds-vds_controller_notification)  |
| 控制器 | **\_ \_ 已移除 VDS NF-E 控制器 \_**          | 351   | [**VDS \_ 控制器 \_ 通知**](/windows/desktop/api/Vds/ns-vds-vds_controller_notification)  |
| 連接埠       | **VDS \_ NF-E \_ 埠 \_ 修改**                 | 352   | [**VDS \_ 埠 \_ 通知**](/windows/desktop/api/Vds/ns-vds-vds_port_notification)              |
| 連接埠       | **\_ \_ 已移除 VDS NF-E 埠 \_**                | 353   | [**VDS \_ 埠 \_ 通知**](/windows/desktop/api/Vds/ns-vds-vds_port_notification)              |
| 磁碟機      | **VDS \_ NF-E \_ 磁片磁碟機 \_ 抵達**                | 105   | [**VDS \_ 磁片磁碟機 \_ 通知**](/windows/desktop/api/Vds/ns-vds-vds_drive_notification)            |
| 磁碟機      | **VDS \_ NF-E \_ 磁片磁碟機 \_**                | 106   | [**VDS \_ 磁片磁碟機 \_ 通知**](/windows/desktop/api/Vds/ns-vds-vds_drive_notification)            |
| 磁碟機      | **VDS \_ NF-E \_ 磁片磁碟機 \_ 修改**                | 107   | [**VDS \_ 磁片磁碟機 \_ 通知**](/windows/desktop/api/Vds/ns-vds-vds_drive_notification)            |
| 磁碟機      | **\_已移除 VDS 的 NF-E \_ 磁片磁碟機 \_**               | 354   | [**VDS \_ 磁片磁碟機 \_ 通知**](/windows/desktop/api/Vds/ns-vds-vds_drive_notification)            |
| LUN        | **VDS \_ NF-E \_ LUN \_ 抵達**                  | 108   | [**VDS \_ LUN \_ 通知**](/windows/desktop/api/Vds/ns-vds-vds_lun_notification)                |
| LUN        | **VDS \_ NF-E \_ LUN \_ 部門**                  | 109   | [**VDS \_ LUN \_ 通知**](/windows/desktop/api/Vds/ns-vds-vds_lun_notification)                |
| LUN        | **VDS \_ NF-E \_ LUN \_ 修改**                  | 110   | [**VDS \_ LUN \_ 通知**](/windows/desktop/api/Vds/ns-vds-vds_lun_notification)                |



 

VDS 會產生剩餘的通知。 下表依類別列出以服務為基礎的通知常數。



| 類別     | 通知                                | 值 | 事件描述的連結                                                 |
|--------------|---------------------------------------------|-------|---------------------------------------------------------------------------|
| 磁碟         | **VDS \_ NF-E \_ 磁片 \_ 送達**                   | 8     | [**VDS \_ 磁片 \_ 通知**](/windows/desktop/api/Vds/ns-vds-vds_disk_notification)                  |
| 磁碟         | **VDS \_ NF-E \_ 磁片 \_ 部門**                   | 9     | [**VDS \_ 磁片 \_ 通知**](/windows/desktop/api/Vds/ns-vds-vds_disk_notification)                  |
| 磁碟         | **VDS \_ NF-E \_ 磁片 \_ 修改**                   | 10    | [**VDS \_ 磁片 \_ 通知**](/windows/desktop/api/Vds/ns-vds-vds_disk_notification)                  |
| 磁碟機代號 | **VDS \_ NF-E \_ 磁碟機 \_ 號 \_ 可用**            | 201   | [**VDS \_ 磁碟機 \_ 號 \_ 通知**](/windows/desktop/api/Vds/ns-vds-vds_drive_letter_notification) |
| 磁碟機代號 | **VDS \_ NF-E \_ 磁碟機 \_ 號 \_ 指派**          | 202   | [**VDS \_ 磁碟機 \_ 號 \_ 通知**](/windows/desktop/api/Vds/ns-vds-vds_drive_letter_notification) |
| 檔案系統  | **VDS \_ NF-E \_ 檔 \_ 系統 \_ 修改**           | 203   | [**VDS \_ 檔 \_ 系統 \_ 通知**](/windows/desktop/api/Vds/ns-vds-vds_file_system_notification)   |
| 檔案系統  | **VDS \_ NF-E \_ 檔 \_ 系統 \_ 格式 \_ 進度** | 204   | [**VDS \_ 檔 \_ 系統 \_ 通知**](/windows/desktop/api/Vds/ns-vds-vds_file_system_notification)   |
| 磁碟區       | **VDS \_ NF-E \_ 裝入 \_ 點 \_ 變更**          | 205   | [**VDS \_ 裝入 \_ 點 \_ 通知**](/windows/desktop/api/Vds/ns-vds-vds_mount_point_notification)   |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[VDS 物件模型](vds-object-model.md)
</dt> <dt>

[**IVdsAdviseSink**](/windows/desktop/api/Vds/nn-vds-ivdsadvisesink)
</dt> <dt>

[**IVdsAdviseSink：： OnNotify**](/windows/desktop/api/Vds/nf-vds-ivdsadvisesink-onnotify)
</dt> <dt>

[**IVdsProviderPrivate：： OnLoad**](/windows/desktop/api/VdsHwPrv/nf-vdshwprv-ivdsproviderprivate-onload)
</dt> <dt>

[**IVdsService：： Advise**](/windows/desktop/api/Vds/nf-vds-ivdsservice-advise)
</dt> </dl>

 

 
