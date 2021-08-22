---
description: 磁片磁碟機物件
ms.assetid: c1c17a97-cf4b-45b7-bc32-4bad94c3ddb2
title: 磁片磁碟機物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d04ec68fab408c4ed6412990296c0ebb265b8c3e4c4c9b05645b1f4bd1e625fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118603418"
---
# <a name="drive-object"></a>磁片磁碟機物件

\[從 Windows 8 和 Windows Server 2012 開始， [Windows 儲存體管理 API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)會取代[虛擬磁碟服務](virtual-disk-service-portal.md)COM 介面。\]

磁片磁碟機物件會建立包含在子系統內的實體磁片磁碟機模型。 每個磁片磁碟機會連線至匯流排、佔用插槽，並包含一組磁片磁碟機範圍。 每個磁片磁碟機都可將範圍貢獻至任意數目的 Lun。 磁片磁碟機也可以指定為熱備用。

使用 [**IVdsSubSystem：： QueryDrives**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-querydrives) 方法來判斷特定子系統所包含的磁片磁碟機。 呼叫端可以取得特定磁片磁碟機的指標，方法是從 **QueryDrives** 方法所傳回的列舉中選取所需的磁片磁碟機物件，或是叫用 [**IVdsSubSystem：： GetDrive**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-getdrive) 方法，並傳入所需的匯流排和插槽號碼。 您可以使用磁片磁碟機物件，設定磁片磁碟機的狀態和查詢磁片磁碟機內容、相關聯的磁片區，以及包含該磁片磁碟機的子系統。

除了物件識別碼、名稱和序號之外，磁片磁碟機物件屬性還包括磁片磁碟機狀態、健康情況和旗標;以位元組為單位的大小;以及匯流排和插槽號碼。

下表列出相關的介面、列舉和結構。



| 類型                                              | 元素                                                                                                                                         |
|---------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| 一律由這個物件公開的介面 | [**IVdsDrive**](/windows/desktop/api/Vds/nn-vds-ivdsdrive)                                                                                                                  |
| 此物件可能公開的介面     | [**IVdsMaintenance**](/windows/desktop/api/Vds/nn-vds-ivdsmaintenance)                                                                                                      |
| 相關聯的列舉                           | [**VDS \_磁片磁碟機 \_ 旗**](/windows/desktop/api/Vds/ne-vds-vds_drive_flag)標、 [**vds \_ 磁片磁碟機 \_ 狀態**](/windows/desktop/api/Vds/ne-vds-vds_drive_status)，以及 [**vds \_ 磁片區的 \_ 範圍**](/windows/desktop/api/Vds/ns-vds-vds_drive_extent)。 |
| 相關聯的結構                             | [**VDS \_磁片 \_ 磁碟機**](/windows/desktop/api/Vds/ns-vds-vds_drive_prop) 和 [**VDS \_ 磁片磁碟機 \_ 通知**](/windows/desktop/api/Vds/ns-vds-vds_drive_notification)。                                      |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[硬體提供者物件](hardware-provider-objects.md)
</dt> <dt>

[**IVdsSubSystem::QueryDrives**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-querydrives)
</dt> <dt>

[**IVdsSubSystem::GetDrive**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-getdrive)
</dt> </dl>

 

 
