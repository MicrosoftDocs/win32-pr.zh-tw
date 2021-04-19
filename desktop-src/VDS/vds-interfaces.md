---
description: 虛擬磁碟服務 (VDS) 物件提供介面來公開查詢、設定和維護存放裝置的方法。
ms.assetid: 0bddfd62-881d-4fda-b303-ed38d434af55
title: VDS 介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06e6bbc6d471c89fd2f01e0875a5e786795813bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106977365"
---
# <a name="vds-interfaces"></a>VDS 介面

\[從 Windows 8 和 Windows Server 2012 開始， [虛擬磁碟服務](virtual-disk-service-portal.md) COM 介面會被 [Windows 儲存體管理 API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)取代。\]

虛擬磁碟服務 (VDS) 物件提供介面來公開查詢、設定和維護存放裝置的方法。



| 介面                                                            | 描述                                                                                                                                                                                           |
|----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IEnumVdsObject**](/windows/desktop/api/Vds/nn-vds-ienumvdsobject)                             | 列舉指定類型的一組 VDS 物件。                                                                                                                                              |
| [**IVdsAdmin**](/windows/desktop/api/VdsHwPrv/nn-vdshwprv-ivdsadmin)                                       | 向 VDS 註冊提供者。                                                                                                                                                                        |
| [**IVdsAdvancedDisk**](/windows/desktop/api/Vds/nn-vds-ivdsadvanceddisk)                         | 建立和刪除分割區，以及修改資料分割屬性。                                                                                                                                    |
| [**IVdsAdvancedDisk2**](/windows/desktop/api/Vds/nn-vds-ivdsadvanceddisk2)                       | 提供變更資料分割類型的方法。                                                                                                                                                          |
| [**IVdsAdviseSink**](/windows/desktop/api/Vds/nn-vds-ivdsadvisesink)                             | 接收 VDS 通知。                                                                                                                                                                           |
| [**IVdsAsync**](/windows/desktop/api/Vds/nn-vds-ivdsasync)                                       | 管理非同步作業。                                                                                                                                                                      |
| [**IVdsController**](/windows/desktop/api/Vds/nn-vds-ivdscontroller)                             | 公開在控制器上執行查詢和設定作業的方法。                                                                                                                    |
| [**IVdsControllerControllerPort**](/windows/desktop/api/Vds/nn-vds-ivdscontrollercontrollerport) | 提供方法來列舉執行 [**IVdsController**](/windows/desktop/api/Vds/nn-vds-ivdscontroller) 介面之類別的控制器埠。                                                                      |
| [**IVdsControllerPort**](/windows/desktop/api/Vds/nn-vds-ivdscontrollerport)                     | 提供在控制器埠上執行查詢和設定作業的方法。                                                                                                              |
| [**IVdsCreatePartitionEx**](/windows/desktop/api/Vds/nn-vds-ivdscreatepartitionex)               | 在基本磁碟上建立磁碟分割。                                                                                                                                                                  |
| [**IVdsDisk**](/windows/desktop/api/Vds/nn-vds-ivdsdisk)                                         | 查詢及設定基本和動態磁碟。                                                                                                                                                       |
| [**IVdsDisk2**](/windows/desktop/api/Vds/nn-vds-ivdsdisk2)                                       | 提供將磁片的 SAN 模式設定為離線或線上的方法。                                                                                                                                 |
| [**IVdsDiskPartitionMF**](/windows/desktop/api/Vds/nn-vds-ivdsdiskpartitionmf)                   | 提供在磁碟分割上執行檔案系統管理作業的方法。                                                                                                                          |
| [**IVdsDiskPartitionMF2**](/windows/desktop/api/Vds/nn-vds-ivdsdiskpartitionmf2)                 | 提供使用其他格式化選項來格式化分割區的方法。                                                                                                                           |
| [**IVdsDrive**](/windows/desktop/api/Vds/nn-vds-ivdsdrive)                                       | 提供在磁片磁碟機上執行查詢和設定作業的方法。                                                                                                                        |
| [**IVdsDrive2**](/windows/desktop/api/Vds/nn-vds-ivdsdrive2)                                     | 提供方法來查詢磁片磁碟機的屬性。                                                                                                                                             |
| [**IVdsHbaPort**](/windows/desktop/api/Vds/nn-vds-ivdshbaport)                                   | 提供方法來查詢本機系統上的 HBA 埠並與其互動。                                                                                                                            |
| [**IVdsHwProvider**](/windows/desktop/api/Vds/nn-vds-ivdshwprovider)                             | 提供在硬體提供者上執行查詢、reenumeration 和重新整理作業的方法。                                                                                                  |
| [**IVdsHwProviderPrivate**](/windows/desktop/api/VdsHwPrv/nn-vdshwprv-ivdshwproviderprivate)               | 提供一種方法，可讓 VDS 判斷硬體提供者是否擁有指定的 LUN。                                                                                                   |
| [**IVdsHwProviderPrivateMpio**](/windows/desktop/api/VdsHwPrv/nn-vdshwprv-ivdshwproviderprivatempio)       | 提供方法，將源自特定 HBA 埠的路徑狀態設定為提供者。                                                                                               |
| [**IVdsHwProviderStoragePools**](/windows/desktop/api/Vds/nn-vds-ivdshwproviderstoragepools)     | 提供在 [存放集區](storage-pool-object.md) 中建立 lun，以及列舉由硬體提供者所管理之存放集區的方法。                                                          |
| [**IVdsHwProviderType**](/windows/desktop/api/Vds/nn-vds-ivdshwprovidertype)                     | 提供方法來取得硬體提供者的類型。                                                                                                                                          |
| [**IVdsHwProviderType2**](/windows/desktop/api/Vds/nn-vds-ivdshwprovidertype2)                   | 此介面不會實作為。 請改用 [**IVdsHwProviderType**](/windows/desktop/api/Vds/nn-vds-ivdshwprovidertype) 。                                                                                                      |
| [**IVdsIscsiInitiatorAdapter**](/windows/desktop/api/Vds/nn-vds-ivdsiscsiinitiatoradapter)       | 提供方法來查詢本機系統上的 iSCSI 啟動器介面卡，並與之互動。                                                                                                             |
| [**IVdsIscsiInitiatorPortal**](/windows/desktop/api/Vds/nn-vds-ivdsiscsiinitiatorportal)         | 提供方法來查詢本機系統上的 iSCSI 啟動器入口網站並與其互動。                                                                                                              |
| [**IVdsIscsiPortal**](/windows/desktop/api/Vds/nn-vds-ivdsiscsiportal)                           | 提供在 iSCSI 入口網站上執行查詢和設定作業的方法。                                                                                                                |
| [**IVdsIscsiPortalGroup**](/windows/desktop/api/Vds/nn-vds-ivdsiscsiportalgroup)                 | 提供在 iSCSI 入口網站群組上執行查詢和設定服務的方法。                                                                                                            |
| [**IVdsIscsiPortalLocal**](/windows/desktop/api/Vds/nn-vds-ivdsiscsiportallocal)                 | 提供在 iSCSI 入口網站上設定本機啟動器特定 IPSEC 預先共用金鑰的方法。                                                                                                       |
| [**IVdsIscsiTarget**](/windows/desktop/api/Vds/nn-vds-ivdsiscsitarget)                           | 提供在 iSCSI 目標上執行查詢和設定作業的方法。                                                                                                                |
| [**IVdsLun**](/windows/desktop/api/Vds/nn-vds-ivdslun)                                           | 提供在 LUN 上執行查詢和設定作業的方法， (邏輯單元編號) 。                                                                                                    |
| [**IVdsLun2**](/windows/desktop/api/Vds/nn-vds-ivdslun2)                                         | 提供套用和查詢邏輯單元編號 (LUN) 提示的方法。                                                                                                                           |
| [**IVdsLunControllerPorts**](/windows/desktop/api/Vds/nn-vds-ivdsluncontrollerports)             | 提供在 LUN 上執行控制器埠設定作業的方法。                                                                                                                    |
| [**IVdsLunIscsi**](/windows/desktop/api/Vds/nn-vds-ivdsluniscsi)                                 | 提供在 iSCSI LUN 上執行查詢和設定作業的方法。                                                                                                                   |
| [**IVdsLunMpio**](/windows/desktop/api/Vds/nn-vds-ivdslunmpio)                                   | 提供在具有 MPIO 擴充功能的 LUN 上執行查詢和設定作業的方法。                                                                                                     |
| [**IVdsLunNaming**](/windows/desktop/api/Vds/nn-vds-ivdslunnaming)                               | 提供方法，為執行 [**IVdsLun**](/windows/desktop/api/Vds/nn-vds-ivdslun) 介面的類別命名 lun。                                                                                                     |
| [**IVdsLunNumber**](/windows/desktop/api/Vds/nn-vds-ivdslunnumber)                               | 提供方法來查詢 LUN 的 LUN 編號。                                                                                                                                                  |
| [**IVdsLunPlex**](/windows/desktop/api/Vds/nn-vds-ivdslunplex)                                   | 提供在 LUN plex 上執行查詢和設定作業的方法。                                                                                                                     |
| [**IVdsMaintenance**](/windows/desktop/api/Vds/nn-vds-ivdsmaintenance)                           | 提供在子系統、控制器或磁片磁碟機上執行維護作業的方法。                                                                                                          |
| [**IVdsOpenVDisk**](/windows/desktop/api/Vds/nn-vds-ivdsopenvdisk)                               | 定義用於管理虛擬磁片的方法。                                                                                                                                                          |
| [**IVdsPack**](/windows/desktop/api/Vds/nn-vds-ivdspack)                                         | 查詢並設定包含磁片的套件，並建立磁片區。                                                                                                                                   |
| [**IVdsPack2**](/windows/desktop/api/Vds/nn-vds-ivdspack2)                                       | 提供方法，在套件上建立對齊的磁片區。                                                                                                                                                |
| [**IVdsProvider**](/windows/desktop/api/Vds/nn-vds-ivdsprovider)                                 | 傳回硬體或軟體提供者的屬性。                                                                                                                                                 |
| [**IVdsProviderPrivate**](/windows/desktop/api/VdsHwPrv/nn-vdshwprv-ivdsproviderprivate)                   | 提供可讓 VDS 針對提供者物件執行其他作業的方法。                                                                                                               |
| [**IVdsProviderSupport**](/windows/desktop/api/Vds/nn-vds-ivdsprovidersupport)                   | 提供方法，指出提供者支援的 VDS 介面版本。                                                                                                      |
| [**IVdsRemovable**](/windows/desktop/api/Vds/nn-vds-ivdsremovable)                               | 查詢並取出抽取式磁碟，例如 CD-ROM。                                                                                                                                                  |
| [**IVdsService**](/windows/desktop/api/Vds/nn-vds-ivdsservice)                                   | 提供使用 VDS 的服務層級方法。                                                                                                                                                  |
| [**IVdsServiceHba**](/windows/desktop/api/Vds/nn-vds-ivdsservicehba)                             | 提供方法來查詢本機系統上的 HBA 埠。                                                                                                                                             |
| [**IVdsServiceIscsi**](/windows/desktop/api/Vds/nn-vds-ivdsserviceiscsi)                         | 提供與本機啟動器服務互動的方法。                                                                                                                                       |
| [**IVdsServiceLoader**](/windows/desktop/api/Vds/nn-vds-ivdsserviceloader)                       | 啟動 VDS。                                                                                                                                                                                         |
| [**IVdsServiceUninstallDisk**](/windows/desktop/api/Vds/nn-vds-ivdsserviceuninstalldisk)         | 提供卸載基本和動態磁碟的方法。                                                                                                                                                |
| [**IVdsStoragePool**](/windows/desktop/api/Vds/nn-vds-ivdsstoragepool)                           | 提供方法來查詢資訊，以及列舉 [存放集區](storage-pool-object.md)的相關物件。                                                                                    |
| [**IVdsSubSystem**](/windows/desktop/api/Vds/nn-vds-ivdssubsystem)                               | 提供在子系統上執行查詢和設定作業的方法。                                                                                                                    |
| [**IVdsSubSystem2**](/windows/desktop/api/Vds/nn-vds-ivdssubsystem2)                             | 提供在子系統上使用 [**vds \_ HINTS2**](/windows/desktop/api/Vds/ns-vds-vds_hints2) 和 [**vds \_ SUB \_ SYSTEM \_ this.prop2**](/windows/desktop/api/Vds/ns-vds-vds_sub_system_prop2) 結構來執行查詢和設定作業的方法。 |
| [**IVdsSubSystemImportTarget**](/windows/desktop/api/Vds/nn-vds-ivdssubsystemimporttarget)       | 提供查詢及設定子系統之預設 VSS 匯入目標的方法。                                                                                                              |
| [**IVdsSubSystemInterconnect**](/windows/desktop/api/Vds/nn-vds-ivdssubsysteminterconnect)       | 提供方法來查詢子系統所支援的互連類型。                                                                                                                  |
| [**IVdsSubSystemIscsi**](/windows/desktop/api/Vds/nn-vds-ivdssubsystemiscsi)                     | 提供方法來查詢和設定子系統上的 iSCSI 目標和入口網站。                                                                                                                     |
| [**IVdsSubSystemNaming**](/windows/desktop/api/Vds/nn-vds-ivdssubsystemnaming)                   | 提供方法來為執行 [**IVdsSubSystem**](/windows/desktop/api/Vds/nn-vds-ivdssubsystem) 介面的類別命名子系統。                                                                                   |
| [**IVdsSwProvider**](/windows/desktop/api/Vds/nn-vds-ivdsswprovider)                             | 執行軟體提供者作業。                                                                                                                                                                |
| [**IVdsVDisk**](/windows/desktop/api/Vds/nn-vds-ivdsvdisk)                                       | 定義用於管理虛擬磁片的方法。                                                                                                                                                          |
| [**IVdsVdProvider**](/windows/desktop/api/Vds/nn-vds-ivdsvdprovider)                             | 定義用來建立和管理虛擬磁片的方法。                                                                                                                                              |
| [**IVdsVolume**](/windows/desktop/api/Vds/nn-vds-ivdsvolume)                                     | 建立和刪除磁片區的 plex，以及修改磁片區的屬性。                                                                                                                                    |
| [**IVdsVolume2**](/windows/desktop/api/Vds/nn-vds-ivdsvolume2)                                   | 提供方法來傳回磁片區屬性資訊，包括磁片區 Guid。                                                                                                              |
| [**IVdsVolumeMF**](/windows/desktop/api/Vds/nn-vds-ivdsvolumemf)                                 | 執行磁片區物件的存取路徑和檔案系統作業。                                                                                                                                    |
| [**IVdsVolumeMF2**](/windows/desktop/api/Vds/nn-vds-ivdsvolumemf2)                               | 提供在磁片區物件上執行其他檔案系統管理作業的方法。                                                                                                        |
| [**IVdsVolumeMF3**](/windows/desktop/api/Vds/nn-vds-ivdsvolumemf3)                               | 提供在磁片區物件上執行其他檔案系統管理作業的方法。                                                                                                        |
| [**IVdsVolumeOnline**](/windows/desktop/api/Vds/nn-vds-ivdsvolumeonline)                         | 提供方法讓單一磁片區上線。                                                                                                                                                     |
| [**IVdsVolumePlex**](/windows/desktop/api/Vds/nn-vds-ivdsvolumeplex)                             | 查詢包含的磁片區，並修復不正確的範圍。                                                                                                                                                |
| [**IVdsVolumeShrink**](/windows/desktop/api/Vds/nn-vds-ivdsvolumeshrink)                         | 提供支援大量壓縮的方法。                                                                                                                                                         |



 

 

 
