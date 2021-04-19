---
description: LUN 物件
ms.assetid: ea22bd6d-4a7a-4674-82e9-08460914ff8e
title: LUN 物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad74fa65802adb1439360fb2fcdb423c642ef736
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997982"
---
# <a name="lun-object"></a>LUN 物件

\[從 Windows 8 和 Windows Server 2012 開始， [虛擬磁碟服務](virtual-disk-service-portal.md) COM 介面會被 [Windows 儲存體管理 API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)取代。\]

LUN (邏輯單元編號) 物件會將由硬體提供者所建立並由子系統所呈現之可定址儲存空間的邏輯單元建立模型。 每個 LUN 都包含至少一個 LUN plex，而後者又是由一或多個磁片磁碟機的範圍所組成。

## <a name="lun-types"></a>LUN 類型

VDS 支援五種 LUN 類型：簡單、跨距、等量、鏡像，以及具有同位的等量。 簡單、跨區和等量 Lun 都不能容錯;鏡像和同位 Lun 具有容錯能力。 本節的其餘部分將說明每個 VDS LUN 類型。

-   簡單的 LUN 是一種非容錯 LUN，由單一磁片磁碟機的單一連續磁片磁碟機範圍組成。 連續的範圍可以由單一區塊範圍或連結在一起的多個區塊範圍所組成。
-   跨距 LUN 是非容錯 LUN，由多個磁片磁碟機的多個不連續範圍所組成。 資料會以線性方式寫入第一個磁片磁碟機上的每個範圍，直到所有第一個磁片區的範圍填滿，然後再填滿第二個磁片磁碟機上的每個範圍等等。 跨距 Lun 可有效地使用子系統中的磁片磁碟機空間，這些子系統包含各種不同大小的磁片磁碟機。
-   等量 LUN 是非容錯 LUN，由多個磁片磁碟機的多個交錯、連續的範圍所組成。 等量 Lun 使用 RAID-0 設定，因此資料會在參與磁片磁碟機的範圍中「等量」迴圈。 等量 Lun 最適合與相同大小、型號和製造商的磁片磁碟機搭配使用。
-   鏡像 Lun 是容錯 Lun，藉由將資料複製到多個 LUN 的 plex 來提供嚴重損壞修復。 鏡像 LUN 中的每個 plex 都包含一份儲存在原始 plex 上的資料複本。 每個 plex 都位於不同的磁片磁碟機上。 寫入至鏡像 LUN 的所有資料都會同時寫入至它的每個 plex。 如果其中一部參與的磁片磁碟機失敗，則該磁片磁碟機上的 plex 會變成無法使用，但系統會使用不受影響的 plex 或 plex 繼續運作。 鏡像的 LUN 可以有任意數目的 plex。
-   具有同位 Lun 的等量是容錯 Lun，可透過在三個或更多磁片磁碟機上間歇性分割的同位資料來提供嚴重損壞修復。 如果其中一部參與的磁片磁碟機失敗，則可以從剩餘的資料和同位重新建立遺失的資料。

## <a name="lun-creation"></a>LUN 建立

VDS 支援四個可讓應用程式建立 Lun 的模型：明確導向、部分導向、automagic 和供應商特定。 所有硬體提供者都必須支援明確且部分導向的 LUN 建立，且強烈建議您支援 automagic LUN 建立。  (廠商特定的 LUN 建立超出本指南的範圍。 ) 

明確導向的 LUN 建立可讓呼叫者指定 LUN 的所有屬性。 部分導向的 LUN 建立可讓呼叫者只指定特別感興趣的屬性，然後允許提供者選擇其餘部分。 Automagic LUN 的建立牽涉到讓呼叫者只需指定 LUN 類型和大小，以及一組「Automagic 提示」 (預先定義的 LUN 屬性) ，然後允許提供者自動建立 LUN。

## <a name="lun-masking"></a>LUN 遮罩

VDS 針對提供這項功能的子系統支援 LUN 取消遮罩。 所有 Lun 都會呈現給執行提供者的電腦。 LUN 取消遮罩可讓呼叫者將選取的 Lun 「取消遮罩」至網路上的其他電腦。 如果您將 LUN 取消遮罩至電腦，電腦就可以存取 LUN。 LUN 遮罩的電腦不會。

未遮罩的 LUN 會將 [**IVdsLun**](/windows/desktop/api/Vds/nn-vds-ivdslun) 和 [**IVdsDisk**](/windows/desktop/api/Vds/nn-vds-ivdsdisk) 介面公開給本機主機。 您可以使用 **IVdsDisk** 將 LUN 新增至軟體提供者套件、建立和移除磁片區、指派磁碟機號等等。 如需在磁片上執行之作業的詳細資訊，請參閱 [Disk 物件](disk-object.md)。

將 LUN 取消遮罩至目的電腦或從目的電腦遮罩之後，該電腦上的 LUN 可見度在執行匯流排重新掃描之前可能不會變更。 目的電腦上的 VDS 應用程式會藉由呼叫 [**IVdsService：： Reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate)起始匯流排重新掃描。 起始匯流排重新掃描是 VDS 應用程式（而不是硬體提供者）的責任。

## <a name="lun-multipathing"></a>LUN 多重路徑

支援多重路徑 i/o (MPIO) 的硬體提供者可以在 LUN 與本機主機之間的路徑上設定負載平衡原則。 支援這項功能的 Lun 會向本機主機公開 [**IVdsLunMpio**](/windows/desktop/api/Vds/nn-vds-ivdslunmpio) 介面。

## <a name="working-with-luns"></a>使用 Lun

使用 [**IVdsSubSystem：： CreateLun**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-createlun) 方法來建立新的 LUN 物件。 您可以藉由叫用 [**QueryLuns**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-queryluns) 方法（也會由 [**IVdsSubSystem**](/windows/desktop/api/Vds/nn-vds-ivdssubsystem)公開）來查詢特定子系統所呈現的 lun。 呼叫端可以從 **QueryLuns** 傳回的列舉中選取所需的 lun 物件，以取得特定 lun 的指標。 您可以使用 LUN 物件來設定 LUN 狀態;查詢所有作用中控制器、plex 和 automagic 提示;擴充和壓縮 LUN;新增和移除 plex;設定遮罩;套用提示;並刪除 LUN。

除了物件識別碼、名稱和序號之外，LUN 物件屬性還包括 LUN 類型、大小、狀態、健康情況、轉換狀態和旗標;取消遮罩清單;以及重建優先權設定。

下表列出相關的介面、列舉和結構。



| 類型                                                                                              | 元素                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 一律由這個物件公開的介面                                                 | [**IVdsLun**](/windows/desktop/api/Vds/nn-vds-ivdslun)                                                                                                                                                                                                                                                                                          |
| 只有在 VDS 1.1 和2.0 光纖通道提供者中，此物件一律公開的介面 | [**IVdsLunControllerPorts**](/windows/desktop/api/Vds/nn-vds-ivdsluncontrollerports)                                                                                                                                                                                                                                                            |
| 只有在 VDS 1.1 和 2.0 iSCSI 提供者中，此物件一律公開的介面         | [**IVdsLunIscsi**](/windows/desktop/api/Vds/nn-vds-ivdsluniscsi)                                                                                                                                                                                                                                                                                |
| 此物件可能公開的介面\*                                                   | [**IVdsMaintenance**](/windows/desktop/api/Vds/nn-vds-ivdsmaintenance)、 [**IVdsLunMpio**](/windows/desktop/api/Vds/nn-vds-ivdslunmpio)、 [**IVdsLunNaming**](/windows/desktop/api/Vds/nn-vds-ivdslunnaming)和 [**IVdsLunNumber**](/windows/desktop/api/Vds/nn-vds-ivdslunnumber)**windows server 2008、Windows Vista 和 windows server 2003：** 不支援 [**IVdsLunNumber**](/windows/desktop/api/Vds/nn-vds-ivdslunnumber) 介面。<br/> |
| 相關聯的列舉                                                                           | [**VDS \_LUN \_ 旗**](/windows/desktop/api/Vds/ne-vds-vds_lun_flag) 標和 [**vds \_ Lun \_ 狀態**](/windows/desktop/api/Vds/ne-vds-vds_lun_status)，以及 [**vds \_ lun \_ 類型**](/windows/desktop/api/Vds/ne-vds-vds_lun_type)                                                                                                                                                                                   |
| 相關聯的結構                                                                             | [**VDS \_LUN \_ 資訊**](/windows/desktop/api/VdsLun/ns-vdslun-vds_lun_information)、 [**Vds \_ lun \_**](/windows/desktop/api/Vds/ns-vds-vds_lun_prop)和 [**vds \_ lun \_ 通知**](/windows/desktop/api/Vds/ns-vds-vds_lun_notification)                                                                                                                                                            |



 

\* 請參閱 [磁片物件](disk-object.md) 以取得額外介面 ([**IVdsDisk**](/windows/desktop/api/Vds/nn-vds-ivdsdisk)) ，此介面會在 LUN 以本機主機電腦上的磁片取消遮罩時公開。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[硬體提供者物件](hardware-provider-objects.md)
</dt> <dt>

[Pack 物件](pack-object.md)
</dt> <dt>

[磁片物件](disk-object.md)
</dt> <dt>

[**IVdsLun**](/windows/desktop/api/Vds/nn-vds-ivdslun)
</dt> <dt>

[**IVdsDisk**](/windows/desktop/api/Vds/nn-vds-ivdsdisk)
</dt> <dt>

[將磁碟機號新增至 LUN](adding-a-drive-letter-to-a-lun.md)
</dt> </dl>

 

