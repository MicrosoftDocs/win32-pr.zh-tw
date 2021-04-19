---
description: VDS 會提供物件來執行與服務相關的活動。 本主題說明每個物件。
ms.assetid: ae4d18f2-4d50-480c-bc7a-4eec0334707d
title: Startup 和 Service 物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92beb0a4f825f767299a7ced74d43ef2487fa252
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997581"
---
# <a name="startup-and-service-objects"></a>Startup 和 Service 物件

\[從 Windows 8 和 Windows Server 2012 開始， [虛擬磁碟服務](virtual-disk-service-portal.md) COM 介面會被 [Windows 儲存體管理 API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)取代。\]

VDS 會提供物件來執行與服務相關的活動。 本主題說明每個物件。

## <a name="service-loader-object"></a>服務載入器物件

服務載入器物件提供應用程式用來載入和初始化 VDS 的方法。 若要準備 VDS 以供使用，應用程式必須執行下列作業：

-   建立服務載入器物件的實例，它會傳回 [**IVdsServiceLoader**](/windows/desktop/api/Vds/nn-vds-ivdsserviceloader) 介面。
-   呼叫 [**IVdsServiceLoader：： LoadService**](/windows/desktop/api/Vds/nf-vds-ivdsserviceloader-loadservice) 方法以載入服務。

如需程式碼範例，請參閱 [載入 VDS](loading-vds.md)。

一律允許服務在呼叫服務物件所公開的方法之前，完全初始化。 您可以使用 [**IVdsService：： IsServiceReady**](/windows/desktop/api/Vds/nf-vds-ivdsservice-isserviceready) 方法來判斷載入進程的狀態。 使用 [**IVdsService：： WaitForServiceReady**](/windows/desktop/api/Vds/nf-vds-ivdsservice-waitforserviceready) 方法來封鎖對 VDS 物件的呼叫，直到初始化完成為止。

下表列出相關的介面、列舉和結構。

| 類型                                              | 元素                                         |
|---------------------------------------------------|-------------------------------------------------|
| 一律由這個物件公開的介面 | [**IVdsServiceLoader**](/windows/desktop/api/Vds/nn-vds-ivdsserviceloader)。 |
| 相關聯的列舉                           | 無。                                           |
| 相關聯的結構                             | 無。                                           |



 

## <a name="service-object"></a>服務物件

服務物件是所有 VDS 應用程式核心的多工物件。 使用這個物件時，呼叫端可以執行下列作業：

-   判斷服務初始化的狀態。
-   取得以 VDS 註冊的所有硬體或軟體提供者。
-   報告未配置的磁片。
-   傳回與磁片上的磁片區相關聯的檔案系統類型和磁碟機號。
-   從登錄中移除未使用的使用者模式路徑和裝載的資料夾，然後重新整理磁片。
-   接收 VDS 通知。
-   重新開機主機。
-   在本機電腦上取出光纖通道 HBA 埠或 iSCSI 啟動器介面卡。
-   安全地準備在本機電腦上公開為磁片的 Lun，以供移除。

VDS 通知結構會將物件 Guid 傳遞給已向 VDS 註冊的所有應用程式，以接收通知。 使用 [**IVdsService：： GetObject**](/windows/desktop/api/Vds/nf-vds-ivdsservice-getobject) 方法將物件 GUID 轉換為物件指標。 如需通知模型的完整說明，請參閱 [VDS 通知](vds-notification-model.md)。

下表列出相關的介面、列舉和結構。 

| 類型                                                                   | 元素                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 一律由這個物件公開的介面                      | [**IVdsService**](/windows/desktop/api/Vds/nn-vds-ivdsservice)、 [**IVdsServiceHba**](/windows/desktop/api/Vds/nn-vds-ivdsservicehba) \* 、 [**IVdsServiceIscsi**](/windows/desktop/api/Vds/nn-vds-ivdsserviceiscsi) \* 、 [**IVdsServiceUninstallDisk**](/windows/desktop/api/Vds/nn-vds-ivdsserviceuninstalldisk) \* 。                                                                                                                                                                                                           |
| 一律會執行但不會對應用程式公開的介面 | [**IVdsAdmin**](/windows/desktop/api/VdsHwPrv/nn-vdshwprv-ivdsadmin)                                                                                                                                                                                                                                                                                                                                                                            |
| 相關聯的列舉                                                | [**VDS \_查詢 \_ 提供者 \_ 旗**](/windows/desktop/api/Vds/ne-vds-vds_query_provider_flag)標， [**VDS \_ 物件 \_ 類型**](/windows/desktop/api/Vds/ne-vds-vds_object_type)， [**VDS \_ 服務 \_ 旗**](/windows/desktop/api/Vds/ne-vds-vds_service_flag)標， [**VDS \_ 磁碟機 \_ 號 \_ 旗**](/windows/desktop/api/Vds/ne-vds-vds_drive_letter_flag)標， [**VDS \_ 檔 \_ 系統 \_ 旗**](/windows/desktop/api/Vds/ne-vds-vds_file_system_flag)標， [**VDS \_ 檔 \_ 系統 \_ \_**](/windows/desktop/api/Vds/ne-vds-vds_file_system_prop_flag)的旗標。                                                      |
| 相關聯的結構                                                  | [**VDS \_服務 \_**](/windows/desktop/api/Vds/ns-vds-vds_service_prop)類別、 [**VDS \_ 檔 \_ 系統的 \_ 主張**](/windows/desktop/api/Vds/ns-vds-vds_file_system_prop)、 [**VDS \_ 檔 \_ 系統 \_ 類型 \_**](/windows/desktop/api/Vds/ns-vds-vds_file_system_type_prop)、 [**VDS \_ 磁片磁碟機 \_ 信件 \_ 通知**](/windows/desktop/api/Vds/ns-vds-vds_drive_letter_notification)、 [**VDS \_ 檔 \_ 系統 \_ 通知**](/windows/desktop/api/Vds/ns-vds-vds_file_system_notification)、 [**VDS \_ 裝入 \_ 點 \_ 通知**](/windows/desktop/api/Vds/ns-vds-vds_mount_point_notification)。 |



 

**\* Windows server 2003：** 在 Windows server 2003 R2 之前，不支援這些介面。

## <a name="initiator-adapter-object"></a>啟動器介面卡物件

啟動器介面卡物件會在 VDS 服務的主機電腦上，為 iSCSI 啟動器介面卡建模。 VDS 服務只能在本機電腦上查看啟動器介面卡。 啟動器介面卡物件的角色是用來管理從本機電腦到 iSCSI 目標的登入會話。

下表列出相關的介面、列舉和結構。 

| 類型                                              | 元素                                                                                                                                                                  |
|---------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 一律由這個物件公開的介面 | [**IVdsIscsiInitiatorAdapter**](/windows/desktop/api/Vds/nn-vds-ivdsiscsiinitiatoradapter) \* 。                                                                                                        |
| 相關聯的列舉                           | [**VDS \_ISCSI \_ 登入 \_ 類型**](/windows/desktop/api/Vds/ne-vds-vds_iscsi_login_type)。 [**VDS \_ISCSI \_ 登入 \_ 旗**](/windows/desktop/api/Vds/ne-vds-vds_iscsi_login_flag)標， [**VDS \_ ISCSI \_ 驗證 \_ 類型**](/windows/desktop/api/Vds/ne-vds-vds_iscsi_auth_type)。 |
| 相關聯的結構                             | [**VDS \_ISCSI \_ 啟動器 \_ 適配 \_ 卡**](/windows/desktop/api/Vds/ns-vds-vds_iscsi_initiator_adapter_prop)。                                                                                        |



 

**\* Windows server 2003：** 在 Windows server 2003 R2 之前，不支援此介面。

## <a name="initiator-portal-object"></a>啟動器入口網站物件

啟動器入口網站物件會將 iscsi 啟動器上的 iSCSI 啟動器入口網站模型。 啟動器入口網站是一種 IP 位址和埠的組合，主機電腦會透過此通訊埠連接到 iSCSI 子系統上的入口網站。 啟動器入口網站物件的角色是作為 MPIO 路徑的其中一個端點，以及設定 IPSEC 安全性設定。

下表列出相關的介面、列舉和結構。 

| 類型                                              | 元素                                                                                                                                                                         |
|---------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 一律由這個物件公開的介面 | [**IVdsIscsiInitiatorPortal**](/windows/desktop/api/Vds/nn-vds-ivdsiscsiinitiatorportal) \* 。                                                                                                                 |
| 相關聯的列舉                           | [**VDS \_ISCSI \_ IPSEC \_ 旗**](/windows/desktop/api/Vds/ne-vds-vds_iscsi_ipsec_flag)標。                                                                                                                        |
| 相關聯的結構                             | [**VDS \_ISCSI \_ 啟動器 \_ 入口網站的 \_ 主張**](/windows/desktop/api/Vds/ns-vds-vds_iscsi_initiator_portal_prop)、 [**VDS \_ ISCSI \_ IPSEC \_ 金鑰**](/windows/desktop/api/Vds/ns-vds-vds_iscsi_ipsec_key)、 [**VDS \_ IPADDRESS**](/windows/desktop/api/Vds/ns-vds-vds_ipaddress)。 |



 

**\* Windows server 2003：** 在 Windows server 2003 R2 之前，不支援此介面。

## <a name="hba-port-object"></a>HBA 埠物件

HBA 埠物件會建立光纖通道的主機匯流排介面卡 (HBA) 埠的模型。

使用 [**IVdsServiceHba：： QueryHbaPorts**](/windows/desktop/api/Vds/nf-vds-ivdsservicehba-queryhbaports) 方法來判斷本機電腦上的 VDS 已知的 HBA 埠。

下表列出相關的介面、列舉和結構。

| 類型                                              | 元素                                                                                                                                                          |
|---------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 一律由這個物件公開的介面 | [**IVdsHbaPort**](/windows/desktop/api/Vds/nn-vds-ivdshbaport) \* 。                                                                                                                            |
| 相關聯的列舉                           | [**VDS \_HBAPORT \_ 類型**](/windows/desktop/api/Vds/ne-vds-vds_hbaport_type)、 [**VDS \_ HBAPORT \_ STATUS**](/windows/desktop/api/Vds/ne-vds-vds_hbaport_status)、 [**VDS \_ HBAPORT \_ SPEED \_ 旗**](/windows/desktop/api/Vds/ne-vds-vds_hbaport_speed_flag)標。 |
| 相關聯的結構                             | [**VDS \_HBAPORT 的 \_ 主張**](/windows/desktop/api/Vds/ns-vds-vds_hbaport_prop)。                                                                                                                  |



 

**\* Windows server 2003：** 在 Windows server 2003 R2 之前，不支援此介面。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[VDS 物件模型](vds-object-model.md)
</dt> <dt>

[**IVdsServiceLoader::LoadService**](/windows/desktop/api/Vds/nf-vds-ivdsserviceloader-loadservice)
</dt> <dt>

[正在載入 VDS](loading-vds.md)
</dt> <dt>

[**IVdsService：： GetObject**](/windows/desktop/api/Vds/nf-vds-ivdsservice-getobject)
</dt> <dt>

[VDS 通知](vds-notification-model.md)
</dt> </dl>

 

 
