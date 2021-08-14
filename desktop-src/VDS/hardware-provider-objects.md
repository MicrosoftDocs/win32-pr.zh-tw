---
description: 硬體提供者物件
ms.assetid: d1724219-1487-485b-9c52-5003069fe9e2
title: 硬體提供者物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0c0050b6a9754b25b6a5027d9470cb2fc46911bf4ab3ef852454d1f0698a1d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118125960"
---
# <a name="hardware-provider-objects"></a>硬體提供者物件

\[從 Windows 8 和 Windows Server 2012 開始， [Windows 儲存體管理 API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)會取代[虛擬磁碟服務](virtual-disk-service-portal.md)COM 介面。\]

VDS 物件模型包含一組用來查詢和設定硬體提供者實體的物件。  (請注意，雖然 VDS 包含軟體提供者，但您必須個別購買硬體提供者和相關聯的硬體，才能利用硬體提供者物件。 ) 這些硬體提供者物件代表實體裝置 (例如子系統、磁片磁碟機和控制器) 以及虛擬裝置 (例如 Lun 和 LUN plex) 。

硬體提供者應該針對每個實體或虛擬裝置建立一個 COM 物件。

下圖顯示提供者物件與一組硬體提供者物件之間的關聯性，以及各種硬體提供者物件本身之間的關聯性。

![顯示「提供者」和「子系統」、「控制器」、「LUN」、「LUN plex」、「磁片磁碟機」和「主軸」之間關聯性的圖表。 ](images/vdshwobjects.png)

提供者物件可以包含任何數目的子系統。 所有硬體提供者都能夠管理相同子系統模型的多個實例。 許多硬體提供者也可以管理不同子系統模型的多個實例。 單一電腦可以裝載任意數量的硬體提供者。

子系統物件可以包含任意數目的控制器和磁片磁碟機，而且可以呈現任何數目的 Lun。 LUN 物件是由至少一個 LUN plex 組成，而且每個 LUN plex 都對應至一或多個磁片磁碟機（視 plex 類型而定）。 控制器物件可以管理任何數目之 LUN 物件的資料輸入/輸出。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[VDS 物件模型](vds-object-model.md)
</dt> </dl>

 

 
