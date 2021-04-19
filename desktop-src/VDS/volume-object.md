---
description: 磁片區物件
ms.assetid: 92013015-b0f5-4b92-937b-c2637f65810c
title: 磁片區物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e47092a237e7b0e9441b08c410d95d0836dbdb7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985155"
---
# <a name="volume-object"></a>磁片區物件

\[從 Windows 8 和 Windows Server 2012 開始， [虛擬磁碟服務](virtual-disk-service-portal.md) COM 介面會被 [Windows 儲存體管理 API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)取代。\]

磁片區物件會建立軟體提供者所建立之邏輯儲存體單位的模型，並以磁片的形式呈現給檔案系統。 每個磁片區都包含至少一個磁片區 plex，而該磁片區是由一或多個磁片的範圍所組成。

## <a name="volume-types"></a>磁碟區類型

VDS 支援五種磁片區類型：簡單、跨距、等量、鏡像，以及具有同位的等量。 簡單、跨距和等量磁片區無法容錯;鏡像和同位磁片區具有容錯能力。 本節的其餘部分將說明每個 VDS 磁片區類型。

-   簡單磁片區是實體磁片的一部分，其運作方式就如同實際的個別單元一樣。 簡單磁碟區可以包含磁碟上的單一區域，或是同一個磁碟中互相連結的多重區域。
-   跨距磁片區會將多個磁片的未配置空間區域結合為一個邏輯磁片區，讓您更有效率地使用多磁片系統上的所有空間和所有磁碟機號。
-   建立等量磁片區的方式是將兩個或多個磁片上的可用空間區域組合成一個邏輯磁片區。 等量磁片區使用 RAID-0，這會將資料分割到多個磁片上。 等量磁片區無法擴充或鏡像，且不提供容錯功能。 如果其中一個包含等量磁片區的磁片失敗，整個磁片區將會失敗。 建立等量磁片區時，最好使用大小、型號和製造商相同的磁片。
-   鏡像磁片區是一種容錯磁片區，可使用磁片區的兩個複本（或 plex）來複製儲存在磁片區上的資料，藉此提供資料冗余。 寫入至鏡像磁片區的所有資料都會寫入至位於不同實體磁片上的 plex。 如果其中一個實體磁片失敗，則故障磁片上的資料會變成無法使用，但系統會使用未受影響的磁片繼續運作。
-   具有同位檢查磁片區的等量是容錯磁片區，其中的資料和同位會間歇性地跨三個或多個實體磁片。 如果實體磁片的一部分故障，您可以從剩餘的資料和同位重新建立失敗部分的資料。 此磁片區類型 (也稱為 RAID-5 磁片區) 在大部分活動都包含讀取資料的電腦環境中，這是很好的資料冗余解決方案。

### <a name="volume-creation"></a>磁片區建立

基本和動態軟體提供者支援部分導向的磁片區建立;呼叫端只會指定特別感興趣的屬性，並允許提供者選擇其餘部分。 VDS 會自動掛接新建立的磁片區，但 Windows Server 2003、Enterprise Edition 和 Windows Server 2003、Datacenter Edition 平臺除外。

### <a name="working-with-volumes"></a>使用磁片區

一律在與提供給它的磁片相同的套件中建立磁片區。 使用 [**IVdsPack：： CreateVolume**](/windows/desktop/api/Vds/nf-vds-ivdspack-createvolume) 方法來建立新的磁片區物件。 您可以叫用 [**QueryVolumes**](/windows/desktop/api/Vds/nf-vds-ivdspack-queryvolumes) 方法（也會由 [**IVdsPack**](/windows/desktop/api/Vds/nn-vds-ivdspack)公開），以判斷包含在特定套件內的磁片區。 呼叫端可以從 **QueryVolumes** 傳回的列舉中選取所需的磁片區物件，以取得特定磁片區的指標。 使用磁片區物件，您可以設定狀態;針對 plex 進行查詢;擴充和壓縮磁片區;新增、中斷和移除 plex;並刪除磁片區。

除了物件識別碼、名稱和序號之外，磁片區物件屬性還包括磁片區類型、大小、狀態、健康情況、轉換狀態、旗標，以及建議的檔案系統類型。

下表列出相關的介面、列舉和結構。



| 類型                                              | 元素                                                                                                                                                                                                               |
|---------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 一律由這個物件公開的介面 | [**IVdsVolume**](/windows/desktop/api/Vds/nn-vds-ivdsvolume)、 [**IVdsVolumeMF**](/windows/desktop/api/Vds/nn-vds-ivdsvolumemf)、 [**IVdsVolumeMF2**](/windows/desktop/api/Vds/nn-vds-ivdsvolumemf2) \* 、 [**IVdsVolumeOnline**](/windows/desktop/api/Vds/nn-vds-ivdsvolumeonline) \* 和 [**IVdsVolumeShrink**](/windows/desktop/api/Vds/nn-vds-ivdsvolumeshrink) \* 。 |
| 相關聯的列舉                           | [**VDS \_磁片區 \_ 旗標**](/windows/desktop/api/Vds/ne-vds-vds_volume_flag)、vds 磁片區 [**\_ \_ 狀態**](/windows/desktop/api/Vds/ne-vds-vds_volume_status)、Vds 磁片區 [**\_ \_ 類型**](/windows/desktop/api/Vds/ne-vds-vds_volume_type)，以及 [**vds \_ 磁片 \_ 區 \_ 類型**](/windows/desktop/api/Vds/ne-vds-vds_disk_extent_type)。            |
| 相關聯的結構                             | [**VDS \_磁片 \_**](/windows/desktop/api/Vds/ns-vds-vds_volume_prop) 區和 [**VDS \_ 大量 \_ 通知**](/windows/desktop/api/Vds/ns-vds-vds_volume_notification)。                                                                                                        |



 

**\* Windows Server 2003：** 在 windows Vista 之前，不支援這些介面。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[軟體提供者物件](software-provider-objects.md)
</dt> </dl>

 

 
