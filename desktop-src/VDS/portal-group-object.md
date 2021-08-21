---
description: 入口網站群組物件
ms.assetid: e5892e96-b6ad-447a-9627-b44fc6f1b27a
title: 入口網站群組物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e1021d74a3c8a6a612372db56952be1dabe5380e8e4a49b1b83c5ae2fe54754
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119057956"
---
# <a name="portal-group-object"></a>入口網站群組物件

\[從 Windows 8 和 Windows Server 2012 開始， [Windows 儲存體管理 API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)會取代[虛擬磁碟服務](virtual-disk-service-portal.md)COM 介面。\]

入口網站群組物件會建立 iscsi 目標中所含 iSCSI 入口網站群組的模型。

使用 [**IVdsIscsiTarget：： QueryPortalGroups**](/windows/desktop/api/Vds/nf-vds-ivdsiscsitarget-queryportalgroups) 方法來判斷特定目標所包含的入口網站群組。 使用 [**IVdsIscsiPortal：： QueryAssociatedPortalGroups**](/windows/desktop/api/Vds/nf-vds-ivdsiscsiportal-queryassociatedportalgroups) 方法來判斷與指定的入口網站相關聯的入口網站群組。 呼叫端可以從 **QueryPortalGroups** 方法或 **QueryAssociatedPortalGroups** 方法所傳回的列舉中選取所需的入口網站群組物件，以取得特定入口網站群組的指標。 使用入口網站群組物件時，您可以新增或移除入口網站群組屬性、相關聯的入口網站，以及包含入口網站群組的目標的入口網站和查詢。

入口網站群組物件屬性包括 [物件識別碼](vds-data-types.md) 和入口網站群組標記。 如需入口網站群組標記的詳細資訊，請參閱中的 iSCSI 規格 <https://go.microsoft.com/fwlink/p/?linkid=158752> 。

下表列出相關的介面、列舉和結構。



| 類型                                                                                      | 元素                                                                                                                                            |
|-------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| 只有在 VDS 1.1 和 2.0 iSCSI 提供者中，此物件一律公開的介面 | [**IVdsIscsiPortalGroup**](/windows/desktop/api/Vds/nn-vds-ivdsiscsiportalgroup)。                                                                                              |
| 相關聯的列舉                                                                   | 無。                                                                                                                                              |
| 相關聯的結構                                                                     | [**VDS \_ISCSI \_ PORTALGROUP \_**](/windows/desktop/api/Vds/ns-vds-vds_iscsi_portalgroup_prop) 和 [**VDS \_ 入口網站 \_ 群組 \_ 通知**](/windows/desktop/api/Vds/ns-vds-vds_portal_group_notification)。 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[硬體提供者物件](hardware-provider-objects.md)
</dt> <dt>

[**IVdsIscsiPortal::QueryAssociatedPortalGroups**](/windows/desktop/api/Vds/nf-vds-ivdsiscsiportal-queryassociatedportalgroups)
</dt> <dt>

[**IVdsIscsiTarget::QueryPortalGroups**](/windows/desktop/api/Vds/nf-vds-ivdsiscsitarget-queryportalgroups)
</dt> </dl>

 

 
