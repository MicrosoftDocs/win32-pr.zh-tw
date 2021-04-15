---
description: 子系統物件
ms.assetid: f605a5de-9256-4b43-8e12-3d78fd6cd9f1
title: 子系統物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c8314a798ea809b3175377bc5484f19629094db
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/04/2021
ms.locfileid: "104560629"
---
# <a name="subsystem-object"></a>子系統物件

\[從 Windows 8 和 Windows Server 2012 開始， [虛擬磁碟服務](virtual-disk-service-portal.md) COM 介面會被 [Windows 儲存體管理 API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)取代。\]

子系統物件會建立儲存子系統的模型。 子系統可以是 RAID 主機殼或 PCI RAID 卡。 單一主機電腦可以連接至任意數目的子系統。 每個子系統只會由一個硬體提供者管理。 在 SAN 設定中，子系統類別代表 SAN 存放裝置主機殼。

子系統可以包含任意數目的控制器和磁片磁碟機，而且可以 (遮罩，) 任意數量的 Lun 寫入執行硬體提供者的電腦。 較高階的子系統可以取消遮罩 Lun 給網路上的其他電腦。 子系統內的每個磁片磁碟機都會連接至匯流排，並佔用匯流排中的插槽。 子系統內的每個控制器都有一或多個控制器埠。

下圖顯示子系統中包含的實體裝置 (Lun 不會顯示) 和它們之間的關聯性。

![此圖表會顯示從左側的「埠」開始、移至「控制器」，然後將「插槽」指向個別「磁片磁碟機」的「匯流排」。](images/vdssubsystem.png)

VDS 應用程式使用 [**IVdsHwProvider：： QuerySubSystems**](/windows/desktop/api/Vds/nf-vds-ivdshwprovider-querysubsystems) 方法來查詢屬於特定硬體提供者的子系統。 呼叫端可以從 **QuerySubSystems** 方法所傳回的列舉中選取所需的子系統物件，以取得特定子系統的指標。 使用子系統物件，您可以設定子系統狀態、建立 Lun、更換磁片磁碟機，以及查詢控制器、磁片磁碟機和 Lun。

除了物件識別碼、名稱和序號之外，子系統物件屬性還包括子系統狀態、健全狀況和旗標;控制器、插槽和匯流排的計數;以及重建優先權設定。

下表列出相關的介面、列舉和結構。



| 類型                                                                                      | 元素                                                                                                                          |
|-------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| 一律由這個物件公開的介面                                         | [**IVdsSubSystem**](/windows/desktop/api/Vds/nn-vds-ivdssubsystem)。                                                                                          |
| 只有在 VDS 1.1 和 2.0 iSCSI 提供者中，此物件一律公開的介面 | [**IVdsSubSystemIscsi**](/windows/desktop/api/Vds/nn-vds-ivdssubsystemiscsi) 和 [**IVdsSubSystemImportTarget**](/windows/desktop/api/Vds/nn-vds-ivdssubsystemimporttarget)。             |
| 此物件可能公開的介面                                             | [**IVdsSubSystemNaming**](/windows/desktop/api/Vds/nn-vds-ivdssubsystemnaming) 和 [**IVdsMaintenance**](/windows/desktop/api/Vds/nn-vds-ivdsmaintenance)。                               |
| 相關聯的列舉                                                                   | [**VDS \_SUB \_ system \_ 旗**](/windows/desktop/api/Vds/ne-vds-vds_sub_system_flag) 標和 [**VDS \_ sub \_ system \_ STATUS**](/windows/desktop/api/Vds/ne-vds-vds_sub_system_status)。             |
| 相關聯的結構                                                                     | [**VDS \_子 \_ 系統的 \_ 主張**](/windows/desktop/api/Vds/ns-vds-vds_sub_system_prop) 和 [**VDS \_ 子 \_ 系統 \_ 通知**](/windows/desktop/api/Vds/ns-vds-vds_sub_system_notification)。 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[硬體提供者物件](hardware-provider-objects.md)
</dt> <dt>

[**IVdsHwProvider::QuerySubSystems**](/windows/desktop/api/Vds/nf-vds-ivdshwprovider-querysubsystems)
</dt> </dl>

 

 
