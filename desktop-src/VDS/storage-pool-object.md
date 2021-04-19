---
description: 儲存集區物件會在儲存子系統中建立存放集區的模型。
ms.assetid: a6104742-3ef9-4570-9728-3e6580953117
title: 存放集區物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c44719b825193faa75546ba1a0f7b42155a3e49
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997972"
---
# <a name="storage-pool-object"></a>存放集區物件

\[從 Windows 8 和 Windows Server 2012 開始， [虛擬磁碟服務](virtual-disk-service-portal.md) COM 介面會被 [Windows 儲存體管理 API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)取代。\]

儲存集區物件會在儲存子系統中建立存放集區的模型。

存放集區包含一或多個由相同硬體提供者所管理之磁片磁碟機的磁片區。

下表列出相關的介面、列舉和結構。



| 類型                                              | 元素                                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 一律由這個物件公開的介面 | [**IVdsStoragePool**](/windows/desktop/api/Vds/nn-vds-ivdsstoragepool)                                                                                                                                                                                                                                                               |
| 相關聯的列舉                           | [**VDS \_RAID \_ 類型**](/windows/desktop/api/Vds/ne-vds-vds_raid_type)、 [**vds \_ 存放 \_ 集區 \_ 狀態**](/windows/desktop/api/Vds/ne-vds-vds_storage_pool_status)，以及 [**vds \_ 儲存 \_ 集區 \_ 類型**](/windows/desktop/api/Vds/ne-vds-vds_storage_pool_type)。                                                                                                                                  |
| 相關聯的結構                             | [**VDS \_HINTS2**](/windows/desktop/api/Vds/ns-vds-vds_hints2)、 [**vds \_ 集區 \_ 屬性**](/windows/desktop/api/Vds/ns-vds-vds_pool_attributes)、 [**vds 集區 \_ \_ 自訂 \_ 屬性**](/windows/desktop/api/Vds/ns-vds-vds_pool_custom_attributes)、 [**vds \_ 儲存 \_ 集 \_ \_ 區磁片區**](/windows/desktop/api/Vds/ns-vds-vds_storage_pool_drive_extent)，以及 [**vds \_ 存放 \_ 集 \_**](/windows/desktop/api/Vds/ns-vds-vds_storage_pool_prop)區的屬性。 |



 

 

 
