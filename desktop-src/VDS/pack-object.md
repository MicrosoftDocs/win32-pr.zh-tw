---
description: Pack 物件
ms.assetid: e84a05a0-ea12-4bc1-83e1-1eb0dd291dc9
title: Pack 物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02b01978747df5ccc273a31ae2f516b35c01df96
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/04/2021
ms.locfileid: "104566114"
---
# <a name="pack-object"></a>Pack 物件

\[從 Windows 8 和 Windows Server 2012 開始， [虛擬磁碟服務](virtual-disk-service-portal.md) COM 介面會被 [Windows 儲存體管理 API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)取代。\]

套件物件會建立磁片群組的模型，這是由基本或動態軟體提供者所管理的磁片和磁片區集合。 提供者可以包含多個套件物件。

使用 API，應用程式可以指示 VDS 將一或多個磁片新增至套件、將磁片系結至磁片區，並選擇性地將磁片移為主機之間的單位。 您無法將現有的磁片區匯入套件中。

> [!Note]  
> 套件中的成員資格不表示與效能、媒體、互連通訊協定或其他特性相關的磁片之間的一致性。

 

磁片物件為未配置、由 VDS 管理，或只是一個套件的成員。 基本軟體提供者可以有零或多個套件，每個都包含單一基本磁碟。 提供者對基本磁碟上的磁片區數目沒有任何限制。 動態提供者可以有零或多個套件，且每個套件中都有多個動態磁碟。 此提供者會根據邏輯磁片管理員 (LDM) 資料庫的一 mb 大小，限制磁片上的磁片區數目。 由於磁片區至少有一個 plex 和一個磁片區，因此套件的磁片區數目上限大約是1000。 當磁片數目增加時，最大值會下降。

除了磁片物件之外，套件還可包含一或多個硬體提供者所執行的一或多個 LUN 物件。 在 Windows 核心中，LUN 只是另一個磁片。  (LUN 物件必須在執行提供者程式的電腦上取消遮罩。 ) 當磁片為 LUN 時，LUN 物件會同時公開 [**IVdsLun**](/windows/desktop/api/Vds/nn-vds-ivdslun) 和 [**IVdsDisk**](/windows/desktop/api/Vds/nn-vds-ivdsdisk) 介面。 套件物件會使用 **IVdsDisk**（而不是 **IVdsLun**）來列舉套件中的 lun。 如需 LUN 的詳細描述，請參閱 [Lun 物件](lun-object.md)。

下圖顯示具有兩個成員的套件：磁片和 LUN。 應用程式可以將這些物件新增至線上元件，並從磁片區和磁片區所代表的磁片區建立磁片區。

![顯示「套件」的圖表，其中包含由應用程式新增的磁片和 LUN，以建立由「磁片磁碟機」和「主軸」表示的磁片區。](images/vdsdisksareluns.png)

使用 [**IVdsSwProvider：： CreatePack**](/windows/desktop/api/Vds/nf-vds-ivdsswprovider-createpack) 方法來建立新的套件物件。 呼叫端可以從 [**IVdsSwProvider：： QueryPacks**](/windows/desktop/api/Vds/nf-vds-ivdsswprovider-querypacks) 方法所傳回的列舉中選取所需的套件物件，以取得特定套件的指標。 您可以使用 pack 物件來加入、移除或取代套件的成員。 當您將磁片物件新增至套件時，VDS 會初始化磁片來解除所有現有磁片區的系結。 相反地，在將所有系結詳細資料加入套件時，LUN 都會保留所有的系結詳細資料。 如果您從套件中移除最後一個磁片，當呼叫端釋出物件的最後一個參考時，VDS 會刪除套件物件。

物件屬性包括物件識別碼、名稱、套件狀態和旗標。 線上套件適用于設定和使用，無法使用離線套件。 VDS 支援任意數量的線上與離線套件。

**Windows Server 2003：** 一次只支援一個線上套件。

VDS 會強制執行套件內的線上磁碟仲裁。 仲裁會判斷套件是否可具有線上狀態，並防止多部主機將線上狀態授與相同的套件。 如果套件中的線上磁片數目落在仲裁 (n/2 + 1) ，則 VDS 會讓線上套件離線。

下表列出相關的介面、列舉和結構。



| 類型                                              | 元素                                                                                                |
|---------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| 一律由這個物件公開的介面 | [**IVdsPack**](/windows/desktop/api/Vds/nn-vds-ivdspack)和 [**IVdsPack2**](/windows/desktop/api/Vds/nn-vds-ivdspack2) \* 。                                     |
| 相關聯的列舉                           | [**VDS \_套件 \_ 旗**](/windows/desktop/api/Vds/ne-vds-vds_pack_flag) 標和 [**VDS \_ PACK \_ 狀態**](/windows/desktop/api/Vds/ne-vds-vds_pack_status)。             |
| 相關聯的結構                             | [**VDS \_套件 \_**](/windows/desktop/api/Vds/ns-vds-vds_pack_prop) 的元件和 [**VDS \_ 套件 \_ 通知**](/windows/desktop/api/Vds/ns-vds-vds_pack_notification)。 |



 

**\* Windows Server 2003：** 在 windows Vista 之前，不支援此介面。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[軟體提供者物件](software-provider-objects.md)
</dt> <dt>

[LUN 物件](lun-object.md)
</dt> <dt>

[**IVdsLun**](/windows/desktop/api/Vds/nn-vds-ivdslun)
</dt> <dt>

[**IVdsDisk**](/windows/desktop/api/Vds/nn-vds-ivdsdisk)
</dt> </dl>

 

 
