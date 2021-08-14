---
description: 磁片區 Plex 物件
ms.assetid: 9e770bfc-2bcb-45f0-a7fc-ba526349839e
title: 磁片區 Plex 物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c140cbf50e1939be7f62499aa90a299e07c157cd22b1a2e039e5e7bb2053b497
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118603023"
---
# <a name="volume-plex-object"></a>磁片區 Plex 物件

\[從 Windows 8 和 Windows Server 2012 開始， [Windows 儲存體管理 API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)會取代[虛擬磁碟服務](virtual-disk-service-portal.md)COM 介面。\]

磁片區 plex 物件會建立磁片區所包含的磁片區 plex 模型。 只有鏡像磁片區可以有多個 plex;所有其他磁片區類型都有一個 plex。 每個 plex 都包含磁片區上的資料複本。 VDS 支援四個磁片區的磁片區 plex 類型：簡單、跨距、等量和同位檢查。 如需這些磁片區類型的說明，請參閱 [磁片區物件](volume-object.md)。

有兩種方式可以建立具有多個 plex 的磁片區。 您可以使用 [**IVdsPack：： CreateVolume**](/windows/desktop/api/Vds/nf-vds-ivdspack-createvolume) 方法直接建立鏡像磁片區，或使用 [**IVdsVolume：： AddPlex**](/windows/desktop/api/Vds/nf-vds-ivdsvolume-addplex) 方法將一個磁片區新增到另一個磁片區。 磁片區 (以及基礎磁片) 必須位於相同的套件中。 下圖顯示一個範例，說明如何將一個磁片區 (B) 做為) 的另一個 (磁片區，以及產生的多工磁片區 () 。 磁片區 A 上的資料會保持不變，而磁片區 B 上的資料會變成磁片區 A 上的鏡像資料複本。

![顯示兩個單一 plex 的圖表，一個具有簡單磁片區 A，另一個具有簡單磁片區 B，等於具有鏡像磁片區 A 的多重 plex。](images/vdsplex.png)

您可以藉由叫用 [**IVdsVolume：： QueryPlexes**](/windows/desktop/api/Vds/nf-vds-ivdsvolume-queryplexes) 方法來查詢磁片區的 plex。 您可以從 **QueryPlexes** 傳回的列舉中選取所需的 plex 物件，以取得特定磁片區 plex 的指標。 除了最後一個 plex 之外，現有的 plex 也可以中斷或移除。 使用 [**IVdsVolume：： BreakPlex**](/windows/desktop/api/Vds/nf-vds-ivdsvolume-breakplex) 從磁片區分割一個 plex，然後將中斷的 plex 物件轉換成磁片區物件。 使用 [**IVdsVolume：： RemovePlex**](/windows/desktop/api/Vds/nf-vds-ivdsvolume-removeplex) 可完全刪除該 plex。 您可以藉由呼叫 [**IVdsVolumePlex：： repair**](/windows/desktop/api/Vds/nf-vds-ivdsvolumeplex-repair) 方法，將錯誤的成員移至良好的磁片，藉以嘗試修復容錯叢。

除了物件識別碼和 plex 類型之外，磁片區 plex 物件屬性還包括 plex 的狀態、健全狀況和轉換狀態。 此物件沒有旗標。

下表列出相關的介面、列舉和結構。



| 類型                                              | 元素                                                                                                                                                                            |
|---------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 一律由這個物件公開的介面 | [**IVdsVolumePlex**](/windows/desktop/api/Vds/nn-vds-ivdsvolumeplex)。                                                                                                                                          |
| 相關聯的列舉                           | [**VDS \_磁片區 \_ PLEX \_ 狀態**](/windows/desktop/api/Vds/ne-vds-vds_volume_plex_status)、vds 磁片區 [**\_ \_ plex \_ 類型**](/windows/desktop/api/Vds/ne-vds-vds_volume_plex_type)，以及 [**VDS \_ 磁片 \_ 區 \_ 類型**](/windows/desktop/api/Vds/ne-vds-vds_disk_extent_type)。 |
| 相關聯的結構                             | [**VDS \_磁片 \_ 區 \_ PLEX**](/windows/desktop/api/Vds/ns-vds-vds_volume_plex_prop)的大小。                                                                                                                           |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[軟體提供者物件](software-provider-objects.md)
</dt> <dt>

[磁片區物件](volume-object.md)
</dt> </dl>

 

 
