---
description: 目標物件
ms.assetid: e88d65ad-9b56-4620-a0f5-573c5e245b3e
title: 目標物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b528d66fb789e4d237dacae151c3dda596e834f84f529c3677905672de3b7588
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119057946"
---
# <a name="target-object"></a>目標物件

\[從 Windows 8 和 Windows Server 2012 開始， [Windows 儲存體管理 API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)會取代[虛擬磁碟服務](virtual-disk-service-portal.md)COM 介面。\]

目標物件會建立包含在 iSCSI 子系統內的 iSCSI 目標模型。

使用 [**IVdsSubSystemIscsi：： QueryTargets**](/windows/desktop/api/Vds/nf-vds-ivdssubsystemiscsi-querytargets) 方法來判斷子系統的 iSCSI 目標。 呼叫端可以從 **QueryTargets** 方法所傳回的列舉中選取所需的目標物件，以取得特定目標的指標。 使用目標物件時，您可以設定目標內容的易記名稱和查詢、相關聯的 Lun，以及包含目標的子系統。

主機電腦必須登入目標，才能存取其相關聯的 Lun。 若要對目標執行登入，目標在其中一個入口網站群組中至少必須有一個相關聯的入口網站。 相關聯 Lun 的輸入和輸出會透過此登入會話進行處理。

目標物件屬性包括物件識別碼、iSCSI 名稱、易記名稱，以及啟用 CHAP 的旗標。

下表列出相關的介面、列舉和結構。



| 類型                                                                                      | 元素                                                                                                                     |
|-------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| 只有在 VDS 1.1 和 2.0 iSCSI 提供者中，此物件一律公開的介面 | [**IVdsIscsiTarget**](/windows/desktop/api/Vds/nn-vds-ivdsiscsitarget)。                                                                                 |
| 相關聯的列舉                                                                   | 無。                                                                                                                       |
| 相關聯的結構                                                                     | [**VDS \_ISCSI \_ 目標的 \_ 主張**](/windows/desktop/api/Vds/ns-vds-vds_iscsi_target_prop) 和 [**VDS \_ 目標 \_ 通知**](/windows/desktop/api/Vds/ns-vds-vds_target_notification)。 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[硬體提供者物件](hardware-provider-objects.md)
</dt> <dt>

[**IVdsSubSystemIscsi::QueryTargets**](/windows/desktop/api/Vds/nf-vds-ivdssubsystemiscsi-querytargets)
</dt> </dl>

 

 
