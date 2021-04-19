---
description: LUN Plex 物件
ms.assetid: db6eabaa-1b84-4613-ab2a-8d5904305e08
title: LUN Plex 物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f1b51657ccbfc0f1bd3d73e54128cac3f0b507c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975935"
---
# <a name="lun-plex-object"></a>LUN Plex 物件

\[從 Windows 8 和 Windows Server 2012 開始， [虛擬磁碟服務](virtual-disk-service-portal.md) COM 介面會被 [Windows 儲存體管理 API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)取代。\]

LUN plex 物件會為 lun 所包含的 LUN plex 建立模型。 只有鏡像的 LUN 可以有多個 plex;所有其他 LUN 類型都有一個 plex。 每個 plex 都包含 LUN 上的資料複本。 新的 plex 可以新增至 LUN，而且除了原始的 plex 之外，現有的 plex 也可以移除。 VDS 支援四個 LUN 的 plex 類型：簡單、跨距、等量和同位檢查。 如需這些 LUN 類型的說明，請參閱 [Lun 物件](lun-object.md)。

使用 [**IVdsLun：： AddPlex**](/windows/desktop/api/Vds/nf-vds-ivdslun-addplex) 方法將 plex 新增至 LUN，並使用 [**IVdsLun：： RemovePlex**](/windows/desktop/api/Vds/nf-vds-ivdslun-removeplex) 方法來刪除該 plex。 您可以藉由叫用 [**IVdsLun：： QueryPlexes**](/windows/desktop/api/Vds/nf-vds-ivdslun-queryplexes) 方法來查詢 LUN 的 plex。 您可以從 **QueryPlexes** 方法所傳回的列舉中選取所需的 plex 物件，以取得特定 LUN plex 的指標。 您可以使用 plex 物件來查詢磁片區範圍和 automagic 提示，並套用新的提示。

除了物件識別碼、名稱和序號之外，LUN plex 物件屬性還包括 plex 類型、大小、狀態、健康情況、轉換狀態和旗標;取消遮罩清單和 stripe 大小;以及重建優先權設定。

下表列出相關的介面、列舉和結構。



| 類型                                              | 元素                                                                                                                                                          |
|---------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 一律由這個物件公開的介面 | [**IVdsLunPlex**](/windows/desktop/api/Vds/nn-vds-ivdslunplex)。                                                                                                                              |
| 相關聯的列舉                           | [**VDS \_LUN \_ plex \_ 旗**](/windows/desktop/api/Vds/ne-vds-vds_lun_plex_flag)標、 [**vds \_ Lun \_ plex \_ 狀態**](/windows/desktop/api/Vds/ne-vds-vds_lun_plex_status)，以及 [**vds \_ lun \_ plex \_ 類型**](/windows/desktop/api/Vds/ne-vds-vds_lun_plex_type)。 |
| 相關聯的結構                             | [**VDS \_LUN \_ PLEX \_**](/windows/desktop/api/Vds/ns-vds-vds_lun_plex_prop)的一種。                                                                                                               |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[硬體提供者物件](hardware-provider-objects.md)
</dt> <dt>

[LUN 物件](lun-object.md)
</dt> </dl>

 

 
