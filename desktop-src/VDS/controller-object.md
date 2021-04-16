---
description: 控制器物件
ms.assetid: ae2c4d47-15a6-4b9d-9165-4ee04a6ff3a8
title: 控制器物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7db9468c1ca4c8f07c5498724333bdad9fc53bf
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/04/2021
ms.locfileid: "104558854"
---
# <a name="controller-object"></a>控制器物件

\[從 Windows 8 和 Windows Server 2012 開始， [虛擬磁碟服務](virtual-disk-service-portal.md) COM 介面會被 [Windows 儲存體管理 API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)取代。\]

控制器物件會在子系統中建立控制器的模型。 控制器是由子系統所包含，而每個控制器都有一或多個控制器埠，可供主機電腦用來寫入和讀取 Lun。 單一控制器可同時設為作用中的一個 LUN，而其他則為非使用中。 作用中的指定 LUN 的控制器，負責處理 LUN 的輸入和輸出。 下圖說明這個概念。

![此圖顯示左邊有作用中 LUN 的「控制器」，以及右邊的兩個作用中 Lun。](images/vdscontroller.png)

**VDS 1.0：** 子系統的每個控制器都會設定為 [作用中] 或 [非使用中]，而不是與子系統所呈現的每個 Lun 相關。

VDS 應用程式會使用 [**IVdsSubSystem：： QueryControllers**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-querycontrollers) 方法來判斷特定子系統所包含的控制器。 呼叫端可以從 **QueryControllers** 方法所傳回的列舉中選取所需的控制器物件，以取得特定控制器的指標。 使用控制器物件時，呼叫端可以設定控制器狀態、查詢其相關聯的 Lun、查詢其控制器埠，以及排清和使快取失效。

除了物件識別碼、名稱和序號之外，控制器物件屬性還包括控制器狀態和健全狀況，以及埠的計數。

下表列出相關的介面、列舉和結構。



| 類型                                                                                              | 元素                                                                                                                        |
|---------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| 一律由這個物件公開的介面                                                 | [**IVdsController**](/windows/desktop/api/Vds/nn-vds-ivdscontroller)                                                                                       |
| 只有在 VDS 1.1 和2.0 光纖通道提供者中，此物件一律公開的介面 | [**IVdsControllerControllerPort**](/windows/desktop/api/Vds/nn-vds-ivdscontrollercontrollerport)                                                           |
| 此物件可能公開的介面                                                     | [**IVdsMaintenance**](/windows/desktop/api/Vds/nn-vds-ivdsmaintenance)                                                                                     |
| 相關聯的列舉                                                                           | [**VDS \_控制器 \_ 狀態**](/windows/desktop/api/Vds/ne-vds-vds_controller_status)。                                                                      |
| 相關聯的結構                                                                             | [**VDS \_控制器 \_**](/windows/desktop/api/Vds/ns-vds-vds_controller_prop) 的和 [**VDS \_ 控制器 \_ 通知**](/windows/desktop/api/Vds/ns-vds-vds_controller_notification)。 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[硬體提供者物件](hardware-provider-objects.md)
</dt> <dt>

[**IVdsSubSystem::QueryControllers**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-querycontrollers)
</dt> </dl>

 

 
