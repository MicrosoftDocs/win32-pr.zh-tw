---
description: 軟體提供者物件
ms.assetid: 0d415238-7558-4d90-a122-e65ae7760344
title: 軟體提供者物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 507abb00b67b51ad68eb0592ff4fa7b5201cff5be0587b7170662556238feb50
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119137153"
---
# <a name="software-provider-objects"></a>軟體提供者物件

\[從 Windows 8 和 Windows Server 2012 開始， [Windows 儲存體管理 API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)會取代[虛擬磁碟服務](virtual-disk-service-portal.md)COM 介面。\]

軟體提供者物件會建立實體裝置的模型，例如 IDE 磁片和 CD-ROM，以及套件、磁片區和磁片區 plex 等虛擬元素。 下圖顯示提供者物件與一組軟體提供者物件之間的關聯性，以及各種軟體提供者物件本身之間的關聯性。

![顯示「提供者」與「軟體提供者」物件之間關聯性的圖表，例如「套件」和「磁片區」。](images/vdsswobjects.png)

提供者物件可以包含零或多個套件。 套件物件可以包含零或多個磁片與磁片區。 磁片區是由至少一個磁片區 plex 所組成，且每個磁片區 plex 都可以對應至一或多個磁片（視 plex 類型而定）。 VDS 直接管理未配置的磁片，沒有套件容器。 本節的其餘主題描述套件、磁片、磁片區和磁片區 plex 物件。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[VDS 物件模型](vds-object-model.md)
</dt> </dl>

 

 
