---
description: 控制器埠物件
ms.assetid: 5f94bcdc-93ab-4522-88bd-009a049b5dc9
title: 控制器埠物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7547581358bd79212b1093384ce1589e331f6ee0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974023"
---
# <a name="controller-port-object"></a>控制器埠物件

\[從 Windows 8 和 Windows Server 2012 開始， [虛擬磁碟服務](virtual-disk-service-portal.md) COM 介面會被 [Windows 儲存體管理 API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)取代。\]

控制器埠物件會建立子系統中控制器埠的模型。 主機電腦可以透過控制器埠寫入和讀取 Lun。 控制器埠是由子系統中的控制器所包含。 在 VDS 1.1 和 VDS 2.0 中，每個子系統的控制器埠都會設定為 [作用中] 或 [非使用中] （相對於子系統所呈現的每個 Lun）。 然後，單一控制器埠可以同時設定為 [作用中]，讓某個 LUN 與其他 LUN 保持為作用中狀態。 針對指定 LUN 使用的控制器埠，負責處理 LUN 的輸入和輸出。

作用中控制器埠可作為光纖通道硬體提供者中 MPIO 路徑的其中一個端點，可在此設定負載平衡原則。

使用 [**IVdsControllerControllerPort：： QueryControllerPorts**](/windows/desktop/api/Vds/nf-vds-ivdscontrollercontrollerport-querycontrollerports) 方法來判斷特定控制器所包含的控制器埠。 呼叫端可以從 **QueryControllerPorts** 方法所傳回的列舉中選取所需的控制器埠物件，以取得特定控制器埠的指標。 使用控制器物件，呼叫端可以設定控制器埠狀態，並查詢其相關聯的 Lun。

控制器物件屬性包括物件識別碼、名稱、序號和控制器埠狀態。

下表列出相關的介面、列舉和結構。



| 類型                                                                                              | 元素                                                                                               |
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| 只有在 VDS 1.1 和2.0 光纖通道提供者中，此物件一律公開的介面 | [**IVdsControllerPort**](/windows/desktop/api/Vds/nn-vds-ivdscontrollerport)                                                      |
| 相關聯的列舉                                                                           | [**VDS \_ 埠 \_ 狀態**](/windows/desktop/api/Vds/ne-vds-vds_port_status)                                                          |
| 相關聯的結構                                                                             | [**VDS \_埠 \_**](/windows/desktop/api/Vds/ns-vds-vds_port_prop)和 [ **VDS \_ 埠 \_ 通知**](/windows/desktop/api/Vds/ns-vds-vds_port_notification) |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[硬體提供者物件](hardware-provider-objects.md)
</dt> <dt>

[**IVdsControllerControllerPort::QueryControllerPorts**](/windows/desktop/api/Vds/nf-vds-ivdscontrollercontrollerport-querycontrollerports)
</dt> </dl>

 

 
