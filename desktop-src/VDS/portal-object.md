---
description: 入口網站物件
ms.assetid: 6655bbae-07d3-416b-9e45-ddcbe3433f40
title: 入口網站物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b7004f648b11b16c8c6279a0a74bae775fa539d8f0a93fc83d7effccea68915
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119864518"
---
# <a name="portal-object"></a>入口網站物件

\[從 Windows 8 和 Windows Server 2012 開始， [Windows 儲存體管理 API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)會取代[虛擬磁碟服務](virtual-disk-service-portal.md)COM 介面。\]

入口網站物件會建立包含在 iSCSI 子系統內的 iSCSI 入口網站模型。

使用 [**IVdsSubSystemIscsi：： QueryPortals**](/windows/desktop/api/Vds/nf-vds-ivdssubsystemiscsi-queryportals) 方法來判斷子系統的 iSCSI 入口網站。 呼叫端可以從 **QueryPortals** 方法所傳回的列舉中選取所需的入口網站物件，以取得特定入口網站的指標。 您可以使用入口網站物件，設定入口網站屬性、相關聯的入口網站群組和包含入口網站的子系統的入口網站狀態和查詢。

入口網站物件最多隻能與指定目標的一個入口網站群組相關聯。

入口網站可作為 iSCSI 硬體提供者中 MPIO 路徑的其中一個端點，可在此設定負載平衡原則。

入口網站物件屬性包括物件識別碼、IP 位址和埠，以及入口網站的狀態。

下表列出相關的介面、列舉和結構。



| 類型                                                                                      | 元素                                                                                                                 |
|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| 只有在 VDS 1.1 和 2.0 iSCSI 提供者中，此物件一律公開的介面 | [**IVdsIscsiPortal**](/windows/desktop/api/Vds/nn-vds-ivdsiscsiportal)。                                                                             |
| 相關聯的列舉                                                                   | [**VDS \_ISCSI \_ 入口網站的 \_ 狀態**](/windows/desktop/api/Vds/ne-vds-vds_iscsi_portal_status)。                                                          |
| 相關聯的結構                                                                     | [**VDS \_ISCSI \_ 入口 \_ 網站**](/windows/desktop/api/Vds/ns-vds-vds_iscsi_portal_prop) 和 [**VDS \_ 埠 \_ 通知**](/windows/desktop/api/Vds/ns-vds-vds_port_notification)。 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[硬體提供者物件](hardware-provider-objects.md)
</dt> <dt>

[**IVdsSubSystemIscsi::QueryPortals**](/windows/desktop/api/Vds/nf-vds-ivdssubsystemiscsi-queryportals)
</dt> </dl>

 

 
