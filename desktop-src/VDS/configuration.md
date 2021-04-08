---
description: 設定總覽
ms.assetid: 5cdc21a1-ff55-4c36-8106-b045256778ce
title: 設定總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d4db13827bf08ee65ed8015f0c19ba2980a9a71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943356"
---
# <a name="configuration-overview"></a>設定總覽

\[從 Windows 8 和 Windows Server 2012 開始， [虛擬磁碟服務](virtual-disk-service-portal.md) COM 介面會被 [Windows 儲存體管理 API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)取代。\]

如果您不熟悉 VDS 所定義的物件，請參閱 [Vds 物件模型](vds-object-model.md)。

虛擬磁片的設定複雜度可能從非常簡單到微調的範圍。 不在意、無人在意和企業虛擬磁片會定義三種一般設定的觀點。 每個觀點都呈現不同的需求：

-   不需要小心設定的虛擬磁片，或許只是為了將新磁片的磁碟分割和格式設定自動化，或暫時建立鏡像磁片區以將資料從一個磁片遷移到另一個磁片，而不需要停機。 這種磁片適用于具有一或多個磁片的筆記本電腦和其他系統。
-   免費的虛擬磁片提供可自行設定、自我修復和可用的儲存體;使用等量磁片區和 Lun 來達到更佳的效能;使用鏡像磁片區和 Lun 來達成更高的可用性;並使用套件使失敗模式變成乾淨且包含。 以新的大型快速磁片來取代舊的小型系統磁片時，此設定層級很理想。 它也適用于使用自動熱備份的鏡像資料—單一備用主軸可以保護許多磁片主軸。 如需詳細資訊，請參閱 [熱備份](hot-sparing.md)。

    小規模 San 取決於此設定層級所提供的彈性和自動化，與網路連接儲存 (NAS) 設備一樣。 免費的虛擬磁片可簡化合並應用程式儲存體的工作（例如，SQL 和 Exchange 的儲存體），而不需要合併伺服器。

-   企業虛擬磁片包含非常大型或複雜的企業設定，具有額外的網站特定或應用程式特定需求。 系統管理員會針對可能只執行的單一應用程式調整儲存子系統，例如訂單交易系統上的每月批次報告作業。 企業虛擬磁片必須調整規模、顯示儲存子系統的即時活動，以及滿足實際操作管理員的需求。

如需有關在 VDS 中鏡像、條紋和其他設定選項的詳細資訊，請參閱 [磁片區和 LUN](volume-and-lun-binding.md)系結。 先進的設定技術稱為「堆疊」，可讓您結合與現有磁片區和 Lun 相關聯的設定。 如需詳細資訊，請參閱設定 [堆疊](configuration-stacking.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[虛擬磁碟服務](virtual-disk-service-portal.md)
</dt> <dt>

[VDS 物件模型](vds-object-model.md)
</dt> <dt>

[熱備份](hot-sparing.md)
</dt> <dt>

[磁片區和 LUN 系結](volume-and-lun-binding.md)
</dt> <dt>

[設定堆疊](configuration-stacking.md)
</dt> </dl>

 

 
