---
description: Reenumerating 和重新整理
ms.assetid: 67d34946-47df-43e2-8ca7-628d0671b869
title: Reenumerating 和重新整理
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42f19d28d44234b773988f3038666212caf447fb45dee39435b0d99169f92212
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118125918"
---
# <a name="reenumerating-and-refreshing"></a>Reenumerating 和重新整理

\[從 Windows 8 和 Windows Server 2012 開始， [Windows 儲存體管理 API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)會取代[虛擬磁碟服務](virtual-disk-service-portal.md)COM 介面。\]

Reenumeration 作業會探索新連線和最近中斷連線的裝置。 重新整理作業會更新現有裝置的設定資訊。

**Reenumerate 軟體提供者物件**

-   呼叫 [**IVdsService：： Reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate) 方法。 此方法會探索所有新連線和已中斷連線的磁片和 CD-ROM 光碟機，並確保所有磁片都具有適當的擁有者。 VDS 擁有原始磁片或失敗的磁片;基本提供者擁有基本磁碟;而且動態提供者擁有動態磁碟。 這種作業可能牽涉到掃描內部子系統匯流排，以及等待超時時間。

**Reenumerate 和重新整理軟體提供者物件**

-   呼叫 [**IVdsService：： Reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate) 方法，然後呼叫 [**IVdsService：： Refresh**](/windows/desktop/api/Vds/nf-vds-ivdsservice-refresh) 方法。 除了探索新連接和中斷連接的磁片和 CD-ROM 光碟機之外，此方法的組合也會針對尚未最近連線或中斷連線的磁片，更新 VDS 快取中的所有磁片、磁片區和 plex 資訊。 單獨呼叫 **refresh** 以重新整理快取中現有物件的屬性資訊。 這種作業可能牽涉到掃描內部子系統匯流排，以及等待超時時間。 請注意，當觸發通知的變更發生時，VDS 會自動更新快取。 此外 **，呼叫重新** 整理以回應 VDS 通知可能會導致傳送無限迴圈的通知。 基於這些理由，只有在出現快取未正確更新時，才應該呼叫 **Refresh** 。

**Reenumerate 硬體子系統**

-   呼叫 [**IVdsHwProvider：： Reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdshwprovider-reenumerate) 方法。 視提供者而定，此作業可能牽涉到傳送網路封包，並等候超時時間、重新掃描 SCSI 匯流排，以及等待超時等等。

**Reenumerate 硬體子系統物件**

-   呼叫 [**IVdsSubSystem：： Reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-reenumerate) 方法來清查物件 (通常會驅動子系統) 。 視子系統而定，此作業可能牽涉到掃描內部子系統匯流排，以及等待超時時間。

**重新整理硬體子系統和子系統物件**

-   呼叫 [**IVdsHwProvider：： refresh**](/windows/desktop/api/Vds/nf-vds-ivdshwprovider-refresh) 方法，以重新整理 vds 硬體提供者所管理之現有子系統的相關資訊。 請注意，當觸發通知的變更發生時，VDS 會自動更新快取。 此外 [**，呼叫重新**](/windows/desktop/api/Vds/nf-vds-ivdsservice-refresh) 整理以回應 VDS 通知可能會導致傳送無限迴圈的通知。 基於這些理由，只有在出現快取未正確更新時，才應該呼叫 **Refresh** 。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 VDS](using-vds.md)
</dt> <dt>

[**IVdsService::Reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate)
</dt> <dt>

[**IVdsService：： Refresh**](/windows/desktop/api/Vds/nf-vds-ivdsservice-refresh)
</dt> <dt>

[**IVdsHwProvider::Reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdshwprovider-reenumerate)
</dt> <dt>

[**IVdsSubSystem::Reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-reenumerate)
</dt> <dt>

[**IVdsHwProvider：： Refresh**](/windows/desktop/api/Vds/nf-vds-ivdshwprovider-refresh)
</dt> </dl>

 

 
