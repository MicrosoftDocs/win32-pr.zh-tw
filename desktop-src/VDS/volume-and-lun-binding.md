---
description: 磁片區和 LUN 系結
ms.assetid: ae32b354-799e-4f9b-8989-02bd95968210
title: 磁片區和 LUN 系結
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c9f62e599f5b5e457a1ce6dbf6a52524d1b80d1
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/04/2021
ms.locfileid: "104195652"
---
# <a name="volume-and-lun-binding"></a>磁片區和 LUN 系結

\[從 Windows 8 和 Windows Server 2012 開始， [虛擬磁碟服務](virtual-disk-service-portal.md) COM 介面會被 [Windows 儲存體管理 API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)取代。\]

系結是指建立磁片區或 Lun。 磁片區是由磁片區和 Lun 組成，由磁片區所組成。 系結會針對實體資源的一組對應進行選取，並且在子系統內、在元件內或同時發生。 所有提供者程式都支援部分導向的系結模型，在此模型中，呼叫端僅指定特定興趣的系結屬性，並允許提供者選擇其餘部分。 在 VDS 中系結磁片區和 Lun 的作業很類似，但不完全相同。 例如，硬體提供者可以提供其他的系結選項。

VDS 針對部分導向的設定支援下列五種磁片區和 LUN 系結類型。  (硬體提供者可以和支援許多其他系結。 ) 



| 詞彙                                                                                                                                             | 描述                                                                                    |
|--------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="Simple"></span><span id="simple"></span><span id="SIMPLE"></span>簡單<br/>                                                     | 只有一個連續範圍的線性對應。<br/>                             |
| <span id="Spanned"></span><span id="spanned"></span><span id="SPANNED"></span>跨越<br/>                                                 | 在多個磁片或磁片磁碟機上具有多個非連續範圍的線性對應。<br/> |
| <span id="Striped"></span><span id="striped"></span><span id="STRIPED"></span>條紋<br/>                                                 | 跨多個磁片或磁片磁碟機交錯連續磁片區範圍的對應。<br/> |
| <span id="Mirrored"></span><span id="mirrored"></span><span id="MIRRORED"></span>鏡像<br/>                                             | 維護兩個以上相同資料複本的對應。<br/>                           |
| <span id="Striped_with_parity"></span><span id="striped_with_parity"></span><span id="STRIPED_WITH_PARITY"></span>以同位等量分割<br/> | 在多個磁片或磁片磁碟機之間分散同位檢查資訊的對應。<br/>  |



 

VDS 會使用來自多個成員的同位系結來建立鏡像、等量和等量分割。 例如，雙向鏡像有兩個成員。 每個成員都可以佔用多個磁片或磁片磁碟機上的範圍。 VDS 會串連範圍來形成成員，然後在成員上系結磁片區或 LUN。 提供者可支援所有系結類型或任何子集。 在 VDS 物件模型中，鏡像的每個成員都是一個稱為 plex 的獨立物件。

同樣地，磁片區和 LUN 類型都很類似，但並非完全相同。 如需磁片區類型的描述，請參閱 [磁片區物件](volume-object.md)。針對 LUN 類型，請參閱 [Lun 物件](lun-object.md)。 系結類型不是容錯或容錯。

### <a name="non-fault-tolerant-binding"></a>不可容錯的系結

非容錯磁片區和 Lun 不提供嚴重損壞修復。 如果有一個磁片區對不容錯磁片區或 LUN 造成故障，則整個磁片區或 LUN 會失敗。 在交換中，對於資料的風險，非容錯磁片區和 Lun 提供的輸入/輸出效能通常會優於容錯磁片區和 Lun 的效能。 VDS 支援下列三種不可容錯的類型：簡單、跨距和等量。

簡單

![此圖顯示具有2個元件和2個子系統的簡單非容錯型別。](images/vdssimplelunvol.png)

合併

![顯示具有1個套件和1個子系統的跨距非容錯類型圖表。](images/vdsspanlunvol.png)

等量

![顯示具有1個套件和1個子系統之等量非容錯類型的圖表。](images/vdsstripelunvol.png)

### <a name="fault-tolerant-binding"></a>容錯系結

下列容錯磁片區和 Lun 提供嚴重損壞修復。 如果其中一個磁片區對容錯磁片區或 LUN 失敗，則可以復原資料。 在資料安全性的 exchange 中，容錯磁片區和 Lun 的輸入/輸出效能通常會與非容錯磁片區和 Lun 的輸入/輸出效能很差。 VDS 支援兩種容錯類型：使用同位鏡像和等量分割。

鏡像 (三向鏡像) 

![顯示鏡像 (三向鏡像) 容錯類型的圖表。](images/vdsmirrorlunvol.png)

以同位等量分割

![顯示具有同位容錯類型之等量的圖表。](images/vdsstripeparitylunvol.png)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[設定總覽](configuration.md)
</dt> <dt>

[磁片區物件](volume-object.md)
</dt> <dt>

[LUN 物件](lun-object.md)
</dt> </dl>

 

