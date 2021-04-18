---
description: 提供者物件會為負責儲存管理的程式進行模型處理。
ms.assetid: 131e927d-d32a-44f6-8aae-28839cfa9e7d
title: 提供者物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb36517f0091776b9429911212610134f31077a2
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/04/2021
ms.locfileid: "104571660"
---
# <a name="provider-object"></a>提供者物件

\[從 Windows 8 和 Windows Server 2012 開始， [虛擬磁碟服務](virtual-disk-service-portal.md) COM 介面會被 [Windows 儲存體管理 API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)取代。\]

提供者物件會為負責儲存管理的程式進行模型處理。 此物件可讓您存取軟體提供者和硬體提供者功能。 提供者程式會在軟體裝置上執行作業 (磁片區和磁片) 和硬體裝置 (儲存子系統和 RAID 控制器) 後方的磁片磁碟機陣列。

VDS 會將提供者物件註冊為 Windows 登錄中的 COM 物件，並使用包含的介面 (非匯總) 來執行其餘的物件、包裝所有介面和方法，並有條件地新增功能。 由提供者物件包裝的物件和介面，會根據提供者類型而有所不同。

您無法直接從您的應用程式具現化提供者物件。 相反地，您必須啟動 VDS、取得服務物件的指標，然後使用服務物件來查詢主機已知的提供者。 如需有關載入 VDS 的指示，請參閱 [啟動和服務物件](startup-and-service-objects.md)。

使用 [**IVdsService：： QueryProviders**](/windows/desktop/api/Vds/nf-vds-ivdsservice-queryproviders) 方法來列舉主機上已註冊的提供者程式。 方法的第一個參數可讓您僅指定軟體提供者、僅限硬體提供者，或兩者。 您可以使用提供者物件，對該提供者所管理的物件執行作業。 如下圖所示，您可以使用 [**IVdsSwProvider**](/windows/desktop/api/Vds/nn-vds-ivdsswprovider) 介面所公開的方法，來建立和查詢與軟體提供者相關聯的套件物件。 同樣地，您可以使用 [**IVdsHwProvider**](/windows/desktop/api/Vds/nn-vds-ivdshwprovider) 介面上的方法，與與硬體提供者相關聯的子系統物件進行互動。

![顯示「應用程式」分支至「提供者」、「套件」或「子系統」以及「主軸」的圖表。](images/vdsproviderobject.png)

物件屬性包含持續性的 GUID 物件識別碼，表示特定提供者和第二個代表提供者版本的 GUID。 請注意，VDS 物件模型中的其他物件識別碼是非持續性的。 此物件的其餘屬性包含提供者名稱、其他版本資訊、提供者類型軟體或硬體) 、各種旗標，以及只適用于軟體提供者的重建優先順序設定。

下表列出相關的介面、列舉和結構 

| 類型                                                                                         | 元素                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 一律由這個物件公開的介面                                            | [**IVdsProvider**](/windows/desktop/api/Vds/nn-vds-ivdsprovider)                                                                                                                                                                                                                                                           |
| 一律由軟體提供者公開的介面                                | [**IVdsSwProvider**](/windows/desktop/api/Vds/nn-vds-ivdsswprovider)                                                                                                                                                                                                                                                       |
| 一律由硬體提供者公開的介面                                | [**IVdsHwProvider**](/windows/desktop/api/Vds/nn-vds-ivdshwprovider)                                                                                                                                                                                                                                                       |
| 此物件可能公開的介面                                                | [**IVdsProviderSupport**](/windows/desktop/api/Vds/nn-vds-ivdsprovidersupport)                                                                                                                                                                                                                                             |
| 僅可由硬體提供者公開的介面                                    | [**IVdsHwProviderType**](/windows/desktop/api/Vds/nn-vds-ivdshwprovidertype)、 [**IVdsHwProviderStoragePools**](/windows/desktop/api/Vds/nn-vds-ivdshwproviderstoragepools)**Windows server 2008、windows Vista 和 windows Server 2003：** 不支援 [**IVdsHwProviderStoragePools**](/windows/desktop/api/Vds/nn-vds-ivdshwproviderstoragepools) 介面。<br/> |
| 一律會執行但不會對應用程式公開的介面                       | [**IVdsProviderPrivate**](/windows/desktop/api/VdsHwPrv/nn-vdshwprv-ivdsproviderprivate)                                                                                                                                                                                                                                             |
| 一律由硬體提供者執行但未公開給應用程式的介面 | [**IVdsHwProviderPrivate**](/windows/desktop/api/VdsHwPrv/nn-vdshwprv-ivdshwproviderprivate)                                                                                                                                                                                                                                         |
| 可能由硬體提供者執行但未公開給應用程式的介面     | [**IVdsHwProviderPrivateMpio**](/windows/desktop/api/VdsHwPrv/nn-vdshwprv-ivdshwproviderprivatempio)                                                                                                                                                                                                                                 |
| 相關聯的列舉                                                                      | [**VDS \_提供者 \_ 旗**](/windows/desktop/api/Vds/ne-vds-vds_provider_flag)標、 [**vds \_ 查詢 \_ 提供者 \_ 旗**](/windows/desktop/api/Vds/ne-vds-vds_query_provider_flag)標，以及 [**vds \_ 提供者 \_ 類型**](/windows/desktop/api/Vds/ne-vds-vds_provider_type)。                                                                                                                         |
| 相關聯的結構                                                                        | 無。                                                                                                                                                                                                                                                                                          |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[VDS 物件模型](vds-object-model.md)
</dt> <dt>

[Startup 和 Service 物件](startup-and-service-objects.md)
</dt> <dt>

[**IVdsService::QueryProviders**](/windows/desktop/api/Vds/nf-vds-ivdsservice-queryproviders)
</dt> <dt>

[**IVdsSwProvider**](/windows/desktop/api/Vds/nn-vds-ivdsswprovider)
</dt> <dt>

[**IVdsHwProvider**](/windows/desktop/api/Vds/nn-vds-ivdshwprovider)
</dt> </dl>

 

